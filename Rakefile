# namespace :greeting do
#   desc 'outputs hello from the terminal'
#   task :hello do
#     puts 'hello from Rake!'
#   end

#   desc 'out puts YELLOW to the terminal'
#   task :yellow do
#     puts 'YELLOW!'
#   end
# end

desc 'drop into pry console'
task console: :environment do
  Pry.start
end

task :environment do
  require_relative './config/environment'
end

namespace :db do
  desc 'migrate changes to your databases'
  task migrate: :environment do
    Student.create_table
  end

  desc 'seed the db with dummy data'
  task seed: :environment do
    require_relative './db/seeds'
  end
end
