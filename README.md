
```python
 def myLife(caffeineLevel: int = 100, hoursOfSleep : int = 5) -> str:
    """
    A function to describe my life based on caffeine intake and hours of sleep.
    
    Args:
    - caffeineLevel (int): The current level of caffeine in my system.
    - hoursOfSleep (int): The number of hours I managed to sleep.
    
    Returns:
    - str: An insightful message about my current situation.
    """
    emoji = {
        'stress': '😰',
        'coding': '💻',
        'study': '📚'
    }
    
    workLoads = {
        'Low': f"Enjoying the calm before the storm.{emoji['coding']}",
        'Medium': f"It's getting closer...{emoji['study']}",
        'High': f"Brace yourself, finals are coming!{emoji['stress']}{emoji['study']}"
    }

    if caffeineLevel >= 100 and hoursOfSleep <= 7:
        message = workLoads["High"]

    elif caffeineLevel >= 50 and hoursOfSleep <= 6:
        message = workLoads["Medium"]
    else:
        message = workLoads["Low"]
    
    return message

lifeStatus = myLife()
print(lifeStatus)

