cmake_minimum_required(VERSION 3.2)
project(uwsgi_py)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")

include_directories(/System/Library/Frameworks/Python.framework/Versions/2.7/include/python2.7 .)
set(SOURCE_FILES uwsgi_main.c uwsgi.h)
add_executable(uwsgi_py ${SOURCE_FILES} core/alarm.c core/errors.c core/legion.c core/offload.c core/sendfile.c core/strings.c
                                     core/async.c core/event.c core/lock.c core/plugins.c core/setup_utils.c core/subscription.c
                                     core/buffer.c core/exceptions.c core/logging.c core/plugins_builder.c  core/sharedarea.c core/timebomb.c
                                     core/cache.c core/fifo.c core/loop.c core/progress.c core/signal.c core/transformations.c
                                     core/chunked.c core/fsmon.c core/master.c core/protocol.c core/skel.c core/utils.c
                                     core/clang_fake.c core/gateway.c core/master_checks.c core/querystring.c core/snmp.c core/uwsgi.c
                                     core/clock.c core/hash.c core/master_events.c core/queue.c core/socket.c core/websockets.c
                                     core/config.c core/hooks.c core/master_utils.c core/rb_timers.c core/spooler.c core/writer.c
                                     core/cookie.c core/ini.c core/metrics.c core/reader.c core/ssl.c core/xmlconf.c
                                     core/cron.c core/init.c core/mount.c core/regexp.c core/static.c core/yaml.c
                                     core/daemons.c core/io.c core/ core/mule.c core/routing.c core/stats.c core/zeus.c
                                     core/emperor.c core/json.c core/notify.c core/rpc.c core/storage.c core/zlib.c
                                     plugins/python/gil.c plugins/python/pyloader.c plugins/python/raw.c 
                                     plugins/python/uwsgi_pymodule.c  plugins/python/wsgi_headers.c 
                                     plugins/python/profiler.c plugins/python/python_plugin.c 
                                     plugins/python/symimporter.c plugins/python/web3_subhandler.c 
                                     plugins/python/wsgi_subhandler.c plugins/python/pump_subhandler.c 
                                     plugins/python/pyutils.c plugins/python/tracebacker.c 
                                     plugins/python/wsgi_handlers.c)                                     