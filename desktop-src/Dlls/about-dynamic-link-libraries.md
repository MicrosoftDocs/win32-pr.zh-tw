---
description: 動態連結可讓模組只包含在載入時間或執行時間尋找匯出的 DLL 函式所需的資訊。
ms.assetid: df2a8e4c-7ad0-46ea-9643-1528a9ea1503
title: 關於 Dynamic-Link 程式庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bdb24048e17e9164aaf39d0ab337aea33576c95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848419"
---
# <a name="about-dynamic-link-libraries"></a><span data-ttu-id="84354-103">關於 Dynamic-Link 程式庫</span><span class="sxs-lookup"><span data-stu-id="84354-103">About Dynamic-Link Libraries</span></span>

<span data-ttu-id="84354-104">動態連結可讓模組只包含在載入時間或執行時間尋找匯出的 DLL 函式所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="84354-104">Dynamic linking allows a module to include only the information needed to locate an exported DLL function at load time or run time.</span></span> <span data-ttu-id="84354-105">動態連結不同于較熟悉的靜態連結，連結器會將程式庫函式的程式碼複製到呼叫它的每個模組。</span><span class="sxs-lookup"><span data-stu-id="84354-105">Dynamic linking differs from the more familiar static linking, in which the linker copies a library function's code into each module that calls it.</span></span>

## <a name="types-of-dynamic-linking"></a><span data-ttu-id="84354-106">動態連結的類型</span><span class="sxs-lookup"><span data-stu-id="84354-106">Types of Dynamic Linking</span></span>

<span data-ttu-id="84354-107">有兩種方法可以在 DLL 中呼叫函數：</span><span class="sxs-lookup"><span data-stu-id="84354-107">There are two methods for calling a function in a DLL:</span></span>

-   <span data-ttu-id="84354-108">在 *載入時間動態連結* 中，模組會對匯出的 DLL 函式發出明確的呼叫，就像它們是區域函數一樣。</span><span class="sxs-lookup"><span data-stu-id="84354-108">In *load-time dynamic linking*, a module makes explicit calls to exported DLL functions as if they were local functions.</span></span> <span data-ttu-id="84354-109">這需要您將模組與包含函式之 DLL 的匯入程式庫連結。</span><span class="sxs-lookup"><span data-stu-id="84354-109">This requires you to link the module with the import library for the DLL that contains the functions.</span></span> <span data-ttu-id="84354-110">匯入程式庫會提供系統載入 DLL 所需的資訊，並在載入應用程式時找出匯出的 DLL 函式。</span><span class="sxs-lookup"><span data-stu-id="84354-110">An import library supplies the system with the information needed to load the DLL and locate the exported DLL functions when the application is loaded.</span></span>
-   <span data-ttu-id="84354-111">在 *執行時間動態連結* 中，模組會使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 或 [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) 函數，在執行時間載入 DLL。</span><span class="sxs-lookup"><span data-stu-id="84354-111">In *run-time dynamic linking*, a module uses the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) or [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) function to load the DLL at run time.</span></span> <span data-ttu-id="84354-112">載入 DLL 之後，模組會呼叫 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函式來取得匯出的 dll 函式的位址。</span><span class="sxs-lookup"><span data-stu-id="84354-112">After the DLL is loaded, the module calls the [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) function to get the addresses of the exported DLL functions.</span></span> <span data-ttu-id="84354-113">模組會使用 **GetProcAddress** 傳回的函式指標來呼叫匯出的 DLL 函式。</span><span class="sxs-lookup"><span data-stu-id="84354-113">The module calls the exported DLL functions using the function pointers returned by **GetProcAddress**.</span></span> <span data-ttu-id="84354-114">這樣就不需要匯入程式庫。</span><span class="sxs-lookup"><span data-stu-id="84354-114">This eliminates the need for an import library.</span></span>

## <a name="dlls-and-memory-management"></a><span data-ttu-id="84354-115">Dll 和記憶體管理</span><span class="sxs-lookup"><span data-stu-id="84354-115">DLLs and Memory Management</span></span>

<span data-ttu-id="84354-116">載入 DLL 的每個進程都會將其對應至其虛擬位址空間。</span><span class="sxs-lookup"><span data-stu-id="84354-116">Every process that loads the DLL maps it into its virtual address space.</span></span> <span data-ttu-id="84354-117">在進程將 DLL 載入其虛擬位址之後，它就可以呼叫匯出的 DLL 函式。</span><span class="sxs-lookup"><span data-stu-id="84354-117">After the process loads the DLL into its virtual address, it can call the exported DLL functions.</span></span>

<span data-ttu-id="84354-118">系統會為每個 DLL 維護每個進程的參考計數。</span><span class="sxs-lookup"><span data-stu-id="84354-118">The system maintains a per-process reference count for each DLL.</span></span> <span data-ttu-id="84354-119">當執行緒載入 DLL 時，參考計數會遞增一。</span><span class="sxs-lookup"><span data-stu-id="84354-119">When a thread loads the DLL, the reference count is incremented by one.</span></span> <span data-ttu-id="84354-120">當進程結束時，或當參考計數變成零 (執行時間動態連結) 時，會從進程的虛擬位址空間卸載 DLL。</span><span class="sxs-lookup"><span data-stu-id="84354-120">When the process terminates, or when the reference count becomes zero (run-time dynamic linking only), the DLL is unloaded from the virtual address space of the process.</span></span>

<span data-ttu-id="84354-121">如同任何其他函式，匯出的 DLL 函式會在呼叫它的執行緒內容中執行。</span><span class="sxs-lookup"><span data-stu-id="84354-121">Like any other function, an exported DLL function runs in the context of the thread that calls it.</span></span> <span data-ttu-id="84354-122">因此，下列條件適用：</span><span class="sxs-lookup"><span data-stu-id="84354-122">Therefore, the following conditions apply:</span></span>

-   <span data-ttu-id="84354-123">呼叫 DLL 之進程的執行緒可以使用 DLL 函式所開啟的控制碼。</span><span class="sxs-lookup"><span data-stu-id="84354-123">The threads of the process that called the DLL can use handles opened by a DLL function.</span></span> <span data-ttu-id="84354-124">同樣地，呼叫進程的任何執行緒所開啟的控制碼都可以在 DLL 函數中使用。</span><span class="sxs-lookup"><span data-stu-id="84354-124">Similarly, handles opened by any thread of the calling process can be used in the DLL function.</span></span>
-   <span data-ttu-id="84354-125">DLL 會使用呼叫執行緒的堆疊，以及呼叫進程的虛擬位址空間。</span><span class="sxs-lookup"><span data-stu-id="84354-125">The DLL uses the stack of the calling thread and the virtual address space of the calling process.</span></span>
-   <span data-ttu-id="84354-126">DLL 會從呼叫進程的虛擬位址空間配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="84354-126">The DLL allocates memory from the virtual address space of the calling process.</span></span>

<span data-ttu-id="84354-127">如需 Dll 的詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="84354-127">For more information about DLLs, see the following topics:</span></span>

-   [<span data-ttu-id="84354-128">動態連結的優點</span><span class="sxs-lookup"><span data-stu-id="84354-128">Advantages of Dynamic Linking</span></span>](advantages-of-dynamic-linking.md)
-   [<span data-ttu-id="84354-129">動態連結程式庫建立</span><span class="sxs-lookup"><span data-stu-id="84354-129">Dynamic-Link Library Creation</span></span>](dynamic-link-library-creation.md)
-   [<span data-ttu-id="84354-130">動態連結程式庫 Entry-Point 函式</span><span class="sxs-lookup"><span data-stu-id="84354-130">Dynamic-Link Library Entry-Point Function</span></span>](dynamic-link-library-entry-point-function.md)
-   [<span data-ttu-id="84354-131">載入時間動態連結</span><span class="sxs-lookup"><span data-stu-id="84354-131">Load-Time Dynamic Linking</span></span>](load-time-dynamic-linking.md)
-   [<span data-ttu-id="84354-132">執行時間動態連結</span><span class="sxs-lookup"><span data-stu-id="84354-132">Run-Time Dynamic Linking</span></span>](run-time-dynamic-linking.md)
-   [<span data-ttu-id="84354-133">動態連結程式庫搜尋順序</span><span class="sxs-lookup"><span data-stu-id="84354-133">Dynamic-Link Library Search Order</span></span>](dynamic-link-library-search-order.md)
-   [<span data-ttu-id="84354-134">動態連結程式庫資料</span><span class="sxs-lookup"><span data-stu-id="84354-134">Dynamic-Link Library Data</span></span>](dynamic-link-library-data.md)
-   [<span data-ttu-id="84354-135">動態連結程式庫重新導向</span><span class="sxs-lookup"><span data-stu-id="84354-135">Dynamic-Link Library Redirection</span></span>](dynamic-link-library-redirection.md)
-   [<span data-ttu-id="84354-136">動態連結程式庫更新</span><span class="sxs-lookup"><span data-stu-id="84354-136">Dynamic-Link Library Updates</span></span>](dynamic-link-library-updates.md)
-   [<span data-ttu-id="84354-137">動態連結程式庫安全性</span><span class="sxs-lookup"><span data-stu-id="84354-137">Dynamic-Link Library Security</span></span>](dynamic-link-library-security.md)
-   [<span data-ttu-id="84354-138">AppInit Dll 和安全開機</span><span class="sxs-lookup"><span data-stu-id="84354-138">AppInit DLLs and Secure Boot</span></span>](secure-boot-and-appinit-dlls.md)

 

 
