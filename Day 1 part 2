rotations = """
L68
L30
R48
L5
R60
L55
L1
L99
R14
L82
""".strip().splitlines()

def part2(rotations, start=50):
    s = start
    total = 0
    for line in rotations:
        line = line.strip()
        if not line: 
            continue
        d = int(line[1:])
        if line[0] == "R":
            total += (s + d) // 100
            s = (s + d) % 100
        else:  # L
            if s == 0:
                total += d // 100
            else:
                if d >= s:
                    total += 1 + (d - s) // 100
            s = (s - d) % 100
    return total

print(part2(rotations))
