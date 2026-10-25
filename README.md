# Mini-Python-Script

Μικρά πειράματα με **Python** και **Jupyter Notebook**: σύντομα, αυτοτελή notebooks που γράφτηκαν για εξοικείωση με τη γλώσσα, με τη βιβλιοθήκη της και με το περιβάλλον του Jupyter.

## Περιεχόμενα

| Notebook | Τι δείχνει | Κατάσταση |
|---|---|---|
| [Python Examples in 5 minutes](Python%20Examples%20in%205%20minutes.ipynb) | Τα βασικά της Python σε 5 λεπτά: `print`, εσοχές, σχόλια, μεταβλητές και τύποι (`int`, `float`, `complex`), λίστες, βρόχοι `for` και `range`, είσοδος από τον χρήστη με `input()`. Περιλαμβάνει και σύγκριση με το «Hello World» της C. | ✅ Λειτουργεί |
| [Find IP and Hostname With Python](Find%20IP%20and%20Hostname%20With%20Python.ipynb) | Βρίσκει το όνομα του υπολογιστή και τη διεύθυνση IP του με το module `socket`. | ✅ Λειτουργεί (δες σημείωση) |
| [Find Wifi Passwords Using Python](Find%20Wifi%20Passwords%20Using%20Python.ipynb) | Εμφανίζει τα αποθηκευμένα δίκτυα Wi-Fi του υπολογιστή και τους κωδικούς τους, καλώντας την εντολή `netsh` των Windows μέσω `subprocess`. | ⚠️ Μόνο σε Windows |

## Σημειώσεις από τη δοκιμή

Τα notebooks ελέγχθηκαν σε Python 3.13 (γράφτηκαν αρχικά σε Python 3.10):

- **Python Examples:** εκτελείται χωρίς σφάλματα. Το τελευταίο κελί περιμένει δύο αριθμούς από τον χρήστη.
- **Find IP and Hostname:** εκτελείται, αλλά σε Linux η `gethostbyname(hostname)` συχνά επιστρέφει `127.0.0.1` αντί για την IP του τοπικού δικτύου. Σε Windows δίνει κανονικά την IP του δικτύου.
- **Find Wifi Passwords:** δουλεύει μόνο σε Windows, γιατί βασίζεται στην εντολή `netsh`. Επίσης ψάχνει τις αγγλικές φράσεις «All User Profile» και «Key Content», οπότε σε Windows με ελληνική γλώσσα συστήματος δεν βρίσκει αποτελέσματα. Το τελευταίο `input("")` κρατάει το κελί ανοιχτό μέχρι να πατηθεί Enter.

> Το notebook για τα Wi-Fi είναι για εκπαιδευτική χρήση και μόνο σε δικό σου υπολογιστή. Βασίζεται στο παράδειγμα του [CodeWithCurious](https://codewithcurious.com/projects/find-wifi-passwords-using-python/).

## Εκτέλεση

```bash
pip install notebook
jupyter notebook
```

Δεν χρειάζονται εξωτερικές βιβλιοθήκες: όλα τα notebooks χρησιμοποιούν μόνο την standard library της Python (`socket`, `subprocess`).

## Τεχνολογίες

- Python 3
- Jupyter Notebook

## Πηγές

- [W3Schools – Python Tutorial](https://www.w3schools.com/python/python_intro.asp)
- [CodeWithCurious – Find WiFi Passwords Using Python](https://codewithcurious.com/projects/find-wifi-passwords-using-python/)
