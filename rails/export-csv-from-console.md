# Exporting a csv from rails console

```ruby
require 'csv' 
file = "#{Rails.root}/public/order_data.csv"
orders = Order.order(:id)
headers = ["ID", "Type", "Source"]
CSV.open(file, 'w', write_headers: true, headers: headers) do |writer|
  orders.each do |order|
    writer << [order.id, order.type, order.source]
  end
end
```
