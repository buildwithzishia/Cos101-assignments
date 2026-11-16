def frequency(period):
    if period == 0:
        return "Period cannot be zero"
    return 1 / period

def coulomb_force(q1, q2, r):
    if r == 0:
        return "Distance cannot be zero"
    return 8.99e9 * q1 * q2 / r**2

def potential_energy(m, h):
    return m * 9.8 * h

def kinetic_energy(m, v):
    return 0.5 * m * v**2

def momentum(m, v):
    return m * v


while True:
    print("\nPhysics Calculator")
    print("1. Frequency")
    print("2. Coulomb Force")
    print("3. Potential Energy")
    print("4. Kinetic Energy")
    print("5. Momentum")

    choice = input("Choose (1-5): ")

    if choice == "1":
        print("Frequency =", frequency(float(input("Period: "))), "Hz")

    elif choice == "2":
        q1 = float(input("Charge 1: "))
        q2 = float(input("Charge 2: "))
        r = float(input("Distance: "))
        print("Force =", coulomb_force(q1, q2, r), "N")

    elif choice == "3":
        m = float(input("Mass: "))
        h = float(input("Height: "))
        print("Potential Energy =", potential_energy(m, h), "J")

    elif choice == "4":
        m = float(input("Mass: "))
        v = float(input("Velocity: "))
        print("Kinetic Energy =", kinetic_energy(m, v), "J")

    elif choice == "5":
        m = float(input("Mass: "))
        v = float(input("Velocity: "))
        print("Momentum =", momentum(m, v), "kg·m/s")

    else:
        print("Invalid choice")

    if input("Continue? (yes/no): ").lower() == "no":
        print("Goodbye!")
        break