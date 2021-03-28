---
description: CPlApplet 回呼函式會處理 Windows 傳送給主控台專案的所有訊息。 傳送至函式的訊息會以特定的順序排列。 藉由相同的 token，cpl 專案需要以特定方式處理訊息。
ms.assetid: 70302698-f9d5-4de4-a662-4815002eea52
title: 主控台訊息處理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b8b43c6e265030279a6644547f41e3630208325
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944787"
---
# <a name="control-panel-message-processing"></a><span data-ttu-id="73d0f-105">主控台訊息處理</span><span class="sxs-lookup"><span data-stu-id="73d0f-105">Control Panel Message Processing</span></span>

<span data-ttu-id="73d0f-106">[**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc)回呼函式會處理 Windows 傳送給主控台專案的所有訊息。</span><span class="sxs-lookup"><span data-stu-id="73d0f-106">The [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) callback function processes all messages sent to a Control Panel item by Windows.</span></span> <span data-ttu-id="73d0f-107">傳送至函式的訊息會以特定的順序排列。</span><span class="sxs-lookup"><span data-stu-id="73d0f-107">Messages sent to the function are in a specific order.</span></span> <span data-ttu-id="73d0f-108">藉由相同的 token，cpl 專案需要以特定方式處理訊息。</span><span class="sxs-lookup"><span data-stu-id="73d0f-108">By the same token, the .cpl item requires the messages to be processed in a specific way.</span></span>

<span data-ttu-id="73d0f-109">首先， [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) 函式會 \_ 在 Windows 第一次載入主控台專案時收到 CPL 初始訊息。</span><span class="sxs-lookup"><span data-stu-id="73d0f-109">First, the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function receives the CPL\_INIT message when Windows first loads the Control Panel item.</span></span> <span data-ttu-id="73d0f-110">函數應該執行任何初始化，例如配置記憶體，並傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="73d0f-110">The function should carry out any initialization, such as allocating memory, and return nonzero.</span></span> <span data-ttu-id="73d0f-111">如果 **CPlApplet** 無法完成初始化，它必須傳回零，將 Windows 導向終止通訊並釋放 DLL。</span><span class="sxs-lookup"><span data-stu-id="73d0f-111">If **CPlApplet** cannot complete the initialization, it must return zero, directing Windows to terminate communication and release the DLL.</span></span>

<span data-ttu-id="73d0f-112">接下來，如果 CPL \_ 初始訊息成功，Windows 會傳送 cpl \_ GETCOUNT 訊息。</span><span class="sxs-lookup"><span data-stu-id="73d0f-112">Next, if the CPL\_INIT message succeeded, Windows sends the CPL\_GETCOUNT message.</span></span> <span data-ttu-id="73d0f-113">函數接著必須傳回 .dll 檔案所支援的主控台專案數。</span><span class="sxs-lookup"><span data-stu-id="73d0f-113">The function must then return the number of Control Panel items supported by the .dll file.</span></span>

<span data-ttu-id="73d0f-114">然後， [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) 函式會 \_ 針對 .dll 檔案所支援的每個主控台專案，接收一個 cpl 查詢訊息和一個 cpl \_ NEWINQUIRE 訊息。</span><span class="sxs-lookup"><span data-stu-id="73d0f-114">The [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function then receives one CPL\_INQUIRE message and one CPL\_NEWINQUIRE message for each Control Panel item supported by the .dll file.</span></span> <span data-ttu-id="73d0f-115">函數會以您的專案相關資訊填入 [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) 或 [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) 結構，例如其名稱、圖示和描述性字串。</span><span class="sxs-lookup"><span data-stu-id="73d0f-115">The function fills in a [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) or [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) structure with information about your item, such as its name, icon, and a descriptive string.</span></span> <span data-ttu-id="73d0f-116">大部分的應用程式都應該處理 CPL \_ 查詢訊息，並忽略 cpl \_ NEWINQUIRE 訊息。</span><span class="sxs-lookup"><span data-stu-id="73d0f-116">Most applications should process the CPL\_INQUIRE message and ignore the CPL\_NEWINQUIRE message.</span></span> <span data-ttu-id="73d0f-117">CPL \_ 查詢訊息以 Windows 可以快取的形式提供資訊，以提供更好的效能。</span><span class="sxs-lookup"><span data-stu-id="73d0f-117">The CPL\_INQUIRE message provides information in a form that Windows can cache, which results in much better performance.</span></span> <span data-ttu-id="73d0f-118">\_只有當您需要變更專案的圖示，或根據電腦的狀態顯示字串時，才會使用 CPL NEWINQUIRE 訊息。</span><span class="sxs-lookup"><span data-stu-id="73d0f-118">The CPL\_NEWINQUIRE message is used only if you need to change your item's icon or display strings based on the state of the computer.</span></span> <span data-ttu-id="73d0f-119">\_Windows Vista 中的 [**開始**] 功能表搜尋無法找到使用 CPL NEWINQUIRE 的主控台專案，因為它依賴快取。</span><span class="sxs-lookup"><span data-stu-id="73d0f-119">Control Panel items that use CPL\_NEWINQUIRE cannot be found by a **Start** menu search in Windows Vista because it relies on caching.</span></span>

<span data-ttu-id="73d0f-120">接著， [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) 函式會接收 CPL \_ DBLCLK 訊息作為通知，表示使用者已選擇代表主控台專案的圖示。</span><span class="sxs-lookup"><span data-stu-id="73d0f-120">The [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function next receives a CPL\_DBLCLK message as a notification that the user has chosen the icon that represents the Control Panel item.</span></span> <span data-ttu-id="73d0f-121">函式可能會在任何次數的情況下接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="73d0f-121">The function might receive this message any number of times.</span></span> <span data-ttu-id="73d0f-122">此訊息包含在對 [**CPL \_ INQUIRE**](cpl-inquire.md)或 [**cpl \_ NEWINQUIRE**](cpl-newinquire.md)的呼叫中，于 [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo)或 [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa)結構中傳回的專案識別碼和 **lpData** 指標。</span><span class="sxs-lookup"><span data-stu-id="73d0f-122">The message includes the item identifier and the **lpData** pointer returned in the [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) or [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) structure in the call to [**CPL\_INQUIRE**](cpl-inquire.md) or [**CPL\_NEWINQUIRE**](cpl-newinquire.md).</span></span> <span data-ttu-id="73d0f-123">函數應該會顯示對應的對話方塊，並處理後續的使用者輸入。</span><span class="sxs-lookup"><span data-stu-id="73d0f-123">The function should display the corresponding dialog box and process subsequent user input.</span></span>

<span data-ttu-id="73d0f-124">除了 CPL \_ DBLCLK， \_ 如果使用輸入參數叫用主控台專案（例如從命令提示字元或從其他程式），就可以傳送 cpl STARTWPARMS 訊息。</span><span class="sxs-lookup"><span data-stu-id="73d0f-124">Besides CPL\_DBLCLK, the CPL\_STARTWPARMS message can be sent if a Control Panel item is invoked with input parameters, such as from a command prompt or from another program.</span></span> <span data-ttu-id="73d0f-125">訊息包含專案識別碼以及其他參數字串。</span><span class="sxs-lookup"><span data-stu-id="73d0f-125">The message includes the item identifier along with the additional parameter string.</span></span>

<span data-ttu-id="73d0f-126">在控制應用程式終止之前， [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) 會 \_ 針對 .dll 檔案所支援的每個主控台專案，接收一次 CPL 停止訊息。</span><span class="sxs-lookup"><span data-stu-id="73d0f-126">Before the controlling application terminates, [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) receives the CPL\_STOP message once for each Control Panel item supported by the .dll file.</span></span> <span data-ttu-id="73d0f-127">此訊息包含主控台專案的識別碼，以及在對 [**CPL \_ INQUIRE**](cpl-inquire.md)或 [**cpl \_ NEWINQUIRE**](cpl-newinquire.md)的呼叫中， [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo)或 [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa)結構中傳回的 **lpData** 指標。</span><span class="sxs-lookup"><span data-stu-id="73d0f-127">The message includes the identifier for the Control Panel item and the **lpData** pointer returned in the [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) or [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) structure in the call to [**CPL\_INQUIRE**](cpl-inquire.md) or [**CPL\_NEWINQUIRE**](cpl-newinquire.md).</span></span> <span data-ttu-id="73d0f-128">函數應該釋放它為指定對話方塊配置的任何記憶體。</span><span class="sxs-lookup"><span data-stu-id="73d0f-128">The function should free any memory that it allocated for the specified dialog box.</span></span>

<span data-ttu-id="73d0f-129">在最後一個 CPL \_ 停止訊息之後， [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) 會接收 CPL 結束 \_ 訊息。</span><span class="sxs-lookup"><span data-stu-id="73d0f-129">After the last CPL\_STOP message, [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) receives a CPL\_EXIT message.</span></span> <span data-ttu-id="73d0f-130">函式應該釋放所有剩餘的已配置記憶體，並取消註冊任何可能已註冊的私用視窗類別。</span><span class="sxs-lookup"><span data-stu-id="73d0f-130">The function should free all remaining allocated memory and unregister any private window classes that it might have registered.</span></span> <span data-ttu-id="73d0f-131">在函式從此訊息傳回之後，Windows 會呼叫 [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) 函式來釋放主控台專案。</span><span class="sxs-lookup"><span data-stu-id="73d0f-131">Immediately after the function returns from this message, Windows releases the Control Panel item by calling the [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="73d0f-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="73d0f-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73d0f-133">主控台專案</span><span class="sxs-lookup"><span data-stu-id="73d0f-133">Control Panel Items</span></span>](control-panel-applications.md)
</dt> <dt>

[<span data-ttu-id="73d0f-134">使用者體驗指南</span><span class="sxs-lookup"><span data-stu-id="73d0f-134">User Experience Guidelines</span></span>](user-experience-guidelines.md)
</dt> <dt>

[<span data-ttu-id="73d0f-135">註冊主控台專案</span><span class="sxs-lookup"><span data-stu-id="73d0f-135">Registering Control Panel Items</span></span>](registering-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="73d0f-136">使用 CPLApplet</span><span class="sxs-lookup"><span data-stu-id="73d0f-136">Using CPLApplet</span></span>](using-cplapplet.md)
</dt> <dt>

[<span data-ttu-id="73d0f-137">執行主控台專案</span><span class="sxs-lookup"><span data-stu-id="73d0f-137">Executing Control Panel Items</span></span>](executing-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="73d0f-138">擴充系統主控台專案</span><span class="sxs-lookup"><span data-stu-id="73d0f-138">Extending System Control Panel Items</span></span>](extending-system-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="73d0f-139">指派主控台分類</span><span class="sxs-lookup"><span data-stu-id="73d0f-139">Assigning Control Panel Categories</span></span>](assigning-control-panel-categories.md)
</dt> <dt>

[<span data-ttu-id="73d0f-140">建立主控台專案的可搜尋工作連結</span><span class="sxs-lookup"><span data-stu-id="73d0f-140">Creating Searchable Task Links for a Control Panel Item</span></span>](creating-searchable-task-links.md)
</dt> <dt>

[<span data-ttu-id="73d0f-141">在 Windows Vista 下存取安全模式下的主控台</span><span class="sxs-lookup"><span data-stu-id="73d0f-141">Accessing the Control Panel in Safe Mode under Windows Vista</span></span>](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 
