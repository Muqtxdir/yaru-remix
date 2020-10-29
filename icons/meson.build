install_subdir('Yaru-remix',
    install_dir: join_paths(get_option('prefix'), 'share/icons')
)

install_subdir('Yaru-remix-dark',
    install_dir: join_paths(get_option('prefix'), 'share/icons')
)

install_subdir('Yaru-remix-light',
    install_dir: join_paths(get_option('prefix'), 'share/icons')
)

meson.add_install_script('meson/post_install.py', 'Yaru-remix')
meson.add_install_script('meson/post_install.py', 'Yaru-remix-dark')
meson.add_install_script('meson/post_install.py', 'Yaru-remix-light')
