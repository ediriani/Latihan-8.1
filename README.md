def is_anagram(kata1, kata2):
    """
    Mendeteksi apakah kata1 adalah anagram dari kata2.

    Args:
        kata1 (str): Kata pertama.
        kata2 (str): Kata kedua.

    Returns:
        bool: True jika kata1 adalah anagram dari kata2, False sebaliknya.
    """
    # Hilangkan spasi dan ubah ke huruf kecil
    kata1 = kata1.replace(" ", "").lower()
    kata2 = kata2.replace(" ", "").lower()

    # Periksa apakah panjang kedua kata sama
    if len(kata1) != len(kata2):
        return False

    # Urutkan huruf dalam kedua kata dan bandingkan
    return sorted(kata1) == sorted(kata2)

# Contoh penggunaan
kata_pertama = input("Masukkan kata pertama: ")
kata_kedua = input("Masukkan kata kedua: ")

if is_anagram(kata_pertama, kata_kedua):
    print(f"'{kata_pertama}' adalah anagram dari '{kata_kedua}'")
else:
    print(f"'{kata_pertama}' bukan anagram dari '{kata_kedua}'")
