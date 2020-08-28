python dynamodump/dynamodump.py -m backup -r ap-southeast-2 -s asx_listed_companies --host localhost --port 8000 # this actually worked, need more workers on AWS though

python dynamodump/dynamodump.py -m restore -r local -s asx_listed_companies --host localhost --port 8000


## schema for asx_raw_prices_2
python dynamodump/dynamodump.py -m backup -r ap-southeast-2 -s asx_raw_prices_2 --schemaOnly

python dynamodump.py -m restore -r local -s asx_raw_prices_2 --schemaOnly


## schema for asx_dividends
python dynamodump.py -m backup -r ap-southeast-2 -s asx_dividends --schemaOnly

python dynamodump.py -m restore -r local -s asx_dividends --schemaOnly


## schema for asx_splits
python dynamodump.py -m backup -r ap-southeast-2 -s asx_splits --schemaOnly
python dynamodump.py -m restore -r local -s asx_splits --schemaOnly


## schema for asx_trade_universe
python dynamodump.py -m backup -r ap-southeast-2 -s asx_trade_universe --schemaOnly

python dynamodump.py -m restore -r local -s asx_trade_universe --schemaOnly
