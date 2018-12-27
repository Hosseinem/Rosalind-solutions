def find_motif(s,t):
    positions = ''
    for i in range(len(s)):
        if s[i] == t[0]:
            if s[i:i+len(t)] == t:
                positions += str(i+1)+' '
    return positions


with open('rosalind_subs.txt','r') as file:
    content = file.read()
DNA, subDNA = content.splitlines()
print(find_motif(DNA, subDNA))
