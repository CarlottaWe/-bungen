# Übungen
Übung 1 kmer in DNA finden

input_sequence = 'AGAGTAATACTAGCAAGCGATAAGTCCCTAACTGGTTGTGGCCTTCTGTAGAGTGAACTTCACCACATATGCTGTCTCTGGCACGTGGATGGTTTGGAGAAATCAGATTCAAGTCTGATCAACCTTCAAACAGATCTAGAGTCTAAAACAGTGATCTCCTGCGTGCGAGATAGAAATACTAGGTAACTACAGGGACTGCGACGTTTTAAACGTTGGTCCGTCAGAAGCGCCATTCAGGATCACGTTACCCCGAAAAAAAGGTACCAGGAGCTCTTCTCCTCTGCAGTCAGGTCTATAG'
from collections import Counter

def main (input_sequence, k):
    kmers = [input_sequence[i:i+k]for i in range(len(input_sequence)-k+1)]
    counts = Counter(kmers)
    maximum = max(counts.values())
    results= [kmer for kmer, count in counts.items()if count ==maximum]
    print(''.join(results))

if __name__== '__main__':
    k=4
    main(input_sequence, k)
