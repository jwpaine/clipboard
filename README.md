```
function mapeStateToProps(state) {
	return { 
		errorMessage: state.create.errorMessage,
		place: state.place,
		initialValues : {
			place: state.place
		}
	}
}

export default compose(
	connect(mapeStateToProps, actions),
	reduxForm({ form: 'createCategory'})
)(requireAuth(Manage));
```