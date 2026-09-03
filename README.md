# Chirpy

brew install ruby@3.3
echo 'export PATH="/opt/homebrew/opt/ruby@3.3/bin:$PATH"' >> ~/.zshrc
source ~/.zshrc;2A
gem install bundler
bundle install
bundle exec jekyll serve

check html functions:
bundle exec htmlproofer _site
