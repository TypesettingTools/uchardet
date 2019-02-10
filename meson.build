project('uchardet', ['c', 'cpp'], license: 'MPL1.1',
        meson_version: '>=0.49.0',
        default_options: ['cpp_std=c++11'],
        version: '0.0.6')

cc = meson.get_compiler('c')
cxx = meson.get_compiler('cpp')

if host_machine.cpu_family().startswith('x86')
    # this all does not work properly with msvc
    if cc.get_argument_syntax() == 'msvc'
        sse2_flags = ['arch:SSE2']
    else
        sse2_flags = ['-msee2', '-mfpmath=sse']
    endif
    cflags = cc.get_supported_arguments(sse2_flags)
    if get_option('check-sse2') and cflags.length() != 0
        add_project_arguments(cflags, language: 'c')
        add_project_arguments(cxx.get_supported_arguments(sse2_flags), language: 'cpp')
    else
        add_project_arguments(cc.get_supported_arguments('-ffloat-store'), language: 'c')
        add_project_arguments(cxx.get_supported_arguments('-ffloat-store'), language: 'cpp')
    endif
endif

subdir('src')
#subdir('doc')
#subdir('test')

pkg = import('pkgconfig')
pkg.generate(uchardet, 
             description: 'An encoding detector library ported from Mozilla',
             url: 'https://www.freedesktop.org/wiki/Software/uchardet/',
             subdirs: meson.project_name())
