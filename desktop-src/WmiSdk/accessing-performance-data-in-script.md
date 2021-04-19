---
description: WMI 腳本可以存取預先安裝的 WMI 效能計數器類別，不論是在本機電腦或遠端。
ms.assetid: 79e47173-c8b6-452d-9400-93e2bd6e9da5
ms.tgt_platform: multiple
title: 存取腳本中的效能資料
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e203acfc7fc23fe0dab466eee383223aad0bf889
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106998899"
---
# <a name="accessing-performance-data-in-script"></a><span data-ttu-id="f994b-103">存取腳本中的效能資料</span><span class="sxs-lookup"><span data-stu-id="f994b-103">Accessing Performance Data in Script</span></span>

<span data-ttu-id="f994b-104">WMI 腳本可以存取預先安裝的 WMI [效能計數器類別](/windows/desktop/CIMWin32Prov/performance-counter-classes)，不論是在本機電腦或遠端。</span><span class="sxs-lookup"><span data-stu-id="f994b-104">WMI scripts can access the preinstalled WMI [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes), either on the local computer or remotely.</span></span> <span data-ttu-id="f994b-105">雖然腳本可以從未計算的類別（例如 [**win32 \_ PerfRawData \_ PerfOS \_ 記憶體**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data)或格式化類別、 [**win32 \_ PerfFormattedData \_ PerfOS \_ 記憶體**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data)）取得資料，但格式化的資料類別可以更容易使用。</span><span class="sxs-lookup"><span data-stu-id="f994b-105">While scripts can obtain data from uncalculated classes, such as [**Win32\_PerfRawData\_PerfOS\_Memory**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data), or formatted classes, [**Win32\_PerfFormattedData\_PerfOS\_Memory**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data), the formatted data classes can be easier to use.</span></span>

<span data-ttu-id="f994b-106">使用效能計數器類別監視效能資料需要使用 [*複習*](gloss-r.md)。</span><span class="sxs-lookup"><span data-stu-id="f994b-106">Monitoring performance data with the performance counter classes requires the use of a [*refresher*](gloss-r.md).</span></span> <span data-ttu-id="f994b-107">使用 [**SWbemRefresher**](swbemrefresher.md) 物件來儲存一或多個效能物件，以供 [**SWbemObjectEx**](swbemobjectex-refresh-.md) 重新整理或重新整理單一物件。</span><span class="sxs-lookup"><span data-stu-id="f994b-107">Use the [**SWbemRefresher**](swbemrefresher.md) object to store one or more performance objects for refresh or refresh a single object by the [**SWbemObjectEx.Refresh**](swbemobjectex-refresh-.md) call.</span></span> <span data-ttu-id="f994b-108">如需詳細資訊，請參閱 [更新腳本中的 WMI 資料](refreshing-wmi-data-in-scripts.md)。</span><span class="sxs-lookup"><span data-stu-id="f994b-108">For more information, see [Refreshing WMI Data in Scripts](refreshing-wmi-data-in-scripts.md).</span></span>

<span data-ttu-id="f994b-109">藉由將 [**SWbemRefresher. AutoReconnect**](swbemrefresher-autoreconnect.md) 屬性設定為 **TRUE**，如果連接中斷，WMI 就會自動重新連接至遠端提供者，如此您就不需要檢查連接狀態。</span><span class="sxs-lookup"><span data-stu-id="f994b-109">By setting the [**SWbemRefresher.AutoReconnect**](swbemrefresher-autoreconnect.md) property to **TRUE**, WMI automatically reconnects to a remote provider if the connection is broken so that you do not need to check for connection status.</span></span>

<span data-ttu-id="f994b-110">如下列腳本程式碼範例腳本所示，您必須進行初始重新整理呼叫，以取得要重新整理之物件的起始值。</span><span class="sxs-lookup"><span data-stu-id="f994b-110">As shown in the following script code example script, you must make an initial refresh call to get a starting value for the object you are refreshing.</span></span> <span data-ttu-id="f994b-111">後續的重新整理呼叫會包含資料。</span><span class="sxs-lookup"><span data-stu-id="f994b-111">Subsequent refresh calls then contain data.</span></span>

> [!Note]  
> <span data-ttu-id="f994b-112">當腳本從遠端電腦存取 WMI 效能計數器資料時，腳本只能在目前登入的使用者帳戶下執行。</span><span class="sxs-lookup"><span data-stu-id="f994b-112">When a script is accessing WMI performance counter data from a remote computer, the script can only run under the current logged-on user account.</span></span> <span data-ttu-id="f994b-113">WMI 不支援傳遞不同使用者認證的 [**wbemscripting.swbemlocator. ConnectServer**](swbemlocator-connectserver.md) 呼叫。</span><span class="sxs-lookup"><span data-stu-id="f994b-113">WMI does not support an [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) call that passes in different user credentials.</span></span> <span data-ttu-id="f994b-114">因此，呼叫遠端電腦的帳戶必須已在該電腦上擁有適當的許可權。</span><span class="sxs-lookup"><span data-stu-id="f994b-114">Therefore, the account calling the remote computer must already have the appropriate privileges on that computer.</span></span>

 

<span data-ttu-id="f994b-115">下列腳本程式碼範例示範如何使用 [**SWbemRefresher**](swbemrefresher.md) 物件來更新效能計數器物件中的資料。</span><span class="sxs-lookup"><span data-stu-id="f994b-115">The following script code example shows how to use an [**SWbemRefresher**](swbemrefresher.md) object to update the data in performance counter objects.</span></span> <span data-ttu-id="f994b-116">如需在 WMI 中使用效能計數器的詳細資訊，請參閱 [存取 Wmi 預先安裝的效能類別](accessing-wmi-preinstalled-performance-classes.md)。</span><span class="sxs-lookup"><span data-stu-id="f994b-116">For more information about using performance counters in WMI, see [Accessing WMI Preinstalled Performance Classes](accessing-wmi-preinstalled-performance-classes.md).</span></span>


```VB
' Get raw and cooked data performance counter instances for the
" wscript process running this script

set RawProc = GetObject("winmgmts:Win32_PerfRawdata_Perfproc_process.name='wscript'")
set CookedProc = GetObject("winmgmts:Win32_Perfformatteddata_Perfproc_process.name='wscript'")

' Display the same property in raw and cooked form in a loop
for I = 1 to 6
    Wscript.Echo "wscript process raw PageFaultsPerSec = & RawProc.PageFaultsPerSec _
                 & " cooked PageFaultsPerSec= " & CookedProc.PageFaultsPerSec 

' Wait 2 seconds
    Wscript.Sleep 2000
    
    ' Refresh the object
    RawProc.Refresh_
    CookedProc.Refresh_
next
```



## <a name="example"></a><span data-ttu-id="f994b-117">範例</span><span class="sxs-lookup"><span data-stu-id="f994b-117">Example</span></span>

<span data-ttu-id="f994b-118">下列腳本範例顯示您必須進行初始重新整理呼叫，以取得重新整理之物件的起始值。</span><span class="sxs-lookup"><span data-stu-id="f994b-118">The following script code example shows that you must make an initial refresh call to get a starting value for the refreshed object.</span></span> <span data-ttu-id="f994b-119">後續的重新整理呼叫會包含資料。</span><span class="sxs-lookup"><span data-stu-id="f994b-119">Subsequent refresh calls then contain data.</span></span>

<span data-ttu-id="f994b-120">下列腳本程式碼範例示範如何使用 [**SWbemRefresher**](swbemrefresher.md) 物件來更新效能計數器物件中的資料。</span><span class="sxs-lookup"><span data-stu-id="f994b-120">The following script code example shows how to use an [**SWbemRefresher**](swbemrefresher.md) object to update the data in performance counter objects.</span></span> <span data-ttu-id="f994b-121">如需在 WMI 中使用效能計數器的詳細資訊，請參閱 [存取 Wmi 預先安裝的效能類別](accessing-wmi-preinstalled-performance-classes.md)。</span><span class="sxs-lookup"><span data-stu-id="f994b-121">For more information about using performance counters in WMI, see [Accessing WMI Preinstalled Performance Classes](accessing-wmi-preinstalled-performance-classes.md).</span></span>


```VB
' Get raw and cooked data performance counter instances for the
" wscript process running this script

set RawProc = GetObject("winmgmts:" _
                        & "Win32_PerfRawdata_Perfproc_process." _
                        & "name='wscript'")
set CookedProc = GetObject("winmgmts:" _ 
                & "Win32_Perfformatteddata_Perfproc_process." _
                & "name='wscript'")

' Display the same property in raw and cooked form in a loop
for I = 1 to 6
    Wscript.Echo "wscript process raw PageFaultsPerSec = " _
                 & RawProc.PageFaultsPerSec _
                 & " cooked PageFaultsPerSec= " _
                 & CookedProc.PageFaultsPerSec 

' Wait 2 seconds
    Wscript.Sleep 2000
    
    ' Refresh the object
    RawProc.Refresh_
    CookedProc.Refresh_
next
```



## <a name="related-topics"></a><span data-ttu-id="f994b-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="f994b-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f994b-123">效能計數器類別</span><span class="sxs-lookup"><span data-stu-id="f994b-123">Performance Counter Classes</span></span>](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[<span data-ttu-id="f994b-124">WMI 工作：效能監視</span><span class="sxs-lookup"><span data-stu-id="f994b-124">WMI Tasks: Performance Monitoring</span></span>](wmi-tasks--performance-monitoring.md)
</dt> <dt>

[<span data-ttu-id="f994b-125">監視效能資料</span><span class="sxs-lookup"><span data-stu-id="f994b-125">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> </dl>

 

 
