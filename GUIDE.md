1. Set initial redux state to lyric array and array position 0.
2. Create userClick function and attach to html.
3. Create store with reducer as an argument.
4. Write test expecting reducer to return intialState.
5. Write reducer to take intialState, action as arugments.
6. Write test expecting reducer to have NEXT_LYRIC action type and arrayPosition of 1.
7. Write reducer to take initialState, NEXT_LYRIC as arguments using switch statement to set state to have updated arrayPosition, else return state.
8. Write renderLyrics function and call on window object on load.
9. Dispatch NEXT_LYRIC action on user click to advance array position in state
10. Subscribe to changes in store using subscribe() with renderLyrics as an argument to render arrayPosition string as it changes with user click.
11. Write test expecting reducer to have RESTART_SONG action type, arrayPosition of 1 and to equal initialState.
12. Modify reducer to define newState before the switch, and include both actions with different values for newState returned.
13. Dispatch RESTART_SONG on user click inside conditional logic based on arrayPosition in relation to songLyricsArray.length.


## Store: holds and mutates state
```
const {createStore} =  Redux;
const store = createStore(reducer);
```


## REDUCER
example:
```
const reducer = (state = initialState, action) => {
  let newState;
  switch (action.type) {
    case 'ACTION_ONE':
      // any necessary logic
      newState = {
        firstStateItem: state.firstStateItem,
        secondStateItem: state.secondStateItem,
        stateItemBeingChanged: action.newUpdatedStateValue,
      }
      return newState;
    case 'ACTION_TWO':
      // any necessary logic
      newState = {
        firstStateItem: state.firstStateItem,
        secondStateItem: state.secondStateItem,
        stateItemBeingChanged: action.differentUpdatedStateValue,
      }
      return newState;
    default:
      return state;
  }
}
```

_Structuring Advanced Redux State_
1. Reorganize state store to include two song objects with keys.
2. Restructure state, reducers, and tests to work with the two state slices. Write a reducer for selecting the current song by id.
