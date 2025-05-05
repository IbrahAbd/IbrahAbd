
```python
def my_life(caffeine=100, sleep=5) -> str:
    if caffeine >= 100 and sleep <= 5:
        return "High workload: running on caffeine and minimal sleep."
    elif caffeine >= 50 and sleep <= 7:
        return "Moderate workload: Getting by."
    else:
        return "Low workload: Rested and focused."

print(my_life())


