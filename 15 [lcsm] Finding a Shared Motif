def find_lca(lst):
    lcas = set()
    last = lst.pop()
    for i in range(len(last)):
        common = True
        n = i
        while common:
            n += 1
            for dna in lst:
                if last[i:n] not in dna:
                    common = False
                    n -= 1
                    break
            if common is False or n > len(last):
                break
            lcas.add(last[i:n])

    lcas = list(lcas)
    return max(lcas,key=len)


with open('rosalind_lcsm.txt', 'r') as file:
    content = file.read()
DNAs_number, lines, line_number, DNAs = content.count('>'), content.splitlines(), 0, []
for i in range(DNAs_number):
    DNA = ''
    line_number += 1
    while lines[line_number][0] != '>':
        DNA += lines[line_number]
        line_number += 1
        if line_number+1 > len(lines):
            break
    DNAs.append(DNA)
print(find_lca(DNAs))
