+++
title = "cli_tools"
outputs = ["Reveal"]
[logowg]
src = "/img/wg_white_removed_medium.png"
alt = "WestGrid logo"
[logocc]
src = "/img/cc_regional_partner_brown_large.png"
alt = "Compute Canada logo"
[reveal_hugo]
custom_theme = "mh.scss"
custom_theme_compile = true
+++

<br>
<br>

<!-- # Fun tools to make your life in the command line easier -->

<!-- ![logo](/img/terminal.png) -->

![](/img/cli_title.png)

#### <center>Marie-Hélène Burle</center>

##### <center><marie.burle@westgrid.ca></center>

###### <center>*February 19, 2020*</center>

---

# <center>fzf: fuzzy finder</center>

<br>

[![logo](/img/fzf.png)](https://github.com/junegunn/fzf)

---

<center>Many commands return long outputs</center>

---

Example: get running processes

<br>
```sh
ps -ef
```

---

<br>

```sh
UID          PID    PPID  C STIME TTY          TIME CMD
root           1       0  0 Jan06 ?        00:00:16 /sbin/init
root           2       0  0 Jan06 ?        00:00:00 [kthreadd]
root           3       2  0 Jan06 ?        00:00:00 [rcu_gp]
root           4       2  0 Jan06 ?        00:00:00 [rcu_par_gp]
root           6       2  0 Jan06 ?        00:00:00 [kworker/0:0H-kblockd]
root           8       2  0 Jan06 ?        00:00:00 [mm_percpu_wq]
root           9       2  0 Jan06 ?        00:00:00 [ksoftirqd/0]
root          10       2  0 Jan06 ?        00:00:00 [rcuc/0]
root          11       2  0 Jan06 ?        00:00:04 [rcu_preempt]
root          12       2  0 Jan06 ?        00:00:00 [rcub/0]
root          13       2  0 Jan06 ?        00:00:00 [migration/0]
root          14       2  0 Jan06 ?        00:00:00 [idle_inject/0]
root          16       2  0 Jan06 ?        00:00:00 [cpuhp/0]
root          17       2  0 Jan06 ?        00:00:00 [cpuhp/1]
root          18       2  0 Jan06 ?        00:00:00 [idle_inject/1]
root          19       2  0 Jan06 ?        00:00:00 [migration/1]
root          20       2  0 Jan06 ?        00:00:00 [rcuc/1]
root          21       2  0 Jan06 ?        00:00:01 [ksoftirqd/1]
root          23       2  0 Jan06 ?        00:00:00 [kworker/1:0H-kblockd]
root          24       2  0 Jan06 ?        00:00:00 [cpuhp/2]
root          25       2  0 Jan06 ?        00:00:00 [idle_inject/2]
root          26       2  0 Jan06 ?        00:00:00 [migration/2]
root          27       2  0 Jan06 ?        00:00:00 [rcuc/2]
root          28       2  0 Jan06 ?        00:00:01 [ksoftirqd/2]
root          30       2  0 Jan06 ?        00:00:00 [kworker/2:0H-kblockd]
root          31       2  0 Jan06 ?        00:00:00 [cpuhp/3]
root          32       2  0 Jan06 ?        00:00:00 [idle_inject/3]
root          33       2  0 Jan06 ?        00:00:00 [migration/3]
root          34       2  0 Jan06 ?        00:00:00 [rcuc/3]
root          35       2  0 Jan06 ?        00:00:00 [ksoftirqd/3]
root          37       2  0 Jan06 ?        00:00:00 [kworker/3:0H-kblockd]
root          38       2  0 Jan06 ?        00:00:00 [kdevtmpfs]
root          39       2  0 Jan06 ?        00:00:00 [netns]
root          40       2  0 Jan06 ?        00:00:00 [rcu_tasks_kthre]
root          41       2  0 Jan06 ?        00:00:00 [kauditd]
root          44       2  0 Jan06 ?        00:00:00 [khungtaskd]
root          45       2  0 Jan06 ?        00:00:00 [oom_reaper]
root          46       2  0 Jan06 ?        00:00:00 [writeback]
root          47       2  0 Jan06 ?        00:00:00 [kcompactd0]
root          48       2  0 Jan06 ?        00:00:00 [ksmd]
root          49       2  0 Jan06 ?        00:00:00 [khugepaged]
root         138       2  0 Jan06 ?        00:00:00 [kintegrityd]
root         139       2  0 Jan06 ?        00:00:00 [kblockd]
root         140       2  0 Jan06 ?        00:00:00 [blkcg_punt_bio]
root         141       2  0 Jan06 ?        00:00:00 [edac-poller]
root         142       2  0 Jan06 ?        00:00:00 [devfreq_wq]
root         144       2  0 Jan06 ?        00:00:00 [watchdogd]
root         145       2  0 Jan06 ?        00:00:00 [kswapd0]
root         148       2  0 Jan06 ?        00:00:00 [kthrotld]
root         149       2  0 Jan06 ?        00:00:00 [acpi_thermal_pm]
root         150       2  0 Jan06 ?        00:00:00 [nvme-wq]
root         151       2  0 Jan06 ?        00:00:00 [nvme-reset-wq]
root         152       2  0 Jan06 ?        00:00:00 [nvme-delete-wq]
root         154       2  0 Jan06 ?        00:00:00 [ipv6_addrconf]
root         165       2  0 Jan06 ?        00:00:00 [kstrp]
root         182       2  0 Jan06 ?        00:00:00 [charger_manager]
root         219       2  0 Jan06 ?        00:00:00 [sdhci]
root         222       2  0 Jan06 ?        00:00:00 [ata_sff]
root         224       2  0 Jan06 ?        00:00:00 [scsi_eh_0]
root         225       2  0 Jan06 ?        00:00:00 [scsi_tmf_0]
root         226       2  0 Jan06 ?        00:00:00 [scsi_eh_1]
root         227       2  0 Jan06 ?        00:00:00 [scsi_tmf_1]
root         232       2  0 Jan06 ?        00:00:00 [kworker/3:1H-events_highpri]
root         234       2  0 Jan06 ?        00:00:00 [kworker/1:1H-events_highpri]
root         238       2  0 Jan06 ?        00:00:00 [kworker/0:1H-kblockd]
root         243       2  0 Jan06 ?        00:00:00 [kworker/2:1H-kblockd]
root         248       2  0 Jan06 ?        00:00:00 [jbd2/sda1-8]
root         249       2  0 Jan06 ?        00:00:00 [ext4-rsv-conver]
root         274       1  0 Jan06 ?        00:00:01 /usr/lib/systemd/systemd-journald
root         279       1  0 Jan06 ?        00:00:00 /usr/bin/lvmetad -f
root         286       1  0 Jan06 ?        00:00:00 /usr/lib/systemd/systemd-udevd
root         311       2  0 Jan06 ?        00:00:00 [irq/18-smo8800]
root         327       2  0 Jan06 ?        00:00:00 [cfg80211]
root         328       2  0 Jan06 ?        00:00:00 [e1000e]
root         337       2  0 Jan06 ?        00:00:00 [cryptd]
root         351       2  0 Jan06 ?        00:00:00 [jbd2/sda3-8]
root         354       2  0 Jan06 ?        00:00:18 [irq/50-iwlwifi]
root         356       2  0 Jan06 ?        00:00:00 [ext4-rsv-conver]
root         358       2  0 Jan06 ?        00:00:01 [jbd2/sda4-8]
root         359       2  0 Jan06 ?        00:00:00 [ext4-rsv-conver]
avahi        451       1  0 Jan06 ?        00:00:00 avahi-daemon: running [prosoitos.local]
bitlbee      452       1  0 Jan06 ?        00:00:00 /usr/bin/bitlbee -F -n
root         453       1  0 Jan06 ?        00:00:00 /usr/lib/bluetooth/bluetoothd
root         454       1  0 Jan06 ?        00:00:00 /usr/bin/crond -n
dbus         455       1  0 Jan06 ?        00:00:02 /usr/bin/dbus-daemon --system --address=systemd: --nofork --nopidfile --systemd-activation --syslog-only
root         459       1  0 Jan06 ?        00:01:27 /usr/bin/thermald --no-daemon --dbus-enable
avahi        463     451  0 Jan06 ?        00:00:00 avahi-daemon: chroot helper
root         488       1  0 Jan06 ?        00:00:02 /usr/bin/ifplugd -i eno1 -r /etc/ifplugd/netctl.action -bfIns
root         534       1  0 Jan06 ?        00:00:09 /usr/lib/systemd/systemd-logind
root         583       1  0 Jan06 ?        00:00:01 wpa_supplicant -q -B -P /run/wpa_supplicant-wlp2s0.pid -i wlp2s0 -D nl80211,wext -c/run/netctl/wpa_supplicant-wlp2s0.conf -W
root         587       1  0 Jan06 ?        00:00:01 wpa_cli -i wlp2s0 -p /run/wpa_supplicant -B -a /usr/lib/netctl/auto.action
root         590       1  0 Jan06 ?        00:00:00 /usr/bin/cupsd -l
ntp          593       1  0 Jan06 ?        00:00:03 /usr/bin/ntpd -g -u ntp:ntp
dnsmasq      594       1  0 Jan06 ?        00:00:00 /usr/bin/dnsmasq -k --enable-dbus --user=dnsmasq --pid-file
root         596       1  0 Jan06 ?        00:00:00 login -- marie
colord       597       1  0 Jan06 ?        00:00:00 /usr/lib/colord
marie        696       1  0 Jan06 ?        00:00:00 /usr/lib/systemd/systemd --user
marie        697     696  0 Jan06 ?        00:00:00 (sd-pam)
marie        704       1  0 Jan06 ?        00:00:00 /usr/bin/gnome-keyring-daemon --daemonize --login
marie        707     596  0 Jan06 tty1     00:00:00 -zsh
marie        773     707  0 Jan06 tty1     00:00:00 /bin/sh /usr/bin/startx
marie        795     773  0 Jan06 tty1     00:00:00 xinit /home/marie/.xinitrc -- /home/marie/.xserverrc :0 vt1 -keeptty -auth /tmp/serverauth.RZgy5sMtHq
marie        796     795  0 Jan06 tty1     00:03:03 /usr/lib/Xorg -nolisten tcp :0 vt1 -keeptty -auth /tmp/serverauth.RZgy5sMtHq vt1
root         798     796  0 Jan06 tty1     00:00:00 xf86-video-intel-backlight-helper intel_backlight
marie        804     795  0 Jan06 tty1     00:00:32 i3
marie        815     696  0 Jan06 ?        00:00:00 /usr/bin/dbus-daemon --session --address=systemd: --nofork --nopidfile --systemd-activation --syslog-only
marie        816     804  0 Jan06 tty1     00:00:05 bash /usr/bin/clipmenud
marie        817     804  0 Jan06 tty1     00:00:01 artha
marie        818     804  0 Jan06 tty1     00:02:30 /usr/bin/python /usr/bin/autokey-gtk
marie        819     804  0 Jan06 tty1     00:00:07 redshift
marie        820     804  0 Jan06 tty1     00:00:01 pasystray -t --notify=all
marie        821     804  0 Jan06 tty1     00:00:00 mictray
marie        822     804  0 Jan06 tty1     00:00:02 twmnd
marie        828       1  0 Jan06 ?        00:00:00 ssh-agent
marie        843     696  0 Jan06 ?        00:00:00 /usr/lib/at-spi-bus-launcher
marie        849     843  0 Jan06 ?        00:00:00 /usr/bin/dbus-daemon --config-file=/usr/share/defaults/at-spi2/accessibility.conf --nofork --print-address 3
marie        851     696  0 Jan06 ?        00:00:32 /usr/bin/pulseaudio --daemonize=no
marie        853     696  0 Jan06 ?        00:00:04 /usr/lib/at-spi2-registryd --use-gnome-session
marie        860       1  2 Jan06 ?        00:37:25 /usr/bin/python3 /usr/bin/qutebrowser
marie        861       1  0 Jan06 ?        00:00:16 i3bar --bar_id=bar-0 --socket=/run/user/1000/i3/ipc-socket.804
marie        864       1  0 Jan06 ?        00:04:56 emacs
marie        866       1  0 Jan06 ?        00:00:00 urxvt
marie        868       1  0 Jan06 ?        00:00:01 urxvt
marie        869       1  0 Jan06 ?        00:00:01 urxvt
rtkit        871       1  0 Jan06 ?        00:00:00 /usr/lib/rtkit-daemon
marie        872     861  0 Jan06 ?        00:01:21 i3status
polkitd      875       1  0 Jan06 ?        00:00:01 /usr/lib/polkit-1/polkitd --no-debug
marie        877     869  0 Jan06 pts/0    00:00:00 zsh
marie        888     868  0 Jan06 pts/1    00:00:08 zsh
marie        889     866  0 Jan06 pts/2    00:00:02 zsh
marie       1012     851  0 Jan06 ?        00:00:00 /usr/lib/pulse/gsettings-helper
root        1031       2  0 Jan06 ?        00:00:00 [krfcommd]
marie       1066     860  0 Jan06 ?        00:00:00 /usr/lib/qt/libexec/QtWebEngineProcess --type=zygote --webengine-schemes=qute:lL;qrc:sLV --lang=en-CA
marie       1068    1066  0 Jan06 ?        00:00:00 /usr/lib/qt/libexec/QtWebEngineProcess --type=zygote --webengine-schemes=qute:lL;qrc:sLV --lang=en-CA
```
{{% fragment %}}
Not very user friendly.\\
Depending on settings, it might not even be possible to scroll up to the line of interest.
{{% /fragment %}}

---

Classic tool to make this more friendly: `less`

<br>
```sh
ps -ef | less
```

---

<br>
<br>

```sh
UID          PID    PPID  C STIME TTY          TIME CMD
root           1       0  0 Jan06 ?        00:00:16 /sbin/init
root           2       0  0 Jan06 ?        00:00:00 [kthreadd]
root           3       2  0 Jan06 ?        00:00:00 [rcu_gp]
root           4       2  0 Jan06 ?        00:00:00 [rcu_par_gp]
root           6       2  0 Jan06 ?        00:00:00 [kworker/0:0H-kblockd]
root           8       2  0 Jan06 ?        00:00:00 [mm_percpu_wq]
root           9       2  0 Jan06 ?        00:00:00 [ksoftirqd/0]
root          10       2  0 Jan06 ?        00:00:00 [rcuc/0]
root          11       2  0 Jan06 ?        00:00:04 [rcu_preempt]
root          12       2  0 Jan06 ?        00:00:00 [rcub/0]
root          13       2  0 Jan06 ?        00:00:00 [migration/0]
root          14       2  0 Jan06 ?        00:00:00 [idle_inject/0]
:
```

{{% fragment %}} - allows to view output one screen at a time {{% /fragment %}}

{{% fragment %}} - allows easy searching {{% /fragment %}}

---

But `fzf` allows much more:

<br>
```sh
ps -ef | fzf
```

---

<br>

<center>Let's go to a terminal:</center>
<br>
![logo](/img/cli.png)

---

```sh
ih() {				# fzf history
	print -z $( ([ -n "$ZSH_NAME" ] && fc -l 1 || history) |
					fzf -i -e +s --tac |
					sed 's/ *[0-9]* *//')
}
```

---

```sh
ik() {				# fzf kill process
	local pid
	if [ "$UID" != "0" ]; then
		pid=$(ps -f -u $UID |
				  sed 1d |
				  fzf -i -e -m |
				  awk '{print $2}')
	else
		pid=$(ps -ef |
				  sed 1d |
				  fzf -i -e -m |
				  awk '{print $2}')
	fi
}
```

---

```sh
gcop() {			# git commit check with preview and copy hash
	glNoGraph |
		fzf -i -e --no-sort --reverse --tiebreak=index --no-multi \
			--ansi --preview="$_viewGitLogLine" \
			--header "enter: view, M-y: copy hash" \
			--bind "enter:execute:$_viewGitLogLine   |
            less -R" \
			--bind "alt-y:execute:$_gitLogLineToHash |
            xclip -r -selection clipboard"
}
```

---

```sh
alias ka='egrep "^alias\ |^.*\(\)" $ZSH_CUSTOM/alias.zsh | fzf -i -e +s'
```

```sh
alias ke='grep -A 1 "(kbd .*)" $HOME/.emacs | fzf -i -e +s'
```


alias kr='egrep "^map\ " $HOME/.config/ranger/rc.conf | fzf -i -e +s'


---

# <center>autojump: smart cd</center>

<br>

[![logo](/img/autojump.png)](https://github.com/wting/autojump)

---

# <center>ranger: file manager</center>

<br>

[![logo](/img/ranger.png)](https://github.com/ranger/ranger)

---

https://github.com/jarun/nnn
https://github.com/gokcehan/lf
https://github.com/dylanaraps/fff

---

https://github.com/jonas/tig
https://github.com/BurntSushi/ripgrep
https://github.com/ggreer/the_silver_searcher
