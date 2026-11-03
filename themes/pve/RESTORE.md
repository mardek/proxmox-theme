Proxmox white/purple theme backup (20261020-005923)
=======================================
Files:
  custom.css               -> /usr/share/pve-manager/css/custom.css
  custom-dark.css          -> /usr/share/pve-manager/css/custom-dark.css
  index.html.tpl           -> /usr/share/pve-manager/index.html.tpl (adds the custom stylesheet <link> elements)
  pve-custom-css-restore   -> /usr/local/sbin/pve-custom-css-restore (chmod +x)
  80pvecustomcss-hook      -> /etc/apt/apt.conf.d/80pvecustomcss-hook

To restore after a PVE update wipes the theme:
  cp custom.css custom-dark.css /usr/share/pve-manager/css/
  cp index.html.tpl /usr/share/pve-manager/index.html.tpl
  cp pve-custom-css-restore /usr/local/sbin/pve-custom-css-restore && chmod +x /usr/local/sbin/pve-custom-css-restore
  cp 80pvecustomcss-hook /etc/apt/apt.conf.d/
  systemctl restart pveproxy

The dark stylesheet is loaded for the explicit Proxmox Dark theme and for Auto
when the operating system prefers dark mode.
Note: the cache-buster versions (custom.css?v=N and custom-dark.css?v=N) must match what is in index.html.tpl.
