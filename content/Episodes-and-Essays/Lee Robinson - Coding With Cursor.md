---
title: "Lee Robinson: Coding With Cursor"
type: podcast
show: How I AI
guest: Lee Robinson
source: https://share.snipd.com/episode/b87eb2c0-d4eb-470c-af9e-21cf8d349470
---

A practical guide to using AI code editors effectively.

---

## Improving Code with AI

- Once you have the first version of your application or a working prototype, open it in Cursor to make sense of the code.
- Leverage traditional software engineering tools to make your code more resilient to errors and help AI models fix them.
- Use a typed language like TypeScript for web development.
- Implement linters to enforce coding standards and identify potential errors based on past developer experiences.
- Set up a formatter to automatically format your code consistently.
- Setting up tests to validate code ensures that changes don't introduce errors and allows AI to fix failing tests by reading their output.

> **Lee Robinson:** There are tools that you can take from traditional software engineering, how software is built, and apply them to make your code more resilient to errors and help the AI models fix errors for you. So if you think about this agent on the right, the agent can only work with the information that we provide it, the context that we provide it. So if it doesn't know how to basically read its own outputs or read its information about the code base, it's a lot harder for it to fix errors for you.

> **Lee Robinson:** I'd recommend three or four of these for any code base that you're setting up. One is to use a typed language. So in the instance of the web, this is TypeScript usually. Two is to use linters. So linters are going to opinions about the way that you write code and usually will help you find and fix errors along the way based on things that developers have stumbled on in the past. The third is to set up a formatter. So it just automatically puts your code into the right formatting, which then you just never have to think about it. And the last one is test.

---

## Cursor's AI Agent Fixes Lint Errors

- Lee Robinson demonstrates how Cursor's AI agent automatically fixes lint errors.
- He uses the command 'fix the lint errors' without complex prompts, leveraging the AI's ability to read and search the codebase.
- The agent identifies issues, such as the use of 'any' type, and automatically applies code changes.
- It then reruns the command to verify the fixes, ensuring code quality and saving the developer time and effort.
- Claire Vo highlights that this process helps new coders to learn by reviewing the changes.

> **Lee Robinson:** I can say, fix the lint errors. And you'll notice I'm not typing a very complex prompt. I'm not giving it a ton of information. The nice thing about AI agents is they can go read things for you. Cursor and other tools basically give the AI agents skills, and we've given them the skill to go read files in your code base and search files in your code base and run a bunch of commands for you.

> **Lee Robinson:** So when I say fix the lint errors, it knows that it can go run a terminal command. So if you've used the terminal before, maybe you haven't used the terminal before, it's like this kind of scary looking place where you can run all these strange commands and do lots of things for you. And you don't have to learn any of that right away. You can ask the agent to teach you how to use terminal commands.

> **Lee Robinson:** And I think this is a really interesting thing, which is that I didn't have to go tell the agent to do anything. It's like, rather than giving you step-by instructions, you're just putting the thing into the GPS and it just figures it out along the way. And at the end, it says, great, we fixed all the errors for you. Here's what we did.

> **Claire Vo:** For people that are really new to coding, and I know many of you out there listening are, that's the way to like read the code and learn. And so it's one of the things that, again, I like about this kind of recursive human in the loop process with cursor is now I know run run lint. Now I know if I want to run lint and I want to get really fancy, I can open up the terminal and cursor and run that function myself.

---

## Custom Rules and Commands

- Create custom rules in your code editor to codify corrections for recurring AI model errors.
- Define specific commands within the editor to automate tasks like code review.
- Use the editor's menu to forward information like Git branches and specific commits to the AI agent.
- Leverage the "@" menu for quick access to files and functions within your code.

> **Lee Robinson:** One thing I found just in general is when I see a model do the wrong thing or something that I did not want two or three times, it's like okay this is probably time for me to notice this hint and kind of pull that out into a custom rule. And rules are just a way for you to codify the places where the models went wrong and actually I want it to work this way in the future.

> **Lee Robinson:** One thing that's really interesting is kind of a newer feature of cursor is, let's say I have the agent open, I can define specific commands. And one of my commands is code review. So if I do code review, I can actually run this over all of my code. And I define that command inside of this folder. And I've just been slowly building this prompt as I kind of go along with some things that are worth checking out.

> **Lee Robinson:** So when you have the cursor agent open, you can do the app menu and the app menu gives you all of this different stuff that you can basically forward to the AI model, forward to the agent. And one of those is Git. So maybe you want the branch, maybe you want the specific commits. The branch is basically all of my working changes on this thing that I'm doing. And then the commit is like one specific change.

---

## Separate Chats for Focused Tasks

- Create new chats for specific features in Cursor to avoid context bloat and maintain quality.
- Plan and provide the agent with necessary context for each specific task.
- Avoid derailing the agent with one-off questions unrelated to the primary workflow.
- For questions like "how do I run Lintz?", start a separate chat or use a different agent.
- This helps maintain a cleaner, more focused path for each task.

> **Lee Robinson:** So what I try to recommend to people is to make new chats for just street features. So sometimes that requires a little bit more planning, a little bit more context that you want to give to the agent, but it does help get better quality, I think.

> **Claire Vo:** The other tip I would give to people is I often think about my agents having to contact switch the same as humans have to contact switch and the cost of that. And sometimes, you know, I'm doing a task and I'll think, oh, wait, how do I run Lintz again, for example? And I can throw into that chat, how do I run Lintz? But again, I'm like taking the agent off the golden path of what we're trying to do. And so sometimes for those one-off questions that are related but not core to a workflow, I try to just kick off a one-off chat to answer them or a separate agent, just to sort of keep that single path cleaner.

---

## LLM Writing Patterns

- LLMs, especially specific models, exhibit their own writing ticks.
- A recent pattern Lee Robinson noticed is the phrase 'it's not just X, it's Y'.
- Though models are trained on good writing, unintended meme-like patterns emerge.
- Identify common AI-generated writing patterns to make your content stand out.

> **Lee Robinson:** I have noticed that, you know, LLMs have, especially specific models, all have their own little ticks or things that they do. For a while, it was, they would always output markdown lists with like the same formatting. It was really annoying because you could always tell it was LLM generated. There was, of course, Delve. The most recent one that I've seen is actually this phrase of, it's not just X, it's Y.

> **Lee Robinson:** It's a very specific way of writing that in some ways, like M dashes is trained on good writing, but in a weird kind of unintended way, then ends up getting memed because so many people did it or so-called good writers did it, right? That now people are like, wait, that seems like an LLM generated thing. And I love M dashes. So it's like, okay, well, I guess I need to change and be very intentional about when I use them. So I built up this list of, you know, little things that kind of just start to feel like an AI generated the code.

---

[Listen to the episode](https://share.snipd.com/episode/b87eb2c0-d4eb-470c-af9e-21cf8d349470)
