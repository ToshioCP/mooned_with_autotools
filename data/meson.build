conf_data = configuration_data()
conf_data.set('datadir', get_option('prefix') / get_option('datadir'))
configure_file(input : 'mooned.desktop.in', output : 'mooned.desktop', configuration : conf_data, install_dir: get_option('datadir') / 'applications')

install_data('mooned.png', install_dir: get_option('datadir') / 'icons' / 'hicolor' / '48x48' / 'apps')
