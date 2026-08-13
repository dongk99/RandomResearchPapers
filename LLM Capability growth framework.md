First, identify what the topic of the conversation is.

Assess the topic's depth first. Then classify whether the user is learning through Claude/AI or delegating the task to it (automation/delegation), and save that label.

Assess how much the user coached Claude and gave it feedback (a subagent can handle this — have it report on the turn-based structure, whether the user coached / gave directives or just vented anger, and what was done with subagents).

Check whether that individual has previously talked with Claude about the topic behind that task.

Check whether that task overlaps with the task they're currently doing.

If yes: determine whether the task has become more advanced, has not, or is a derivative task (a different function of the same task). (Have it write down the reasoning as well.)

If no: check whether the current task directly or indirectly requires information or knowledge from the previous task (for example, in coding, writing pseudocode with if/for/while loops requires prior knowledge or derivative logic).

If it does: check whether the user directly used that knowledge in their prompting.

If the knowledge is required, assume capability has increased (since the prompting requires that prior knowledge, and if they understood it, they'd be giving the model direction).

If it's absent: assume no capability growth occurred.

Strip user information (name, task specifics — e.g., the name of the game if it's a game project), then run an ONET filter to find the best-matching occupational field vector (the way AEI did it). Task classification gets coarse-bucketed that way, which handles anonymization. Then you can claim: "x amount of users in this ONET category have grown their capability."

Privacy-Keeping version 
(Likely used at scale, after small controlled study for looking at effectiveness and after implementation of modular course pipeline): 
Strip User information, but tag if users are taking some sort of fluency course (self-reported via survey or extracted from conversation and then saved locally, then pushed alongside with conversation data to CLIO).

Group de-tagged individual users using O*net classifier and add a new axis (how many people are taking fluency course or not). then track augmentation/automation/directive/learning behavior over time. If needed, Wall-time, token usage & task success ratios can be tracked alongside to measure capability growth.
