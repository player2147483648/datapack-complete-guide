# Chapter 1: What Are Commands?

Just to warn you, all of the chapters in this book are very *dense* with information. To combat this, the chapters are quite short, and there will be more of them.

### Definition

To understand what a command is, we have to look outside of Minecraft, but just for a moment.

A command, in it's simplest form, is a message that tells a program or interpreter to perform an instruction; that's it. To understand more what I'm saying here, take this command that is usable with in the *Command Prompt* app on Windows, or BASH if you don't use Windows:
```bat
echo Hello 
```
As you can see, this command, or message, has 2 parts: an instruction and an argument. The instruction here, or `echo`, tells the program what action to do; in this case, `echo` will output a message.

The argument, or `Hello`, is a value that is passed in to the program; this argument tells the program what message to output. You'll understand this concept more by the end of the chapter.

---

### Typing a command

Before learning anything new, we should start by writing your first command: `say`, which writes text to the chat as if you're saying it. 

Let's say you want to write the message "Hello World!" To do so, open the chat and type the following:
```
/say Hello World!
```

If done correctly, you should see following in chat:
```
[your username] Hello World!
```

> [!NOTE]
>
> When typing commands in chat, **always** use a forward slash (`/`)!
>
> The forward slash is only used for commands typed inside of chat, but goes unused when inside Datapacks and *Command Blocks*. I will refer commands by their names *without* the slash, and indicate commands typed in chat with a slash.

Now that you've typed out your first command, it's necessary to know what you wrote down; and, in the future, learn how that applies to other commands.

---

### How commands are structured

Every command has a set of rules called a syntax, that tells you how a command is to be formed. If it's formed incorrectly - even by one character - the command will fail and have to be corrected. This is why it's important to learn the *structure* of syntax, which is what this section is about.

The *syntax*, or the rules, for the `say` command looks like this:
```
/say <message>
```
> [!NOTE]
>
> The slash will, for consistency sake, also appear in syntax definitions.

Command syntax can be separated into *terms*, which are individual rules of the syntax. To understand what these terms can represent, here are the rules for these term:
- Terms written in plain text must be written exactly as shown;
- Terms surrounded with angle brackets (`<>`) are *arguments*, with the text inside briefly explaining its purpose;
- Terms surrounded in square brackets are **optional**, and not needed to run the command;
  - Optional terms can either be written as-is (e.g. `[plain text]`) or can accept arguments (e.g. `[<argument>]`);
- Terms surrounded in parentheses with options separated with vertical lines (e.g. `(entry1|entry2|entry3)`) are required to run, but only one of the listed options can be picked;
  - If you replace the parentheses with square brackets  (e.g. `[entry1|entry2|entry3]`), the term becomes optional.

In this example, there are 2 terms: `say` and `<message>`. `say` is plain text, so it goes unchanged. `<message>` is surrounded in angle brackets (`<>`), so it's an *argument*; you'll learn what *exactly* that means in a second, just let me explain myself.

--- 

### Arguments and Flexibility in commands

To more fully grasp what arguments are, Let's now compare the syntax to the command you wrote:
```mcfunction
/say <message>
/say Hello World!
```
Here, we can make the observation that our message `Hello World!` **replaced** the `<message>` argument from the syntax. You also learned earlier that arguments are values *passed in* to a program or interpreter.

From here, it's easy to understand that an argument tells the command the *expected* value of information, where **the user is expected to give it**. In other words, `<message>` could be anything the user wants; `I love pizza!`, `1 + 1` and `abc123` are all valid values for this argument. However this doesn't apply to **all** arguments, as you'll learn right here.

### Argument datatypes

Before moving on to the next chapter, let's look at the syntax of this **fake** command, which adds two numbers, and prints the result in chat. Note that this command **has never existed within Minecraft**, and is only used here to convey an example:
```
/add <number> <otherNumber>
```

If you replaced `<number>` with say 5, and `<otherNumber>` with say 7.5 (e.g. `/add 5 7.5`), that would make sense - you're adding 2 real numbers; and the command would run as normal. But what if number **wasn't** an actual number, and instead 'pizza'? You can't add 7.5 to the word 'pizza' like with the number 5, so the command would fail and print an error. This is because the arguments here expect a numeric value, but got words or phrases instead. Thus, the *datatype* of these arguments, is a *number*.

A datatype is the **type of value** that an argument expects to receive, like a number, word, item, block, etc. It's not always this clear what the specific requirements of an argument could be; for example the `<message>` argument: the word 'message' doesn't fully explain what you can type here.

Just to reassure you, every command you learn in this book will have its arguments' datatype and purpose explained to you.

---

### Summary

In this chapter (or by next), you should have:
- Learned to run commands inside of the chat;
- Grasped what syntax means when it comes to commands;
- Understood how differently formatted terms can change the term's type and relevance;
- Understood what arguments are for; and
- Learned that arguments can have limitations, depending on the target *datatype*.

The next chapter will focus on some basic argument datatypes, while learning some other commands.