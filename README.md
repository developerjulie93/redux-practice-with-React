# redux-practice-with-React
Make logic about state updating with redux.



ERROR
---------------------------
before)

export default connect(
    state => ({
        number: state.counter.number,
    }),
    {
        increase,
        decrease,
    },
)(CounterContainer);


after)

export default connect(
    state => ({
        number: state.number,
    }),
    {
        increase,
        decrease,
    },
)(CounterContainer);


because we didn't import counter(from modules)
