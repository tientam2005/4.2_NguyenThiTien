# 4.2_NguyenThiTien
#k=47
#P=NGUYENTHITIEN

def encrypt_caesar(plaintext, K):
    ketqua = ""
    for ch in plaintext.upper():
        if ch.isalpha(): 
            P = ord(ch) - ord('A')   # đưa về số 0..25
            C = (P + K) % 26       
            ketqua += chr(C + ord('A'))
        else:
            ketqua += ch 
    return ketqua
# Thử nghiệm
plaintext = "NGUYENTHITIEN"
K = 47
ciphertext = encrypt_caesar(plaintext, K)

print("Plaintext :", plaintext)
print("Ciphertext:", ciphertext)
