# Chapter 1: What Are Commands?

Just to warn you, these first 2 chapters are very dense with information; which might be a turnoff for most, but it will make typing commands *much easier*.

### Definition

To understand what a command is, we have to look outside of Minecraft, but just for a moment.

A command, in it's simplest form, is a message that performs an instruction depending on what arguments (if any) are passed in; that's it. To understand more what I'm saying here, take this command that is usable with in the *Command Prompt* app on Windows, or BASH if you don't use Windows:
```bat
echo Hello 
```
As you can see, this command only has 2 parts: an instruction and an argument. The instruction here, or `echo`, tells the program what action to do; in this case, `echo` will output a message.

The argument, or `Hello`, is a value that is passed in to the program; this argument tells the program what message to output.

### Typing a command

Before learning anything new, we should start by writing your first command: `/say`, which writes text to the chat as if you're saying it. 

Let's say you want to write the message "Hello World!" To do so, open the chat and type the following:
```
/say Hello World!
```

If done correctly, you should see following in chat:
```
[your username] Hello World!
```

Now that you've typed out your first command, it's necessary to know what you wrote down; and, in the future, learn how that applies to other commands.
### How commands are structured

Every command has a set of rules called a syntax, that tells you how a command is to be formed. If it's formed incorrectly - even by one character - the command will fail and have to be corrected. This is why it's important to learn the *structure* of syntax, which is what this section is about.

One rule is that **all** commands start with a forward slash (`/`)

The *syntax*, or the rules, for the `/say` command looks like this:
```
/say <message>
```
Lines of syntax can be separated into *entries*, which are these phrases that are separated by spaces. To understand what these entries can represent, here are the rules for entries:
- Entries written in plain text must be written exactly as shown
- Entries surrounded with angle brackets (`<>`) are arguments, with the text inside indicating its purpose
- Entries surrounded in square brackets are **optional**, and not needed to run the command
  - Optional entries can either be as-is (e.g. `[plain text]`) or arguments (e.g. `[<argument>]`)
- Entries surrounded in parentheses with options separated with vertical lines (e.g. `(entry1|entry2|entry3)`) are required to run, but only one of the list entries can be picked.
  - If you replace the parentheses with square brackets  (e.g. `[entry1|entry2|entry3]`), the entry becomes optional

In this example, `/say` is plain text, so it goes unchanged. `<message>` is the argument in the command, and you'll learn what *exactly* that means in a second, just let me explain myself.

### Arguments and Flexibility in commands

To more fully grasp what arguments are, Let's now compare the syntax to the command you wrote:
```
/say <message> - syntax
/say Hello World! - your command
```
Here, we can make the observation that our message `Hello World!` **replaced** the `<message>` argument from the syntax.
Therefore, an argument tells the command the *expected* value of information, where the typer is expected to give it. This explanation fits best because arguments can *fail* if it isn't the right data type. 

Speaking of data types, we will be moving onto to argument data types in the next chapter.
