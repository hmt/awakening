#The Awakening by Kate Chopin

This beautiful novel has its dedicated repository here on GitHub.

I'll subsequently add new files with special features like:

* proper quotes and dashes
* Latex file with sections and all
* whatever else comes to my mind

As long as it doesn't clutter the Readme I'll add information about the process here.

The original text was taken from Project Gutenberg, stripped and reduced to its original text. 

###Converting quotes, dashes etc
In order to get the nice typographical features I used a Ruby gem:

    require 'rubypants-unicode'
    file = File.open("awakening.txt", "r")
    text = file.read
    File.open('awakening_smart.txt', 'w') do |f|
      f.puts RubyPants.new(text, 2).to_html
    end