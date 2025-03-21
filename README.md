# Real-Time-Process-Monitoring-Dashboard
Create a graphical dashboard that displays real-time information about process states, CPU usage, and memory consumption. The tool should allow administrators to manage processes efficiently and identify potential issues promptly
With the help of Python library like pands, numpy, matplotetc.
A sample of code is given as:-
def check_computer_health():
    processor_busy = psutil.cpu_percent(interval=1)
    memory_status = psutil.virtual_memory()
    memory_used = memory_status.percent
    running_tasks = []
    for task in psutil.process_iter(['pid', 'name', 'cpu_percent', 'memory_percent']):
        running_tasks.append(task.info)
    computer_stats = {
        'processor_busy': processor_busy,
        'memory_used': memory_used,
        'running_tasks': running_tasks
    }
