Unscheduled Tasks
========================

There's a possibility to add tasks without dates into the Gantt chart.

<img src="desktop/unscheduled_tasks.png" style="display:block; margin:0 auto;">

It can be implemented by setting the *unscheduled* parameter with the value *true* in the task's description:

~~~js
{"id":11, "text":"Project #1", type:gantt.config.types.project, "progress": 0.6, 
	"open": true},
   {"id":14, "text":"Task #1", unscheduled:false, "start_date":"02-04-2013", 
   		"duration":"6", "parent":"11"},
   {"id":17, "text":"Task #2", unscheduled:true,  "start_date":"", 			 
   		"duration":"", "parent":"11"}
~~~

Thus, the task with the id "17" will be added to the gantt without the start date and displayed as an empty row.

In order to display unscheduled tasks, use the config parameter api/gantt_show_unscheduled_config.md set to *true*:

~~~js
gantt.config.show_unscheduled = true;
~~~

{{sample
01_initialization/19_tasks_without_dates.html
}}
