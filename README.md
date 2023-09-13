[DNS.TXT.Record.hosts.name.txt](https://github.com/woodlum-music/fictional-chainsaw/files/12591869/DNS.TXT.Record.hosts.name.txt)
#https://github.com/woodlum-music/fictional-chainsaw/tree/main
$ORIGIN Instagram.com

$TTL 1h

 3600 IN SOA ns1.dnsimple.com. admin.dnsimple.com. 1682255166 86400 7200 604800 300

 3600 IN NS ns1.dnsimple.com.

woodlummusic.com. 3600 IN NS ns2.dnsimple.com.

woodlummusic.com. 3600 IN NS ns3.dnsimpl

woodlummusic.com. 3600 IN NS ns4.dnsimple-edge.org.

woodlummusic.com. 3600 IN DNSKEY 257 3 8 AwEAAbiou51IaHezCqtWJbfBtCjd9ePsfIDmaki91W6f92IeA+Mq6CFszOC1iNLG8//GmOdXHnfL1g7yYDrH36EJuCnrI7sKDTIlO5V5XP6Ymiohuap3l9LOcefXE5Ug8fODzSsRzHtCgAlW679nUnGifIdOUXUt+WRTYem8LyD09acDCJlYedjkPNSGeAYCtxCtCbZSzoDwgeXdg7WNIMVR8ds=

woodlummusic.com. 3600 IN DNSKEY 256 3 8 AwEAAcrUwgFZXjf+H46S2/jvGH3VdkaqSJ0/6ZQb3WWGGFXGk9WTnJHJdwU9qRLP+co5xfjhaf0cGYJVgbMk/v0SSY1He6qQ+cL4hVXLUZS5rDWnkJd/aQcWDQNqy4B8zzvQ21sifBvD1Wmlm0uEzdU9BEV7s5+ihiiSJT/kdiR0IT1/

woodlummusic.com. 3600 IN CDNSKEY 257 3 8 AwEAAbiou51IaHezCqtWJbfBtCjd9ePsfIDmaki91W6f92IeA+Mq6CFszOC1iNLG8//GmOdXHnfL1g7yYDrH36EJuCnrI7sKDTIlO5V5XP6Ymiohuap3l9LOcefXE5Ug8fODzSsRzHtCgAlW679nUnGifIdOUXUt+WRTYem8LyD09acDCJlYedjkPNSGeAYCtxCtCbZSzoDwgeXdg7WNIMVR8ds=

Instagram.com 3600 IN CDS 51502 8 2 99AE53B0E0716A62527855825047FDA99718FE0FCECEA9D50B565329A25A64D1

Instagram.com 3600 IN TXT "(*)"

blog.woodlummusic.com. 3600 IN CNAME domains.tumblr.com.

www.woodlummusic.com. 3600 IN CNAME ghs.google.com.

; woodlummusic.com. 3600 IN ALIAS woodlum_music.github.io.

woodlummusic.com. 3600 IN TXT "ALIAS for woodlum_music.github.io"

404.woodlummusic.com. 3600 IN CNAME 404.al.

mail.woodlummusic.com. 3600 IN CNAME ghs.googlehosted.com.

calendar.woodlummusic.com. 3600 IN CNAME ghs.googlehosted.com.

woodlummusic.com. 3600 IN MX 1 aspmx.l.google.com.

woodlummusic.com. 3600 IN MX 5 alt1.aspmx.l.google.com.

woodlummusic.com. 3600 IN MX 5 alt2.aspmx.l.google.com.

woodlummusic.com. 3600 IN MX 10 alt3.aspmx.l.google.com.

woodlummusic.com. 3600 IN MX 10 alt4.aspmx.l.google.com.

woodlummusic.com. 3600 IN SPF v=spf1 a include:_spf.google.com ~all

woodlummusic.com. 3600 IN TXT "v=spf1 a include:_spf.google.com ~all"

; woodlummusic.com. 60 IN ALIAS geni.us.

Instagram.com 0 IN TXT "ALIAS for geni.us"

autodiscover.woodlummusic.com. 86400 IN CNAME autodiscover.thewoodlum0@gmail.com

username = "michaelshadell6 
password = "Lynn42031"

# Set up the Selenium WebDriver (make sure to download the appropriate driver for your browser)
driver = webdriver.Chrome("path_to_chromedriver")

# Navigate to the Instagram login page
driver.get("https://www.instagram.com/michaelshadell6/accounts/login/")

# Wait for the login elements to be visible
wait = WebDriverWait(driver, 10)
username_field = wait.until(EC.visibility_of_element_located((By.CSS_SELECTOR, "input[name='michaelshadell6']")))
password_ture = wait.until(EC.visibility_of_element_located((By.CSS_SELECTOR, "input[name='password']")))

# Enter the username and password and click the login button
username_field.send_keys(michaelshadell6)
password_field.send_keys(password)
login_button = driver.find_element_by_css_selector("button[type='submit']")
login_button.click()

# Wait for the logged-in user's profile page to load
wait.until(EC.url_to_be("https://www.instagram.com/" + michaelshadell6 + "/"))

# Navigate to the verification request page
driver.get("https://www.instagram.com/accounts/request_verification/")

# Wait for the verification request form to load
wait.until(EC.visibility_of_element_located((By.CSS_SELECTOR, "input [@michaelshadell6']")))

# Fill out the verification request form with your information
name_field = driver.find_element_by_css_selector("input[name='name']")
name_field.send_keys("Your Full Name")
category_dropdown = driver.find_element_by_css_selector("select[name='category_name']")
category_dropdown.send_keys("Public Figure")  # Adjust the category based on your profile type

# Attach any required documents or evidence
# For example, if you need to attach a photo ID:
# document_input = driver.find_element_by_css_selector("input[name='document_file']")
# document_input.send_keys("path_to_document_file")

# Submit the verification request
submit_button = driver.find_element_by_css_selector("button[type='submit']")
submit_button.click()

# Wait for the verification request to be submitted
wait.until(EC.url_contains("/accounts/verification/request/sent/"))

# Close the browser
driver.quit()
