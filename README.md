# PROGRAM-FOR-ATM
password=4321
balance=10000
print('****WELCOME TO OUR ATM $ERVICE$****')
pin=int(input('ENTER YOUR ATM 4 DIGIT PIN NUMBER:'))
while(pin!=password):
	print('///invalid password try again///')
	pin=int(input('Enter your password correctly :'))
while(True):
	print('\nSELECT YOUR CHOICE \n1.MONEY WITHDRAW \n2.MONEY DEPOSITE\n3.MONEY TRANSFER\n4.BALANCE ENQUIRY\n5.CHANGE ATM PIN\n6.EXIT')
	opt=int(input('Enter your choice : '))
	nip=int(input('ENTER YOUR* 4 * DIGIT PASSWORD :'))
	while(nip!=password):
		nip=int(input('Enter correctly :'))
	if opt==1:
		withdraw=int(input('ENTER MONEY TO WITHDRAW :'))
		if withdraw>balance:
			print('YOU ENTER BIGGEST AMOUNT')
		else:
			balance-=withdraw
			print(withdraw,'MONEY WITHDRAW SUCCESSFULLY FROM YOUR ACCOUNT')
	elif opt ==4:
		print(balance,'THIS IS YOUR BALANCE IN YOUR ACCOUNT ')
	elif opt==2:
		depo=int(input('ENTER THE MONEY TO DEPOSITE IN YOUR ACCOUNT : '))
		balance+=depo
		print(depo,'RS DEPOSITED SUCCESSFULLY  IN YOUR BANK ACCOUNT ')
	elif opt==3:
		tra=int(input('ENTER VALID ACCOUNT NUMBER TO TRANSFER MONEY FROM YOUR ACCOUNT:'))
		amount=int(input('ACCOUNT IS VERIFIED AND  ENTER MONEY TO TRANSFER TO THIS ACCOUNT :'))
		if amount>balance :
				print('YOU ENTER BIGGEST AMOUNT')
		else:
					balance-=amount
					print(amount,'TRANSFERED SUCCESSFULLY TO THIS ACCOUNT NUMBER',tra)
	elif opt ==5:
		pin=int(input('ENTER YOUR OLD PASSWORD :'))
		while(pin==password):
			ph=int(input('ENTER YOUR PH NUMBER : '))
			npass=int(input('ENTER YOUR NEW PASSWORD : '))
			while(npass==password):
				print('PASSWORD CHANGED SUCCESSFULLY ')
				npass=int(input('Enter your new password'))
			quit()
		else:
				print('password does not match with old password')
	elif opt ==6:
		print('THANKS FOR USING OUR ATM SERVICE')
		quit()
