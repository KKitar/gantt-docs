onAfterTaskMove
=============
@short:fires after a task was moved to a new position
	


@params: 
- sid			string, number				the id of the task to move
- tindex		number						the index of the position that the task will be moved to <br> (the index in the whole tree)
* parent		string, number				the parent id. If specified, the <b>tindex</b> will  refer to the  index in the <br> <b>'parent'</b> branch


@example:
//prevent moving to another sub-branch
gantt.attachEvent("onAfterTaskMove", function(id, parent, tindex){
	//any custom logic here
});


@relatedapi: 
	api/gantt_movetask.md
	api/gantt_onbeforetaskmove_event.md
@template:	api_event
@descr:
Note, the event fires in 2 cases:

1. While calling the method api/gantt_movetask.md 
2. While the option api/gantt_order_branch_config.md is enabled and a user drags tasks 

