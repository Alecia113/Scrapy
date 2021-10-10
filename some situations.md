First of all I don't know what scrapy is, scrapy is a framework for crawlers.
Nor do I know how scapy works. Couldn't even read the task requirements. First find some research cases to analyze.
Found that scapy is using item + a spider.py to achieve the data from HTML. Also need to know HTML knowledge.

web url： response.url
<p>some function about response.xpath</p>
<img src="https://github.com/Alecia113/Scrapy/blob/main/img/11.png">
This one has both categories and tagged content
<p> response.xpath('//a/@href').extract() </p>
<p> More specifically </p>
<img src="https://github.com/Alecia113/Scrapy/blob/main/img/12.png">
<p> If there is a problem with XPath, then the result after extract() may be an empty list. </p>
<p> We extract the first result of the match directly using the extract_first() method </p>
<img src="https://github.com/Alecia113/Scrapy/blob/main/img/13.png">
<p> Extract the first </p>
<p> response.xpath('//a/text()').extract_first() </p>
<p> Extracting website title tag content </p>
<img src="https://github.com/Alecia113/Scrapy/blob/main/img/14.png">
<p> https://blog.csdn.net/Python_sn/article/details/108827436?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522163301544016780261980026%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=163301544016780261980026&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~sobaiduend~default-2-108827436.first_rank_v2_pc_rank_v29&utm_term=response.selector.xpath&spm=1018.2226.3001.4187</p>
<p> response.xpath('//meta[count(title)]/@id').extract() </p>
<p> response.selector.xpath('//title/text()').extract_first() </p>
<p> title </p>
<img src ="https://github.com/Alecia113/Scrapy/blob/main/img/15.png">
<p> scrapy shell "http://www.dmoztools.net" </p>
<img src="https://github.com/Alecia113/Scrapy/blob/main/img/16.png">
<p> input:scrapy crawl dmoz -o items.json -t json </p>
<p> cd quotes </p>
<p> scrapy genspider www.dmoztools.net/ </p>
<p> input:scrapy crawl dmoz -o items.csv -t csv </p>
<p> Why can't it come out. The code is not put together </p>
<p> <meta property="og:title"         content="DMOZ" /> </p>
<p>(wrong)response.xpath('//meta[@property="og:title"]/text()').extract()</p>
<p> response.xpath('//title').extract() </p>
<p> <div class="outer-cats"></p>
<p> response.xpath('//div[@class="outer-cats"]//a/@href').extract()</p>
                                             
<p> response.xpath('//a/@href').extract() </p>
<p> response.xpath('//a/@href').extract() </p>
<p> response.xpath('//a/@href').extract() </p>
<p> response.xpath('//a/@href').extract() </p>
<p> response.xpath('//a/@href').extract() </p>
<p> response.xpath('//a/@href').extract() </p>
<p> response.xpath('//a/@href').extract() </p>
<p> response.xpath('//a/@href').extract() </p>





