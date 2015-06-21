desc 'Create a new post'
task :new_post do
  title = ENV["title"] || "New Title"
  slug = title.gsub(' ', '-').downcase
 
  # new file with format ex 2014-09-13-name-of-post.markdown
  date = Time.new.strftime('%Y-%m-%d')
  file_name = "#{date}-#{slug}.markdown"
  
  header = <<-HEAD
---
layout: post
title: #{title}
category: blog
date: #{date}
---
HEAD

  File.open("_posts/#{file_name}", "w") do |f|
    f.puts header
  end

end

