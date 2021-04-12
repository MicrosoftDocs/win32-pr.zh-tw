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
# <a name="registering-for-power-events"></a><span data-ttu-id="64d96-103">註冊電源事件</span><span class="sxs-lookup"><span data-stu-id="64d96-103">Registering for Power Events</span></span>

<span data-ttu-id="64d96-104">應用程式可以藉由註冊電源事件，更妥善地將其行為調整為電腦目前的電源狀態。</span><span class="sxs-lookup"><span data-stu-id="64d96-104">Applications can better adapt their behavior to the current power state of the computer by registering for power events.</span></span> <span data-ttu-id="64d96-105">應用程式應該針對可能影響其行為的每個電源變更事件註冊。</span><span class="sxs-lookup"><span data-stu-id="64d96-105">An application should register for each power change event that might impact its behavior.</span></span>

<span data-ttu-id="64d96-106">應用程式或服務會使用 [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification) 函數來註冊通知。</span><span class="sxs-lookup"><span data-stu-id="64d96-106">An application or service uses the [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification) function to register for notifications.</span></span> <span data-ttu-id="64d96-107">當對應的電源設定變更時，系統會傳送通知，如下所示：</span><span class="sxs-lookup"><span data-stu-id="64d96-107">When the corresponding power setting changes, the system sends notifications as follows:</span></span>

-   <span data-ttu-id="64d96-108">應用程式會接收 *wParam* 為 [PBT \_ POWERSETTINGCHANGE](pbt-powersettingchange.md)的 [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)訊息，以及指向 [**lParam \_ 設定**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting)結構的 *POWERBROADCAST* 。</span><span class="sxs-lookup"><span data-stu-id="64d96-108">An application receives a [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message with a *wParam* of [PBT\_POWERSETTINGCHANGE](pbt-powersettingchange.md) and an *lParam* that points to a [**POWERBROADCAST\_SETTING**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) structure.</span></span>
-   <span data-ttu-id="64d96-109">服務會呼叫 [**RegisterServiceCtrlHandlerEx**](/windows/desktop/api/winsvc/nf-winsvc-registerservicectrlhandlerexa)函式來呼叫它所註冊的 [*HandlerEx*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex)回呼函數。</span><span class="sxs-lookup"><span data-stu-id="64d96-109">A service receives a call to the [*HandlerEx*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) callback function it registered by calling the [**RegisterServiceCtrlHandlerEx**](/windows/desktop/api/winsvc/nf-winsvc-registerservicectrlhandlerexa) function.</span></span> <span data-ttu-id="64d96-110">傳送至 *HandlerEx* 回呼函數的 *lpEventData* 參數會指向 [**POWERBROADCAST \_ 設定**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting)結構。</span><span class="sxs-lookup"><span data-stu-id="64d96-110">The *lpEventData* parameter sent to the *HandlerEx* callback function points to a [**POWERBROADCAST\_SETTING**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) structure.</span></span>

<span data-ttu-id="64d96-111">在 [**POWERBROADCAST \_ 設定**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) 結構中， **PowerSetting** 成員包含可識別通知的 GUID，而 **資料** 成員包含電源設定的新值。</span><span class="sxs-lookup"><span data-stu-id="64d96-111">In the [**POWERBROADCAST\_SETTING**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) structure, the **PowerSetting** member contains the GUID that identifies the notification and the **Data** member contains the new value of the power setting.</span></span>

<span data-ttu-id="64d96-112">如需最適合應用程式之通知的電源設定 Guid 清單，請參閱 [**電源設定 guid**](power-setting-guids.md)。</span><span class="sxs-lookup"><span data-stu-id="64d96-112">For a list of power setting GUIDs for notifications that are most useful to applications, see [**Power Setting GUIDs**](power-setting-guids.md).</span></span>

 

 
