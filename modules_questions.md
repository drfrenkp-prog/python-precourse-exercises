# Modules & Imports - Short Answer Questions

**What is a module?**
A module is a Python file containing reusable code (usually functions) that can be imported and used in other Python files. It's like a toolbox — a file full of tools (functions) that can be reached into from other files, whether the module is one you wrote yourself or a built-in one like `random` or `math`.

**List three ways to import a module in Python.**
1. `import module_name` — import the whole module
2. `from module_name import specific_thing` — import just one piece of it
3. `import module_name as nickname` — import the whole module, but give it a shorter name

**What is the purpose of importing?**
Importing lets you reuse code instead of rewriting it every time you need it. It also allows you to organize large projects into separate, logical files (e.g. `helpers.py`, `app.py`), and to use code that other people have already written and published (e.g. `random`, `math`, `pandas`).

**List three examples when you would use the random module.**
1. Games — rolling a dice, shuffling cards, spawning a random enemy
2. Testing/sampling data — randomly selecting a sample of rows from a large dataset
3. Simulations — e.g. simulating coin flips or dice rolls to study probability

**What is an ImportError?**
An `ImportError` occurs when Python cannot find or load something you are trying to import — either because the module itself doesn't exist/isn't installed, or because the specific function/object you're trying to import doesn't exist inside that module.

**When would using an OrderedDict be useful?**
When you want to pull data back out in the exact order it was originally added — for example, a step-by-step process log or a ranking/leaderboard where insertion order matters. (Note: as of Python 3.7+, regular dictionaries already preserve insertion order, so `OrderedDict` is less necessary today than in older versions of Python, but the concept is still useful to recognize.)

**When would using a defaultdict be useful?**
When building up counts, groups, or lists inside a dictionary and you don't want to manually check "does this key already exist?" every time. For example, counting how many times each word appears in a sentence — a `defaultdict(int)` automatically starts any new key at 0, instead of raising a `KeyError`.

**What is the purpose of the following code:**
```python
if __name__ == '__main__':
    pass
```
This checks whether the current file is being run directly (in which case `__name__` equals `'__main__'`) versus being imported by another file (in which case `__name__` equals the file's own name). The code inside the `if` block only runs when the file is executed directly, not when it's imported. `pass` is a placeholder meaning "do nothing" — used here as scaffolding for logic that would be added later.
