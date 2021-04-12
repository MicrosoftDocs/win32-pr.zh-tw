---
description: 應用程式可以藉由註冊電源事件，更妥善地將其行為調整為電腦目前的電源狀態。
ms.assetid: 840390ca-d32a-4cf3-9e75-66322c7cdee0
title: 註冊電源事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da084592414d1c58ab4ab43dd2b5c35f028552b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192767"
---
# <a name="registering-for-power-events"></a>註冊電源事件

應用程式可以藉由註冊電源事件，更妥善地將其行為調整為電腦目前的電源狀態。 應用程式應該針對可能影響其行為的每個電源變更事件註冊。

應用程式或服務會使用 [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification) 函數來註冊通知。 當對應的電源設定變更時，系統會傳送通知，如下所示：

-   應用程式會接收 *wParam* 為 [PBT \_ POWERSETTINGCHANGE](pbt-powersettingchange.md)的 [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)訊息，以及指向 [**lParam \_ 設定**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting)結構的 *POWERBROADCAST* 。
-   服務會呼叫 [**RegisterServiceCtrlHandlerEx**](/windows/desktop/api/winsvc/nf-winsvc-registerservicectrlhandlerexa)函式來呼叫它所註冊的 [*HandlerEx*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex)回呼函數。 傳送至 *HandlerEx* 回呼函數的 *lpEventData* 參數會指向 [**POWERBROADCAST \_ 設定**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting)結構。

在 [**POWERBROADCAST \_ 設定**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) 結構中， **PowerSetting** 成員包含可識別通知的 GUID，而 **資料** 成員包含電源設定的新值。

如需最適合應用程式之通知的電源設定 Guid 清單，請參閱 [**電源設定 guid**](power-setting-guids.md)。

 

 
