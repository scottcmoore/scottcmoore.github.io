## Custom post types in Jekyll
When building this site as a place to showcase independent projects I'm working on, I was really impressed by how simply Jekyll handles looping through the file system to generate posts.

From the docs: "Jekyll traverses your site looking for files to process. Any files with YAML Front Matter are subject to processing."

What's cool is that Jekyll's loops and YAML front matter are so straightforward that it's easy to tweak that processing to suit your needs. For this site, I knew I'd have blog posts like this one, but I've also got projects that I want to show off. For these, I wanted a way to describe the project in a straightforward Markdown file, but have Jekyll handle the prettying up and displaying in the same way as it handles posts. For example, posts are automatically labeled with a date that's interpreted from a string in the file name.

How do you go about creating custom post types in Jekyll? To start, we need to think of the filesystem in terms of an array (since that's roughly how Jekyll treats it). Rather than looping through just the "_posts/" directory, we need to loop through multiple subdirectories. We can tell Jekyll 