namespace :greeting do
desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end

desc 'outputs hola to the terminal'
  task :hola do
    puts "hola de Rake!"
  end
end

desc 'drop into the Pry console'
  task :console do
    Pry.start
  end

namespace :db do
desc 'invokes the environment.rb file'
  task :environment do
    require_relative './config/environment'
  end

desc 'migrates tables to the DB'
  task :migrate => :environment do
    Student.create_table
  end

desc 'seeds the db with some dummy data'
  task :seed do
    require_relative './db/seeds'
  end
end

