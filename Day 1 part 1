def count_zero_hits(lines, start=50):
    pos = start
    count = 0
    for line in lines:
        line = line.strip()
        if not line:
            continue
        dir_ = line[0].upper()
        dist = int(line[1:])
        if dir_ == 'L':
            pos = (pos - dist) % 100
        elif dir_ == 'R':
            pos = (pos + dist) % 100
        else:
            raise ValueError(f"Bad direction: {dir_} in line {line}")
        if pos == 0:
            count += 1
    return count

# Example test
example = """L68
L30
R48
L5
R60
L55
L1
L99
R14
L82""".splitlines()
print(count_zero_hits(example))
