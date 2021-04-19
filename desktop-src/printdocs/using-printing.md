---
description: 本節說明如何從原生 Windows 桌面程式進行列印。
ms.assetid: C1EDBE38-9D18-41BB-961C-12CF2283C639
title: 桌面應用程式列印
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbecbac997d000f50e7c912e57be42cc8fe239b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988390"
---
# <a name="desktop-app-printing"></a><span data-ttu-id="7d1bc-103">桌面應用程式列印</span><span class="sxs-lookup"><span data-stu-id="7d1bc-103">Desktop App Printing</span></span>

<span data-ttu-id="7d1bc-104">本節說明如何從原生 Windows 桌面程式進行列印。</span><span class="sxs-lookup"><span data-stu-id="7d1bc-104">This section describes how to print from a native Windows desktop program.</span></span>

## <a name="overview"></a><span data-ttu-id="7d1bc-105">概觀</span><span class="sxs-lookup"><span data-stu-id="7d1bc-105">Overview</span></span>

<span data-ttu-id="7d1bc-106">當您從原生 Windows 程式進行列印時，為了提供最佳的使用者體驗，程式必須設計成從專用的執行緒進行列印。</span><span class="sxs-lookup"><span data-stu-id="7d1bc-106">To provide the best user experience when you print from a native Windows program, the program must be designed to print from a dedicated thread.</span></span> <span data-ttu-id="7d1bc-107">在原生的 Windows 程式中，程式負責管理使用者介面事件和訊息。</span><span class="sxs-lookup"><span data-stu-id="7d1bc-107">In a native Windows program, the program is responsible for managing user interface events and messages.</span></span> <span data-ttu-id="7d1bc-108">列印工作可能需要大量計算的時間，因為應用程式內容是針對印表機呈現，如果在與使用者互動的事件處理相同的執行緒中執行這項處理，則可以防止程式回應使用者互動。</span><span class="sxs-lookup"><span data-stu-id="7d1bc-108">Printing operations can require periods of intense computation as the application content is rendered for the printer, which can prevent the program from responding to user interaction if this processing is performed in the same thread as event processing of the user interaction.</span></span>

<span data-ttu-id="7d1bc-109">如果您已經熟悉如何撰寫多執行緒原生 Windows 程式，您可以直接前往 [如何從 Windows 應用程式進行列印](how-to--print-from-a-windows-application.md) ，以及瞭解如何將列印功能新增至您的程式。</span><span class="sxs-lookup"><span data-stu-id="7d1bc-109">If you are already familiar with how to write a multi-threaded native Windows program, you go directly to [How to print from a Windows application](how-to--print-from-a-windows-application.md) and learn how to add printing functionality to your program.</span></span>

### <a name="basic-windows-program-requirements"></a><span data-ttu-id="7d1bc-110">基本 Windows 程式需求</span><span class="sxs-lookup"><span data-stu-id="7d1bc-110">Basic Windows Program Requirements</span></span>

<span data-ttu-id="7d1bc-111">為了達到最佳效能和程式回應性，請勿在處理使用者互動的執行緒中執行程式的列印工作處理。</span><span class="sxs-lookup"><span data-stu-id="7d1bc-111">For best performance and program responsiveness, do not perform a program's print job processing in the thread that processes user interaction.</span></span>

<span data-ttu-id="7d1bc-112">這種從使用者互動的列印區隔將會影響程式管理應用程式資料的方式。</span><span class="sxs-lookup"><span data-stu-id="7d1bc-112">This separation of printing from user interaction will influence how the program manages the application data.</span></span> <span data-ttu-id="7d1bc-113">在開始撰寫應用程式之前，您應該徹底瞭解這些含意。</span><span class="sxs-lookup"><span data-stu-id="7d1bc-113">You should thoroughly understand these implications before you start writing the application.</span></span> <span data-ttu-id="7d1bc-114">下列主題描述在程式的個別執行緒中處理列印的基本需求。</span><span class="sxs-lookup"><span data-stu-id="7d1bc-114">The following topics describe the basic requirements of handling printing in a separate thread of a program.</span></span>

### <a name="windows-program-basics"></a><span data-ttu-id="7d1bc-115">Windows 程式基本概念</span><span class="sxs-lookup"><span data-stu-id="7d1bc-115">Windows Program Basics</span></span>

<span data-ttu-id="7d1bc-116">原生 Windows 程式必須提供主視窗程式來處理從作業系統接收的視窗訊息。</span><span class="sxs-lookup"><span data-stu-id="7d1bc-116">A native Windows program must provide the main window procedure to process the window messages that it receives from the operating system.</span></span> <span data-ttu-id="7d1bc-117">Windows 程式中的每個視窗都有對應的 **WndProc** 函式，可處理這些視窗訊息。</span><span class="sxs-lookup"><span data-stu-id="7d1bc-117">Every window in a Windows program has a corresponding **WndProc** function that processes these window messages.</span></span> <span data-ttu-id="7d1bc-118">執行此函式的執行緒稱為使用者介面或 UI 執行緒。</span><span class="sxs-lookup"><span data-stu-id="7d1bc-118">The thread in which this function runs is called the user interface, or UI, thread.</span></span>

<span data-ttu-id="7d1bc-119">**使用資源的字串。**</span><span class="sxs-lookup"><span data-stu-id="7d1bc-119">**Use resources for strings.**</span></span>  
<span data-ttu-id="7d1bc-120">使用程式資源檔中的字串資源，而不是當您支援另一種語言時，可能需要變更之字串的字串常數。</span><span class="sxs-lookup"><span data-stu-id="7d1bc-120">Use string resources from the program's resource file instead of string constants for strings that might need to be changed when you support another language.</span></span> <span data-ttu-id="7d1bc-121">程式必須先從資源檔取出資源，然後將它複製到本機記憶體緩衝區，程式才能使用字串資源作為字串。</span><span class="sxs-lookup"><span data-stu-id="7d1bc-121">Before a program can use a string resource as a string, the program must retrieve the resource from the resource file and copy it to a local memory buffer.</span></span> <span data-ttu-id="7d1bc-122">這需要一開始就需要進行一些額外的程式設計，但是未來可以更輕鬆地修改、轉譯和當地語系化程式。</span><span class="sxs-lookup"><span data-stu-id="7d1bc-122">This requires some additional programming in the beginning, but allows for easier modification, translation, and localization of the program in the future.</span></span>  
<span data-ttu-id="7d1bc-123">**在步驟中處理資料。**</span><span class="sxs-lookup"><span data-stu-id="7d1bc-123">**Process data in steps.**</span></span>  
<span data-ttu-id="7d1bc-124">在可能中斷的步驟中處理列印工作。</span><span class="sxs-lookup"><span data-stu-id="7d1bc-124">Process the print job in steps that can be interrupted.</span></span> <span data-ttu-id="7d1bc-125">這種設計可讓使用者在完成之前取消長時間處理作業，並防止程式封鎖可能同時執行的其他程式。</span><span class="sxs-lookup"><span data-stu-id="7d1bc-125">This design makes it possible for the user to cancel a long processing operation before it completes and prevents the program from blocking other programs that might be running at the same time.</span></span>  
<span data-ttu-id="7d1bc-126">**使用視窗使用者資料。**</span><span class="sxs-lookup"><span data-stu-id="7d1bc-126">**Use window user data.**</span></span>  
<span data-ttu-id="7d1bc-127">列印應用程式通常會有數個視窗和執行緒。</span><span class="sxs-lookup"><span data-stu-id="7d1bc-127">Printing applications often have several windows and threads.</span></span> <span data-ttu-id="7d1bc-128">若要在不使用靜態的全域變數的情況下，讓執行緒和處理步驟之間的資料保持可用，請參考資料結構，此資料指標是使用它們之視窗的一部分。</span><span class="sxs-lookup"><span data-stu-id="7d1bc-128">To keep the data available between threads and processing steps without using static, global variables, reference the data structures by a data pointer that is part of the window in which they are used.</span></span>  


<span data-ttu-id="7d1bc-129">下列程式碼範例會顯示列印應用程式的主要進入點。</span><span class="sxs-lookup"><span data-stu-id="7d1bc-129">The following code example shows a main entry point for a printing application.</span></span> <span data-ttu-id="7d1bc-130">這個範例示範如何使用字串資源，而不是字串常數，也會顯示處理常式視窗訊息的主要訊息迴圈。</span><span class="sxs-lookup"><span data-stu-id="7d1bc-130">This example shows how to use string resources instead of string constants and also shows the main message loop that processes the program's window messages.</span></span>


```C++
int APIENTRY 
wWinMain(
        HINSTANCE hInstance, 
        HINSTANCE hPrevInstance, 
        LPWSTR lpCmdLine, 
        int nCmdShow
)
{
    UNREFERENCED_PARAMETER(hPrevInstance);
    UNREFERENCED_PARAMETER(lpCmdLine);

    MSG msg;
    HACCEL hAccelTable;
    HRESULT hr = S_OK;

    // Register the main window class name
    WCHAR szWindowClass[MAXIMUM_RESOURCE_STRING_LENGTH];            
    LoadString(
        hInstance, 
        IDC_PRINTSAMPLE, 
        szWindowClass, 
        MAXIMUM_RESOURCE_STRING_LENGTH);
    MyRegisterClass(hInstance, szWindowClass);

    // Perform application initialization:
    if (!InitInstance (hInstance, nCmdShow))
    {
        // Unable to initialize this instance of the application
        //  so display error message and exit
        MessageBoxWithResourceString (
            hInstance, 
            GetDesktopWindow(), 
            IDS_ERROR_INSTINITFAIL, 
            IDS_CAPTION_ERROR, 
            (MB_OK | MB_ICONEXCLAMATION));
        return FALSE;
    }    
    
    // Init COM for printing interfaces
    if (FAILED(hr = CoInitializeEx(0, COINIT_MULTITHREADED)))
    {
        // Unable to initialize COM
        //  so display error message and exit
        MessageBoxWithResourceString (
            hInstance, 
            GetDesktopWindow(), 
            IDS_ERROR_COMINITFAIL, 
            IDS_CAPTION_ERROR, 
            (MB_OK | MB_ICONEXCLAMATION));
        return FALSE;
    }

    hAccelTable = LoadAccelerators(
                    hInstance, 
                    MAKEINTRESOURCE(IDC_PRINTSAMPLE));

    // Main message handling loop
    while (GetMessage(&msg, NULL, 0, 0))
    {
        if (!TranslateAccelerator(msg.hwnd, hAccelTable, &msg))
        {
            TranslateMessage(&msg);
            DispatchMessage(&msg);
        }
    }

    // Uninitialize (close) the COM interface
    CoUninitialize();

    return (int) msg.wParam;
}
```



### <a name="document-information"></a><span data-ttu-id="7d1bc-131">檔資訊</span><span class="sxs-lookup"><span data-stu-id="7d1bc-131">Document Information</span></span>

<span data-ttu-id="7d1bc-132">列印的原生 Windows 程式應設計為多執行緒處理。</span><span class="sxs-lookup"><span data-stu-id="7d1bc-132">Native Windows programs that print should be designed for multi-threaded processing.</span></span> <span data-ttu-id="7d1bc-133">多執行緒設計的其中一個需求是保護程式的資料元素，讓多個執行緒可以安全地同時使用。</span><span class="sxs-lookup"><span data-stu-id="7d1bc-133">One of the requirements of a multi-threaded design is to protect the program's data elements so that they are safe for multiple threads to use at the same time.</span></span> <span data-ttu-id="7d1bc-134">您可以使用同步處理物件和組織資料來保護資料元素，以避免執行緒之間發生衝突。</span><span class="sxs-lookup"><span data-stu-id="7d1bc-134">You can protect data elements by using synchronization objects and organizing the data to avoid conflicts between the threads.</span></span> <span data-ttu-id="7d1bc-135">同時，程式必須在列印時防止變更程式資料。</span><span class="sxs-lookup"><span data-stu-id="7d1bc-135">At the same time, the program must prevent changes to the program data while it is being printed.</span></span> <span data-ttu-id="7d1bc-136">範例程式使用數個不同的多執行緒程式設計技術。</span><span class="sxs-lookup"><span data-stu-id="7d1bc-136">The sample program uses several different multi-threaded programming techniques.</span></span>

 <span data-ttu-id="7d1bc-137">**同步處理事件**</span><span class="sxs-lookup"><span data-stu-id="7d1bc-137">**Synchronization Events**</span></span>  
<span data-ttu-id="7d1bc-138">範例程式會使用事件、執行緒控制碼和 wait 函式來同步處理列印執行緒和主要程式之間的處理，以及表示資料正在使用中。</span><span class="sxs-lookup"><span data-stu-id="7d1bc-138">The sample program uses events, thread handles, and wait functions to synchronize the processing between the print thread and the main program and to indicate that the data is in use.</span></span>  
<span data-ttu-id="7d1bc-139">**應用程式特定的 Windows 訊息**</span><span class="sxs-lookup"><span data-stu-id="7d1bc-139">**Application-Specific Windows Messages**</span></span>  
<span data-ttu-id="7d1bc-140">範例程式會使用應用程式特定的視窗訊息，讓程式與其他原生 Windows 程式更相容。</span><span class="sxs-lookup"><span data-stu-id="7d1bc-140">The sample program uses application-specific window messages to make the program more compatible with other native Windows programs.</span></span> <span data-ttu-id="7d1bc-141">將處理常式分成較小的步驟，並在視窗訊息迴圈中將這些步驟排入佇列，可讓 Windows 更輕鬆地管理處理，而不會封鎖可能也會在電腦上執行的其他應用程式。</span><span class="sxs-lookup"><span data-stu-id="7d1bc-141">Breaking the processing into smaller steps and queuing those steps in the window message loop makes it easier for Windows to manage the processing without blocking other applications that might also be running on the computer.</span></span>  
<span data-ttu-id="7d1bc-142">**資料結構**</span><span class="sxs-lookup"><span data-stu-id="7d1bc-142">**Data Structures**</span></span>  
<span data-ttu-id="7d1bc-143">範例程式不是使用物件和類別以物件導向的樣式來撰寫，雖然它會將資料元素分組到資料結構中。</span><span class="sxs-lookup"><span data-stu-id="7d1bc-143">The sample program is not written in an object-oriented style using objects and classes, although it does group data elements into data structures.</span></span> <span data-ttu-id="7d1bc-144">此範例不會使用物件導向的方法，以避免其中一個方法比另一個方法更好或更糟。</span><span class="sxs-lookup"><span data-stu-id="7d1bc-144">The sample does not use an object-oriented approach to avoid implying that one approach is better or worse than another.</span></span>  
<span data-ttu-id="7d1bc-145">當您設計程式時，可以使用範例程式的函式和資料結構作為起點。</span><span class="sxs-lookup"><span data-stu-id="7d1bc-145">You can use the functions and data structures of the sample program as a starting point when you design your program.</span></span> <span data-ttu-id="7d1bc-146">無論您是否決定設計物件導向程式，要記住的重要設計考慮是將相關的資料元素分組，讓您可以視需要在不同的執行緒中安全地使用它們。</span><span class="sxs-lookup"><span data-stu-id="7d1bc-146">Whether you decide to design an object-oriented program or not, the important design consideration to remember is to group the related data elements so that you can use them safely in different threads as necessary.</span></span>  


### <a name="printer-device-context"></a><span data-ttu-id="7d1bc-147">印表機裝置內容</span><span class="sxs-lookup"><span data-stu-id="7d1bc-147">Printer Device Context</span></span>

<span data-ttu-id="7d1bc-148">列印時，您可能會想要將內容轉譯為要列印到裝置內容。</span><span class="sxs-lookup"><span data-stu-id="7d1bc-148">When printing, you might want to render the content to be printed to a device context.</span></span> <span data-ttu-id="7d1bc-149">[如何：取出印表機裝置內容](retrieving-a-printer-device-context.md) 說明您可以取得印表機裝置內容的不同方式。</span><span class="sxs-lookup"><span data-stu-id="7d1bc-149">[How To: Retrieve a Printer Device Context](retrieving-a-printer-device-context.md) describes the different ways that you can obtain a printer device context.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7d1bc-150">相關主題</span><span class="sxs-lookup"><span data-stu-id="7d1bc-150">Related topics</span></span>



[<span data-ttu-id="7d1bc-151">如何從 Windows 應用程式列印</span><span class="sxs-lookup"><span data-stu-id="7d1bc-151">How to print from a Windows application</span></span>](how-to--print-from-a-windows-application.md)


 

 



