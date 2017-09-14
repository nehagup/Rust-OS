# Rust-OS
<!-- Banner Image -->
[![Banner Title]][banner_flickr]

[banner.jpg]: docs/images/banner.jpg
[banner_flickr]: #

 generate_banner = (opts) ->
    if opts.informative then inform "Generating banner to place on the very top"
  
    path = opts.readme_folder
    banner_file = opts.banner
    output = opts.output

    f = path+"/"+banner_file
  
    unless grunt.file.exists f
      grunt.fail.fatal "Source file \"" + f + "\" not found."
    else
      fs.appendFileSync output, grunt.file.read f
      fs.appendFileSync output, "\n"
      
      
      
      banner: null
      
     
    # generate banner
    if options.banner?
      generate_banner options
