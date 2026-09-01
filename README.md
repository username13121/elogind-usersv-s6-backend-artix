# Native s6 backend for elogind-usersv on Artix

This repository packages `elogind-usersv-backend-s6`. It is an Artix-specific
`elogind-usersv` backend that invokes `s6` and `s6-rc` directly. It does not use
or depend on `s6-frontend`.

The backend is selected in `/etc/elogind-usersv/config.toml` with:

```toml
backend = "s6"
```

It installs the backend at:

```text
/usr/libexec/elogind-usersv/backends/s6
```

Its fixed path policy is:

```text
/etc/s6/user/sv
/etc/s6/user/adminsv
$XDG_CONFIG_HOME/s6/sv
$XDG_STATE_HOME/s6/repo
$XDG_STATE_HOME/s6/rc/compiled
$XDG_RUNTIME_DIR/s6-rc
$XDG_RUNTIME_DIR/service
```

Build and install as a normal user:

```sh
makepkg -Csi
```
