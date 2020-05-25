pyDismail
==============

:info: a pretty basic scraper for yadim.dismail.de, a disposable mail provider

Installation
------------
not on pyPi soo..
.. code-block:: shell

    pip install .

Usage
-----

.. code-block:: python

    from pyDismail import Dismail
    disposable_mail = Dismail(mail="example")
	print(disposable_mail.mail)
	# example@yadim.dismail.de
	
	mails = Dismail.fetch_all_mails()
	print(mails[0])
	# (Mail Object: 92345, example@gmail.com, datetime.datetime(2020, 5, 25, 12, 12, 12), SUBJECT, CONTENT)
	
	disposable_mail.delete_by_id(mail[0].id)
	
	disposable_mail.check_for_new() # return True if new mail arrived after object created
	
	
