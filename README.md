
```python
 def myLife(courseWorkLoad, caffeineLevel: int = 100, hoursOfSleep : int = 5) -> str:
    """
    A function to describe a my life based on caffeine intake, hours of sleep, and course workload.
    
    Args:
    - caffeineLevel (int): The current level of caffeine in my system.
    - hoursOfSleep (int): The number of hours I managed to sleep.
    - courseWorkLoad (str): The intensity of my coursework. Can be 'Low', 'Medium', or 'High'.
    
    Returns:
    - str: An insightful message about my life.
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
    
    return f"{message}"

life_status = myLife(caffeineLevel=60, hoursOfSleep=6, courseWorkLoad="Medium")
print(life_status)

