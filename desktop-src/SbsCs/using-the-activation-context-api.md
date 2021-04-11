---
description: 應用程式可以直接呼叫啟用內容函式來管理啟用內容。
ms.assetid: 606147a8-435d-43d4-8fb5-79d2d1a8d870
title: 使用啟用內容 API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62b3aec5b7840e70e8fae93575e65c2f06668936
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112693"
---
# <a name="using-the-activation-context-api"></a><span data-ttu-id="0ee6d-103">使用啟用內容 API</span><span class="sxs-lookup"><span data-stu-id="0ee6d-103">Using the Activation Context API</span></span>

<span data-ttu-id="0ee6d-104">應用程式可以直接呼叫啟用內容函式來管理 [啟用內容](activation-contexts.md) 。</span><span class="sxs-lookup"><span data-stu-id="0ee6d-104">Applications can manage an [activation context](activation-contexts.md) by directly calling the activation context functions.</span></span> <span data-ttu-id="0ee6d-105">啟用內容是記憶體中的資料結構。</span><span class="sxs-lookup"><span data-stu-id="0ee6d-105">Activation contexts are data structures in memory.</span></span> <span data-ttu-id="0ee6d-106">系統可以使用啟用內容中的資訊，將應用程式重新導向以載入特定 DLL 版本、COM 物件實例或自訂視窗版本。</span><span class="sxs-lookup"><span data-stu-id="0ee6d-106">The system can use the information in the activation context to redirect an application to load a particular DLL version, COM object instance, or custom window version.</span></span> <span data-ttu-id="0ee6d-107">如需詳細資訊，請參閱 [啟用內容參考](activation-context-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="0ee6d-107">For more information, see [Activation Context Reference](activation-context-reference.md).</span></span>

<span data-ttu-id="0ee6d-108"> (API) 的應用程式開發介面可以用來管理啟用內容，並使用 [資訊清單](manifests.md)來建立版本命名的物件。</span><span class="sxs-lookup"><span data-stu-id="0ee6d-108">The application programming interface (API) can be used to manage the activation context and create version-named objects with [manifests](manifests.md).</span></span> <span data-ttu-id="0ee6d-109">下列兩個案例說明應用程式如何藉由直接呼叫啟用內容函式來管理啟用內容。</span><span class="sxs-lookup"><span data-stu-id="0ee6d-109">The following two scenarios illustrate how an application can manage an activation context by directly calling the activation context functions.</span></span> <span data-ttu-id="0ee6d-110">不過，在大部分情況下，啟用內容是由系統所管理。</span><span class="sxs-lookup"><span data-stu-id="0ee6d-110">In most cases however, the activation context is managed by the system.</span></span> <span data-ttu-id="0ee6d-111">應用程式開發人員和元件提供者通常不需要對堆疊進行呼叫來管理啟用內容。</span><span class="sxs-lookup"><span data-stu-id="0ee6d-111">Application developers and assembly providers do not commonly need to make calls to the stack to manage the activation context.</span></span>

-   <span data-ttu-id="0ee6d-112">執行間接取值或分派層的進程和應用程式。</span><span class="sxs-lookup"><span data-stu-id="0ee6d-112">Processes and applications that implement indirection or dispatch layers.</span></span>

    <span data-ttu-id="0ee6d-113">例如，在事件迴圈中管理啟用內容的使用者。</span><span class="sxs-lookup"><span data-stu-id="0ee6d-113">For example, a user managing activation contexts in the event loop.</span></span> <span data-ttu-id="0ee6d-114">每次存取視窗時（例如將滑鼠移至視窗上方）都會呼叫 [**ActivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-activateactctx) ，以啟動資源目前的啟用內容，如下列程式碼片段所示。</span><span class="sxs-lookup"><span data-stu-id="0ee6d-114">Each time the window is accessed, such as by moving the mouse over the window, [**ActivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-activateactctx) is called, which activates the current activation context for the resource, as shown in the following code fragment.</span></span>

    <dl> <span data-ttu-id="0ee6d-115">處理 hActCtx;</span><span class="sxs-lookup"><span data-stu-id="0ee6d-115">HANDLE hActCtx;</span></span>  
    <span data-ttu-id="0ee6d-116">CreateWindow () ;</span><span class="sxs-lookup"><span data-stu-id="0ee6d-116">CreateWindow();</span></span>  
    <span data-ttu-id="0ee6d-117">...</span><span class="sxs-lookup"><span data-stu-id="0ee6d-117">...</span></span>  
    <span data-ttu-id="0ee6d-118">GetCurrentActCtx (&ActCtx) ;</span><span class="sxs-lookup"><span data-stu-id="0ee6d-118">GetCurrentActCtx(&ActCtx);</span></span>  
    <span data-ttu-id="0ee6d-119">...</span><span class="sxs-lookup"><span data-stu-id="0ee6d-119">...</span></span>  
    <span data-ttu-id="0ee6d-120">ReleaseActCtx (&ActCtx) ;</span><span class="sxs-lookup"><span data-stu-id="0ee6d-120">ReleaseActCtx(&ActCtx);</span></span>  
    </dl>

    <span data-ttu-id="0ee6d-121">在下列程式碼片段中，API 函式會先啟用適當的啟用內容，然後再呼叫 [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca)。</span><span class="sxs-lookup"><span data-stu-id="0ee6d-121">In the following code fragment, the API function activates the appropriate activation contexts before calling [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca).</span></span> <span data-ttu-id="0ee6d-122">當呼叫 **CallWindowProc** 時，它會使用此內容將訊息傳遞給 Windows。</span><span class="sxs-lookup"><span data-stu-id="0ee6d-122">When **CallWindowProc** is called, it uses this context to pass a message to Windows.</span></span> <span data-ttu-id="0ee6d-123">當所有資源作業都完成時，此函式將會停用內容。</span><span class="sxs-lookup"><span data-stu-id="0ee6d-123">When all resource operations have completed, the function will deactivate the context.</span></span>

    <dl> <span data-ttu-id="0ee6d-124">ULONG \_ PTR ulpCookie;</span><span class="sxs-lookup"><span data-stu-id="0ee6d-124">ULONG\_PTR ulpCookie;</span></span>  
    <span data-ttu-id="0ee6d-125">處理 hActCtx;</span><span class="sxs-lookup"><span data-stu-id="0ee6d-125">HANDLE hActCtx;</span></span>  
    <span data-ttu-id="0ee6d-126">如果 (ActivateActCtx (hActCtx，&ulpCookie) ) </span><span class="sxs-lookup"><span data-stu-id="0ee6d-126">if(ActivateActCtx(hActCtx, &ulpCookie))</span></span>  
    <span data-ttu-id="0ee6d-127">{</span><span class="sxs-lookup"><span data-stu-id="0ee6d-127">{</span></span>  
    <span data-ttu-id="0ee6d-128">...</span><span class="sxs-lookup"><span data-stu-id="0ee6d-128">...</span></span>  
    <span data-ttu-id="0ee6d-129">CallWindowProc ( ... ) ;</span><span class="sxs-lookup"><span data-stu-id="0ee6d-129">CallWindowProc(...);</span></span>  
    <span data-ttu-id="0ee6d-130">...</span><span class="sxs-lookup"><span data-stu-id="0ee6d-130">...</span></span>  
    <span data-ttu-id="0ee6d-131">DeactivateActCtx (0、ulpCookie) ;</span><span class="sxs-lookup"><span data-stu-id="0ee6d-131">DeactivateActCtx(0, ulpCookie);</span></span>  
    <span data-ttu-id="0ee6d-132">}</span><span class="sxs-lookup"><span data-stu-id="0ee6d-132">}</span></span>  
    </dl>

-   <span data-ttu-id="0ee6d-133">Delegator 分派層。</span><span class="sxs-lookup"><span data-stu-id="0ee6d-133">Delegator dispatch layer.</span></span>

    <span data-ttu-id="0ee6d-134">此案例適用于使用通用 API 層（例如驅動程式管理員）管理多個實體的管理員。</span><span class="sxs-lookup"><span data-stu-id="0ee6d-134">This scenario applies to managers that manage multiple entities with a common API layer, such as a driver manager.</span></span> <span data-ttu-id="0ee6d-135">雖然尚未實作為範例，但這是 ODBC 驅動程式。</span><span class="sxs-lookup"><span data-stu-id="0ee6d-135">Although it has not yet been implemented, an example of this would be the ODBC driver.</span></span>

    <span data-ttu-id="0ee6d-136">在此案例中，仲介層將能夠處理元件系結。</span><span class="sxs-lookup"><span data-stu-id="0ee6d-136">In this scenario, the middle layer becomes capable of processing assembly bindings.</span></span> <span data-ttu-id="0ee6d-137">若要取得版本特定的系結驅動程式，發行者必須提供資訊清單，並指定該資訊清單中特定元件的相依性。</span><span class="sxs-lookup"><span data-stu-id="0ee6d-137">To get the version-specific binding driver, publishers must provide a manifest and specify dependencies on specific components in that manifest.</span></span> <span data-ttu-id="0ee6d-138">基底應用程式不會動態繫結至元件;在執行時間，驅動程式管理員會管理呼叫。</span><span class="sxs-lookup"><span data-stu-id="0ee6d-138">The base application does not dynamically bind to the components; at run time, the driver manager manages the calls.</span></span> <span data-ttu-id="0ee6d-139">當根據連接字串呼叫 ODBC 驅動程式時，它會載入適當的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="0ee6d-139">When the ODBC driver is called based on the connect string it loads the appropriate driver.</span></span> <span data-ttu-id="0ee6d-140">然後，它會使用組件資訊清單檔中的資訊來建立啟用內容。</span><span class="sxs-lookup"><span data-stu-id="0ee6d-140">It then creates the activation context using the information in the assembly manifest file.</span></span>

    <span data-ttu-id="0ee6d-141">如果沒有資訊清單，驅動程式的預設動作會使用與應用程式所指定的相同內容，在此範例中為 MSVCRT.LIB 的第2版。</span><span class="sxs-lookup"><span data-stu-id="0ee6d-141">Without the manifest, the default action for the driver is to use the same context as that specified by the application—in this example, version 2 of MSVCRT.</span></span> <span data-ttu-id="0ee6d-142">因為資訊清單存在，所以會建立個別的啟用內容。</span><span class="sxs-lookup"><span data-stu-id="0ee6d-142">Since a manifest does exist, a separate activation context is established.</span></span> <span data-ttu-id="0ee6d-143">當 ODBC 驅動程式執行時，它會系結至 MSVCRT.LIB 元件的第1版。</span><span class="sxs-lookup"><span data-stu-id="0ee6d-143">When the ODBC driver runs, it binds to version 1 of the MSVCRT assembly.</span></span>

    <span data-ttu-id="0ee6d-144">每次驅動程式管理員呼叫分派層時（例如，取得下一組資料），就會根據啟用內容使用適當的元件。</span><span class="sxs-lookup"><span data-stu-id="0ee6d-144">Each time the driver manager calls the dispatch layer—for example, to get the next set of data—it uses the appropriate assemblies based on the activation context.</span></span> <span data-ttu-id="0ee6d-145">下列程式碼片段說明這一點。</span><span class="sxs-lookup"><span data-stu-id="0ee6d-145">The following code fragment illustrates this.</span></span>

    <dl> <span data-ttu-id="0ee6d-146">處理 hActCtx;</span><span class="sxs-lookup"><span data-stu-id="0ee6d-146">HANDLE hActCtx;</span></span>  
    <span data-ttu-id="0ee6d-147">ULONG \_ PTR ulpCookie;</span><span class="sxs-lookup"><span data-stu-id="0ee6d-147">ULONG\_PTR ulpCookie;</span></span>  
    <span data-ttu-id="0ee6d-148">ACTCTX ActCtxToCreate = {...};</span><span class="sxs-lookup"><span data-stu-id="0ee6d-148">ACTCTX ActCtxToCreate = {...};</span></span>  
    <span data-ttu-id="0ee6d-149">hActCtx = CreateActCtx (&ActCtxToCreate) ;</span><span class="sxs-lookup"><span data-stu-id="0ee6d-149">hActCtx = CreateActCtx(&ActCtxToCreate);</span></span>  
    <span data-ttu-id="0ee6d-150">...;</span><span class="sxs-lookup"><span data-stu-id="0ee6d-150">...;</span></span>  
    <span data-ttu-id="0ee6d-151">如果 (ActivateActCtx (hActCtx，&ulpCookie) ) </span><span class="sxs-lookup"><span data-stu-id="0ee6d-151">if (ActivateActCtx(hActCtx, &ulpCookie))</span></span>  
    <span data-ttu-id="0ee6d-152">{</span><span class="sxs-lookup"><span data-stu-id="0ee6d-152">{</span></span>  
    <span data-ttu-id="0ee6d-153">...</span><span class="sxs-lookup"><span data-stu-id="0ee6d-153">...</span></span>  
    <span data-ttu-id="0ee6d-154">ConnectDb ( ... ) ;</span><span class="sxs-lookup"><span data-stu-id="0ee6d-154">ConnectDb(...);</span></span>  
    <span data-ttu-id="0ee6d-155">DeactivateActCtx (0、ulpCookie) ;</span><span class="sxs-lookup"><span data-stu-id="0ee6d-155">DeactivateActCtx(0, ulpCookie);</span></span>  
    <span data-ttu-id="0ee6d-156">}</span><span class="sxs-lookup"><span data-stu-id="0ee6d-156">}</span></span>  
    <span data-ttu-id="0ee6d-157">...</span><span class="sxs-lookup"><span data-stu-id="0ee6d-157">...</span></span>  
    <span data-ttu-id="0ee6d-158">ReleaseActCtx (hActCtx) ;</span><span class="sxs-lookup"><span data-stu-id="0ee6d-158">ReleaseActCtx(hActCtx);</span></span>  
    </dl>

 

 
