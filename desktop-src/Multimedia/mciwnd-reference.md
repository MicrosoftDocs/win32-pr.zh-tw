---
title: MCIWnd 參考
description: MCIWnd 參考
ms.assetid: 11fba6bb-17f1-4fbe-b148-4755a3c6216a
keywords:
- MCI (媒體控制介面) 、MCIWnd 參考
- MCIWnd 視窗類別，參考
- MCIWnd 視窗，參考
- MCIWnd 參考，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76333f38a5dec3edaadcae69777703ebea61296f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462116"
---
# <a name="mciwnd-reference"></a>MCIWnd 參考

本節描述與 MCIWnd 視窗類別相關聯的函式、訊息和宏。 這些元素的分組方式如下。

## <a name="window-management"></a>視窗管理

-   [**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles)
-   [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea)
-   [**MCIWndGetStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstyles)
-   [**MCIWndRegisterClass**](/windows/desktop/api/Vfw/nf-vfw-mciwndregisterclass)

## <a name="file-and-device-management"></a>檔案和裝置管理

-   [**MCIWndClose**](/windows/desktop/api/Vfw/nf-vfw-mciwndclose)
-   [**MCIWndDestroy**](/windows/desktop/api/Vfw/nf-vfw-mciwnddestroy)
-   [**MCIWndEject**](/windows/desktop/api/Vfw/nf-vfw-mciwndeject)
-   [**MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew)
-   [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen)
-   [**MCIWndOpenDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndopendialog)
-   [**MCIWndSave**](/windows/desktop/api/Vfw/nf-vfw-mciwndsave)
-   [**MCIWndSaveDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndsavedialog)

## <a name="playback-options"></a>播放選項

-   [**MCIWndGetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetrepeat)
-   [**MCIWndPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay)
-   [**MCIWndPlayFrom**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom)
-   [**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto)
-   [**MCIWndPlayReverse**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayreverse)
-   [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto)
-   [**MCIWndSetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat)

## <a name="recording"></a>記錄

-   [**MCIWndRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndrecord)

## <a name="positioning"></a>定位

-   [**MCIWndEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndend)
-   [**MCIWndGetEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend)
-   [**MCIWndGetLength**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetlength)
-   [**MCIWndGetPosition**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetposition)
-   [**MCIWndGetPositionString**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpositionstring)
-   [**MCIWndGetStart**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart)
-   [**MCIWndHome**](/windows/desktop/api/Vfw/nf-vfw-mciwndhome)
-   [**MCIWndSeek**](/windows/desktop/api/Vfw/nf-vfw-mciwndseek)
-   [**MCIWndStep**](/windows/desktop/api/Vfw/nf-vfw-mciwndstep)

## <a name="pause-and-resume-playback"></a>暫停和繼續播放

-   [**MCIWndGetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetrepeat)
-   [**MCIWndPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay)
-   [**MCIWndPlayFrom**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom)
-   [**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto)
-   [**MCIWndPlayReverse**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayreverse)
-   [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto)
-   [**MCIWndSetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat)

## <a name="performance-tuning"></a>效能微調

-   [**MCIWndGetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetspeed)
-   [**MCIWndGetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetvolume)
-   [**MCIWndGetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetzoom)
-   [**MCIWndSetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetspeed)
-   [**MCIWndSetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetvolume)
-   [**MCIWndSetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetzoom)

## <a name="image-and-palette-adjustments"></a>影像和調色板調整

-   [**MCIWndGetDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdest)
-   [**MCIWndGetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpalette)
-   [**MCIWndGetSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetsource)
-   [**MCIWndPutDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndputdest)
-   [**MCIWndPutSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndputsource)
-   [**MCIWndRealize**](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize)
-   [**MCIWndSetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetpalette)

## <a name="event-and-error-notification"></a>事件和錯誤通知

-   [**MCIWndGetError**](/windows/desktop/api/Vfw/nf-vfw-mciwndgeterror)
-   [**MCIWNDM \_ NOTIFYERROR**](mciwndm-notifyerror.md)
-   [**MCIWNDM \_ NOTIFYMEDIA**](mciwndm-notifymedia.md)
-   [**MCIWNDM \_ NOTIFYMODE**](mciwndm-notifymode.md)
-   [**MCIWNDM \_ NOTIFYPOS**](mciwndm-notifypos.md)
-   [**MCIWNDM \_ NOTIFYSIZE**](mciwndm-notifysize.md)

## <a name="time-formats"></a>時間格式

-   [**MCIWndGetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat)
-   [**MCIWndSetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimeformat)
-   [**MCIWndUseFrames**](/windows/desktop/api/Vfw/nf-vfw-mciwnduseframes)
-   [**MCIWndUseTime**](/windows/desktop/api/Vfw/nf-vfw-mciwndusetime)
-   [**MCIWndValidateMedia**](/windows/desktop/api/Vfw/nf-vfw-mciwndvalidatemedia)

## <a name="status-updates"></a>狀態更新

-   [**MCIWndGetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetactivetimer)
-   [**MCIWndGetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetinactivetimer)
-   [**MCIWndSetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetactivetimer)
-   [**MCIWndSetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetinactivetimer)
-   [**MCIWndSetTimers**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimers)

## <a name="device-capabilities"></a>裝置功能

-   [**MCIWndCanConfig**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanconfig)
-   [**MCIWndCanEject**](/windows/desktop/api/Vfw/nf-vfw-mciwndcaneject)
-   [**MCIWndCanPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanplay)
-   [**MCIWndCanRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanrecord)
-   [**MCIWndCanSave**](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave)
-   [**MCIWndCanWindow**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanwindow)

## <a name="mci-device-settings"></a>MCI 裝置設定

-   [**MCIWndGetAlias**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetalias)
-   [**MCIWndGetDevice**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdevice)
-   [**MCIWndGetDeviceID**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdeviceid)
-   [**MCIWndGetFileName**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetfilename)
-   [**MCIWndGetMode**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetmode)

## <a name="mci-command-string-interface"></a>MCI Command-String 介面

-   [**MCIWndReturnString**](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring)
-   [**MCIWndSendString**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[MCIWnd 視窗類別](mciwnd-window-class.md)
</dt> </dl>

 

 




