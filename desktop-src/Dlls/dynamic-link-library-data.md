---
description: Dynamic-Link 程式庫 (DLL) 可以包含全域資料或本機資料。
ms.assetid: b1f6811e-c413-4124-9ccb-ea59b7a8a7ff
title: Dynamic-Link 程式庫資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83280d3bfc449061c44f9e8bfd9b47833e7eca19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988994"
---
# <a name="dynamic-link-library-data"></a><span data-ttu-id="e8621-103">Dynamic-Link 程式庫資料</span><span class="sxs-lookup"><span data-stu-id="e8621-103">Dynamic-Link Library Data</span></span>

<span data-ttu-id="e8621-104">Dynamic-Link 程式庫 (DLL) 可以包含全域資料或本機資料。</span><span class="sxs-lookup"><span data-stu-id="e8621-104">A Dynamic-Link Library (DLL) can contain global data or local data.</span></span>

## <a name="variable-scope"></a><span data-ttu-id="e8621-105">變數範圍</span><span class="sxs-lookup"><span data-stu-id="e8621-105">Variable Scope</span></span>

<span data-ttu-id="e8621-106">編譯器和連結器會將在 DLL 原始程式碼檔中宣告為全域變數的變數視為全域變數，但每個載入指定 DLL 的進程會取得自己的 DLL 全域變數複本。</span><span class="sxs-lookup"><span data-stu-id="e8621-106">Variables that are declared as global in a DLL source code file are treated as global variables by the compiler and linker, but each process that loads a given DLL gets its own copy of that DLL's global variables.</span></span> <span data-ttu-id="e8621-107">靜態變數的範圍僅限於宣告靜態變數的區塊。</span><span class="sxs-lookup"><span data-stu-id="e8621-107">The scope of static variables is limited to the block in which the static variables are declared.</span></span> <span data-ttu-id="e8621-108">因此，每個進程預設都有自己的 DLL 全域和靜態變數實例。</span><span class="sxs-lookup"><span data-stu-id="e8621-108">As a result, each process has its own instance of the DLL global and static variables by default.</span></span>

> [!Note]  
> <span data-ttu-id="e8621-109">您的開發工具可讓您覆寫預設行為。</span><span class="sxs-lookup"><span data-stu-id="e8621-109">Your development tools may allow you to override the default behavior.</span></span> <span data-ttu-id="e8621-110">例如，Visual C++ 編譯器支援 **\# pragma 區段**，而連結器支援/SECTION 選項。</span><span class="sxs-lookup"><span data-stu-id="e8621-110">For example, the Visual C++ compiler supports **\#pragma section** and the linker supports the /SECTION option.</span></span> <span data-ttu-id="e8621-111">如需詳細資訊，請參閱您的開發工具隨附的檔。</span><span class="sxs-lookup"><span data-stu-id="e8621-111">For more information, see the documentation included with your development tools.</span></span>

 

## <a name="dynamic-memory-allocation"></a><span data-ttu-id="e8621-112">動態記憶體配置</span><span class="sxs-lookup"><span data-stu-id="e8621-112">Dynamic Memory Allocation</span></span>

<span data-ttu-id="e8621-113">當 DLL 使用任何記憶體配置函式來配置記憶體時 ([**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc)、 [**LocalAlloc**](/windows/desktop/api/winbase/nf-winbase-localalloc)、 [**HeapAlloc**](/windows/desktop/api/heapapi/nf-heapapi-heapalloc)和 [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc)) ，記憶體會配置在呼叫進程的虛擬位址空間中，且只有該進程的執行緒才能存取。</span><span class="sxs-lookup"><span data-stu-id="e8621-113">When a DLL allocates memory using any of the memory allocation functions ([**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc), [**LocalAlloc**](/windows/desktop/api/winbase/nf-winbase-localalloc), [**HeapAlloc**](/windows/desktop/api/heapapi/nf-heapapi-heapalloc), and [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc)), the memory is allocated in the virtual address space of the calling process and is accessible only to the threads of that process.</span></span>

<span data-ttu-id="e8621-114">DLL 可以使用檔案對應來配置可在進程間共用的記憶體。</span><span class="sxs-lookup"><span data-stu-id="e8621-114">A DLL can use file mapping to allocate memory that can be shared among processes.</span></span> <span data-ttu-id="e8621-115">如需如何使用檔案對應來建立命名共用記憶體的一般討論，請參閱檔案 [對應](/windows/desktop/Memory/file-mapping)。</span><span class="sxs-lookup"><span data-stu-id="e8621-115">For a general discussion of how to use file mapping to create named shared memory, see [File Mapping](/windows/desktop/Memory/file-mapping).</span></span> <span data-ttu-id="e8621-116">如需使用 [**DllMain**](dllmain.md) 函式來設定使用檔案對應之共用記憶體的範例，請參閱 [使用 Dynamic-Link 程式庫中的共用記憶體](using-shared-memory-in-a-dynamic-link-library.md)。</span><span class="sxs-lookup"><span data-stu-id="e8621-116">For an example that uses the [**DllMain**](dllmain.md) function to set up shared memory using file mapping, see [Using Shared Memory in a Dynamic-Link Library](using-shared-memory-in-a-dynamic-link-library.md).</span></span>

## <a name="thread-local-storage"></a><span data-ttu-id="e8621-117">執行緒區域儲存區</span><span class="sxs-lookup"><span data-stu-id="e8621-117">Thread Local Storage</span></span>

<span data-ttu-id="e8621-118">執行緒區域儲存 (TLS) 函數可讓 DLL 配置索引，以針對多執行緒進程的每個執行緒儲存和取得不同的值。</span><span class="sxs-lookup"><span data-stu-id="e8621-118">The thread local storage (TLS) functions enable a DLL to allocate an index for storing and retrieving a different value for each thread of a multithreaded process.</span></span> <span data-ttu-id="e8621-119">例如，每次使用者開啟新的試算表時，試算表應用程式都可以建立相同執行緒的新實例。</span><span class="sxs-lookup"><span data-stu-id="e8621-119">For example, a spreadsheet application can create a new instance of the same thread each time the user opens a new spreadsheet.</span></span> <span data-ttu-id="e8621-120">提供各種試算表作業之函式的 DLL，可以使用 TLS 來儲存每個試算表目前狀態的相關資訊 (資料列、資料行等等) 。</span><span class="sxs-lookup"><span data-stu-id="e8621-120">A DLL providing the functions for various spreadsheet operations can use TLS to save information about the current state of each spreadsheet (row, column, and so on).</span></span> <span data-ttu-id="e8621-121">如需執行緒區域儲存區的一般討論，請參閱 [執行緒區域儲存區](/windows/desktop/ProcThread/thread-local-storage)。</span><span class="sxs-lookup"><span data-stu-id="e8621-121">For a general discussion of thread local storage, see [Thread Local Storage](/windows/desktop/ProcThread/thread-local-storage).</span></span> <span data-ttu-id="e8621-122">如需使用 [**DllMain**](dllmain.md) 函數設定執行緒區域儲存區的範例，請參閱 [在 Dynamic-Link 程式庫中使用執行緒區域儲存區](using-thread-local-storage-in-a-dynamic-link-library.md)。</span><span class="sxs-lookup"><span data-stu-id="e8621-122">For an example that uses the [**DllMain**](dllmain.md) function to set up thread local storage, see [Using Thread Local Storage in a Dynamic-Link Library](using-thread-local-storage-in-a-dynamic-link-library.md).</span></span>

<span data-ttu-id="e8621-123">**Windows Server 2003 和 WINDOWS XP：** Visual C++ 編譯器支援可讓您宣告執行緒區域變數的語法： **\_ declspec (執行緒)**。</span><span class="sxs-lookup"><span data-stu-id="e8621-123">**Windows Server 2003 and Windows XP:** The Visual C++ compiler supports a syntax that enables you to declare thread-local variables: **\_declspec(thread)**.</span></span> <span data-ttu-id="e8621-124">如果您在 DLL 中使用此語法，您將無法在 Windows Vista 之前的 Windows 版本上，使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 或 [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) 明確地載入 DLL。</span><span class="sxs-lookup"><span data-stu-id="e8621-124">If you use this syntax in a DLL, you will not be able to load the DLL explicitly using [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) or [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) on versions of Windows prior to Windows Vista.</span></span> <span data-ttu-id="e8621-125">如果您的 DLL 將明確載入，您必須使用執行緒區域儲存函式，而不是 **\_ declspec (執行緒)**。</span><span class="sxs-lookup"><span data-stu-id="e8621-125">If your DLL will be loaded explicitly, you must use the thread local storage functions instead of **\_declspec(thread)**.</span></span>

 

 
