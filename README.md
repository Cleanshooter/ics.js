ics.js
============

A browser firendly .ics/.vcs file generator written entirely in javascript!!!!!!

Now you can make calendar friendly files client-side.  It outputs .ics files, so the files are compatible with all modern calendar software (Outlook, Apple Calendar, Google, etc.)

How To Use
----------
Simply use invoke the object and use the functions...

	var cal = ics();
	cal.addEvent(subject, description, location, begin, end);
	cal.addEvent(subject, description, location, begin, end); // yes, you can have multiple events :-)
    cal.download(filename);

`begin` and `end` need to be formatted in a way that is friendly to `Date()`


Example
-------
* **[Demo](http://htmlpreview.github.io/?https://github.com/nwcell/ics.js/blob/master/demo/demo.html)**

```
<<<<<<< HEAD
<a href="javascript:download_ics('demo', 'Demo Event', 'This is an awesome demo event. Won't you go to Sexy Land?', 'Sexy Land, AK', 'Tue Feb 25 2014 09:30:00 GMT-0600 (CST)', 'Tue Feb 25 2014 10:30:00 GMT-0600 (CST)')">Demo</a>
=======
<script>
	var cal = ics();
	cal.addEvent('Demo Event', 'This is an all day event', 'Nome, AK', '8/7/2013', '8/7/2013');
	cal.addEvent('Demo Event', 'This is thirty minut event', 'Nome, AK', '8/7/2013 5:30 pm', '8/9/2013 6:00 pm');
</script>
<a href="javascript:cal.download()">Demo</a>
>>>>>>> upstream/master
```


Dependencies
------------
The tool uses 2 libraries from the following projects:
* [FileSaver.js](https://github.com/eligrey/FileSaver.js)
* [Blob.js](https://github.com/eligrey/Blob.js)

I've compressed them and included them into the source for the normal file.  Other variations are available in the repo.

If you want IE to allow for either opening documents as well as saving documents, you can use my fork of FileSaver.js (https://github.com/nwcell/FileSaver.js)...  Though you honestly are probebly best off using their main.

Supported Browsers
------------------

| Browser        | Dependancies |
| -------------- | ------------ |
| Firefox 20+    | [FileSaver.js](https://github.com/eligrey/FileSaver.js) |
| Firefox ≤ 19   | [FileSaver.js](https://github.com/eligrey/FileSaver.js), [Blob.js](https://github.com/eligrey/Blob.js) |
| Chrome         | [FileSaver.js](https://github.com/eligrey/FileSaver.js) |
| Chrome for Android v28+ | [FileSaver.js](https://github.com/eligrey/FileSaver.js) |
| IE 10+         | [FileSaver.js](https://github.com/eligrey/FileSaver.js)         |
| Opera Next     | [FileSaver.js](https://github.com/eligrey/FileSaver.js) |
| Opera < 15     | [FileSaver.js](https://github.com/eligrey/FileSaver.js), [Blob.js](https://github.com/eligrey/Blob.js) |
| Safari ≤ 6     | [FileSaver.js](https://github.com/eligrey/FileSaver.js), [Blob.js](https://github.com/eligrey/Blob.js) |


Credits
------------------
* [Travis Krause](https://github.com/nwcell): Me
* [Kyle Hornberg](https://github.com/khornberg): Added multi event functionality and made everything a package firendly
