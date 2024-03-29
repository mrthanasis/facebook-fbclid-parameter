# How to remove Facebook's fbclid parameter using mod_rewrite

With mod_rewrite, we can manipulate the query string and remove any occurrence of fbclid=whatever while preserving the remaining parameters. 

What is the fbclid parameter?
The fbclid parameter is set by Facebook when somebody clicks through to your website from an advert on their platform. It is a feature that was introduced in late 2018, likely in response to emerging cookie policy updates and anti-tracking features in browsers. It almost certainly allows Facebook to more reliably collect click data on third party websites featuring the Facebook pixel by setting a unique URL for each visitor.

Unfortunately a side-affect of the unique URL structure is that your analytics package can think that hundreds or even thousands of your pageviews are for different pages even though the only difference is the tracking ID.


****Please note that the above configuration uses the default WordPress .htaccess file. The rewrite rule must be placed before the WordPress rewrite rules (# BEGIN WordPress … # END WordPress).


Luckily Google offers a simple feature for removing the fbclid and any other parameter from your analytics…

# How to remove the fbclid parameter from Google Analytics

Log in to **Google Analytics**.
Go to the **Admin section**.
Go to your **View** Settings.
Add fbclid to the **Exclude URL Query Parameters** field.
Hit **Save**

So there you have it, a super simple fix for this annoying quirk in your analytics. You can also use this same technique if any other parameters are messing up your analytics views.
