# marcopolo

# hive table for mens items table

create table mens_products_full (
category				int,
subcategory				string,
name					string,
current_price				    Float,
raw_price				Float,
currency				string,
discount				int,
likes_count				int,
is_new				string,
brand			string,
brand_url			string,
codCountry				string,
variation_0_color		string,
variation_1_color		string,
variation_0_thumbnail	string,    
variation_0_image		string,
variation_1_thumbnail	string,
variation_1_image		string,
image_url				string,
url						string,
id						int,
model					string
)
ROW FORMAT DELIMITED
FIELDS TERMINATED BY ','
LINES TERMINATED BY '\n'
STORED AS TEXTFILE
TBLPROPERTIES("skip.header.line.count"="1");
LOAD DATA LOCAL INPATH '/Users/jsenjaliya/Downloads/mens_items.csv' OVERWRITE INTO TABLE mens_products_full;
