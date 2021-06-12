# Quá Trình Thu Thập Dữ liệu 
1. Với website https://babylonbee.com/ (1): Chỉ lấy article headlines ở https://babylonbee.com/news. Hàm babylonbee_articles viết bên trên nhận vào số trang muốn scrape và sẽ tiến hành chạy từ trang 1 đến trang đó, Như trên đây nhóm lấy 354 trang là hết tất cả các trang luôn rồi.
2. Với website https://thehardtimes.net/ (1): Tương tự như babylonbee cũng có một hàm babylonbee_articles nhận vào số trang muốn scrape và chạy từ trang 1 tới trang đó. Ở đây nhóm scrape tất cả các trang là 372 trang.
3. Với website https://www.nytimes.com/ (0): Ở đây nhóm scrape theo ngày tháng năm nhờ vào site map. URL có dạng như https://www.nytimes.com/sitemap/2021/06/07/. Nhóm đã scrape từ năm 2020 đến hết năm 2016
4. Với website https://www.thetimes.co.uk/ (0): Tương tự nytimes, the times cũng có sitemap nhưng URL có dạng https://www.thetimes.co.uk/html-sitemap/2020-01-2 với chỉ số cuối thay vì ngày là số từ 1 tới 4. Nhóm đã scrape từ năm 2020 đến hết năm 2016.
5. Với website https://www.ft.com/: Nhóm scrape theo category urls = ["https://www.ft.com/world?page=","https://www.ft.com/companies?page=","https://www.ft.com/technology?page=","https://www.ft.com/markets?page=","https://www.ft.com/climate-capital?page=","https://www.ft.com/opinion?page=","https://www.ft.com/work-careers?page=","https://www.ft.com/arts?page=","https://www.ft.com/books?page=","https://www.ft.com/food-drink?page=","https://www.ft.com/magazine?page=","https://www.ft.com/house-home?page=","https://www.ft.com/style?page=","https://www.ft.com/travel?page=","https://www.ft.com/htsi?page="], tiến hành chạy từ trang 1 đến khi nào lỗi thì chuyển sang category tiếp theo
6. Với website https://www.theguardian.com/: cách làm y hệt như web https://www.ft.com/ với urls = ["https://www.theguardian.com/world?page=","https://www.theguardian.com/commentisfree?page=","https://www.theguardian.com/sport?page=","https://www.theguardian.com/culture?page=","https://www.theguardian.com/lifeandstyle?page="]
7.Với website https://www.breitbart.com/(0), lấy headline ở các mục lục page sau:
https://www.breitbart.com/politics/
https://www.breitbart.com/entertainment/
https://www.breitbart.com/the-media/
https://www.breitbart.com/economy/
https://www.breitbart.com/europe/
https://www.breitbart.com/border/
https://www.breitbart.com/middle-east/
https://www.breitbart.com/africa/
https://www.breitbart.com/asia/
https://www.breitbart.com/latin-america/
https://www.breitbart.com/world-news/
https://www.breitbart.com/tech/
https://www.breitbart.com/sports/
https://www.breitbart.com/tag/on-the-hill/
/news/
https://www.breitbart.com/tag/b-inspired-news/
Với mỗi mục lục page sẽ tiến hành chạy từng trang 1(giới hạn bài báo cho mỗi mục lục page là 5000 bài):
* Thu thập headline và link dẫn từng bài báo
* Lấy ra thời gian đăng bài báo và chỉ chọn những bài báo được đăng trong 2 năm trở lại đây
* Chạy đến cuối trang thì chuyển sang trang báo tiếp theo
Số dữ liệu đã thu thập được là:65996
7. Với website https://www.huffpost.com/, đầu tiên ta lấy tất cả các articles ở các mục trong page, tiếp theo sẽ lọc lấy headline từ các articles, sau đó in ra mỗi mẫu dữ liệu với các thuộc tính là headline, article_link, is_sarcastic được ngăn cách bởi dấu "|" và lưu dưới định dạng file.txt. Các dữ liệu sẽ được lấy trong 3 năm gần nhất (tính tới ngày 1/1/2019). Kết quả thu được bao gồm 54785 mẫu dữ liệu.
# Nguồn tham khảo:
1. Thư viện pandas: https://pandas.pydata.org/docs/
2. Thư viện request: https://docs.python-requests.org/en/master/
3. Thư viện bs4: https://www.crummy.com/software/BeautifulSoup/bs4/doc/
4. Thông tin dữ liệu: https://www.kaggle.com/rmisra/news-headlines-dataset-for-sarcasm-detection
