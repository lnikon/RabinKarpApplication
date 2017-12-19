<h1><a id="Application_Of_RabinKarp_Algorithm_0"></a>Application Of Rabin-Karp Algorithm</h1>
<p>Image that we’ve such a problem.<br>
We have some document file, and we need to find how many times concrete words appeared in the text of this document and make decision about the context of the file.</p>
<p>For this purposes we can use some pattern matching algorithm. One of these, is <strong>Rabin-Karp String Matching algorithm</strong>, which uses <em>hashing</em> principles to find occurences of substring in the given string.</p>
<h1><a id="How_RabinKarp_algorithm_works_7"></a>How Rabin-Karp algorithm works.</h1>
<p>Suppose, given two strings and their lenghts. String <strong>S</strong> and it’s length <strong>N</strong> and string <strong>T</strong> and it’s length <strong>M</strong>. We need to find number of occurences of string <strong>T</strong> in the string <strong>S</strong>.<br>
At first, we need to define Hash function.</p>
<p>Hash function will take an argument as string and based on this string return us some number. Or, more abstract <em>A hash function is simply a function that takes in input value, and from that input creates an output value deterministic of the input value.</em></p>
<p>Okey, try to use this hash function to solve our problem. As meintoned previously, this function <em>creates an output value deterministic of the input value</em>, that means that for concrete <em>x</em> we’ll always get same <em>y</em>.<br>
If <code>x = &quot;Hello&quot;</code> then <code>y = Hash(&quot;Hello&quot;)</code>.</p>
<p>Now, calculate the hash for our <code>substring</code>. Denote it <code>hpat</code>. And compare <code>hpat</code> with hash of first <code>M</code> characters of our string <code>S</code>. If these hashes are equal, then compare string <strong>T</strong> with substring of length <strong>M</strong> of <strong>S</strong>. If they’re equal two, that means that we found occurence.<br>
Continue these steps until the end of the string S.<br>
In this way, we can calculate occurences number of any string in some text.<br>
After calculating, we need to store string and their occurences numbers in form of <code>pairs</code> in some <code>vector</code> and sort that vector based on occurences number.<br>
After this all, we’ll get number of occurences for every string in out text.</p>
