import random
from art import logo, vs
from game_data import data


def print_person_a():
    print(f"Compare A: {person_a["name"]}, {person_a["description"]}, from {person_a["country"]}")

def print_person_b():
    print(f"Against B: {person_b["name"]}, {person_b["description"]}, from {person_b["country"]}")

person_a = random.choice(data)
person_b = random.choice(data)
follower_a = person_a["follower_count"]
follower_b = person_b["follower_count"]

print(logo)
print_person_a()
print(vs)
print_person_b()
score = 0
is_continue = True
while is_continue:

    user_answer = input("Who has more followers? Type 'A' or 'B': ").lower()
    if user_answer == "a":
        if follower_a >= follower_b:
            score += 1
            print(f"You're right! Current score: {score}")
            person_a = person_b
            follower_a = follower_b
            person_b = random.choice(data)
            follower_b = person_b["follower_count"]
            print("\n" * 20)
            print(logo)
            print_person_a()
            print(vs)
            print_person_b()
        else:
            print(f"That's wrong! Final score: {score}")
            is_continue = False
    elif user_answer == "b":
        if follower_b >= follower_a:
            score += 1
            print(f"You're right! Current score: {score}")
            person_a = person_b
            follower_a = follower_b
            person_b = random.choice(data)
            follower_b = person_b["follower_count"]
            print("\n" * 20)
            print(logo)
            print_person_a()
            print(vs)
            print_person_b()
        else:
            print(f"That's wrong! Final score: {score}")
            is_continue = False
    else:
        print(f"That's wrong! Final score: {score}")
        is_continue = False
