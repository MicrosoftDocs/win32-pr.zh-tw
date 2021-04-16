---
title: 在燒錄期間防止登出或暫停
description: 如果未在應用程式中進行適當的預防措施，使用者可能會在燒錄作業期間登出。 這會導致燒錄程式中斷，這可能會導致資料遺失，而且可能會導致無法使用光碟。
ms.assetid: 5223c9f6-30f6-43ce-b46c-267da0a53d4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5922fbe6dbc27303cee82e7ed745cbaaf2744781
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463024"
---
# <a name="preventing-logoff-or-suspend-during-a-burn"></a><span data-ttu-id="c1011-104">在燒錄期間防止登出或暫停</span><span class="sxs-lookup"><span data-stu-id="c1011-104">Preventing Logoff or Suspend During a Burn</span></span>

<span data-ttu-id="c1011-105">如果未在應用程式中進行適當的預防措施，使用者可能會在燒錄作業期間登出。</span><span class="sxs-lookup"><span data-stu-id="c1011-105">If proper precautions are not made within an application, it is possible for a user to log off during a burn operation.</span></span> <span data-ttu-id="c1011-106">這會導致燒錄程式中斷，這可能會導致資料遺失，而且可能會導致無法使用光碟。</span><span class="sxs-lookup"><span data-stu-id="c1011-106">This leads to the interruption of the burn process, which can result in lost data and possibly render the disc unusable.</span></span>

<span data-ttu-id="c1011-107">若要避免這個問題，應用程式應該處理在登出之前傳遞的 [**WM \_ QUERYENDSESSION**](/windows/desktop/Shutdown/wm-queryendsession) 訊息。</span><span class="sxs-lookup"><span data-stu-id="c1011-107">To avoid this problem, the application should process the [**WM\_QUERYENDSESSION**](/windows/desktop/Shutdown/wm-queryendsession) message which is delivered prior to log off.</span></span> <span data-ttu-id="c1011-108">如果應用程式在執行燒錄操作時收到此訊息，則會傳回 **FALSE** 以取消登出程式。</span><span class="sxs-lookup"><span data-stu-id="c1011-108">If the application receives this message while performing a burn operation, return **FALSE** to cancel the logoff procedure.</span></span> <span data-ttu-id="c1011-109">如果應用程式可讓使用者決定是否要繼續登出，則應該提供警告，指出使用者將會遺失資料。</span><span class="sxs-lookup"><span data-stu-id="c1011-109">If the application allows the user to decide whether to continue logging off, a warning should be provided indicating that user will lose data.</span></span>

<span data-ttu-id="c1011-110">燒錄程式期間的電源轉換也可能會在燒錄活動成功時產生潛在問題。</span><span class="sxs-lookup"><span data-stu-id="c1011-110">Power transitions during the burn process can also create potential problems in the success of a burn activity.</span></span> <span data-ttu-id="c1011-111">在燒錄程式中避免這些複雜性，需要應用程式知道何時即將進行電源轉換。</span><span class="sxs-lookup"><span data-stu-id="c1011-111">Preventing these complications during the burn process requires an application to be aware of when power transitions are about to take place.</span></span> <span data-ttu-id="c1011-112">這是藉由讓應用程式處理 [**WM \_ POWERBROADCAST**](/windows/desktop/Power/wm-powerbroadcast) 訊息來完成。</span><span class="sxs-lookup"><span data-stu-id="c1011-112">This is accomplished by by enabling the application to process the [**WM\_POWERBROADCAST**](/windows/desktop/Power/wm-powerbroadcast) message.</span></span> <span data-ttu-id="c1011-113">針對 Windows XP 或 Windows Server 2003 開發的應用程式可能會傳回「 **廣播 \_ 查詢 \_ 拒絕** 」以回應 [**PBT \_ APMQUERYSUSPEND**](/windows/desktop/Power/pbt-apmquerysuspend)，以防止在燒錄過程中暫停。</span><span class="sxs-lookup"><span data-stu-id="c1011-113">Applications developed for Windows XP or Windows Server 2003 can return **BROADCAST\_QUERY\_DENY** in response to [**PBT\_APMQUERYSUSPEND**](/windows/desktop/Power/pbt-apmquerysuspend), preventing Suspend during the burn process.</span></span>

<span data-ttu-id="c1011-114">由於 Windows Vista 和 Windows Server 2008 的電源管理模型有所變更，因此 [**PBT \_ APMQUERYSUSPEND**](/windows/desktop/Power/pbt-apmquerysuspend) 事件不再傳遞給應用程式。</span><span class="sxs-lookup"><span data-stu-id="c1011-114">Due to changes in the Power Management Model for Windows Vista and Windows Server 2008, the [**PBT\_APMQUERYSUSPEND**](/windows/desktop/Power/pbt-apmquerysuspend) event is no longer delivered to applications.</span></span> <span data-ttu-id="c1011-115">相反地，系統會傳遞 [**PBT \_ APMSUSPEND**](/windows/desktop/Power/pbt-apmsuspend) 事件，讓應用程式有兩秒鐘的時間來準備進行轉換。</span><span class="sxs-lookup"><span data-stu-id="c1011-115">Instead the [**PBT\_APMSUSPEND**](/windows/desktop/Power/pbt-apmsuspend) event is delivered, providing two seconds for an application to prepare for the transition.</span></span>

<span data-ttu-id="c1011-116">由於這些變更的結果，建議應用程式呼叫 [**SetThreadExecutionState**](/windows/desktop/api/winbase/nf-winbase-setthreadexecutionstate) 函式來防止系統閒置時間，這通常會導致轉換暫停。</span><span class="sxs-lookup"><span data-stu-id="c1011-116">As a result of these changes, it is recommended that applications call the [**SetThreadExecutionState**](/windows/desktop/api/winbase/nf-winbase-setthreadexecutionstate) function to prevent a system idle time-out which ordinarily results in the transition to Suspend.</span></span> <span data-ttu-id="c1011-117">請務必記得，使用適當的旗標來呼叫這個函式只會防止系統閒置，而非進行中的暫止。</span><span class="sxs-lookup"><span data-stu-id="c1011-117">It is important to remember that calling this function with the appropriate flags set will only prevent system idle, not an in-progress Suspend.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c1011-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="c1011-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1011-119">使用 IMAPI.EXE</span><span class="sxs-lookup"><span data-stu-id="c1011-119">Using IMAPI</span></span>](using-imapi.md)
</dt> <dt>

[<span data-ttu-id="c1011-120">**SetThreadExecutionState**</span><span class="sxs-lookup"><span data-stu-id="c1011-120">**SetThreadExecutionState**</span></span>](/windows/desktop/api/winbase/nf-winbase-setthreadexecutionstate)
</dt> </dl>

 

 