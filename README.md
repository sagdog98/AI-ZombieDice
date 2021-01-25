# AI-ZombieDice
You are to provide two JavaTM functions, implemented as static methods of the provided Eval class. Your provided JavaTM source code must be compatible with a collection of provided JavaTM classes that implement a two-player version of the Zombie DiceTM game.

You are to provide the following two static functions:

 -static double value_roll_hand (State s, int depth)
This static function returns a real-valued evaluation of the quality of the given state of play, s. In general, this value is positive if the state is good for the computer player and negative if the state is good for the human user. This function assumes that the given state is one in which the player whose turn it is has already drawn a handful of dice from the dice cup and is about to roll them. Thus, the function must calculate the expected utility of the state by considering every possible outcome of the dice roll and the resulting utility value of each of those possible outcomes. The utility values of the outcomes are to be calculated using the minimax algorithm for game-tree search, looking ahead to recursively calculate the expected utility values of the potential future outcome states. You need not implement this look-ahead process, however, as a provided function called value rolled hand already calculates the expected utility of a game state in which the dice have already been rolled. The depth argument to this function, recording the depth of the look-ahead search, need only be passed on to any calls to value rolled hand.

    
  -static public double heuristic (State s)
This static function returns a real-valued evaluation of the quality of the given state of play, s. This function should not perform any game-tree search in order to determine this value, however. Instead, it should quickly calculate a heuristic estimate of the quality of the current state of play. This function is used to evaluate non-terminal states at the maximum depth of the game tree. As before, the evaluation value should be positive if the state is good for the computer player and negative if the state is good for the human user. The function should handle any valid state of play.
