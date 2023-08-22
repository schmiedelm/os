<p align="center">
  <a href="#build-framework">
   <img src="https://raw.githubusercontent.com/armbian/build/master/.github/armbian-logo.png" alt="Armbian logo" width="144">
  </a><br>
  <strong>Armbian OS</strong><br>
<br>
<a href=https://github.com/armbian/os/actions/workflows/complete-artifact-matrix-all.yml><img alt="GitHub Workflow Status" src="https://img.shields.io/github/actions/workflow/status/armbian/os/complete-artifact-matrix-all.yml?logo=githubactions&label=Artifacts%20make&style=for-the-badge&branch=main"></a>
<a href=https://github.com/armbian/os/actions/workflows/repository-update.yml><img alt="GitHub Workflow Status" src="https://img.shields.io/github/actions/workflow/status/armbian/os/repository-update.yml?logo=githubactions&label=Repository%20update&style=for-the-badge&branch=main"></a>
<a href=https://github.com/armbian/os#latest-smoke-tests-results><img alt="GitHub Workflow Status" src="https://img.shields.io/github/actions/workflow/status/armbian/os/smoke-tests.yml?logo=githubactions&label=Smoke%20tests&style=for-the-badge&branch=main"></a>
</p>


# What does this project do?

- Keeps build framework [packages artifacts](https://github.com/orgs/armbian/packages) cache up to date
- Keeps stable [apt.armbian.com](https://apt.armbian.com) and nightly [beta.armbian.com](https://beta.armbian.com) packages repository up to date
- Builds [nightly](https://github.com/armbian/os/releases) and [stable images](https://www.armbian.com/download/) and uploads them to Armbian CDN
- Keep synchronizing the selection of [3rd party](external) applications with Armbian repositories
- Tests install of all packages added onto stable and testing Debian and Ubuntu releases

# How to enable images?

If you want to enable build configurations, edit [yaml config files](userpatches) and send a pull request. ([example](https://github.com/armbian/os/commit/70f3be4f3d96e9a301be751d3ecf3a24394356f9) )

# When is this happening?

- Artifacts cache is updated every eight hours, starting at 0:00 AM UTC
- Repository update starts after **artifacts cache update** is done succesfully.
- Smoke tests starts after **repository update** is done succesfully.
- Nightly images are build once per day, at 5:00 AM UTC, or if [build config is changed](https://github.com/armbian/os/blob/main/userpatches/targets-release-nightly.yaml)
- Manually, when Armbian [release manager](https://github.com/orgs/armbian/teams/release-manager) executes a build action

# Latest smoke tests results:

- installs kernels, dtb and headers that are defined and supported by the board
- runs network and computing performance tests (7z benchmark)
- store armbianmonitor logs

<!--START_SECTION:data-section-->
<table width="100%"><tr><td align="left"><a href=""><b>Board name</b></a></td><td align="left"><b>Started</b></td><td align=right><b>Kernel version</b></td><td align=right><b>Iperf</b></td><td align=right><b>7z -b</b></td></tr><tr><td align="left"><a href="https://paste.armbian.com/kovudatude">Orange Pi Win</a></td><td align="left">2023-08-22&nbsp;10:36:53</td><td align=right>6.1.46-current-sunxi64</td><td align=right>674</td><td align=right>2883</td></tr><tr><td align="left"><a href="https://paste.armbian.com/oducikapeb">Orange Pi Win</a></td><td align="left">2023-08-22&nbsp;10:50:13</td><td align=right>5.15.93-sunxi64</td><td align=right>688</td><td align=right>2492</td></tr><tr><td align="left"><a href="https://paste.armbian.com/oducikapeb">Orange Pi Win</a></td><td align="left">2023-08-22&nbsp;11:18:18</td><td align=right>5.15.93-sunxi64</td><td align=right>688</td><td align=right>2492</td></tr><tr><td align="left"><a href="https://paste.armbian.com/oducikapeb">Orange Pi Win</a></td><td align="left">2023-08-22&nbsp;11:18:19</td><td align=right>5.15.93-sunxi64</td><td align=right>688</td><td align=right>2492</td></tr><tr><td align="left"><a href="https://paste.armbian.com/ebikuvumel">Espressobin</a></td><td align="left">2023-08-22&nbsp;10:46:43</td><td align=right>5.15.127-current-mvebu64</td><td align=right>860</td><td align=right>1016</td></tr><tr><td align="left"><a href="https://paste.armbian.com/eregulumuv">Espressobin</a></td><td align="left">2023-08-22&nbsp;11:10:11</td><td align=right>5.15.93-mvebu64</td><td align=right>796</td><td align=right>1005</td></tr><tr><td align="left"><a href="https://paste.armbian.com/heniteyulu">Pine H64</a></td><td align="left">2023-08-22&nbsp;10:33:19</td><td align=right>6.1.46-current-sunxi64</td><td align=right>942</td><td align=right>3729</td></tr><tr><td align="left"><a href="https://paste.armbian.com/roguqegupu">Pine H64</a></td><td align="left">2023-08-22&nbsp;10:43:56</td><td align=right>5.15.93-sunxi64</td><td align=right>853</td><td align=right>3602</td></tr><tr><td align="left"><a href="https://paste.armbian.com/qusebulero">Pine H64</a></td><td align="left">2023-08-22&nbsp;10:53:39</td><td align=right>6.4.11-edge-sunxi64</td><td align=right>831</td><td align=right>3540</td></tr><tr><td align="left"><a href="https://paste.armbian.com/zibijekela">Pine H64</a></td><td align="left">2023-08-22&nbsp;11:04:28</td><td align=right>6.1.11-sunxi64</td><td align=right>809</td><td align=right>3489</td></tr><tr><td align="left"><a href="n/a">UEFI x86</a></td><td align="left">2023-08-22&nbsp;10:24:28</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">UEFI x86</a></td><td align="left">2023-08-22&nbsp;10:24:29</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">UEFI x86</a></td><td align="left">2023-08-22&nbsp;10:24:29</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">UEFI x86</a></td><td align="left">2023-08-22&nbsp;10:24:30</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">UEFI x86</a></td><td align="left">2023-08-22&nbsp;10:24:31</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">UEFI x86</a></td><td align="left">2023-08-22&nbsp;10:24:32</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="https://paste.armbian.com/enifesuhiy">RockPro 64</a></td><td align="left">2023-08-22&nbsp;10:30:52</td><td align=right>6.1.46-current-rockchip64</td><td align=right>890</td><td align=right>6413</td></tr><tr><td align="left"><a href="https://paste.armbian.com/upewodedar">RockPro 64</a></td><td align="left">2023-08-22&nbsp;10:37:49</td><td align=right>5.15.93-rockchip64</td><td align=right>890</td><td align=right>6447</td></tr><tr><td align="left"><a href="https://paste.armbian.com/kaqurutozo">RockPro 64</a></td><td align="left">2023-08-22&nbsp;10:44:37</td><td align=right>6.4.11-edge-rockchip64</td><td align=right>890</td><td align=right>6527</td></tr><tr><td align="left"><a href="https://paste.armbian.com/ahonuteboj">RockPro 64</a></td><td align="left">2023-08-22&nbsp;10:51:37</td><td align=right>6.1.11-rockchip64</td><td align=right>858</td><td align=right>6455</td></tr><tr><td align="left"><a href="https://paste.armbian.com/romoqonawi">Rockpi E</a></td><td align="left">2023-08-22&nbsp;10:39:44</td><td align=right>6.1.46-current-rockchip64</td><td align=right>90</td><td align=right>3341</td></tr><tr><td align="left"><a href="https://paste.armbian.com/dinafisole">Rockpi E</a></td><td align="left">2023-08-22&nbsp;10:53:15</td><td align=right>5.15.93-rockchip64</td><td align=right>90</td><td align=right>2840</td></tr><tr><td align="left"><a href="https://paste.armbian.com/iwusukepiq">Rockpi E</a></td><td align="left">2023-08-22&nbsp;11:07:29</td><td align=right>6.4.11-edge-rockchip64</td><td align=right>90</td><td align=right>3276</td></tr><tr><td align="left"><a href="https://paste.armbian.com/xatadokize">Rockpi E</a></td><td align="left">2023-08-22&nbsp;11:21:41</td><td align=right>6.1.11-rockchip64</td><td align=right>90</td><td align=right>2837</td></tr><tr><td align="left"><a href="https://paste.armbian.com/ibihayudaw">Odroid C2</a></td><td align="left">2023-08-22&nbsp;10:34:19</td><td align=right>6.1.46-current-meson64</td><td align=right>810</td><td align=right>3960</td></tr><tr><td align="left"><a href="https://paste.armbian.com/irapojahew">Odroid C2</a></td><td align="left">2023-08-22&nbsp;10:45:38</td><td align=right>6.1.11-meson64</td><td align=right>890</td><td align=right>4039</td></tr><tr><td align="left"><a href="https://paste.armbian.com/posazebadi">Odroid C2</a></td><td align="left">2023-08-22&nbsp;10:56:00</td><td align=right>6.4.11-edge-meson64</td><td align=right>799</td><td align=right>4031</td></tr><tr><td align="left"><a href="https://paste.armbian.com/ebolomufev">Odroid C2</a></td><td align="left">2023-08-22&nbsp;11:07:15</td><td align=right>6.2.0-rc3-meson64</td><td align=right>860</td><td align=right>4045</td></tr><tr><td align="left"><a href="https://paste.armbian.com/bobiyuyenu">NanoPi R6S</a></td><td align="left">2023-08-22&nbsp;10:27:35</td><td align=right>5.10.160-legacy-rk35xx</td><td align=right>2440</td><td align=right>15892</td></tr><tr><td align="left"><a href="https://paste.armbian.com/sunuqakuso">Orange Pi 3 LTS</a></td><td align="left">2023-08-22&nbsp;10:33:01</td><td align=right>6.1.46-current-sunxi64</td><td align=right>870</td><td align=right>3819</td></tr><tr><td align="left"><a href="https://paste.armbian.com/ukebanumij">Orange Pi 3 LTS</a></td><td align="left">2023-08-22&nbsp;10:43:11</td><td align=right>5.15.93-sunxi64</td><td align=right>866</td><td align=right>3810</td></tr><tr><td align="left"><a href="https://paste.armbian.com/suxokojure">Orange Pi 3 LTS</a></td><td align="left">2023-08-22&nbsp;10:52:20</td><td align=right>6.4.11-edge-sunxi64</td><td align=right>867</td><td align=right>3786</td></tr><tr><td align="left"><a href="https://paste.armbian.com/zijotubomo">Orange Pi 3 LTS</a></td><td align="left">2023-08-22&nbsp;11:02:30</td><td align=right>6.1.11-sunxi64</td><td align=right>838</td><td align=right>3805</td></tr><tr><td align="left"><a href="https://paste.armbian.com/apehunamuz">Odroid C4</a></td><td align="left">2023-08-22&nbsp;10:31:45</td><td align=right>6.1.46-current-meson64</td><td align=right>880</td><td align=right>5611</td></tr><tr><td align="left"><a href="https://paste.armbian.com/uvinohazop">Odroid C4</a></td><td align="left">2023-08-22&nbsp;10:40:29</td><td align=right>6.1.11-meson64</td><td align=right>890</td><td align=right>5683</td></tr><tr><td align="left"><a href="https://paste.armbian.com/owaxusofaz">Odroid C4</a></td><td align="left">2023-08-22&nbsp;10:48:37</td><td align=right>6.4.11-edge-meson64</td><td align=right>890</td><td align=right>5635</td></tr><tr><td align="left"><a href="https://paste.armbian.com/roxolibobo">Odroid C4</a></td><td align="left">2023-08-22&nbsp;10:57:18</td><td align=right>6.2.0-rc3-meson64</td><td align=right>890</td><td align=right>5627</td></tr><tr><td align="left"><a href="https://paste.armbian.com/lodapunale">Rockpi 4B</a></td><td align="left">2023-08-22&nbsp;10:31:17</td><td align=right>6.1.46-current-rockchip64</td><td align=right>890</td><td align=right>6433</td></tr><tr><td align="left"><a href="https://paste.armbian.com/ujufamakig">Rockpi 4B</a></td><td align="left">2023-08-22&nbsp;10:38:48</td><td align=right>5.15.93-rockchip64</td><td align=right>888</td><td align=right>6182</td></tr><tr><td align="left"><a href="https://paste.armbian.com/robupukano">Rockpi 4B</a></td><td align="left">2023-08-22&nbsp;10:46:22</td><td align=right>6.4.11-edge-rockchip64</td><td align=right>890</td><td align=right>6163</td></tr><tr><td align="left"><a href="https://paste.armbian.com/lomoqacota">Rockpi 4B</a></td><td align="left">2023-08-22&nbsp;10:53:42</td><td align=right>6.1.11-rockchip64</td><td align=right>967</td><td align=right>6157</td></tr><tr><td align="left"><a href="https://paste.armbian.com/exucijegug">NanoPi M4</a></td><td align="left">2023-08-22&nbsp;10:30:57</td><td align=right>6.1.46-current-rockchip64</td><td align=right>890</td><td align=right>6683</td></tr><tr><td align="left"><a href="https://paste.armbian.com/mokehigiqu">NanoPi M4</a></td><td align="left">2023-08-22&nbsp;10:38:15</td><td align=right>5.15.93-rockchip64</td><td align=right>890</td><td align=right>6744</td></tr><tr><td align="left"><a href="https://paste.armbian.com/ovuriwasur">NanoPi M4</a></td><td align="left">2023-08-22&nbsp;10:45:14</td><td align=right>6.4.11-edge-rockchip64</td><td align=right>890</td><td align=right>6693</td></tr><tr><td align="left"><a href="https://paste.armbian.com/heyifaxuwa">NanoPi M4</a></td><td align="left">2023-08-22&nbsp;10:52:16</td><td align=right>6.1.11-rockchip64</td><td align=right>906</td><td align=right>6695</td></tr><tr><td align="left"><a href="https://paste.armbian.com/wazanonane">Banana Pi Pro</a></td><td align="left">2023-08-22&nbsp;10:38:04</td><td align=right>6.1.46-current-sunxi</td><td align=right>430</td><td align=right>1010</td></tr><tr><td align="left"><a href="https://paste.armbian.com/obowujirum">Banana Pi Pro</a></td><td align="left">2023-08-22&nbsp;10:53:35</td><td align=right>5.15.93-sunxi</td><td align=right>319</td><td align=right>1025</td></tr><tr><td align="left"><a href="https://paste.armbian.com/qihamivopu">Banana Pi Pro</a></td><td align="left">2023-08-22&nbsp;11:08:13</td><td align=right>6.4.11-edge-sunxi</td><td align=right>594</td><td align=right>1010</td></tr><tr><td align="left"><a href="https://paste.armbian.com/nigupuxuta">ZeroPi</a></td><td align="left">2023-08-22&nbsp;10:34:17</td><td align=right>5.15.127-legacy-sunxi</td><td align=right>524</td><td align=right>2651</td></tr><tr><td align="left"><a href="https://paste.armbian.com/esefusevul">ZeroPi</a></td><td align="left">2023-08-22&nbsp;10:42:21</td><td align=right>5.15.127-legacy-sunxi</td><td align=right>553</td><td align=right>2653</td></tr><tr><td align="left"><a href="https://paste.armbian.com/afodacohev">ZeroPi</a></td><td align="left">2023-08-22&nbsp;10:49:48</td><td align=right>5.15.127-legacy-sunxi</td><td align=right>551</td><td align=right>2648</td></tr><tr><td align="left"><a href="https://paste.armbian.com/bisuwiyita">ZeroPi</a></td><td align="left">2023-08-22&nbsp;10:58:05</td><td align=right>5.15.127-legacy-sunxi</td><td align=right>550</td><td align=right>2688</td></tr><tr><td align="left"><a href="https://paste.armbian.com/uwetezetej">ZeroPi</a></td><td align="left">2023-08-22&nbsp;11:07:37</td><td align=right>6.4.11-edge-sunxi</td><td align=right>563</td><td align=right>2648</td></tr><tr><td align="left"><a href="https://paste.armbian.com/mosetusixe">ZeroPi</a></td><td align="left">2023-08-22&nbsp;11:16:02</td><td align=right>6.4.11-edge-sunxi</td><td align=right>531</td><td align=right>2656</td></tr><tr><td align="left"><a href="n/a">Cubietruck</a></td><td align="left">2023-08-22&nbsp;10:23:44</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Cubietruck</a></td><td align="left">2023-08-22&nbsp;10:23:45</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Cubietruck</a></td><td align="left">2023-08-22&nbsp;10:23:46</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Cubietruck</a></td><td align="left">2023-08-22&nbsp;10:23:47</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="https://paste.armbian.com/xutatiyuci">NanoPi R4S</a></td><td align="left">2023-08-22&nbsp;10:31:41</td><td align=right>6.1.46-current-rockchip64</td><td align=right>890</td><td align=right>6435</td></tr><tr><td align="left"><a href="https://paste.armbian.com/azuwobigel">NanoPi R4S</a></td><td align="left">2023-08-22&nbsp;10:40:08</td><td align=right>5.15.93-rockchip64</td><td align=right>860</td><td align=right>6356</td></tr><tr><td align="left"><a href="https://paste.armbian.com/dojoyudumi">NanoPi R4S</a></td><td align="left">2023-08-22&nbsp;10:47:59</td><td align=right>6.4.11-edge-rockchip64</td><td align=right>970</td><td align=right>6488</td></tr><tr><td align="left"><a href="https://paste.armbian.com/oxofidisos">NanoPi R4S</a></td><td align="left">2023-08-22&nbsp;10:56:09</td><td align=right>6.1.11-rockchip64</td><td align=right>860</td><td align=right>6450</td></tr><tr><td align="left"><a href="https://paste.armbian.com/unifocoxiw">Odroid N2</a></td><td align="left">2023-08-22&nbsp;10:28:32</td><td align=right>6.1.46-current-meson64</td><td align=right>890</td><td align=right>8716</td></tr><tr><td align="left"><a href="https://paste.armbian.com/imapafisim">Odroid N2</a></td><td align="left">2023-08-22&nbsp;10:34:08</td><td align=right>6.1.11-meson64</td><td align=right>890</td><td align=right>8430</td></tr><tr><td align="left"><a href="https://paste.armbian.com/upizececag">Odroid N2</a></td><td align="left">2023-08-22&nbsp;10:39:24</td><td align=right>6.4.11-edge-meson64</td><td align=right>890</td><td align=right>8980</td></tr><tr><td align="left"><a href="https://paste.armbian.com/enedomoxac">Odroid N2</a></td><td align="left">2023-08-22&nbsp;10:44:56</td><td align=right>6.2.0-rc3-meson64</td><td align=right>890</td><td align=right>8953</td></tr><tr><td align="left"><a href="https://paste.armbian.com/deceyavovu">Orange Pi 3</a></td><td align="left">2023-08-22&nbsp;10:30:40</td><td align=right>6.1.46-current-sunxi64</td><td align=right>860</td><td align=right>4385</td></tr><tr><td align="left"><a href="https://paste.armbian.com/quleqeredi">Orange Pi 3</a></td><td align="left">2023-08-22&nbsp;10:38:32</td><td align=right>5.15.93-sunxi64</td><td align=right>867</td><td align=right>4228</td></tr><tr><td align="left"><a href="https://paste.armbian.com/itiratataz">Orange Pi 3</a></td><td align="left">2023-08-22&nbsp;10:45:55</td><td align=right>6.4.11-edge-sunxi64</td><td align=right>854</td><td align=right>4202</td></tr><tr><td align="left"><a href="https://paste.armbian.com/zumupaduhu">Orange Pi 3</a></td><td align="left">2023-08-22&nbsp;10:53:52</td><td align=right>6.1.11-sunxi64</td><td align=right>864</td><td align=right>4169</td></tr><tr><td align="left"><a href="https://paste.armbian.com/rejapajuje">NanoPi Neo 3</a></td><td align="left">2023-08-22&nbsp;10:32:04</td><td align=right>6.1.46-current-rockchip64</td><td align=right>922</td><td align=right>3406</td></tr><tr><td align="left"><a href="https://paste.armbian.com/alusosexaz">NanoPi Neo 3</a></td><td align="left">2023-08-22&nbsp;10:42:03</td><td align=right>5.15.93-rockchip64</td><td align=right>960</td><td align=right>2432</td></tr><tr><td align="left"><a href="https://paste.armbian.com/ruvuwanida">NanoPi Neo 3</a></td><td align="left">2023-08-22&nbsp;10:52:45</td><td align=right>6.4.11-edge-rockchip64</td><td align=right>765</td><td align=right>1872</td></tr><tr><td align="left"><a href="https://paste.armbian.com/ugitunitob">NanoPi Neo 3</a></td><td align="left">2023-08-22&nbsp;11:05:25</td><td align=right>6.1.11-rockchip64</td><td align=right>562</td><td align=right>1582</td></tr><tr><td align="left"><a href="n/a">Orange Pi Zero</a></td><td align="left">2023-08-22&nbsp;10:23:33</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi Zero</a></td><td align="left">2023-08-22&nbsp;10:23:34</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi Zero</a></td><td align="left">2023-08-22&nbsp;10:23:34</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi Zero</a></td><td align="left">2023-08-22&nbsp;10:23:36</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi Zero</a></td><td align="left">2023-08-22&nbsp;10:23:36</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi Zero</a></td><td align="left">2023-08-22&nbsp;10:23:37</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="https://paste.armbian.com/begutiqale">Orange Pi Zero Plus</a></td><td align="left">2023-08-22&nbsp;10:37:13</td><td align=right>6.1.46-current-sunxi64</td><td align=right>842</td><td align=right>2510</td></tr><tr><td align="left"><a href="https://paste.armbian.com/luvawuwizo">Orange Pi Zero Plus</a></td><td align="left">2023-08-22&nbsp;10:51:31</td><td align=right>5.15.93-sunxi64</td><td align=right>782</td><td align=right>2424</td></tr><tr><td align="left"><a href="https://paste.armbian.com/xemataxuto">Orange Pi Zero Plus</a></td><td align="left">2023-08-22&nbsp;11:06:32</td><td align=right>6.4.11-edge-sunxi64</td><td align=right>799</td><td align=right>2397</td></tr><tr><td align="left"><a href="https://paste.armbian.com/omosusituy">Orange Pi Zero Plus</a></td><td align="left">2023-08-22&nbsp;11:21:05</td><td align=right>6.1.11-sunxi64</td><td align=right>843</td><td align=right>2467</td></tr><tr><td align="left"><a href="https://paste.armbian.com/jutakivivu">Orange Pi Zero2</a></td><td align="left">2023-08-22&nbsp;10:36:49</td><td align=right>6.1.46-current-sunxi64</td><td align=right>747</td><td align=right>2657</td></tr><tr><td align="left"><a href="https://paste.armbian.com/vupofanode">Orange Pi Zero2</a></td><td align="left">2023-08-22&nbsp;10:58:08</td><td align=right>5.15.93-sunxi64</td><td align=right>0</td><td align=right>1183</td></tr><tr><td align="left"><a href="https://paste.armbian.com/">Clearfog Pro</a></td><td align="left">2023-08-22&nbsp;10:31:56</td><td align=right>6.1.46-current-mvebu</td><td align=right>890</td><td align=right>2181</td></tr><tr><td align="left"><a href="https://paste.armbian.com/">Clearfog Pro</a></td><td align="left">2023-08-22&nbsp;10:40:34</td><td align=right>5.15.93-mvebu</td><td align=right>882</td><td align=right>2176</td></tr><tr><td align="left"><a href="https://paste.armbian.com/">Clearfog Pro</a></td><td align="left">2023-08-22&nbsp;10:48:34</td><td align=right>6.2.16-edge-mvebu</td><td align=right>680</td><td align=right>2169</td></tr><tr><td align="left"><a href="https://paste.armbian.com/">Clearfog Pro</a></td><td align="left">2023-08-22&nbsp;10:57:11</td><td align=right>6.1.11-mvebu</td><td align=right>881</td><td align=right>2171</td></tr><tr><td align="left"><a href="https://paste.armbian.com/ahidusayak">ODROID M1</a></td><td align="left">2023-08-22&nbsp;10:33:48</td><td align=right>6.3.13-edge-rk3568-odroid</td><td align=right>770</td><td align=right>5301</td></tr><tr><td align="left"><a href="https://paste.armbian.com/pebocequca">ODROID M1</a></td><td align="left">2023-08-22&nbsp;10:44:15</td><td align=right>6.1.12-rk3568-odroid</td><td align=right>890</td><td align=right>4994</td></tr><tr><td align="left"><a href="https://paste.armbian.com/powabalisu">Tinker Board 2</a></td><td align="left">2023-08-22&nbsp;10:32:11</td><td align=right>6.1.46-current-rockchip64</td><td align=right>906</td><td align=right>6889</td></tr><tr><td align="left"><a href="https://paste.armbian.com/pivonufiga">Tinker Board 2</a></td><td align="left">2023-08-22&nbsp;10:40:11</td><td align=right>5.15.93-rockchip64</td><td align=right>890</td><td align=right>6783</td></tr><tr><td align="left"><a href="https://paste.armbian.com/onikunigol">Tinker Board 2</a></td><td align="left">2023-08-22&nbsp;10:47:52</td><td align=right>6.4.11-edge-rockchip64</td><td align=right>970</td><td align=right>6668</td></tr><tr><td align="left"><a href="https://paste.armbian.com/owanufisor">Tinker Board 2</a></td><td align="left">2023-08-22&nbsp;10:55:55</td><td align=right>6.1.11-rockchip64</td><td align=right>880</td><td align=right>6625</td></tr><tr><td align="left"><a href="https://paste.armbian.com/uwemogebub">Orange Pi 4 LTS</a></td><td align="left">2023-08-22&nbsp;10:30:28</td><td align=right>6.1.46-current-rockchip64</td><td align=right>820</td><td align=right>5408</td></tr><tr><td align="left"><a href="https://paste.armbian.com/hupufapola">Orange Pi 4 LTS</a></td><td align="left">2023-08-22&nbsp;10:40:11</td><td align=right>5.15.93-rockchip64</td><td align=right>906</td><td align=right>4019</td></tr><tr><td align="left"><a href="https://paste.armbian.com/ugejaqoxip">Orange Pi 4 LTS</a></td><td align="left">2023-08-22&nbsp;10:48:28</td><td align=right>6.4.11-edge-rockchip64</td><td align=right>800</td><td align=right>4520</td></tr><tr><td align="left"><a href="https://paste.armbian.com/ohitewoyuh">Orange Pi 4 LTS</a></td><td align="left">2023-08-22&nbsp;10:58:35</td><td align=right>6.1.11-rockchip64</td><td align=right>890</td><td align=right>3896</td></tr><tr><td align="left"><a href="https://paste.armbian.com/litoruguqe">Le potato</a></td><td align="left">2023-08-22&nbsp;10:37:30</td><td align=right>6.1.46-current-meson64</td><td align=right>89</td><td align=right>3736</td></tr><tr><td align="left"><a href="https://paste.armbian.com/uqusiyogez">Le potato</a></td><td align="left">2023-08-22&nbsp;10:51:15</td><td align=right>6.1.11-meson64</td><td align=right>93</td><td align=right>3746</td></tr><tr><td align="left"><a href="https://paste.armbian.com/osezolixir">Le potato</a></td><td align="left">2023-08-22&nbsp;11:04:13</td><td align=right>6.4.11-edge-meson64</td><td align=right>89</td><td align=right>3721</td></tr><tr><td align="left"><a href="https://paste.armbian.com/fuminiluha">Le potato</a></td><td align="left">2023-08-22&nbsp;11:18:16</td><td align=right>6.2.0-rc3-meson64</td><td align=right>90</td><td align=right>3736</td></tr><tr><td align="left"><a href="n/a">BigTreeTech CB1</a></td><td align="left">2023-08-22&nbsp;10:23:26</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">BigTreeTech CB1</a></td><td align="left">2023-08-22&nbsp;10:23:28</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Banana Pi CM4IO</a></td><td align="left">2023-08-22&nbsp;10:23:34</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Banana Pi CM4IO</a></td><td align="left">2023-08-22&nbsp;10:23:34</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Banana Pi CM4IO</a></td><td align="left">2023-08-22&nbsp;10:23:35</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Banana Pi CM4IO</a></td><td align="left">2023-08-22&nbsp;10:23:36</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="https://paste.armbian.com/acahameyef">Banana Pi M5</a></td><td align="left">2023-08-22&nbsp;10:29:18</td><td align=right>6.1.46-current-meson64</td><td align=right>740</td><td align=right>5586</td></tr><tr><td align="left"><a href="https://paste.armbian.com/ujubakohoc">Banana Pi M5</a></td><td align="left">2023-08-22&nbsp;10:35:40</td><td align=right>6.1.11-meson64</td><td align=right>890</td><td align=right>5559</td></tr><tr><td align="left"><a href="https://paste.armbian.com/uqufegerem">Banana Pi M5</a></td><td align="left">2023-08-22&nbsp;10:41:34</td><td align=right>6.4.11-edge-meson64</td><td align=right>890</td><td align=right>5551</td></tr><tr><td align="left"><a href="https://paste.armbian.com/eyiwohanoh">Banana Pi M5</a></td><td align="left">2023-08-22&nbsp;10:47:51</td><td align=right>6.2.0-rc3-meson64</td><td align=right>890</td><td align=right>5558</td></tr><tr><td align="left"><a href="n/a">Tinker Board</a></td><td align="left">2023-08-22&nbsp;10:24:07</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Tinker Board</a></td><td align="left">2023-08-22&nbsp;10:24:07</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Tinker Board</a></td><td align="left">2023-08-22&nbsp;10:24:08</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Tinker Board</a></td><td align="left">2023-08-22&nbsp;10:24:09</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="https://paste.armbian.com/edidoreroj">Khadas VIM2</a></td><td align="left">2023-08-22&nbsp;10:34:10</td><td align=right>6.1.46-current-meson64</td><td align=right>890</td><td align=right>6119</td></tr><tr><td align="left"><a href="https://paste.armbian.com/uquhociguv">Khadas VIM2</a></td><td align="left">2023-08-22&nbsp;10:45:33</td><td align=right>6.1.11-meson64</td><td align=right>810</td><td align=right>6094</td></tr><tr><td align="left"><a href="https://paste.armbian.com/ovupomutib">Khadas VIM2</a></td><td align="left">2023-08-22&nbsp;10:56:44</td><td align=right>6.4.11-edge-meson64</td><td align=right>940</td><td align=right>6216</td></tr><tr><td align="left"><a href="https://paste.armbian.com/luxemezito">Khadas VIM2</a></td><td align="left">2023-08-22&nbsp;11:08:12</td><td align=right>6.2.0-rc3-meson64</td><td align=right>861</td><td align=right>6122</td></tr><tr><td align="left"><a href="https://paste.armbian.com/anonosofok">Khadas VIM1</a></td><td align="left">2023-08-22&nbsp;10:32:50</td><td align=right>6.1.46-current-meson64</td><td align=right>93</td><td align=right>3671</td></tr><tr><td align="left"><a href="https://paste.armbian.com/cenunetisi">Khadas VIM1</a></td><td align="left">2023-08-22&nbsp;10:42:50</td><td align=right>6.1.11-meson64</td><td align=right>93</td><td align=right>3684</td></tr><tr><td align="left"><a href="https://paste.armbian.com/kijekivora">Khadas VIM1</a></td><td align="left">2023-08-22&nbsp;10:52:32</td><td align=right>6.4.11-edge-meson64</td><td align=right>89</td><td align=right>3716</td></tr><tr><td align="left"><a href="https://paste.armbian.com/asowazubon">Khadas VIM1</a></td><td align="left">2023-08-22&nbsp;11:02:31</td><td align=right>6.2.0-rc3-meson64</td><td align=right>90</td><td align=right>3674</td></tr><tr><td align="left"><a href="n/a">Orange Pi R1 Plus LTS</a></td><td align="left">2023-08-22&nbsp;10:23:21</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi R1 Plus LTS</a></td><td align="left">2023-08-22&nbsp;10:23:22</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi R1 Plus LTS</a></td><td align="left">2023-08-22&nbsp;10:23:23</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi R1 Plus LTS</a></td><td align="left">2023-08-22&nbsp;10:23:24</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Rock 5B</a></td><td align="left">2023-08-22&nbsp;10:24:08</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Rock 5B</a></td><td align="left">2023-08-22&nbsp;10:24:09</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi Zero Plus 2</a></td><td align="left">2023-08-22&nbsp;10:23:33</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi Zero Plus 2</a></td><td align="left">2023-08-22&nbsp;10:23:33</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi Zero Plus 2</a></td><td align="left">2023-08-22&nbsp;10:23:34</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi Zero Plus 2</a></td><td align="left">2023-08-22&nbsp;10:23:35</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr></table>
<!--END_SECTION:data-section-->

## Would you like to join spare hardware to this automated testings?

All you need to do is:

- deploy any latest Armbian image to hardware
- provide IP address
- [contact us](https://www.armbian.com/contact/)

Device has to be always on and easily accesible for you to re-image in case of failed upgrade.

## Development

- [Pull request](https://github.com/armbian/build/pulls)
- [Weekly developers meetings](https://forum.armbian.com/events/)
- [Forums for developers](https://forum.armbian.com/forum/4-advanced-users-development/)

## OS download

- [Download](https://www.armbian.com/download/)

## Support

- [Using Armbian](https://forum.armbian.com/forum/23-using-armbian/)

## Contact

- [Forums](https://forum.armbian.com) for Participate in Armbian
- IRC: `#armbian` on Libera.chat
- Discord: [https://discord.gg/armbian](https://discord.gg/armbian)
- Follow [@armbian](https://twitter.com/armbian) on Twitter, [Fosstodon](https://fosstodon.org/@armbian) or [LinkedIn](https://www.linkedin.com/company/armbian).
- Bugs: [issues](https://github.com/armbian/build/issues) / [JIRA](https://armbian.atlassian.net/jira/dashboards/10000)
- Office hours: [Wednesday, 12 midday, 18 afternoon, CET](https://calendly.com/armbian/office-hours)

## License

This software is published under the GPL-2.0 License license.
