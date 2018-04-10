package com.example.samuel.tictactoe;

/**
 * Created by SAMUEL on 4/10/2018.
 */

import java.util.Random;

public class TicTacScreenGameObject2 {

    private char mBoard[];
    private final static int BOARD_SIZE2 = 25;

    public static final char PLAYER_ONE = 'X';
    public static final char PLAYER_TWO = '0';
    public static final char EMPTY_SPACE = ' ';
    private Random mRand;

    public static int getBoardSize2(){

        return BOARD_SIZE2;
    }

    public TicTacScreenGameObject2(){
        mBoard = new char[BOARD_SIZE2];
        for (int i = 0 ; i< BOARD_SIZE2;i++){
            mBoard[i] = EMPTY_SPACE;
            mRand = new Random();
        }
    }

    public void clearrBoard2(){
        for(int i =0;i<BOARD_SIZE2;i++){
            mBoard[i] = EMPTY_SPACE;
        }
    }

    public void setMove2(char player, int location){
        mBoard[location] = player;
    }


    public int getComputerMove2(){

        for(int i = 0 ; i < getBoardSize2() ;i++){

            if(mBoard[i] != PLAYER_ONE && mBoard[i] != PLAYER_TWO){
                char curr = mBoard[i];
                mBoard[i] = PLAYER_TWO;
                if(checkforWinnerForFive()==3){
                    setMove2(PLAYER_TWO,i);
                    return i;
                }
                else{
                    mBoard[i] = curr;
                }
            }
        }
        /**
         Check to see if there is a move Player O can make to prevent X from winnng
         */
        //Loop through the board size
        for(int i = 0 ; i < getBoardSize2(); i++){
            //if no move have being made in any of the boxes
            if(mBoard[i] != PLAYER_ONE && mBoard[i] != PLAYER_TWO){
                //hold the 'X' and 'O' character in the curr variable
                char curr = mBoard[i];
                //set the first move to be player one
                mBoard[i] = PLAYER_ONE;
                //if the player is about to win the game
                if(checkforWinnerForFive()==2){
                    //Player two can make a move to block
                    setMove2(PLAYER_TWO,i);
                    return i;
                }
                else{
                    mBoard[i] = curr;
                }

            }
        }
        //Generate Random move
        do
        {
            move_for_five = mRand.nextInt(getBoardSize2());
        } while (mBoard[move_for_five] == PLAYER_ONE || mBoard[move_for_five] == PLAYER_TWO);

        setMove2(PLAYER_TWO, move_for_five);
        return move_for_five;

    }
    int move_for_five;


    public int checkforWinnerForFive(){
        //check for horizontal wins
        for(int i = 0 ; i < 10 ; i++){
            if(mBoard[i] == PLAYER_ONE && mBoard[i + 1]==PLAYER_ONE && mBoard[i + 2]==PLAYER_ONE && mBoard[i + 3]==PLAYER_ONE && mBoard[i + 4]==PLAYER_ONE){
                return 2;
            }
            if(mBoard[i] == PLAYER_TWO && mBoard[i + 1]==PLAYER_TWO && mBoard[i + 2]==PLAYER_TWO && mBoard[i + 3]==PLAYER_TWO && mBoard[i + 4]==PLAYER_TWO){
                return 3;
            }
        }

        //check for vertical wins
        for(int i =0 ; i < 5 ; i++){
            if(mBoard[i]==PLAYER_ONE && mBoard[i + 5]==PLAYER_ONE && mBoard[i + 10]==PLAYER_ONE && mBoard[i + 15]==PLAYER_ONE && mBoard[i + 20]==PLAYER_ONE ){
                return 2;
            }
            if(mBoard[i]==PLAYER_TWO && mBoard[i + 5]==PLAYER_TWO && mBoard[i + 10]==PLAYER_TWO && mBoard[i + 15]==PLAYER_TWO && mBoard[i + 20]==PLAYER_TWO ){
                return 3;
            }



        }

        //check for diagonal wins
        for(int i =0; i<25;i++ ){
            if(mBoard[i]==PLAYER_ONE && mBoard[i + 6]==PLAYER_ONE && mBoard[i + 12]==PLAYER_ONE && mBoard[i+18]==PLAYER_ONE && mBoard[i + 24]==PLAYER_ONE) {
                return 2;
            }
            if(mBoard[i + 4]==PLAYER_ONE && mBoard[i + 8]==PLAYER_ONE && mBoard[i + 12]==PLAYER_ONE && mBoard[i+16]==PLAYER_ONE && mBoard[i + 20]==PLAYER_ONE) {
                return 2;
            }
            if(mBoard[i]==PLAYER_TWO && mBoard[i + 6]==PLAYER_TWO && mBoard[i + 12]==PLAYER_TWO && mBoard[i+18]==PLAYER_TWO && mBoard[i + 24]==PLAYER_TWO) {
                return 3;
            }
            if(mBoard[i + 4]==PLAYER_TWO && mBoard[i + 8]==PLAYER_TWO && mBoard[i + 12]==PLAYER_TWO && mBoard[i+16]==PLAYER_TWO && mBoard[i + 20]==PLAYER_TWO) {
                return 3;
            }

        }
        //Check for a tie
        for(int i =0;i<BOARD_SIZE2;i++){
            if(mBoard[i]!=PLAYER_ONE && mBoard[i]!=PLAYER_TWO){
                return 0;
            }
        }
        // If we make it through the previous loop, all places are taken, so it's a tie
        return 1;
    }


}
