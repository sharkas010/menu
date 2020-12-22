@import url(https://mwittrien.github.io/BetterDiscordAddons/Themes/_res/ThemeDevBadge.css);
@import url(https://mwittrien.github.io/BetterDiscordAddons/Themes/BlurpleRecolor/BlurpleRecolor.css);
@import url(https://discord-custom-covers.github.io/usrbg/dist/usrbg.css);

:root {
	--dtransparencycolor:			0,0,0;
	--dtransparencyalpha:			0.15;
	--dmessagetransparency:			0.5;
	--dguildchanneltransparency:	0.15;
	--dmemberlisttransparency:		0.0;
	--daccentcolor:					190,78,180;
	
	--dfont:						Whitney, Helvetica Neue, Helvetica, Arial, sans-serif;
	--dtextshadow:					transparent;
	
	--dbackground:					url(https://mwittrien.github.io/BetterDiscordAddons/Themes/BasicBackground/background.jpg);
	--dbackgroundsize:				cover;
	--dbackgroundposition:			center;
	--dblur:						unset;
	--dbackdrop:					rgba(0,0,0,0.85);

	--vtransparencycolor:			var(--transparencycolor,			var(--dtransparencycolor));
	--vtransparencyalpha:			var(--transparencyalpha,			var(--dtransparencyalpha));
	--vmessagetransparency:			var(--messagetransparency,			var(--dmessagetransparency));
	--vusechatbubbles: 				calc(var(--vmessagetransparency) / (var(--vmessagetransparency) + 0.00000000000000000000001));
	--vguildchanneltransparency:	var(--guildchanneltransparency,		var(--dguildchanneltransparency));
	--vmemberlisttransparency:		var(--memberlisttransparency,		var(--dmemberlisttransparency));
	--vaccentcolor:					var(--accentcolor,					var(--daccentcolor));
	--vlinkcolor:					var(--vaccentcolor);
	
	--vfont:						var(--font,							var(--dfont));
	--vtextshadow:					var(--textshadow,					var(--dtextshadow));
	
	--vbackground:					var(--background,					var(--dbackground));
	--vbackgroundposition:			var(--backgroundposition,			var(--dbackgroundposition));
	--vbackgroundsize:				var(--backgroundsize,				var(--dbackgroundsize));
	--vbackgroundblur:				var(--backgroundblur,				var(--dblur));
	
	--vpopout:						var(--popout,						var(--vbackground));
	--vpopoutposition:				var(--backgroundposition,			var(--vbackgroundposition));
	--vpopoutsize:					var(--popoutsize,					var(--vbackgroundsize));
	--vpopoutblur:					var(--popoutblur,					var(--vbackgroundblur));
	
	--vbackdrop:					var(--backdrop,						var(--dbackdrop));
	--vbackdropposition:			var(--backgroundposition,			var(--vbackgroundposition));
	--vbackdropsize:				var(--backdropsize,					var(--vbackgroundsize));
	--vbackdropblur:				var(--backdropblur,					var(--vbackgroundblur));

	--fontwhite1: 					255,255,255;
	--fontwhite2: 					210,210,210;
	--fontwhite3: 					170,170,170;
	--fontwhite4: 					120,120,120;
}

.theme-light, .theme-dark {
	--header-primary: rgb(var(--fontwhite1));
	--header-secondary: rgb(var(--fontwhite2));
	--text-normal: rgb(var(--fontwhite2));
	--text-muted: rgb(var(--fontwhite4));
	--text-link: rgb(var(--vaccentcolor));
	--channels-default: rgb(var(--fontwhite4));
	--interactive-normal: rgb(var(--fontwhite3));
	--interactive-hover: rgb(var(--fontwhite2));
	--interactive-active: rgb(var(--fontwhite1));
	--interactive-muted: rgb(var(--fontwhite4));
	--elevation-low: 0 1px 5px 0 rgba(var(--vtransparencycolor), 0.3);
	--elevation-high: 0 2px 10px 0 rgba(var(--vtransparencycolor), 0.3);
	--logo-primary: rgb(var(--fontwhite1));
}


/* ~~~~		0.		TABLE OF CONTENTS				~~~~ */
/*
	1.	TRANSPARENCY
	2.	BACKGROUND
	3.	TITLEBAR
	4.	GUILDLIST
	5.	CHANNELLIST
		1.	GUILDHEADER
		2.	CHANNELS
		3.	DMCHANNELS
		4.	ACCOUNT/VOICE/GOLIVE
	6.	CHAT
		1.	CHANNELHEADER
		2.	MESSAGES
			1.	MESSAGE
			2.	EMBEDS
			3.	NITROGIFT
			4.	INVITE
		3.	TEXTAREA
		4.	AUTOCOMPLETEMENU
		5.	MEMBERLIST
		6.	SEARCHPAGE
		7.	CALL
		8.	UNAVAILABLESCREEN
	7.	PEOPLES
	8.	STORE/NITRO
	9.	LIBRARY
	10.	DISCOVERY
	11.	USERSETTINGS
	12.	GUILDSETTINGS
	13.	MODALS
		1.	USERMODAL
		2.	GUILDADD/CREATION
		3.	REGIONSELECTMODAL
		4.	UPLOADMODAL
		5.	KEYBOARDSHORTCUTSMODAL
		6.	QUICKSWITCHER
		7.	INVITEMODAL/GROUPCREATE
		8.	LOGINSCREEN
		9.	TERMACCEPTMODAL
		10.	DOWNLOADAPPMODAL
		11.	GUILDBOOSTMODAL
		12.	REACTIONSMODAL
		13.	GUILDTEMPLATEMODAL
		14.	GUILDWELCOMEMODAL
		15.	SCREENSHAREMODAL
	14.	POPOUTS
		1.	CONTEXTMENU
		2.	USERPOPOUT
		3.	EMOJIPICKER
		4.	PINS/MENTIONS
		5.	SEARCHPOPOUT
		6.	COLORPICKER
		7.	ADDROLE
		8.	EVERYONEMENTION
		9.	CHANNELFOLLOW
		10.	CHANNELFOLLOWINFO
		11.	EMOJIINFO
		12.	STREAMPREVIEW
	15.	GENERAL
		1.	TEXT
		2.	BUTTONS
		3.	INPUTS
		4.	SEARCHBARS
		5.	TAGS
		6.	ICONS
		7.	SCROLLBARS
		8.	NOTIFICATIONBAR
		9.	TOOLTIPS
		10.	TOASTS
	16.	BDSUPPORT
	17.	PLUGINSUPPORT
		1.	DATEVIEWER
		2.	SERVERFOLDERS
		3.	MEMBERCOUNT
		4.	SENDBUTTON
		5.	CHARCOUNTER
		6.	REPLYER
		7.	CITADOR
		8.	LINENUMBERS
		9.	PERMISSIONVIEWER
		10.	DIRECTDOWNLOAD
		11.	BETTERFORMATINGREDUX
		12.	PLUGIN/THEMEREPO
		13.	CHANNELHISTORY
		14.	DISPLAYLARGEMESSAGES
		15.	CHANNELTABS
	18.	UPDATENOTICE
	19.	WATERMARK
*/


/* ~~~~		1.		TRANSPARENCY					~~~~ */

body,														/* body														*/
#app-mount .app-1q1i1E,										/* app					container							*/
#app-mount .app-2rEoOp,										/* app					inner								*/
#app-mount .container-16j22k,								/* app					loadingscreen						*/
#app-mount .wrapper-1prNyd,									/* app					errorscreen							*/
#app-mount .bg-h5JY_x,										/* app					background							*/
#app-mount .layer-3QrUeG,									/* layer				container							*/
#app-mount .container-3w7J-x,								/* channels				inner								*/
#app-mount .privateChannels-1nO12o,							/* dmchannels												*/
#app-mount .panels-j1Uci_ > *,								/* account/voice		inner								*/
#app-mount .chat-3bRxxu,									/* chat					container							*/
#app-mount .wrapper-3vR61M,									/* chat					messages loading					*/
#app-mount .noChannel-Z1DQK7,								/* nochannel												*/
#app-mount .members-1998pB,									/* members													*/
#app-mount .members-1998pB > div,							/* members				content								*/
#app-mount .content-MLh4nU,									/* unavailable												*/
#app-mount .container-1D34oG,								/* peoples													*/
#app-mount .applicationStore-1pNvnv,						/* nitro													*/
#app-mount .pageWrapper-1PgVDX,								/* guilddiscovery											*/
#app-mount .scrollerBase-289Jih,							/* scroller													*/
#app-mount .scroller-2FKFPG,								/* scroller old												*/
#app-mount .standardSidebarView-3F1I7i,						/* settings													*/
#app-mount .contentRegion-3nDuYy {							/* settings				content								*/
	background: transparent;
}

#app-mount .sidebarRegion-VFTUkN {							/* settings				sidebar								*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
#app-mount .sidebar-_0OpfR {								/* sidebarlist			sidebar								*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}

#app-mount {												/* app-mount												*/
	background-color: rgba(var(--vtransparencycolor), var(--vtransparencyalpha));
}
#app-mount .wrapper-1Rf91z {								/* guilds				container							*/
	background-color: rgba(var(--vtransparencycolor), calc(var(--vguildchanneltransparency) * 2));
}
#app-mount .sidebar-2K8pFh {								/* channels				container							*/
	background-color: rgba(var(--vtransparencycolor), var(--vguildchanneltransparency));
}
#app-mount .panels-j1Uci_ {									/* account/voice		container							*/
	background-color: rgba(var(--vtransparencycolor), calc(var(--vguildchanneltransparency) / 1.5));
}
#app-mount .container-1r6BKw.themed-ANHk51 {				/* channelheader		container							*/
	background-color: rgba(var(--vtransparencycolor), var(--vguildchanneltransparency));
}
#app-mount .membersWrap-2h-GB4 {							/* members				container							*/
	background-color: rgba(var(--vtransparencycolor), var(--vmemberlisttransparency));
}
#app-mount .tabBar-fg4VK9 {									/* members				tabbar								*/
	background-color: rgba(var(--vtransparencycolor), var(--vmemberlisttransparency));
}
#app-mount .nowPlayingColumn-2sl4cE {						/* peoples				now playing							*/
	background-color: rgba(var(--vtransparencycolor), var(--vmemberlisttransparency));
}

#app-mount .image-3zK3Wt {									/* app					errorscreen image					*/
	background-image: url(https://discordapp.com/assets/e9baf4b505eb54129f832556ea16538e.svg);
	opacity: 0.6;
}


/* ~~~~		2.		BACKGROUND						~~~~ */

body::before {
	content: "";
	top: 0;
	left: 0;
	right: 0;
	bottom: 0;
	position: fixed;
	background: var(--vbackground) var(--vbackgroundposition)/var(--vbackgroundsize);
	filter: blur(var(--vbackgroundblur));
}
#ace_settingsmenu_container,
.uploadArea-3QgLtW,
.backdropWithLayer-3_uhz4,
.backdrop-1wrmKB {
	background: var(--vbackdrop) var(--vbackdropposition)/var(--vbackdropsize) !important;
	filter: blur(var(--vbackdropblur));
	opacity: 1;
	animation: none;
}
.backdropWithLayer-3_uhz4 {
	z-index: -1;
}


/* ~~~~		3.		TITLEBAR						~~~~ */

.titleBar-AC4pGV {
	z-index: 5001;
}
.titleBar-AC4pGV::after {
	content: "";
	pointer-events: none;
	position: absolute;
	z-index: -1;
	top: 0;
	left: 0;
	width: 100%;
	background-color: rgba(var(--vtransparencycolor), calc(0.1 + var(--vguildchanneltransparency) * 2));
}
.titleBar-AC4pGV:not(.typeMacOS-3EmCyP)::after {
	height: 22px;
}
.titleBar-AC4pGV.typeMacOS-3EmCyP::after {
	height: 28px;
	width: calc(100% - 4px);
	margin: 2px;
	border-radius: 5px;
}
.titleBar-AC4pGV.typeMacOS-3EmCyP,
.titleBar-AC4pGV.typeMacOS-3EmCyP .macButtons-2MuSAC {
	width: 72px;
}
.titleBar-AC4pGV.typeMacOS-3EmCyP.typeMacOSWithFrame-3R_i5S .macButtons-2MuSAC {
	margin-top: 0;
	margin-right: 0;
}
.platform-osx .wrapper-1Rf91z {
	margin-top: 0;
	padding-top: 32px;
}
.platform-osx .standardSidebarView-3F1I7i::before {
	left: 72px;
}
.winButton-iRh8-Z {
	color: rgb(var(--fontwhite3));
}
.winButtonMinMax-PBQ2gm:hover {
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
.winButtonClose-1HsbF-:hover,
.winButtonMinMax-PBQ2gm:hover {
	color: rgb(var(--fontwhite1));
}


/* ~~~~		4.		GUILDLIST						~~~~ */

.childWrapper-anI2G9,										/* homebutton/acronym	innerwrap							*/
#bd-pub-button {											/* publicbutton			innerwrap							*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
	color: rgb(var(--fontwhite2));
	font-weight: 500;
}
.wrapper-1BJsBx:hover svg,
.wrapper-1BJsBx.selected-bZ3Lue svg {
	filter: drop-shadow(1px 1px var(--vtextshadow));
}
.wrapper-1BJsBx:hover .childWrapper-anI2G9,
.wrapper-1BJsBx.selected-bZ3Lue .childWrapper-anI2G9,
#bd-pub-button:hover {
	color: rgb(var(--fontwhite1));
	text-shadow: 1px 1px var(--vtextshadow);
}
.noIcon-1a_FrS {											/* acronym				minicontainer						*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
	color: rgb(var(--fontwhite2));
}

.circleIconButton-jET_ig {									/* guildadd/discovery	innerwrap							*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
.circleIconButton-jET_ig.selected-ugP_am {
	color: rgb(var(--fontwhite1));
}

.guildIconUnavailable-5PMHDN,								/* guilderror			miniicon							*/
.guildsError-b7zR5H {										/* guilderror			innerwrap							*/
	background-color: rgba(240, 71, 71, 0.3);
}

.dragInner-_SHftW {											/* dragplaceholder											*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}

.guildSeparator-3s64Iy {									/* guildseparator											*/
	background-color: rgba(var(--fontwhite1), 0.2);
}

.item-2hkk8m {												/* unread/selectedpill										*/
	background-color: rgb(var(--fontwhite1));
}

.wrapper-21YSNc {											/* folder				outerwrap							*/
	margin-bottom: 8px;
}
.folder-21wGz3 {											/* folder				iconwrap							*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
.folder-21wGz3.hover-2ji_A7 {
	background-color: rgba(var(--vtransparencycolor), 0.4);
}
.expandedFolderBackground-2sPsd- {							/* folder				background							*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
	border-radius: 15px 15px 24px 24px;
	top: 0;
	bottom: 0;
	margin-bottom: 8px;
	transition: border-radius 3s ease, background-color 1s ease;
}
.expandedFolderBackground-2sPsd-.hover-2ji_A7 {
	background-color: rgba(var(--vtransparencycolor), 0.4);
}

.wrapper-1Rf91z .wrapper-21YSNc [role="group"] {			/* folder				guildwrap							*/
	margin-bottom: -8px;
}
.wrapper-1Rf91z .wrapper-21YSNc [role="group"] .listItem-2P_4kh:last-child {
	margin-bottom: 0;
}

.bar-30k2ka {												/* guild/channelbar		inner								*/
	box-shadow: 0 2px 6px rgba(var(--vtransparencycolor), 0.24);
	color: rgb(var(--fontwhite1));
}
.bar-30k2ka:not(.mention-1f5kbO) {
	background-color: transparent;
	overflow: hidden;
}
.bar-30k2ka:not(.mention-1f5kbO)::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--vbackground) var(--vbackgroundposition)/var(--vbackgroundsize);
	background-attachment: fixed;
	filter: blur(var(--vbackgroundblur));
	pointer-events: none;
	z-index: -1;
}
.bar-30k2ka:not(.mention-1f5kbO)::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.1));
	pointer-events: none;
	z-index: -1;
}
.sidebar-2K8pFh .bar-30k2ka:not(.mention-1f5kbO)::after {
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + var(--vguildchanneltransparency) * 0.85 + 0.1));
}
.wrapper-1Rf91z .bar-30k2ka:not(.mention-1f5kbO)::after {
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + var(--vguildchanneltransparency) * 1.9 + 0.1));
}


/* ~~~~		5.		CHANNELLIST						~~~~ */

#app-mount .sidebar-2K8pFh {								/* channels				container							*/
	border-radius: 0;
}

/* ----		5.1.	GUILDHEADER						---- */

.container-1taM1r .animatedContainer-1NSq4T {				/* banner				wrap								*/
	background: none;
	box-shadow: none;
}
.bannerImage-1jOskm {										/* banner				image								*/
	-webkit-mask: linear-gradient(rgba(0,0,0,0.9) 70%, rgba(0,0,0,0) 100%);
}
.bannerImage-1jOskm::before {
	display: none;
}

.header-2V-4Sw,												/* header				inner								*/
.searchBar-6Kv8R2 {											/* header				searchbar							*/
	box-shadow: 0 1px 0 rgba(var(--vtransparencycolor), 0.2), 0 1.5px 0 rgba(var(--vtransparencycolor), 0.05), 0 2px 0 rgba(var(--vtransparencycolor), 0.05);
}
.searchBar-6Kv8R2 .searchBarComponent-32dTOx {				/* header				searchbarinner						*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
	color: rgb(var(--fontwhite3));
}
.header-2V-4Sw,
.bannerVisible-2ZE_qG .header-2V-4Sw {
	color: rgb(var(--fontwhite1));
}
.clickable-25tGDB:not(.hasBanner-2SrLR3) .header-2V-4Sw:hover,
.selected-31Nl7x:not(.hasBanner-2SrLR3) .header-2V-4Sw {
	background-color: rgba(var(--vtransparencycolor), 0.2);
}

.channelNotice-1-XFjC {										/* notice				container							*/
	box-shadow: inset 0 -1px 0 rgba(var(--fontwhite4), 0.3);
}
.close-relY5R {												/* notice				close								*/
	color: rgb(var(--fontwhite3));
}
.close-relY5R:hover {
	color: rgb(var(--fontwhite1));
}
.message-3SOT5P {											/* notice				text								*/
	color: rgb(var(--fontwhite2));
}


/* ----		5.2.	CHANNELS						---- */

.wrapper-PY0fhH {											/* category				wrapper								*/
	color: rgb(var(--fontwhite3));
}
.wrapper-PY0fhH.muted-2JBAyG {
	color: rgb(var(--fontwhite4));
}
.wrapper-PY0fhH.muted-2JBAyG:hover,
.wrapper-PY0fhH:hover {
	color: rgb(var(--fontwhite1));
}
.wrapper-PY0fhH.muted-2JBAyG:hover .icon-2yIBmh,			/* category				icon								*/
.wrapper-PY0fhH:hover .icon-2yIBmh {
	color: rgb(var(--fontwhite1));
}
.wrapper-PY0fhH .name-3l27Hl {								/* category				name								*/
	color: rgb(var(--fontwhite3));
}
.wrapper-PY0fhH.muted-2JBAyG .name-3l27Hl {
	color: rgb(var(--fontwhite4));
}
.wrapper-PY0fhH.muted-2JBAyG:hover .name-3l27Hl,
.wrapper-PY0fhH:hover .name-3l27Hl {
	color: rgb(var(--fontwhite1));
}
.addButtonIcon-2CbG1X {										/* category				addbutton							*/
	opacity: 0.5;
}
.addButtonIcon-2CbG1X:hover {
	color: rgb(var(--fontwhite1));
	opacity: 1;
}

.wrapper-2jXpOf:hover .content-1x5b-n {						/* channel				content								*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
.modeSelected-346R90 .content-1x5b-n,
.modeSelected-346R90:hover .content-1x5b-n {
	background-color: rgb(var(--vaccentcolor));
	text-shadow: 1px 1px var(--vtextshadow);
}
.modeSelected-346R90 .content-1x5b-n svg,
.modeSelected-346R90:hover .content-1x5b-n svg {
	filter: drop-shadow(1px 1px var(--vtextshadow));
}
.icon-1DeIlz {												/* channel				icon								*/
	color: rgb(var(--fontwhite3));
}
.modeMuted-onO3r- .icon-1DeIlz {
	color: rgb(var(--fontwhite4));
}
.modeConnected-3IsKId .icon-1DeIlz,
.modeConnected-3IsKId:hover .icon-1DeIlz,
.modeSelected-346R90 .icon-1DeIlz,
.modeSelected-346R90:hover .icon-1DeIlz,
.modeUnread-1qO3K1 .icon-1DeIlz,
.modeUnread-1qO3K1:hover .icon-1DeIlz,
.notInteractive-1X92pj.modeConnected-3IsKId .icon-1DeIlz,
.notInteractive-1X92pj.modeSelected-346R90 .icon-1DeIlz,
.wrapper-2jXpOf:hover .icon-1DeIlz {
	color: rgb(var(--fontwhite1));
}
.name-23GUGE {												/* channel				name								*/
	color: rgb(var(--fontwhite3));
}
.modeMuted-onO3r- .name-23GUGE {
	color: rgb(var(--fontwhite4));
}
.modeConnected-3IsKId .name-23GUGE,
.modeConnected-3IsKId:hover .name-23GUGE,
.modeSelected-346R90 .name-23GUGE,
.modeSelected-346R90:hover .name-23GUGE,
.modeUnread-1qO3K1 .name-23GUGE,
.modeUnread-1qO3K1:hover .name-23GUGE,
.notInteractive-1X92pj.modeConnected-3IsKId .name-23GUGE,
.notInteractive-1X92pj.modeSelected-346R90 .name-23GUGE,
.wrapper-2jXpOf:hover .name-23GUGE {
	color: rgb(var(--fontwhite1));
}
.modeSelected-346R90 .actionIcon-PgcMM2,
.modeSelected-346R90:hover .actionIcon-PgcMM2,
.wrapper-2jXpOf:hover .actionIcon-PgcMM2 {
	color: rgb(var(--fontwhite1));
}
.actionIcon-PgcMM2 {
	opacity: 0.5;
}
.actionIcon-PgcMM2:hover {
	opacity: 1.0;
}
.unread-2lAfLh {
	background-color: rgb(var(--fontwhite1));
}

#app-mount .channelIcon-2xPHJh {							/* channelselect		icon								*/
	color: rgb(var(--fontwhite3));
}
#app-mount .selected-2rGcKN .channelIcon-2xPHJh {
	color: rgb(var(--fontwhite1));
}

.icon-2IuuZd,												/* voicechat			icon								*/
.username-3KYl0N {											/* voicechat			username							*/
	color: rgb(var(--fontwhite3));
}
.listDefault-3ir5aS .clickable-1lCRLF:hover .username-3KYl0N {
	color: rgb(var(--fontwhite2));
}
.listDefault-3ir5aS .clickable-1lCRLF.selected-3t3Csj .username-3KYl0N,
.listDefault-3ir5aS .clickable-1lCRLF:hover .usernameSpeaking-RmltQx,
.usernameSpeaking-RmltQx {
	color: rgb(var(--fontwhite1));
}
.wrapper-2tAnRe {											/* voicechat			limit								*/
	background-color: rgba(var(--vtransparencycolor), 0.15);
	color: rgb(var(--fontwhite3));
}
.modeConnected-3IsKId .wrapper-2tAnRe {
	color: rgb(var(--fontwhite1));
}
.wrapper-2tAnRe .users-3kndPl {
	background-color: transparent;
}
.wrapper-2tAnRe .total-i6us2n {
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
.wrapper-2tAnRe .total-i6us2n::after {
	border-right-color: rgba(var(--vtransparencycolor), 0.3);
}

.listDefault-3ir5aS .clickable-1lCRLF:hover .content-1Wq3SX {
	background-color: rgba(var(--vtransparencycolor), 0.2);
}


/* ----		5.3.	DMCHANNELS						---- */

.channel-2QD9_O {											/* dmchannel/page		container						*/
	color: rgb(var(--fontwhite3));
}
.clickable-1JJAn8.channel-2QD9_O:hover {
	color: rgb(var(--fontwhite2));
}
.clickable-1JJAn8.channel-2QD9_O:active,
.selected-aXhQR6.channel-2QD9_O {
	color: rgb(var(--fontwhite1));
}
.channel-2QD9_O:hover .layout-2DM8Md {						/* dmchannel/page		inner							*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
.selected-aXhQR6.channel-2QD9_O .layout-2DM8Md {
	background-color: rgb(var(--vaccentcolor));
	text-shadow: 1px 1px var(--vtextshadow);
}
.selected-aXhQR6.channel-2QD9_O .layout-2DM8Md svg:not(.svg-2V3M55) {
	filter: drop-shadow(1px 1px var(--vtextshadow));
}
.channel-2QD9_O .linkButtonIcon-Mlm5d6 {
	color: rgb(var(--fontwhite2));
}
.channel-2QD9_O .name-uJV0GL {
	color: rgb(var(--fontwhite2));
}
.channel-2QD9_O .subtext-1RtU34 {
	color: rgb(var(--fontwhite3));
}
.channel-2QD9_O:hover .linkButtonIcon-Mlm5d6,
.channel-2QD9_O.selected-aXhQR6 .linkButtonIcon-Mlm5d6 {
	color: rgb(var(--fontwhite1));
}
.channel-2QD9_O:hover .name-uJV0GL,
.channel-2QD9_O.selected-aXhQR6 .name-uJV0GL {
	color: rgb(var(--fontwhite1));
}
.channel-2QD9_O:hover .subtext-1RtU34,
.channel-2QD9_O.selected-aXhQR6 .subtext-1RtU34 {
	color: rgb(var(--fontwhite2));
}

.header-zu8eWb {
	color: rgb(var(--fontwhite2));
}

.empty-388osJ {												/* loadingplaceholders										*/
	fill: rgba(var(--vtransparencycolor), 0.4);
}

/* ----		5.4.	ACCOUNT/VOICE/GOLIVE			---- */

.panels-j1Uci_ > * {										/* account/voice		inner								*/
	border: none;
}
.panels-j1Uci_ > * + * {
	border-top: 1px solid rgba(var(--fontwhite4), 0.2);
}

.title-eS5yk3 {												/* account/voice		title								*/
	color: rgb(var(--fontwhite1));
}
.subtext-3CDbHg {											/* account/voice		subtext								*/
	color: rgb(var(--fontwhite3));
}
.button-14-BFJ {
	color: rgb(var(--fontwhite3));
}
.button-14-BFJ.enabled-2cQ-u7,								/* account/voice		buttons								*/
.button-14-BFJ.enabled-2cQ-u7:hover {
	color: rgb(var(--fontwhite1));
}
.button-14-BFJ.enabled-2cQ-u7 {
	opacity: 0.7;
}
.button-14-BFJ.enabled-2cQ-u7:hover {
	opacity: 1;
	background-color: rgb(var(--vaccentcolor));
}
.button-14-BFJ.enabled-2cQ-u7:hover svg {
	filter: drop-shadow(1px 1px var(--vtextshadow));
}
.button-1YfofB.buttonColor-7qQbGO {
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
.button-1YfofB.buttonColor-7qQbGO:hover {
	background-color: rgba(var(--vtransparencycolor), 0.4);
}
.button-1YfofB.buttonColor-7qQbGO.buttonActive-3FrkXp,
.button-1YfofB.buttonColor-7qQbGO.buttonActive-3FrkXp:hover {
	background-color: rgb(var(--vaccentcolor));
	text-shadow: 1px 1px var(--vtextshadow);
}
.button-1YfofB.buttonColor-7qQbGO.buttonActive-3FrkXp svg,
.button-1YfofB.buttonColor-7qQbGO.buttonActive-3FrkXp:hover svg {
	filter: drop-shadow(1px 1px var(--vtextshadow));
}


/* ~~~~		6.		CHAT							~~~~ */

/* ----		6.1.	CHANNELHEADER					---- */

.container-1r6BKw {											/* header				container							*/
	color: rgb(var(--fontwhite1));
}
.container-1r6BKw.themed-ANHk51 {							/* header				themedcontainer						*/
	box-shadow: 0 1px 0 rgba(var(--vtransparencycolor), 0.2),0 1.5px 0 rgba(var(--vtransparencycolor), 0.05),0 2px 0 rgba(var(--vtransparencycolor), 0.05);
}

.title-29uC1r {												/* header				title								*/
	color: rgb(var(--fontwhite1));
}
.input-2A_zIr {												/* header				dmchannelinput						*/
	color: rgb(var(--fontwhite1));
}
.input-2A_zIr:focus {										/* header				dmchannelinput						*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
.input-2A_zIr:focus,
.outer-o9SjPm:hover .input-2A_zIr {
	box-shadow: inset 0 0 0 1px rgba(var(--vtransparencycolor), 0.2);
}
.topic-TCb_qw {												/* header				topic								*/
	color: rgb(var(--fontwhite2));
}
.children-19S4PO::after {									/* header				topicgradient						*/
	display: none;
}

.akaBadge-1M-1Gw {											/* header				aka									*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}

.icon-22AiRD {												/* header				typeicon							*/
	color: rgb(var(--fontwhite1));
}
.clickable-3rdHwn .icon-22AiRD,								/* header				actionicon							*/
#app-mount .link-2T7oYD {									/* header				linkicon							*/
	color: rgb(var(--fontwhite3));
	opacity: 1;
}
.clickable-3rdHwn:hover .icon-22AiRD,
#app-mount .link-2T7oYD:hover {
	color: rgb(var(--fontwhite2));
}
.clickable-3rdHwn:active .icon-22AiRD,
.clickable-3rdHwn.selected-1GqIat .icon-22AiRD,
#app-mount .link-2T7oYD:active {
	color: rgb(var(--fontwhite1));
}

.badge-2qGa_k::after {										/* header				iconbadge red dot					*/
	border: none;
}

.divider-3FBTu8 {											/* header				divider								*/
	background-color: rgba(var(--fontwhite1), 0.1);
}

.searchBar-3dMhjb {											/* header				searchbar							*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
	color: rgb(var(--fontwhite1));
}
.search-2oPWTC .DraftEditor-root .public-DraftEditorPlaceholder-root {
	color: rgb(var(--fontwhite3));
}
#app-mount .searchFilter-2ESiM3,
#app-mount .searchAnswer-3Dz2-q {
	background-color: rgb(var(--vaccentcolor));
	color: rgb(var(--fontwhite1));
}

/* ----		6.2.	MESSAGES						---- */

.emptyChannelIcon-cc932w {									/* welcomemessage		empty channelicon					*/
	background-color: rgba(var(--vtransparencycolor), 0.4);
}
.card-1yV8cG {												/* welcomemessage		first steps card					*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
.card-1yV8cG:hover {
	background-color: rgba(var(--vtransparencycolor), 0.5);
}

.divider-JfaTT5:not(.isUnread-3Ef-o9) {						/* divider				time								*/
	border-color: rgba(var(--fontwhite1), 0.2);
}
.divider-JfaTT5.hasContent-1cNJDh {							/* divider				hascontent							*/
	border-color: transparent;
}
.unreadPill-2HyYtt {										/* divider				unreadPill							*/
	color: rgb(var(--fontwhite1));
}
.content-1o0f9g {											/* divider				content								*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
	color: rgb(var(--fontwhite3));
	width: 100%;
	text-align: center;
}

.hasMore-3POVhk {											/* bar					hasmore								*/
	box-shadow: inset 0 0 0 1px rgba(var(--fontwhite1), 0.1);
}
.hasMore-3POVhk:hover {
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
.jumpToPresentBar-G1R9s6 {									/* bar					jumptopresent						*/
	background-color: transparent;
	overflow: hidden;
	opacity: 1;
}
.jumpToPresentBar-G1R9s6::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--vbackground) var(--vbackgroundposition)/var(--vbackgroundsize);
	background-attachment: fixed;
	filter: blur(var(--vbackgroundblur));
	pointer-events: none;
	z-index: -1;
}
.jumpToPresentBar-G1R9s6::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.2));
	pointer-events: none;
	z-index: -1;
}
.barButtonBase-3UKlW2 {										/* bar					text								*/
	color: rgb(var(--fontwhite1));
}

/* ====		6.2.1.	MESSAGE							==== */

#app-mount .message-2qRu38 {								/* message				confirm modal						*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
	box-shadow: none;
}
.message-2qnXI6,											/* message				container							*/
.wrapper-1F5TKx,											/* message				loading 							*/
.message-2DieIs,											/* message				mention popout						*/
.message-2g38UB,											/* message				inbox popout						*/
.message-2qRu38 .wrapper-2a6GCs,							/* message				settings preview					*/
.messageGroupCozy-2iY6cT,									/* message				pin popout							*/
.messageGroupCozy-2-Q370 {									/* message				searchpage							*/
	background-color: rgba(var(--vtransparencycolor), var(--vmessagetransparency));
	contain: unset;
}
.message-2qnXI6.selected-2P5D_Z,
.mouse-mode .message-2qnXI6:hover,
.mouse-mode.full-motion .message-2qnXI6:hover,
.mouse-mode .wrapper-1F5TKx:hover,
.mouse-mode.full-motion .wrapper-1F5TKx:hover {
	background-color: rgba(var(--vtransparencycolor), calc(var(--vmessagetransparency) * 1.2 * var(--vusechatbubbles) + 0.3 * (1 - var(--vusechatbubbles))));
}
.message-2qnXI6.ephemeral-1PsL1r,							/* message				localbot							*/
.message-2qnXI6.replying-1x3H0T {							/* message				replying							*/
	background-image: linear-gradient(rgba(var(--vaccentcolor), calc(0.1 * (1 - var(--vusechatbubbles)))), rgba(var(--vaccentcolor), calc(0.2 * (1 - var(--vusechatbubbles)))));
}
.message-2qnXI6.mentioned-xhSam7 {							/* message				mentioned							*/
	background-image: linear-gradient(rgba(var(--vaccentcolor), calc(0.2 * (1 - var(--vusechatbubbles)))), rgba(var(--vaccentcolor), calc(0.2 * (1 - var(--vusechatbubbles)))));
}
.message-2qnXI6.ephemeral-1PsL1r::before,
.message-2qnXI6.replying-1x3H0T::before,
.message-2qnXI6.mentioned-xhSam7::before {
	background-color: rgb(var(--vaccentcolor));
}
.message-2qnXI6.mentioned-xhSam7 .markup-2BOw-j {
	border-radius: 3px;
	background-color: rgba(var(--vaccentcolor), calc(0.3 * var(--vusechatbubbles)));
}
#app-mount .avatar-1BDn8e,									/* message				container avatar					*/
#app-mount .avatar-2daVqv {									/* message				loading avatar						*/
	position: absolute;
	top: 2px;
	left: calc(-70px * var(--vusechatbubbles) + 16px);
}
#app-mount .repliedMessage-VokQwo ~ * .avatar-1BDn8e {
	top: 24px;
}
.container-3FojY8 .avatar-1BDn8e {
	left: calc(-10px * var(--vusechatbubbles));
}
#app-mount .replyBadge-r1su3o {
	background-color: rgba(var(--vtransparencycolor), 0.5);
}
#app-mount .repliedMessage-VokQwo::before {
	border-color: rgba(var(--vtransparencycolor), 0.5);
	left: calc((-41px * var(--vusechatbubbles)) + ((1 - var(--vusechatbubbles)) * (-1*(var(--avatar-size)/2 + var(--gutter)))));
	right: unset;
	width: 32px;
}
.cozy-3raOZG .header-23xsNx::after,							/* message				container header					*/
.cozy-12kSNU .header-1oLBbW::after {						/* message				loading header						*/
	content: "";
	position: absolute;
	top: 12px;
	left: -32px;
	border: 10px solid transparent;
	border-right: 12px solid rgba(var(--vtransparencycolor), var(--vmessagetransparency));
}
.cozy-3raOZG .container-3FojY8 .header-23xsNx::after {
	left: 40px;
}
.messageGroupWrapper-o-Zw7G .messageGroupCozy-2iY6cT .header-23xsNx::after,
.searchResult-9tQ1uo .messageGroupCozy-2-Q370 .header-23xsNx::after {
	top: 2px;
}
.cozy-3raOZG .timestamp-3ZCmNB.alt-1uNpEt {
	left: calc(-78px * var(--vusechatbubbles));
}
.cozy-3raOZG .iconContainer-3GkGRf {
	background-color: rgba(var(--vtransparencycolor), var(--vmessagetransparency));
	border-radius: 50%;
	left: calc(1px * (-58 * var(--vusechatbubbles) + -48 * (1 - var(--vusechatbubbles))));
	height: 25px;
	width: 25px;
	padding: 0;
}
.cozy-3raOZG .blockedSystemMessage-2Rk1ek .iconContainer-3GkGRf {
	background-color: transparent;
}
.cozy-3raOZG .iconContainer-3GkGRf::after {
	content: "";
	position: absolute;
	top: 2px;
	left: 26px;
	border: 10px solid transparent;
	border-right: 12px solid rgba(var(--vtransparencycolor), var(--vmessagetransparency));
}
.cozy-3raOZG .blockedSystemMessage-2Rk1ek .iconContainer-3GkGRf::after {
	display: none;
}
.selected-2P5D_Z.message-2qnXI6.cozy-3raOZG .header-23xsNx::after, 
.mouse-mode .message-2qnXI6.cozy-3raOZG:hover .header-23xsNx::after,
.mouse-mode.full-motion .message-2qnXI6.cozy-3raOZG:hover .header-23xsNx::after,
.mouse-mode .wrapper-1F5TKx.cozy-12kSNU:hover .header-1oLBbW::after,
.mouse-mode.full-motion .wrapper-1F5TKx.cozy-12kSNU:hover .header-1oLBbW::after
.selected-2P5D_Z.message-2qnXI6.cozy-3raOZG .iconContainer-3GkGRf::after,
.mouse-mode .message-2qnXI6.cozy-3raOZG:hover .iconContainer-3GkGRf::after,
.mouse-mode.full-motion .message-2qnXI6.cozy-3raOZG:hover .iconContainer-3GkGRf::after {
	border-right-color: rgba(var(--vtransparencycolor), calc(var(--vmessagetransparency) * 1.2));
}
#app-mount .ephemeral-1PsL1r.cozy-3raOZG .header-23xsNx::after,
#app-mount .replying-1x3H0T.cozy-3raOZG .header-23xsNx::after,
#app-mount .mentioned-xhSam7.cozy-3raOZG .header-23xsNx::after {
	border-right-color: rgba(var(--vaccentcolor), calc(var(--vmessagetransparency) * 100000000000000000000000000000));
}
.message-2DieIs,
.message-2g38UB,
.zalgo-jN1Ica .messageContent-2qWWxC,
.zalgo-jN1Ica.cozy-3raOZG .header-23xsNx,
.wrapper-1F5TKx,
.cozy-12kSNU .header-1oLBbW {
	overflow: visible;
}
.container-3FojY8 {
	padding: 0;
	overflow: visible;
}
#app-mount .cozyMessage-3V1Y8y,								/* message				container cozy						*/
#app-mount .cozy-12kSNU {									/* message				loading cozy						*/
	margin-left: calc(80px * var(--vusechatbubbles));
	padding-left: calc(1px * (10 * var(--vusechatbubbles) + 72 * (1 - var(--vusechatbubbles))));
}
#app-mount .compact-3Dy1Ya {								/* message				loading compact						*/
	margin-top: .0625rem;
}
#app-mount .cozy-3raOZG .header-23xsNx,
#app-mount .cozy-3raOZG .messageContent-2qWWxC,
#app-mount .cozy-12kSNU .header-1oLBbW {
	margin-left: 0;
	padding-left: 0;
}
.messageContainer-gbhlwo .wrapper-2a6GCs,
.messages-3G3erD .wrapper-2a6GCs,
.message-2qRu38 .wrapper-2a6GCs,
.messageGroupWrapper-o-Zw7G .messageGroupCozy-2iY6cT,
.searchResult-9tQ1uo .messageGroupCozy-2-Q370 {
	border-radius: 5px;
	margin-left: calc(60px * var(--vusechatbubbles));
	padding-left: calc(1px * (10 * var(--vusechatbubbles) + 72 * (1 - var(--vusechatbubbles))));
}
.messages-3G3erD .wrapper-2a6GCs {
	border-radius: 0;
}

.avatar-2daVqv {											/* message				loading avatar						*/
	background: rgba(var(--vtransparencycolor), 0.4);
	opacity: 1 !important;
}
.attachment-2p5mHK,											/* message				loading attachment					*/
.blob-2w7iIK {												/* message				loading blob						*/
	background: rgb(var(--vaccentcolor));
}

.expanded-13sWhZ {											/* message				expanded blocked					*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
	border-radius: 5px 5px 0 5px;
	margin-bottom: .5625rem;
}

.edited-DL9ECl {											/* message				editedtag							*/
	color: rgb(var(--fontwhite3));
}

.timestampCozy-1HNQR2,										/* message				timestamp							*/
.timestampCompact-29LLPQ,
.timestamp-1E3uAL {
	color: rgb(var(--fontwhite3));
}

.reaction-1hd86g {											/* message				reaction							*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
.reactionCount-2mvXRV {										/* message				reactioncount						*/
	color: rgb(var(--fontwhite4));
}
.reaction-1hd86g:hover .reactionCount-2mvXRV {
	color: rgb(var(--fontwhite2));
}

.wrapper-2aW0bm {											/* message				buttons								*/
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.25));
	position: relative;
}
.wrapper-2aW0bm::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--vpopout) var(--vpopoutposition)/var(--vpopoutsize);
	background-attachment: fixed;
	filter: blur(var(--vpopoutblur));
	width: unset;
	height: unset;
	border-radius: 4px;
	pointer-events: none;
	z-index: -1;
}
.separator-42rNt0 {											/* message				buttonsseparator					*/
	border-left-color: rgba(var(--fontwhite1), 0.1);
}
.button-1ZiXG9:hover {										/* message				button								*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
.button-1ZiXG9.selected-LCBEAU {
	background-color: rgba(var(--vtransparencycolor), 0.4);
}

#app-mount .ephemeralMessage-1fEWtQ,						/* message				localbotoperations					*/
#app-mount .operations-36ENbA {								/* message				editoperations						*/
	color: rgb(var(--fontwhite3));
}

.bumpBox-1r5p3c {											/* messageelement		publish box							*/
	background-color: rgba(var(--vtransparencycolor), 0.4);
}

.markup-2BOw-j {											/* message				markup								*/
	color: rgb(var(--fontwhite2));
}
.markup-2BOw-j code {										/* messageelement		code								*/
	background-color: transparent;
	border-color: transparent;
}
.markup-2BOw-j pre {										/* messageelement		pre									*/
	background-color: rgba(var(--vtransparencycolor), 0.4);
	border-color: rgba(var(--vtransparencycolor), 0.1);
}
.markup-2BOw-j .inline,										/* messageelement		inline								*/
.after_inlineCode-1KfVgj,
.before_inlineCode-1G9rTK,
.inlineCode-2ngu6Y {
	background-color: rgba(var(--vtransparencycolor), 0.4);
}
.markup-2BOw-j .hljs {										/* messageelement		hljs								*/
	color: rgb(var(--fontwhite2));
}
.blockquoteDivider-2hH8H6 {									/* messageelement		quotedivider						*/
	background-color: rgb(var(--fontwhite4));
}

#app-mount .spoilerText-3p6IlD {							/* messageelement		spoiler								*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
#app-mount .spoilerText-3p6IlD.hidden-HHr2R9 {				/* messageelement		hiddenspoiler						*/
	background-color: rgba(var(--vtransparencycolor), 0.5);
}

.container-3-pyIM {											/* systemmessage		content								*/
	color: rgb(var(--fontwhite3));
}
.icon-2Po-VO[style*="/assets/5da4cdab01d4d89c593c48c62ae0d937.svg"] {		/* systemmessage			pinicon									*/
	-webkit-mask: url(https://discordapp.com/assets/5da4cdab01d4d89c593c48c62ae0d937.svg) center/cover no-repeat;
	background: rgb(var(--fontwhite3)) !important;
}
.icon-2Po-VO[style*="/assets/d80d1fdc43a3c42134a31a39581160ac.svg"] {		/* systemmessage			missedcall								*/
	-webkit-mask: url(https://discordapp.com/assets/d80d1fdc43a3c42134a31a39581160ac.svg) center/cover no-repeat;
	background: rgb(var(--fontwhite3)) !important;
}
.icon-2Po-VO[style*="/assets/b8029fe196b8f1382e90bbe81dab50dc.svg"] {		/* systemmessage			joincallicon							*/
	-webkit-mask: url(https://discordapp.com/assets/b8029fe196b8f1382e90bbe81dab50dc.svg) center/cover no-repeat;
	background: rgb(var(--vaccentcolor)) !important;
}
.icon-2Po-VO[style*="/assets/c30220457097b064286a8759a9b6c4af.svg"] {		/* systemmessage			recievecallicon							*/
	-webkit-mask: url(https://discordapp.com/assets/c30220457097b064286a8759a9b6c4af.svg) center/cover no-repeat;
	background: rgb(var(--vaccentcolor)) !important;
}

/* ====		6.2.2.	EMBEDS							==== */

#app-mount .embedFull-2tM8-- {								/* embed				wrapper								*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
	border-left-color: rgb(var(--fontwhite4));
}
#app-mount .embedAuthorName-3mnTWj,							/* embed				author								*/
#app-mount .embedFieldName-NFrena,							/* embed				fieldname							*/
#app-mount .embedTitle-3OXDkz {								/* embed				title								*/
	color: rgb(var(--fontwhite1)) !important;
}
#app-mount .embedDescription-1Cuq9a,						/* embed				description							*/
#app-mount .embedFieldValue-nELq2s {						/* embed				fieldvalue							*/
	color: rgb(var(--fontwhite3));
}
#app-mount .embedProvider-3k5pfl {							/* embed				provider							*/
	color: rgb(var(--fontwhite3)) !important;
}
#app-mount .embedFooterText-28V_Wb {						/* embed				footer								*/
	color: rgb(var(--fontwhite4));
}

#app-mount .attachment-33OFj0 {								/* attachment			container							*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
	border-color: rgba(var(--vtransparencycolor), 0.1);
	margin-left: 18px;
}
#app-mount .message-2qnXI6 .attachment-33OFj0 {
	margin-left: 0;
}
#app-mount .filename-3eBB_v {								/* attachment			filename							*/
	color:	rgb(var(--fontwhite1));
}
#app-mount .size-1Arx_I {									/* attachment			sizesize							*/
	color:	rgb(var(--fontwhite4));
}
#app-mount .metadata-3WGS0M {								/* attachment			metadata							*/
	color: rgb(var(--fontwhite4));
}
#app-mount .cancelButton-3hVEV6,							/* attachment			cancelbutton						*/
#app-mount .downloadButton-23tKQp {							/* attachment			downloadbutton						*/
	color: rgb(var(--fontwhite4));
}
#app-mount .cancelButton-3hVEV6:hover,
#app-mount .downloadButton-23tKQp:hover {
	color: rgb(var(--fontwhite3));
}
#app-mount .cancelButton-3hVEV6:active,
#app-mount .downloadButton-23tKQp:active {
	color: rgb(var(--fontwhite2));
}
#app-mount .twitchSectionPlayButton-2RamGG {
	background-image: url('data:image/svg+xml; utf8, <svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 32 32" fill="none"><path d="M12.3333 10.002V22.002L22.3333 16.002L12.3333 10.002Z" fill="rgb(185,187,190)"/></svg>');
	background-color: rgba(var(--vtransparencycolor), 0.4);
	border-radius: 50%;
	object-position: -9999999px -9999999px;
}
#app-mount .twitchSectionPlayButton-2RamGG:hover {
	background-color: rgba(var(--vtransparencycolor), 0.8);
}

#app-mount .wrapper-2TxpI8 {								/* attachment			videowrapper						*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}

#app-mount .embedSuppressButton-1FonMn {					/* attachment			closebutton							*/
	color: rgb(var(--fontwhite3));
}
#app-mount .embedSuppressButton-1FonMn:hover {
	color: rgb(var(--fontwhite3));
}

/* ====		6.2.3.	NITROGIFT						==== */

#app-mount .tile-2OwFgW {									/* gift					container							*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
	box-shadow: 0 0 0 rgba(var(--vtransparencycolor), 0.15);
}
#app-mount .title-1rUb9I {									/* gift					title								*/
	color: rgb(var(--fontwhite2));
}
#app-mount .tagline-2nvxi0 {								/* gift					tagline								*/
	color: rgb(var(--fontwhite4));
}

/* ====		6.2.4.	INVITE							==== */

#app-mount .wrapper-35wsBm {								/* invite				container							*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
	border-color: rgba(var(--vtransparencycolor), 0.1);
}
#app-mount .guildIconImage-3qTk45 {							/* invite				icon								*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
#app-mount .guildName-2hvnt_ {								/* invite				name								*/
	color: rgb(var(--fontwhite1));
}
#app-mount .guildDetail-1nRKNE {							/* invite				details								*/
	color: rgb(var(--fontwhite4));
}

#app-mount .invite-18yqGF {									/* invite				group invite						*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
	border-color: rgba(var(--vtransparencycolor), 0.1);
}
#app-mount .header-Hg_qNF {
	color: rgb(var(--fontwhite3));
}
#app-mount .name-GG2Mcs,
#app-mount .partyStatus-6AjDud {
	color: rgb(var(--fontwhite1));
}
#app-mount .moreUsers-1sZP3U {
	background-color: rgba(var(--vtransparencycolor), 0.3);
	color: rgb(var(--fontwhite3));
}
#app-mount .partyMemberEmpty-2iyh5g {
	background-color: rgba(var(--vtransparencycolor), 0.3);
}


/* ----		6.3.	TEXTAREA						---- */

.form-2fGMdU {												/* textarea				form								*/
	padding-top: 0;
	margin-top: 0;
}
.form-2fGMdU::before {
	display: none;
}

.channelTextArea-rNsIhG {									/* textarea				channeltextarea						*/
	background-color: transparent;
	border-top-color: rgba(var(--fontwhite1), 0.1);
}

.container-2fRDfG {											/* textarea				reply								*/
	background: rgba(var(--vtransparencycolor), 0.3);
	border: none;
	border-bottom: 1px solid rgba(var(--fontwhite1), 0.1);
}

.scrollableContainer-2NUZem {								/* textarea				container							*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}

.attachButtonPlus-jWVFah {									/* textarea				attachbuttoninner					*/
	fill: rgb(var(--fontwhite3));
}
.attachButton-2WznTc:hover .attachButtonPlus-jWVFah {
	fill: rgb(var(--fontwhite2));
}
.attachButton-2WznTc:active .attachButtonPlus-jWVFah {
	fill: rgb(var(--fontwhite1));
}
.attachWrapper-2TRKBi {										/* textarea				attachdivider						*/
	border-color: rgb(var(--fontwhite3));
}

#app-mount .textArea-12jD-V {								/* textarea				textarea							*/
	color: rgb(var(--fontwhite1));
}
#app-mount .textArea-12jD-V::placeholder {
	color: rgb(var(--fontwhite4));
}
.placeholder-37qJjk,
.slateTextArea-1Mkdgw .hljs-comment,
.slateTextArea-1Mkdgw .hljs-quote {
	color: rgb(var(--fontwhite4));
}

.button-3AYNKb {											/* textarea				buttons								*/
	color: rgb(var(--fontwhite3));
}
.button-3AYNKb:hover,
.buttonWrapper-1ZmCpA:hover .icon-3D60ES {
	color: rgb(var(--fontwhite2));
}
.active-23Nm0T .icon-3D60ES,
.active-23Nm0T:hover .icon-3D60ES {
	color: rgb(var(--fontwhite1));
}
.sprite-2iCowe {											/* textarea				emojibutton							*/
	transform: none !important;
}

.base-gE7OpD {												/* textarea				typingusers							*/
	color: rgb(var(--fontwhite1));
}

.wrapper-39oAo3 {											/* textarea				placeholder							*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
	color: rgb(var(--fontwhite2));
}

.toolbar-2bjZV7 {											/* textarea				formattoolbar						*/
	background-color: rgb(var(--vaccentcolor));
}
.toolbar-2bjZV7::before {
	border-top-color: rgb(var(--vaccentcolor));
}
.divider-24xeUg {											/* textarea				formattoolbardivider				*/
	border-left-color: rgba(var(--fontwhite1), 0.1);
}
.active-2HPddW,												/* textarea				buttonactive						*/
.hover-28QbSq:hover {										/* textarea				buttonhover							*/
	background-color: rgba(var(--fontwhite1), 0.2);
}
.icon-KgGMGo {												/* textarea				buttonicon							*/
	color: rgb(var(--fontwhite2));
}
.active-2HPddW .icon-KgGMGo,
.hover-28QbSq:hover .icon-KgGMGo {
	color: rgb(var(--fontwhite1));
}

#app-mount .pill-2pQByF {									/* textarea				command query pill					*/
	background-color: rgba(var(--vtransparencycolor), 0.5);
	border-radius: 5px;
}

/* ----		6.4.	AUTOCOMPLETEMENU				---- */

#app-mount .autocomplete-1vrmpx {							/* autocomplete			container							*/
	background-color: transparent;
	overflow: hidden;
}
#app-mount .autocomplete-1vrmpx::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--vpopout) var(--vpopoutposition)/var(--vpopoutsize);
	background-attachment: fixed;
	filter: blur(var(--vpopoutblur));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
#app-mount .autocomplete-1vrmpx::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.25));
	width: unset;
	height: unset;
	border-radius: 5px;
	pointer-events: none;
	z-index: -1;
}
.theme-brand .autocomplete-1vrmpx {
	background: rgb(var(--vaccentcolor)) linear-gradient(rgba(var(--vtransparencycolor), 0.2), rgba(var(--vtransparencycolor), 0.2)) !important;
}
.theme-brand .autocomplete-1vrmpx::before,
.theme-brand .autocomplete-1vrmpx::after {
	display: none;
}
#app-mount .bar-AokMp3 {									/* autocomplete			command info						*/
	background-color: transparent;
}
#app-mount .container-3ISnnM::after {
	box-shadow: inset 0 -7px 12px -7px rgba(var(--vtransparencycolor), 0.3);
}
#app-mount .header-1TOWci {									/* autocomplete			header								*/
	box-shadow: 0 1px 0 0 rgba(var(--vtransparencycolor), 0.2), 0 1px 2px 0 rgba(var(--vtransparencycolor), 0.2);
}
#app-mount .contentTitle-2tG_sM {							/* autocomplete			searchtitle							*/
	color: rgb(var(--fontwhite3));
}
#app-mount .contentTitle-2tG_sM strong {
	color: rgb(var(--fontwhite1));
}
#app-mount .divider-23swzi {								/* autocomplete			divider								*/
	background-color: rgba(var(--fontwhite4), 0.3);
}
#app-mount .selected-1Tbx07 {								/* autocomplete			rowselected							*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
#app-mount .content-Qb0rXO {								/* autocomplete			rowcontent							*/
	color: rgb(var(--fontwhite2));
}
#app-mount .iconForeground-1w5n7R {							/* autocomplete			icon								*/
	fill: rgb(var(--fontwhite3));
}
#app-mount .description-11DmNu,								/* autocomplete			description							*/
#app-mount .descriptionUsername-J_75O8 {					/* autocomplete			username							*/
	color: rgb(var(--fontwhite3));
}
#app-mount .descriptionDiscriminator-3vUOCc {				/* autocomplete			discriminator						*/
	color: rgb(var(--fontwhite3));
}
#app-mount .option-1B5ZV8 {									/* autocomplete			option								*/
	background-color: rgba(var(--vtransparencycolor), 0.5);
}
#app-mount .selected-1Tbx07 .content-Qb0rXO {
	color: rgb(var(--fontwhite1));
}
#app-mount .selected-1Tbx07 .iconForeground-1w5n7R {
	fill: rgb(var(--fontwhite2));
}
#app-mount .selected-1Tbx07 .description-11DmNu,
#app-mount .selected-1Tbx07 .descriptionUsername-J_75O8 {
	color: rgb(var(--fontwhite2));
}
#app-mount .selected-1Tbx07 .descriptionDiscriminator-3vUOCc {
	color: rgb(var(--fontwhite2));
}

#app-mount .wrapper-uf3cnO {								/* autocomplete			categories							*/
	background-color: transparent;
}
#app-mount .selected-3xBBKs,								/* autocomplete			category selected					*/
#app-mount .selected-3xBBKs:hover {
	background-color: rgb(var(--vaccentcolor));
}

#app-mount .searchSuggestion-2K8OBX:hover {					/* gifpicker			suggestions							*/
	color: rgb(var(--fontwhite1));
}

#app-mount .placeholder-1kJjXI {							/* gifpicker			result placeholder					*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}


/* ----		6.5.	MEMBERLIST						---- */

.member-3-YXUe {											/* member				container							*/
	color: rgb(var(--fontwhite3));
}
.clickable-1JJAn8.member-3-YXUe:hover {
	color: rgb(var(--fontwhite2));
}
.clickable-1JJAn8.member-3-YXUe:active,
.selected-aXhQR6.member-3-YXUe {
	color: rgb(var(--fontwhite1));
}
.member-3-YXUe:hover .layout-2DM8Md {						/* member				inner								*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
.selected-aXhQR6.member-3-YXUe .layout-2DM8Md {
	background-color: rgb(var(--vaccentcolor));
	text-shadow: 1px 1px var(--vtextshadow);
}
.selected-aXhQR6.member-3-YXUe .layout-2DM8Md svg:not(.svg-2V3M55) {
	filter: drop-shadow(1px 1px var(--vtextshadow));
}
.member-3-YXUe .name-uJV0GL {
	color: rgb(var(--fontwhite2));
}
.member-3-YXUe .activity-2Gy-9S {
	color: rgb(var(--fontwhite3));
}
.member-3-YXUe:hover .linkButtonIcon-Mlm5d6,
.member-3-YXUe.selected-aXhQR6 .linkButtonIcon-Mlm5d6 {
	color: rgb(var(--fontwhite1));
}
.member-3-YXUe:hover .name-uJV0GL,
.member-3-YXUe.selected-aXhQR6 .name-uJV0GL {
	color: rgb(var(--fontwhite1));
}
.member-3-YXUe:hover .activity-2Gy-9S,
.member-3-YXUe.selected-aXhQR6 .activity-2Gy-9S {
	color: rgb(var(--fontwhite2));
}
.member-3-YXUe.selected-aXhQR6 .premiumIcon-2IFPOX {
	color: rgb(var(--fontwhite1)) !important;
}

.membersGroup-v9BXpm {										/* roleheader												*/
	color: rgb(var(--fontwhite2));
}

.avatar-VxgULZ::before {										/* emptyavatar												*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}

.memberGroupsPlaceholder-3mwPub,							/* loadingplaceholders										*/
.placeholderAvatar-damqh6,
.placeholderUsername-2B_OA9 {
	background-color: rgba(var(--vtransparencycolor), 0.4);
}

/* ----		6.6.	SEARCHPAGE						---- */

#app-mount .searchResultsWrap-3-pOjs {						/* searchpage			container							*/
	background-color: transparent;
}
#app-mount .searchHeader-2XoQg7 {							/* searchpage			header								*/
	background-color: rgba(var(--vtransparencycolor), calc(var(--vguildchanneltransparency) * 0.8));
	box-shadow: 0 1px 0 rgba(var(--vtransparencycolor), 0.2);
}
#app-mount .searchHeader-2XoQg7 .totalResults--dyAxF {		/* searchpage			results								*/
	color: rgb(var(--fontwhite3));
	opacity: 1;
}
#app-mount .searchHeader-2XoQg7 .tab-2j5AEF {				/* searchpage			tab									*/
	color: rgb(var(--fontwhite3));
	opacity: 1;
}
#app-mount .searchHeader-2XoQg7 .tab-2j5AEF:hover {
	color: rgb(var(--fontwhite2));
	border-bottom-color: rgb(var(--fontwhite2));
}
#app-mount .searchHeader-2XoQg7 .tab-2j5AEF.selected-2LAck8 {
	color: rgb(var(--fontwhite1));
	border-bottom-color: rgb(var(--fontwhite1));
}
#app-mount .scroller-3GIiMh {
	background-color: rgba(var(--vtransparencycolor), calc(var(--vguildchanneltransparency) * 0.5));
}
#app-mount .channelSeparator-1DOiGt {						/* searchpage			separator							*/
	overflow: hidden;
	width: 390px;
}
#app-mount .channelSeparator-1DOiGt:not(:empty)::before {
	display: none;
}
#app-mount .channelSeparator-1DOiGt .channelName-1JRO3C {	/* searchpage			channelname							*/
	background: transparent;
	color: rgb(var(--fontwhite3));
}
#app-mount .channelSeparator-1DOiGt .channelName-1JRO3C::after {
	content: "";
	border-bottom: 1px solid rgba(var(--fontwhite3), 0.5);
	height: 1px;
	margin-left: 10px;
	position: absolute;
	pointer-events: none;
	top: 50%;
	width: 100vw;
	z-index: 0;
}
.searchResult-9tQ1uo::before,								/* searchpage			result								*/
.searchResult-9tQ1uo::after {
	display: none;
}
#app-mount .searchResult-9tQ1uo .hit-1fVM9e {
	background-color: rgba(var(--vtransparencycolor), 0.1);
	border-color: rgba(var(--vtransparencycolor), 0.1);
	box-shadow: none;
}
#app-mount .searchResult-9tQ1uo.expanded-w_LCGl {
	background-color: rgba(var(--vtransparencycolor), 0.1);
	border-color: rgba(var(--vtransparencycolor), 0.1);
}
#app-mount .searchResult-9tQ1uo:not(.expanded-w_LCGl) .before-2RL1Gz.sibling-1eJVjd {
	-webkit-mask: linear-gradient(to bottom, rgba(0,0,0,1) 0%, rgba(0,0,0,0.9) 50%, rgba(0,0,0,0.1) 85%, rgba(0,0,0,0) 100%);
}
#app-mount .searchResult-9tQ1uo:not(.expanded-w_LCGl) .after-20SH8W.sibling-1eJVjd {
	-webkit-mask: linear-gradient(to top, rgba(0,0,0,0) 0%, rgba(0,0,0,0.8) 30%, rgba(0,0,0,0.9) 50%, rgba(0,0,0,0.1) 85%, rgba(0,0,0,0) 100%);
}
#app-mount .searchResult-9tQ1uo:not(.expanded-w_LCGl) .before-2RL1Gz:not(.sibling-1eJVjd),
#app-mount .searchResult-9tQ1uo:not(.expanded-w_LCGl) .after-20SH8W:not(.sibling-1eJVjd) {
	display: none;
}

.jumpButton-JkYoYK {										/* message				jumpbutton							*/ 
	background-color: rgba(var(--vtransparencycolor), 0.4);
	color: rgb(var(--fontwhite2));
}
.jumpButton-JkYoYK:hover {
	background-color: rgb(var(--vaccentcolor));
	color: rgb(var(--fontwhite1));
}
.jumpButton-JkYoYK + .jumpButton-JkYoYK {
	margin-left: 2px;
}

#app-mount .pagination-2KMrRB {
	color: rgb(var(--fontwhite3));
}

/* ----		6.7.	CALL							---- */

#app-mount .incomingCallInner-2VmFiR,
#app-mount .root-3JVdIJ {									/* popout				inner								*/
	background-color: transparent;
	border: none;
}
.incomingCallInner-2VmFiR::before,
.root-3JVdIJ::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--vpopout) var(--vpopoutposition)/var(--vpopoutsize);
	background-attachment: fixed;
	filter: blur(var(--vpopoutblur));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.incomingCallInner-2VmFiR::after,
.root-3JVdIJ::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.25));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
#app-mount .members-2BNiuX {								/* popout				members							*/
	color: rgb(var(--fontwhite1));
}
#app-mount .subtitle-1H8FPn {								/* popout				subtitle						*/
	color: rgb(var(--fontwhite3));
}

#app-mount .wrapper-2qzCYF {								/* call					wrapper							*/
	background-color: rgba(var(--vtransparencycolor), calc(var(--vguildchanneltransparency) * 0.8));
}
#app-mount .root-217Brm {									/* call					root							*/
	color: rgb(var(--fontwhite1));
}
.videoWrapper-2v09vt {										/* call					video wrapper					*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
.video-1FfuMD {												/* call					video							*/
	background-color: transparent;
}
.tile-2naSqK,												/* call					user video voicechannel			*/
.tile-2gi3tr {												/* call					user video dm					*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
.gradientContainer-10lXLB {									/* call					gradientcontainer				*/
	display: none;
}
.participantsButton-KYW-IW {								/* call					participantsbutton				*/
	background-color: rgba(0, 0, 0, 0.3);
}
.participantsButton-KYW-IW:hover {
	background-color: rgba(0, 0, 0, 0.6);
}
.centerButton-3CaNcJ,
.colorable-1bkp8v.primaryDark-3mSFDl {
	background-color: rgba(var(--vtransparencycolor), 0.5);
}
.centerButton-3CaNcJ:hover,
.colorable-1bkp8v.primaryDark-3mSFDl:hover {
	background-color: rgb(var(--vaccentcolor));
}
.button-3HqqDX {
	background-color: rgba(var(--vtransparencycolor), 0.4);
	color: rgb(var(--fontwhite1));
}
.button-3HqqDX:hover {
	background-color: rgba(var(--vtransparencycolor), 0.6);
}
.controlButton-2MhVEL.leaveButton-2YnTyt {
	background-color: rgba(240, 71, 71, 0.5);
}
.controlButton-2MhVEL.leaveButton-2YnTyt:hover {
	background-color: rgb(240, 71, 71);
}
.regionSelectPopout-p9-0_W {
	width: 170px;
}

/* ----		6.8.	UNAVAILABLESCREEN				---- */

.category-2haXBH,											/* loadingplaceholders										*/
.channelIcon-1TvDoP,
.channelName-2wrHHc {
	background: rgba(var(--vtransparencycolor), 0.4);
}
.splashImage-13vBzp {										/* screen				image								*/
	opacity: 0.7;
}
.splashHeader-ehL7gZ {										/* screen				headertext							*/
	color: rgb(var(--fontwhite1));
}


/* ~~~~		7.		PEOPLES							~~~~ */

.wrapper-1cBijl {											/* friendsadd			inputcontainer						*/
	background-color: rgba(var(--vtransparencycolor), 0.1);
	border-color: rgba(var(--vtransparencycolor), 0.3);
}
.wrapper-1cBijl:hover {
	border-color: rgb(var(--vtransparencycolor));
}
.wrapper-1cBijl .addFriendInput-4bcerK {
	color: rgb(var(--fontwhite1));
}
.wrapper-1cBijl .addFriendInput-4bcerK::placeholder,
.addFriendHint-3Y70FX {
	color: rgb(var(--fontwhite4));
}

.tableHeaderText-2io-_N,									/* tableheader			text								*/
.onlineStatusGroupTitle-6ObdV6 {							/* groupheader												*/
	color: rgb(var(--fontwhite2));
}

.tableHeader-2Ctu7Y {										/* tablerheader			border								*/
	border-top-color: rgba(var(--fontwhite4), 0.5);
}
.peopleListItem-2nzedh {									/* peoples				row									*/
	border-top-color: rgba(var(--fontwhite1), 0.1);
}
.peopleListItem-2nzedh .username-31C1TQ {					/* peoples				username							*/
	color: rgb(var(--fontwhite2));
}
.peopleListItem-2nzedh .discriminator-22Okc1 {				/* peoples				discriminator						*/
	color: rgb(var(--fontwhite4));
}
.peopleListItem-2nzedh .subtext-24R4-w {					/* peoples				subtext								*/
	color: rgb(var(--fontwhite3));
}
.peopleListItem-2nzedh .actionButton-uPB8Fs {				/* peoples				actionbutton						*/
	background-color: rgba(var(--vtransparencycolor), 0.1);
	color: rgb(var(--fontwhite3));
}
.peopleListItem-2nzedh:hover {
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
.peopleListItem-2nzedh:hover .username-31C1TQ {
	color: rgb(var(--fontwhite1));
}
.peopleListItem-2nzedh:hover .discriminator-22Okc1 {
	color: rgb(var(--fontwhite3));
}
.peopleListItem-2nzedh:hover .subtext-24R4-w {
	color: rgb(var(--fontwhite2));
}
.peopleListItem-2nzedh:hover .actionButton-uPB8Fs {
	background-color: rgba(var(--vtransparencycolor), 0.3);
	color: rgb(var(--fontwhite2));
}
.peopleListItem-2nzedh .actionButton-uPB8Fs:hover {
	background-color: rgb(var(--vaccentcolor));
	color: rgb(var(--fontwhite1));
}
.header-13Cw0- {											/* playing				header								*/
	color: rgb(var(--fontwhite2));
}
#app-mount .outer-1AjyKL {									/* playing				card								*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
#app-mount .outer-1AjyKL.active-1xchHY,
#app-mount .outer-1AjyKL.interactive-3B9GmY:hover {
	background-color: rgba(var(--vtransparencycolor), 0.4);
}
#app-mount .inset-3sAvek {									/* playing				card inner							*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
.emptyCard-1RJw8n {											/* playing				empty card							*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
#app-mount .partyMemberOverflow-lXnzvu {
	background: rgba(var(--vtransparencycolor), 0.5);
}
#app-mount .partyMemberBackground-3XOgDv,
#app-mount .partyMemberUnknown-fwK2DC {
	background-color: rgba(var(--vtransparencycolor), 0.5);
}
#app-mount .partyMemberUnknownIcon-1eDbV6 {
	color: color: rgb(var(--fontwhite4));
}
#app-mount .popout-38lTFE {									/* playing				popout								*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--vtransparencycolor), 0.3), 0 8px 16px 0 rgba(var(--vtransparencycolor), 0.3);
	overflow: hidden;
}
.popout-38lTFE::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--vpopout) var(--vpopoutposition)/var(--vpopoutsize);
	background-attachment: fixed;
	filter: blur(var(--vpopoutblur));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.popout-38lTFE::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.3));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
#app-mount .memberListItem-31QoHj:not(.popoutDisabled-2RK7MF):hover,
#app-mount .enabled-1t_Gxm:hover {
	background-color: rgba(var(--vtransparencycolor), 0.2);
}


/* ~~~~		7.		STORE/NITRO						~~~~ */

.gridItemBadge-1Se-Pu {
	text-shadow: 1px 1px var(--vtextshadow);
}
.gridItemHeading-3D4Rb2 {
	color: rgb(var(--fontwhite1));
}
.gridItemSubheading-FIneEP {
	color: rgb(var(--fontwhite1));
}

.marketingHeader-2Iq7qk {									/* marketingheader											*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}

.detailsBlock-FoDTGA {										/* billing 				details								*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}

.sectionHeader-127c3L {										/* header													*/
	color: rgb(var(--fontwhite1));
}
.tier2PlanName-2TttcQ {										/* header				svgtitle							*/
	color: rgb(var(--fontwhite1));
}
#app-mount .title-2a5mvx {									/* header				title								*/
	color: rgb(var(--fontwhite1));
}
#app-mount .subtitle-UfhpvR,								/* header				subtitle							*/
#app-mount .subtitleRepositioned-11uB9- {
	color: rgb(var(--fontwhite2));
}
.yearlyButtonDiscount-2K7GZZ {
	border-color: rgba(var(--fontwhite1), 0.3);
}

.subsectionHeader-1SVMaW {									/* subsection			header								*/
	color: rgb(var(--fontwhite1));
}
.blurb-1H7VPv {												/* subsection			description							*/
	color: rgb(var(--fontwhite2));
}
.title-3IUNJ6 {												/* subsection			featuretitle						*/
	color: rgb(var(--fontwhite1));
}
.description-yMw5z0 {										/* subsection			featuredescription					*/
	color: rgb(var(--fontwhite2));
}
.guildMoreFeatures-svfRvH {									/* subsection			footer								*/
	color: rgb(var(--fontwhite1));
}

#app-mount .categoryHeader-1D7Tqy,							/* categoryheader											*/
#app-mount .premiumApplicationsHeader-Zmkm5e {
	color: rgb(var(--fontwhite1));
	border-color: rgba(var(--fontwhite4), 0.3);
}

.gradientOverlay-298TBM {									/* cardscroller			gradient							*/
	display: none;
}
.scrollerButton-1Vm5_P {									/* cardscroller			button								*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
	color: rgb(var(--fontwhite1));
}

#app-mount .tile-QA_yMc {									/* gamecard				container							*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
	box-shadow: 0 0 0 rgba(var(--vtransparencycolor), 0.15);
}
#app-mount .description-2oYgWO {							/* gamecard				description							*/
	color: rgb(var(--fontwhite1));
}
#app-mount .tagline-EIH5-W,									/* gamecard				tagline								*/
#app-mount .title-2XwaXv {									/* gamecard				title								*/
	color: rgb(var(--fontwhite2));
}
#app-mount .perkTag-2O4dx4 {								/* gamecard				perktag								*/
	border-radius: 4px;
	color: rgb(var(--fontwhite1));
}

#app-mount .tier1Banner-1BTgv0 {							/* tier1banner			container							*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
	color: rgb(var(--fontwhite1));
}
.headerIcon-3bqya6 {										/* tier1banner			svgtitle							*/
	color: rgb(var(--fontwhite1));
}

.carouselButtonsContainer-Rba2-D {							/* gamepreview			container							*/
	color: rgb(var(--fontwhite1));
}
.smallCarousel-2e0IQc {
	background-color: rgba(var(--vtransparencycolor), 0.3);
	border-radius: 5px;
}
#app-mount .item-3V15ea {									/* gamepreview			previewitem							*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
.arrow-3jRqK8 {												/* gamepreview			prev/nextarrow (big)				*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
.arrow-vOpU7R {												/* gamepreview			prev/nextarrow (small)				*/
	color: rgb(var(--fontwhite1));
}
.dot-2Q_mMZ {												/* gamepreview			itemdot (small)						*/
	background-color: rgb(var(--fontwhite1));
}

#app-mount .root-1bFE0x {									/* gameinfo				sectioncontainer					*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
#app-mount .header-3HFF3R {									/* gameinfo				sectionheader						*/
	color: rgb(var(--fontwhite1));
}
#app-mount .section-7tu4tu {								/* gameinfo				subsection							*/
	border-bottom-color: rgba(var(--fontwhite4), 0.3);
}
#app-mount .playerOverflow-2Hf77M {
	background-color: rgba(var(--vtransparencycolor), 0.3);
	color: rgb(var(--fontwhite2));
}
#app-mount .description-2Ifi6N {							/* gameinfo				subsectiondescription				*/
	color: rgb(var(--fontwhite3));
}
#app-mount .description-2Ifi6N strong,
#app-mount .username-2gp_Xw {								/* gameinfo				subsectionusername					*/
	color: rgb(var(--fontwhite1));
}
#app-mount .smallHeader-2h-9-U {							/* gameinfo				subsectionheader					*/
	color: rgb(var(--fontwhite3));
}
#app-mount .text-1Z3P6i {									/* gameinfo				subsectiontext						*/
	color: rgb(var(--fontwhite1));
}
#app-mount .iconCircle-1dlYo0 {
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
#app-mount .circle-1nK_79 {
	color: rgb(var(--fontwhite1));
}

#app-mount .divider-21LyPb {								/* section				divider								*/
	border-color: rgba(var(--fontwhite4), 0.3);
}
#app-mount .blurb-1iBKJy {									/* section				description							*/
	color: rgb(var(--fontwhite1));
}
#app-mount .description-1AwRKJ,								/* section				subdescription						*/
#app-mount .markdown-11q6EU {
	color: rgb(var(--fontwhite3));
}

#app-mount .tile-PuWjfs {									/* perkcard				container							*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
	box-shadow: 0 0 0 rgba(var(--vtransparencycolor), 0.15);
}
.tile-PuWjfs div.splashPlaceholder-1ev-9c {					/* perkcard				imagecontainer						*/
	background-color: transparent;
	position: relative;
	z-index: 5;
}
.tile-PuWjfs div.splashPlaceholder-1ev-9c::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--vbackground) var(--vbackgroundposition)/var(--vbackgroundsize);
	background-attachment: fixed;
	filter: blur(var(--vbackgroundblur));
	pointer-events: none;
	z-index: -1;
}
.tile-PuWjfs div.splashPlaceholder-1ev-9c::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.2));
	pointer-events: none;
	z-index: -1;
}
.tile-PuWjfs img.splashPlaceholder-1ev-9c {					/* perkcard				image								*/
	-webkit-mask: linear-gradient(rgba(0,0,0,1) 60%, rgba(0,0,0,0) 100%);
}
.tile-PuWjfs .description-2h6giI {							/* perkcard				imagecontainer						*/
	color: rgb(var(--fontwhite1));
	z-index: 6;
}
#app-mount .mediaFade-2NVPtV {								/* perkcard				fade								*/
	background: transparent;
}
#app-mount .item-2yFVoY {									/* newscard				container							*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
	box-shadow: 0 0 0 rgba(var(--vtransparencycolor), 0.15);
}
#app-mount .collapsedTimestamp-2gjDIM,						/* newscard				timestamp							*/
#app-mount .openTimestamp-sTgPmn {
	color: rgb(var(--fontwhite3));
}
#app-mount .title-i-qCkH {									/* newscard				title								*/
	color: rgb(var(--fontwhite1));
}
#app-mount .openDescription-2XUOH3 {						/* newscard				description							*/
	color: rgb(var(--fontwhite3));
}

#app-mount .requirements-dEriwm {							/* requirements												*/
	color: rgb(var(--fontwhite2));
}
#app-mount .requirementKey-14DT2D {							/* requirements			key									*/
	color: rgb(var(--fontwhite4));
}
#app-mount .content-1zhNsr {								/* requirements			rating								*/
	color: rgb(var(--fontwhite4));
}
#app-mount .content-3FEARf {								/* requirements			copyright							*/
	color: rgb(var(--fontwhite4));
}

#app-mount .bodySection-jqkkIP {							/* sidebar				section								*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
	border-top-color: rgba(var(--fontwhite4), 0.3);
}
#app-mount .actionText-3EKWER {								/* sidebar				header								*/
	color: rgb(var(--fontwhite2));
}
#app-mount .purchaseUnitOperatingSystem-cnbJPz {			/* sidebar				OSicon								*/
	color: rgb(var(--fontwhite2));
}
#app-mount .price-4PDWNj,									/* sidebar				price								*/
#app-mount .listingPrice-2GiDSc {
	color: rgb(var(--fontwhite1));
}
#app-mount .title-2xCQKy {									/* sidebar				subtitle							*/
	color: rgb(var(--fontwhite1));
}
#app-mount .skuNormal-3h1es- {								/* sidebar				pricerow							*/
	border-bottom-color: rgba(var(--fontwhite4), 0.4);
}
#app-mount .name-u2zgy7 {									/* sidebar				pricename							*/
	color: rgb(var(--fontwhite3));
}
#app-mount .price-NUANu6 {									/* sidebar				priceamount							*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
	color: rgb(var(--fontwhite1));
}
#app-mount .label-13UUcd {									/* sidebar				label								*/
	color: rgb(var(--fontwhite4));
}
#app-mount .info-1Emy1X {									/* sidebar				labelinfo							*/
	color: rgb(var(--fontwhite1));
}

#app-mount .content-35aVm0 {								/* invitecard			container							*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
#app-mount .name-3TBxUq {									/* invitecard			guildname							*/
	color: rgb(var(--fontwhite3));
}
#app-mount .memberInfo-1TAaKC {								/* invitecard			memberinfo							*/
	color: rgb(var(--fontwhite4));
}

#app-mount .row-1bU71H {									/* features				row									*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
	color: rgb(var(--fontwhite3));
}
#app-mount .featureIcon-1f78KU {							/* features				featureicon							*/
	color: rgb(var(--fontwhite3));
}
#app-mount .feature-2w65J5 {								/* features				feature								*/
	background-color: rgba(var(--vtransparencycolor), 0.4);
}
.featureImage-2L9kA0 {										/* features				image								*/
	opacity: 0.7;
}
.banner-WELp4M {											/* features				xbox promo							*/
	background-color: rgba(var(--vtransparencycolor), 0.4);
}


/* ~~~~		9.		LIBRARY							~~~~ */

.header-39GIC8 {											/* library				table header						*/
	background-color: transparent;
	border-bottom-color: rgba(var(--fontwhite4), 0.5);
	color: rgb(var(--fontwhite3));
	position: relative;
}
.header-39GIC8::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--vbackground) var(--vbackgroundposition)/var(--vbackgroundsize);
	background-attachment: fixed;
	filter: blur(var(--vbackgroundblur));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.header-39GIC8::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--vtransparencycolor), 0.4);
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.headerCell-3L6rFG {										/* library				table headercell					*/
	border-left-color: rgba(var(--fontwhite4), 0.3);
}
.clickable-VxMZ3b {
	color: rgb(var(--fontwhite2));
}
.clickable-VxMZ3b:hover {
	color: rgb(var(--fontwhite1));
}
.lastPlayedCell-2arbtc,
.platformCell-XyBBs6 {
	color: rgb(var(--fontwhite3));
}
.headerCellSorted-3a5AzJ,
.headerCellSorted-3a5AzJ:hover {
	color: rgb(var(--fontwhite1));
}
.row-ZLfFhY {												/* library				table row							*/
	color: rgb(var(--fontwhite3));
}
.rowWrapperActive-2L7i9f {
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
.rowWrapper-2fB6P0 + .rowWrapper-2fB6P0 .row-ZLfFhY {
	border-top-color: rgba(var(--fontwhite4), 0.3);
}
.nameCellText-1mpqtF {										/* library				table namecell						*/
	color: rgb(var(--fontwhite2));
}
.row-ZLfFhY:hover .nameCellText-1mpqtF {
	color: rgb(var(--fontwhite1));
}
.textCell-1aBIUP {											/* library				table textcell						*/
	color: rgb(var(--fontwhite4));
}
.row-ZLfFhY:hover .textCell-1aBIUP {
	color: rgb(var(--fontwhite3));
}
.icon-1IKq3C {												/* library				table icon							*/
	color: rgb(var(--fontwhite4));
}
.row-ZLfFhY:hover .icon-1IKq3C {
	color: rgb(var(--fontwhite3));
}
.emptyWumpus-12J3jI {										/* library				no games							*/
	opacity: 0.6;
}


/* ~~~~		10.		DISCOVERY						~~~~ */

.categoryItem-3zFJns {										/* categoryitem			container						*/
	color: rgb(var(--fontwhite3));
}
.clickable-1JJAn8.categoryItem-3zFJns:hover {
	color: rgb(var(--fontwhite2));
}
.clickable-1JJAn8.categoryItem-3zFJns:active,
.selected-aXhQR6.categoryItem-3zFJns {
	color: rgb(var(--fontwhite1));
}
.categoryItem-3zFJns:hover .layout-2DM8Md {					/* categoryitem			inner							*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
.selected-aXhQR6.categoryItem-3zFJns .layout-2DM8Md {
	background-color: rgb(var(--vaccentcolor));
	text-shadow: 1px 1px var(--vtextshadow);
}
.selected-aXhQR6.categoryItem-3zFJns .layout-2DM8Md svg:not(.svg-2V3M55) {
	filter: drop-shadow(1px 1px var(--vtextshadow));
}
.categoryItem-3zFJns .name-uJV0GL {
	color: rgb(var(--fontwhite2));
}
.categoryItem-3zFJns:hover .name-uJV0GL,
.categoryItem-3zFJns.selected-aXhQR6 .name-uJV0GL {
	color: rgb(var(--fontwhite1));
}

#app-mount .pageWrapper-1PgVDX {							/* guilddiscovery		container							*/
	color: rgb(var(--fontwhite1));
}
.select-2TCrqx.languageSelector-1R8fPE [class*="css-"][class*="-control"] {
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
.container-RHl2Ju {											/* guilddiscovery		news container						*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
#app-mount .sectionSeparator-2OWiNT {						/* guilddiscovery		separator							*/
	border-top-color: rgba(var(--fontwhite4), 0.3);
}
															/* guilddiscovery		pagebutton							*/
#app-mount .pageButton-MknE-_:not(.activeButton-1BJAiN):hover {
	background-color: rgba(var(--vtransparencycolor), 0.3);
	color: rgb(var(--fontwhite1));
}
#app-mount .activeButton-1BJAiN,
#app-mount .activeButton-1BJAiN:hover {						/* guilddiscovery		pagebuttonactive					*/
	color: rgb(var(--fontwhite1));
}

#app-mount .card-3DjzTQ {									/* guildcard			container							*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
#app-mount .iconMask-3b8GzQ {								/* guildcard			iconmask							*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
#app-mount .card-3DjzTQ:hover,
#app-mount .iconMask-3b8GzQ:hover {
	background-color: rgba(var(--vtransparencycolor), 0.4);
}
#app-mount .cardPlaceholder-1zrbbe {						/* guildcard			placeholder							*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
#app-mount .loading-17PYl_ {								/* guildcard			loading								*/
	background-color: rgba(var(--vtransparencycolor), 0.5);
}
#app-mount .guildName-1yURO5 {								/* guildcard			guildname							*/
	color: rgb(var(--fontwhite1));
}
#app-mount .description-2QALGo {							/* guildcard			description							*/
	color: rgb(var(--fontwhite3));
}

.search-1iTphC .searchBox-2_mAlO .searchBoxInput-K6mkng {	/* search				searchinput							*/
	color: rgb(var(--fontwhite1));
}
.search-1iTphC .searchBox-2_mAlO .cta-BiH9zX {				/* search				searchtip							*/
	color: rgb(var(--fontwhite3));
}
.categoryPill-34fszg .categoryLabel-2G3r2V {				/* search				categorypill						*/
	color: rgb(var(--fontwhite3));
}
.emojiContainer-1u-_sQ {									/* search				emojicontainer						*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
.emptyContainer-1_gwCl {									/* search				no results							*/
	background-color: rgba(var(--vtransparencycolor), 0.4);
}


/* ~~~~		11.		USERSETTINGS					~~~~ */

.themed-OHr7kt.item-PXvHYJ {								/* sidebar				item								*/
	color: rgb(var(--fontwhite3));
}
.item-PXvHYJ[style^="color: rgb(255, 255, 255)"],
.item-PXvHYJ[style*=" color: rgb(255, 255, 255)"] {
	color: rgb(var(--fontwhite1)) !important;
}
.item-PXvHYJ[style*="background-color: rgb(114, 137, 218)"] {
	text-shadow: 1px 1px var(--vtextshadow);
}
.themed-OHr7kt.item-PXvHYJ:hover {
	color: rgb(var(--fontwhite2));
}
.side-8zPYf6 .themed-OHr7kt.item-PXvHYJ:hover,				/* sidebar				sideitem							*/
.topPill-30KHOu .themed-OHr7kt.item-PXvHYJ:hover {			/* sidebar				tabitems							*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
.side-8zPYf6 .themed-OHr7kt.selected-3s45Ha.item-PXvHYJ,
.topPill-30KHOu .themed-OHr7kt.selected-3s45Ha.item-PXvHYJ {
	background-color: rgb(var(--vaccentcolor));
	color: rgb(var(--fontwhite1));
	text-shadow: 1px 1px var(--vtextshadow);
}

.header-2RyJ0Y {											/* sidebar				sideitemheader						*/
	color: rgb(var(--fontwhite3));
}
.separator-gCa7yv {											/* sidebar				sideitemseparator					*/
	background-color: rgba(var(--fontwhite4), 0.3);
}
#app-mount .foreground-26ym5y {								/* sidebar				sideitemlink						*/
	fill: rgb(var(--fontwhite3));
}
#app-mount .link-1IoFq-:hover .foreground-26ym5y {
	fill: rgb(var(--fontwhite1));
}

#app-mount .closeButton-1tv5uR {							/* closebutton			item								*/
	border-color: rgb(var(--fontwhite4));
}
#app-mount .closeButton-1tv5uR path.fill {
	fill: rgb(var(--fontwhite4));
}
#app-mount .closeButton-1tv5uR:hover {
	background-color: rgba(var(--vaccentcolor), 0.2);
	border-color: rgb(var(--vaccentcolor));
}
#app-mount .closeButton-1tv5uR:hover path.fill {
	fill: rgb(var(--vaccentcolor));
}
#app-mount .keybind-KpFkfr {								/* closebutton			keybind								*/
	color: rgb(var(--fontwhite4));
}

.cardPrimary-1Hv-to, .cardPrimaryEditable-3KtE4g {			/* settingsitems		card								*/
	border-color: rgba(var(--vtransparencycolor), 0.1);
}
.cardPrimary-1Hv-to {
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
.cardPrimaryEditable-3KtE4g {
	background-color: rgba(var(--vtransparencycolor), 0.1);
}
.cardPrimaryOutline-29Ujqw {
	border-color: rgba(var(--vtransparencycolor), 0.2);
}
#app-mount .card-2qG0dv {
	color: rgb(var(--fontwhite1));
}

.title-31JmR4 {												/* settingsitems		settingstitle						*/
	color: rgb(var(--fontwhite1));
}
.divider-3573oO {											/* settingsitems		settingstitle						*/
	border-color: rgba(var(--fontwhite1), 0.1);
}

#app-mount .userSettingsAccount-2eMFVR .viewBody-2Qz-jg {	/* accountsettings		info								*/
	color: rgb(var(--fontwhite3));
}
.questionMark-CWEQZn .icon-3a_Jgd,							/* accountsettings		questionmark						*/
.questionMark-3qBhGj .icon-3OA7an {							/* accountsettings		questionmark new					*/
	color: rgb(var(--fontwhite1));
}
#app-mount .avatarUploader-3XDtmn .removeButton-1hcZyG	{	/* accountsettings		removeavatar						*/
	color: rgb(var(--fontwhite3));
}
#app-mount .userSettingsSecurity-3IYeMF .codeCheckbox-1T0TTy {
	color: rgb(var(--fontwhite2));
}
#app-mount .background-1QDuV2 {								/* accountsettings		container							*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
#app-mount .fieldList-21DyL8 {								/* accountsettings		settings							*/
	background-color: rgba(var(--vtransparencycolor), 0.4);
}

.accountList-33MS45 {										/* connections			container							*/
	background-color: rgba(var(--vtransparencycolor), 0.4);
}
.accountBtn-2Nozo3 .accountBtnInner-sj5jLs {				/* connections			connectioninner						*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
.accountBtn-2Nozo3 .accountBtnInner-sj5jLs:hover {
	background-color: rgb(var(--vaccentcolor));
}
.connection-1fbD7X {										/* connections			connection							*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
.connectionHeader-2MDqhu {									/* connections			connection header					*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
.connectionHeader-2MDqhu .connectionAccountValue-3VdBGs {
	color: rgb(var(--fontwhite1));
}
.connectionHeader-2MDqhu .description-3_Ncsb {
	color: rgb(var(--fontwhite2)) !important;
	opacity: 1;
}
.subEnabledTitle-2ElRo_ {
	color: rgb(var(--fontwhite1));
}

#app-mount .codeRedemptionRedirect-1wVR4b {					/* payment				coderedem							*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
	border-color: rgba(var(--vtransparencycolor), 0.1);
	color: rgb(var(--fontwhite1));
}

.emptyStateImage-2MrSNs {									/* giftinventory		no gifts							*/
	opacity: 0.6;
}

.guildHeader-3nh5RK {										/* boostsettings		suggestioncard						*/
	background-color: rgba(var(--vtransparencycolor), 0.5);
}
.guildSubscriptionSlots-JPXXvN {							/* boostsettings		suggestioncard						*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
.cardWrapper-2Min21 {										/* boostsettings		suggestioncard						*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
.cardWrapper-2Min21:hover {
	background-color: rgba(var(--vtransparencycolor), 0.4);
}
.cardWrapper-2Min21 .card-3AyPWq,							/* boostsettings		suggestioncard inner				*/
.cardWrapper-2Min21 .card-3AyPWq:hover {
	background-color: transparent;
}
#app-mount .gemIndicatorContainer-2jdECl {					/* boostsettings		suggestioncard circle				*/
	background-color: transparent;
}
#app-mount .paymentPane-3bwJ6A {							/* boostsettings		past transations					*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
	color: rgb(var(--fontwhite1));
}
#app-mount .summaryInfo-2QFKUg {							/* boostsettings		past transations summary			*/
	color: rgb(var(--fontwhite1));
}
#app-mount .paymentHeader-3QlZQi {							/* boostsettings		past transations header				*/
	border-color: rgba(var(--fontwhite3), 0.5);
	color: rgb(var(--fontwhite3));
}
#app-mount .payment-xT17Mq {								/* boostsettings		past transations payment			*/
	background-color: transparent;
	color: rgb(var(--fontwhite2));
}
#app-mount .hoverablePayment-Yc6mK7:hover {
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
#app-mount .paymentText-2vaF7U {							/* boostsettings		past transations paymenttext		*/
	color: rgb(var(--fontwhite3));
}
#app-mount .expandedInfo-3kfShd {							/* boostsettings		past transations expandedinfo		*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
#app-mount .giftIcon-3DRGI6 {								/* boostsettings		past transations gifticon			*/
	color: rgb(var(--fontwhite1));
}
#app-mount .paginator-166-09 {								/* boostsettings		past transations paginator			*/
	background: rgba(var(--vtransparencycolor), 0.3);
}
#app-mount .bottomDivider-1K9Gao {							/* boostsettings		past transations divider			*/
	border-bottom-color: rgba(var(--fontwhite3), 0.5);
}
#app-mount .tab-1kx2RU {									/* boostsettings		past transations tab				*/
	color: rgb(var(--fontwhite3));
}
#app-mount .appleRowHeader-241O5v {							/* boostsettings		past transations applerowheader		*/
	color: rgb(var(--fontwhite2));
}
#app-mount .appleRowBody-2B5tp2 {							/* boostsettings		past transations applerowbody		*/
	color: rgb(var(--fontwhite3));
}

.introHeader-4MPach {										/* hypesquad			header								*/
	color: rgb(var(--fontwhite1));
}
.introBlurb-3gFgTQ {										/* hypesquad			description							*/
	color: rgb(var(--fontwhite2));
}
.title-PMZpEi {												/* hypesquad			perktitle							*/
	color: rgb(var(--fontwhite1));
}
.description-1W0DiL {										/* hypesquad			description							*/
	color: rgb(var(--fontwhite2));
}
.attendeeCTA-3ZZQWt {										/* hypesquad			attendeeCTA							*/
	color: rgb(var(--fontwhite2));
}
.membershipDialogHouse1-3KhKE- {							/* hypesquad			membershipdialogs					*/
	background-color: rgba(156, 132, 239, 0.8);
}
.membershipDialogHouse2-35h9SY {
	background-color: rgba(244, 123, 103, 0.8);
}
.membershipDialogHouse3-15OBIQ {
	background-color: rgba(69, 221, 192, 0.8);
}

.container-3PXSwK {											/* voicesettings		voicebarcontainer					*/
	-webkit-mask: url('data:image/svg+xml;base64,PHN2ZyB4bWxuczp4bGluaz0iaHR0cDovL3d3dy53My5vcmcvMTk5OS94bGluayIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIiB3aWR0aD0iOCIgaGVpZ2h0PSIyMCIgZmlsbD0iIzM2MzkzZiI+PHBhdGggZmlsbC1ydWxlPSJldmVub2RkIiBkPSJNNCAyYTIgMiAwIDAgMC0yIDJ2MTJhMiAyIDAgMSAwIDQgMFY0YTIgMiAwIDAgMC0yLTJ6Ii8+PC9zdmc+');
}
.notches-1sAcEM {
	background: transparent !important;
}
#app-mount .progress-1IcQ3A {								/* voicesettings		voicebar							*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
.userSettingsVoice-iwdUCU .media-engine-video {				/* voicesettings		video								*/
	background: transparent;
}
#app-mount .userSettingsVoice-iwdUCU .previewOverlay-2O7_KC {
	background-color: rgba(var(--vtransparencycolor), 0.2);
	border-color: rgba(var(--vtransparencycolor), 0.1);
}

.option-n0icdO {											/* overlay				option								*/
	background-color: rgba(var(--vtransparencycolor), 0.4);
}
.option-n0icdO:hover,
.option-n0icdO.selected-mKYnfr {
	box-shadow: 0 2px 0 rgba(var(--vtransparencycolor), 0.3);
}
.disabled-3I9jyo {
	color: rgba(var(--vtransparencycolor), 0.4);
}

.notificationsSound-27jFSh {								/* notifications		row									*/
	color: rgb(var(--fontwhite2));
	box-shadow: inset 0 -1px 0 0 rgba(var(--fontwhite4), 0.2);
}

#app-mount .row-2okwlC {									/* hotkeys				row									*/
	color: rgb(var(--fontwhite2));
	box-shadow: inset 0 -1px 0 rgba(var(--fontwhite4), 0.3);
}

#app-mount .card-FDVird::before {							/* settingscard			backdrop							*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
	border-color: rgba(var(--vtransparencycolor), 0.1);
}
#app-mount .button-2CgfFz {									/* settingscard			removebutton						*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
	box-shadow: 0 0 0 1px rgba(var(--vtransparencycolor), 0.6), 0 1px 5px 0 rgba(var(--vtransparencycolor), 0.3);
}
#app-mount .button-2CgfFz:hover {
	background-color: rgba(var(--vtransparencycolor), 0.7);
}

#app-mount .game-1ipmAa {									/* games				card								*/
	box-shadow: 0 1px 0 0 rgba(var(--fontwhite4), 0.3);
}
#app-mount .notDetected-33MY4s {							/* games				nogame								*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
#app-mount .nowPlayingAdd-1Kdmh_ {							/* games				descriptionhint						*/
	color: rgb(var(--fontwhite3));
}
#app-mount .gameName-1RiWHm {								/* games				gamename							*/
	color: rgb(var(--fontwhite1));
}
#app-mount .lastPlayed-3bQ7Bo,								/* games				lastplayed							*/
#app-mount .overlayStatusText-L2IACa {						/* games				overlaystatustext					*/
	color: rgb(var(--fontwhite3));
}
#app-mount .overlayToggleIconOn-3UNmty .fill-1ugeBG {		/* games				overlaystatusicon					*/
	fill: rgb(var(--fontwhite3));
}
#app-mount .nowPlaying-284llR .lastPlayed-3bQ7Bo,
#app-mount .nowPlaying-284llR .overlayStatusText-L2IACa {
	color: rgb(var(--fontwhite2));
}
#app-mount .nowPlaying-284llR .overlayToggleIconOff-1kT42w .fill-1ugeBG,
#app-mount .nowPlaying-284llR .overlayToggleIconOn-3UNmty .fill-1ugeBG {
	fill: rgb(var(--fontwhite2));
}
#app-mount .gameNameInput-385LoS:focus,
#app-mount .gameNameInput-385LoS:hover {
	background-color: rgba(var(--vtransparencycolor), 0.3);
	border-color: rgba(var(--vtransparencycolor), 0.1);
}
#app-mount .text-GwUZgS,
#app-mount .title-2BxgL2 {
	color: rgb(var(--fontwhite4));
}

#app-mount .installationPath-24giJj {						/* gamelibrary			path								*/
	box-shadow: 0 1px 0 0 rgba(var(--fontwhite4), 0.3);
}
#app-mount .usageInfo-2WQAwr {								/* gamelibrary			usageinfo							*/
	color: rgb(var(--fontwhite2));
}
#app-mount .background-yZEZik {								/* gamelibrary			usagebar							*/
	stroke: rgb(var(--vtransparencycolor), 0.5);
}
#app-mount .rowTitle-3xCiqy {								/* gamelibrary			rowtitle							*/
	color: rgb(var(--fontwhite3));
}
#app-mount .defaultIndicator-2X8Auf {						/* gamelibrary			rowtag								*/
	background-color: rgba(var(--vtransparencycolor), 0.5);
	color: rgb(var(--fontwhite1));
}
#app-mount .rowBody-10yI-R {								/* gamelibrary			rowdescription						*/
	color: rgb(var(--fontwhite3));
}

.preview-2nSL_2 {											/* appearance			preview								*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
	border-color: rgba(var(--vtransparencycolor), 0.2);
}

#app-mount .item-3eFBNF {									/* languagesettings		row									*/
	border-radius: 5px;
	box-shadow: 0 1px 0 0 rgba(var(--fontwhite4), 0.3);
}
.item-3eFBNF:hover {
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
.item-3eFBNF.selected-2DeaDa {
	background-color: rgba(var(--vtransparencycolor), 0.4);
}

#app-mount .experimentDate-2ymg99 {							/* experiments			date								*/
	color: rgb(var(--fontwhite3));
}


/* ~~~~		12.		GUILDSETTINGS					~~~~ */

.container-2VW0UT {											/* settings				confirmnotice						*/
	position: relative;
}
.container-2VW0UT[style*="background-color: rgba(248, 249, 249"],
.container-2VW0UT[style*="background-color: rgba(32, 34, 37"] {
	background-color: rgba(var(--vtransparencycolor), 0.7) !important;
}
.container-2VW0UT::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--vbackground) var(--vbackgroundposition)/var(--vbackgroundsize);
	background-attachment: fixed;
	filter: blur(var(--vbackgroundblur));
	pointer-events: none;
	z-index: -1;
}

#app-mount .emojiAliasInput-1y-NBz .emojiInput-1aLNse {		/* emojisettings		nameinput							*/
	background-color: rgba(var(--vtransparencycolor), 0.1);
}

#app-mount .selectableItem-1MP3MQ {							/* auditlogs			popoutitem							*/
	color: rgb(var(--fontwhite2));
}
#app-mount .selectableItem-1MP3MQ:hover {
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
#app-mount .selectableItem-1MP3MQ[style*=" color: rgb(255, 255, 255)"] {
	color: rgb(var(--fontwhite1)) !important;
}
#app-mount .selectableItem-1MP3MQ polyline[stroke="#ffffff"] {
	stroke: rgb(var(--fontwhite1));
}

#app-mount .auditLog-3jNbM6 {								/* auditlogs			logitem								*/
	border-color: rgba(var(--vtransparencycolor), 0.1);
	color: rgb(var(--fontwhite4));
}
#app-mount .headerClickable-2IVFo9,							/* auditlogs			loginner							*/
#app-mount .headerDefault-1wrJcN {
	background-color: rgba(var(--vtransparencycolor), 0.2);
	color: rgb(var(--fontwhite3));
}
#app-mount .headerExpanded-CUEwZ5 {
	background-color: rgba(var(--vtransparencycolor), 0.3);
	color: rgb(var(--fontwhite2));
}
#app-mount .divider-1pnAR2 {								/* auditlogs			loginnerdivider						*/
	background-color: rgba(var(--fontwhite4), 0.3);
}
#app-mount .changeDetails-bk98pu {							/* auditlogs			logdetails							*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
#app-mount .userHook-3AdCBF {								/* auditlogs			userhook							*/
	color: rgb(var(--fontwhite1));
}
#app-mount .auditLog-3jNbM6 strong {						/* auditlogs			targets								*/
	color: rgb(var(--fontwhite1));
}
#app-mount .timestamp-1mruiI {								/* auditlogs			timestamp							*/
	color: rgb(var(--fontwhite4));
}
#app-mount .expandForeground-1nZ4VR {						/* auditlogs			expandarrow							*/
	stroke: rgb(var(--fontwhite2));
}
.themeOverrideLight-3bx_5B.icon-RTGJu3,						/* auditlogs			logicon								*/
.themeOverrideDark-1u5Vo0.icon-RTGJu3,
#app-mount .icon-RTGJu3 {
	background: none !important;
}
.icon-RTGJu3::before {
	content: "";
	position: absolute;
	top: 0;
	left: 0;
	right: 0;
	bottom: 0;
	background: rgb(var(--fontwhite1));
}
.icon-RTGJu3.targetAll-13V3n6::before {
	-webkit-mask: url(https://discordapp.com/assets/fc3f5f9be1a4db14b02336b7cb02e6ce.svg);
}
.icon-RTGJu3.targetBan-3mbIPL::before {
	-webkit-mask: url(https://discordapp.com/assets/edb23a53ea40ac60f212ebae66e5c5c7.svg);
}
.icon-RTGJu3.targetChannel-TrRFlx::before {
	-webkit-mask: url(https://discordapp.com/assets/343c9ff4c775c66a7d4af1f8691c34e0.svg);
}
.icon-RTGJu3.targetGuild-mDWfAV::before {
	-webkit-mask: url(https://discordapp.com/assets/30af96a386520760ad107c5b77ba002a.svg);
}
.icon-RTGJu3.targetEmoji-3vhPhM::before {
	-webkit-mask: url(https://discordapp.com/assets/7a9bf92329dad473ef0383ae75367215.svg);
}
.icon-RTGJu3.targetInvite-1RQBlr::before {
	-webkit-mask: url(https://discordapp.com/assets/4b33371531a1a89f99296a73fc9ef588.svg);
}
.icon-RTGJu3.targetMemberRole-jowY3I::before {
	-webkit-mask: url(https://discordapp.com/assets/a9098042cb36b955c5021259f1d48f91.svg);
}
.icon-RTGJu3.targetMember-2iuwxX::before {
	-webkit-mask: url(https://discordapp.com/assets/af043346e036ef7b1aac1cf42cd1e699.svg);
}
.icon-RTGJu3.targetPermission-ZRUN5n::before {
	-webkit-mask: url(https://discordapp.com/assets/2a37995eb832bae805190a93ba043857.svg);
}
.icon-RTGJu3.targetRole-2MoUny::before {
	-webkit-mask: url(https://discordapp.com/assets/0176a91b4c44ed05c05af68784e78da8.svg);
}
.icon-RTGJu3.targetVanityUrl-3OpsYX::before {
	-webkit-mask: url(https://discordapp.com/assets/84215a5fec3d9de9960a225143238d74.svg);
}
.icon-RTGJu3.targetWebhook-1xS7Z7::before {
	-webkit-mask: url(https://discordapp.com/assets/a6975850d800aa86162b4aa5f18c41ac.svg);
}
.icon-RTGJu3.targetWidget-3hFVSM::before {
	-webkit-mask: url(https://discordapp.com/assets/4ac0e382cc7b8aa0cb1d6d074b0e8ba5.svg);
}
.icon-RTGJu3.targetMessage-2kBYMT::before {
	-webkit-mask: url(https://discordapp.com/assets/8c85e30795486caa8caacd829703459d.svg);
}
.icon-RTGJu3.targetIntegration-3rnyMN::before {
	-webkit-mask: url(https://discordapp.com/assets/da8463a04b4a289801d2516f50eb4c19.svg);
}

#app-mount .card-o7rAq- {									/* integrationsettings	card								*/
	border-color: rgba(var(--vtransparencycolor), 0.1)
}
#app-mount .card-3IImnr {									/* integrationsettings	webhook card						*/
	border-color: rgba(var(--vtransparencycolor), 0.1)
}
#app-mount .card-1o0mns {									/* integrationsettings	apps card							*/
	border-color: rgba(var(--vtransparencycolor), 0.1)
}
.iconWrapper-lS1uig {										/* integrationsettings	icon								*/
	background-color: rgba(var(--vtransparencycolor), 0.4);
}

.guildDetails-2p1NmK {										/* communitysettings	intro		details					*/
	background-color: rgba(var(--vtransparencycolor), 0.4);
}
.featureCard-1RR4Tl {										/* communitysettings	intro		featurecard				*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
.featureIcon-3p1TC_ {										/* communitysettings	intro		featureicon				*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
.checklistContainer-mFJZEJ {								/* communitysettings	intro		checklist				*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
.checklistHeader-1KWcEY {									/* communitysettings	intro		checklist header		*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}

.upsellContainer-L9xv7w {									/* communitysettings	general		upsellcontainer			*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
.upsellFooter-ZYsio_ {										/* communitysettings	general		upsellfooter			*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}

.developerPortalCtaWrapper-2XNafh {							/* communitysettings	analytics	info					*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
.analyticsCard-qckucw {										/* communitysettings	analytics	card					*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}

#app-mount .card-3_CqkU {									/* communitysettings	discovery	card					*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
#app-mount .iconMask-30Tvqs {								/* communitysettings	discovery	icon					*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
.perkArt-1SGWbA {											/* communitysettings	discovery	perk					*/
	background-color: rgba(var(--vtransparencycolor), 0.4);
}
.container-2w0lh0 {											/* communitysettings	discovery	checklist				*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
.header-2Y0-A- {											/* communitysettings	discovery	checklist header		*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}

.exampleContainer-25sB-A {									/* communitysettings	welcome		examplecontainer		*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
#app-mount .exampleModal-2X2Vf8 {							/* communitysettings	welcome		examplemodal			*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--vtransparencycolor), 0.3), 0 2px 10px 0 rgba(var(--vtransparencycolor), 0.3);
	position: relative;
	border-radius: 5px;
}
.exampleModal-2X2Vf8 > * {
	z-index: 1;
}
.exampleModal-2X2Vf8::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--vpopout) var(--vpopoutposition)/var(--vpopoutsize);
	background-attachment: fixed;
	filter: blur(var(--vpopoutblur));
	width: unset;
	height: unset;
	border-radius: 5px;
	pointer-events: none;
}
.exampleModal-2X2Vf8::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.2));
	width: unset;
	height: unset;
	border-radius: 5px;
	pointer-events: none;
}
.optionContainer-1FtykV {									/* communitysettings	welcome		exampleoption			*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
.enableContainer-6E-puu {									/* communitysettings	welcome		previewheader			*/
	background-color: rgba(var(--vtransparencycolor), 0.4);
}
.previewContainer-1SS3uO {									/* communitysettings	welcome		previewcontainer		*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
.welcomeChannel-1rFrIO {									/* communitysettings	welcome		welcomechannel			*/
	background-color: rgba(var(--vtransparencycolor), 0.4);
}

.addRoleIcon-3YjErH {										/* rolesettings			addrolebutton						*/
	-webkit-mask: url(https://discordapp.com/assets/cef02719c12d8aaf38894c16dca7fbe6.svg);
	background: rgb(var(--fontwhite3));
	object-position: -9999999px -9999999px;
}
#app-mount .colorPickerSwatch-5GX3Ve.noColor-1pdBDm {		/* rolesettings			colorswatchnocolor					*/
	border-color: rgba(var(--fontwhite1), 0.3);
}
#app-mount .colorPickerSwatch-5GX3Ve.noColor-1pdBDm .colorPickerDropperFg-3jYKWI {
	fill: rgb(var(--fontwhite1));
}
#app-mount .colorPickerSwatch-5GX3Ve.noColor-1pdBDm polyline {
	stroke: rgb(var(--fontwhite1));
}

.descriptionBox-1EKQKL {									/* templatesettings		descriptionbox						*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}

#app-mount .tierHeaderLocked-1a2opw {						/* boostsettings		tierheaderlocked					*/
	background-color: rgba(var(--vtransparencycolor), 0.4);
	color: rgb(var(--fontwhite3));
}
#app-mount .tierLock-1oFMOZ {								/* boostsettings		tierlock							*/
	color: rgb(var(--fontwhite4));
}
#app-mount .tierHeaderUnlocked-2RhWqn {						/* boostsettings		tierheaderunlocked					*/
	background-color: rgba(var(--vtransparencycolor), 0.5);
	color: rgb(var(--fontwhite1));
}
#app-mount .tierUnlocked-27DwHo {							/* boostsettings		tierunlocked						*/
	background-color: rgb(var(--fontwhite1));
}
#app-mount .tierBody-x9kBBp {								/* boostsettings		tierbody							*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
	color: rgb(var(--fontwhite3));
}
#app-mount .tierInProgress-3mBoXq {							/* boostsettings		tiermilestone						*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
#app-mount .background-3xPPFc {								/* boostsettings		tierbar	(settings)					*/
	color: rgba(var(--vtransparencycolor), 0.3);
}

#app-mount .member-1q7VfX {									/* membersettings		membercard							*/
	box-shadow: 0 1px 0 0 rgba(var(--fontwhite4), 0.3);
}
#app-mount .member-1q7VfX .name-8yzEIY {					/* membersettings		membercardname						*/
	color: rgb(var(--fontwhite1));
}
#app-mount .member-1q7VfX .tag-1YGWN9 {						/* membersettings		membercardtag						*/
	color: rgb(var(--fontwhite4));
}
#app-mount .actionButton-VzECiy {							/* membersettings		addrolebutton						*/
	border-color: rgb(var(--fontwhite4));
	color: rgb(var(--fontwhite3));
}
#app-mount .member-1q7VfX .overflowIconFg-QMRRFI {			/* membersettings		3-doticon							*/
	fill: rgb(var(--fontwhite1));
}

#app-mount .overflowRolesPopout-140n9i,						/* membersettings		roleoverflow popout					*/
#app-mount .overflowRolesPopoutArrow-2O66oH {
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--vtransparencycolor), 0.2), 0 2px 10px 0 rgba(var(--vtransparencycolor), 0.2);
	border: none;
	border-radius: 3px;
	overflow: hidden;
}
.overflowRolesPopout-140n9i::before,
.overflowRolesPopoutArrow-2O66oH::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--vpopout) var(--vpopoutposition)/var(--vpopoutsize);
	background-attachment: fixed;
	filter: blur(var(--vpopoutblur));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.overflowRolesPopout-140n9i::after,
.overflowRolesPopoutArrow-2O66oH::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.1));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.overflowRolesPopoutHeaderIcon-6PNEZA path {
	fill: rgb(var(--fontwhite2));
}
.overflowRolesPopoutHeaderText-1SW-y3 {
	color: rgb(var(--fontwhite2));
}

#app-mount .inviteSettingsInviteRow-3p2O-N {				/* invitesettings		invitecard							*/
	box-shadow: 0 1px 0 0 rgba(var(--fontwhite4), 0.3);
	color: rgb(var(--fontwhite2));
}
.user-3x-NP9 {												/* invitesettings		user								*/
	color: rgb(var(--fontwhite1));
}
.channelName-13-Sm9 {										/* invitesettings		channelname							*/
	color: rgb(var(--fontwhite3));
}

#app-mount .bannedUser-1IalTM {								/* bansettings			bancard								*/
	box-shadow: 0 1px 0 0 rgba(var(--fontwhite4), 0.3);
}
#app-mount .bannedUser-1IalTM .username-1b3MVI {			/* invitesettings		username							*/
	color: rgb(var(--fontwhite1));
}
#app-mount .bannedUserModal-3RJCOV .reasonHeader-2etdjy {	/* invitesettings		banmodalreasonheader				*/
	color: rgb(var(--fontwhite2));
}
#app-mount .bannedUser-1IalTM .username-1b3MVI .discrim-oGb-FO,
#app-mount .bannedUserModal-3RJCOV .reason-YbfGC6,			/* invitesettings		banmodalreason						*/
#app-mount .bannedUserModal-3RJCOV .userDiscrim-1D2NlF {	/* invitesettings		discriminator						*/
	color: rgb(var(--fontwhite3));
}


/* ~~~~		13.		MODALS							~~~~ */

.layer-2KE1M9:nth-child(1),
.backdropWithLayer-3_uhz4:nth-child(1) {
	z-index: 1002;
}
.layer-2KE1M9:nth-child(2),
.backdropWithLayer-3_uhz4:nth-child(2) {
	z-index: 1003;
}
.layer-2KE1M9:nth-child(3),
.backdropWithLayer-3_uhz4:nth-child(3) {
	z-index: 1004;
}
.layer-2KE1M9:nth-child(4),
.backdropWithLayer-3_uhz4:nth-child(4) {
	z-index: 1005;
}
.layer-2KE1M9:nth-child(5),
.backdropWithLayer-3_uhz4:nth-child(5) {
	z-index: 1006;
}
.layer-2KE1M9:nth-child(6),
.backdropWithLayer-3_uhz4:nth-child(6) {
	z-index: 1007;
}
.layer-2KE1M9:nth-child(7),
.backdropWithLayer-3_uhz4:nth-child(7) {
	z-index: 1008;
}
.layer-2KE1M9:nth-child(8),
.backdropWithLayer-3_uhz4:nth-child(8) {
	z-index: 1009;
}
.layer-2KE1M9:nth-child(9),
.backdropWithLayer-3_uhz4:nth-child(9) {
	z-index: 1010;
}

#app-mount .root-1gCeng,									/* modal				container (foldersettings)			*/
#app-mount .modal-yWgWj- {									/* modal				container							*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--vtransparencycolor), 0.3), 0 2px 10px 0 rgba(var(--vtransparencycolor), 0.3);
	position: relative;
	border-radius: 5px;
}
.root-1gCeng > *,
.modal-yWgWj- > * {
	z-index: 1;
}
.root-1gCeng::before,
.modal-yWgWj-::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--vpopout) var(--vpopoutposition)/var(--vpopoutsize);
	background-attachment: fixed;
	filter: blur(var(--vpopoutblur));
	width: unset;
	height: unset;
	border-radius: 5px;
	pointer-events: none;
	z-index: -1;
}
.root-1gCeng::after,
.modal-yWgWj-::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.2));
	width: unset;
	height: unset;
	border-radius: 5px;
	pointer-events: none;
	z-index: -1;
}
.root-1gCeng .modal-yWgWj-::before,
.modal-qgFCbT::before,
.root-1gCeng .modal-yWgWj-::after,
.modal-qgFCbT::after {
	display: none;
}
#app-mount .footer-2gL1pp {									/* modal				footer							*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
	box-shadow: none;
}
#app-mount .footer-1lnhms {									/* modal				footer info						*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
#app-mount .closeButton-1tv5uR,								/* modal				closebutton						*/
#app-mount .close-hZ94c6 {
	color: rgb(var(--fontwhite1));
}

#app-mount .guildName-3WI6ml,								/* modal				guildname						*/
#app-mount .date-2WJGyu,
#app-mount .override-2YgiXd,
#app-mount .overrideHighlight-YPcBxt {
	color: rgb(var(--fontwhite3));
}
#app-mount .channelName-28iMRJ {							/* modal				channelname						*/
	color: rgb(var(--fontwhite1));
}

.tabBarContainer-1s1u-z {									/* modal				tabbarcontainer					*/
	border-top-color: rgba(var(--vtransparencycolor), 0.3);
}
#app-mount .modal-6GHvdM .tabBarContainer-1s1u-z {
	background: rgba(var(--vtransparencycolor), 0.2);
	box-shadow: 0 2px 3px 0 rgba(var(--vtransparencycolor), 0.1);
}
.top-28JiJ- .themed-OHr7kt.item-PXvHYJ,						/* modal				tabbaritem						*/
.top-28JiJ- .item-PXvHYJ[style*="rgba(79, 84, 92, 0.4)"],
.top-28JiJ- .item-PXvHYJ[style*="rgba(255, 255, 255, 0.4)"],
.themed-OHr7kt.tabBarItem-1b8RUP,
.tabBarItem-1b8RUP[style*="rgba(79, 84, 92, 0.4)"],
.tabBarItem-1b8RUP[style*="rgba(255, 255, 255, 0.4)"] {
	color: rgba(var(--fontwhite1), 0.4) !important;
}
.top-28JiJ- .themed-OHr7kt.item-PXvHYJ:hover,				/* modal				tabbaritem hover				*/
.top-28JiJ- .item-PXvHYJ[style*="rgba(79, 84, 92, 0.6)"],
.top-28JiJ- .item-PXvHYJ[style*="rgba(255, 255, 255, 0.6)"],
.themed-OHr7kt.tabBarItem-1b8RUP:hover,
.tabBarItem-1b8RUP[style*="rgba(79, 84, 92, 0.6)"],
.tabBarItem-1b8RUP[style*="rgba(255, 255, 255, 0.6)"] {
	border-color: rgba(var(--fontwhite1), 0.6) !important;
	color: rgba(var(--fontwhite1), 0.6) !important;
}
.top-28JiJ- .themed-OHr7kt.item-PXvHYJ.selected-3s45Ha,		/* modal				tabbaritem selected				*/
.top-28JiJ- .item-PXvHYJ[style*="rgb(79, 84, 92)"],
.top-28JiJ- .item-PXvHYJ[style*="rgb(255, 255, 255)"],
.themed-OHr7kt.tabBarItem-1b8RUP.selected-3s45Ha,
.tabBarItem-1b8RUP[style*="rgb(79, 84, 92)"],
.tabBarItem-1b8RUP[style*="rgb(255, 255, 255)"] {
	border-color: rgb(var(--fontwhite1)) !important;
	color: rgb(var(--fontwhite1)) !important;
}
#app-mount .content-8biNdB p,								/* modal				listentry						*/
#app-mount .content-8biNdB ul li {
	color: rgb(var(--fontwhite2));
}
#app-mount .content-8biNdB ul li::before {					/* modal				listentrydot					*/
	background-color: rgb(var(--fontwhite2));
}

/* ----		13.1.	USERMODAL						----- */

#app-mount .root-SR8cQa {									/* modal				container							*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--vtransparencycolor), 0.3), 0 2px 10px 0 rgba(var(--vtransparencycolor), 0.3);
	position: relative;
	overflow: hidden;
}
.root-SR8cQa::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--user-background, var(--vpopout)) var(--vpopoutposition)/var(--vpopoutsize);
	filter: blur(var(--vpopoutblur));
	background-attachment: fixed;
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.root-SR8cQa::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.2));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
#app-mount .topSectionNormal-2-vo2m {						/* modal				headernormal						*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
.topSectionPlaying-1J5E4n {									/* modal				headerplaying						*/
	text-shadow: 1px 1px var(--vtextshadow);
}
.headerFill-adLl4x {										/* modal				activity							*/
	background-color: rgba(var(--vtransparencycolor), 0.1);
}
.body-3ND3kc {												/* modal				body								*/
	background-color: transparent;
}
.discriminator-xUhQkU {										/* header				discriminator						*/
	color: rgb(var(--fontwhite1));
}
.topSectionNormal-2-vo2m .discriminator-xUhQkU {
	color: rgb(var(--fontwhite2));
}
.additionalActionsIcon-1FoUlE,								/* header				additionalactionsicon				*/
.topSectionNormal-2-vo2m .additionalActionsIcon-1FoUlE,
.topSectionNormal-2-vo2m .additionalActionsIcon-1FoUlE:hover {
	color: rgb(var(--fontwhite1));
}
.topSectionNormal-2-vo2m .tabBarContainer-1s1u-z {			/* header				tabbarcontainer						*/
	border-top-color: rgba(var(--vtransparencycolor), 0.3);
}
#app-mount .header-QKLPzZ .textRow-19NEd_ {
	color: rgb(var(--fontwhite2));
}
#app-mount .topSectionNormal-2-vo2m .header-QKLPzZ .textRow-19NEd_ {
	color: rgb(var(--fontwhite3));
}
#app-mount .activityProfile-2bJRaP .headerText-1HLrL7 {		/* header				activitytext						*/
	color: rgb(var(--fontwhite1));
}
#app-mount .activityProfile-2bJRaP .content-3JfFJh,			/* header				activitycontent						*/
#app-mount .activityProfile-2bJRaP .details-38sfDr,			/* header				activitydetails						*/
#app-mount .activityProfile-2bJRaP .name-29ETJS {			/* header				activityname						*/
	color: rgb(var(--fontwhite2));
}
.activityName-1IaRLn,
.nameNormal-2lqVQK,
.nameWrap-3Z4G_9 {
	color: rgb(var(--fontwhite1));
}
.userInfoSectionHeader-CBvMDh {								/* body					sectionheader						*/
	color: rgb(var(--fontwhite3));
}
.userInfoSection-2acyCx + .userInfoSection-2acyCx {
	border-top-color: rgba(var(--fontwhite4), 0.3);
}
.connectedAccount-36nQx7 {									/* body					connectedaccount					*/
	border-color: rgba(var(--fontwhite4), 0.3);
}
.connectedAccountName-f8AEe2 {								/* body					connectedaccountname				*/
	color: rgb(var(--fontwhite2));
}
.connectedAccountOpenIcon-2cNbq5 {
	color: rgb(var(--fontwhite2));
}
.connectedAccountOpenIcon-2cNbq5:hover {
	color: rgb(var(--fontwhite1));
}
.listRow-hutiT_ {											/* body					listrow								*/
	color: rgb(var(--fontwhite2));
}
.guildNick-3uAm3i {											/* body					guildnick							*/
	color: rgb(var(--fontwhite3));
}
.listRow-hutiT_:hover {
	background-color: rgba(var(--vtransparencycolor), 0.2);
	color: rgb(var(--fontwhite1));
}
.listRow-hutiT_:hover .guildNick-3uAm3i {
	color: rgb(var(--fontwhite2));
}
.emptyIcon-pGTAhd {											/* body					emptypic							*/
	opacity: 0.6;
}
.emptyText-6tYmO5 {											/* body					emptytext							*/
	color: rgb(var(--fontwhite2));
}

/* ----		13.2.	GUILDADD/CREATION				----- */

.container-UC8Ug1 {											/* modal				item								*/
	background-color: rgb(var(--vtransparencycolor), 0.2);
	border: none;
}
.container-UC8Ug1:hover {
	background-color: rgb(var(--vtransparencycolor), 0.4);
}
.text-1FOLJS {												/* modal				text								*/
	color: rgb(var(--fontwhite2));
}
.container-UC8Ug1:hover .text-1FOLJS {
	color: rgb(var(--fontwhite1));
}
.arrow-hynWUl {												/* modal				arrow								*/
	object-position: -9999999px -9999999px;
	-webkit-mask: url(https://discordapp.com/assets/69a0ea5dbf79a129c81a0cb171b60b7a.svg) center/cover no-repeat;
	background: rgb(var(--fontwhite2));
}
.container-UC8Ug1:hover .arrow-hynWUl {
	background: rgb(var(--fontwhite1));
}
.input--jS-j2 {												/* modal				invite input						*/
	background: transparent;
}
.inputInner-2akrSS {										/* modal				invite input inner					*/
	border-width: 1px;
	border-style: solid;
}
.container-1CE3eW .footer-2gL1pp .lookBlank-3eh9lL {
	color: rgb(var(--fontwhite2));
}
.container-1CE3eW .footer-2gL1pp .lookBlank-3eh9lL:hover {
	color: rgb(var(--fontwhite1));
}

/* ----		13.3.	REGIONSELECTMODAL				---- */

#app-mount .regionSelectModal-12e-57 {						/* modal				container							*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--vtransparencycolor), 0.3), 0 2px 10px 0 rgba(var(--vtransparencycolor), 0.3);
	position: relative;
	overflow: hidden;
}
.regionSelectModal-12e-57::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--vpopout) var(--vpopoutposition)/var(--vpopoutsize);
	background-attachment: fixed;
	filter: blur(var(--vpopoutblur));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.regionSelectModal-12e-57::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.2));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
#app-mount .regionSelectModal-12e-57 .regionSelectModalOption-2DSIZ3 {
	background-color: rgba(var(--vtransparencycolor), 0.2);
	border-color: rgba(var(--vtransparencycolor), 0.1);
}
#app-mount .regionSelectModal-12e-57 .regionSelectModalOption-2DSIZ3:hover {
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
#app-mount .regionSelectModal-12e-57 .regionSelectModalFooter-20C5iA {
	color: rgb(var(--fontwhite3));
}

/* ----		13.4.	UPLOADMODAL						---- */

#app-mount .uploadModal-2ifh8j {							/* modal				container							*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--vtransparencycolor), 0.3), 0 2px 10px 0 rgba(var(--vtransparencycolor), 0.3);
	position: relative;
	border-radius: 10px;
}
.uploadModal-2ifh8j::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--vpopout) var(--vpopoutposition)/var(--vpopoutsize);
	background-attachment: fixed;
	filter: blur(var(--vpopoutblur));
	width: unset;
	height: unset;
	pointer-events: none;
	border-radius: 10px;
	z-index: -1;
}
.uploadModal-2ifh8j::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.2));
	width: unset;
	height: unset;
	pointer-events: none;
	border-radius: 10px;
	z-index: -1;
}

.uploadModalIn-1z07Bv .uploadDropModal-2kTwbc {
	width: unset;
}
.uploadModal-2ifh8j .inner-3nWsbo,							/* modal				inner								*/
.uploadModalIn-1z07Bv .uploadDropModal-2kTwbc .inner-3nWsbo {
	border-color: rgba(var(--fontwhite1), 0.5);
	color: rgb(var(--fontwhite1));
}
.uploadModal-2ifh8j .inner-3nWsbo .file-34mY5K .description-2ug5H_ .filename-ovv3c5 {
	color: rgb(var(--fontwhite1));
}
.uploadModalIn-1z07Bv .uploadDropModal-2kTwbc .inner-3nWsbo .title-2Vtl4y {
	text-shadow: 1px 1px var(--vtextshadow);
}
.uploadModalIn-1z07Bv .uploadDropModal-2kTwbc .inner-3nWsbo .instructions-2Du9gG {
	color: rgb(var(--fontwhite3));
	text-shadow: 1px 1px var(--vtextshadow);
}
.content-P4SiGI {											/* modal				errorcontent						*/
	color: rgb(var(--fontwhite3));
}
.navArrow-3Q9QPC {											/* modal				navarrow							*/
	-webkit-mask: url(https://discordapp.com/assets/c83861b2303b7ee40c419e9590d57f11.svg) center/contain no-repeat;
	background-color: rgb(var(--fontwhite3));
	object-position: -9999999px -9999999px;
}
.uploadModal-2ifh8j .inner-zqa7da {							/* modal				channeltextarea						*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
.uploadModal-2ifh8j .footer-3mqk7D {						/* modal				footer								*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
.uploadModal-2ifh8j .checkbox-1ix_J3 {						/* modal				checkbox							*/
	border-color: rgb(var(--fontwhite1)) !important;
}
.uploadModal-2ifh8j .inner-3nWsbo .file-34mY5K .icon-kyxXVr.image-2yrs5j {
	box-shadow: 0 2px 8px rgba(var(--vtransparencycolor), 0.4);
}

/* ----		13.5.	KEYBOARDSHORTCUTSMODAL			---- */

#app-mount .keyboardShortcutsModal-3piNz7 {					/* modal				container							*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--vtransparencycolor), 0.3), 0 2px 10px 0 rgba(var(--vtransparencycolor), 0.3);
	position: relative;
	overflow: hidden;
}
.keyboardShortcutsModal-3piNz7::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--vpopout) var(--vpopoutposition)/var(--vpopoutsize);
	background-attachment: fixed;
	filter: blur(var(--vpopoutblur));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.keyboardShortcutsModal-3piNz7::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.2));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
#app-mount .modalTitle-37O4n6 {								/* modal				title								*/
	color: rgb(var(--fontwhite1));
}
#app-mount .modalSubtitle-1Pj5nv {							/* modal				subtitle							*/
	border-color: rgba(var(--fontwhite4), 0.3);
	color: rgb(var(--fontwhite1));
}
#app-mount .keyboardShortcutList-13cQ-8 .keybindGroup--6Qp-w .keybindDescription-2RDbC2 {
	color: rgb(var(--fontwhite2));
}
#app-mount .keybindShortcut-1BD6Z1 {
	color: rgb(var(--fontwhite1));
}
#app-mount .keybindShortcut-1BD6Z1 span {
	background-color: rgb(var(--fontwhite4));
	border: 1px solid rgb(0, 0, 0, 0.4);
	box-shadow: inset 0 -4px 0 rgb(0, 0, 0, 0.4);
	color: rgb(var(--fontwhite1));
}
#app-mount .keybindShortcut-1BD6Z1 span [fill^="#"] {
	fill: rgb(var(--fontwhite1));
}
#app-mount .tabButton-1n4gNP {
	background-color: rgb(var(--fontwhite4));
	border: 1px solid rgb(0, 0, 0, 0.4);
    border-radius: 4px;
	box-shadow: inset 0 -4px 0 rgb(0, 0, 0, 0.4);
	color: rgb(var(--fontwhite1));
}
#app-mount .tabButton-1n4gNP rect[fill="#4F545C"],
#app-mount .tabButton-1n4gNP path[fill="#36393F"] {
	display: none;
}

/* ----		13.6.	QUICKSWITCHER					---- */

#app-mount .quickswitcher-3JagVE {							/* modal				container							*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--vtransparencycolor), 0.3), 0 2px 10px 0 rgba(var(--vtransparencycolor), 0.3);
	position: relative;
	overflow: hidden;
}
.quickswitcher-3JagVE::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--vpopout) var(--vpopoutposition)/var(--vpopoutsize);
	background-attachment: fixed;
	filter: blur(var(--vpopoutblur));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.quickswitcher-3JagVE::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.2));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.scroller-zPkAnE {
	background-color: transparent;
}
#app-mount .input-2VB9rf {									/* modal				input								*/
	background-color: rgba(var(--vtransparencycolor), 0.4);
	box-shadow: 0 2px 10px 0 rgba(var(--vtransparencycolor), 0.3);
	color: rgb(var(--fontwhite1));
}
#app-mount .input-2VB9rf::placeholder {
	color: rgb(var(--fontwhite3));
}
#app-mount .header-13MUnb {									/* modal				header								*/
	color: rgb(var(--fontwhite2));
}
#app-mount .resultFocused-3aIoYe {							/* modal				resultfocused						*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
#app-mount .contentUnread-3gTHvA {							/* modal				contentunread						*/
	color: rgb(var(--fontwhite1));
}
#app-mount .contentDefault-16dKSY,							/* modal				contentdefault						*/
#app-mount .icon-30q1Or,									/* modal				icon								*/
#app-mount .misc-1CT3G7 {									/* modal				misc								*/
	color: rgb(var(--fontwhite3));
}
#app-mount .note-S--UP5 {									/* modal				note								*/
	color: rgb(var(--fontwhite4));
}
#app-mount .resultFocused-3aIoYe .contentDefault-16dKSY,
#app-mount .resultFocused-3aIoYe .icon-30q1Or,
#app-mount .contentUnread-3gTHvA .icon-30q1Or,
#app-mount .resultFocused-3aIoYe .misc-1CT3G7 {
	color: rgb(var(--fontwhite1));
}
#app-mount .resultFocused-3aIoYe .note-S--UP5 {
	color: rgb(var(--fontwhite3));
}
#app-mount .tipsWithoutResults-lGY-De,
#app-mount .tipsWithResults-HhTE9b {
	border-color: rgba(var(--fontwhite4), 0.3);
	color: rgb(var(--fontwhite3));
}
#app-mount .keybindShortcutTipsSelect-HDyfe8:last-of-type::before {
	background-color: rgba(var(--fontwhite4), 0.3);
}

/* ----		13.7.	INVITEMODAL/GROUPCREATE			---- */

#app-mount .contentWrapper-3WC1ID {								/* modal				guildinvitemodal				*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--vtransparencycolor), 0.3), 0 2px 10px 0 rgba(var(--vtransparencycolor), 0.3);
	position: relative;
	overflow: hidden;
}
.contentWrapper-3WC1ID::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--vpopout) var(--vpopoutposition)/var(--vpopoutsize);
	background-attachment: fixed;
	filter: blur(var(--vpopoutblur));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.contentWrapper-3WC1ID::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.2));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}

#app-mount .friendSelected-1sa4bG,								/* modal				groupdmrow						*/
#app-mount .inviteRow-2L02ae:hover {							/* modal				guildrow						*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
#app-mount .friend-3KALPe,										/* modal				groupdmrow						*/
#app-mount .inviteRowName-1tVaxu {								/* modal				username						*/
	color: rgb(var(--fontwhite2));
}
#app-mount .friendSelected-1sa4bG,
#app-mount .inviteRow-2L02ae:hover .inviteRowName-1tVaxu {
	color: rgb(var(--fontwhite1));
}
#app-mount .checkBoxLabel-4PWfpk,
#app-mount .footerText-2a7NxZ,
#app-mount .subTitle-3TUjmF,
#app-mount .subtitle-2P4u9v,
#app-mount .subText-bCySlS {
	color: rgb(var(--fontwhite3));
}
.tag-2gHSR7 {													/* modal				added user						*/
	background-color: rgb(var(--vaccentcolor));
	color: rgb(var(--fontwhite1));
	text-shadow: 1px 1px var(--vtextshadow);
}
.pill-1dHPfk {
	background-color: rgba(var(--vtransparencycolor), 0.5);
}

/* ----		13.8.	LOGINSCREEN						---- */

#app-mount .wrapper-3Q5DdO {								/* login				wrapper								*/
	background: transparent;
}
.wrapper-3Q5DdO::before,										/* login				winbuttonshadow						*/
.wrapper-3Q5DdO .rightSplit-2US0xy,							/* login				background							*/
.wrapper-3Q5DdO .canvas-3XuBXe {							/* login				movingshadow						*/
	display: none;
}
#app-mount .authBox-hW6HRx {								/* login				modal								*/
	background-color: rgba(var(--vtransparencycolor), 0.5);
	box-shadow: 0 0 0 1px rgba(var(--vtransparencycolor), 0.3), 0 2px 10px 0 rgba(var(--vtransparencycolor), 0.3);
	color: rgb(var(--fontwhite3));
	position: relative;
	overflow: hidden;
}
#app-mount .quote-3aooyW {									/* login				loadingquote						*/
	color: rgb(var(--fontwhite1));
}
#app-mount .contentBase-11jeVK {							/* login				loadingcontent						*/
	color: rgb(var(--fontwhite3));
}
#app-mount .problems-3mgf6w {								/* login				loadingproblems						*/
	color: rgb(var(--fontwhite1));
}
#app-mount .problemsText-1Yx-Kl {							/* login				loadingproblemtext					*/
	color: rgb(var(--fontwhite3));
}

/* ----		13.9.	TERMACCEPTMODAL					---- */

#app-mount .modal-DRZfgq {									/* modal				container							*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--vtransparencycolor), 0.3), 0 2px 10px 0 rgba(var(--vtransparencycolor), 0.3);
	position: relative;
	overflow: hidden;
}
.modal-DRZfgq::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--vpopout) var(--vpopoutposition)/var(--vpopoutsize);
	background-attachment: fixed;
	filter: blur(var(--vpopoutblur));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.modal-DRZfgq::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.2));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}

[style*="/assets/a13cfdd7220132fff399a76c3ed64519.svg"],	/* modal				image								*/
[src*="/assets/a13cfdd7220132fff399a76c3ed64519.svg"] {
	filter: brightness(85%) invert(100%);
	opacity: 0.7;
}

#app-mount .modal-DRZfgq .checked-3_4uQ9 {					/* modal				ackcheckbox							*/
	background-color: rgb(var(--vaccentcolor));
}
#app-mount .modal-DRZfgq .checkbox-1ix_J3 [stroke="#7289da"] {
	stroke: rgb(var(--fontwhite1)) !important;
}
#app-mount .ack-2yIUvY {									/* modal				acklabel							*/
	color: rgb(var(--fontwhite2));
}
#app-mount .buttonContainer-3S_miP {						/* modal				footer							*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
	box-shadow: none;
}

/* ----		13.10.	DOWNLOADAPPMODAL				---- */

#app-mount .downloadApps-wbBFdZ {							/* modal				container							*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--vtransparencycolor), 0.3), 0 2px 10px 0 rgba(var(--vtransparencycolor), 0.3);
	position: relative;
	overflow: hidden;
}
.downloadApps-wbBFdZ::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--vpopout) var(--vpopoutposition)/var(--vpopoutsize);
	background-attachment: fixed;
	filter: blur(var(--vpopoutblur));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.downloadApps-wbBFdZ::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.2));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.downloadApps-wbBFdZ .header-nJMe-Q {
	color: rgb(var(--fontwhite2));
}
.downloadApps-wbBFdZ .platforms-28Rb-3 .platform-iik236 {
	border-color: rgb(var(--fontwhite3));
}
.downloadApps-wbBFdZ .platforms-28Rb-3 .platform-iik236 p {
	color: rgb(var(--fontwhite3));
}
.downloadApps-wbBFdZ .platforms-28Rb-3 .platform-iik236 .downloadButton-1bWXpg {
	background-color: rgb(var(--fontwhite3));
}
.downloadApps-wbBFdZ .footer-1nkeBm {
	color: rgb(var(--fontwhite3));
}

/* ----		13.11.	GUILDBOOSTMODAL					---- */

#app-mount .perksModal-fSYqOq {								/* modal				wrapper								*/
	background-color: transparent;
}
.carouselContainer-2-vIZS {									/* modal				scrollercontainer					*/
	-webkit-mask: linear-gradient(to right, rgba(0,0,0,0) 0px, rgba(0,0,0,1) 60px, rgba(0,0,0,1) calc(100vw - 60px), rgba(0,0,0,0) 100vw);
}
.carouselGradientEdge-2W94ou {								/* modal				scrollergradient					*/
	display: none;
}
#app-mount .subscriberCount-27QHc5 {						/* modal				subcount							*/
	color: rgb(var(--fontwhite3));
}
#app-mount .subscriberCount-27QHc5 strong {
	color: rgb(var(--fontwhite2));
}
#app-mount .moreSubscribers-1cuWDE {						/* modal				suboverflow							*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
	color: rgb(var(--fontwhite1));
}

#app-mount .subscribersPopout-2CP6Ln {						/* subpopout			container							*/
	background-color: transparent;
	box-shadow: 0 2px 10px rgba(var(--vtransparencycolor), 0.2);
	overflow: hidden;
}
.subscribersPopout-2CP6Ln::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--vpopout) var(--vpopoutposition)/var(--vpopoutsize);
	background-attachment: fixed;
	filter: blur(var(--vpopoutblur));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.subscribersPopout-2CP6Ln::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.35));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
#app-mount .subscribersPopoutUser-3rC75S {					/* subpopout			users								*/
	color: rgb(var(--fontwhite3));
}

#app-mount .ctaBar-2UsjF2 {									/* current boost stats	container							*/
	background-color: rgba(var(--vtransparencycolor), 0.4);
	background-image: url(https://discordapp.com/assets/94ff6fdc535b6ecb7b1bc54f2dd56a10.svg);
}
.guildIcon-3raYf3 {											/* current boost stats	guild icon							*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}

#app-mount .perk-2WeBWW {									/* modal				perkcard							*/
	background-color: rgba(var(--vtransparencycolor), 0.4);
}

#app-mount .tierHeaderLocked-1s2JJz {						/* modal				tierheaderlocked 					*/
	background-color: rgba(var(--vtransparencycolor), 0.4);
	color: rgb(var(--fontwhite3));
}
#app-mount .tierLock-3CSxSX {								/* modal				tierlock 							*/
	color: rgb(var(--fontwhite4));
}
#app-mount .tierHeaderUnlocked-1n-OTI {						/* modal				tierheaderunlocked 					*/
	background-color: rgba(var(--vtransparencycolor), 0.5);
	color: rgb(var(--fontwhite1));
}
#app-mount .tierUnlocked-25K6Kv {							/* modal				tierunlocked 						*/
	background-color: rgb(var(--fontwhite1));
}
#app-mount .boostCount-UFqabz {
	background-color: rgba(var(--vtransparencycolor), 0.4);
	color: rgb(var(--fontwhite3));
}
#app-mount .tierBody-16Chc9 {								/* modal				tierbody 							*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
	color: rgb(var(--fontwhite3));
}
#app-mount .tierNoneContainer-3hhK3h {						/* modal				tiernonecontainer					*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
.tierNoneCard-peD7hV {										/* modal				tiernonecard						*/
	opacity: 0.6;
}
#app-mount .tierNoneText-2OvCv7 {
	color: rgb(var(--fontwhite3));
}
#app-mount .tierCloseHint-380zIA,							/* modal				tierclose							*/
#app-mount .tierCloseClose-2z5dSa {
	color: rgb(var(--fontwhite1));
}
#app-mount .tierMarkerBackground-3q29am {					/* modal				tiermilestone 						*/
	background: transparent;
}
#app-mount .tierMarkerInProgress-24LMzJ {
	background: rgba(var(--vtransparencycolor), 0.3) !important;
}
#app-mount .selectedTier-1JkO7i .tierMarker-5HkGJ_ {
	box-shadow: 0 4px 8px rgba(var(--vtransparencycolor), 0.24);
}
#app-mount .tierMarkerLabel-2PluTw {						/* modal				tiermilestonelabel					*/
	color: rgb(var(--fontwhite3));
}
#app-mount .selectedTier-1JkO7i .tierMarkerLabel-2PluTw {
	color: rgb(var(--fontwhite1));
}
#app-mount .barBackground-2EEiLw {							/* modal				tierbar 								*/
	background: linear-gradient(to right, rgba(0,0,0,0) 0%, rgba(0,0,0,0) 3%, rgba(var(--vtransparencycolor), 0.3) 3%, rgba(var(--vtransparencycolor), 0.3) 30.2%, rgba(0,0,0,0) 30.2%, rgba(0,0,0,0) 36.2%, rgba(var(--vtransparencycolor), 0.3) 36.2%, rgba(var(--vtransparencycolor), 0.3) 63.5%, rgba(0,0,0,0) 63.5%, rgba(0,0,0,0) 69.5%, rgba(var(--vtransparencycolor), 0.3) 69.5%, rgba(var(--vtransparencycolor), 0.3) 96.7%, rgba(0,0,0,0) 96.7%, rgba(0,0,0,0) 100%);
}
.barSecondary-3B1aP2 {
	background-color: rgb(var(--vaccentcolor));
}
.wrapper-3nSjSv .heading-4znNKq {							/* modal				boostaddwrapper header						*/
	text-shadow: 1px 1px var(--vtextshadow);
}
.tier-1EY-yj {												/* modal				boostaddwrapper tier						*/
	background-color: rgb(var(--vtransparencycolor), 0.3);
}
#app-mount .giftIcon-2Pjbiy {								/* modal				gifticon							*/
	color: rgb(var(--fontwhite3));
	margin: 0 18px;
}
#app-mount .button-38aScr:hover .giftIcon-2Pjbiy {
	color: rgb(var(--fontwhite2));
}
#app-mount .button-38aScr:active .giftIcon-2Pjbiy {
	color: rgb(var(--fontwhite1));
}

.header-1F6gxU {											/* prebuy popout		header								*/
	background: rgba(var(--vtransparencycolor), 0.3);
	padding-bottom: 10px;
	margin-bottom: 10px;
}
#app-mount .iconWrapper-3LVgIo {							/* prebuy popout		amount icon wrapper					*/
	background: rgba(var(--vtransparencycolor), 0.3);
}
.icon-TYbVk4:hover {										/* prebuy popout		amount icon							*/
	background: rgb(var(--vaccentcolor));
	color: rgb(var(--fontwhite1));
}
.upsellFooter-6EgwMe {										/* prebuy popout		footer details						*/
	background: rgba(var(--vtransparencycolor), 0.3);
}
.perksList-1vtwXn {											/* prebuy popout		perkslist							*/
	background: rgba(var(--vtransparencycolor), 0.3);
}
.perkRow-2dYUqs {											/* prebuy popout		perkrow								*/
	border-bottom-color: rgba(var(--fontwhite3), 0.3);
}

#app-mount .selectGuild-1Ygl76:hover {
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
#app-mount .tierPill-3gJ0eN {
	background-color: rgba(var(--vtransparencycolor), 0.3);
	color: rgb(var(--fontwhite1));
}

/* ----		13.12.	REACTIONSMODAL					---- */

#app-mount .scroller-1-nKid {								/* modal				sidebar								*/
	background-color: rgba(var(--vtransparencycolor), 0.4);
}
#app-mount .reactors-Blmlhw {								/* modal				list								*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
#app-mount .reactionDefault-GBA58K:hover {					/* modal				reaction							*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
#app-mount .reactionSelected-1pqISm {
	background-color: rgba(var(--vtransparencycolor), 0.4);
}
#app-mount .count-1vzEyg {									/* modal				reaction count						*/
	color: rgb(var(--fontwhite2));
}
#app-mount .reactionDefault-GBA58K:hover .count-1vzEyg,
#app-mount .reactionSelected-1pqISm .count-1vzEyg {
	color: rgb(var(--fontwhite1));
}
#app-mount .nickname-miBZxb {								/* modal				nickname							*/
	color: rgb(var(--fontwhite1));
}
#app-mount .username-Af3M5Y {								/* modal				username							*/
	color: rgb(var(--fontwhite1));
}
#app-mount .discriminator-byOsvi {							/* modal				discriminator						*/
	color: rgb(var(--fontwhite3));
}
#app-mount .tagFaded-WP86yt {
	opacity: 0.5;
}
#app-mount .remove-3V-yj8 {									/* modal				remove								*/
	color: rgb(var(--fontwhite2));
}
#app-mount .remove-3V-yj8:hover {
	background-color: rgba(var(--vtransparencycolor), 0.4);
	color: rgb(var(--fontwhite1));
}

/* ----		13.13.	GUILDTEMPLATEMODAL				---- */

.ctaSection-izWwhs {										/* modal				ctasection							*/
	background-color: transparent;
}
.formSection-1NFAGI {										/* modal				formsection							*/
	background-color: transparent;
}

.divider-2gQcba {											/* modal				divider								*/
	border-color: rgba(var(--fontwhite3), 0.5);
}

.usagePill-2WGS4A {											/* modal				usagepill 1							*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
.usagePill-_nSrnP {											/* modal				usagePill 2							*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}

.channelsWrapper-2HhUER {									/* modal				channelswrapper						*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}

.channel-OaJouZ {											/* modal				channel								*/
	color: rgb(var(--fontwhite3));
}

.rolesWrapper-2yOx9S {										/* modal				roleswrapper							*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}

#app-mount .role-3paDXR {									/* modal				role								*/
	border-color: rgba(var(--fontwhite3), 0.6);
	border-radius: 5px;
	padding: 0 5px;
	position: relative;
}
#app-mount .role-3paDXR[style*="border-color: rgba(185, 187, 190, 0.6)"] {
	border-color: rgba(var(--fontwhite3), 0.6) !important;
}
#app-mount .role-3paDXR .roleName-1JcOmP {					/* modal				rolename							*/
	color: rgb(var(--fontwhite1));
	margin: 0;
	font-weight: normal;
	position: relative;
	height: 20px;
	line-height: 20px;
	z-index: 1000;
	pointer-events: none;
}
#app-mount .role-3paDXR .roleCircle-3DE8xJ {				/* modal				rolecircle							*/
	position: absolute;
	background-color: rgb(var(--fontwhite3));
	border-radius: 3px;
	opacity: 0.3;
	height: 100%;
	width: 100%;
	left: 0;
	top: 0;
}
#app-mount .role-3paDXR .roleCircle-3DE8xJ[style*="background-color: rgb(185, 187, 190)"] {
	background-color: rgb(var(--fontwhite3)) !important;
}

/* ----		13.14.	GUILDWELCOMEMODAL				---- */

.optionContainer-15srkc {									/* modal				option								*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
.optionContainer-15srkc:hover {
	background-color: rgba(var(--vtransparencycolor), 0.4);
}

/* ----		13.15.	SCREENSHAREMODAL				---- */

#app-mount .sourceThumbnail-27dolk {						/* modal				preview tiles						*/
	background-color: rgba(var(--vtransparencycolor), 0.4);
	box-shadow: 0 2px 5px rgba(var(--vtransparencycolor), 0.2), 0 0 0 1px rgba(var(--vtransparencycolor), 0.6);
}
.card-2Mz_4z {
	background-color: rgba(var(--vtransparencycolor), 0.2);
	border-color: rgba(var(--vtransparencycolor), 0.4);
}
#app-mount .item-3T2z1R {
	border-color: rgba(var(--vtransparencycolor), 0.4);
}
.selectorButton-EEUWed:not(.selectorButtonSelected-t5V9On) {
	background-color: rgba(var(--vtransparencycolor), 0.2);
}


/* ~~~~		14.		POPOUTS							~~~~ */


.layer-v9HyYc:nth-child(1) {
	z-index: 1002;
}
.layer-v9HyYc:nth-child(2) {
	z-index: 1003;
}
.layer-v9HyYc:nth-child(3) {
	z-index: 1004;
}
.layer-v9HyYc:nth-child(4) {
	z-index: 1005;
}
.layer-v9HyYc:nth-child(5) {
	z-index: 1006;
}
.layer-v9HyYc:nth-child(6) {
	z-index: 1007;
}
.layer-v9HyYc:nth-child(7) {
	z-index: 1008;
}
.layer-v9HyYc:nth-child(8) {
	z-index: 1009;
}
.layer-v9HyYc:nth-child(9) {
	z-index: 1010;
}

#app-mount .popout-2iWAc-:not(.noShadow-3pu20z) {
	box-shadow: 0 0 1px rgba(var(--vtransparencycolor), 0.2), 0 1px 4px rgba(var(--vtransparencycolor), 0.1);
}
.popout-2iWAc-[style*="translateY(-100%)"] {
	transform: unset !important;
}
.popout-2iWAc-[style*="translateX(-50."],
.popout-2iWAc-[style*="translateX(-50%)"] {
	transform: translateX(-50%) !important;
}
.popout-2iWAc-[style*="translateX(-84."],
.popout-2iWAc-[style*="translateX(-84%)"] {
	transform: translateX(-84%) !important;
}
.popout-2iWAc-[style*="translateX(-100%)"] {
	transform: translateX(-100%) !important;
}
.popout-2iWAc-[style*="translateY(-100%)"] > *:only-child {
	margin-top: -100%;
}
.popout-2iWAc-[style*="translateX(-50."] > *,
.popout-2iWAc-[style*="translateX(-50%)"] > * {
	margin-left: -50%;
	transform: translateX(50%);
}
.popout-2iWAc-[style*="translateX(-84."] > *,
.popout-2iWAc-[style*="translateX(-84%)"] > * {
	margin-left: -84%;
	transform: translateX(84%);
}
.popout-2iWAc-[style*="translateX(-100%)"] > * {
	margin-left: -100%;
	transform: translateX(100%);
}
.popout-2iWAc-[style*="translateX(-50."] > *.scrollerWrap-2lJEkd,
.popout-2iWAc-[style*="translateX(-50%)"] > *.scrollerWrap-2lJEkd {
	margin-right: 50%;
}
.popout-2iWAc-[style*="translateX(-100%)"] > *.scrollerWrap-2lJEkd {
	margin-right: 100%;
}

#app-mount .container-2x5lvQ,								/* RTCpopout			(for example voicequality)			*/
#app-mount .quickSelectPopout-X1hvgV,						/* quickselect			(for example regionselect)			*/
#app-mount .themedPopout-1TrfdI,							/* themed popout		(for example mentionpopout)			*/
#app-mount .popoutList-T9CKZQ {								/* listpopout			(for example auditlogs)				*/
	background-color: transparent;
	border: none;
	border-radius: 5px;
	box-shadow: 0 0 0 1px rgba(var(--vtransparencycolor), 0.3), 0 2px 10px 0 rgba(var(--vtransparencycolor), 0.3);
	color: rgb(var(--fontwhite1));
	position: relative;
}
.container-2x5lvQ::before,
.quickSelectPopout-X1hvgV::before,
.themedPopout-1TrfdI::before,
.popoutList-T9CKZQ::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--vpopout) var(--vpopoutposition)/var(--vpopoutsize);
	background-attachment: fixed;
	filter: blur(var(--vpopoutblur));
	width: unset;
	height: unset;
	pointer-events: none;
	border-radius: 5px;
	z-index: -1;
}
.container-2x5lvQ::after,
.quickSelectPopout-X1hvgV::after,
.themedPopout-1TrfdI::after,
.popoutList-T9CKZQ::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.25));
	width: unset;
	height: unset;
	pointer-events: none;
	border-radius: 5px;
	z-index: -1;
}
#app-mount .quickSelectPopoutOption-opKBx9:hover {
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
#app-mount .quickSelectPopoutOption-opKBx9.selected {
	background-color: rgba(var(--vtransparencycolor), 0.4);
	color: rgb(var(--fontwhite1));
}
#app-mount .container-2x5lvQ .header-2C89wJ {
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
#app-mount .container-2x5lvQ section {
	background-color: transparent;
}
#app-mount .container-2x5lvQ section p {
	color: rgb(var(--fontwhite3));
}
#app-mount .container-2x5lvQ section strong {
	color: rgb(var(--fontwhite1));
}
#app-mount .debugButton-1Zec0y {
	color: rgb(var(--fontwhite3));
}

#app-mount .header-3po9qd {									/* popout				innerheader (for example GoLive)	*/
	color: rgb(var(--fontwhite1));
}
#app-mount .breadcrumbWrapper-WmDjgG {						/* popout				breadcrumbs (for example NitroGift)	*/
	color: rgb(var(--fontwhite3));
}
#app-mount .activeBreadcrumb-p6aw-F {
	color: rgb(var(--fontwhite1));
}

#app-mount .divider-1que2t {								/* popout				divider								*/
	border-color: rgba(var(--fontwhite4), 0.3);
}
#app-mount .giftBlurb-4VKZWm,
#app-mount .trialNote-wEO1RW,
#app-mount .trialText-2gR3-S {
	color: rgb(var(--fontwhite2));
}
#app-mount .price-3dKlQv,
#app-mount .annualDiscount-1VxngV {
	color: rgb(var(--fontwhite1));
}
#app-mount .interval-bfFUiQ {
	color: rgb(var(--fontwhite3));
}
#app-mount .option-1l2vXE {
	background-color: rgba(var(--vtransparencycolor), 0.3);
}

#app-mount .addGamePopout-2RY8Ju {							/* addgamepopout											*/
	background-color: transparent;
}
.addGamePopout-2RY8Ju::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--vpopout) var(--vpopoutposition)/var(--vpopoutsize);
	background-attachment: fixed;
	filter: blur(var(--vpopoutblur));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.addGamePopout-2RY8Ju::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.15));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}

/* ----		14.1.	CONTEXTMENU						---- */

.styleFlexible-wGDiIL,										/* contextmenu			flexible							*/
.styleFixed-sX-yHV,											/* contextmenu			fixed								*/
.submenu-2-ysNh {											/* contextmenu			submenu								*/
	background: transparent;
	box-shadow: 0 0 0 1px rgba(var(--vtransparencycolor), 0.3), 0 2px 10px 0 rgba(var(--vtransparencycolor), 0.3);
}
.styleFlexible-wGDiIL::before,
.styleFixed-sX-yHV::before,
.submenu-2-ysNh::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--vpopout) var(--vpopoutposition)/var(--vpopoutsize);
	background-attachment: fixed;
	filter: blur(var(--vpopoutblur));
	width: unset;
	height: unset;
	border-radius: 4px;
	pointer-events: none;
	z-index: -1;
}
.styleFlexible-wGDiIL::after,
.styleFixed-sX-yHV::after,
.submenu-2-ysNh::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.3));
	width: unset;
	height: unset;
	border-radius: 4px;
	pointer-events: none;
	z-index: -1;
}
.submenu-2-ysNh {
	position: relative;
}
.item-1tOPte.colorDefault-2K3EoJ {							/* contextmenu			item								*/
	color: rgb(var(--fontwhite2));
}
.item-1tOPte.colorBrand-ROmMP1,
.item-1tOPte.colorPremium-p4p7qO {
	color: rgb(var(--vaccentcolor));
}
.item-1tOPte.colorDanger-2qLCe1 {
	color: #F04747;
}
.item-1tOPte.colorDefault-2K3EoJ.focused-3afm-j,
.item-1tOPte.colorDefault-2K3EoJ:hover:not(.hideInteraction-1iHO1O) {
	background-color: rgba(var(--vtransparencycolor), 0.2);
	color: rgb(var(--fontwhite1));
}
.item-1tOPte.colorDanger-2qLCe1.focused-3afm-j,
.item-1tOPte.colorDanger-2qLCe1:hover:not(.hideInteraction-1iHO1O) {
	background-color: rgba(240, 71, 71, 0.2);
	color: rgb(var(--fontwhite1)) !important;
}
.item-1tOPte.colorBrand-ROmMP1.focused-3afm-j,
.item-1tOPte.colorBrand-ROmMP1:hover:not(.hideInteraction-1iHO1O),
.item-1tOPte.colorPremium-p4p7qO.focused-3afm-j,
.item-1tOPte.colorPremium-p4p7qO:hover:not(.hideInteraction-1iHO1O) {
	background-color: rgba(var(--vaccentcolor), 0.2);
	color: rgb(var(--fontwhite1)) !important;
}
#app-mount .item-1tOPte .checkbox-3s5GYZ {					/* contextmenu			checkbox 							*/
	color: rgb(var(--vaccentcolor));
}
#app-mount .item-1tOPte.colorDanger-2qLCe1 .checkbox-3s5GYZ {
	color: #F04747;
}
#app-mount .item-1tOPte .check-1JyqgN {						/* contextmenu			checkmark 							*/
	color: rgb(var(--fontwhite1));
	stroke: var(--vtextshadow);
}
.separator-2I32lJ {											/* contextmenu			separator							*/
	border-bottom-color: rgba(var(--fontwhite4), 0.3);
}
.button-F9qN4n {											/* contextmenu			quick reaction button				*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
.button-F9qN4n:hover {
	background-color: rgb(var(--vaccentcolor));
}

/* ----		14.2.	USERPOPOUT						---- */

.userPopout-3XzG_A {										/* popout				container							*/
	box-shadow: 0 0 0 1px rgba(var(--vtransparencycolor), 0.3), 0 2px 10px 0 rgba(var(--vtransparencycolor), 0.3);
}
.userPopout-3XzG_A::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--user-background, var(--vpopout)) var(--vpopoutposition)/var(--vpopoutsize);
	filter: blur(var(--vpopoutblur));
	background-attachment: fixed;
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.userPopout-3XzG_A::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.25));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.header-2BwW8b {											/* popout				header								*/
	color: rgb(var(--fontwhite1));
}
#app-mount .headerNormal-T_seeN {							/* popout				headernormal						*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
.headerPlaying-j0WQBV {										/* popout				headerplaying						*/
	text-shadow: 1px 1px var(--vtextshadow);
}
.headerStreaming-2FjmGz {									/* popout				headerstreaming						*/
	background: #593695;
}
.activity-11LB_k {											/* popout				activity							*/
	background-color: rgba(var(--vtransparencycolor), 0.1);
}
#app-mount .body-3iLsc4,									/* popout				body								*/
#app-mount .bodyInner-245q0L,								/* popout				bodyinner							*/
#app-mount .footer-1fjuF6 {									/* popout				footer								*/
	background-color: transparent;
	color: rgb(var(--fontwhite2));
}
#app-mount .footer-1fjuF6 {
	border-color: rgba(var(--fontwhite4), 0.3);
}

.headerTag-2pZJzA {											/* header				headertag							*/
	color: rgb(var(--fontwhite2));
}
.headerName-fajvi9,											/* header				username							*/
.headerTagUsernameNoNickname-2_H881,
#app-mount .headerNormal-T_seeN .headerName-fajvi9,
#app-mount .headerNormal-T_seeN .headerTagUsernameNoNickname-2_H881 {
	color: rgb(var(--fontwhite1));
}
#app-mount .headerTop-3C2Zn0 .textRow-19NEd_ {
	color: rgb(var(--fontwhite2));
}
#app-mount .headerNormal-T_seeN .headerTop-3C2Zn0 .textRow-19NEd_ {
	color: rgb(var(--fontwhite3));
}
#app-mount .activityUserPopout-2yItg2 .headerText-1HLrL7 {	/* header				activitytext						*/
	color: rgb(var(--fontwhite1));
}
#app-mount .activityUserPopout-2yItg2 .content-3JfFJh,		/* header				activitycontent						*/
#app-mount .activityUserPopout-2yItg2 .details-38sfDr,		/* header				activitydetails						*/
#app-mount .activityUserPopout-2yItg2 .name-29ETJS {		/* header				activityname						*/
	color: rgb(var(--fontwhite2));
}
.activityName-1IaRLn {										/* header				activityname						*/
	color: rgb(var(--fontwhite1));
}
.bar-3urHkF {												/* header				activitybar							*/
	background-color: rgba(var(--fontwhite1), 0.2);
}
.barInner-3NDaY_ {											/* header				activitybarfill						*/
	background-color: rgb(var(--fontwhite1));
}
.text-AOoUen {												/* header				activitybartext						*/
	color: rgb(var(--fontwhite2));
}
.listenAlongIcon-2vb1HG {									/* header				listenalong							*/
	color: rgb(var(--fontwhite1));
}

.bodyTitle-Y0qMQz {											/* body					title								*/
	color: rgb(var(--fontwhite3));
}
.root-3-B5F3 {												/* body					roles								*/
	max-height: 100px;
	overflow-x: hidden;
	overflow-y: scroll;
}
#app-mount .root-3-B5F3::-webkit-scrollbar {
	width: 4px;
}
#app-mount .role-2irmRk {									/* body					role								*/
	border-color: rgba(var(--fontwhite3), 0.6);
	border-radius: 5px;
	padding: 0 5px;
	position: relative;
}
#app-mount .role-2irmRk[style*="border-color: rgba(185, 187, 190, 0.6)"] {
	border-color: rgba(var(--fontwhite3), 0.6) !important;
}
#app-mount .role-2irmRk .roleName-32vpEy {					/* body					rolename							*/
	color: rgb(var(--fontwhite1));
	margin: 0;
	font-weight: normal;
	position: relative;
	height: 20px;
	line-height: 20px;
	z-index: 1000;
	pointer-events: none;
}
#app-mount .role-2irmRk .roleCircle-3xAZ1j {				/* body					rolecircle							*/
	position: absolute;
	background-color: rgb(var(--fontwhite3));
	border-radius: 3px;
	opacity: 0.3;
	height: 100%;
	width: 100%;
	left: 0;
	top: 0;
}
#app-mount .role-2irmRk .roleCircle-3xAZ1j[style*="background-color: rgb(185, 187, 190)"] {
	background-color: rgb(var(--fontwhite3)) !important;
}
#app-mount .role-2irmRk .roleCircle-3xAZ1j:not(:empty):hover {
	opacity: 1;
	z-index: 2000;
	cursor: pointer;
}

.textarea-2r0oV8:focus {									/* body					note 								*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
.textarea-2r0oV8::placeholder {
	color: rgba(var(--fontwhite4));
}

.wumpusWrapper-yrvoR3 {										/* footer				wumpus new user 					*/
	margin-top: 27px;
}

#app-mount .quickMessage-1yeL4E {							/* footer				quickmessage						*/
	background-color: rgba(var(--vtransparencycolor), 0.1);
	border-color: rgba(var(--vtransparencycolor), 0.3);
	color: rgb(var(--fontwhite1));
}
#app-mount .quickMessage-1yeL4E:hover {
	border-color: rgb(var(--vtransparencycolor));
}
#app-mount .quickMessage-1yeL4E:focus {
	border-color: rgb(var(--vaccentcolor));
}
#app-mount .quickMessage-1yeL4E::placeholder {
	color: rgb(var(--fontwhite3));
}

/* ----		14.3.	EMOJIPICKER						---- */

.contentWrapper-SvZHNd,										/* picker				expression wrapper					*/
.emojiPicker-3PwZFl,										/* picker				inner								*/
.diversitySelectorPopout-3FiGaM {							/* picker				diversityselector					*/
	background: transparent;
	box-shadow: 0 2px 10px 0 rgba(var(--vtransparencycolor), 0.3);
	border: none;
	overflow: hidden;
}
.contentWrapper-SvZHNd::before,
.emojiPicker-3PwZFl::before,
.diversitySelectorPopout-3FiGaM::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--vpopout) var(--vpopoutposition)/var(--vpopoutsize);
	background-attachment: fixed;
	filter: blur(var(--vpopoutblur));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.contentWrapper-SvZHNd::after,
.emojiPicker-3PwZFl::after,
.diversitySelectorPopout-3FiGaM::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.25));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.diversitySelectorPopout-3FiGaM::after,
.diversitySelectorPopout-3FiGaM::before {
	border-radius: 5px;
}
.emojiPickerInExpressionPicker-3IzIcv .emojiPicker-3PwZFl {
	box-shadow: unset;
}
.emojiPickerInExpressionPicker-3IzIcv .emojiPicker-3PwZFl::after,
.emojiPickerInExpressionPicker-3IzIcv .emojiPicker-3PwZFl::before {
	display: none;
}

.diversityEmojiItem-L6_IXw:hover {							/* picker				diversityemoji						*/
	background-color: rgb(var(--vaccentcolor));
}

.navButton-2gQCx- {											/* picker				navbutton							*/
	color: rgb(var(--fontwhite3));
}
.navButtonActive-1MkytQ {									/* picker				navbuttonactive						*/
	background-color: rgb(var(--vaccentcolor));
	color: rgb(var(--fontwhite1));
}

.wrapper-2Gsate {											/* picker				sidebar								*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}

.guildIcon-3h-1IH {											/* picker				guildicon							*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}

.categoryItemDefaultCategory-aBZ6nJ:first-child,
.categoryItemDefaultCategory-aBZ6nJ:first-child + .categoryItemDefaultCategory-aBZ6nJ,
.stickerCategoryRecent-1WVWrj {
	margin-bottom: 8px;
}
.categoryItemDefaultCategory-aBZ6nJ:hover,					/* picker				categoryitem						*/
.stickerCategory-3Yz7vN:hover,								/* picker				stickercategoryitem					*/
.stickerCategoryShopWrapper-3EnJdQ:hover .stickerCategoryShop-d5zC3B {
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
.categoryItemDefaultCategorySelected-_HCKoz,				/* picker				categoryitem selected				*/
.categoryItemDefaultCategorySelected-_HCKoz:hover,		
.stickerCategorySelected-2uaMAG,							/* picker				stickercategoryitem selected		*/
.stickerCategorySelected-2uaMAG:hover {
	background-color: rgb(var(--vaccentcolor));
}
.categoryItemDefaultCategorySelected-_HCKoz svg,			/* picker				categoryitem selected				*/
.categoryItemDefaultCategorySelected-_HCKoz:hover svg,
.stickerCategorySelected-2uaMAG svg,						/* picker				stickercategoryitem selected		*/
.stickerCategorySelected-2uaMAG:hover svg {	
	filter: drop-shadow(1px 1px var(--vtextshadow));
}

.unicodeShortcut-15J8Ck,									/* picker				unicodeemojis shortcut				*/
.stickerCategoryShopWrapper-3EnJdQ {						/* picker				unicodeemojis shortcut				*/
	background-color: transparent;
	color: rgb(var(--fontwhite3));
	border: none;
	overflow: hidden;
	z-index: 100;
}
.unicodeShortcut-15J8Ck:hover {
	color: rgb(var(--fontwhite1));
}
.unicodeShortcut-15J8Ck::before,
.stickerCategoryShopWrapper-3EnJdQ::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--vpopout) var(--vpopoutposition)/var(--vpopoutsize);
	background-attachment: fixed;
	filter: blur(var(--vpopoutblur));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.unicodeShortcut-15J8Ck::after,
.stickerCategoryShopWrapper-3EnJdQ::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.35));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}

.inspector-S2gM3e {											/* picker				emojiinfowrapper					*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}

#app-mount .wrapper-1-Fsb8 {								/* picker				categoryheader						*/
	background: transparent;
	position: static;
}

#app-mount .imageLoading-bpSr0M {							/* picker				emoji loading						*/
	background: rgba(var(--vtransparencycolor), 0.3);
	border-radius: 10px;
}
.emojiItem-14v6tW.emojiItemSelected-1aLkfV {				/* picker				emoji selected						*/
	background-color: rgb(var(--vaccentcolor));
}
.emojiItemDisabled-1FvFuF {									/* picker				emoji disabled						*/
	filter: none;
	cursor: no-drop;
}
.emojiItemDisabled-1FvFuF > * {
	filter: grayscale(1);
}

.shape-2kfO2v {												/* picker				sticker loading						*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
.feature-3kpTdS {											/* picker				sticker feature						*/
	background: transparent;
	color: rgb(var(--fontwhite1));
}

.stickerInspected-2EM4w- .stickerBackground-2XECKi {		/* picker				sticker focused						*/
	background-color: rgb(var(--vaccentcolor));
}
.viewAllBackground-3Bn1vh {									/* picker				sticker view all					*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
.viewAll-2RLt-n:hover .viewAllBackground-3Bn1vh,
.viewAllInspected-FsmJHj .viewAllBackground-3Bn1vh {
	background-color: rgba(var(--vtransparencycolor), 0.4);
}

.premiumPromo-fVlLu- {										/* picker				premium warning						*/
	background-color: transparent;
	opacity: 1;
}
.premiumPromo-fVlLu-::before {
	content: "";
	opacity: 0.9;
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--vpopout) var(--vpopoutposition)/var(--vpopoutsize);
	background-attachment: fixed;
	filter: blur(var(--vpopoutblur));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.premiumPromo-fVlLu-::after {
	content: "";
	opacity: 0.9;
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.29));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}

#app-mount .backButton-JyKGC1 {								/* gifpicker			backbutton							*/
	color: rgb(var(--fontwhite3));
}
#app-mount .backButton-JyKGC1:hover {
	color: rgb(var(--fontwhite2));
}
#app-mount .focused-1En8bG,									/* gifpicker			result								*/
#app-mount .result-3w1ZcL:hover {
	box-shadow: 0 11px 22px 1px rgba(var(--vtransparencycolor), 0.3);
}
#app-mount .emptyHintCard-2mUdMe {
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
#app-mount .emptyHintText-1QDF9N {
	color: rgb(var(--fontwhite1));
}
#app-mount .endText-3SrwuD {
	color: rgb(var(--fontwhite3));
}
#app-mount .endContainer-1ZDW8j::after {
	background-image: url(https://discordapp.com/assets/0c735bf91232f2a2266e6ba9d6753565.svg);
	opacity: 0.6;
}


/* ----		14.4.	PINS/MENTIONS					---- */

.messagesPopoutWrap-1MQ1bW,								/* popout				wrapper								*/
.container-enaOkj {										/* popout				wrapper	(inbox)						*/
	background-color: transparent
	box-shadow: 0 2px 10px 0 rgba(var(--vtransparencycolor), 0.3);
	border: none;
	overflow: hidden;
}
.messagesPopoutWrap-1MQ1bW > *,
.container-enaOkj > * {
	z-index: 1000;
}
.messagesPopoutWrap-1MQ1bW::before,
.container-enaOkj::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--vpopout) var(--vpopoutposition)/var(--vpopoutsize);
	background-attachment: fixed;
	filter: blur(var(--vpopoutblur));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.messagesPopoutWrap-1MQ1bW::after,
.container-enaOkj::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.25));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
#app-mount .messagesPopout-24nkyi {							/* popout				innerwrap							*/
	background-color: transparent;
}

.themedPopout-1TrfdI .header-2Kf7Yu {
	box-shadow: 0 2px 3px 0 rgba(var(--vtransparencycolor), 0.1);
}
.header-ykumBX {											/* popout				header								*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
	box-shadow: 0 2px 3px 0 rgba(var(--vtransparencycolor), 0.2);
}
.header-ykumBX .title-3pkaKd {								/* popout				headertitle							*/
	color: rgb(var(--fontwhite1));
}

.themedPopout-1TrfdI .footer-1K57q_ {
	background-color: rgba(var(--vtransparencycolor), 0.1);
}
.footer-1kmXd4 {											/* popout				footer								*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}

.tutorial-i_drPV {											/* popout				tutorial							*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
.tutorialIcon-G9i5Ne {										/* popout				tutorial icon						*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
	color: rgb(var(--fontwhite1));
}

.messageGroupWrapper-o-Zw7G {
	background-color: transparent;
	border: none;
	overflow: visible;
	padding: 11px 10px 10px 10px;
}
.messageGroupWrapper-o-Zw7G + .messageGroupWrapper-o-Zw7G::before {
	content: "";
	border-top: 1px solid rgba(var(--fontwhite4), 0.3);
	position: absolute;
	top: -3px;
	left: 0;
	width: 100%;
}
.messageGroupWrapper-o-Zw7G .contentCozy-3XX413 {
	overflow: hidden;
}
.actionButtons-1sUUug {										/* popout				actionbuttonscontainer				*/
	top: 4px;
	right: 14px;
}
.jumpButton-2dvRSC,											/* popout				jumpbutton (mentions)				*/
.jumpButton-3DTcS_ {										/* popout				jumpbutton (pins)					*/
	background-color: rgba(var(--vtransparencycolor), 0.4);
	color: rgb(var(--fontwhite2));
}
.jumpButton-2dvRSC:hover,
.jumpButton-3DTcS_:hover {
	background-color: rgb(var(--vaccentcolor));
}
.jumpButton-2dvRSC:hover .text-3KVtey,
.jumpButton-3DTcS_:hover {
	color: rgb(var(--fontwhite1));
}
.jumpButton-2dvRSC + .jumpButton-2dvRSC,
.jumpButton-3DTcS_ + .jumpButton-3DTcS_ {
	margin-left: 2px;
}
.messageGroupWrapper-o-Zw7G:hover .actionButtons-1sUUug .closeButton-17RIVZ {
	opacity: 1;
}
.channelName-3kBz6H {										/* popout				dividerchannelname					*/
	color: rgb(var(--fontwhite1));
}
.guildName-1Bc3Ta {											/* popout				dividerguildname					*/
	color: rgb(var(--fontwhite2));
}
.hasMoreButton-1MELpI {										/* popout				hasmorebutton						*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
	border: none;
}

.emptyPlaceholder-1zh-Eu .body-bvcIjN {						/* popout				emptytext							*/
	color: rgb(var(--fontwhite3));
}
.image-2JDb81 {												/* popout				emptyimage							*/
	opacity: 0.6;
}

															/* popout				active tab							*/
#app-mount .header-2-Imhb .tabBar-1kuXvJ .tab-ck0077.active-1MbGPa {
	background-color: rgb(var(--vaccentcolor));
}
.secondary-dIudih,											/* popout				header button						*/
.tertiary-aMXF0g,											/* popout				message button						*/
.collapseButton-3V3Cqh {									/* popout				collapse button						*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
	color: rgb(var(--fontwhite3));
}
.secondary-dIudih:hover,
.tertiary-aMXF0g:hover,
.collapseButton-3V3Cqh:hover {
	background-color: rgba(var(--vtransparencycolor), 0.4);
	color: rgb(var(--fontwhite1));
}
.collapseButton-3V3Cqh {
	position: static;
	margin-left: 12px;
	border-radius: 32px;
	box-sizing: border-box;
	cursor: pointer;
	flex-shrink: 0;
	height: 32px;
	min-height: 32px;
	width: 32px;
	min-width: 32px;
	padding: 8px;
	transform: unset !important;
}
.collapseButton-3V3Cqh.collapsed-b6uSCG svg {
	transform: rotate(-90deg);
}

.channelHeader-3Gd2xq {										/* popout				channelheader						*/
	background-color: rgba(var(--vtransparencycolor), 0.4);
	padding-right: 16px;
	border-radius: 5px 5px 0 0;
	position: static;
}
.channelHeader-3Gd2xq:only-child {
	border-radius: 0;
}
.messageContainer-gbhlwo,									/* popout				messagecontainer					*/
.messages-3G3erD {											/* popout				messagecontainer (inbox)			*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
	border-radius: 0;
}
.messageContainer-gbhlwo:last-child,
.messages-3G3erD:last-child {
	border-radius: 0 0 5px 5px;
}

.tutorial-3w5I9h {											/* popout				tutorial (inbox)					*/
	background-color: rgba(var(--vtransparencycolor), 0.4);
}
.tutorialIcon-3f1miQ {										/* popout				tutorial (inbox)					*/
	background-color: rgba(var(--vtransparencycolor), 0.4);
	color: rgb(var(--fontwhite2));
}

.emptyStateIcon-3VCpT2 {									/* popout				no messages (inbox)					*/
	background-color: rgba(var(--vtransparencycolor), 0.4);
	color: rgb(var(--fontwhite2));
}

/* ----		14.5.	SEARCHPOPOUT					---- */

#app-mount .container-3ayLPN {								/* popout				wrapper								*/
	background-color: transparent;
	box-shadow: 0 2px 10px 0 rgba(var(--vtransparencycolor), 0.3);
	border: none;
	overflow: hidden;
	position: relative;
}
.container-3ayLPN::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--vpopout) var(--vpopoutposition)/var(--vpopoutsize);
	background-attachment: fixed;
	filter: blur(var(--vpopoutblur));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.container-3ayLPN::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.25));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
#app-mount .queryContainer-RKFJW- {
	color: rgb(var(--fontwhite3));
	border-bottom-color: rgba(var(--fontwhite4), 0.3);
}
#app-mount .queryContainer-RKFJW- strong {
	color: rgb(var(--fontwhite1));
}
#app-mount .focused-2bY0OD {
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
#app-mount .resultsGroup-r_nuzN::before {
	border-top-color: rgba(var(--fontwhite4), 0.3);
}
#app-mount .resultsGroup-r_nuzN .header-2N-gMV,
#app-mount .resultsGroup-r_nuzN .plusIcon-v0BTrL,
#app-mount .resultsGroup-r_nuzN .searchClearHistory-2cSSMO,
#app-mount .resultsGroup-r_nuzN .searchLearnMore-3SQUAj a {
	color: rgb(var(--fontwhite2));
}
#app-mount .option-96V44q::after {
	display: none;
}
#app-mount .option-96V44q.selected-rZcOL- {
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
#app-mount .option-96V44q.selected-rZcOL-::before {
	background-color: rgb(var(--vaccentcolor));
	border-radius: 3px;
	width: 34px;
}
#app-mount .option-96V44q .answer-1n6g43,
#app-mount .option-96V44q .nonText-3CRkO0,
#app-mount .option-96V44q strong {
	color: rgb(var(--fontwhite2));
}
#app-mount .option-96V44q .filter-3Y_im- {
	color: rgb(var(--fontwhite4));
}
#app-mount .option-96V44q.user-O3Czj0 .displayedNick-3xxvzU {
	color: rgb(var(--fontwhite2));
}
#app-mount .option-96V44q.user-O3Czj0 .displayUsername-Qekxml {
	color: rgb(var(--fontwhite3));
}
#app-mount .searchOption-zQ-1l6 .filter-3Y_im- {
	color: rgb(var(--fontwhite2));
}
#app-mount .searchOption-zQ-1l6 .answer-1n6g43 {
	color: rgb(var(--fontwhite4));
}
#app-mount .datePicker--XZbmJ .datePickerHint-3Q1Udw {
	border-top-color: rgba(var(--fontwhite4), 0.3);
}
#app-mount .datePicker--XZbmJ .datePickerHint-3Q1Udw .hint-165cR4 {
	color: rgb(var(--fontwhite2));
}
#app-mount .datePicker--XZbmJ .datePickerHint-3Q1Udw .hintValue-29ny8Z {
	color: rgb(var(--fontwhite1));
}
#app-mount .datePicker--XZbmJ .datePickerHint-3Q1Udw .hintValue-29ny8Z:hover {
	background-color: #677bc4;
}
#app-mount .searchResultChannelCategory-1l0lSn,
#app-mount .searchResultChannelIcon-1DnTme {
	color: rgb(var(--fontwhite4));
}

#app-mount .calendarPicker-2yf6Ci .react-datepicker {
	background: transparent;
}
#app-mount .datePicker--XZbmJ .react-datepicker__day:not(.react-datepicker__day--outside-month) {
	border-color: rgba(var(--vtransparencycolor), 0.5);
}
#app-mount .datePicker--XZbmJ .react-datepicker__day--outside-month {
	border-color: transparent;
	background: rgba(var(--vtransparencycolor), 0.5);
}
#app-mount .datePicker--XZbmJ .react-datepicker__header,
#app-mount .datePicker--XZbmJ .react-datepicker__month-container,
#app-mount .datePicker--XZbmJ .react-datepicker__day--disabled:not(.react-datepicker__day--outside-month) {
	background: rgba(var(--vtransparencycolor), 0.2);
}
#app-mount .datePicker--XZbmJ .react-datepicker__header {
	padding-bottom: 5px;
}
#app-mount .datePicker--XZbmJ .react-datepicker__navigation {
	background: transparent;
	border-color: rgba(var(--fontwhite1), 0.5);
	top: 30px;
}
#app-mount .datePicker--XZbmJ .react-datepicker__navigation::before {
	content: "";
	position: absolute;
	top: 0;
	right: 0;
	bottom: 0;
	left: 0;
	-webkit-mask: url(https://discordapp.com/assets/7619529e87dad31fd2ae83d9b9583e49.svg) center/6px 12px no-repeat;
	background-color: rgb(var(--fontwhite1));
}
#app-mount .datePicker--XZbmJ .react-datepicker__navigation--previous {
	left: 30px;
}
#app-mount .datePicker--XZbmJ .react-datepicker__navigation--next {
	right: 30px;
}
#app-mount .datePicker--XZbmJ .react-datepicker__current-month {
	border-color: transparent;
	padding: 10px 0;
}
#app-mount .datePicker--XZbmJ .react-datepicker__current-month,
#app-mount .datePicker--XZbmJ .react-datepicker__day-name,
#app-mount .datePicker--XZbmJ .react-datepicker__day:not(.react-datepicker__day--disabled):hover,
#app-mount .datePicker--XZbmJ .react-datepicker__day:not(.react-datepicker__day--disabled):not(.react-datepicker__day--outside-month),
#app-mount .datePicker--XZbmJ .datePickerHint-3Q1Udw .hint-165cR4,
#app-mount .datePicker--XZbmJ .datePickerHint-3Q1Udw .hintValue-29ny8Z {
	color: rgb(var(--fontwhite1));
}
#app-mount .datePicker--XZbmJ .react-datepicker__day--disabled:not(.react-datepicker__day--outside-month) {
	color: rgb(var(--fontwhite3));
}
#app-mount .datePicker--XZbmJ .react-datepicker__day--outside-month {
	color: rgb(var(--fontwhite4));
}
#app-mount .datePicker--XZbmJ .datePickerHint-3Q1Udw {
	margin: 0;
	padding: 20px;
	display: flex;
	justify-content: center;
}

/* ----		14.6.	COLORPICKER						---- */

#app-mount .colorPickerCustom-2CWBn2 {						/* popout				wrapper								*/
	background-color: transparent
	box-shadow: 0 0 0 1px rgba(var(--vtransparencycolor), 0.3), 0 2px 10px 0 rgba(var(--vtransparencycolor), 0.3);
	border: none;
	border-radius: 3px;
	overflow: hidden;
}
.colorPickerCustom-2CWBn2::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--vpopout) var(--vpopoutposition)/var(--vpopoutsize);
	background-attachment: fixed;
	filter: blur(var(--vpopoutblur));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.colorPickerCustom-2CWBn2::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.35));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
#app-mount .saturation-1FDvtn > div > div > div > div {							/* popout				saturationcursor					*/
	box-shadow: rgb(var(--fontwhite1)) 0px 0px 0px 1.5px, rgba(var(--vtransparencycolor), 0.6) 0px 0px 1px 1px inset, rgba(var(--vtransparencycolor), 0.6) 0px 0px 1px 2px !important;
}
#app-mount .hue-13HAGb > div > div > div > div,									/* popout				huecursor							*/
#app-mount .BDFDB-colorpicker .alpha-bar > div > div > div > div {				/* popout				alphacursor							*/
	background: rgb(var(--fontwhite1)) !important;
	box-shadow: rgba(var(--vtransparencycolor), 1) 0px 0px 2px !important;
}
#app-mount .BDFDB-colorpicker .gradient-button {								/* popout				gradientbutton						*/
	color: rgb(var(--fontwhite1));
}
#app-mount .BDFDB-colorpicker .gradient-bar .gradient-cursor > div {			/* popout				gradientcursor						*/
	border-color: rgb(var(--fontwhite4));
}
#app-mount .BDFDB-colorpicker .gradient-bar .gradient-cursor > div::before {		/* popout				gradientcursorpointer				*/
	border-top-color: rgb(var(--fontwhite4));
}
#app-mount .BDFDB-colorpicker .gradient-bar .gradient-cursor.selected > div {
	border-color: rgb(var(--fontwhite1));
}
#app-mount .BDFDB-colorpicker .gradient-bar .gradient-cursor.selected > div::before {
	border-top-color: rgb(var(--fontwhite1));
}

/* ----		14.7.	ADDROLE							---- */

#app-mount .container-VSDcQc {								/* popout				wrapper								*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--vtransparencycolor), 0.3), 0 2px 10px 0 rgba(var(--vtransparencycolor), 0.3);
	border: none;
	border-radius: 3px;
	overflow: hidden;
}
.container-VSDcQc::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--vpopout) var(--vpopoutposition)/var(--vpopoutsize);
	background-attachment: fixed;
	filter: blur(var(--vpopoutblur));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.container-VSDcQc::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.1));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
#app-mount .header-2bNvm4,
#app-mount .autocompleteHeaderBackground-30T70q {			/* popout				header								*/
	background: rgba(var(--vtransparencycolor), 0.3);
	border-radius: 5px 5px 0 0;
}
#app-mount .container-VSDcQc .headerText-3i6A8K {			/* popout				headertext							*/
	color: rgb(var(--fontwhite2));
}
#app-mount .container-VSDcQc .input-1ppKdn {				/* popout				headerinput							*/
	color: rgb(var(--fontwhite1));
}
#app-mount .container-VSDcQc .input-1ppKdn::placeholder {
	color: rgb(var(--fontwhite4));
}
#app-mount .autocompleteArrow-Zxoy9H {						/* popout				arrow								*/
	display: none;
}
#app-mount .autocompleteShadow-iiGWFU {						/* popout				shadow								*/
	box-shadow: 0 1px 5px 0 rgba(var(--vtransparencycolor), 0.3);
}
#app-mount .container-VSDcQc .sectionTag-pXyto9 {			/* popout				body								*/
	background: transparent;
	border-radius: 0 0 5px 5px;
	color: rgb(var(--fontwhite3));
}
.row-rrHHJU:focus .rowInner-1vvRiF,
.row-rrHHJU:hover .rowInner-1vvRiF {
	background: rgba(var(--vtransparencycolor), 0.2);
}
.row-rrHHJU.selected-1pIgLL .rowInner-1vvRiF {
	background: rgba(var(--vtransparencycolor), 0.4);
}


/* ----		14.8.	EVERYONEMENTION					---- */

#app-mount .everyonePopout-nEbJY3 {							/* popout				wrapper								*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--vtransparencycolor), 0.3), 0 2px 10px 0 rgba(var(--vtransparencycolor), 0.3);
	border: none;
	border-radius: 3px;
	overflow: hidden;
	position: relative;
}
.everyonePopout-nEbJY3::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--vpopout) var(--vpopoutposition)/var(--vpopoutsize);
	background-attachment: fixed;
	filter: blur(var(--vpopoutblur));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.everyonePopout-nEbJY3::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.1));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.everyonePopout-nEbJY3 .animation-3GofIz {
	opacity: 0.7;
}
#app-mount .header-3_S6dz {
	color: rgb(var(--fontwhite1));
}
#app-mount .buttonHint-2OxJB8 {
	color: rgb(var(--fontwhite3));
}
#app-mount .buttonHint-2OxJB8 strong {
	color: rgb(var(--fontwhite1));
}
#app-mount .footer-2aTx0s {
	background-color: rgba(var(--vtransparencycolor), 0.2);
	color: rgb(var(--fontwhite3));
}
#app-mount .footer-2aTx0s .icon-2qOzDL path {
	fill: rgb(var(--fontwhite3));
}


/* ----		14.9.	CHANNELFOLLOW					---- */

#app-mount .header-1pGpFt {
	background: rgba(var(--vtransparencycolor), 0.3);
}
#app-mount .separator-3gy7tq {
	box-shadow: 0 1px 0 0 rgba(var(--vtransparencycolor), 0.3), 0 1px 2px 0 rgba(var(--vtransparencycolor), 0.3);
}
.channelContainer-1x3D6I {
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
.channel-2PJTLY {
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
.channelContainer-1x3D6I .channel-2PJTLY {
	background-color: transparent;
}
.channelIcon-3ci4bV {
	color: rgb(var(--fontwhite3));
}

/* ----		14.10.	CHANNELFOLLOWINFO				---- */

#app-mount .guildPopout-3CgKqR {							/* popout				wrapper								*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--vtransparencycolor), 0.3), 0 2px 10px 0 rgba(var(--vtransparencycolor), 0.3);
	border: none;
	border-radius: 3px;
	overflow: hidden;
	position: relative;
}
.guildPopout-3CgKqR::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--vpopout) var(--vpopoutposition)/var(--vpopoutsize);
	background-attachment: fixed;
	filter: blur(var(--vpopoutblur));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.guildPopout-3CgKqR::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.1));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}

/* ----		14.11.	EMOJIINFO						---- */

#app-mount .popoutContainer-1MXdqN {						/* popout				wrapper								*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--vtransparencycolor), 0.3), 0 2px 10px 0 rgba(var(--vtransparencycolor), 0.3);
	border: none;
	border-radius: 3px;
	overflow: hidden;
	position: relative;
}
.popoutContainer-1MXdqN::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--vpopout) var(--vpopoutposition)/var(--vpopoutsize);
	background-attachment: fixed;
	filter: blur(var(--vpopoutblur));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.popoutContainer-1MXdqN::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.2));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}

.emojiSection-3Fb9ix {										/* popout				emojisection						*/
	background-color: transparent;
}

.guildSection-1EoFKd {										/* popout				emojisection						*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}

.loading-1lSwpg {											/* popout				loading placeholder					*/
	background: rgba(var(--vtransparencycolor), 0.3);
}

/* ----		14.12.	STREAMPREVIEW					---- */

#app-mount .streamPreview-2-WUWT {							/* popout				wrapper								*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--vtransparencycolor), 0.3), 0 2px 10px 0 rgba(var(--vtransparencycolor), 0.3);
	border: none;
	border-radius: 3px;
	overflow: hidden;
	position: relative;
}
.streamPreview-2-WUWT::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--vpopout) var(--vpopoutposition)/var(--vpopoutsize);
	background-attachment: fixed;
	filter: blur(var(--vpopoutblur));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.streamPreview-2-WUWT::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.2));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}

#app-mount .previewContainer-12UlHl	{						/* popout				preview								*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
}

/* ----		14.13.	PUBLICGUILDANNOUNCEMENT			---- */

#app-mount .popout-6p6fkZ {									/* popout				wrapper								*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--vtransparencycolor), 0.3), 0 2px 10px 0 rgba(var(--vtransparencycolor), 0.3);
	border: none;
	border-radius: 3px;
	overflow: hidden;
	position: relative;
}
.popout-6p6fkZ::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--vpopout) var(--vpopoutposition)/var(--vpopoutsize);
	background-attachment: fixed;
	filter: blur(var(--vpopoutblur));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.popout-6p6fkZ::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.2));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}


/* ~~~~		15.		GENERAL							~~~~ */

::-webkit-input-placeholder, body, button, input, select, textarea {
	font-family: var(--vfont);
}

::selection {												/* selection												*/
	background: rgb(var(--vaccentcolor));
}
.highlight {
	background: rgb(var(--vaccentcolor));
}

#app-mount .elevationLow-2lY09M, #app-mount .elevationLow-126AxN, .lightElevationLow-3_Ybxi, .darkElevationLow-DABD7i {
	box-shadow: 0 1px 5px 0 rgba(var(--vtransparencycolor), 0.3);
}
#app-mount .elevationHigh-3A9Xbf, #app-mount .elevationHigh-1PneE4, .lightElevationHigh-3usmGv, .darkElevationHigh-6iWpWi {
	box-shadow: 0 2px 10px 0 rgba(var(--vtransparencycolor), 0.3);
}
#app-mount .elevationBorderLow-2qgTRQ, #app-mount .elevationBorderLow-2_BGCd, .lightElevationBorderLow-3APXjz, .darkElevationBorderLow-39dDV7 {
	box-shadow: 0 0 0 1px rgba(var(--vtransparencycolor), 0.3), 0 1px 5px 0 rgba(var(--vtransparencycolor), 0.3);
}
#app-mount .elevationBorderHigh-2WYJ09, #app-mount .elevationBorderHigh-2_BGCd, .lightElevationBorderHigh-2T98IF, .darkElevationBorderHigh-2U1nXW {
	box-shadow: 0 0 0 1px rgba(var(--vtransparencycolor), 0.3), 0 2px 10px 0 rgba(var(--vtransparencycolor), 0.3);
}

.pointerEvents-2zdfdO[fill="#ffffff"] {						/* status				whitedot							*/
	fill: rgb(var(--fontwhite1));
}

.dots-3Bkt3k,												/* loading				3-dots								*/
.dots-3Bkt3k.themed-IQiCm3 {
	color: rgb(var(--fontwhite1));
}

/* ----		15.1.	TEXT							---- */

.username-3gJmXY {
	color: rgb(var(--fontwhite1));
}
.discriminator-uTZ08z {
	color: rgb(var(--fontwhite3));
}
.h5-18_1nd {
	color: rgb(var(--fontwhite3));
}
.white-1VR_aZ,
.white-3xi-nx {
	color: rgb(var(--fontwhite1));
}
#app-mount h1.title-3KTIjF,
#app-mount h2.title-3KTIjF {
	color: rgb(var(--fontwhite1));
}
#app-mount h3.title-3KTIjF {
	color: rgb(var(--fontwhite2));
}
#app-mount h4.title-3KTIjF,
#app-mount h5.title-3KTIjF,
#app-mount h6.title-3KTIjF {
	color: rgb(var(--fontwhite3));
}
#app-mount .coloredText-1kAd0O {
	color: rgb(var(--fontwhite1));
}
#app-mount .defaultColor-1_ajX0 {
	color: rgb(var(--fontwhite1));
}

/* ----		15.2.	BUTTONS							---- */

.searchSuggestion-2K8OBX:hover,
.form-236Xmo .btnPrimary-346kfV,
.button-22FETM,
.questionMark-CWEQZn,
.questionMark-3qBhGj,
.btn-1PnLxm.btnPrimary-1jluZW,
.btn-15Au6M.btnPrimary-ggBniE,
.bd-modal-wrapper .footer button,
.bd-pfbtn,
.bda-settings-button,
.btn-primary,
.platform-iik236.active-iLSdWQ .downloadButton-1bWXpg,
.action-1lSjCi.create-3jownz .actionButton-2PeQbJ,
.ui-button.brand.filled,
.lookFilled-1Gx00P.hoverBrand-1_Fxlk.hasHover-3X1-zV:hover,
.lookFilled-1Gx00P.colorBrand-3pXr91:not(.buttonColor-7qQbGO):not([style*="background-color"]) {
	text-shadow: 1px 1px var(--vtextshadow);
}
.lookFilled-1Gx00P.hoverBrand-1_Fxlk.hasHover-3X1-zV:hover svg,
.lookFilled-1Gx00P.colorBrand-3pXr91:not(.buttonColor-7qQbGO):not([style*="background-color"]) svg {
	filter: drop-shadow(1px 1px var(--vtextshadow));
}

.lookFilled-1Gx00P:not(.colorWhite-rEQuAQ) .spinnerItem-3GlVyU {
	background-color: rgb(var(--fontwhite1)) !important;
}
.lookFilled-1Gx00P:not(.colorWhite-rEQuAQ) {
	color: rgb(var(--fontwhite1)) !important;
}
.lookInverted-2D7oAl:not(.colorWhite-rEQuAQ):hover {
	background: rgb(var(--fontwhite1)) linear-gradient(0deg,rgba(0,0,0,.1),rgba(0,0,0,.1)) !important;
}
.lookInverted-2D7oAl:not(.colorWhite-rEQuAQ):active {
	background: rgb(var(--fontwhite1)) linear-gradient(0deg,rgba(0,0,0,.2),rgba(0,0,0,.2)) !important;
}
.lookInverted-2D7oAl:not(.colorWhite-rEQuAQ),
.lookInverted-2D7oAl:not(.colorWhite-rEQuAQ):disabled {
	background: rgb(var(--fontwhite1)) !important;
}
.theme-light .lookFilled-1Gx00P:not(.colorWhite-rEQuAQ).hasHover-3X1-zV:hover,
.theme-dark .lookFilled-1Gx00P:not(.colorWhite-rEQuAQ).hasHover-3X1-zV:hover,
.theme-light .lookFilled-1Gx00P:not(.colorWhite-rEQuAQ).hasHover-3X1-zV:active,
.theme-dark .lookFilled-1Gx00P:not(.colorWhite-rEQuAQ).hasHover-3X1-zV:active {
	color: rgb(var(--fontwhite1)) !important;
}
.theme-light .lookInverted-2D7oAl:not(.colorWhite-rEQuAQ).hasHover-3X1-zV:hover,
.theme-dark .lookInverted-2D7oAl:not(.colorWhite-rEQuAQ).hasHover-3X1-zV:hover {
	background-color: rgb(var(--fontwhite2)) !important;
}
.theme-light .lookInverted-2D7oAl:not(.colorWhite-rEQuAQ).hasHover-3X1-zV:active,
.theme-dark .lookInverted-2D7oAl:not(.colorWhite-rEQuAQ).hasHover-3X1-zV:active {
	background-color: rgb(var(--fontwhite3)) !important;
}


.lookFilled-1Gx00P.colorWhite-rEQuAQ .spinnerItem-3GlVyU {
	background-color: rgb(var(--vtransparencycolor));
}
.lookInverted-2D7oAl.colorWhite-rEQuAQ .spinnerItem-3GlVyU,
.lookOutlined-3sRXeN.colorWhite-rEQuAQ .spinnerItem-3GlVyU,
.lookGhost-2Fn_0-.colorWhite-rEQuAQ .spinnerItem-3GlVyU,
.lookLink-9FtZy-.colorWhite-rEQuAQ .spinnerItem-3GlVyU {
	background-color: rgb(var(--fontwhite1));
}
.lookFilled-1Gx00P.colorWhite-rEQuAQ {
	color: rgb(var(--vtransparencycolor));
}
.lookFilled-1Gx00P.colorWhite-rEQuAQ:hover,
.theme-light .lookFilled-1Gx00P.hoverWhite-2uUmXw.hasHover-3X1-zV:hover,
.theme-dark .lookFilled-1Gx00P.hoverWhite-2uUmXw.hasHover-3X1-zV:hover {
	background: rgb(var(--fontwhite1)) linear-gradient(0deg,rgba(0,0,0,.1),rgba(0,0,0,.1)) !important;
}
.lookFilled-1Gx00P.colorWhite-rEQuAQ:active,
.theme-light .lookFilled-1Gx00P.hoverWhite-2uUmXw.hasHover-3X1-zV:active,
.theme-dark .lookFilled-1Gx00P.hoverWhite-2uUmXw.hasHover-3X1-zV:active {
	background: rgb(var(--fontwhite1)) linear-gradient(0deg,rgba(0,0,0,.2),rgba(0,0,0,.2)) !important;
}
.lookFilled-1Gx00P.colorWhite-rEQuAQ,
.lookFilled-1Gx00P.colorWhite-rEQuAQ:disabled {
	background: rgb(var(--fontwhite1));
}
.lookInverted-2D7oAl.colorWhite-rEQuAQ:hover,
.theme-light .lookInverted-2D7oAl.hoverWhite-2uUmXw.hasHover-3X1-zV:hover,
.theme-dark .lookInverted-2D7oAl.hoverWhite-2uUmXw.hasHover-3X1-zV:hover {
	background: rgb(var(--vtransparencycolor)) linear-gradient(0deg,rgba(255,255,255,.1),rgba(255,255,255,.1));
	color: rgb(var(--fontwhite2));
}
.lookInverted-2D7oAl.colorWhite-rEQuAQ:active,
.theme-light .lookInverted-2D7oAl.hoverWhite-2uUmXw.hasHover-3X1-zV:active,
.theme-dark .lookInverted-2D7oAl.hoverWhite-2uUmXw.hasHover-3X1-zV:active {
	background: rgb(var(--vtransparencycolor)) linear-gradient(0deg,rgba(255,255,255,.2),rgba(255,255,255,.2));
	color: rgb(var(--fontwhite3));
}
.lookInverted-2D7oAl.colorWhite-rEQuAQ,
.lookInverted-2D7oAl.colorWhite-rEQuAQ:disabled {
	background-color: rgb(var(--vtransparencycolor));
	color: rgb(var(--fontwhite1));
}
.lookOutlined-3sRXeN.colorWhite-rEQuAQ {
	border-color: rgba(var(--fontwhite1), 0.3);
	color: rgb(var(--fontwhite1));
}
.lookOutlined-3sRXeN.colorWhite-rEQuAQ:hover,
.theme-light .lookOutlined-3sRXeN.hoverWhite-2uUmXw.hasHover-3X1-zV:hover,
.theme-dark .lookOutlined-3sRXeN.hoverWhite-2uUmXw.hasHover-3X1-zV:hover {
	border-color: rgba(var(--fontwhite1), 0.6);
	color: rgb(var(--fontwhite1));
}
.lookOutlined-3sRXeN.colorWhite-rEQuAQ:active,
.theme-light .lookOutlined-3sRXeN.hoverWhite-2uUmXw.hasHover-3X1-zV:hover,
.theme-dark .lookOutlined-3sRXeN.hoverWhite-2uUmXw.hasHover-3X1-zV:hover {
	background-color: rgba(var(--fontwhite1), 0.1);
	border-color: rgb(var(--fontwhite1));
	color: rgb(var(--fontwhite1));
}
.lookOutlined-3sRXeN.colorWhite-rEQuAQ:disabled {
	border-color: rgba(var(--fontwhite1), 0.3);
}
.lookGhost-2Fn_0-.colorWhite-rEQuAQ {
	background-color: rgba(var(--fontwhite1), 0.1);
	color: rgb(var(--fontwhite1));
}
.lookGhost-2Fn_0-.colorWhite-rEQuAQ:hover {
	color: rgb(var(--fontwhite1));
	background-color: rgba(var(--fontwhite1), 0.15);
}
.lookGhost-2Fn_0-.colorWhite-rEQuAQ:active,
.theme-light .lookGhost-2Fn_0-.hoverWhite-2uUmXw.hasHover-3X1-zV:active,
.theme-dark .lookGhost-2Fn_0-.hoverWhite-2uUmXw.hasHover-3X1-zV:active {
	background-color: rgba(var(--fontwhite1), 0.2);
	color: rgb(var(--fontwhite1));
}
.lookGhost-2Fn_0-.colorWhite-rEQuAQ:disabled {
	background-color: rgba(var(--fontwhite1), 0.1);
}
#app-mount .backButtonColor-1zIPlh,
#app-mount .backButtonColor-N09dXJ,
.lookLink-9FtZy-.colorWhite-rEQuAQ {
	color: rgb(var(--fontwhite1));
}
#app-mount .backButtonColor-1zIPlh:hover .contents-18-Yxp,
#app-mount .backButtonColor-N09dXJ:hover .contents-18-Yxp,
.lookLink-9FtZy-.colorWhite-rEQuAQ:hover .contents-18-Yxp,
.theme-light .lookLink-9FtZy-.hoverWhite-2uUmXw.hasHover-3X1-zV:hover .contents-18-Yxp,
.theme-dark .lookLink-9FtZy-.hoverWhite-2uUmXw.hasHover-3X1-zV:hover .contents-18-Yxp {
	color: rgb(var(--fontwhite1));
	background-image: linear-gradient(0deg, transparent, transparent 1px, rgb(var(--fontwhite1)) 0, rgb(var(--fontwhite1)) 2px, transparent 0);
}

.lookInverted-2D7oAl.colorBlack-1jwPVL .spinnerItem-3GlVyU,
.lookOutlined-3sRXeN.colorBlack-1jwPVL .spinnerItem-3GlVyU,
.lookGhost-2Fn_0-.colorBlack-1jwPVL .spinnerItem-3GlVyU,
.lookLink-9FtZy-.colorBlack-1jwPVL .spinnerItem-3GlVyU {
	background-color: rgb(var(--vtransparencycolor));
}
.lookFilled-1Gx00P.colorBlack-1jwPVL:hover,
.theme-light .lookFilled-1Gx00P.hoverBlack-3jULb8.hasHover-3X1-zV:hover,
.theme-dark .lookFilled-1Gx00P.hoverBlack-3jULb8.hasHover-3X1-zV:hover {
	background: rgb(var(--vtransparencycolor)) linear-gradient(0deg,rgba(255,255,255,.1),rgba(255,255,255,.1));
}
.lookFilled-1Gx00P.colorBlack-1jwPVL:active,
.theme-light .lookFilled-1Gx00P.hoverBlack-3jULb8.hasHover-3X1-zV:active,
.theme-dark .lookFilled-1Gx00P.hoverBlack-3jULb8.hasHover-3X1-zV:active {
	background: rgb(var(--vtransparencycolor)) linear-gradient(0deg,rgba(255,255,255,.2),rgba(255,255,255,.2));
}
.lookFilled-1Gx00P.colorBlack-1jwPVL,
.lookFilled-1Gx00P.colorBlack-1jwPVL:disabled {
	background: rgb(var(--vtransparencycolor));
}
.theme-light .lookInverted-2D7oAl.hoverBlack-3jULb8.hasHover-3X1-zV:hover,
.theme-dark .lookInverted-2D7oAl.hoverBlack-3jULb8.hasHover-3X1-zV:hover,
.theme-light .lookInverted-2D7oAl.hoverBlack-3jULb8.hasHover-3X1-zV:active,
.theme-dark .lookInverted-2D7oAl.hoverBlack-3jULb8.hasHover-3X1-zV:active {
	color: rgb(var(--vtransparencycolor));
}
.lookInverted-2D7oAl.colorBlack-1jwPVL,
.lookInverted-2D7oAl.colorBlack-1jwPVL:disabled {
	color: rgb(var(--vtransparencycolor));
}
.lookOutlined-3sRXeN.colorBlack-1jwPVL:hover,
.theme-light .lookOutlined-3sRXeN.hoverBlack-3jULb8.hasHover-3X1-zV:hover,
.theme-dark .lookOutlined-3sRXeN.hoverBlack-3jULb8.hasHover-3X1-zV:hover {
	border-color: rgba(var(--vtransparencycolor), 0.6);
	color: rgb(var(--vtransparencycolor));
}
.lookOutlined-3sRXeN.colorBlack-1jwPVL:active,
.theme-light .lookOutlined-3sRXeN.hoverBlack-3jULb8.hasHover-3X1-zV:active,
.theme-dark .lookOutlined-3sRXeN.hoverBlack-3jULb8.hasHover-3X1-zV:active {
	background-color: rgba(var(--vtransparencycolor), 0.1);
	border-color: rgb(var(--vtransparencycolor));
	color: rgb(var(--vtransparencycolor));
}
.lookOutlined-3sRXeN.colorBlack-1jwPVL,
.lookOutlined-3sRXeN.colorBlack-1jwPVL:disabled {
	border-color: rgba(var(--vtransparencycolor), 0.3);
}
.lookGhost-2Fn_0-.colorBlack-1jwPVL:active,
.theme-light .lookGhost-2Fn_0-.hoverBlack-3jULb8.hasHover-3X1-zV:active,
.theme-dark .lookGhost-2Fn_0-.hoverBlack-3jULb8.hasHover-3X1-zV:active {
	background-color: rgba(var(--vtransparencycolor), 0.2);
	color: rgb(var(--vtransparencycolor));
}
.lookGhost-2Fn_0-.colorBlack-1jwPVL,
.lookGhost-2Fn_0-.colorBlack-1jwPVL:disabled {
	background-color: rgba(var(--vtransparencycolor), 0.1);
}
.lookLink-9FtZy-.colorBlack-1jwPVL {
	color: rgb(var(--vtransparencycolor));
}
.lookLink-9FtZy-.colorBlack-1jwPVL:hover .contents-18-Yxp,
.theme-light .lookLink-9FtZy-.hoverBlack-3jULb8.hasHover-3X1-zV:hover .contents-18-Yxp,
.theme-dark .lookLink-9FtZy-.hoverBlack-3jULb8.hasHover-3X1-zV:hover .contents-18-Yxp {
	background-image: linear-gradient(0deg, transparent, transparent 1px, rgb(var(--vtransparencycolor)) 0, rgb(var(--vtransparencycolor)) 2px, transparent 0);
	color: rgb(var(--vtransparencycolor));
}

.theme-light .lookInverted-2D7oAl.colorGrey-2DXtkV .spinnerItem-3GlVyU,
.theme-dark .lookInverted-2D7oAl.colorGrey-2DXtkV .spinnerItem-3GlVyU,
.theme-light .lookOutlined-3sRXeN.colorGrey-2DXtkV .spinnerItem-3GlVyU,
.theme-dark .lookOutlined-3sRXeN.colorGrey-2DXtkV .spinnerItem-3GlVyU,
.theme-light .lookGhost-2Fn_0-.colorGrey-2DXtkV .spinnerItem-3GlVyU,
.theme-dark .lookGhost-2Fn_0-.colorGrey-2DXtkV .spinnerItem-3GlVyU,
.theme-light .lookLink-9FtZy-.colorGrey-2DXtkV .spinnerItem-3GlVyU,
.theme-dark .lookLink-9FtZy-.colorGrey-2DXtkV .spinnerItem-3GlVyU {
	background-color: rgb(var(--fontwhite4));
}

.buttonColor-1agP3J:hover,
.theme-light .lookFilled-1Gx00P.colorGrey-2DXtkV:hover,
.theme-dark .lookFilled-1Gx00P.colorGrey-2DXtkV:hover,
.theme-light .lookFilled-1Gx00P.hoverGrey-2CBXu0.hasHover-3X1-zV:hover,
.theme-dark .lookFilled-1Gx00P.hoverGrey-2CBXu0.hasHover-3X1-zV:hover {
	background: rgb(var(--fontwhite4)) linear-gradient(0deg,rgba(0,0,0,.1),rgba(0,0,0,.1));
}
.buttonColor-1agP3J:active,
.theme-light .lookFilled-1Gx00P.colorGrey-2DXtkV:active,
.theme-dark .lookFilled-1Gx00P.colorGrey-2DXtkV:active,
.theme-light .lookFilled-1Gx00P.hoverGrey-2CBXu0.hasHover-3X1-zV:active,
.theme-dark .lookFilled-1Gx00P.hoverGrey-2CBXu0.hasHover-3X1-zV:active {
	background: rgb(var(--fontwhite4)) linear-gradient(0deg,rgba(0,0,0,.2),rgba(0,0,0,.2));
}
.buttonColor-1agP3J,
.theme-light .lookFilled-1Gx00P.colorGrey-2DXtkV,
.theme-dark .lookFilled-1Gx00P.colorGrey-2DXtkV,
.theme-light .lookFilled-1Gx00P.colorGrey-2DXtkV:disabled,
.theme-dark .lookFilled-1Gx00P.colorGrey-2DXtkV:disabled {
	background: rgb(var(--fontwhite4));
}
.theme-light .lookInverted-2D7oAl.hoverGrey-2CBXu0.hasHover-3X1-zV:hover,
.theme-dark .lookInverted-2D7oAl.hoverGrey-2CBXu0.hasHover-3X1-zV:hover,
.theme-light .lookInverted-2D7oAl.hoverGrey-2CBXu0.hasHover-3X1-zV:active,
.theme-dark .lookInverted-2D7oAl.hoverGrey-2CBXu0.hasHover-3X1-zV:active {
	color: rgb(var(--fontwhite4));
}
.theme-light .lookInverted-2D7oAl.colorGrey-2DXtkV,
.theme-dark .lookInverted-2D7oAl.colorGrey-2DXtkV,
.theme-light .lookInverted-2D7oAl.colorGrey-2DXtkV:disabled,
.theme-dark .lookInverted-2D7oAl.colorGrey-2DXtkV:disabled {
	color: rgb(var(--fontwhite4));
}
.theme-light .lookOutlined-3sRXeN.colorGrey-2DXtkV:hover,
.theme-dark .lookOutlined-3sRXeN.colorGrey-2DXtkV:hover,
.theme-light .lookOutlined-3sRXeN.hoverGrey-2CBXu0.hasHover-3X1-zV:hover,
.theme-dark .lookOutlined-3sRXeN.hoverGrey-2CBXu0.hasHover-3X1-zV:hover {
	border-color: rgba(var(--fontwhite4), 0.6);
	color: rgb(var(--fontwhite4));
}
.theme-light .lookOutlined-3sRXeN.colorGrey-2DXtkV:active,
.theme-dark .lookOutlined-3sRXeN.colorGrey-2DXtkV:active,
.theme-light .lookOutlined-3sRXeN.hoverGrey-2CBXu0.hasHover-3X1-zV:active,
.theme-dark .lookOutlined-3sRXeN.hoverGrey-2CBXu0.hasHover-3X1-zV:active {
	background-color: rgba(var(--fontwhite4), 0.1);
	border-color: rgb(var(--fontwhite4));
	color: rgb(var(--fontwhite4));
}
.theme-light .lookOutlined-3sRXeN.colorGrey-2DXtkV,
.theme-dark .lookOutlined-3sRXeN.colorGrey-2DXtkV,
.theme-light .lookOutlined-3sRXeN.colorGrey-2DXtkV:disabled,
.theme-dark .lookOutlined-3sRXeN.colorGrey-2DXtkV:disabled {
	border-color: rgba(var(--fontwhite4), 0.3);
	color: rgb(var(--fontwhite4));
}
.theme-light .lookGhost-2Fn_0-.colorGrey-2DXtkV:active,
.theme-dark .lookGhost-2Fn_0-.colorGrey-2DXtkV:active,
.theme-light .lookGhost-2Fn_0-.hoverGrey-2CBXu0.hasHover-3X1-zV:active,
.theme-dark .lookGhost-2Fn_0-.hoverGrey-2CBXu0.hasHover-3X1-zV:active {
	background-color: rgba(var(--fontwhite4), 0.2);
}
.theme-light .lookGhost-2Fn_0-.colorGrey-2DXtkV,
.theme-dark .lookGhost-2Fn_0-.colorGrey-2DXtkV,
.theme-light .lookGhost-2Fn_0-.colorGrey-2DXtkV:disabled,
.theme-dark .lookGhost-2Fn_0-.colorGrey-2DXtkV:disabled {
	background-color: rgba(var(--fontwhite4), 0.1);
	color: rgb(var(--fontwhite4));
}
.theme-light .lookLink-9FtZy-.colorGrey-2DXtkV,
.theme-dark .lookLink-9FtZy-.colorGrey-2DXtkV {
	color: rgb(var(--fontwhite4));
}
.theme-light .lookLink-9FtZy-.colorGrey-2DXtkV:hover .contents-18-Yxp,
.theme-dark .lookLink-9FtZy-.colorGrey-2DXtkV:hover .contents-18-Yxp,
.theme-light .lookLink-9FtZy-.hoverGrey-2CBXu0.hasHover-3X1-zV:hover .contents-18-Yxp,
.theme-dark .lookLink-9FtZy-.hoverGrey-2CBXu0.hasHover-3X1-zV:hover .contents-18-Yxp {
	color: rgb(var(--fontwhite4));
	background-image: linear-gradient(0deg, transparent, transparent 1px, rgb(var(--fontwhite4)) 0, rgb(var(--fontwhite4)) 2px, transparent 0);
}

.theme-light .lookInverted-2D7oAl.colorPrimary-3b3xI6 .spinnerItem-3GlVyU,
.theme-dark .lookInverted-2D7oAl.colorPrimary-3b3xI6 .spinnerItem-3GlVyU,
.theme-light .lookOutlined-3sRXeN.colorPrimary-3b3xI6 .spinnerItem-3GlVyU,
.theme-dark .lookOutlined-3sRXeN.colorPrimary-3b3xI6 .spinnerItem-3GlVyU,
.theme-light .lookGhost-2Fn_0-.colorPrimary-3b3xI6 .spinnerItem-3GlVyU,
.theme-dark .lookGhost-2Fn_0-.colorPrimary-3b3xI6 .spinnerItem-3GlVyU,
.theme-light .lookLink-9FtZy-.colorPrimary-3b3xI6 .spinnerItem-3GlVyU,
.theme-dark .lookLink-9FtZy-.colorPrimary-3b3xI6 .spinnerItem-3GlVyU {
	background-color: rgb(var(--fontwhite3));
}
.theme-light .lookFilled-1Gx00P.colorPrimary-3b3xI6:hover,
.theme-dark .lookFilled-1Gx00P.colorPrimary-3b3xI6:hover,
.theme-light .lookFilled-1Gx00P.hoverPrimary-2D1j2r.hasHover-3X1-zV:hover,
.theme-dark .lookFilled-1Gx00P.hoverPrimary-2D1j2r.hasHover-3X1-zV:hover {
	background: rgb(var(--fontwhite3)) linear-gradient(0deg,rgba(0,0,0,.1),rgba(0,0,0,.1));
}
.theme-light .lookFilled-1Gx00P.colorPrimary-3b3xI6:active,
.theme-dark .lookFilled-1Gx00P.colorPrimary-3b3xI6:active,
.theme-light .lookFilled-1Gx00P.hoverPrimary-2D1j2r.hasHover-3X1-zV:active,
.theme-dark .lookFilled-1Gx00P.hoverPrimary-2D1j2r.hasHover-3X1-zV:active {
	background: rgb(var(--fontwhite3)) linear-gradient(0deg,rgba(0,0,0,.2),rgba(0,0,0,.2));
}
.theme-light .lookFilled-1Gx00P.colorPrimary-3b3xI6,
.theme-dark .lookFilled-1Gx00P.colorPrimary-3b3xI6,
.theme-light .lookFilled-1Gx00P.colorPrimary-3b3xI6:disabled,
.theme-dark .lookFilled-1Gx00P.colorPrimary-3b3xI6:disabled {
	background: rgb(var(--fontwhite3));
}
.theme-light .lookInverted-2D7oAl.hoverPrimary-2D1j2r.hasHover-3X1-zV:hover,
.theme-dark .lookInverted-2D7oAl.hoverPrimary-2D1j2r.hasHover-3X1-zV:hover,
.theme-light .lookInverted-2D7oAl.hoverPrimary-2D1j2r.hasHover-3X1-zV:active,
.theme-dark .lookInverted-2D7oAl.hoverPrimary-2D1j2r.hasHover-3X1-zV:active {
	color: rgb(var(--fontwhite3));
}
.theme-light .lookInverted-2D7oAl.colorPrimary-3b3xI6,
.theme-dark .lookInverted-2D7oAl.colorPrimary-3b3xI6,
.theme-light .lookInverted-2D7oAl.colorPrimary-3b3xI6:disabled,
.theme-dark .lookInverted-2D7oAl.colorPrimary-3b3xI6:disabled {
	color: rgb(var(--fontwhite3));
}
.theme-light .lookOutlined-3sRXeN.colorPrimary-3b3xI6:hover,
.theme-dark .lookOutlined-3sRXeN.colorPrimary-3b3xI6:hover,
.theme-light .lookOutlined-3sRXeN.hoverPrimary-2D1j2r.hasHover-3X1-zV:hover,
.theme-dark .lookOutlined-3sRXeN.hoverPrimary-2D1j2r.hasHover-3X1-zV:hover {
	border-color: rgba(var(--fontwhite3), 0.6);
	color: rgb(var(--fontwhite3));
}
.theme-light .lookOutlined-3sRXeN.colorPrimary-3b3xI6:active,
.theme-dark .lookOutlined-3sRXeN.colorPrimary-3b3xI6:active,
.theme-light .lookOutlined-3sRXeN.hoverPrimary-2D1j2r.hasHover-3X1-zV:active,
.theme-dark .lookOutlined-3sRXeN.hoverPrimary-2D1j2r.hasHover-3X1-zV:active {
	background-color: rgba(var(--fontwhite3), 0.1);
	border-color: rgb(var(--fontwhite3));
	color: rgb(var(--fontwhite3));
}
.theme-light .lookOutlined-3sRXeN.colorPrimary-3b3xI6,
.theme-dark .lookOutlined-3sRXeN.colorPrimary-3b3xI6,
.theme-light .lookOutlined-3sRXeN.colorPrimary-3b3xI6:disabled,
.theme-dark .lookOutlined-3sRXeN.colorPrimary-3b3xI6:disabled {
	border-color: rgba(var(--fontwhite3), 0.3);
	color: rgb(var(--fontwhite3));
}
.theme-light .lookGhost-2Fn_0-.colorPrimary-3b3xI6:active,
.theme-dark .lookGhost-2Fn_0-.colorPrimary-3b3xI6:active,
.theme-light .lookGhost-2Fn_0-.hoverPrimary-2D1j2r.hasHover-3X1-zV:active,
.theme-dark .lookGhost-2Fn_0-.hoverPrimary-2D1j2r.hasHover-3X1-zV:active {
	background-color: rgba(var(--fontwhite3), 0.2);
}
.theme-light .lookGhost-2Fn_0-.colorPrimary-3b3xI6,
.theme-dark .lookGhost-2Fn_0-.colorPrimary-3b3xI6,
.theme-light .lookGhost-2Fn_0-.colorPrimary-3b3xI6:disabled,
.theme-dark .lookGhost-2Fn_0-.colorPrimary-3b3xI6:disabled {
	background-color: rgba(var(--fontwhite3), 0.1);
	color: rgb(var(--fontwhite3));
}
.theme-light .lookLink-9FtZy-.colorPrimary-3b3xI6,
.theme-dark .lookLink-9FtZy-.colorPrimary-3b3xI6 {
	color: rgb(var(--fontwhite3));
}
.theme-light .lookLink-9FtZy-.colorPrimary-3b3xI6:hover .contents-18-Yxp,
.theme-dark .lookLink-9FtZy-.colorPrimary-3b3xI6:hover .contents-18-Yxp,
.theme-light .lookLink-9FtZy-.hoverPrimary-2D1j2r.hasHover-3X1-zV:hover .contents-18-Yxp,
.theme-dark .lookLink-9FtZy-.hoverPrimary-2D1j2r.hasHover-3X1-zV:hover .contents-18-Yxp {
	color: rgb(var(--fontwhite3));
	background-image: linear-gradient(0deg, transparent, transparent 1px, rgb(var(--fontwhite3)) 0, rgb(var(--fontwhite3)) 2px, transparent 0);
}

.theme-light .lookInverted-2D7oAl.colorTransparent-1ewNp9 .spinnerItem-3GlVyU,
.theme-dark .lookInverted-2D7oAl.colorTransparent-1ewNp9 .spinnerItem-3GlVyU {
	background-color: rgba(var(--fontwhite1), 0.1);
}
.theme-light .lookOutlined-3sRXeN.colorTransparent-1ewNp9 .spinnerItem-3GlVyU,
.theme-dark .lookOutlined-3sRXeN.colorTransparent-1ewNp9 .spinnerItem-3GlVyU,
.theme-light .lookGhost-2Fn_0-.colorTransparent-1ewNp9 .spinnerItem-3GlVyU,
.theme-dark .lookGhost-2Fn_0-.colorTransparent-1ewNp9 .spinnerItem-3GlVyU,
.theme-light .lookLink-9FtZy-.colorTransparent-1ewNp9 .spinnerItem-3GlVyU,
.theme-dark .lookLink-9FtZy-.colorTransparent-1ewNp9 .spinnerItem-3GlVyU {
	background-color: rgb(var(--fontwhite2));
}
.theme-light .lookFilled-1Gx00P.colorTransparent-1ewNp9:hover,
.theme-dark .lookFilled-1Gx00P.colorTransparent-1ewNp9:hover,
.theme-light .lookFilled-1Gx00P.hoverTransparent-2Lz5CN.hasHover-3X1-zV:hover,
.theme-dark .lookFilled-1Gx00P.hoverTransparent-2Lz5CN.hasHover-3X1-zV:hover {
	background-color: rgba(var(--fontwhite1), 0.05);
	color: rgb(var(--fontwhite1));
}
.theme-light .lookFilled-1Gx00P.colorTransparent-1ewNp9:active,
.theme-dark .lookFilled-1Gx00P.colorTransparent-1ewNp9:active,
.theme-light .lookFilled-1Gx00P.hoverTransparent-2Lz5CN.hasHover-3X1-zV:active,
.theme-dark .lookFilled-1Gx00P.hoverTransparent-2Lz5CN.hasHover-3X1-zV:active {
	background-color: rgba(var(--fontwhite1), 0.01);
	color: rgb(var(--fontwhite1));
}
.theme-light .lookFilled-1Gx00P.colorTransparent-1ewNp9,
.theme-dark .lookFilled-1Gx00P.colorTransparent-1ewNp9,
.theme-light .lookFilled-1Gx00P.colorTransparent-1ewNp9:disabled,
.theme-dark .lookFilled-1Gx00P.colorTransparent-1ewNp9:disabled {
	background-color: rgba(var(--fontwhite1), 0.1);
}
.theme-light .lookInverted-2D7oAl.colorTransparent-1ewNp9:hover,
.theme-dark .lookInverted-2D7oAl.colorTransparent-1ewNp9:hover,
.theme-light .lookInverted-2D7oAl.hoverTransparent-2Lz5CN.hasHover-3X1-zV:hover,
.theme-dark .lookInverted-2D7oAl.hoverTransparent-2Lz5CN.hasHover-3X1-zV:hover {
	background-color: rgba(var(--fontwhite1), 0.05);
	color: rgba(var(--fontwhite1), 0.1);
}
.theme-light .lookInverted-2D7oAl.colorTransparent-1ewNp9:active,
.theme-dark .lookInverted-2D7oAl.colorTransparent-1ewNp9:active,
.theme-light .lookInverted-2D7oAl.hoverTransparent-2Lz5CN.hasHover-3X1-zV:active,
.theme-dark .lookInverted-2D7oAl.hoverTransparent-2Lz5CN.hasHover-3X1-zV:active {
	background-color: rgba(var(--fontwhite1), 0.1);
	color: rgba(var(--fontwhite1), 0.1);
}
.theme-light .lookInverted-2D7oAl.colorTransparent-1ewNp9,
.theme-dark .lookInverted-2D7oAl.colorTransparent-1ewNp9,
.theme-light .lookInverted-2D7oAl.colorTransparent-1ewNp9:disabled,
.theme-dark .lookInverted-2D7oAl.colorTransparent-1ewNp9:disabled {
	background-color: rgb(var(--fontwhite1));
	color: rgba(var(--fontwhite1), 0.1);
}
.theme-light .lookOutlined-3sRXeN.colorTransparent-1ewNp9:hover,
.theme-dark .lookOutlined-3sRXeN.colorTransparent-1ewNp9:hover,
.theme-light .lookOutlined-3sRXeN.hoverTransparent-2Lz5CN.hasHover-3X1-zV:hover,
.theme-dark .lookOutlined-3sRXeN.hoverTransparent-2Lz5CN.hasHover-3X1-zV:hover {
	border-color: rgba(var(--fontwhite2), 0.6);
	color: rgb(var(--fontwhite2));
}
.theme-light .lookOutlined-3sRXeN.colorTransparent-1ewNp9:active,
.theme-dark .lookOutlined-3sRXeN.colorTransparent-1ewNp9:active,
.theme-light .lookOutlined-3sRXeN.hoverTransparent-2Lz5CN.hasHover-3X1-zV:active,
.theme-dark .lookOutlined-3sRXeN.hoverTransparent-2Lz5CN.hasHover-3X1-zV:active {
	background-color: rgba(var(--fontwhite2), 0.1);
	border-color: rgb(var(--fontwhite2));
	color: rgb(var(--fontwhite2));
}
.theme-light .lookOutlined-3sRXeN.colorTransparent-1ewNp9,
.theme-dark .lookOutlined-3sRXeN.colorTransparent-1ewNp9,
.theme-light .lookOutlined-3sRXeN.colorTransparent-1ewNp9:disabled,
.theme-dark .lookOutlined-3sRXeN.colorTransparent-1ewNp9:disabled {
	border-color: rgba(var(--fontwhite2), 0.3);
	color: rgb(var(--fontwhite2));
}
.theme-light .lookGhost-2Fn_0-.colorTransparent-1ewNp9:active,
.theme-dark .lookGhost-2Fn_0-.colorTransparent-1ewNp9:active,
.theme-light .lookGhost-2Fn_0-.hoverTransparent-2Lz5CN.hasHover-3X1-zV:active,
.theme-dark .lookGhost-2Fn_0-.hoverTransparent-2Lz5CN.hasHover-3X1-zV:active {
	background-color: rgba(var(--fontwhite2), 0.2);
	color: rgb(var(--fontwhite2));
}
.theme-light .lookGhost-2Fn_0-.colorTransparent-1ewNp9,
.theme-dark .lookGhost-2Fn_0-.colorTransparent-1ewNp9,
.theme-light .lookGhost-2Fn_0-.colorTransparent-1ewNp9:disabled,
.theme-dark .lookGhost-2Fn_0-.colorTransparent-1ewNp9:disabled {
	background-color: rgba(var(--fontwhite2), 0.1);
	color: rgb(var(--fontwhite2));
}
.theme-light .lookLink-9FtZy-.colorTransparent-1ewNp9,
.theme-dark .lookLink-9FtZy-.colorTransparent-1ewNp9 {
	color: rgb(var(--fontwhite2));
}
.theme-light .lookLink-9FtZy-.colorTransparent-1ewNp9:hover .contents-18-Yxp,
.theme-dark .lookLink-9FtZy-.colorTransparent-1ewNp9:hover .contents-18-Yxp,
.theme-light .lookLink-9FtZy-.hoverTransparent-2Lz5CN.hasHover-3X1-zV:hover .contents-18-Yxp,
.theme-dark .lookLink-9FtZy-.hoverTransparent-2Lz5CN.hasHover-3X1-zV:hover .contents-18-Yxp {
	background-image: linear-gradient(0deg, transparent, transparent 1px, rgb(var(--fontwhite2)) 0, rgb(var(--fontwhite2)) 2px, transparent 0);
	color: rgb(var(--fontwhite2));
}

/* ----		15.3.	INPUTS							---- */

.input-cIJ7To {												/* valueinput			bordered							*/
	background-color: rgba(var(--vtransparencycolor), 0.1);
	border-color: rgba(var(--vtransparencycolor), 0.3);
	color: rgb(var(--fontwhite1));
}
.input-cIJ7To:hover:not(:focus) {
	border-color: rgb(var(--vtransparencycolor));
}
.input-cIJ7To::placeholder {
	color: rgb(var(--fontwhite3));
}
#app-mount .input-1mgnkM,									/* valueinput			underlined							*/
#app-mount .input-UJ9Tr3 {
	border-color: rgba(var(--fontwhite1), 0.3);
	color: rgb(var(--fontwhite1));
}
#app-mount .input-1mgnkM:hover,
#app-mount .input-UJ9Tr3:hover {
	border-color: rgb(var(--fontwhite1));
}
#app-mount .input-1mgnkM:focus,
#app-mount .input-UJ9Tr3:focus {
	border-color: rgb(var(--vaccentcolor));
}
#app-mount .input-1mgnkM::placeholder,
#app-mount .input-UJ9Tr3::placeholder {
	color: rgb(var(--fontwhite3));
}
#app-mount .copyInput-2rOSt7 {
	background-color: rgba(var(--vtransparencycolor), 0.1);
}
#app-mount .copyInputDefault-21sXtF {
	border-color: rgba(var(--vtransparencycolor), 0.3);
}
#app-mount .hiddenMessage-1iiFV5,
#app-mount .inputDefault-A2ud2y {
	color: rgb(var(--fontwhite1));
}
#app-mount .inputDefault-A2ud2y::placeholder {
	color: rgb(var(--fontwhite3));
}
#app-mount .multiInputLast-1aQ3YA::before {
	border-color: rgb(var(--fontwhite1));
}
#app-mount .inputPrefix-2VAOGg {
	color: rgb(var(--fontwhite1));
	opacity: 0.3;
}
.maxLength-39QFBo {
	color: rgb(var(--fontwhite3));
}
#app-mount .inputNumberWrapper .numberinput-button-up {
	border-bottom-color: rgb(var(--fontwhite3));
}
#app-mount .inputNumberWrapper .numberinput-button-up:hover {
	border-bottom-color: rgb(var(--fontwhite1));
}
#app-mount .inputNumberWrapper .numberinput-button-down {
	border-top-color: rgb(var(--fontwhite3));
}
#app-mount .inputNumberWrapper .numberinput-button-down:hover {
	border-top-color: rgb(var(--fontwhite1));
}

#app-mount .container-3auIfb {								/* checkboxswitch											*/
	background-color: rgba(var(--vtransparencycolor), 0.3) !important;
}
#app-mount .container-3auIfb[style*="background-color: rgb(67, 181, 129)"],
#app-mount .container-3auIfb[style*="background-color: rgb(114, 137, 218)"] {
	background-color: rgba(var(--vaccentcolor), 0.8) !important;
}
#app-mount .container-3auIfb[style*="background-color: rgb(67, 181, 129)"]:hover,
#app-mount .container-3auIfb[style*="background-color: rgb(114, 137, 218)"]:hover {
	background: var(--vaccentcolor-hover);
}
#app-mount .container-3auIfb[style*="background-color: rgb(67, 181, 129)"]:active,
#app-mount .container-3auIfb[style*="background-color: rgb(114, 137, 218)"]:active {
	background: var(--vaccentcolor-active);
}
#app-mount .container-3auIfb rect[fill] {
	fill: rgb(var(--fontwhite1)) !important;
}
#app-mount .container-3auIfb path[fill] {
	fill: rgb(var(--vtransparencycolor)) !important;
}
#app-mount .container-3auIfb[style*="background-color: rgb(67, 181, 129)"] path[fill],
#app-mount .container-3auIfb[style*="background-color: rgb(114, 137, 218)"] path[fill] {
	fill: rgb(var(--vaccentcolor)) !important;
}

#app-mount .item-26Dhrx {									/* radiogroup			container							*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
	color: rgb(var(--fontwhite3));
}
#app-mount .item-26Dhrx:hover {
	background-color: rgba(var(--vtransparencycolor), 0.4);
	color: rgb(var(--fontwhite2));
}
#app-mount .item-26Dhrx[aria-checked=true] .radioBar-bMNUI- {
	background: rgb(var(--vaccentcolor));
	color: rgb(var(--fontwhite1));
}
#app-mount .item-26Dhrx[aria-checked=true] .radioBar-bMNUI- .radioIconForeground-XwlXQN {
	color: rgb(var(--fontwhite1));
}
#app-mount .item-26Dhrx .radioBar-bMNUI-[style*="--radio-bar-accent-color"] {
	background: var(--radio-bar-accent-color);
	border: unset;
	color: rgb(var(--fontwhite1));
}
#app-mount .item-26Dhrx[aria-checked=false]:hover .radioBar-bMNUI-[style*="--radio-bar-accent-color"] {
	background: var(--radio-bar-accent-color) linear-gradient(to right, rgba(255, 255, 255, 0.2), rgba(255, 255, 255, 0.2));
}

#app-mount .checkboxContainer-2vV9zd::before {				/* checkbox				container							*/
	background-color: rgba(var(--fontwhite4), 0.3);
}
#app-mount .checkbox-1ix_J3 {								/* checkbox				inner								*/
	border-color: rgb(var(--fontwhite3));
}
#app-mount .checked-3_4uQ9 {								/* checkbox				checked								*/
	background-color: rgb(var(--fontwhite1));
	border-color: rgb(var(--fontwhite1));
}
#app-mount .checked-3_4uQ9.round-2jCFai,					/* checkbox				roundchecked						*/
#app-mount .checked-3_4uQ9[style*="border-color: rgb(79, 84, 92)"] {
	background-color: rgb(var(--vaccentcolor)) !important;
	border-color: rgb(var(--vaccentcolor)) !important;
}
#app-mount .checked-3_4uQ9.round-2jCFai svg,
#app-mount .checked-3_4uQ9[style*="border-color: rgb(79, 84, 92)"] svg,
#app-mount .checked-3_4uQ9[style*="background-color: rgb(114, 137, 218)"] svg {
	filter: drop-shadow(1px 1px var(--vtextshadow));
}
#app-mount .checked-3_4uQ9 polyline[stroke="#43b581"],		/* checkbox				checkmark							*/
#app-mount .checked-3_4uQ9 polyline[stroke="#4f545c"],
#app-mount .checked-3_4uQ9 polyline[stroke="#ffffff"] {
	stroke: rgb(var(--fontwhite1));
}
.checkboxMute-14hTGS::before {
	background-color: rgba(var(--vtransparencycolor), 0.2);
}

#app-mount .bar-2Qqk5Z {									/* slider				backgroundbar						*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
.grabber-3mFHz2 {											/* slider				grabber								*/
	background-color: rgb(var(--fontwhite1));
	border-color: rgb(var(--fontwhite1));
	box-shadow: 0 3px 1px 0 rgba(var(--vtransparencycolor), 0.05), 0 2px 2px 0 rgba(var(--vtransparencycolor), 0.1), 0 3px 3px 0 rgba(var(--vtransparencycolor), 0.05);
}
#app-mount .markValue-2DwdXI {								/* slider				markvalue							*/
	color: rgb(var(--fontwhite3));
}
#app-mount .defaultValue-3gC7yw .markValue-2DwdXI {
	color: #43b581;
}
#app-mount .markDash-3hAolZ {
	background: transparent;
	color: rgba(var(--vtransparencycolor), 0.3);
}
#app-mount .defaultValue-3gC7yw .markDash-3hAolZ {
	color: #43b581;
}
#app-mount .markDash-3hAolZ::before,
#app-mount .markDash-3hAolZ::after {
	content: "";
	position: absolute;
	background: currentColor;
	height: 8px;
	width: 2px;
}
#app-mount .markDash-3hAolZ::before {
	top: 14px;
}
#app-mount .markDash-3hAolZ::after {
	top: 30px;
}
#app-mount .fontScaleLarge-3xtq7i,
#app-mount .fontScaleSmall-368quy {
	color: rgb(var(--fontwhite1));
}
#app-mount .bubble-3we2di {									/* slider				bubble								*/
	background-color: rgb(var(--vaccentcolor));
	color: rgb(var(--fontwhite1));
}
#app-mount .bubble-3we2di::before {
	border-top-color: rgb(var(--vaccentcolor));
}

#app-mount .container-1nZlH6 {								/* hotkeyinput			container							*/
	background-color: rgba(var(--vtransparencycolor), 0.1);
	border-color: rgba(var(--vtransparencycolor), 0.3);
}
.input-1UhAnY {												/* hotkeyinput			input								*/
	color: rgb(var(--fontwhite1));
}
.input-1UhAnY::placeholder {
	color: rgb(var(--fontwhite3));
}
#app-mount .editIcon-13gaox {								/* hotkeyinput			editicon							*/
	-webkit-mask: url(https://discordapp.com/assets/860396b3ff3fa1c4ae355bebfabadecb.svg) center/cover no-repeat;
	background: rgb(var(--fontwhite1));
}
#app-mount .container-CpszHS.recording-1H2dS7 .button-34kXw5 {
	color: #f04747;
	background-color: rgba(240,71,71,.1);
}

#app-mount .quickSelect-3BxO0K {							/* quickselect			container							*/
	color: rgb(var(--fontwhite1));
}
#app-mount .quickSelectLabel-2r3iJ_ {						/* quickselect			label								*/
	color: rgb(var(--fontwhite3));
}
#app-mount .quickSelectArrow-1QublR {						/* quickselect			arrow								*/
	-webkit-mask: url(https://discordapp.com/assets/f58cf3b8fc79e9d671ab649ab37651a9.svg) 50% no-repeat;
	background: rgb(var(--fontwhite1));
}

.select-2TCrqx [class*="css-"][class*="-container"] {		/* select				container							*/
	background-color: transparent;
}
#app-mount .lookFilled-1h1y05.select-1Pkeg4,
.select-2TCrqx [class*="css-"][class*="-control"] {
	background-color: rgba(var(--vtransparencycolor), 0.1);
	border-color: rgba(var(--vtransparencycolor), 0.3);
}
#app-mount .lookFilled-1h1y05.select-1Pkeg4:hover.selectOpen-hQuR6b,
#app-mount .lookFilled-1h1y05.selectOpen-hQuR6b {
	border-color: rgb(var(--vtransparencycolor)) rgb(var(--vtransparencycolor)) rgba(var(--vtransparencycolor), 0.3);
}
#app-mount .select-1Pkeg4,
#app-mount .lookFilled-1h1y05 .arrow-2KJjTM,
.select-2TCrqx [class*="css-"][class*="-singleValue"],
.select-2TCrqx [class*="css-"][class*="-placeholder"],
.select-2TCrqx [class*="css-"][class*="-indicatorContainer"] {
	color: rgb(var(--fontwhite1));
}
#app-mount .optionNormal-12VR9V,
.css-1gfjib6-option,
.css-1yz4bi9-option,
.css-ru8b0x-option,
.css-1yz4bi9-option {
	background-color: rgba(var(--vtransparencycolor), 0.1);
	color: rgb(var(--fontwhite2));
}
#app-mount .optionNormal-12VR9V:hover,
.css-pkcurw-option,
.css-rzbxvl-option,
.css-1qxn4c5-option,
.css-rzbxvl-option {
	background-color: rgba(var(--vtransparencycolor), 0.3);
	color: rgb(var(--fontwhite2));
}
#app-mount .optionActive-KkAdqq,
.css-1gxgi19-option,
.css-1ba14n5-option,
.css-6qzljd-option,
.css-1ba14n5-option {
	background-color: rgba(var(--vtransparencycolor), 0.5);
	color: rgb(var(--fontwhite1));
}
.role-3ulsK-:hover {
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
#app-mount .popout-2sKjHu,
.container-3LUQwT,
.select-2TCrqx > [class*="css-"][class*="-container"] > [class*="css-"][class*="-menu"] {
	background-color: transparent;
	border: 1px solid rgba(var(--vtransparencycolor), 0.3);
	box-shadow: 0px 1px 5px 0px rgba(var(--vtransparencycolor), 0.3);
	overflow: hidden;
}
#app-mount .popout-2sKjHu::before,
.container-3LUQwT::before,
.select-2TCrqx > [class*="css-"][class*="-container"] > [class*="css-"][class*="-menu"]::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--vpopout) var(--vpopoutposition)/var(--vpopoutsize);
	background-attachment: fixed;
	filter: blur(var(--vpopoutblur));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
#app-mount .popout-2sKjHu::after,
.container-3LUQwT::after,
.select-2TCrqx > [class*="css-"][class*="-container"] > [class*="css-"][class*="-menu"]::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.2));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}


/* ----		15.4.	SEARCHBARS						---- */

.container-2XeR5Z,											/* searchbar			inner								*/
.container-cMG81i {
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
.input-1Rv96N,												/* searchbar			input								*/
.input-3Xdcic {
	color: rgb(var(--fontwhite1));
}
.input-1Rv96N::placeholder,
.input-3Xdcic::placeholder,
#app-mount .searchBox-3Y2Vi7 .searchBoxInput-uJtBcv::placeholder {
	color: rgb(var(--fontwhite3));
}
.icon-3cZ1F_,												/* searchbar			icon								*/
.icon-1S6UIr,
#app-mount .clearIcon-2N9YIn,
#app-mount .searchIcon-1a1-yA,
#app-mount .searchIcon-32i2pb {
	color: rgb(var(--fontwhite3));
}
.clear-1pMieT .icon-3cZ1F_,
.icon-1S6UIr.clear--Eywng,
#app-mount .clearIcon-xXwSFS,
#app-mount .clear-U3WkKp .clearIcon-2N9YIn,
#app-mount .clear-U3WkKp .searchIcon-1a1-yA,
#app-mount .clear-U3WkKp .searchIcon-32i2pb {
	color: rgb(var(--fontwhite2));
}
.clear-1pMieT.iconLayout-1WxHy4:hover .icon-3cZ1F_,
.iconLayout-3OgqU3:hover .icon-1S6UIr.clear--Eywng,
#app-mount .clearIcon-xXwSFS:hover,
#app-mount .clear-U3WkKp:hover .clearIcon-2N9YIn,
#app-mount .clear-U3WkKp:hover .searchIcon-1a1-yA,
#app-mount .clear-U3WkKp:hover .searchIcon-32i2pb {
	color: rgb(var(--fontwhite1));
}

#app-mount .searchBox-3Y2Vi7 {
	background-color: rgba(var(--vtransparencycolor), 0.3);
	box-shadow: 0 2px 5px 0 rgba(var(--vtransparencycolor), 0.2);
}

/* ----		15.5.	TAGS							---- */

.botTagRegular-2HEhHi {										/* bottag				regular								*/
	color: rgb(var(--fontwhite1));
}
.botTagRegular-2HEhHi:not([style]) {						/* bottag				regular								*/
	text-shadow: 1px 1px var(--vtextshadow);
}
.botTagRegular-2HEhHi:not([style]) svg {
	filter: drop-shadow(1px 1px var(--vtextshadow));
}
.botTagInvert-18-95s {										/* bottag				inverted							*/
	background-color: rgb(var(--fontwhite1));
}

.iconBadge-2wi9r4 {											/* iconbadge												*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
.base-PmTxvP {												/* mentionbadge												*/
	color: rgb(var(--fontwhite1));
}

.disableColor-MwOAZf,										/* nitrobadge			flower							*/
.iconBackgroundTierNone-3MPhMJ,
.iconBackgroundTierOne-2LhaMB,
.iconBackgroundTierThree-3qw3JX,
.iconBackgroundTierTwo-3bCmdc {
	color: rgb(var(--fontwhite4));
}
.bannerVisible-2ZE_qG .iconBackgroundTierOne-2LhaMB,		/* nitrobadge			icon							*/
.bannerVisible-2ZE_qG .iconBackgroundTierThree-3qw3JX,
.bannerVisible-2ZE_qG .iconBackgroundTierTwo-3bCmdc,
.iconTierOne-BHC2T8, .iconTierTwo-_1edeM {
	color: rgb(var(--fontwhite1));
}
.flowerStarContainer-3zDVtj path[fill="#4f545c"] {			/* flowerbadge			flower							*/
	fill: rgb(var(--fontwhite4));
}
.flowerStarContainer-3zDVtj path[fill="#ffffff"] {			/* flowerbadge			icon							*/
	fill: rgb(var(--fontwhite1));
}
.icon-1ihkOt {												/* flowerbadge			icon							*/
	color: rgb(var(--fontwhite1));
}

/* ----		15.6.	ICONS							---- */

.emptySearchImage-1qOMLW,									/* empty search												*/
.image-1GzsFd {												/* no peoples/webhooks/etc.									*/
	opacity: 0.6;
}

.gameIcon-gg34Dz {											/* gameicon				unknowngame							*/
	color: rgb(var(--fontwhite1));
}

#app-mount .invalidPoop-pnUbq7 {							/* erroricon			invalidpoop							*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
	opacity: 0.7;
}
#app-mount .guildIconExpired-2Qcq05 {						/* erroricon			expiredguild						*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
	opacity: 0.7;
}

img[src="/assets/4c1bab3f945269a5c1be0b3a2c177141.png"],	/* connectionicon		twitch								*/
img[src="/assets/402008166e5ef53b0045b10930b263b0.png"] {
	-webkit-mask: url(https://discordapp.com/assets/4c1bab3f945269a5c1be0b3a2c177141.png) center/contain no-repeat;
	background: rgb(var(--fontwhite1));
	object-position: -9999999px -9999999px;
}
img[src="/assets/0ef81742942677bcef0bebdfb7061d29.png"],	/* connectionicon		youtube								*/
img[src="/assets/3f8d3e1dd3c9426ac7e680dada39650e.png"] {
	-webkit-mask: url(https://discordapp.com/assets/0ef81742942677bcef0bebdfb7061d29.png) center/contain no-repeat;
	background: rgb(var(--fontwhite1));
	object-position: -9999999px -9999999px;
}
img[src="/assets/3a257c4cab129e956b05bd50047eb0f9.png"],	/* connectionicon		battlenet							*/
img[src="/assets/cf74f0c780cba6ae11728b8ca740b30c.png"] {
	-webkit-mask: url(https://discordapp.com/assets/3a257c4cab129e956b05bd50047eb0f9.png) center/contain no-repeat;
	background: rgb(var(--fontwhite1));
	object-position: -9999999px -9999999px;
}
img[src="/assets/de5fb9e860729912c65048c1c657e1a3.png"],	/* connectionicon		skype								*/
img[src="/assets/1c419ecaf6e5406addbae729c7fa2e75.png"] {
	-webkit-mask: url(https://discordapp.com/assets/de5fb9e860729912c65048c1c657e1a3.png) center/contain no-repeat;
	background: rgb(var(--fontwhite1));
	object-position: -9999999px -9999999px;
}
img[src="/assets/fbbd224a0d94747c102515090682bbe1.png"],	/* connectionicon		LoL									*/
img[src="/assets/f87228c98e49168b6cf7ad38651b4e87.png"] {
	-webkit-mask: url(https://discordapp.com/assets/fbbd224a0d94747c102515090682bbe1.png) center/contain no-repeat;
	background: rgb(var(--fontwhite1));
	object-position: -9999999px -9999999px;
}
img[src="/assets/baf4bdd36b7ef74e8f34b402e66f81f4.png"],	/* connectionicon		steam								*/
img[src="/assets/6ca4a49418715a16e226be1280494f46.png"] {
	-webkit-mask: url(https://discordapp.com/assets/baf4bdd36b7ef74e8f34b402e66f81f4.png) center/contain no-repeat;
	background: rgb(var(--fontwhite1));
	object-position: -9999999px -9999999px;
}
img[src="/assets/bcc7bc0c0b27f9cbadaa1a47ea79db22.png"],	/* connectionicon		reddit								*/
img[src="/assets/51edbb92b1904c19197eb16be97bc6fb.png"] {
	-webkit-mask: url(https://discordapp.com/assets/bcc7bc0c0b27f9cbadaa1a47ea79db22.png) center/contain no-repeat;
	background: rgb(var(--fontwhite1));
	object-position: -9999999px -9999999px;
}
img[src="/assets/c926e69c482dac25b8e940db74496813.png"],	/* connectionicon		facebook							*/
img[src="/assets/27fb89c30127405c6a5370b477590da6.png"] {
	-webkit-mask: url(https://discordapp.com/assets/c926e69c482dac25b8e940db74496813.png) center/contain no-repeat;
	background: rgb(var(--fontwhite1));
	object-position: -9999999px -9999999px;
}
img[src="/assets/2ac50d286a1c883f28b5149239a8ad36.png"],	/* connectionicon		twitter								*/
img[src="/assets/c38327e52d3a859d550af398edb8d8e0.png"] {
	-webkit-mask: url(https://discordapp.com/assets/2ac50d286a1c883f28b5149239a8ad36.png) center/contain no-repeat;
	background: rgb(var(--fontwhite1));
	object-position: -9999999px -9999999px;
}
img[src="/assets/fe3770614c2658a07dea3ecb286ce745.png"],	/* connectionicon		spotify								*/
img[src="/assets/739cb09703de9dcfe68d0200a163d9fc.png"] {
	-webkit-mask: url(https://discordapp.com/assets/fe3770614c2658a07dea3ecb286ce745.png) center/contain no-repeat;
	background: rgb(var(--fontwhite1));
	object-position: -9999999px -9999999px;
}
img[src="/assets/850ed4fcf5839b7a32651f5959e8511e.png"],	/* connectionicon		xbox								*/
img[src="/assets/4c59c8e37dda86294d3cf237b2695dde.png"] {
	-webkit-mask: url(https://discordapp.com/assets/850ed4fcf5839b7a32651f5959e8511e.png) center/contain no-repeat;
	background: rgb(var(--fontwhite1));
	object-position: -9999999px -9999999px;
}

img[src="/assets/e8b66317ab0dc9ba3bf8d41a4f3ec914.png"] {	/* videosettings		opus								*/
	-webkit-mask: url(https://discordapp.com/assets/e8b66317ab0dc9ba3bf8d41a4f3ec914.png) center/contain no-repeat;
	background: rgb(var(--fontwhite2));
	object-position: -9999999px -9999999px;
}

.container-q03LZO:not(.colored-1armap) .profileBadgeStaff-3BXdTO {
	background: rgb(var(--fontwhite1));
	-webkit-mask: url(https://discordapp.com/assets/7cfd90c8062139e4804a1fa59f564731.svg) center/contain no-repeat;
}
.container-q03LZO:not(.colored-1armap) .profileBadgePartner-j6Lwhr {
	background: rgb(var(--fontwhite1));
	-webkit-mask: url(https://discordapp.com/assets/a0e288a458c48dfcf548dadc277e42e6.svg) center/contain no-repeat;
}
.container-q03LZO:not(.colored-1armap) .profileBadgeHypesquad-12E2P6 {
	background: rgb(var(--fontwhite1));
	-webkit-mask: url(https://discordapp.com/assets/3a050fcc884255231b99b7033c776070.svg) center/contain no-repeat;
}
.container-q03LZO:not(.colored-1armap) .profileBadgeHypeSquadOnlineHouse1-3rBtjf {
	background: rgb(var(--fontwhite1));
	-webkit-mask: url(https://discordapp.com/assets/1115767aed344e96a27a12e97718c171.svg) center/contain no-repeat;
}
.container-q03LZO:not(.colored-1armap) .profileBadgeHypeSquadOnlineHouse2-2oU04B {
	background: rgb(var(--fontwhite1));
	-webkit-mask: url(https://discordapp.com/assets/d3478c6bd5cee0fc600e55935ddc81aa.svg) center/contain no-repeat;
}
.container-q03LZO:not(.colored-1armap) .profileBadgeHypeSquadOnlineHouse3-1DoJkv {
	background: rgb(var(--fontwhite1));
	-webkit-mask: url(https://discordapp.com/assets/2a085ed9c86f3613935a6a8667ba8b89.svg) center/contain no-repeat;
}
.container-q03LZO:not(.colored-1armap) .profileBadgeHypeSquadOnlineHouse1Winner-3wCl80 {
	background: rgb(var(--fontwhite1));
	-webkit-mask: url(https://discordapp.com/assets/75f75c3142b8d44ea7052c2bcb9a9043.svg) center/contain no-repeat;
}
.container-q03LZO:not(.colored-1armap) .profileBadgeHypeSquadOnlineHouse2Winner-AS5bXe {
	background: rgb(var(--fontwhite1));
	-webkit-mask: url(https://discordapp.com/assets/d4a8fe68fc5f40c8a778f858881a7b84.svg) center/contain no-repeat;
}
.container-q03LZO:not(.colored-1armap) .profileBadgeHypeSquadOnlineHouse3Winner-2CwwQi {
	background: rgb(var(--fontwhite1));
	-webkit-mask: url(https://discordapp.com/assets/5dc48a7859a00e7d95ad8382156aab84.svg) center/contain no-repeat;
}
.container-q03LZO:not(.colored-1armap) .profileBadgeEarlySupporter-2ng_jL {
	background: rgb(var(--fontwhite1));
	-webkit-mask: url(https://discordapp.com/assets/ce15562552e3d70c56d5408cfeed2ffd.svg) center/contain no-repeat;
}
.container-q03LZO:not(.colored-1armap) .profileBadgePremium-1KDZYC {
	background: rgb(var(--fontwhite1));
	-webkit-mask: url(https://discordapp.com/assets/379d2b3171722ef8be494231234da5d1.svg) center/contain no-repeat;
}
.container-q03LZO:not(.colored-1armap) .profileBadgeVerifiedDeveloper-195KfD {
	background: rgb(var(--fontwhite1));
	-webkit-mask: url(https://discordapp.com/assets/785d81fdbedd133e213da693aba98774.svg) center/contain no-repeat;
}
.container-q03LZO:not(.colored-1armap) .profileBadgeBugHunterLevel1-dbEzVz {
	background: rgb(var(--fontwhite1));
	-webkit-mask: url(https://discordapp.com/assets/df26f079738a4dcd07cbce6eb3c957f1.svg) center/contain no-repeat;
}
.container-q03LZO:not(.colored-1armap) .profileBadgeBugHunterLevel2-3TUciC {
	background: rgb(var(--fontwhite1));
	-webkit-mask: url(https://discordapp.com/assets/16def052b03d75dac0ed9234c5d6a880.svg) center/contain no-repeat;
}
.container-q03LZO:not(.colored-1armap) .profileGuildSubscriberlvl1-3oI9tx {
	background: rgb(var(--fontwhite1));
	-webkit-mask: url(https://discordapp.com/assets/24e49184598820f274e62293349a2e43.svg) center/contain no-repeat;
}
.container-q03LZO:not(.colored-1armap) .profileGuildSubscriberlvl2-r6nJHT {
	background: rgb(var(--fontwhite1));
	-webkit-mask: url(https://discordapp.com/assets/cc73fba5c2e9b70752bbd1db35a1b9c3.svg) center/contain no-repeat;
}
.container-q03LZO:not(.colored-1armap) .profileGuildSubscriberlvl3-38s3Dj {
	background: rgb(var(--fontwhite1));
	-webkit-mask: url(https://discordapp.com/assets/a4c3939a9b03274246df9b144fcd86cf.svg) center/contain no-repeat;
}
.container-q03LZO:not(.colored-1armap) .profileGuildSubscriberlvl4-2NXrsI {
	background: rgb(var(--fontwhite1));
	-webkit-mask: url(https://discordapp.com/assets/d01bee8a9b41bd9dda26a43221b2e7e8.svg) center/contain no-repeat;
}
.container-q03LZO:not(.colored-1armap) .profileGuildSubscriberlvl5-3XIa2K {
	background: rgb(var(--fontwhite1));
	-webkit-mask: url(https://discordapp.com/assets/a99def5f819c077e5e5061cab741b7e6.svg) center/contain no-repeat;
}
.container-q03LZO:not(.colored-1armap) .profileGuildSubscriberlvl6-3e3sxW {
	background: rgb(var(--fontwhite1));
	-webkit-mask: url(https://discordapp.com/assets/2cfb317f3db3963d8ded9a97ee967bac.svg) center/contain no-repeat;
}
.container-q03LZO:not(.colored-1armap) .profileGuildSubscriberlvl7-1dVhQT {
	background: rgb(var(--fontwhite1));
	-webkit-mask: url(https://discordapp.com/assets/278736f579d810b11ddf308cb598b19e.svg) center/contain no-repeat;
}
.container-q03LZO:not(.colored-1armap) .profileGuildSubscriberlvl8-1kXdFr {
	background: rgb(var(--fontwhite1));
	-webkit-mask: url(https://discordapp.com/assets/38e40f25802a0fdf480d9b855a37a2f3.svg) center/contain no-repeat;
}
.container-q03LZO:not(.colored-1armap) .profileGuildSubscriberlvl9-1d6zav {
	background: rgb(var(--fontwhite1));
	-webkit-mask: url(https://discordapp.com/assets/cfbc2d8ceacfacf07850f986c8165195.svg) center/contain no-repeat;
}

/* ----		15.7.	SCROLLBARS						---- */

::-webkit-scrollbar,
#app-mount ::-webkit-scrollbar {
	width: 8px;
	height: 8px;
}
#app-mount .scroller-3vODG7::-webkit-scrollbar {
	width: 6px;
	height: 6px;
}
#app-mount .scroller--qpKGq::-webkit-scrollbar,
#app-mount .scrollbar-3dvm_9::-webkit-scrollbar,
#app-mount .scroller-2PSBSf::-webkit-scrollbar {
	width: 4px;
	height: 4px;
}
::-webkit-scrollbar,
::-webkit-scrollbar-track,
::-webkit-scrollbar-track-piece,
#app-mount ::-webkit-scrollbar,
#app-mount ::-webkit-scrollbar-track,
#app-mount ::-webkit-scrollbar-track-piece {
	border-color: transparent !important;
	background: transparent !important;
}
::-webkit-scrollbar-thumb,
#app-mount ::-webkit-scrollbar-thumb {
	border-radius: 10px;
	border: none;
	background-color: rgb(var(--vaccentcolor)) !important;
}
.none-2Eo-qx::-webkit-scrollbar-corner,
.none-2Eo-qx::-webkit-scrollbar-thumb,
.none-2Eo-qx::-webkit-scrollbar-track,
.none-2Eo-qx::-webkit-scrollbar {
	display: none;
}

/* ----		15.8.	NOTIFICATIONBAR					---- */

#app-mount .notice-2FJMB4 {
	box-shadow: 0 1px 5px 0 rgba(var(--vtransparencycolor), 0.3);
	color: rgb(var(--fontwhite1));
}
#app-mount .notice-2X5hT5 {
	background-color: rgba(var(--vtransparencycolor), 0.6);
}
#app-mount .button-1MICoQ:not(:hover) {
	border-color: rgba(var(--fontwhite1), 0.25);
	color: rgb(var(--fontwhite1));
}
#app-mount .button-1MICoQ:hover {
	border-color: rgb(var(--fontwhite1));
	background-color: rgb(var(--fontwhite1));
}
#app-mount .dismiss-SCAH9H {
	-webkit-mask: url(https://discordapp.com/assets/69a0ea5dbf79a129c81a0cb171b60b7a.svg) 50% 55%/10px 10px no-repeat;
	background: rgb(var(--fontwhite1));
}
#app-mount .icon-KgjVwm:empty,
#app-mount .platformIcon-2NdO9F:empty {
	background: rgb(var(--fontwhite1));
}
#app-mount .iconWindows-1KG_XN {
	-webkit-mask: url(https://discordapp.com/assets/24b843ed68d70abffbf4fdab9b400cc9.svg) center/contain no-repeat;
}
#app-mount .iconApple-1hp9Sq {
	-webkit-mask: url(https://discordapp.com/assets/ca511da5c9b326e5cb3f6befab1a3143.svg) center/contain no-repeat;
}
#app-mount .iconAndroid-3HTSwF {
	-webkit-mask: url(https://discordapp.com/assets/296aebeec33f5ce47db9ebbee9ccf1fc.svg) center/contain no-repeat;
}
#app-mount .premiumLogo-30dge3 {
	-webkit-mask: url(https://discordapp.com/assets/9328a2df4b542ac8725b57010a52f73b.svg) center/contain no-repeat;
	background: rgb(var(--fontwhite1));
}
.noticeBrand-3nQBC_ {
	text-shadow: 1px 1px var(--vtextshadow);
}
.noticeBrand-3nQBC_ .button-1MICoQ {
	box-shadow: 1px 1px var(--vtextshadow);
	text-shadow: 1px 1px var(--vtextshadow);
}
#app-mount .noticeBrand-3nQBC_ .icon-KgjVwm:empty::after,
#app-mount .noticeBrand-3nQBC_ .platformIcon-2NdO9F:empty::after,
#app-mount .noticeBrand-3nQBC_ .premiumLogo-30dge3::after,
#app-mount .noticeBrand-3nQBC_ .dismiss-SCAH9H::after {
	content: "";
	position: absolute;
	top: 0;
	right: 0;
	left: 0;
	bottom: 0;
	background: var(--vtextshadow);
}

/* ----		15.9.	TOOLTIPS						---- */

.headerText-1e7ZU0,
.bodyText-3yi6Dj {
	color: rgb(var(--fontwhite1));
}
#app-mount .tooltip-2QfLtc {
	box-shadow: 0 2px 10px 0 rgba(var(--vtransparencycolor), 0.3);
	color: rgb(var(--fontwhite1));
}
#app-mount .tooltipGrey-1hnvTt,
#app-mount .tooltipBlack-PPG47z {
	background-color: rgb(var(--vaccentcolor));
	text-shadow: 1px 1px var(--vtextshadow);
}
#app-mount .tooltipGrey-1hnvTt .tooltipPointer-3ZfirK,
#app-mount .tooltipBlack-PPG47z .tooltipPointer-3ZfirK {
	border-top-color: rgb(var(--vaccentcolor));
}
.emptyUser-7txhlW {
	background: rgba(var(--vtransparencycolor), 0.5);
}
.moreUsers-7v8yWY {
	background: rgba(var(--vtransparencycolor), 0.5);
}

/* ----		15.10.	TOASTS							---- */

html .toast,
html .bd-toast {
	background-color: rgb(var(--vaccentcolor));
	box-shadow: 0 0 0 1px rgba(var(--vtransparencycolor), 0.3), 0 2px 10px 0 rgba(var(--vtransparencycolor), 0.3);
	color: rgb(var(--fontwhite1));
	text-shadow: 1px 1px var(--vtextshadow);
}
html .toast.icon,
html .bd-toast.icon {
	background-image: none !important;
}
html .toast.icon::before,
html .bd-toast.icon::before {
	content: "";
	position: absolute;
	top: 0;
	right: 0;
	bottom: 0;
	left: 0;
	background: rgb(var(--fontwhite1)) !important;
}
html .toast.toast-brand.icon::after,
html .bd-toast.toast-brand.icon::after {
	content: "";
	position: absolute;
	top: 0;
	right: 0;
	left: 0;
	bottom: 0;
	background: var(--vtextshadow);
}
html .toast.toast-brand.icon::before,
html .bd-toast.toast-brand.icon::before,
html .toast.toast-brand.icon::after,
html .bd-toast.toast-brand.icon::after {
	-webkit-mask: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHhtbG5zOnhsaW5rPSJodHRwOi8vd3d3LnczLm9yZy8xOTk5L3hsaW5rIiB2ZXJzaW9uPSIxLjEiIHhtbDpzcGFjZT0icHJlc2VydmUiIHg9IjBweCIgeT0iMHB4IiB3aWR0aD0iNTEycHgiIGhlaWdodD0iNTEycHgiIHZpZXdCb3g9IjI3IDI3IDExNSAxMTUiIHN0eWxlPSJlbmFibGUtYmFja2dyb3VuZDpuZXcgMCAwIDkwIDkwOyI+PHBhdGggZmlsbD0id2hpdGUiIGQ9Ik0xMTEuMywxMjQuMWMwLDAtMy40LTQuMS02LjMtNy43YzEyLjYtMy41LDE3LjQtMTEuMywxNy40LTExLjMgYy00LDIuNi03LjcsNC40LTExLjEsNS42Yy00LjgsMi05LjUsMy4zLTE0LDQuMWMtOS4yLDEuNy0xNy42LDEuMy0yNC45LTAuMWMtNS41LTEtMTAuMi0yLjUtMTQuMS00LjFjLTIuMi0wLjgtNC42LTEuOS03LjEtMy4zIGMtMC4zLTAuMi0wLjYtMC4zLTAuOS0wLjVjLTAuMS0wLjEtMC4zLTAuMi0wLjQtMC4yYy0xLjctMS0yLjYtMS42LTIuNi0xLjZzNC42LDcuNiwxNi44LDExLjJjLTIuOSwzLjYtNi40LDcuOS02LjQsNy45IGMtMjEuMi0wLjYtMjkuMy0xNC41LTI5LjMtMTQuNWMwLTMwLjYsMTMuOC01NS40LDEzLjgtNTUuNGMxMy44LTEwLjMsMjYuOS0xMCwyNi45LTEwbDEsMS4xQzUyLjgsNTAuMyw0NSw1Ny45LDQ1LDU3LjkgczIuMS0xLjIsNS43LTIuN2MxMC4zLTQuNSwxOC40LTUuNywyMS44LTZjMC41LTAuMSwxLjEtMC4yLDEuNi0wLjJjNS45LTAuNywxMi41LTAuOSwxOS40LTAuMmM5LjEsMSwxOC45LDMuNywyOC45LDkuMSBjMCwwLTcuNS03LjItMjMuOS0xMi4xbDEuMy0xLjVjMCwwLDEzLjEtMC4zLDI2LjksMTBjMCwwLDEzLjgsMjQuOCwxMy44LDU1LjRDMTQwLjYsMTA5LjYsMTMyLjUsMTIzLjUsMTExLjMsMTI0LjF6IE0xMDEuNyw3OS43Yy01LjQsMC05LjgsNC43LTkuOCwxMC41YzAsNS44LDQuNCwxMC41LDkuOCwxMC41YzUuNCwwLDkuOC00LjcsOS44LTEwLjUgQzExMS41LDg0LjQsMTA3LjEsNzkuNywxMDEuNyw3OS43eiBNNjYuNyw3OS43Yy01LjQsMC05LjgsNC43LTkuOCwxMC41YzAsNS44LDQuNCwxMC41LDkuOCwxMC41YzUuNCwwLDkuOC00LjcsOS44LTEwLjUgQzc2LjUsODQuNCw3Mi4xLDc5LjcsNjYuNyw3OS43eiIvPjwvc3ZnPg==) 6px 50%/20px 20px no-repeat;
}
html .toast.toast-danger.icon::before,
html .toast.toast-error.icon::before,
html .bd-toast.toast-danger.icon::before,
html .bd-toast.toast-error.icon::before {
	-webkit-mask: url(data:image/svg+xml;base64,PHN2ZyBmaWxsPSIjRkZGRkZGIiBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4gICAgPHBhdGggZD0iTTEyIDJDNi40NyAyIDIgNi40NyAyIDEyczQuNDcgMTAgMTAgMTAgMTAtNC40NyAxMC0xMFMxNy41MyAyIDEyIDJ6bTUgMTMuNTlMMTUuNTkgMTcgMTIgMTMuNDEgOC40MSAxNyA3IDE1LjU5IDEwLjU5IDEyIDcgOC40MSA4LjQxIDcgMTIgMTAuNTkgMTUuNTkgNyAxNyA4LjQxIDEzLjQxIDEyIDE3IDE1LjU5eiIvPiAgICA8cGF0aCBkPSJNMCAwaDI0djI0SDB6IiBmaWxsPSJub25lIi8+PC9zdmc+) 6px 50%/20px 20px no-repeat;
}
html .toast.toast-facebook.icon::before,
html .bd-toast.toast-facebook.icon::before {
	-webkit-mask: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHhtbG5zOnhsaW5rPSJodHRwOi8vd3d3LnczLm9yZy8xOTk5L3hsaW5rIiB2ZXJzaW9uPSIxLjEiIGlkPSJDYXBhXzEiIHg9IjBweCIgeT0iMHB4IiB3aWR0aD0iNTEycHgiIGhlaWdodD0iNTEycHgiIHZpZXdCb3g9Ii01IC01IDEwMCAxMDAiIHN0eWxlPSJlbmFibGUtYmFja2dyb3VuZDpuZXcgMCAwIDkwIDkwOyIgeG1sOnNwYWNlPSJwcmVzZXJ2ZSI+PGc+PHBhdGggaWQ9IkZhY2Vib29rX194MjhfYWx0X3gyOV8iIGQ9Ik05MCwxNS4wMDFDOTAsNy4xMTksODIuODg0LDAsNzUsMEgxNUM3LjExNiwwLDAsNy4xMTksMCwxNS4wMDF2NTkuOTk4ICAgQzAsODIuODgxLDcuMTE2LDkwLDE1LjAwMSw5MEg0NVY1NkgzNFY0MWgxMXYtNS44NDRDNDUsMjUuMDc3LDUyLjU2OCwxNiw2MS44NzUsMTZINzR2MTVINjEuODc1QzYwLjU0OCwzMSw1OSwzMi42MTEsNTksMzUuMDI0VjQxICAgaDE1djE1SDU5djM0aDE2YzcuODg0LDAsMTUtNy4xMTksMTUtMTUuMDAxVjE1LjAwMXoiIGZpbGw9IndoaXRlIi8+PC9nPjxnPjwvZz48Zz48L2c+PGc+PC9nPjxnPjwvZz48Zz48L2c+PGc+PC9nPjxnPjwvZz48Zz48L2c+PGc+PC9nPjxnPjwvZz48Zz48L2c+PGc+PC9nPjxnPjwvZz48Zz48L2c+PGc+PC9nPjwvc3ZnPg==) 6px 50%/20px 20px no-repeat;
}
html .toast.toast-info.icon::before,
html .bd-toast.toast-info.icon::before {
	-webkit-mask: url(data:image/svg+xml;base64,PHN2ZyBmaWxsPSIjRkZGRkZGIiBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4gICAgPHBhdGggZD0iTTAgMGgyNHYyNEgweiIgZmlsbD0ibm9uZSIvPiAgICA8cGF0aCBkPSJNMTIgMkM2LjQ4IDIgMiA2LjQ4IDIgMTJzNC40OCAxMCAxMCAxMCAxMC00LjQ4IDEwLTEwUzE3LjUyIDIgMTIgMnptMSAxNWgtMnYtNmgydjZ6bTAtOGgtMlY3aDJ2MnoiLz48L3N2Zz4=) 6px 50%/20px 20px no-repeat;
}
html .toast.toast-premium.icon::before,
html .bd-toast.toast-premium.icon::before {
	-webkit-mask: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxMDMiIGhlaWdodD0iMjYiPiAgPHBhdGggZmlsbD0iI0ZGRiIgZmlsbC1ydWxlPSJldmVub2RkIiBkPSJNOTYuMjgyNiA4LjYwMjc4ODI0bC0xLjIxNTUgOC4zOTAzNTI5NmMtLjI3NzUgMS45ODI2Mjc0LTIuNDY1NSAyLjkwMzMzMzMtNC40NzkgMi45MDMzMzMzLTEuODc1IDAtMy43MTU1LS45MjA3MDU5LTMuNDcyNS0yLjcyNTkyMTZsMS4yMTU1LTguNTY3NzY0NjZjLjI3NzUtMS44NzY1ODgyNCAyLjQ2NTUtMi44MzI0NzA2IDQuNDc5LTIuODMyNDcwNiAyLjAxNCAwIDMuNzUuOTU1ODgyMzYgMy40NzI1IDIuODMyNDcwNk05My43NzIxLjAwMzkyNTVsLjAwMDUtLjAwNDA3ODQ0aC0xMy4wODRjLS4zMzQgMC0uNjE4LjI1MDMxMzcyLS42NjYuNTg3Mjk0MTJsLS42MzY1IDQuNDMyMjM1M2MtLjA1OTUuNDE0NDcwNTguMjU2Ljc4NjExNzY0LjY2NjUuNzg2MTE3NjRoMi4zODk1Yy4yNCAwIC40MDQ1LjI0OTgwMzkyLjMxLjQ3NTY0NzA2LS4yOTguNzEyMTk2MDctLjUxNTUgMS40ODYwNzg0My0uNjM2IDIuMzIxNjQ3MDZsLTEuMjE1NSA4LjU2Nzc2NDY2Yy0uNzk5IDUuNzM1Mjk0MiAzLjg4OSA4LjYwMjQzMTQgOC45OTMgOC42MDI0MzE0IDUuMzQ3NSAwIDEwLjU5MDUtMi44NjcxMzcyIDExLjM4OS04LjYwMjQzMTRsMS4yMTUtOC41Njc3NjQ2NmMuNzgzLTUuNjIyMTE3NjUtMy43Mzk1LTguNDg4MjM1My04LjcyNTUtOC41OTg4NjI3NW0tNzguNTk1MjUgMTEuNzI4NjUxbC4wNjcgNC4xNTg5ODA0Yy4wMDE1LjA4NTEzNzItLjA1NS4xNjA1ODgyLS4xMzYuMTgxNDkwMmgtLjAwMDVsLTEuMzg1NS01LjAxNjQ3MDZjLS4wMDItLjAwNzY0NzEtLjAwNS0uMDE0Nzg0My0uMDA4LS4wMjI0MzE0TDkuNDE0MzUuNzcwNzcyNTNjLS4xMDYtLjI1Mjg2Mjc1LS4zNDk1LS40MTY1MDk4LS42MTk1LS40MTY1MDk4aC00Ljg3MjVjLS4zMzYgMC0uNjIwNS4yNTIzNTI5NC0uNjY3LjU5MTM3MjU0TC4wMDY4NSAyNC42MzcyNDMxYy0uMDU3LjQxMzQ1MS4yNTc1Ljc4MjAzOTMuNjY2NS43ODIwMzkzaDQuODU0Yy4zMzY1IDAgLjYyMTUtLjI1MzM3MjYuNjY3NS0uNTkyOTAybDEuMjcyLTkuNDEyNTA5OGMuMDAxNS0uMDA5MTc2NS4wMDItLjAxODM1My4wMDItLjAyNzUyOTRsLS4wNjk1LTQuODM2NTA5OC4xMzg1LS4wMzUxNzY1IDEuNDU1NSA1LjAxNjQ3MDZjLjAwMjUuMDA3MTM3Mi4wMDUuMDEzNzY0Ny4wMDc1LjAyMDkwMmw0LjAyMTUgOS40NTM4MDM5Yy4xMDY1LjI1MDgyMzUuMzQ5NS40MTM0NTEuNjE3NS40MTM0NTFoNS4yNTY1Yy4zMzYgMCAuNjIwNS0uMjUyMzUzLjY2Ny0uNTkxODgyNGwzLjI0OTUtMjMuNjkxNjA3ODRjLjA1NjUtLjQxMjk0MTE4LS4yNTgtLjc4MTUyOTQyLS42NjctLjc4MTUyOTQyaC00LjgyMDVjLS4zMzYgMC0uNjIwNS4yNTE4NDMxNC0uNjY3LjU5MDg2Mjc1bC0xLjQ4IDEwLjc1ODkwMmMtLjAwMS4wMDkxNzY0LS4wMDE1LjAxODg2MjctLjAwMTUuMDI4NTQ5bTkuMzk0IDEzLjY4NjYwMzloNC44NTVjLjMzNiAwIC42MjA1LS4yNTIzNTI5LjY2Ny0uNTkxMzcyNmwzLjI0OS0yMy42OTIxMTc2Yy4wNTY1LS40MTI5NDEyLS4yNTgtLjc4MTUyOTQ0LS42NjctLjc4MTUyOTQ0aC00Ljg1NWMtLjMzNiAwLS42MjA1LjI1MjM1Mjk0LS42NjcuNTkxMzcyNTVsLTMuMjQ5IDIzLjY5MjExNzY4Yy0uMDU2NS40MTI5NDEyLjI1OC43ODE1Mjk0LjY2Ny43ODE1Mjk0TTM2LjYyMTE1LjkwNjA3NDVsLS42MzYgNC40MzIyMzUzYy0uMDU5NS40MTQ0NzA2LjI1NTUuNzg2MTE3NjUuNjY2Ljc4NjExNzY1aDUuMDgwNWMuNDA4NSAwIC43MjMuMzY3NTY4NjMuNjY3NS43ODA1MDk4bC0yLjM5MzUgMTcuNzM0MDM5MjVjLS4wNTU1LjQxMjQzMTMuMjU4NS43OC42NjcuNzhoNC45MjU1Yy4zMzY1IDAgLjYyMS0uMjUyODYyOC42NjctLjU5MjkwMmwyLjQ0NC0xOC4xMDg3NDUxYy4wNDYtLjMzOTUyOTQuMzMwNS0uNTkyOTAxOTUuNjY3LS41OTI5MDE5NWg1LjQ2MjVjLjMzNCAwIC42MTgtLjI0OTgwMzkyLjY2Ni0uNTg3Mjk0MTJsLjYzNy00LjQzMjIzNTNjLjA1OTUtLjQxNDQ3MDU4LS4yNTU1LS43ODYxMTc2NC0uNjY2NS0uNzg2MTE3NjRoLTE4LjE4NzVjLS4zMzQ1IDAtLjYxOC4yNTAzMTM3LS42NjY1LjU4NzI5NDFNNzEuMDM4NyA5LjA5ODM2ODZjLS4xNzQgMS40NTE0MTE3Ny0xLjI4NDUgMi45MDI4MjM1Ny0zLjE5NSAyLjkwMjgyMzU3aC0yLjg2OTVjLS40MSAwLS43MjQ1LS4zNjk2MDc5LS42NjctLjc4MzA1ODlsLjYwNzUtNC4zNjE4ODIzM2MuMDQ3LS4zMzg1MDk4LjMzMTUtLjU5MDM1Mjk0LjY2Ny0uNTkwMzUyOTRoMy4wNjFjMS44NDA1IDAgMi41Njk1IDEuMzEwMTk2MDggMi4zOTYgMi44MzI0NzA2TTY5LjMzNzIuMzU0MjExNzZoLTkuMjQwNWMtLjMzNiAwLS42MjA1LjI1MjM1Mjk0LS42NjcuNTkxMzcyNTRsLTMuMjQ5IDIzLjY5MjExNzdjLS4wNTY1LjQxMjk0MTEuMjU4Ljc4MTUyOTQuNjY3Ljc4MTUyOTRoNC45MjM1Yy4zMzY1IDAgLjYyMTUtLjI1MzM3MjYuNjY3NS0uNTkyOTAybC45NTYtNy4wNzY1ODgyYy4wMjMtLjE2OTc2NDcuMTY1LS4yOTYxOTYxLjMzMzUtLjI5NjE5NjFoLjYzM2MuMTE0NSAwIC4yMjE1LjA1OTY0NzEuMjgzNS4xNTgwMzkybDQuNzAyIDcuNDkxMDU4OGMuMTI0LjE5NzI5NDIuMzM3NS4zMTY1ODgzLjU2NzUuMzE2NTg4M2g2LjA4MWMuNTQ1IDAgLjg2NDUtLjYyNTAxOTYuNTUyLTEuMDgwMjc0NWwtNC45MzQ1LTcuMTkxODA0Yy0uMTE4LS4xNzI4MjM1LS4wNTc1LS40MTI0MzEzLjEyOC0uNTA0NzA1OCAzLjE1MDUtMS41Njk2ODYzIDQuOTc5NS0zLjE3ODExNzcgNS41ODMtNy42NTAxMTc3LjY5MzUtNS44NzcwMTk2LTIuOTE3LTguNjM4MTE3NjMtNy45ODY1LTguNjM4MTE3NjMiLz48L3N2Zz4=) 6px 50%/63px 16px no-repeat;
}
html .toast.toast-spotify.icon::before,
html .bd-toast.toast-spotify.icon::before {
	-webkit-mask: url(data:image/svg+xml;base64,PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0iaXNvLTg4NTktMSI/Pgo8IS0tIEdlbmVyYXRvcjogQWRvYmUgSWxsdXN0cmF0b3IgMTkuMC4wLCBTVkcgRXhwb3J0IFBsdWctSW4gLiBTVkcgVmVyc2lvbjogNi4wMCBCdWlsZCAwKSAgLS0+CjxzdmcgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIiB4bWxuczp4bGluaz0iaHR0cDovL3d3dy53My5vcmcvMTk5OS94bGluayIgdmVyc2lvbj0iMS4xIiBpZD0iQ2FwYV8xIiB4PSIwcHgiIHk9IjBweCIgdmlld0JveD0iMCAwIDUwOC41MiA1MDguNTIiIHN0eWxlPSJlbmFibGUtYmFja2dyb3VuZDpuZXcgMCAwIDUwOC41MiA1MDguNTI7IiB4bWw6c3BhY2U9InByZXNlcnZlIiB3aWR0aD0iMjRweCIgaGVpZ2h0PSIyNHB4Ij4KPGc+Cgk8Zz4KCQk8Zz4KCQkJPHBhdGggZD0iTTI1NC4yNiwwQzExMy44NDUsMCwwLDExMy44NDUsMCwyNTQuMjZzMTEzLjg0NSwyNTQuMjYsMjU0LjI2LDI1NC4yNiAgICAgczI1NC4yNi0xMTMuODQ1LDI1NC4yNi0yNTQuMjZTMzk0LjY3NSwwLDI1NC4yNiwweiBNMzcxLjY5Niw0MDMuMjg4Yy0zLjE3OCw1LjgxNi05LjEyMiw5LjA1OC0xNS4yODcsOS4wNTggICAgIGMtMi44NiwwLTUuNzIxLTAuNjY3LTguNDIyLTIuMTI5Yy00MC43MTMtMjIuNDM4LTg2Ljk1Ny0zNC4yOTMtMTMzLjY3Ny0zNC4yOTNjLTI4LDAtNTUuNjUxLDQuMTYzLTgyLjEyNiwxMi4zNjMgICAgIGMtOS4yMTcsMi44Ni0xOS4wMDYtMi4yODgtMjEuODM1LTExLjUzN2MtMi44Ni05LjE4NSwyLjI4OC0yOC43LDExLjUzNy0zMS41OTJjMjkuODQ0LTkuMjQ5LDYwLjk1OS0xMy45MjEsOTIuNDU1LTEzLjkyMSAgICAgYzUyLjU2OCwwLDEwNC42NiwxMy4zNDksMTUwLjUyMiwzOC42MTZDMzczLjMxNywzNzQuNDYxLDM3Ni40LDM5NC44NjYsMzcxLjY5Niw0MDMuMjg4eiBNNDA0LjAxOSwzMDcuNTI3ICAgICBjLTMuNjIzLDcuMDI0LTEwLjc0MiwxOC4zMzgtMTguMDg0LDE4LjMzOGMtMy4yMSwwLTYuMzg4LTAuNjk5LTkuMzc2LTIuMzJjLTUwLjQ3MS0yNi4xODktMTA1LjA0MS0zOS40NzQtMTYyLjIxOC0zOS40NzQgICAgIGMtMzEuNDk2LDAtNjIuNzcsNC4xMzItOTIuOTY0LDEyLjQ1OWMtMTAuOTAxLDIuOTU2LTIyLjA4OS0zLjQwMS0yNS4wNDUtMTQuMzAyYy0yLjkyNC0xMC45MDEsMy40NjQtMjkuNDMxLDE0LjMzNC0zMi4zODYgICAgIGMzMy42ODktOS4xODUsNjguNTg3LTEzLjg1NywxMDMuNjc0LTEzLjg1N2M2Mi44OTgsMCwxMjUuNDQ1LDE1LjI1NiwxODAuOTM4LDQ0LjExNCAgICAgQzQwNS4yOSwyODUuMjQ4LDQwOS4xOTksMjk3LjUxNiw0MDQuMDE5LDMwNy41Mjd6IE00MTcuNTI2LDIzMC44MzZjLTMuNDY0LDAtNy4wMjQtMC43OTUtMTAuMzYxLTIuNDQ3ICAgICBjLTYwLjIyOC0zMC4wMzQtMTI1LjA5Ni00NS4yMjYtMTkyLjc2MS00NS4yMjZjLTM1LjI3OSwwLTcwLjQzLDQuMjkxLTEwNC41MzMsMTIuNzEzYy0xMi41MjIsMy4wODMtMjUuMTQtNC41MTMtMjguMjIzLTE3LjAwNCAgICAgYy0zLjExNS0xMi40NTksNC41MTMtMjcuNTU1LDE3LjAwNC0zMC42MzhjMzcuNzI2LTkuMzc2LDc2LjY1OS0xNC4xMTEsMTE1LjcyLTE0LjExMWM3NC45NzUsMCwxNDYuODY3LDE2Ljg3NywyMTMuNTc4LDUwLjEyMSAgICAgYzExLjUzNyw1Ljc1MywxNi4yNDEsMTkuNzM3LDEwLjQ4OCwzMS4yNDJDNDM0LjMwOCwyMjMuNjUzLDQyNi4xMDgsMjMwLjgzNiw0MTcuNTI2LDIzMC44MzZ6IiBmaWxsPSIjRkZGRkZGIi8+CgkJPC9nPgoJPC9nPgo8L2c+CjxnPgo8L2c+CjxnPgo8L2c+CjxnPgo8L2c+CjxnPgo8L2c+CjxnPgo8L2c+CjxnPgo8L2c+CjxnPgo8L2c+CjxnPgo8L2c+CjxnPgo8L2c+CjxnPgo8L2c+CjxnPgo8L2c+CjxnPgo8L2c+CjxnPgo8L2c+CjxnPgo8L2c+CjxnPgo8L2c+Cjwvc3ZnPgo=) 6px 50%/20px 20px no-repeat;
}
html .toast.toast-streamermode.icon::before,
html .bd-toast.toast-streamermode.icon::before {
	-webkit-mask: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHhtbG5zOnhsaW5rPSJodHRwOi8vd3d3LnczLm9yZy8xOTk5L3hsaW5rIiB2ZXJzaW9uPSIxLjEiIGlkPSJDYXBhXzEiIHg9IjBweCIgeT0iMHB4IiB2aWV3Qm94PSItMjUgLTI1IDU0MiA1NDIiIHN0eWxlPSJlbmFibGUtYmFja2dyb3VuZDpuZXcgMCAwIDQ5MiA0OTI7IiB4bWw6c3BhY2U9InByZXNlcnZlIiB3aWR0aD0iNTEycHgiIGhlaWdodD0iNTEycHgiPjxwYXRoIGQ9Ik00ODguMywxNDIuNXYyMDMuMWMwLDE1LjctMTcsMjUuNS0zMC42LDE3LjdsLTg0LjYtNDguOHYxMy45YzAsNDEuOC0zMy45LDc1LjctNzUuNyw3NS43SDc1LjdDMzMuOSw0MDQuMSwwLDM3MC4yLDAsMzI4LjQgICBWMTU5LjljMC00MS44LDMzLjktNzUuNyw3NS43LTc1LjdoMjIxLjhjNDEuOCwwLDc1LjcsMzMuOSw3NS43LDc1Ljd2MTMuOWw4NC42LTQ4LjhDNDcxLjMsMTE3LDQ4OC4zLDEyNi45LDQ4OC4zLDE0Mi41eiIgZmlsbD0iI0ZGRkZGRiIvPjwvc3ZnPg==) 6px 50%/20px 20px no-repeat;
}
html .toast.toast-success.icon::before,
html .bd-toast.toast-success.icon::before {
	-webkit-mask: url(data:image/svg+xml;base64,PHN2ZyBmaWxsPSIjRkZGRkZGIiBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4gICAgPHBhdGggZD0iTTAgMGgyNHYyNEgweiIgZmlsbD0ibm9uZSIvPiAgICA8cGF0aCBkPSJNMTIgMkM2LjQ4IDIgMiA2LjQ4IDIgMTJzNC40OCAxMCAxMCAxMCAxMC00LjQ4IDEwLTEwUzE3LjUyIDIgMTIgMnptLTIgMTVsLTUtNSAxLjQxLTEuNDFMMTAgMTQuMTdsNy41OS03LjU5TDE5IDhsLTkgOXoiLz48L3N2Zz4=) 6px 50%/20px 20px no-repeat;
}
html .toast.toast-warning.icon::before,
html .toast.toast-warn.icon::before,
html .bd-toast.toast-warning.icon::before,
html .bd-toast.toast-warn.icon::before {
	-webkit-mask: url(data:image/svg+xml;base64,PHN2ZyBmaWxsPSIjRkZGRkZGIiBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4gICAgPHBhdGggZD0iTTAgMGgyNHYyNEgweiIgZmlsbD0ibm9uZSIvPiAgICA8cGF0aCBkPSJNMSAyMWgyMkwxMiAyIDEgMjF6bTEyLTNoLTJ2LTJoMnYyem0wLTRoLTJ2LTRoMnY0eiIvPjwvc3ZnPg==) 6px 50%/20px 20px no-repeat;
}
html .toast.icon:not(.toast-brand):not(.toast-danger):not(.toast-error):not(.toast-facebook):not(.toast-info):not(.toast-premium):not(.toast-spotify):not(.toast-streamermode):not(.toast-success):not(.toast-warning):not(.toast-warn)::before, .bd-toast.icon:not(.toast-brand):not(.toast-danger):not(.toast-error):not(.toast-facebook):not(.toast-info):not(.toast-premium):not(.toast-spotify):not(.toast-streamermode):not(.toast-success):not(.toast-warning):not(.toast-warn)::before {
	display: none;
}


/* ~~~~		16.		BDSUPPORT						~~~~ */

#app-mount .fav {
	background: var(--header-primary);
	width: 16px;
	height: 16px;
	padding: 0;
	-webkit-mask: url('data:image/svg+xml;utf8, <svg viewBox="0 0 24 24" width="16" height="16" xmlns="http://www.w3.org/2000/svg"><path fill="currentColor" d="M19.6, 9l-4.2-0.4c-0.4, 0-0.7-0.3-0.8-0.6l-1.6-3.9c-0.3-0.8-1.5-0.8-1.8, 0L9.4, 8.1C9.3, 8.4, 9, 8.6, 8.6, 8.7L4.4, 9 c-0.9, 0.1-1.2, 1.2-0.6, 1.8L7, 13.6c0.3, 0.2, 0.4, 0.6, 0.3, 1l-1, 4.1c-0.2, 0.9, 0.7, 1.5, 1.5, 1.1l3.6-2.2c0.3-0.2, 0.7-0.2, 1, 0l3.6, 2.2 c0.8, 0.5, 1.7-0.2, 1.5-1.1l-1-4.1c-0.1-0.4, 0-0.7, 0.3-1l3.2-2.8C20.9, 10.2, 20.5, 9.1, 19.6, 9z M12, 15.4l-3.8, 2.3l1-4.3l-3.3-2.9 l4.4-0.4l1.7-4l1.7, 4l4.4, 0.4l-3.3, 2.9l1, 4.3L12, 15.4z"></path></svg>') center/contain no-repeat;
}
#app-mount .fav:hover,
#app-mount .fav.active {
	background: #faa61a;
}
#app-mount .fav.active {
	-webkit-mask: url('data:image/svg+xml;utf8, <svg viewBox="0 0 24 24" width="16" height="16" xmlns="http://www.w3.org/2000/svg"><path d="M0, 0H24V24H0Z" fill="none"></path><path fill="currentColor" d="M12.5, 17.6l3.6, 2.2a1, 1, 0, 0, 0, 1.5-1.1l-1-4.1a1, 1, 0, 0, 1, .3-1l3.2-2.8A1, 1, 0, 0, 0, 19.5, 9l-4.2-.4a.87.87, 0, 0, 1-.8-.6L12.9, 4.1a1.05, 1.05, 0, 0, 0-1.9, 0l-1.6, 4a1, 1, 0, 0, 1-.8.6L4.4, 9a1.06, 1.06, 0, 0, 0-.6, 1.8L7, 13.6a.91.91, 0, 0, 1, .3, 1l-1, 4.1a1, 1, 0, 0, 0, 1.5, 1.1l3.6-2.2A1.08, 1.08, 0, 0, 1, 12.5, 17.6Z"></path></svg>') center/contain no-repeat;
}

#app-mount .bd-modal-inner {								/* modal				container							*/
	background-color: transparent;
	border: none;
	box-shadow: 0 0 0 1px rgba(var(--vtransparencycolor), 0.3), 0 2px 10px 0 rgba(var(--vtransparencycolor), 0.3);
	position: relative;
	overflow: hidden;
}
.bd-modal-inner::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--vpopout) var(--vpopoutposition)/var(--vpopoutsize);
	background-attachment: fixed;
	filter: blur(var(--vpopoutblur));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.bd-modal-inner::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.2));
	width: unset;
	height: unset;
	border-radius: 5px;
	pointer-events: none;
	z-index: -1;
}
.bd-modal-wrapper .header {									/* modal				header								*/
	background-color: transparent;
	box-shadow: none;
	color: rgb(var(--fontwhite1));
}
.bd-modal-wrapper .bd-modal-body {							/* modal				body								*/
	background-color: transparent;
	color: rgb(var(--fontwhite1));
}
.bd-modal-wrapper .footer {									/* modal				footer								*/
	background-color: rgba(var(--vtransparencycolor), 0.2);
	box-shadow: none;
}
.bd-modal-wrapper .footer button {
	color: rgb(var(--fontwhite1));
}
.bd-modal-wrapper .tab-bar-container {						/* modal				tabbarcontainer						*/
	background: rgba(var(--vtransparencycolor), 0.2);
	border-top-color: rgba(var(--vtransparencycolor), 0.3);
	box-shadow: 0 2px 3px 0 rgba(var(--vtransparencycolor), 0.1);
}		
.bd-modal-wrapper .tab-bar-container .tab-bar-item {		/* modal				tabbaritem							*/
	color: rgb(var(--fontwhite1)) !important;
}
.bd-modal-wrapper .tab-bar-container .tab-bar-item.selected,/* modal				tabbaritem selected					*/
.bd-modal-wrapper .tab-bar-container .tab-bar-item:hover {	/* modal				tabbaritem hover					*/
	border-color: rgb(var(--fontwhite1)) !important;
}
.bd-modal-wrapper .table-header,							/* modal				tableheader							*/
.bd-modal-wrapper .error {									/* modal				tablerow							*/
	border-color: rgba(var(--fontwhite4), 0.3);
	color: rgb(var(--fontwhite1));
}
	
#pubslayer .ui-tab-bar-item,
#app-mount #bd-settings-sidebar .ui-tab-bar-item {			/* sidebar				item								*/
	color: rgb(var(--fontwhite3));
}
#pubslayer .ui-tab-bar-item:hover,
#app-mount #bd-settings-sidebar .ui-tab-bar-item:hover {
	background-color: rgba(var(--vtransparencycolor), 0.2);
	color: rgb(var(--fontwhite2));
}
#pubslayer .ui-tab-bar-item.selected,
#app-mount #bd-settings-sidebar .ui-tab-bar-item.selected {
	background-color: rgb(var(--vaccentcolor));
	color: rgb(var(--fontwhite1));
	text-shadow: 1px 1px var(--vtextshadow);
}
#pubslayer .ui-tab-bar-header,
#app-mount #bd-settings-sidebar .ui-tab-bar-header {		/* sidebar				sideitemheader						*/
	color: rgb(var(--fontwhite3));
}
#pubslayer .ui-tab-bar-separator,
#app-mount #bd-settings-sidebar .ui-tab-bar-separator {		/* sidebar				sideitemseparator					*/
	background-color: rgba(var(--fontwhite4), 0.3);
}
#bd-settings-sidebar [style*=" color: rgb(114, 118, 125)"] {/* sidebar				credits								*/
	color: rgb(var(--fontwhite4)) !important;
}

.bd-server-description-container {							/* pubslayer			guilddescription					*/
	border-color: rgba(var(--fontwhite4), 0.3);
	color: rgb(var(--fontwhite3));
}
.bd-server-card .bd-server-tags {							/* pubslayer			guildtags							*/
	color: rgb(var(--fontwhite3));
}
#pubslayer h2.ui-form-title {								/* pubslayer			header								*/
	color: rgb(var(--fontwhite1));
}
#pubslayer button {											/* pubslayer			button								*/
	color: rgb(var(--fontwhite1));
}
#pubslayer input {											/* pubslayer			input								*/
	background-color: rgba(var(--vtransparencycolor), 0.1);
	border-color: rgba(var(--vtransparencycolor), 0.3);
	color: rgb(var(--fontwhite1));
}
#pubslayer input:hover {
	border-color: rgb(var(--vtransparencycolor));
}
#pubslayer input::placeholder {
	color: rgb(var(--fontwhite3));
}

#app-mount #bd-settingspane-container h2.ui-form-title {	/* settingsitems		header								*/
	color: rgb(var(--fontwhite1));
	min-width: 100px;
}
#app-mount #bd-settingspane-container .ui-switch-item h3 {
	color: rgb(var(--fontwhite1));
}
#app-mount #bd-settingspane-container .ui-switch-item .style-description {
	border-bottom-color: rgba(var(--fontwhite4), 0.3);
	color: rgb(var(--fontwhite3));
}

.bd-switch: {												/* bd switch												*/
	box-shadow: inset 0 1px 1px rgba(var(--vtransparencycolor), 0.15);
}
.bd-switch:not(.bd-switch-checked) {
	background-color: rgba(var(--vtransparencycolor), 0.3);
}
.bd-switch::before {
	background-color: rgb(var(--fontwhite1));
	box-shadow: 0 2px 4px rgba(var(--vtransparencycolor), 0.6);
}

.bd-select-wrapper {										/* bd select			wrapper								*/
	color: rgb(var(--fontwhite1));
}
.bd-select {												/* bd select			inner								*/
	background-color: rgba(var(--vtransparencycolor), 0.1);
	border-color:  rgba(var(--vtransparencycolor), 0.3);
	color: rgb(var(--fontwhite1));
}
.bd-select-arrow {											/* bd select			arrow								*/
	fill: rgb(var(--fontwhite1));
}
.bd-select .bd-select-options {								/* bd select			popout								*/
	background-color: transparent;
	border: none;
	border-radius: 4px;
	box-shadow: rgba(var(--vtransparencycolor), 0.3) 0px 2px 5px 0px;
	box-sizing: border-box;
	padding: 6px 8px;
	margin-left: -9px;
}
.bd-select .bd-select-options::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--vpopout) var(--vpopoutposition)/var(--vpopoutsize);
	background-attachment: fixed;
	filter: blur(var(--vpopoutblur));
	width: unset;
	height: unset;
	border-radius: 4px;
	pointer-events: none;
	z-index: -1;
}
.bd-select .bd-select-options::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.3));
	width: unset;
	height: unset;
	border-radius: 4px;
	pointer-events: none;
	z-index: -1;
}
.bd-select .bd-select-option {								/* bd select			popout option						*/
	display: flex;
	align-items: center;
	min-height: 32px;
	border-radius: 2px;
	box-sizing: border-box;
	color: var(--interactive-normal);
	font-size: 14px;
	font-weight: 500;
	line-height: 18px;
	margin-top: 2px;
	margin-bottom: 2px;
	padding: 0 8px;
}
.bd-select .bd-select-option:hover {
	background-color: rgba(var(--vtransparencycolor), 0.2);
	color: var(--interactive-hover);
}
.bd-select .bd-select-option.selected {
	background-color: rgba(var(--vtransparencycolor), 0.3);
	color: var(--interactive-active);
}

.bd-pfbtn {													/* addonlist			folderbutton						*/
	color: rgb(var(--fontwhite1));
}

.bd-search-wrapper {										/* addonlist			searchbar container					*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
	color: rgb(var(--fontwhite1));
}
.bd-search {												/* addonlist			searchbar input						*/
	color: rgb(var(--fontwhite1))
}
.bd-search::placeholder {
	color: rgb(var(--fontwhite3));
}
.bd-search-wrapper svg[fill] {								/* addonlist			searchbar icon						*/
	fill: rgb(var(--fontwhite1));
}

#app-mount .bd-addon-list .bd-addon-card {					/* addonlist			addoncard							*/
	background-color: rgba(var(--vtransparencycolor), 0.4);
	border-color: transparent;
	color: rgb(var(--fontwhite1));
	max-height: unset;
}
#app-mount .bd-addon-list .bd-addon-header {				/* addonlist			header								*/
	background-color: rgba(var(--vtransparencycolor), 0.3);
	border-bottom-color: rgba(var(--fontwhite2), 0.3);
	color: rgb(var(--fontwhite1));
}
#app-mount .bd-addon-list .bda-header {						/* addonlist			header old							*/
	background-color: transparent;
}
#app-mount .bd-addon-list .bd-addon-button svg[fill] {		/* addonlist			header button icon					*/
	fill: currentColor;
}
#app-mount .bd-addon-list .bd-addon-button svg {			/* addonlist			header button icon					*/
	color: rgb(var(--fontwhite3));
}
#app-mount .bd-addon-list .bd-button.bd-addon-button svg,
#app-mount .bd-addon-list .bd-addon-button svg:hover {
	color: rgb(var(--fontwhite1));
}
#app-mount .bd-addon-list .bd-description {					/* addonlist			description							*/
	color: rgb(var(--fontwhite2));
}
#app-mount .bd-addon-list .bd-description::-webkit-scrollbar {
	width: 4px;
	height: 4px;
}
#app-mount .bd-addon-list .bd-footer {						/* addonlist			footer								*/
	border-top-color: rgba(var(--fontwhite2), 0.3);
}
.bd-addon-list .bd-footer button {							/* addonlist			footer button						*/
	color: rgb(var(--fontwhite1));
}

#bd-customcss-detach-container {							/* customcsseditor		detached							*/
	background: transparent;
}
#bd-customcss-attach-controls {
	background-color: rgba(var(--vtransparencycolor), 0.8);
	box-shadow: none;
}
.contentRegion-3nDuYy #bd-customcss-attach-controls,
#bd-customcss-detach-container #bd-customcss-attach-controls {
	background-color: rgba(var(--vtransparencycolor), 0.5);
	box-shadow: inset 0 1px 0 0 rgba(var(--fontwhite4), 0.3);
	color: rgb(var(--fontwhite1));
}
.standardSidebarView-3F1I7i #bd-customcss-attach-controls button,
.bd-detached-css-editor #bd-customcss-attach-controls button {
	color: rgb(var(--fontwhite1));
	background: rgba(var(--vtransparencycolor), 0.5);
	border: none !important;
	border-radius: 3px !important;
	margin: 5px 5px 0 0;
	transition: background-color 0.1s ease;
}
.standardSidebarView-3F1I7i #bd-customcss-attach-controls button:hover,
.bd-detached-css-editor #bd-customcss-attach-controls button:hover {
	background: rgb(var(--vaccentcolor));
}
.standardSidebarView-3F1I7i #editor-detached h3 {
	color: rgb(var(--fontwhite3));
}
#bd-customcss-attach-controls .help-text .inline {
	background-color: rgba(var(--vtransparencycolor), 0.4);
}
html .monaco-editor .reference-zone-widget .ref-tree .referenceMatch .highlight {
	background: rgb(var(--vaccentcolor));
}



/* ~~~~		17.		PLUGINSUPPORT					~~~~ */

/* ----		17.1.	DATEVIEWER						---- */

#app-mount #dv-mount {
	background: transparent;
}
#app-mount #dv-main {
	border-top-color: rgba(var(--fontwhite1), 0.1);
	color: rgb(var(--fontwhite1));
}
#app-mount #dv-main .dv-date {
	color: rgb(var(--fontwhite3));
	opacity: 1;
}

/* ----		17.2.	SERVERFOLDERS					---- */

.base-PmTxvP[style*="background-color: rgb(114, 137, 218)"] {
	text-shadow: 1px 1px var(--vtextshadow);
}

/* ----		17.3.	MEMBERCOUNT						---- */

#app-mount #MemberCount {
	background-color: transparent;
	color: rgb(var(--fontwhite2));
	width: calc(100% - 8px);
	margin: 0;
	line-height: 0;
	height: 30px;
}
#MemberCount::after,
#MemberCount::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	pointer-events: none;
	z-index: -1;
}
#MemberCount::after {
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + var(--vmemberlisttransparency) * 0.85));
}
#MemberCount::before {
	background: var(--vbackground) var(--vbackgroundposition)/var(--vbackgroundsize);
	background-attachment: fixed;
	filter: blur(var(--vbackgroundblur));
}

/* ----		17.4.	SENDBUTTON						---- */

.send-button img {
	-webkit-mask: url(data:image/svg+xml;base64,PHN2ZyBmaWxsPSIjRkZGRkZGIiBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4gICAgPHBhdGggZD0iTTIuMDEgMjFMMjMgMTIgMi4wMSAzIDIgMTBsMTUgMi0xNSAyeiIvPiAgICA8cGF0aCBkPSJNMCAwaDI0djI0SDB6IiBmaWxsPSJub25lIi8+PC9zdmc+) center/contain no-repeat;
	background: rgb(var(--fontwhite3));
	cursor: pointer;
	object-position: -9999999px -9999999px;
	opacity: 1;
}
.send-button img:hover {
	background: rgb(var(--fontwhite2));
	transform: none;
}
.send-button img:active {
	background: rgb(var(--fontwhite1));
}
.innerDisabled-2mc-iF .send-button {
	display: none;
}

/* ----		17.5.	CHARCOUNTER						---- */

#app-mount #charcounter {
	color: rgb(var(--fontwhite3));
	opacity: 1;
}
.innerDisabled-2mc-iF #charcounter {
	display: none;
}

/* ----		17.6.	REPLYER							---- */

.replyer-icon {
	-webkit-mask: url(data:image/svg+xml;base64,PHN2ZyBmaWxsPSIjRkZGRkZGIiBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4gICAgPHBhdGggZD0iTTEwIDlWNWwtNyA3IDcgN3YtNC4xYzUgMCA4LjUgMS42IDExIDUuMS0xLTUtNC0xMC0xMS0xMXoiLz4gICAgPHBhdGggZD0iTTAgMGgyNHYyNEgweiIgZmlsbD0ibm9uZSIvPjwvc3ZnPg==) center/contain no-repeat !important;
	background: rgb(var(--fontwhite1)) !important;
	border-radius: 3px !important;
	position: relative;
	padding: 0 3px 1px 3px;
	margin-top: 1px;
}
.replyer[style*="cursor:pointer;color:rgba(255,255,255,.4) !important;position:relative;top:-1px;"] {
	-webkit-mask: url(data:image/svg+xml;base64,PHN2ZyBmaWxsPSIjRkZGRkZGIiBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4gICAgPHBhdGggZD0iTTEwIDlWNWwtNyA3IDcgN3YtNC4xYzUgMCA4LjUgMS42IDExIDUuMS0xLTUtNC0xMC0xMS0xMXoiLz4gICAgPHBhdGggZD0iTTAgMGgyNHYyNEgweiIgZmlsbD0ibm9uZSIvPjwvc3ZnPg==) center/70% no-repeat !important;
	background: rgb(var(--fontwhite1)) !important;
	border-radius: 3px !important;
	filter: none !important;
	font-size: 0 !important;
	margin: 0 0 0 6px !important;
	opacity: 0.7 !important;
	padding: 7px 10px !important;
	top: -5px !important;
	transition: unset !important;
}
.replyer-icon:hover,
.replyer[style*="cursor:pointer;color:rgba(255,255,255,.4) !important;position:relative;top:-1px;"]:hover {
	-webkit-mask: none !important;
	background: rgba(var(--vtransparencycolor), 0.4) url(data:image/svg+xml;base64,PHN2ZyBmaWxsPSIjRkZGRkZGIiBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4gICAgPHBhdGggZD0iTTEwIDlWNWwtNyA3IDcgN3YtNC4xYzUgMCA4LjUgMS42IDExIDUuMS0xLTUtNC0xMC0xMS0xMXoiLz4gICAgPHBhdGggZD0iTTAgMGgyNHYyNEgweiIgZmlsbD0ibm9uZSIvPjwvc3ZnPg==) center/70% no-repeat !important;
	opacity: 1 !important;
}
.replyer-icon:active,
.replyer[style*="cursor:pointer;color:rgba(255,255,255,.4) !important;position:relative;top:-1px;"]:active {
	-webkit-mask: none !important;
	background: rgb(var(--vaccentcolor)) url(data:image/svg+xml;base64,PHN2ZyBmaWxsPSIjRkZGRkZGIiBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4gICAgPHBhdGggZD0iTTEwIDlWNWwtNyA3IDcgN3YtNC4xYzUgMCA4LjUgMS42IDExIDUuMS0xLTUtNC0xMC0xMS0xMXoiLz4gICAgPHBhdGggZD0iTTAgMGgyNHYyNEgweiIgZmlsbD0ibm9uZSIvPjwvc3ZnPg==) center/70% no-repeat !important;
}

/* ----		17.7.	CITADOR							---- */

.quote-msg {
	background-color: rgba(var(--vtransparencycolor) , 0.2);
	border-radius: 5px 5px 0 0;
}
.quote-msg .replyer,
.quote-msg .replyer-icon,
.quote-msg .buttonContainer-KtQ8wc {
	display: none;
}
.quote-msg ~ .inner-zqa7da {
	border-radius: 0 0 8px 8px;
}
.quote-close {
	-webkit-mask: url(data:image/svg+xml;base64,PHN2ZyB4bWxuczpza2V0Y2g9Imh0dHA6Ly93d3cuYm9oZW1pYW5jb2RpbmcuY29tL3NrZXRjaC9ucyIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIiB4bWxuczp4bGluaz0iaHR0cDovL3d3dy53My5vcmcvMTk5OS94bGluayIgdmVyc2lvbj0iMS4xIiBpZD0iTGF5ZXJfMSIgeD0iMHB4IiB5PSIwcHgiIHdpZHRoPSIyMHB4IiBoZWlnaHQ9IjIwcHgiIHZpZXdCb3g9IjQwIDQwIDIwIDIwIiBlbmFibGUtYmFja2dyb3VuZD0ibmV3IDQwIDQwIDIwIDIwIiB4bWw6c3BhY2U9InByZXNlcnZlIj4NCjxnIGlkPSJQYWdlXzEiPg0KCTxwYXRoIGlkPSJDbG9zZSIgZmlsbD0iIzk5YWFiNSIgZD0iTTQwLjQ0NSw0Mi44NTNsMi40MDgtMi40MDhjMC41OTMtMC41OTMsMS41NTUtMC41OTMsMi4xNDcsMGw1LDVsNS01ICAgYzAuNTkzLTAuNTkzLDEuNTU0LTAuNTkzLDIuMTQ3LDBsMi40MDgsMi40MDhjMC41OTMsMC41OTMsMC41OTMsMS41NTQsMCwyLjE0N2wtNSw1bDUsNWMwLjU5MywwLjU5MywwLjU5MiwxLjU1NCwwLDIuMTQ3ICAgbC0yLjQwOCwyLjQwOGMtMC41OTMsMC41OTMtMS41NTUsMC41OTMtMi4xNDcsMGwtNS01bC01LDVjLTAuNTkzLDAuNTkzLTEuNTU0LDAuNTkzLTIuMTQ3LDBsLTIuNDA4LTIuNDA4ICAgYy0wLjU5My0wLjU5My0wLjU5My0xLjU1NCwwLTIuMTQ3bDUtNWwtNS01QzM5Ljg1Miw0NC40MDcsMzkuODUyLDQzLjQ0NSw0MC40NDUsNDIuODUzeiIvPg0KPC9nPg0KPC9zdmc+) center/contain no-repeat !important;
	background: rgb(var(--fontwhite1)) !important;
}
.delete-msg-btn {
	-webkit-mask: url(data:image/svg+xml;base64,PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0idXRmLTgiPz4KPCEtLSBHZW5lcmF0b3I6IEFkb2JlIElsbHVzdHJhdG9yIDE3LjEuMCwgU1ZHIEV4cG9ydCBQbHVnLUluIC4gU1ZHIFZlcnNpb246IDYuMDAgQnVpbGQgMCkgIC0tPgo8IURPQ1RZUEUgc3ZnIFBVQkxJQyAiLS8vVzNDLy9EVEQgU1ZHIDEuMS8vRU4iICJodHRwOi8vd3d3LnczLm9yZy9HcmFwaGljcy9TVkcvMS4xL0RURC9zdmcxMS5kdGQiPgo8c3ZnIHZlcnNpb249IjEuMSIgaWQ9IkxheWVyXzEiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyIgeG1sbnM6eGxpbms9Imh0dHA6Ly93d3cudzMub3JnLzE5OTkveGxpbmsiIHg9IjBweCIgeT0iMHB4IgoJIHZpZXdCb3g9IjAgMCAxNiAxNiIgZW5hYmxlLWJhY2tncm91bmQ9Im5ldyAwIDAgMTYgMTYiIHhtbDpzcGFjZT0icHJlc2VydmUiPgo8ZyBpZD0iZWRpdG9yaWFsXy1fdHJhc2hfY2FuIj4KCTxnPgoJCTxwYXRoIGZpbGw9IiNmZmZmZmYiIGQ9Ik01LDYuNUg0djZoMVY2LjV6IE0xNC41LDJIMTBWMC41QzEwLDAuMiw5LjgsMCw5LjUsMGgtNEM1LjIsMCw1LDAuMiw1LDAuNVYySDAuNUMwLjIsMiwwLDIuMiwwLDIuNQoJCQlTMC4yLDMsMC41LDNIMXYxMmMwLDAuNiwwLjQsMSwxLDFoMTFjMC42LDAsMS0wLjQsMS0xVjNoMC41QzE0LjgsMywxNSwyLjgsMTUsMi41UzE0LjgsMiwxNC41LDJ6IE02LDFoM3YxSDZWMXogTTEzLDE0LjUKCQkJYzAsMC4zLTAuMiwwLjUtMC41LDAuNWgtMTBDMi4yLDE1LDIsMTQuOCwyLDE0LjVWM2gxMVYxNC41eiBNOCw1LjVIN3Y3aDFWNS41eiBNMTEsNi41aC0xdjZoMVY2LjV6Ii8+Cgk8L2c+CjwvZz4KPC9zdmc+Cg==) center/contain no-repeat !important;
	background: rgb(var(--fontwhite1)) !important;
}

.citar-btn {
	-webkit-mask: url(https://storage.googleapis.com/material-icons/external-assets/v4/icons/svg/ic_format_quote_white_48px.svg) center/contain no-repeat !important;
	background: rgb(var(--fontwhite1)) !important;
	border-radius: 3px;
	filter: none !important;
	font-size: 0;
	margin: 0 0 0 6px !important;
	opacity: 0.7;
	padding: 7px 10px;
	position: relative;
	top: -5px;
	transition: unset !important;
}
.citar-btn:hover {
	-webkit-mask: none !important;
	background: rgba(var(--vtransparencycolor), 0.4) url(https://storage.googleapis.com/material-icons/external-assets/v4/icons/svg/ic_format_quote_white_48px.svg) center/contain no-repeat !important;
	opacity: 1;
}
.citar-btn:active {
	-webkit-mask: none !important;
	background: rgb(var(--vaccentcolor)) url(https://storage.googleapis.com/material-icons/external-assets/v4/icons/svg/ic_format_quote_white_48px.svg) center/contain no-repeat !important;
}
/* ----		17.8.	LINENUMBERS						---- */

.hljs ol li {
	border-left-color: rgba(var(--fontwhite1), 0.2);
}
.hljs ol li::before {
	color: rgb(var(--fontwhite4));
}

/* ----		17.9.	PERMISSIONVIEWER				---- */

#permissions-modal-wrapper #permissions-modal {				/* modal				container							*/
	background-color: transparent;
	border: none;
	box-shadow: 0 0 0 1px rgba(var(--vtransparencycolor), 0.3), 0 2px 10px 0 rgba(var(--vtransparencycolor), 0.3);
	position: relative;
	overflow: hidden;
}
#permissions-modal-wrapper #permissions-modal::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--vpopout) var(--vpopoutposition)/var(--vpopoutsize);
	background-attachment: fixed;
	filter: blur(var(--vpopoutblur));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
#permissions-modal-wrapper #permissions-modal::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--vtransparencycolor), calc(var(--vtransparencyalpha) + 0.2));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
#permissions-modal-wrapper .header {
	background-color: rgba(var(--vtransparencycolor), 0.2);
	box-shadow: 0 2px 3px 0 rgba(var(--vtransparencycolor), 0.2);
	color: rgb(var(--fontwhite1));
}
#permissions-modal-wrapper .modal-body {
	background-color: transparent;
}
#permissions-modal-wrapper .scroller-title {
	border-bottom: 1px solid rgba(var(--vtransparencycolor), 0.3);
}
#permissions-modal-wrapper .role-side {
	background-color: rgba(var(--vtransparencycolor), 0.1);
}
#permissions-modal-wrapper .role-item {
	color: rgb(var(--fontwhite2));
}
#permissions-modal-wrapper .role-item:hover {
	background-color: rgba(var(--vtransparencycolor), 0.1);
}
#permissions-modal-wrapper .role-item.selected {
	background-color: rgba(var(--vtransparencycolor), 0.2);
}
#permissions-modal-wrapper .perm-side {
	background-color: transparent;
}
#permissions-modal-wrapper .perm-item {
	box-shadow: inset 0 -1px 0 rgba(var(--fontwhite4), 0.3);
}
#permissions-modal-wrapper .perm-name {
	color: rgb(var(--fontwhite3));
}

/* ----		17.10.	DIRECTDOWNLOAD					---- */

#files_directDownload .file {
	background-color: rgba(var(--vtransparencycolor), 0.4);
	border-color: rgba(var(--vaccentcolor), 0.2);
	border-radius: 6px 6px 0 0;
}
#files_directDownload .file svg {
	fill: rgb(var(--fontwhite1));
	opacity: 0.5;
}
#files_directDownload .file svg:hover {
	opacity: 1;
}
#files_directDownload .file span {
	color: rgb(var(--fontwhite1));
}
#files_directDownload .file .progress-bar {
	background-color: rgb(var(--vaccentcolor));
}

/* ----		17.11.	BETTERFORMATINGREDUX			---- */

.innerDisabled-2mc-iF ~ .bf-toolbar {
	display: none;
}
.bf-arrow {
	-webkit-mask: url('data:image/svg+xml;utf8,<svg fill="white" height="24" viewBox="0 0 24 24" width="24" xmlns="http://www.w3.org/2000/svg"><path d="M7.41 15.41L12 10.83l4.59 4.58L18 14l-6-6-6 6z"/><path d="M0 0h24v24H0z" fill="none"/></svg>') center/contain no-repeat;
	background: rgb(var(--fontwhite1)) !important;
}
.bf-toolbar {
	background: transparent;
	overflow: hidden;
	transform: none;
	top: -50px;
}
.bf-toolbar::after {	
	content: "";
	display: block;
	position: absolute;
	width: 100%;
	height: calc(100% - 15px);
	pointer-events: none;
	left: 0px;
	top: 5px;
	background-color: rgba(var(--vtransparencycolor), 0.5);
	border-radius: 3px;
	transform: translate(0, 55px);
	transition: all 200ms ease;
	z-index: 200;
}
.bf-toolbar.bf-visible::after,
.bf-toolbar.bf-hover:hover::after {
	transform: translate(0, 0);
	transition: all 200ms cubic-bezier(0,0,0,1);
}
.bf-toolbar::before {
	background: var(--vpopout) var(--vpopoutposition)/var(--vpopoutsize);
	background-attachment: fixed;
	filter: blur(var(--vpopoutblur));
	z-index: 100;
}
.theme-brand .bf-toolbar::after {
	background: rgb(var(--vaccentcolor)) linear-gradient(rgba(var(--vtransparencycolor), 0.2), rgba(var(--vtransparencycolor), 0.2))!important;
}
.theme-brand .bf-toolbar::before {
	display: none;
}
.bf-toolbar > * {
	z-index: 300;
}
.bf-toolbar .format {
	color: rgb(var(--fontwhite2));
}
.bf-toolbar .format:hover {
	background-color: rgb(var(--vaccentcolor));
	color: rgb(var(--fontwhite1));
}

/* ----		17.12	PLUGIN/THEMEREPO				---- */

#app-mount .pluginEntry svg[fill="currentColor"],
#app-mount .pluginEntry .gifFavoriteButton-1gYkEU:not(.selected-2QpwIN),
#app-mount .themeEntry svg[fill="currentColor"],
#app-mount .themeEntry .gifFavoriteButton-1gYkEU:not(.selected-2QpwIN) {
	color: rgb(var(--fontwhite2)) !important;
}

#app-mount .pluginEntry svg[fill="currentColor"]:hover,
#app-mount .pluginEntry .gifFavoriteButton-1gYkEU:not(.selected-2QpwIN):hover,
#app-mount .themeEntry svg[fill="currentColor"]:hover,
#app-mount .themeEntry .gifFavoriteButton-1gYkEU:not(.selected-2QpwIN):hover {
	color: rgb(var(--fontwhite1)) !important;
}

/* ----		17.13	CHANNELHISTORY					---- */

.channelHistoryButtons {
	top: 4px;
	left: 310px;
}
/* ----		17.14	DISPLAYLARGEMESSAGES			---- */

#app-mount .injectButton-8eKqGu,							/* attachment			injectbutton						*/
#app-mount .popoutButton-a26sRh {							/* attachment			popoutbutton						*/
	color: rgb(var(--fontwhite4));
}
#app-mount .injectButton-8eKqGu:hover,
#app-mount .popoutButton-a26sRh:hover {
	color: rgb(var(--fontwhite3));
}
#app-mount .injectButton-8eKqGu:active,
#app-mount .popoutButton-a26sRh:active {
	color: rgb(var(--fontwhite2));
}

/* ----		17.15	CHANNELTABS						---- */

html .channelTabs-tabContainer,
html .channelTabs-favContainer {
	display: flex;
	align-items: center;
	flex-wrap: wrap;
	min-height: 28px;
	height: unset;
	overflow: hidden;
	transition: height 0.3s linear;
}
html .channelTabs-tabContainer {
	background: rgba(var(--vtransparencycolor), calc(0.05 + var(--vguildchanneltransparency) * 2));
	box-shadow: 0 1px 0 rgba(var(--vtransparencycolor), 0.2),0 1.5px 0 rgba(var(--vtransparencycolor), 0.05),0 2px 0 rgba(var(--vtransparencycolor), 0.05);
	padding-top: 6px;
}
html .channelTabs-favContainer {
	background: rgba(var(--vtransparencycolor), calc(var(--vguildchanneltransparency) * 2));
	padding-top: 3px;
	padding-bottom: 3px;
}
html .channelTabs-noFavs {
	background: transparent;
	padding: 0 6px;
}

html .channelTabs-tab,
html .channelTabs-fav {
	display: flex;
	align-items: center;
	color: var(--interactive-normal);
	height: 28px;
	margin: 0 4px;
	padding: 0 4px;
	cursor: pointer;
}
html .channelTabs-tab {
	background: rgba(var(--vtransparencycolor), 0.3);
	border-radius: 5px 5px 0 0;
}
html .channelTabs-tab:not(.channelTabs-selected):hover,
html .channelTabs-fav:hover {
	background: rgba(var(--vtransparencycolor), 0.4);
	color: var(--interactive-hover);
}
html .channelTabs-tab.channelTabs-selected,
html .channelTabs-fav:active {
	background: rgb(var(--vaccentcolor));
	color: var(--interactive-active);
}
html .channelTabs-tab > *,
html .channelTabs-fav > *,
html .channelTabs-tab .channelTabs-mentionBadge,
html .channelTabs-fav .channelTabs-mentionBadge,
html .channelTabs-tab .channelTabs-unreadBadge,
html .channelTabs-fav .channelTabs-unreadBadge {
	position: static !important;
	transform: unset !important;
	float: unset !important;
}
html .channelTabs-tabIcon,
html .channelTabs-favIcon {
	margin-right: 6px !important;
}
html .channelTabs-tabName,
html .channelTabs-favName {
	margin: 0 !important;
	font-size: 16px;
	line-height: 20px;
	font-weight: 500;
	white-space: nowrap;
}
html .channelTabs-tab .channelTabs-tabName ~ *,
html .channelTabs-fav .channelTabs-favName ~ * {
	margin: 0 0 0 4px !important;
}
html .channelTabs-closeTab,
html .channelTabs-tab.channelTabs-selected .channelTabs-closeTab {
	position: static;
	background: rgba(var(--vtransparencycolor), 0.3);
	color: var(--interactive-hover);
	border-radius: 50%;
	width: 14px;
	height: 14px;
	min-width: 14px;
	min-height: 14px;
	font-size: 14px;
	line-height: unset;
}
html .channelTabs-closeTab:hover,
html .channelTabs-tab.channelTabs-selected .channelTabs-closeTab:hover {
	background: #f04747;
	color: var(--interactive-active);
}
html .channelTabs-newTab {
	position: static;
	display: flex;
	justify-content: center;
	align-items: center;
	background: rgba(var(--vtransparencycolor), 0.3);
	color: var(--interactive-hover);
	padding: 0;
	width: 22px;
	height: 22px;
}
html .channelTabs-newTab:hover {
	background: rgb(var(--vaccentcolor));
	color: var(--interactive-active);
}


/* ~~~~		18.		UPDATENOTICE					~~~~ */

html:only-child > head + body > div#app-mount.appMount-3lHmkl > div.app-1q1i1E > div.app-2rEoOp::before {
	content: "Your version of   BasicBackground   by DevilBro is outdated. Please download the newest version from:	https://github.com/mwittrien/BetterDiscordAddons/blob/master/Themes/BasicBackground" !important;
	display: var(--version1_0_5, block) !important;
	background-color: #4a90e2 !important;
	box-shadow: 0 1px 5px 0 rgba(var(--vtransparencycolor), 0.3) !important;
	color: rgb(var(--fontwhite1)) !important;
	flex-grow: 0 !important;
	flex-shrink: 0 !important;
	font-size: 14px !important;
	font-weight: 500 !important;
	height: 36px !important;
	line-height: 36px !important;
	opacity: 1 !important;
	padding-left: 4px !important;
	padding-right: 28px !important;
	position: relative !important;
	text-align: center !important;
	visibility: unset !important;
	white-space: pre !important;
	top: 0 !important;
	left: 0 !important;
	bottom: unset !important;
	right: unset !important;
	max-width: unset !important;
	min-width: unset !important;
	max-height: unset !important;
	min-height: unset !important;
	transform: unset !important;
	animation: unset !important;
	z-index: 101 !important;
	pointer-events: none !important;
}


/* ~~~~		19.		WATERMARK						~~~~ */

html:only-child > head + body > div#app-mount.appMount-3lHmkl > div.typeWindows-1za-n7.titleBar-AC4pGV.horizontalReverse-3tRjY7.flex-1O1GKY.directionRowReverse-m8IjIq.justifyStart-2NDFzi.alignStretch-DpGPf3 > div.wordmark-2iDDfm {
	color: white !important;
	display: block !important;
	position: absolute !important;
	max-width: unset !important;
	min-width: unset !important;
	width: 55px !important;
	max-height: unset !important;
	min-height: unset !important;
	height: 16px !important;
	margin: 0 !important;
	padding: 3px 9px 3px !important;
	top: 0 !important;
	left: 0 !important;
	bottom: unset !important;
	right: unset !important;
	opacity: 0.6 !important;
	visibility: visible !important;
	transform: unset !important;
	animation: unset !important;
}
html:only-child > head + body > div#app-mount.appMount-3lHmkl > div.typeWindows-1za-n7.titleBar-AC4pGV.horizontalReverse-3tRjY7.flex-1O1GKY.directionRowReverse-m8IjIq.justifyStart-2NDFzi.alignStretch-DpGPf3 > div.wordmark-2iDDfm::after {
	content: url('data:image/svg+xml; utf8, <svg width="400" height="18" version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink"><path stroke="none" fill="rgb(255, 255, 255)" fill-rule="evenodd" transform="scale(0.6,0.6) translate(5,4)" d="M58.488 0.690 C 54.786 0.948,52.503 3.334,52.961 6.466 C 53.321 8.926,55.135 10.509,58.186 11.025 C 60.205 11.366,61.177 12.097,60.818 13.004 C 60.260 14.412,57.255 14.154,55.679 12.564 L 55.440 12.323 55.340 12.411 C 55.125 12.602,52.767 14.824,52.768 14.836 C 52.768 14.843,52.842 14.938,52.932 15.047 C 55.188 17.761,58.434 18.568,61.663 17.218 C 63.879 16.291,65.049 14.673,65.056 12.523 C 65.066 9.499,63.520 7.999,59.581 7.209 C 57.730 6.838,56.956 6.245,57.139 5.336 C 57.409 3.990,59.424 3.729,61.092 4.823 C 61.328 4.978,61.513 5.126,61.754 5.350 L 61.902 5.489 63.269 4.436 C 64.021 3.857,64.640 3.372,64.645 3.357 C 64.668 3.286,63.905 2.499,63.488 2.164 C 62.141 1.082,60.367 0.559,58.488 0.690 M79.453 0.691 C 76.162 0.865,73.785 2.780,73.354 5.604 C 73.306 5.919,73.281 11.980,73.325 12.570 C 73.506 14.979,75.020 16.759,77.535 17.519 C 80.709 18.479,83.881 17.374,85.557 14.725 C 85.782 14.369,85.916 14.116,85.893 14.093 C 85.872 14.073,82.327 12.430,82.254 12.406 C 82.224 12.397,82.198 12.429,82.144 12.544 C 81.882 13.103,81.353 13.555,80.730 13.752 C 79.382 14.177,77.866 13.572,77.593 12.501 C 77.539 12.288,77.540 6.228,77.595 6.015 C 78.042 4.261,81.252 4.104,82.289 5.785 C 82.338 5.865,82.385 5.930,82.393 5.930 C 82.409 5.930,85.820 4.554,85.837 4.541 C 85.856 4.526,85.497 3.838,85.340 3.588 C 84.071 1.573,82.003 0.555,79.453 0.691 M122.233 0.698 C 118.928 0.954,116.621 2.860,116.252 5.640 C 116.198 6.046,116.207 12.646,116.263 13.000 C 116.678 15.665,118.768 17.446,121.919 17.818 C 124.720 18.149,127.505 16.687,128.743 14.235 L 128.815 14.092 128.669 14.026 C 128.589 13.989,127.762 13.608,126.832 13.177 C 125.902 12.747,125.135 12.395,125.129 12.395 C 125.122 12.395,125.079 12.471,125.032 12.564 C 124.149 14.321,121.136 14.341,120.519 12.593 L 120.453 12.407 120.447 9.350 C 120.442 6.713,120.445 6.267,120.476 6.106 C 120.814 4.288,124.035 4.054,125.172 5.764 C 125.233 5.855,125.288 5.930,125.294 5.930 C 125.318 5.930,128.710 4.554,128.727 4.537 C 128.750 4.515,128.506 4.030,128.302 3.691 C 127.042 1.592,124.822 0.498,122.233 0.698 M150.163 0.690 C 146.674 0.881,144.259 2.928,144.024 5.893 C 143.992 6.292,143.992 12.111,144.024 12.535 C 144.229 15.291,146.239 17.273,149.317 17.756 C 152.815 18.304,156.021 16.678,156.902 13.907 C 157.157 13.104,157.167 12.980,157.179 10.250 L 157.190 7.907 153.816 7.907 L 150.442 7.907 150.442 9.686 L 150.442 11.465 151.770 11.465 L 153.098 11.465 153.088 11.948 C 153.069 12.840,152.771 13.335,152.028 13.707 C 150.559 14.443,148.672 13.843,148.297 12.522 L 148.244 12.337 148.244 9.221 L 148.244 6.105 148.296 5.922 C 148.641 4.708,150.215 4.096,151.595 4.640 C 152.111 4.844,152.607 5.305,152.816 5.777 C 152.852 5.859,152.875 5.885,152.903 5.877 C 152.970 5.857,156.383 4.277,156.404 4.256 C 156.456 4.205,156.028 3.438,155.709 3.012 C 154.517 1.418,152.475 0.563,150.163 0.690 M180.081 0.700 C 176.707 0.925,174.383 2.695,173.857 5.442 C 173.796 5.758,173.758 12.153,173.814 12.721 C 174.112 15.773,176.906 17.847,180.721 17.847 C 184.496 17.847,187.238 15.831,187.594 12.794 C 187.645 12.357,187.645 6.177,187.593 5.740 C 187.221 2.553,184.063 0.434,180.081 0.700 M390.026 0.701 C 386.623 0.917,384.214 2.823,383.799 5.628 C 383.750 5.958,383.722 11.716,383.765 12.444 C 383.954 15.593,386.593 17.735,390.430 17.853 C 394.202 17.969,397.090 15.976,397.551 12.938 C 397.616 12.508,397.615 6.017,397.550 5.593 C 397.065 2.452,393.986 0.450,390.026 0.701 M249.326 4.333 C 249.326 7.601,249.328 7.786,249.366 7.797 C 249.389 7.803,250.338 8.626,251.477 9.625 C 252.615 10.624,253.554 11.442,253.564 11.442 C 253.574 11.442,253.581 9.871,253.581 7.952 L 253.581 4.462 254.948 4.471 C 256.262 4.479,256.321 4.481,256.495 4.530 C 257.918 4.924,257.953 6.870,256.547 7.343 L 256.360 7.405 255.366 7.414 L 254.372 7.422 254.372 8.954 L 254.372 10.486 255.413 10.494 C 256.589 10.503,256.592 10.504,257.000 10.704 C 258.198 11.291,258.196 13.081,256.998 13.659 C 256.517 13.891,256.654 13.884,252.716 13.884 L 249.326 13.884 249.326 15.744 L 249.326 17.605 252.831 17.604 C 256.414 17.604,256.877 17.595,257.522 17.512 C 260.168 17.172,261.703 15.747,262.103 13.259 C 262.394 11.447,261.566 9.707,259.993 8.829 C 259.761 8.699,259.762 8.700,259.877 8.639 C 260.813 8.141,261.456 6.960,261.452 5.744 C 261.445 3.299,259.914 1.508,257.419 1.024 C 256.765 0.897,256.875 0.901,252.959 0.890 L 249.326 0.881 249.326 4.333 M317.842 0.913 C 317.848 0.929,319.202 4.691,320.851 9.273 L 323.849 17.604 325.791 17.604 L 327.733 17.605 330.739 9.259 C 332.392 4.669,333.744 0.907,333.744 0.899 C 333.744 0.891,332.721 0.884,331.471 0.884 L 329.198 0.884 327.877 4.983 L 326.556 9.081 326.185 11.012 C 325.982 12.073,325.815 12.955,325.814 12.971 C 325.814 12.987,325.801 13.000,325.785 13.000 C 325.765 13.000,325.639 12.389,325.380 11.025 L 325.004 9.049 323.695 4.966 L 322.385 0.884 320.109 0.884 C 318.298 0.884,317.834 0.890,317.842 0.913 M354.349 4.333 C 354.349 7.601,354.351 7.786,354.390 7.797 C 354.412 7.803,355.362 8.626,356.500 9.625 C 357.638 10.624,358.578 11.442,358.587 11.442 C 358.597 11.442,358.605 9.871,358.605 7.952 L 358.605 4.462 359.971 4.471 C 361.286 4.479,361.344 4.481,361.519 4.530 C 362.941 4.924,362.976 6.870,361.570 7.343 L 361.384 7.405 360.390 7.414 L 359.395 7.422 359.395 8.954 L 359.395 10.486 360.436 10.494 C 361.613 10.503,361.615 10.504,362.023 10.704 C 363.221 11.291,363.220 13.081,362.021 13.659 C 361.541 13.891,361.678 13.884,357.739 13.884 L 354.349 13.884 354.349 15.744 L 354.349 17.605 357.855 17.604 C 361.438 17.604,361.900 17.595,362.546 17.512 C 365.191 17.172,366.726 15.747,367.126 13.259 C 367.418 11.447,366.589 9.707,365.017 8.829 C 364.784 8.699,364.785 8.700,364.900 8.639 C 365.836 8.141,366.479 6.960,366.475 5.744 C 366.468 3.299,364.938 1.508,362.442 1.024 C 361.788 0.897,361.898 0.901,357.983 0.890 L 354.349 0.881 354.349 4.333 M24.186 4.356 C 24.186 7.624,24.188 7.809,24.227 7.820 C 24.249 7.827,25.199 8.649,26.337 9.648 C 27.476 10.647,28.415 11.465,28.424 11.465 C 28.434 11.465,28.442 9.895,28.442 7.975 L 28.442 4.485 29.808 4.494 C 31.123 4.502,31.181 4.505,31.356 4.553 C 32.778 4.947,32.813 6.893,31.407 7.366 L 31.221 7.429 30.227 7.437 L 29.233 7.445 29.233 8.977 L 29.233 10.509 30.273 10.517 C 31.450 10.527,31.452 10.527,31.860 10.727 C 33.058 11.314,33.057 13.104,31.858 13.682 C 31.378 13.914,31.515 13.907,27.576 13.907 L 24.186 13.907 24.186 15.767 L 24.186 17.628 27.692 17.627 C 31.275 17.627,31.737 17.618,32.383 17.535 C 35.028 17.195,36.564 15.770,36.964 13.282 C 37.255 11.471,36.426 9.731,34.854 8.852 C 34.621 8.722,34.622 8.724,34.738 8.662 C 35.674 8.165,36.316 6.984,36.312 5.767 C 36.305 3.322,34.775 1.531,32.279 1.047 C 31.625 0.921,31.735 0.924,27.820 0.914 L 24.186 0.904 24.186 4.356 M42.922 0.925 C 42.916 0.934,41.608 4.678,40.015 9.244 C 38.423 13.811,37.113 17.565,37.104 17.587 C 37.089 17.626,37.206 17.628,39.368 17.628 C 41.519 17.628,41.649 17.626,41.660 17.587 C 41.667 17.565,41.898 16.817,42.173 15.925 C 42.449 15.034,42.674 14.298,42.674 14.292 C 42.674 14.285,43.673 14.279,44.894 14.279 L 47.114 14.279 47.346 14.994 C 47.474 15.388,47.718 16.141,47.888 16.669 L 48.198 17.628 50.473 17.628 C 52.284 17.628,52.747 17.622,52.739 17.599 C 52.734 17.583,51.390 13.821,49.754 9.238 L 46.779 0.907 44.856 0.907 C 43.798 0.907,42.928 0.915,42.922 0.925 M66.860 9.267 L 66.860 17.628 68.977 17.628 L 71.093 17.628 71.093 9.267 L 71.093 0.907 68.977 0.907 L 66.860 0.907 66.860 9.267 M103.247 9.239 C 101.649 13.821,100.337 17.583,100.331 17.599 C 100.323 17.622,100.786 17.628,102.598 17.628 L 104.875 17.628 105.348 16.099 C 105.609 15.258,105.841 14.504,105.865 14.424 L 105.909 14.279 108.128 14.279 L 110.346 14.279 110.448 14.599 C 110.504 14.775,110.747 15.528,110.989 16.273 L 111.427 17.628 113.704 17.628 C 115.516 17.628,115.980 17.622,115.971 17.599 C 115.965 17.583,114.622 13.821,112.986 9.239 L 110.012 0.908 108.081 0.908 L 106.151 0.908 103.247 9.239 M130.326 9.267 L 130.326 17.628 132.453 17.628 L 134.581 17.628 134.581 14.740 L 134.581 11.851 134.644 11.761 C 134.696 11.686,134.711 11.676,134.731 11.705 C 134.745 11.723,135.703 13.064,136.860 14.683 L 138.965 17.627 141.648 17.627 C 144.025 17.628,144.329 17.624,144.317 17.593 C 144.308 17.568,137.994 9.268,137.789 9.011 C 137.778 8.996,139.071 7.397,141.060 4.969 C 142.869 2.759,144.349 0.941,144.349 0.929 C 144.349 0.915,143.342 0.907,141.715 0.908 L 139.081 0.909 136.837 3.975 L 134.593 7.041 134.587 3.974 L 134.581 0.907 132.453 0.907 L 130.326 0.907 130.326 9.267 M159.116 9.266 L 159.116 17.628 161.256 17.628 L 163.395 17.628 163.395 14.977 L 163.395 12.326 163.762 12.326 L 164.129 12.326 166.058 14.976 L 167.988 17.626 170.625 17.627 C 172.875 17.628,173.259 17.623,173.248 17.595 C 173.241 17.577,172.224 16.288,170.987 14.730 C 169.750 13.172,168.747 11.894,168.759 11.890 C 170.569 11.276,171.641 9.837,171.917 7.651 C 172.346 4.246,170.890 1.873,167.930 1.154 C 166.981 0.924,166.973 0.924,162.785 0.913 L 159.116 0.904 159.116 9.266 M189.767 6.704 C 189.767 12.984,189.763 12.742,189.893 13.354 C 190.564 16.526,194.059 18.450,197.907 17.766 C 200.535 17.299,202.429 15.647,202.943 13.372 C 203.088 12.729,203.079 13.167,203.087 6.750 L 203.094 0.907 200.955 0.907 L 198.815 0.907 198.808 6.599 C 198.801 11.986,198.798 12.299,198.759 12.453 C 198.236 14.492,194.735 14.570,194.112 12.558 L 194.058 12.384 194.052 6.645 L 194.046 0.907 191.907 0.907 L 189.767 0.907 189.767 6.704 M205.558 9.267 L 205.558 17.628 207.674 17.628 L 209.791 17.628 209.790 14.238 L 209.790 10.849 209.526 9.285 C 209.175 7.205,209.135 7.199,210.080 9.366 L 210.797 11.012 212.694 14.320 L 214.591 17.628 216.726 17.628 L 218.860 17.628 218.860 9.267 L 218.860 0.907 216.756 0.907 L 214.651 0.907 214.651 4.682 C 214.651 7.186,214.659 8.500,214.675 8.587 C 214.747 8.973,215.111 11.338,215.102 11.354 C 215.060 11.421,214.969 11.226,214.320 9.692 L 213.610 8.012 211.600 4.465 L 209.590 0.919 207.574 0.913 L 205.558 0.907 205.558 9.267 M221.488 4.334 C 221.488 7.579,221.491 7.763,221.529 7.774 C 221.551 7.780,222.501 8.603,223.640 9.602 C 224.778 10.601,225.717 11.418,225.727 11.418 C 225.736 11.419,225.744 9.948,225.744 8.150 L 225.744 4.881 227.087 4.889 L 228.430 4.897 228.663 4.960 C 229.357 5.146,229.767 5.539,229.922 6.163 C 229.963 6.328,229.965 6.490,229.965 9.244 L 229.965 12.151 229.913 12.349 C 229.704 13.139,229.110 13.560,228.105 13.628 C 227.923 13.641,226.390 13.651,224.634 13.651 L 221.488 13.651 221.488 15.640 L 221.488 17.628 224.738 17.628 C 228.530 17.628,228.747 17.619,229.628 17.442 C 232.189 16.927,233.789 15.382,234.170 13.058 C 234.229 12.694,234.263 6.624,234.209 5.965 C 233.966 2.989,231.727 1.114,228.198 0.930 C 227.951 0.918,226.369 0.907,224.622 0.907 L 221.488 0.907 221.488 4.334 M261.518 0.936 C 261.525 0.952,262.834 3.230,264.428 5.997 L 267.326 11.030 267.326 14.329 L 267.326 17.628 269.453 17.628 L 271.581 17.628 271.581 14.331 L 271.581 11.034 274.491 6.000 C 276.091 3.232,277.406 0.953,277.412 0.937 C 277.421 0.913,276.956 0.907,274.937 0.907 L 272.450 0.907 270.952 3.953 C 270.128 5.629,269.448 7.000,269.442 6.999 C 269.435 6.999,268.756 5.628,267.932 3.953 L 266.435 0.907 263.971 0.907 C 262.009 0.907,261.509 0.913,261.518 0.936 M290.535 4.334 C 290.535 7.579,290.537 7.763,290.576 7.774 C 290.598 7.780,291.548 8.603,292.686 9.602 C 293.824 10.601,294.764 11.418,294.773 11.418 C 294.783 11.419,294.791 9.948,294.791 8.150 L 294.791 4.881 296.134 4.889 L 297.477 4.897 297.709 4.960 C 298.403 5.146,298.814 5.539,298.968 6.163 C 299.009 6.328,299.012 6.490,299.012 9.244 L 299.012 12.151 298.959 12.349 C 298.751 13.139,298.157 13.560,297.151 13.628 C 296.970 13.641,295.436 13.651,293.680 13.651 L 290.535 13.651 290.535 15.640 L 290.535 17.628 293.785 17.628 C 297.577 17.628,297.794 17.619,298.674 17.442 C 301.235 16.927,302.836 15.382,303.216 13.058 C 303.276 12.694,303.310 6.624,303.256 5.965 C 303.013 2.989,300.774 1.114,297.244 0.930 C 296.998 0.918,295.416 0.907,293.669 0.907 L 290.535 0.907 290.535 4.334 M305.512 9.267 L 305.512 17.628 311.337 17.628 L 317.163 17.628 317.163 15.616 L 317.163 13.605 313.488 13.605 L 309.814 13.605 309.814 12.372 L 309.814 11.140 313.186 11.140 L 316.558 11.140 316.558 9.302 L 316.558 7.465 313.186 7.465 L 309.814 7.465 309.814 6.186 L 309.814 4.907 313.488 4.907 L 317.163 4.907 317.163 2.907 L 317.163 0.907 311.337 0.907 L 305.512 0.907 305.512 9.267 M334.814 9.267 L 334.814 17.628 336.942 17.628 L 339.070 17.628 339.070 9.267 L 339.070 0.907 336.942 0.907 L 334.814 0.907 334.814 9.267 M341.674 9.267 L 341.674 17.628 347.198 17.628 L 352.721 17.628 352.721 15.523 L 352.721 13.419 349.326 13.419 L 345.930 13.419 345.930 7.163 L 345.930 0.907 343.802 0.907 L 341.674 0.907 341.674 9.267 M369.070 9.267 L 369.070 17.628 371.221 17.628 L 373.372 17.628 373.372 14.977 L 373.372 12.326 373.738 12.327 L 374.105 12.328 376.034 14.978 L 377.963 17.628 380.598 17.628 C 382.047 17.628,383.232 17.620,383.232 17.610 C 383.232 17.601,382.367 16.505,381.311 15.174 C 380.254 13.844,379.235 12.561,379.047 12.324 L 378.704 11.891 378.916 11.815 C 380.927 11.094,382.015 9.124,381.947 6.327 C 381.871 3.234,380.093 1.352,376.892 0.978 C 376.397 0.920,375.607 0.908,372.424 0.907 L 369.070 0.907 369.070 9.267 M87.395 4.380 C 87.395 7.647,87.398 7.832,87.436 7.843 C 87.458 7.850,88.408 8.672,89.547 9.672 C 90.685 10.671,91.624 11.488,91.634 11.488 C 91.643 11.488,91.651 9.918,91.651 7.998 L 91.651 4.508 93.017 4.517 C 94.332 4.526,94.391 4.528,94.565 4.576 C 95.987 4.971,96.023 6.916,94.616 7.389 L 94.430 7.452 93.436 7.460 L 92.442 7.468 92.442 9.000 L 92.442 10.532 93.483 10.541 C 94.659 10.550,94.662 10.550,95.070 10.750 C 96.268 11.337,96.266 13.127,95.067 13.706 C 94.587 13.937,94.724 13.930,90.785 13.930 L 87.395 13.930 87.395 15.791 L 87.395 17.651 90.901 17.651 C 94.484 17.650,94.947 17.641,95.592 17.558 C 98.238 17.219,99.773 15.793,100.173 13.306 C 100.464 11.494,99.636 9.754,98.063 8.875 C 97.831 8.745,97.832 8.747,97.947 8.686 C 98.883 8.188,99.526 7.007,99.522 5.791 C 99.514 3.345,97.984 1.554,95.488 1.071 C 94.834 0.944,94.944 0.947,91.029 0.937 L 87.395 0.927 87.395 4.380 M181.387 4.605 C 182.483 4.791,183.204 5.337,183.359 6.098 C 183.414 6.371,183.414 12.174,183.358 12.426 C 182.924 14.391,178.570 14.432,178.069 12.475 C 178.004 12.220,177.997 6.370,178.061 6.086 C 178.311 4.984,179.776 4.331,181.387 4.605 M391.352 4.603 C 392.415 4.786,393.110 5.288,393.318 6.023 C 393.384 6.258,393.384 12.254,393.318 12.488 C 392.775 14.411,388.490 14.392,388.036 12.464 C 387.983 12.238,387.982 6.267,388.035 6.057 C 388.309 4.975,389.775 4.332,391.352 4.603 M166.461 4.949 C 168.323 5.517,168.296 8.092,166.423 8.599 L 166.198 8.660 164.797 8.669 L 163.395 8.678 163.395 6.780 L 163.395 4.881 164.843 4.889 C 166.263 4.897,166.294 4.898,166.461 4.949 M376.423 4.947 C 378.081 5.414,378.313 7.706,376.779 8.453 C 376.357 8.659,376.206 8.674,374.634 8.674 L 373.372 8.674 373.372 6.778 L 373.372 4.882 374.808 4.889 C 376.199 4.896,376.250 4.898,376.423 4.947 M44.953 5.669 C 44.953 5.679,45.210 6.770,45.523 8.093 C 45.837 9.416,46.093 10.501,46.093 10.505 C 46.093 10.509,45.538 10.512,44.859 10.512 C 43.881 10.512,43.626 10.506,43.635 10.483 C 43.641 10.467,43.916 9.373,44.247 8.052 C 44.823 5.756,44.851 5.651,44.901 5.651 C 44.930 5.651,44.953 5.659,44.953 5.669 M108.742 8.052 C 109.054 9.373,109.314 10.467,109.320 10.483 C 109.328 10.506,109.073 10.512,108.093 10.512 C 107.113 10.512,106.858 10.506,106.865 10.483 C 106.871 10.467,107.147 9.373,107.478 8.052 C 108.029 5.862,108.085 5.651,108.128 5.651 C 108.171 5.651,108.222 5.849,108.742 8.052 M5.419 9.453 L 5.419 11.465 9.105 11.465 L 12.791 11.465 12.791 9.453 L 12.791 7.442 9.105 7.442 L 5.419 7.442 5.419 9.453"></path></svg>') !important;
	display: inline !important;
	position: absolute !important;
	top: unset !important;
	left: unset !important;
	bottom: unset !important;
	right: unset !important;
	opacity: 1 !important;
	padding: 0 !important;
	margin: 0 !important;
	visibility: visible !important;
	transform: unset !important;
	animation: unset !important;
}
html:only-child > head + body > div#app-mount.appMount-3lHmkl > div.app-1q1i1E > div.app-2rEoOp > div.layers-3iHuyZ.layers-3q14ss > div.layer-3QrUeG.baseLayer-35bLyl + div.layer-3QrUeG > div.standardSidebarView-3F1I7i::after {
	content: url('data:image/svg+xml; utf8, <svg width="400" height="18" version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink"><path stroke="none" fill="rgb(255, 255, 255)" fill-rule="evenodd" d="M58.488 0.690 C 54.786 0.948,52.503 3.334,52.961 6.466 C 53.321 8.926,55.135 10.509,58.186 11.025 C 60.205 11.366,61.177 12.097,60.818 13.004 C 60.260 14.412,57.255 14.154,55.679 12.564 L 55.440 12.323 55.340 12.411 C 55.125 12.602,52.767 14.824,52.768 14.836 C 52.768 14.843,52.842 14.938,52.932 15.047 C 55.188 17.761,58.434 18.568,61.663 17.218 C 63.879 16.291,65.049 14.673,65.056 12.523 C 65.066 9.499,63.520 7.999,59.581 7.209 C 57.730 6.838,56.956 6.245,57.139 5.336 C 57.409 3.990,59.424 3.729,61.092 4.823 C 61.328 4.978,61.513 5.126,61.754 5.350 L 61.902 5.489 63.269 4.436 C 64.021 3.857,64.640 3.372,64.645 3.357 C 64.668 3.286,63.905 2.499,63.488 2.164 C 62.141 1.082,60.367 0.559,58.488 0.690 M79.453 0.691 C 76.162 0.865,73.785 2.780,73.354 5.604 C 73.306 5.919,73.281 11.980,73.325 12.570 C 73.506 14.979,75.020 16.759,77.535 17.519 C 80.709 18.479,83.881 17.374,85.557 14.725 C 85.782 14.369,85.916 14.116,85.893 14.093 C 85.872 14.073,82.327 12.430,82.254 12.406 C 82.224 12.397,82.198 12.429,82.144 12.544 C 81.882 13.103,81.353 13.555,80.730 13.752 C 79.382 14.177,77.866 13.572,77.593 12.501 C 77.539 12.288,77.540 6.228,77.595 6.015 C 78.042 4.261,81.252 4.104,82.289 5.785 C 82.338 5.865,82.385 5.930,82.393 5.930 C 82.409 5.930,85.820 4.554,85.837 4.541 C 85.856 4.526,85.497 3.838,85.340 3.588 C 84.071 1.573,82.003 0.555,79.453 0.691 M122.233 0.698 C 118.928 0.954,116.621 2.860,116.252 5.640 C 116.198 6.046,116.207 12.646,116.263 13.000 C 116.678 15.665,118.768 17.446,121.919 17.818 C 124.720 18.149,127.505 16.687,128.743 14.235 L 128.815 14.092 128.669 14.026 C 128.589 13.989,127.762 13.608,126.832 13.177 C 125.902 12.747,125.135 12.395,125.129 12.395 C 125.122 12.395,125.079 12.471,125.032 12.564 C 124.149 14.321,121.136 14.341,120.519 12.593 L 120.453 12.407 120.447 9.350 C 120.442 6.713,120.445 6.267,120.476 6.106 C 120.814 4.288,124.035 4.054,125.172 5.764 C 125.233 5.855,125.288 5.930,125.294 5.930 C 125.318 5.930,128.710 4.554,128.727 4.537 C 128.750 4.515,128.506 4.030,128.302 3.691 C 127.042 1.592,124.822 0.498,122.233 0.698 M150.163 0.690 C 146.674 0.881,144.259 2.928,144.024 5.893 C 143.992 6.292,143.992 12.111,144.024 12.535 C 144.229 15.291,146.239 17.273,149.317 17.756 C 152.815 18.304,156.021 16.678,156.902 13.907 C 157.157 13.104,157.167 12.980,157.179 10.250 L 157.190 7.907 153.816 7.907 L 150.442 7.907 150.442 9.686 L 150.442 11.465 151.770 11.465 L 153.098 11.465 153.088 11.948 C 153.069 12.840,152.771 13.335,152.028 13.707 C 150.559 14.443,148.672 13.843,148.297 12.522 L 148.244 12.337 148.244 9.221 L 148.244 6.105 148.296 5.922 C 148.641 4.708,150.215 4.096,151.595 4.640 C 152.111 4.844,152.607 5.305,152.816 5.777 C 152.852 5.859,152.875 5.885,152.903 5.877 C 152.970 5.857,156.383 4.277,156.404 4.256 C 156.456 4.205,156.028 3.438,155.709 3.012 C 154.517 1.418,152.475 0.563,150.163 0.690 M180.081 0.700 C 176.707 0.925,174.383 2.695,173.857 5.442 C 173.796 5.758,173.758 12.153,173.814 12.721 C 174.112 15.773,176.906 17.847,180.721 17.847 C 184.496 17.847,187.238 15.831,187.594 12.794 C 187.645 12.357,187.645 6.177,187.593 5.740 C 187.221 2.553,184.063 0.434,180.081 0.700 M390.026 0.701 C 386.623 0.917,384.214 2.823,383.799 5.628 C 383.750 5.958,383.722 11.716,383.765 12.444 C 383.954 15.593,386.593 17.735,390.430 17.853 C 394.202 17.969,397.090 15.976,397.551 12.938 C 397.616 12.508,397.615 6.017,397.550 5.593 C 397.065 2.452,393.986 0.450,390.026 0.701 M249.326 4.333 C 249.326 7.601,249.328 7.786,249.366 7.797 C 249.389 7.803,250.338 8.626,251.477 9.625 C 252.615 10.624,253.554 11.442,253.564 11.442 C 253.574 11.442,253.581 9.871,253.581 7.952 L 253.581 4.462 254.948 4.471 C 256.262 4.479,256.321 4.481,256.495 4.530 C 257.918 4.924,257.953 6.870,256.547 7.343 L 256.360 7.405 255.366 7.414 L 254.372 7.422 254.372 8.954 L 254.372 10.486 255.413 10.494 C 256.589 10.503,256.592 10.504,257.000 10.704 C 258.198 11.291,258.196 13.081,256.998 13.659 C 256.517 13.891,256.654 13.884,252.716 13.884 L 249.326 13.884 249.326 15.744 L 249.326 17.605 252.831 17.604 C 256.414 17.604,256.877 17.595,257.522 17.512 C 260.168 17.172,261.703 15.747,262.103 13.259 C 262.394 11.447,261.566 9.707,259.993 8.829 C 259.761 8.699,259.762 8.700,259.877 8.639 C 260.813 8.141,261.456 6.960,261.452 5.744 C 261.445 3.299,259.914 1.508,257.419 1.024 C 256.765 0.897,256.875 0.901,252.959 0.890 L 249.326 0.881 249.326 4.333 M317.842 0.913 C 317.848 0.929,319.202 4.691,320.851 9.273 L 323.849 17.604 325.791 17.604 L 327.733 17.605 330.739 9.259 C 332.392 4.669,333.744 0.907,333.744 0.899 C 333.744 0.891,332.721 0.884,331.471 0.884 L 329.198 0.884 327.877 4.983 L 326.556 9.081 326.185 11.012 C 325.982 12.073,325.815 12.955,325.814 12.971 C 325.814 12.987,325.801 13.000,325.785 13.000 C 325.765 13.000,325.639 12.389,325.380 11.025 L 325.004 9.049 323.695 4.966 L 322.385 0.884 320.109 0.884 C 318.298 0.884,317.834 0.890,317.842 0.913 M354.349 4.333 C 354.349 7.601,354.351 7.786,354.390 7.797 C 354.412 7.803,355.362 8.626,356.500 9.625 C 357.638 10.624,358.578 11.442,358.587 11.442 C 358.597 11.442,358.605 9.871,358.605 7.952 L 358.605 4.462 359.971 4.471 C 361.286 4.479,361.344 4.481,361.519 4.530 C 362.941 4.924,362.976 6.870,361.570 7.343 L 361.384 7.405 360.390 7.414 L 359.395 7.422 359.395 8.954 L 359.395 10.486 360.436 10.494 C 361.613 10.503,361.615 10.504,362.023 10.704 C 363.221 11.291,363.220 13.081,362.021 13.659 C 361.541 13.891,361.678 13.884,357.739 13.884 L 354.349 13.884 354.349 15.744 L 354.349 17.605 357.855 17.604 C 361.438 17.604,361.900 17.595,362.546 17.512 C 365.191 17.172,366.726 15.747,367.126 13.259 C 367.418 11.447,366.589 9.707,365.017 8.829 C 364.784 8.699,364.785 8.700,364.900 8.639 C 365.836 8.141,366.479 6.960,366.475 5.744 C 366.468 3.299,364.938 1.508,362.442 1.024 C 361.788 0.897,361.898 0.901,357.983 0.890 L 354.349 0.881 354.349 4.333 M24.186 4.356 C 24.186 7.624,24.188 7.809,24.227 7.820 C 24.249 7.827,25.199 8.649,26.337 9.648 C 27.476 10.647,28.415 11.465,28.424 11.465 C 28.434 11.465,28.442 9.895,28.442 7.975 L 28.442 4.485 29.808 4.494 C 31.123 4.502,31.181 4.505,31.356 4.553 C 32.778 4.947,32.813 6.893,31.407 7.366 L 31.221 7.429 30.227 7.437 L 29.233 7.445 29.233 8.977 L 29.233 10.509 30.273 10.517 C 31.450 10.527,31.452 10.527,31.860 10.727 C 33.058 11.314,33.057 13.104,31.858 13.682 C 31.378 13.914,31.515 13.907,27.576 13.907 L 24.186 13.907 24.186 15.767 L 24.186 17.628 27.692 17.627 C 31.275 17.627,31.737 17.618,32.383 17.535 C 35.028 17.195,36.564 15.770,36.964 13.282 C 37.255 11.471,36.426 9.731,34.854 8.852 C 34.621 8.722,34.622 8.724,34.738 8.662 C 35.674 8.165,36.316 6.984,36.312 5.767 C 36.305 3.322,34.775 1.531,32.279 1.047 C 31.625 0.921,31.735 0.924,27.820 0.914 L 24.186 0.904 24.186 4.356 M42.922 0.925 C 42.916 0.934,41.608 4.678,40.015 9.244 C 38.423 13.811,37.113 17.565,37.104 17.587 C 37.089 17.626,37.206 17.628,39.368 17.628 C 41.519 17.628,41.649 17.626,41.660 17.587 C 41.667 17.565,41.898 16.817,42.173 15.925 C 42.449 15.034,42.674 14.298,42.674 14.292 C 42.674 14.285,43.673 14.279,44.894 14.279 L 47.114 14.279 47.346 14.994 C 47.474 15.388,47.718 16.141,47.888 16.669 L 48.198 17.628 50.473 17.628 C 52.284 17.628,52.747 17.622,52.739 17.599 C 52.734 17.583,51.390 13.821,49.754 9.238 L 46.779 0.907 44.856 0.907 C 43.798 0.907,42.928 0.915,42.922 0.925 M66.860 9.267 L 66.860 17.628 68.977 17.628 L 71.093 17.628 71.093 9.267 L 71.093 0.907 68.977 0.907 L 66.860 0.907 66.860 9.267 M103.247 9.239 C 101.649 13.821,100.337 17.583,100.331 17.599 C 100.323 17.622,100.786 17.628,102.598 17.628 L 104.875 17.628 105.348 16.099 C 105.609 15.258,105.841 14.504,105.865 14.424 L 105.909 14.279 108.128 14.279 L 110.346 14.279 110.448 14.599 C 110.504 14.775,110.747 15.528,110.989 16.273 L 111.427 17.628 113.704 17.628 C 115.516 17.628,115.980 17.622,115.971 17.599 C 115.965 17.583,114.622 13.821,112.986 9.239 L 110.012 0.908 108.081 0.908 L 106.151 0.908 103.247 9.239 M130.326 9.267 L 130.326 17.628 132.453 17.628 L 134.581 17.628 134.581 14.740 L 134.581 11.851 134.644 11.761 C 134.696 11.686,134.711 11.676,134.731 11.705 C 134.745 11.723,135.703 13.064,136.860 14.683 L 138.965 17.627 141.648 17.627 C 144.025 17.628,144.329 17.624,144.317 17.593 C 144.308 17.568,137.994 9.268,137.789 9.011 C 137.778 8.996,139.071 7.397,141.060 4.969 C 142.869 2.759,144.349 0.941,144.349 0.929 C 144.349 0.915,143.342 0.907,141.715 0.908 L 139.081 0.909 136.837 3.975 L 134.593 7.041 134.587 3.974 L 134.581 0.907 132.453 0.907 L 130.326 0.907 130.326 9.267 M159.116 9.266 L 159.116 17.628 161.256 17.628 L 163.395 17.628 163.395 14.977 L 163.395 12.326 163.762 12.326 L 164.129 12.326 166.058 14.976 L 167.988 17.626 170.625 17.627 C 172.875 17.628,173.259 17.623,173.248 17.595 C 173.241 17.577,172.224 16.288,170.987 14.730 C 169.750 13.172,168.747 11.894,168.759 11.890 C 170.569 11.276,171.641 9.837,171.917 7.651 C 172.346 4.246,170.890 1.873,167.930 1.154 C 166.981 0.924,166.973 0.924,162.785 0.913 L 159.116 0.904 159.116 9.266 M189.767 6.704 C 189.767 12.984,189.763 12.742,189.893 13.354 C 190.564 16.526,194.059 18.450,197.907 17.766 C 200.535 17.299,202.429 15.647,202.943 13.372 C 203.088 12.729,203.079 13.167,203.087 6.750 L 203.094 0.907 200.955 0.907 L 198.815 0.907 198.808 6.599 C 198.801 11.986,198.798 12.299,198.759 12.453 C 198.236 14.492,194.735 14.570,194.112 12.558 L 194.058 12.384 194.052 6.645 L 194.046 0.907 191.907 0.907 L 189.767 0.907 189.767 6.704 M205.558 9.267 L 205.558 17.628 207.674 17.628 L 209.791 17.628 209.790 14.238 L 209.790 10.849 209.526 9.285 C 209.175 7.205,209.135 7.199,210.080 9.366 L 210.797 11.012 212.694 14.320 L 214.591 17.628 216.726 17.628 L 218.860 17.628 218.860 9.267 L 218.860 0.907 216.756 0.907 L 214.651 0.907 214.651 4.682 C 214.651 7.186,214.659 8.500,214.675 8.587 C 214.747 8.973,215.111 11.338,215.102 11.354 C 215.060 11.421,214.969 11.226,214.320 9.692 L 213.610 8.012 211.600 4.465 L 209.590 0.919 207.574 0.913 L 205.558 0.907 205.558 9.267 M221.488 4.334 C 221.488 7.579,221.491 7.763,221.529 7.774 C 221.551 7.780,222.501 8.603,223.640 9.602 C 224.778 10.601,225.717 11.418,225.727 11.418 C 225.736 11.419,225.744 9.948,225.744 8.150 L 225.744 4.881 227.087 4.889 L 228.430 4.897 228.663 4.960 C 229.357 5.146,229.767 5.539,229.922 6.163 C 229.963 6.328,229.965 6.490,229.965 9.244 L 229.965 12.151 229.913 12.349 C 229.704 13.139,229.110 13.560,228.105 13.628 C 227.923 13.641,226.390 13.651,224.634 13.651 L 221.488 13.651 221.488 15.640 L 221.488 17.628 224.738 17.628 C 228.530 17.628,228.747 17.619,229.628 17.442 C 232.189 16.927,233.789 15.382,234.170 13.058 C 234.229 12.694,234.263 6.624,234.209 5.965 C 233.966 2.989,231.727 1.114,228.198 0.930 C 227.951 0.918,226.369 0.907,224.622 0.907 L 221.488 0.907 221.488 4.334 M261.518 0.936 C 261.525 0.952,262.834 3.230,264.428 5.997 L 267.326 11.030 267.326 14.329 L 267.326 17.628 269.453 17.628 L 271.581 17.628 271.581 14.331 L 271.581 11.034 274.491 6.000 C 276.091 3.232,277.406 0.953,277.412 0.937 C 277.421 0.913,276.956 0.907,274.937 0.907 L 272.450 0.907 270.952 3.953 C 270.128 5.629,269.448 7.000,269.442 6.999 C 269.435 6.999,268.756 5.628,267.932 3.953 L 266.435 0.907 263.971 0.907 C 262.009 0.907,261.509 0.913,261.518 0.936 M290.535 4.334 C 290.535 7.579,290.537 7.763,290.576 7.774 C 290.598 7.780,291.548 8.603,292.686 9.602 C 293.824 10.601,294.764 11.418,294.773 11.418 C 294.783 11.419,294.791 9.948,294.791 8.150 L 294.791 4.881 296.134 4.889 L 297.477 4.897 297.709 4.960 C 298.403 5.146,298.814 5.539,298.968 6.163 C 299.009 6.328,299.012 6.490,299.012 9.244 L 299.012 12.151 298.959 12.349 C 298.751 13.139,298.157 13.560,297.151 13.628 C 296.970 13.641,295.436 13.651,293.680 13.651 L 290.535 13.651 290.535 15.640 L 290.535 17.628 293.785 17.628 C 297.577 17.628,297.794 17.619,298.674 17.442 C 301.235 16.927,302.836 15.382,303.216 13.058 C 303.276 12.694,303.310 6.624,303.256 5.965 C 303.013 2.989,300.774 1.114,297.244 0.930 C 296.998 0.918,295.416 0.907,293.669 0.907 L 290.535 0.907 290.535 4.334 M305.512 9.267 L 305.512 17.628 311.337 17.628 L 317.163 17.628 317.163 15.616 L 317.163 13.605 313.488 13.605 L 309.814 13.605 309.814 12.372 L 309.814 11.140 313.186 11.140 L 316.558 11.140 316.558 9.302 L 316.558 7.465 313.186 7.465 L 309.814 7.465 309.814 6.186 L 309.814 4.907 313.488 4.907 L 317.163 4.907 317.163 2.907 L 317.163 0.907 311.337 0.907 L 305.512 0.907 305.512 9.267 M334.814 9.267 L 334.814 17.628 336.942 17.628 L 339.070 17.628 339.070 9.267 L 339.070 0.907 336.942 0.907 L 334.814 0.907 334.814 9.267 M341.674 9.267 L 341.674 17.628 347.198 17.628 L 352.721 17.628 352.721 15.523 L 352.721 13.419 349.326 13.419 L 345.930 13.419 345.930 7.163 L 345.930 0.907 343.802 0.907 L 341.674 0.907 341.674 9.267 M369.070 9.267 L 369.070 17.628 371.221 17.628 L 373.372 17.628 373.372 14.977 L 373.372 12.326 373.738 12.327 L 374.105 12.328 376.034 14.978 L 377.963 17.628 380.598 17.628 C 382.047 17.628,383.232 17.620,383.232 17.610 C 383.232 17.601,382.367 16.505,381.311 15.174 C 380.254 13.844,379.235 12.561,379.047 12.324 L 378.704 11.891 378.916 11.815 C 380.927 11.094,382.015 9.124,381.947 6.327 C 381.871 3.234,380.093 1.352,376.892 0.978 C 376.397 0.920,375.607 0.908,372.424 0.907 L 369.070 0.907 369.070 9.267 M87.395 4.380 C 87.395 7.647,87.398 7.832,87.436 7.843 C 87.458 7.850,88.408 8.672,89.547 9.672 C 90.685 10.671,91.624 11.488,91.634 11.488 C 91.643 11.488,91.651 9.918,91.651 7.998 L 91.651 4.508 93.017 4.517 C 94.332 4.526,94.391 4.528,94.565 4.576 C 95.987 4.971,96.023 6.916,94.616 7.389 L 94.430 7.452 93.436 7.460 L 92.442 7.468 92.442 9.000 L 92.442 10.532 93.483 10.541 C 94.659 10.550,94.662 10.550,95.070 10.750 C 96.268 11.337,96.266 13.127,95.067 13.706 C 94.587 13.937,94.724 13.930,90.785 13.930 L 87.395 13.930 87.395 15.791 L 87.395 17.651 90.901 17.651 C 94.484 17.650,94.947 17.641,95.592 17.558 C 98.238 17.219,99.773 15.793,100.173 13.306 C 100.464 11.494,99.636 9.754,98.063 8.875 C 97.831 8.745,97.832 8.747,97.947 8.686 C 98.883 8.188,99.526 7.007,99.522 5.791 C 99.514 3.345,97.984 1.554,95.488 1.071 C 94.834 0.944,94.944 0.947,91.029 0.937 L 87.395 0.927 87.395 4.380 M181.387 4.605 C 182.483 4.791,183.204 5.337,183.359 6.098 C 183.414 6.371,183.414 12.174,183.358 12.426 C 182.924 14.391,178.570 14.432,178.069 12.475 C 178.004 12.220,177.997 6.370,178.061 6.086 C 178.311 4.984,179.776 4.331,181.387 4.605 M391.352 4.603 C 392.415 4.786,393.110 5.288,393.318 6.023 C 393.384 6.258,393.384 12.254,393.318 12.488 C 392.775 14.411,388.490 14.392,388.036 12.464 C 387.983 12.238,387.982 6.267,388.035 6.057 C 388.309 4.975,389.775 4.332,391.352 4.603 M166.461 4.949 C 168.323 5.517,168.296 8.092,166.423 8.599 L 166.198 8.660 164.797 8.669 L 163.395 8.678 163.395 6.780 L 163.395 4.881 164.843 4.889 C 166.263 4.897,166.294 4.898,166.461 4.949 M376.423 4.947 C 378.081 5.414,378.313 7.706,376.779 8.453 C 376.357 8.659,376.206 8.674,374.634 8.674 L 373.372 8.674 373.372 6.778 L 373.372 4.882 374.808 4.889 C 376.199 4.896,376.250 4.898,376.423 4.947 M44.953 5.669 C 44.953 5.679,45.210 6.770,45.523 8.093 C 45.837 9.416,46.093 10.501,46.093 10.505 C 46.093 10.509,45.538 10.512,44.859 10.512 C 43.881 10.512,43.626 10.506,43.635 10.483 C 43.641 10.467,43.916 9.373,44.247 8.052 C 44.823 5.756,44.851 5.651,44.901 5.651 C 44.930 5.651,44.953 5.659,44.953 5.669 M108.742 8.052 C 109.054 9.373,109.314 10.467,109.320 10.483 C 109.328 10.506,109.073 10.512,108.093 10.512 C 107.113 10.512,106.858 10.506,106.865 10.483 C 106.871 10.467,107.147 9.373,107.478 8.052 C 108.029 5.862,108.085 5.651,108.128 5.651 C 108.171 5.651,108.222 5.849,108.742 8.052"></path></svg>') !important;
	display: inline !important;
	position: absolute !important;
	left: unset !important;
	bottom: 7px !important;
	top: unset !important;
	right: 15px !important;
	opacity: 0.3 !important;
	padding: 0 !important;
	margin: 0 !important;
	visibility: visible !important;
	transform: unset !important;
	animation: unset !important;
}
html:only-child > head + body > div#app-mount.appMount-3lHmkl > div.app-1q1i1E > div.app-2rEoOp > div.layers-3iHuyZ.layers-3q14ss > div.layer-3QrUeG.baseLayer-35bLyl + div.layer-3QrUeG > div.standardSidebarView-3F1I7i > div.sidebarRegion-VFTUkN > div.sidebarRegionScroller-3MXcoP.thin-1ybCId.scrollerBase-289Jih.fade-2kXiP2 > nav.sidebar-CFHs9e > div.side-8zPYf6 > div.info-1VyQPT {
	position: relative !important;
}
html:only-child > head + body > div#app-mount.appMount-3lHmkl > div.app-1q1i1E > div.app-2rEoOp > div.layers-3iHuyZ.layers-3q14ss > div.layer-3QrUeG.baseLayer-35bLyl + div.layer-3QrUeG > div.standardSidebarView-3F1I7i > div.sidebarRegion-VFTUkN > div.sidebarRegionScroller-3MXcoP.thin-1ybCId.scrollerBase-289Jih.fade-2kXiP2 > nav.sidebar-CFHs9e > div.side-8zPYf6 > div.info-1VyQPT::after {
	content: "BasicBackground by" !important;
	font-size: 12px !important;
	color: var(--text-muted) !important;
	cursor: pointer !important;
	display: inline !important;
	opacity: 1 !important;
	padding: 0 !important;
	margin: 0 !important;
	cursor: text !important;
	visibility: visible !important;
	position: relative !important;
	top: unset !important;
	left: unset !important;
	bottom: unset !important;
	right: unset !important;
	transform: unset !important;
	animation: unset !important;
}
html:only-child > head + body > div#app-mount.appMount-3lHmkl > div.app-1q1i1E > div.app-2rEoOp > div.layers-3iHuyZ.layers-3q14ss > div.layer-3QrUeG.baseLayer-35bLyl + div.layer-3QrUeG > div.standardSidebarView-3F1I7i > div.sidebarRegion-VFTUkN > div.sidebarRegionScroller-3MXcoP.thin-1ybCId.scrollerBase-289Jih.fade-2kXiP2 > nav.sidebar-CFHs9e > div.side-8zPYf6 > div.info-1VyQPT::before {
	content: "DevilBro" !important;
	font-size: 12px !important;
	color: rgb(var(--vaccentcolor)) !important;
	display: inline !important;
	opacity: 1 !important;
	padding: 0 !important;
	margin: 0 !important;
	cursor: pointer !important;
	visibility: visible !important;
	position: absolute !important;
	top: unset !important;
	left: 113px !important;
	bottom: 9px !important;
	right: unset !important;
	transform: unset !important;
	animation: unset !important;
}
