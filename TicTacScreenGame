package com.example.samuel.tictactoe;

import android.support.v7.app.AppCompatActivity;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.TextView;
import android.widget.Toast;

import org.w3c.dom.Text;

public class TicTacScreenGame extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_tic_tac_screen_game);
        //Class instantiation for TicTacScreenGameObject class
        mGame = new TicTacScreenGameObject();
        mGame2 = new TicTacScreenGameObject2();
        //Instantintion for the Button array
        mBoardButtons = new Button[mGame.getBOARD_SIZE()];
        mBoardButtons[0] = (Button) findViewById(R.id.one);
        mBoardButtons[1] = (Button) findViewById(R.id.two);
        mBoardButtons[2] = (Button) findViewById(R.id.three);
        mBoardButtons[3] = (Button) findViewById(R.id.sixth);
        mBoardButtons[4] = (Button) findViewById(R.id.seventh);
        mBoardButtons[5] = (Button) findViewById(R.id.eight);
        mBoardButtons[6] = (Button) findViewById(R.id.eleventh);
        mBoardButtons[7] = (Button) findViewById(R.id.twelveth);
        mBoardButtons[8] = (Button) findViewById(R.id.thirteenth);

//instantiation for the button array for getGame    
        mBoardButtons2 = new Button[mGame2.getBoardSize2()];
        mBoardButtons2[0] = (Button)findViewById(R.id.one);
        mBoardButtons2[1]=(Button)findViewById(R.id.two);
        mBoardButtons2[2] = (Button)findViewById(R.id.three);
        mBoardButtons2[3] = (Button)findViewById(R.id.fourth);

        mBoardButtons2[4] = (Button)findViewById(R.id.fifth);
        mBoardButtons2[5]=(Button)findViewById(R.id.sixth);
        mBoardButtons2[6] = (Button)findViewById(R.id.seventh);
        mBoardButtons2[7] = (Button)findViewById(R.id.eight);
        mBoardButtons2[8] = (Button)findViewById(R.id.ninth);
        mBoardButtons2[9]=(Button)findViewById(R.id.tenth);
        mBoardButtons2[10] = (Button)findViewById(R.id.eleventh);
        mBoardButtons2[11] = (Button)findViewById(R.id.twelveth);
        mBoardButtons2[12] = (Button)findViewById(R.id.thirteenth);
increaseBoard = (Button)findViewById(R.id.increase_board);

        mBoardButtons2[13] = (Button)findViewById(R.id.fourteenth);
        mBoardButtons2[14] = (Button)findViewById(R.id.fifteenth);
        mBoardButtons2[15]=(Button)findViewById(R.id.sixteenth);
        mBoardButtons2[16] = (Button)findViewById(R.id.seventeenth);
        mBoardButtons2[17] = (Button)findViewById(R.id.eighteenth);

        mBoardButtons2[18] = (Button)findViewById(R.id.nineteenth);
        mBoardButtons2[19]=(Button)findViewById(R.id.twentyth);
        mBoardButtons2[20] = (Button)findViewById(R.id.twentyth_one);
        mBoardButtons2[21] = (Button)findViewById(R.id.twentyth_two);
        mBoardButtons2[22] = (Button)findViewById(R.id.twentyth_three);
        mBoardButtons2[23]=(Button)findViewById(R.id.twentyth_four);
        mBoardButtons2[24]=(Button)findViewById(R.id.twentyth_five);
        //method call for adding listener to button of 3 by 3
        addListenerOnButton();
//set the other button to visibility false until user decides to increase board
        mBoardButtons2[3].setVisibility(View.GONE);
        mBoardButtons2[4].setVisibility(View.GONE);
        mBoardButtons2[8].setVisibility(View.GONE);
        mBoardButtons2[9].setVisibility(View.GONE);
        mBoardButtons2[13].setVisibility(View.GONE);
        mBoardButtons2[14].setVisibility(View.GONE);
        mBoardButtons2[18].setVisibility(View.GONE);
        mBoardButtons2[19].setVisibility(View.GONE);

        mBoardButtons2[23].setVisibility(View.GONE);
        mBoardButtons2[24].setVisibility(View.GONE);

        // setup the textviews
        mInfoTextView = (TextView) findViewById(R.id.information);
        mPlayerOneCount = (TextView) findViewById(R.id.humanCount);
        mTieCount = (TextView) findViewById(R.id.tiesCount);
        mPlayerTwoCount = (TextView) findViewById(R.id.androidCount);
        mPlayerOneText = (TextView) findViewById(R.id.human);
        mPlayerTwoText = (TextView) findViewById(R.id.android);
        board_size = (TextView)findViewById(R.id.board_size_value);
        // set the initial counter display values
        mPlayerOneCount.setText(Integer.toString(mPlayerOneCounter));
        mTieCount.setText(Integer.toString(mTieCounter));
        mPlayerTwoCount.setText(Integer.toString(mPlayerTwoCounter));

//implementing click listener on board increment
        increaseBoard.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
           addListenerOnButton2();
                boardIncrement();
            }
        });


    }

//Varoius Button and class Declaration
    private Button mBoardButtons[];
    private Button mBoardButtons2[];
    private Button increaseBoard;
    private Button mNewGame;
    private TicTacScreenGameObject mGame;
    private TicTacScreenGameObject2 mGame2;

    // Various text displayed
    private TextView mInfoTextView;
    private TextView mPlayerOneCount;
    private TextView mTieCount;
    private TextView board_size;
    private TextView mPlayerTwoCount;
    private TextView mPlayerOneText;
    private TextView mPlayerTwoText;

    // Counters for the wins and ties
    private int mPlayerOneCounter = 0;
    private int mTieCounter = 0;
    private int mPlayerTwoCounter = 0;

    // Bools needed to see if player one goes first
    // if the gameType is to be single or local multiplayer
    // if it is player one's turn
    // and if the game is over
    private boolean mPlayerOneFirst = true;
    private boolean mIsSinglePlayer = false;
    private boolean mIsPlayerOneTurn = true;
    private boolean mGameOver = false;

//method that handles board increment button action clicked
    private void boardIncrement(){
        board_size.setText("5");
        mBoardButtons2[3].setVisibility(View.VISIBLE);
        mBoardButtons2[4].setVisibility(View.VISIBLE);
        mBoardButtons2[8].setVisibility(View.VISIBLE);
        mBoardButtons2[9].setVisibility(View.VISIBLE);
        mBoardButtons2[13].setVisibility(View.VISIBLE);
        mBoardButtons2[14].setVisibility(View.VISIBLE);
        mBoardButtons2[18].setVisibility(View.VISIBLE);
        mBoardButtons2[19].setVisibility(View.VISIBLE);

        mBoardButtons2[23].setVisibility(View.VISIBLE);
        mBoardButtons2[24].setVisibility(View.VISIBLE);
    }
    
    //method for returning board to normal size
    private void returnBoardToNormal(){
        board_size.setText("3");
        mBoardButtons2[3].setVisibility(View.GONE);
        mBoardButtons2[4].setVisibility(View.GONE);
        mBoardButtons2[8].setVisibility(View.GONE);
        mBoardButtons2[9].setVisibility(View.GONE);
        mBoardButtons2[13].setVisibility(View.GONE);
        mBoardButtons2[14].setVisibility(View.GONE);
        mBoardButtons2[18].setVisibility(View.GONE);
        mBoardButtons2[19].setVisibility(View.GONE);

        mBoardButtons2[23].setVisibility(View.GONE);
        mBoardButtons2[24].setVisibility(View.GONE);
    }

//method for set game move for a 3 by 3
    private void setMove(char player, int location)
    {
        mGame.setMove(player, location);
        mBoardButtons[location].setEnabled(false);
        if (player == mGame.PLAYER_ONE)
            mBoardButtons[location].setBackground(getResources().getDrawable(R.drawable.x));
        else
            mBoardButtons[location].setBackground(getResources().getDrawable(R.drawable.o));
    }

//method for set game move for a 5 by 5
    private void setMove2(char player, int location){
        mGame2.setMove2(player, location);
        mBoardButtons2[location].setEnabled(false);
        if(player==mGame2.PLAYER_ONE){
            mBoardButtons2[location].setBackground(getResources().getDrawable(R.drawable.x));
        }
        else{
            mBoardButtons2[location].setBackground(getResources().getDrawable(R.drawable.o));
        }
    }

//method for adding listener on a button click on a 5 by 5
    public void addListenerOnButton2(){
        mNewGame = (Button)findViewById(R.id.NewGame);
        mNewGame.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                startNewGame2(mIsSinglePlayer);
            }
        });
    }

    //method for adding listener on a button click on a 3 by 3
    public void addListenerOnButton(){

            mNewGame = (Button) findViewById(R.id.NewGame);

            mNewGame.setOnClickListener(new View.OnClickListener() {

                @Override
                public void onClick(View v) {
                    // TODO Auto-generated method stub
                    startNewGame(mIsSinglePlayer);
                }
            });}







//method for handling click action when new game button is clicked for a 5 by 5
    private void startNewGame2(boolean isSingle)
    {

        this.mIsSinglePlayer = isSingle;

        mGame2.clearrBoard2();

        for (int i = 0; i < mBoardButtons2.length; i++)
        {
            mBoardButtons2[i].setText("");
            mBoardButtons2[i].setEnabled(true);
            mBoardButtons2[i].setOnClickListener(new ButtonClickListener(i));
            mBoardButtons2[i].setBackground(getResources().getDrawable(R.drawable.blank));
        }


        if (mIsSinglePlayer)
        {
            mPlayerOneText.setText("Human:");
            mPlayerTwoText.setText("Android:");

            if (mPlayerOneFirst)
            {
                mInfoTextView.setText(R.string.first_human);
                mPlayerOneFirst = false;
            }
            else
            {
                mInfoTextView.setText(R.string.turn_computer);
                int move = mGame2.getComputerMove2();
                setMove2(mGame.PLAYER_TWO, move);
                mPlayerOneFirst = true;
            }
        }
        else
        {
            mPlayerOneText.setText("Player One:");
            mPlayerTwoText.setText("Player Two:");

            if (mPlayerOneFirst)
            {
                mInfoTextView.setText(R.string.turn_player_one);
                mPlayerOneFirst = false;
            }
            else
            {
                mInfoTextView.setText(R.string.turn_player_two);
                mPlayerOneFirst = true;
            }
        }

        mGameOver = false;
    }



//method for handling click action when new game button is clicked for a 5 by 5

    private void startNewGame(boolean isSingle)
    {

        this.mIsSinglePlayer = isSingle;

        mGame.clearBoard();

        for (int i = 0; i < mBoardButtons.length; i++)
        {
            mBoardButtons[i].setText("");
            mBoardButtons[i].setEnabled(true);
            mBoardButtons[i].setOnClickListener(new ButtonClickListener(i));
            mBoardButtons[i].setBackground(getResources().getDrawable(R.drawable.blank));
        }


        if (mIsSinglePlayer)
        {
            mPlayerOneText.setText("Human:");
            mPlayerTwoText.setText("Android:");

            if (mPlayerOneFirst)
            {
                mInfoTextView.setText(R.string.first_human);
                mPlayerOneFirst = false;
            }
            else
            {
                mInfoTextView.setText(R.string.turn_computer);
                int move = mGame.getComputerMove();
                setMove(mGame.PLAYER_TWO, move);
                mPlayerOneFirst = true;
            }
        }
        else
        {
            mPlayerOneText.setText("Player One:");
            mPlayerTwoText.setText("Player Two:");

            if (mPlayerOneFirst)
            {
                mInfoTextView.setText(R.string.turn_player_one);
                mPlayerOneFirst = false;
            }
            else
            {
                mInfoTextView.setText(R.string.turn_player_two);
                mPlayerOneFirst = true;
            }
        }

        mGameOver = false;
    }


    private class ButtonClickListener implements View.OnClickListener {
        int location;

        public ButtonClickListener(int location) {
            this.location = location;
        }

        public void onClick(View view) {
            if (!mGameOver) {
                if (mBoardButtons[location].isEnabled()) {
                    if (mIsSinglePlayer) {
                        setMove(mGame.PLAYER_ONE, location);

                        int winner = mGame.checkForWinner();

                        if (winner == 0) {
                            mInfoTextView.setText(R.string.turn_computer);
                            int move = mGame.getComputerMove();
                            setMove(mGame.PLAYER_TWO, move);
                            winner = mGame.checkForWinner();
                        }

                        if (winner == 0)
                            mInfoTextView.setText(R.string.turn_human);
                        else if (winner == 1) {
                            mInfoTextView.setText(R.string.result_tie);
                            mTieCounter++;
                            mTieCount.setText(Integer.toString(mTieCounter));
                            mGameOver = true;
                        } else if (winner == 2) {
                            mInfoTextView.setText(R.string.result_human_wins);
                            mPlayerOneCounter++;
                            mPlayerOneCount.setText(Integer.toString(mPlayerOneCounter));
                            mGameOver = true;
                        } else {
                            mInfoTextView.setText(R.string.result_android_wins);
                            mPlayerTwoCounter++;
                            mPlayerTwoCount.setText(Integer.toString(mPlayerTwoCounter));
                            mGameOver = true;
                        }
                    } else {
                        if (mIsPlayerOneTurn)
                            setMove(mGame.PLAYER_ONE, location);
                        else
                            setMove(mGame.PLAYER_TWO, location);

                        int winner = mGame.checkForWinner();

                        if (winner == 0) {
                            if (mIsPlayerOneTurn) {
                                mInfoTextView.setText(R.string.turn_player_two);
                                mIsPlayerOneTurn = false;
                            } else {
                                mInfoTextView.setText(R.string.turn_player_one);
                                mIsPlayerOneTurn = true;
                            }
                        } else if (winner == 1) {
                            mInfoTextView.setText(R.string.result_tie);
                            mTieCounter++;
                            mTieCount.setText(Integer.toString(mTieCounter));
                            mGameOver = true;
                        } else if (winner == 2) {
                            mInfoTextView.setText(R.string.result_player_one_wins);
                            mPlayerOneCounter++;
                            mPlayerOneCount.setText(Integer.toString(mPlayerOneCounter));
                            mGameOver = true;
                            mIsPlayerOneTurn = false;
                        } else {
                            mInfoTextView.setText(R.string.result_player_two_wins);
                            mPlayerTwoCounter++;
                            mPlayerTwoCount.setText(Integer.toString(mPlayerTwoCounter));
                            mGameOver = true;
                            mIsPlayerOneTurn = true;
                        }
                    }
                }
                else if(mBoardButtons2[location].isEnabled()){
                    if (mIsSinglePlayer) {
                        setMove2(mGame2.PLAYER_ONE, location);

                        int winner = mGame2.checkforWinnerForFive();

                        if (winner == 0) {
                            mInfoTextView.setText(R.string.turn_computer);
                            int move = mGame2.getComputerMove2();
                            setMove2(mGame2.PLAYER_TWO, move);
                            winner = mGame2.checkforWinnerForFive();
                        }

                        if (winner == 0)
                            mInfoTextView.setText(R.string.turn_human);
                        else if (winner == 1) {
                            mInfoTextView.setText(R.string.result_tie);
                            mTieCounter++;
                            mTieCount.setText(Integer.toString(mTieCounter));
                            mGameOver = true;
                        } else if (winner == 2) {
                            mInfoTextView.setText(R.string.result_human_wins);
                            mPlayerOneCounter++;
                            mPlayerOneCount.setText(Integer.toString(mPlayerOneCounter));
                            mGameOver = true;
                        } else {
                            mInfoTextView.setText(R.string.result_android_wins);
                            mPlayerTwoCounter++;
                            mPlayerTwoCount.setText(Integer.toString(mPlayerTwoCounter));
                            mGameOver = true;
                        }
                    } else {
                        if (mIsPlayerOneTurn)
                            setMove2(mGame2.PLAYER_ONE, location);
                        else
                            setMove2(mGame2.PLAYER_TWO, location);

                        int winner = mGame2.checkforWinnerForFive();

                        if (winner == 0) {
                            if (mIsPlayerOneTurn) {
                                mInfoTextView.setText(R.string.turn_player_two);
                                mIsPlayerOneTurn = false;
                            } else {
                                mInfoTextView.setText(R.string.turn_player_one);
                                mIsPlayerOneTurn = true;
                            }
                        } else if (winner == 1) {
                            mInfoTextView.setText(R.string.result_tie);
                            mTieCounter++;
                            mTieCount.setText(Integer.toString(mTieCounter));
                            mGameOver = true;
                        } else if (winner == 2) {
                            mInfoTextView.setText(R.string.result_player_one_wins);
                            mPlayerOneCounter++;
                            mPlayerOneCount.setText(Integer.toString(mPlayerOneCounter));
                            mGameOver = true;
                            mIsPlayerOneTurn = false;
                        } else {
                            mInfoTextView.setText(R.string.result_player_two_wins);
                            mPlayerTwoCounter++;
                            mPlayerTwoCount.setText(Integer.toString(mPlayerTwoCounter));
                            mGameOver = true;
                            mIsPlayerOneTurn = true;
                        }
                    }


                }
            }
        }
    }
    }
