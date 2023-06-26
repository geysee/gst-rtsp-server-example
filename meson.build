project('gst-rtsp-examples', 'c')

srcs = [
    'test-onvif-client',
    'test-onvif-server',
    ]
args = []
incs = include_directories('.')

glib_req = '>= 2.56.0'
gst_req = '>= 1.19.2'

glib_dep = dependency('glib-2.0', version : glib_req,
  fallback: ['glib', 'libglib_dep'])
gst_dep = dependency('gstreamer-1.0', version : gst_req,
  fallback : ['gstreamer', 'gst_dep'])
gstrtsp_dep = dependency('gstreamer-rtsp-1.0', version : gst_req,
  fallback : ['gst-plugins-good', 'rtsp_dep'])
gstrtsp_server_dep = dependency('gstreamer-rtsp-server-1.0', version : gst_req,
  fallback : ['gstreamer', 'gst_rtsp_server_dep'])

foreach src : srcs
  executable(src, '@0@.c'.format(src),
    c_args : args,
    include_directories : incs,
    dependencies : [
      glib_dep, 
      gst_dep, 
      gstrtsp_dep, 
      gstrtsp_server_dep
      ],
    install: false)
endforeach
