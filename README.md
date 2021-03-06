# ISO 3166-1 Country List in English and Russian

[![Build Status](https://travis-ci.org/artemshitov/iso3166_ru.png?branch=master)](https://travis-ci.org/artemshitov/iso3166_ru) [![Code Climate](https://codeclimate.com/github/artemshitov/iso3166_ru.png)](https://codeclimate.com/github/artemshitov/iso3166_ru)

## Installation

Add this line to your application's Gemfile:

    gem 'iso3166_ru', '~> 0.2.0'

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install iso3166_ru

## Usage

### Country finders

    Iso3166Ru.find_by(alpha2: "RU")
    Iso3166Ru.find_by(alpha3: "RUS")
    Iso3166Ru.find_by(name: "Россия")
    Iso3166Ru.find_by(full_name: "Российская Федерация")
    Iso3166Ru.find_by(english: "Russian Federation")
    Iso3166Ru.find_by(iso: "643")

All finders return an `Iso3166Ru::Country` struct.

### Country

    country = Iso3166Ru.find_by(alpha2: "RU")

    country.alpha2             #=> "RU"
    country.alpha3             #=> "RUS"
    country.name               #=> "Россия"
    country.full_name          #=> "Российская Федерация"
    country.english            #=> "Russian Federation"
    country.iso                #=> "643"
    country.location           #=> "Европа"
    country.location_precise   #=> "Восточная Европа"


## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request
