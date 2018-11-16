DeepSearch - Advanced Web Dir Scanner 
--
__DeepSearch__ is a simple command line tool for bruteforce directories and files in websites.

![screen](https://raw.githubusercontent.com/m4ll0k/DeepSearch/master/screen.png)

Installation
--
```sh
$ git clone https://github.com/m4ll0k/DeepSearch.git deepsearch
$ cd deepsearch 
$ pip3 install requests
$ python3 deepsearch.py

```

Screenshots
--

![screen_2](https://raw.githubusercontent.com/m4ll0k/DeepSearch/master/screen2.png)


Usage
--
 __Basic:__

`python3 deepsearch.py -u http://testphp.vulnweb.com/ -e php -w wordlist.txt`

__Force extension for every wordlist entry (support one extension):__

`python3 deepsearch.py -u http://testphp.vulnweb.com/ -e php -w wordlist.txt -f`

__Make a request by hostname (ip):__

`python3 deepsearch.py -u http://testphp.vulnweb.com/ -e php -w wordlist.txt -b`

__Force lowercase for every wordlist entry:__

`python3 deepsearch.py -u http://testphp.vulnweb.com/ -e php -w wordlist.txt -l`

__Force uppercase for every wordlist entry:__

`python3 deepsearch.py -u http://testphp.vulnweb.com/ -e php -w wordlist.txt -p`

__Show only status code separated by comma:__

`python3 deepsearch.py -u http://testphp.vulnweb.com/ -e php -w wordlist.txt -o 200,301,302`

__Exclude status code separated by comma:__

`python3 deepsearch.py -u http://testphp.vulnweb.com/ -e php -w wordlist.txt -x 501,502,503,401`

__URL Injection Point (%word%):__

`python3 deepsearch.py -u http://testphp.vulnweb.com/test%1%.php -e php -w wordlist.txt`

__URL Injection Point (%%):__

`python3 deepsearch.py -u http://testphp.vulnweb.com/id/%%/index.html -e php -w wordlist.txt`

__URL Injection Point in Parameters:__

`python3 deepsearch.py -u http://testphp.vulnweb.com/index.php?id=%2%&user=1 -e php -w wordlist.txt`

`python3 deepsearch.py -u http://testphp.vulnweb.com/index.php?%id%=1&user=2 -e php -w wordlist.txt`

__Add Headers:__

`python3 deepsearch.py -u http://testphp.vulnweb.com/ -e php -w wordlist.txt -H "Content-Type:text/html\nETag:1234" `

__Proxy:__

`python3 deepsearch.py -u http://testphp.vulnweb.com/ -e php -w wordlist.txt -P 127.0.0.1:8080`

__URLs by list:__

`python3 deepsearch.py -U my_urls.txt -e php -w wordlist.txt`

__Other Options:__

`python3 deepsearch.py -u http://testphp.vulnweb.com/ -e php -w wordlist.txt -t 10 -T 3 -d 2 -R -c "test=test" --random-agent`
