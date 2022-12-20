# Praktikum9

Repository ini digunakan untuk memenuhi Tugas Bahasa Pemrograman Pertemuan-13

Nama    : Mohamad Irvan Zidni

NIM     : 312210308

Kelas   : TI.22.A.3

# COMING SOON!!!

Python menyediakan 2 fitur paling penting untuk menangani unexpected error untuk Python yaitu

1. Exception Handling
2. Assertions

### Assertions in Python
Assertions Exception adalah sebuah peristiwa, yang terjadi selama pelaksanaan program yang mengganggu aliran normal instruksi program

Syntax untuk assert

	assert Expression[, Arguments]

contohnya:

	def KtoF(Temperature):
	    assert(Temperature >= 0),"Sangat dingin melebihi nol derajat"
	    return((Temperature-273)*1.8)+32

	print (KtoF(273))
	print (int(KtoF(505.78)))
	print (KtoF(-5))

### try...except

Contoh syntax nya:

	try:
	......................

	except ExceptionI:
	......................

	except ExceptionII:
	......................

	else:
	......................

Contoh:

	try:
	    fh = open("testfile","w ")
	    fh.write("File for exception handling")

	except IOError:
	    print("Error: cannot find file or read data")

	else:
	    print("Konten berhasil di-write")
	    fh.close()

### try-finally

Contoh syntax nya

	try:
	......................

	finally:
	......................

Contoh penggunaannya:

	try:
	    fh = open("testfile","w")
	    fh.write("Hello :)")
	finally:
	    print("ERROR: CANNOT FIND FILE OR DATA")

Contoh lainnya:

	try:
	    fh = open("testfile","w")
	    try:
	        fh.write("File for exception handling")
	    finally:
	        print("FILE AKAN DITUTUP")
	        fh.close()
	except IOError:
	    print("ERROR: CANNOT FIND THE FILE OR DATA")

### Raise

Contoh syntax:

	raise [Exception [, args [, traceback]]]

Contohnya:

	def level(level):
	    if level < 1 :
	        raise Exception("Invalid level ! ",level)

	print(level(0))


### User Defined Exceptions

Contohnya :

	class NetworkError(RuntimeError):
	    def __init__(self, arg):
	        self.args = arg
	try:
	    raise NetworkError("Bad Hostname")
	except NetworkError as e:
	    print (e.args)