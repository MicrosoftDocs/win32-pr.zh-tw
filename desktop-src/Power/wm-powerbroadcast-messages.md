---
description: 當電源管理事件發生時，系統會將訊息廣播至所有應用程式和可安裝的驅動程式。
ms.assetid: a64ed11a-43d6-41f7-aabd-5dca2a2b4a12
title: WM_POWERBROADCAST 訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f70c5848ec5d71666c26fcd4b5b161e31465543
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983630"
---
# <a name="wm_powerbroadcast-messages"></a><span data-ttu-id="c46df-103">WM \_ POWERBROADCAST 訊息</span><span class="sxs-lookup"><span data-stu-id="c46df-103">WM\_POWERBROADCAST Messages</span></span>

<span data-ttu-id="c46df-104">當電源管理事件發生時，系統會將訊息廣播至所有應用程式和可安裝的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="c46df-104">The system broadcasts a message to all applications and installable drivers whenever a power management event occurs.</span></span> <span data-ttu-id="c46df-105">系統會透過 [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) 訊息來廣播這些事件，並將 *wParam* 參數設定為適當的電源管理事件。</span><span class="sxs-lookup"><span data-stu-id="c46df-105">The system broadcasts these events through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message, setting the *wParam* parameter to the appropriate power management event.</span></span> <span data-ttu-id="c46df-106">例如， [PBT \_ APMPOWERSTATUSCHANGE](pbt-apmpowerstatuschange.md) 事件表示系統電源狀態變更。</span><span class="sxs-lookup"><span data-stu-id="c46df-106">For example, the [PBT\_APMPOWERSTATUSCHANGE](pbt-apmpowerstatuschange.md) event indicates a system power status change.</span></span> <span data-ttu-id="c46df-107">您必須確保您的應用程式能夠正確地回應 **WM \_ POWERBROADCAST** 訊息。</span><span class="sxs-lookup"><span data-stu-id="c46df-107">You must ensure that your application responds properly to the **WM\_POWERBROADCAST** message.</span></span>

<span data-ttu-id="c46df-108">系統會在暫停操作之前，立即廣播 [PBT \_ APMSUSPEND](pbt-apmsuspend.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="c46df-108">The system broadcasts a [PBT\_APMSUSPEND](pbt-apmsuspend.md) event immediately before suspending operation.</span></span> <span data-ttu-id="c46df-109">這讓應用程式和驅動程式最後有機會為事件做好準備。</span><span class="sxs-lookup"><span data-stu-id="c46df-109">This gives applications and drivers one last chance to prepare for the event.</span></span> <span data-ttu-id="c46df-110">在許多情況下，系統會在不要求許可權的情況下廣播這些訊息。</span><span class="sxs-lookup"><span data-stu-id="c46df-110">In many cases, the system broadcasts these messages without requesting permission to do so.</span></span> <span data-ttu-id="c46df-111">例如，如果應用程式使用 [**SetSuspendState**](/windows/desktop/api/PowrProf/nf-powrprof-setsuspendstate) 函式來強制暫停，就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="c46df-111">This happens, for example, if an application forces suspension with the [**SetSuspendState**](/windows/desktop/api/PowrProf/nf-powrprof-setsuspendstate) function.</span></span>

<span data-ttu-id="c46df-112">系統作業還原後，系統會廣播 [PBT \_ APMRESUMESUSPEND](pbt-apmresumesuspend.md) 或 [PBT \_ APMRESUMECRITICAL](pbt-apmresumecritical.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="c46df-112">The system broadcasts the [PBT\_APMRESUMESUSPEND](pbt-apmresumesuspend.md) or [PBT\_APMRESUMECRITICAL](pbt-apmresumecritical.md) event when system operation has been restored.</span></span> <span data-ttu-id="c46df-113">如果應用程式在暫停電腦之前收到 [PBT \_ APMSUSPEND](pbt-apmsuspend.md) 事件，它會收到 PBT \_ APMRESUMESUSPEND 事件。</span><span class="sxs-lookup"><span data-stu-id="c46df-113">If an application received a [PBT\_APMSUSPEND](pbt-apmsuspend.md) event before the computer was suspended, it will receive the PBT\_APMRESUMESUSPEND event.</span></span> <span data-ttu-id="c46df-114">否則，它會收到 PBT \_ APMRESUMECRITICAL 事件。</span><span class="sxs-lookup"><span data-stu-id="c46df-114">Otherwise, it will receive the PBT\_APMRESUMECRITICAL event.</span></span>

<span data-ttu-id="c46df-115">系統會將 [PBT \_ POWERSETTINGCHANGE](pbt-powersettingchange.md) 事件傳送至使用 [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification)註冊特定事件的應用程式。</span><span class="sxs-lookup"><span data-stu-id="c46df-115">The system sends a [PBT\_POWERSETTINGCHANGE](pbt-powersettingchange.md) event to applications that have registered for the specific event using [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification).</span></span> <span data-ttu-id="c46df-116">如需詳細資訊，請參閱 [註冊電源事件](registering-for-power-events.md)。</span><span class="sxs-lookup"><span data-stu-id="c46df-116">For more information, see [Registering for Power Events](registering-for-power-events.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c46df-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="c46df-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c46df-118">關於電源管理</span><span class="sxs-lookup"><span data-stu-id="c46df-118">About Power Management</span></span>](about-power-management.md)
</dt> </dl>

 

 



