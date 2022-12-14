### Translate a date with Shopify Liquid.

You can change the formatting of the date string with Shopify, the output will be on English by default and we can't change it from translation file,  with the following codes it will be easy to change the months and date to any languages and you don't need to change it from the code.


### Usage

- Donwload and upload the file `date-translation.liquid` on the **snippet** folder.
- Go to **locales** folder and look for default language `en.default.json` open it and add the following content `months_abbr` and `days_abbr`.
- last call the `date-translation.liquid`

``` liquid
{%- comment -%}
** date:  example 'order.created_at' or current_variant.next_incoming_date.
** translation true to enable the translation.
{%- endcomment -%}

{% render 'date-translation', date: current_variant.next_incoming_date, translation: true %}
```


#### en.default.json

Indented 4 spaces, like `<pre>` (Preformatted Text).

```JSON
  "general": {
   {},
  "months_abbr": {
      "january" : "Jan",
      "february" : "Feb",
      "march" : "Mar",
      "april" : "Apr",
      "may" : "May",
      "june" : "Jun",
      "july" : "Jul",
      "august" : "Aug",
      "september" : "Sep",
      "october" : "Oct",
      "november" : "Nov",
      "december" : "Dec"
    },
    "days_abbr": {
      "monday" : "Mon",
      "tuesday" : "Tue",
      "wednesday" : "Wed",
      "thursday" : "Thu",
      "friday" : "Fri",
      "saturday" : "Sat",
      "sunday" : "Sun"
    }
  }
```

### End
