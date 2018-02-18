1. Set initial redux state to lyric array and array position 0.
2. Create userClick function and attach to html.
3. Create store with reducer as an argument.
4. Write test expecting reducer to return intialState.
5. Write reducer to take intialState, action as arugments.
6. Write test expecting reducer to have NEXT_LYRIC action type and arrayPosition of 1.
7. Write reducer to take initalState, NEXT_LYRIC as arguments using switch statement to set state to have updated arrayPosition, else return state.
8. Write renderLyrics function and call on window object on load.
9. Dispatch NEXT_LYRIC action on user click to advance array position in state
10. Subscribe to changes in store using subscribe() with renderLyrics as an argument to render arrayPosition string as it changes with user click.
