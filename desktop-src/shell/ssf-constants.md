---
description: 由 SHGetSetSettings 函數用來指定應設定或擷取其 SHELLSTATE 結構的成員。
title: 'SSF 常數 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2a883110-fdc3-4451-9e47-e58894600e3b
api_name:
- SSF_SHOWALLOBJECTS
- SSF_SHOWEXTENSIONS
- SSF_HIDDENFILEEXTS
- SSF_SERVERADMINUI
- SSF_SHOWCOMPCOLOR
- SSF_SORTCOLUMNS
- SSF_SHOWSYSFILES
- SSF_DOUBLECLICKINWEBVIEW
- SSF_SHOWATTRIBCOL
- SSF_DESKTOPHTML
- SSF_WIN95CLASSIC
- SSF_DONTPRETTYPATH
- SSF_MAPNETDRVBUTTON
- SSF_SHOWINFOTIP
- SSF_HIDEICONS
- SSF_NOCONFIRMRECYCLE
- SSF_FILTER
- SSF_WEBVIEW
- SSF_SHOWSUPERHIDDEN
- SSF_SEPPROCESS
- SSF_NONETCRAWLING
- SSF_STARTPANELON
- SSF_SHOWSTARTPAGE
- SSF_AUTOCHECKSELECT
- SSF_ICONSONLY
- SSF_SHOWTYPEOVERLAY
- SSF_SHOWSTATUSBAR
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c022b1d93cb411f0cce73822a47f2d8f85b30e8093bbe2064fb3c50eab5c4870
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967937"
---
# <a name="ssf-constants"></a>SSF 常數

由 [**SHGetSetSettings**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetsetsettings) 函數用來指定應設定或擷取其 [**SHELLSTATE**](/windows/win32/api/shlobj_core/ns-shlobj_core-shellstatea) 結構的成員。

<dl> <dt>

<span id="SSF_SHOWALLOBJECTS"></span><span id="ssf_showallobjects"></span>**SSF \_ SHOWALLOBJECTS**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



正在要求 **fShowAllObjects** 成員。


</dt> </dl> </dd> <dt>

<span id="SSF_SHOWEXTENSIONS"></span><span id="ssf_showextensions"></span>**SSF \_ SHOWEXTENSIONS**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



正在要求 **fShowExtensions** 成員。


</dt> </dl> </dd> <dt>

<span id="SSF_HIDDENFILEEXTS"></span><span id="ssf_hiddenfileexts"></span>**SSF \_ HIDDENFILEEXTS**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



未使用。


</dt> </dl> </dd> <dt>

<span id="SSF_SERVERADMINUI"></span><span id="ssf_serveradminui"></span>**SSF \_ SERVERADMINUI**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



未使用。


</dt> </dl> </dd> <dt>

<span id="SSF_SHOWCOMPCOLOR"></span><span id="ssf_showcompcolor"></span>**SSF \_ SHOWCOMPCOLOR**
</dt> <dd> <dl> <dt>

0x00000008
</dt> <dt>



正在要求 **fShowCompColor** 成員。


</dt> </dl> </dd> <dt>

<span id="SSF_SORTCOLUMNS"></span><span id="ssf_sortcolumns"></span>**SSF \_ SORTCOLUMNS**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



正在要求 **lParamSort** 與 **iSortDirection** 成員。


</dt> </dl> </dd> <dt>

<span id="SSF_SHOWSYSFILES"></span><span id="ssf_showsysfiles"></span>**SSF \_ SHOWSYSFILES**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



正在要求 **fShowSysFiles** 成員。


</dt> </dl> </dd> <dt>

<span id="SSF_DOUBLECLICKINWEBVIEW"></span><span id="ssf_doubleclickinwebview"></span>**SSF \_ DOUBLECLICKINWEBVIEW**
</dt> <dd> <dl> <dt>

0x00000080
</dt> <dt>



正在要求 **fDoubleClickInWebView** 成員。


</dt> </dl> </dd> <dt>

<span id="SSF_SHOWATTRIBCOL"></span><span id="ssf_showattribcol"></span>**SSF \_ SHOWATTRIBCOL**
</dt> <dd> <dl> <dt>

0x00000100
</dt> <dt>



正在要求 **fShowAttribCol** 成員。

**Windows Vista：** 未使用。


</dt> </dl> </dd> <dt>

<span id="SSF_DESKTOPHTML"></span><span id="ssf_desktophtml"></span>**SSF \_ DESKTOPHTML**
</dt> <dd> <dl> <dt>

0x00000200
</dt> <dt>



正在要求 **fDesktopHTML** 成員。 設定為 [無法使用]。 相反地，針對 Windows XP 之前的 Windows 版本，請啟用 [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop)的桌面 HTML。 但是，不建議將 **IActiveDesktop** 用於此用途，Windows XP 和更新版本的 Windows，而且在 Windows Vista 中已淘汰。


</dt> </dl> </dd> <dt>

<span id="SSF_WIN95CLASSIC"></span><span id="ssf_win95classic"></span>**SSF \_ WIN95CLASSIC**
</dt> <dd> <dl> <dt>

0x00000400
</dt> <dt>



正在要求 **fWin95Classic** 成員。


</dt> </dl> </dd> <dt>

<span id="SSF_DONTPRETTYPATH"></span><span id="ssf_dontprettypath"></span>**SSF \_ DONTPRETTYPATH**
</dt> <dd> <dl> <dt>

0x00000800
</dt> <dt>



正在要求 **fDontPrettyPath** 成員。


</dt> </dl> </dd> <dt>

<span id="SSF_MAPNETDRVBUTTON"></span><span id="ssf_mapnetdrvbutton"></span>**SSF \_ MAPNETDRVBUTTON**
</dt> <dd> <dl> <dt>

0x00001000
</dt> <dt>



正在要求 **fMapNetDrvBtn** 成員。


</dt> </dl> </dd> <dt>

<span id="SSF_SHOWINFOTIP"></span><span id="ssf_showinfotip"></span>**SSF \_ SHOWINFOTIP**
</dt> <dd> <dl> <dt>

0x00002000
</dt> <dt>



正在要求 **fShowInfoTip** 成員。


</dt> </dl> </dd> <dt>

<span id="SSF_HIDEICONS"></span><span id="ssf_hideicons"></span>**SSF \_ HIDEICONS**
</dt> <dd> <dl> <dt>

0x00004000
</dt> <dt>



正在要求 **fHideIcons** 成員。


</dt> </dl> </dd> <dt>

<span id="SSF_NOCONFIRMRECYCLE"></span><span id="ssf_noconfirmrecycle"></span>**SSF \_ NOCONFIRMRECYCLE**
</dt> <dd> <dl> <dt>

0x00008000
</dt> <dt>



正在要求 **fNoConfirmRecycle** 成員。


</dt> </dl> </dd> <dt>

<span id="SSF_FILTER"></span><span id="ssf_filter"></span>**SSF \_ 篩選**
</dt> <dd> <dl> <dt>

0x00010000
</dt> <dt>



正在要求 **fFilter** 成員。

**Windows Vista：** 未使用。


</dt> </dl> </dd> <dt>

<span id="SSF_WEBVIEW"></span><span id="ssf_webview"></span>**SSF \_ WEB 視圖**
</dt> <dd> <dl> <dt>

0x00020000
</dt> <dt>



正在要求 **fWebView** 成員。


</dt> </dl> </dd> <dt>

<span id="SSF_SHOWSUPERHIDDEN"></span><span id="ssf_showsuperhidden"></span>**SSF \_ SHOWSUPERHIDDEN**
</dt> <dd> <dl> <dt>

0x00040000
</dt> <dt>



正在要求 **fShowSuperHidden** 成員。


</dt> </dl> </dd> <dt>

<span id="SSF_SEPPROCESS"></span><span id="ssf_sepprocess"></span>**SSF \_ SEPPROCESS**
</dt> <dd> <dl> <dt>

0x00080000
</dt> <dt>



正在要求 **fSepProcess** 成員。


</dt> </dl> </dd> <dt>

<span id="SSF_NONETCRAWLING"></span><span id="ssf_nonetcrawling"></span>**SSF \_ NONETCRAWLING**
</dt> <dd> <dl> <dt>

0x00100000
</dt> <dt>



**Windows XP 及更新版本**。 正在要求 **fNoNetCrawling** 成員。


</dt> </dl> </dd> <dt>

<span id="SSF_STARTPANELON"></span><span id="ssf_startpanelon"></span>**SSF \_ STARTPANELON**
</dt> <dd> <dl> <dt>

0x00200000
</dt> <dt>



**Windows XP 及更新版本**。 正在要求 **fStartPanelOn** 成員。


</dt> </dl> </dd> <dt>

<span id="SSF_SHOWSTARTPAGE"></span><span id="ssf_showstartpage"></span>**SSF \_ SHOWSTARTPAGE**
</dt> <dd> <dl> <dt>

0x00400000
</dt> <dt>



未使用。


</dt> </dl> </dd> <dt>

<span id="SSF_AUTOCHECKSELECT"></span><span id="ssf_autocheckselect"></span>**SSF \_ AUTOCHECKSELECT**
</dt> <dd> <dl> <dt>

0x00800000
</dt> <dt>



**Windows Vista 和更新版本**。 正在要求 **fAutoCheckSelect** 成員。


</dt> </dl> </dd> <dt>

<span id="SSF_ICONSONLY"></span><span id="ssf_iconsonly"></span>**SSF \_ ICONSONLY**
</dt> <dd> <dl> <dt>

0x01000000
</dt> <dt>



**Windows Vista 和更新版本**。 正在要求 **fIconsOnly** 成員。


</dt> </dl> </dd> <dt>

<span id="SSF_SHOWTYPEOVERLAY"></span><span id="ssf_showtypeoverlay"></span>**SSF \_ SHOWTYPEOVERLAY**
</dt> <dd> <dl> <dt>

0x02000000
</dt> <dt>



**Windows Vista 和更新版本**。 正在要求 **fShowTypeOverlay** 成員。


</dt> </dl> </dd> <dt>

<span id="SSF_SHOWSTATUSBAR"></span><span id="ssf_showstatusbar"></span>**SSF \_ SHOWSTATUSBAR**
</dt> <dd> <dl> <dt>

0x04000000
</dt> <dt>



**Windows 8 和更新版本**：正在要求 **fShowStatusBar** 成員。


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Shlobj.h。h</dt> </dl> |



 

 
