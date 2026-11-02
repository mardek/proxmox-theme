Proxmox white/purple theme backup (20261020-005923)
=======================================
Files:
  custom.css               -> /usr/share/pve-manager/css/custom.css
  index.html.tpl           -> /usr/share/pve-manager/index.html.tpl (adds the custom.css <link>)
  pve-custom-css-restore   -> /usr/local/sbin/pve-custom-css-restore (chmod +x)
  80pvecustomcss-hook      -> /etc/apt/apt.conf.d/80pvecustomcss-hook

To restore after a PVE update wipes the theme:
  cp custom.css /usr/share/pve-manager/css/custom.css
  cp index.html.tpl /usr/share/pve-manager/index.html.tpl
  cp pve-custom-css-restore /usr/local/sbin/pve-custom-css-restore && chmod +x /usr/local/sbin/pve-custom-css-restore
  cp 80pvecustomcss-hook /etc/apt/apt.conf.d/
  systemctl restart pveproxy
Note: the cache-buster version (custom.css?v=N) must match what is in index.html.tpl.
