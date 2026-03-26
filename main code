print("----- STUDY WEAKNESS ANALYZER -----\n")

# Just using simple lists for everything
names = []
marks = []
diffs = []

# Ask for total subjects
n = int(input("How many subjects do you have? "))

# Input loop
for i in range(n):
    print("\nSubject " + str(i+1))
    s_name = input("Name: ")
    s_marks = float(input("Marks (out of 100): "))
    s_diff = int(input("Difficulty (1-5): "))
    
    names.append(s_name)
    marks.append(s_marks)
    diffs.append(s_diff)

# Logic for study hours: (100 - marks) * difficulty / 50
# Basically, lower marks + high difficulty = more time
temp_h = []
for i in range(n):
    val = (100 - marks[i]) * diffs[i] / 50
    temp_h.append(val)

# Normalize to a 6-hour study day
total_temp = sum(temp_h)
final_h = []
for h in temp_h:
    # Scale it so the total is exactly 6 hours
    final_h.append((h / total_temp) * 6)

print("\n" + "="*30)
print("     ANALYSIS RESULT")
print("="*30)

# Finding the weakest subject manually
low_score = 101
worst_sub = ""

for i in range(n):
    # Manual classification
    if marks[i] < 50:
        lab = "Weak"
    elif marks[i] < 70:
        lab = "Average"
    else:
        lab = "Strong"
    
    # Track the lowest one
    if marks[i] < low_score:
        low_score = marks[i]
        worst_sub = names[i]
        
    print(names[i] + " | Marks: " + str(marks[i]) + " | Status: " + lab)

print("\n ALERT: You really need to focus on " + worst_sub.upper())

print("\n----- PREDICTED MARKS BOOST -----")
# Logic: Every hour of study adds 2 marks to the score
for i in range(n):
    boost = marks[i] + (final_h[i] * 2)
    # Cap it at 100 max
    if boost > 100: 
        boost = 100
    print(names[i] + ": Now " + str(marks[i]) + " -> After Study: " + str(round(boost, 1)))

# Making a text-based bar chart using symbols
print("\n----- PERFORMANCE GRAPH -----")
for i in range(n):
    # One block for every 10 marks
    blocks = "█" * int(marks[i] // 10)
    print(names[i].ljust(10) + ": " + blocks + " (" + str(marks[i]) + ")")

print("\n----- DAILY STUDY PLAN -----")
for i in range(n):
    print("- " + names[i] + ": " + str(round(final_h[i], 2)) + " hours")

print("\nDone! Follow this and you'll improve for sure. ") 
