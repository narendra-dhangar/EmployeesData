# Create a dictionary of 5 employees
employees = {
    1: {'name': 'Alice', 'age': 30, 'department': 'HR'},
    2: {'name': 'Bob', 'age': 24, 'department': 'Engineering'},
    3: {'name': 'Charlie', 'age': 35, 'department': 'Marketing'},
    4: {'name': 'David', 'age': 29, 'department': 'Sales'},
    5: {'name': 'Eve', 'age': 32, 'department': 'Engineering'}
}

print("Original Employees Dictionary:")
for emp_id, emp_data in employees.items():
    print(f"  ID: {emp_id}, Data: {emp_data}")

# 1. Print all names
print("\n1. All Employee Names:")
for emp_id in employees:
    print(employees[emp_id]['name'])

# 2. Find the average age
total_age = 0
for emp_id in employees:
    total_age += employees[emp_id]['age']
average_age = total_age / len(employees)
print(f"\n2. Average Employee Age: {average_age:.2f}")

# 3. Add a new employee
next_id = max(employees.keys()) + 1 if employees else 1
employees[next_id] = {'name': 'Frank', 'age': 28, 'department': 'IT'}
print(f"\n3. Added new employee 'Frank'. Updated Employees Dictionary:")
for emp_id, emp_data in employees.items():
    print(f"  ID: {emp_id}, Data: {emp_data}")

# 4. Remove one employee (e.g., Bob with ID 2)
if 2 in employees:
    removed_employee = employees.pop(2)
    print(f"\n4. Removed employee '{removed_employee['name']}'. Updated Employees Dictionary:")
else:
    print("\n4. Employee with ID 2 not found.")

for emp_id, emp_data in employees.items():
    print(f"  ID: {emp_id}, Data: {emp_data}")
