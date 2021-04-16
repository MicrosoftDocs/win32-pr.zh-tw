---
description: 從外部進程載入圖形
ms.assetid: 1c657c7f-46d7-4feb-88a7-4a3227c9070b
title: 從外部進程載入圖形
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eac42db3a87b00b1cb8f3a9ae5297215ae9bd3fa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104560161"
---
# <a name="loading-a-graph-from-an-external-process"></a><span data-ttu-id="e0a6c-103">從外部進程載入圖形</span><span class="sxs-lookup"><span data-stu-id="e0a6c-103">Loading a Graph From an External Process</span></span>

<span data-ttu-id="e0a6c-104">GraphEdit 可以載入外部進程所建立的篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="e0a6c-104">GraphEdit can load a filter graph created by an external process.</span></span> <span data-ttu-id="e0a6c-105">使用這項功能，您可以查看應用程式所建立的篩選圖形，而且您的應用程式中只會有少量的額外程式碼。</span><span class="sxs-lookup"><span data-stu-id="e0a6c-105">With this feature, you can see exactly what filter graph your application builds, with only a minimal amount of additional code in your application.</span></span>

> [!Note]  
> <span data-ttu-id="e0a6c-106">這項功能需要 Windows 2000、Windows XP 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="e0a6c-106">This feature requires Windows 2000, Windows XP, or later.</span></span>

 

> [!Note]  
> <span data-ttu-id="e0a6c-107">從 Windows Vista 開始，您必須註冊 proppage.dll 以啟用這項功能。</span><span class="sxs-lookup"><span data-stu-id="e0a6c-107">Starting in Windows Vista, you must register proppage.dll to enable this feature.</span></span> <span data-ttu-id="e0a6c-108">Proppage.dll 包含在 Windows SDK 中。</span><span class="sxs-lookup"><span data-stu-id="e0a6c-108">Proppage.dll is included in the Windows SDK.</span></span>

 

<span data-ttu-id="e0a6c-109">應用程式必須在執行中的物件資料表中註冊篩選圖形實例， (的 ROT) 。</span><span class="sxs-lookup"><span data-stu-id="e0a6c-109">The application must register the filter graph instance in the Running Object Table (ROT).</span></span> <span data-ttu-id="e0a6c-110">ROT 是可全域存取的查閱資料表，可追蹤正在執行的物件。</span><span class="sxs-lookup"><span data-stu-id="e0a6c-110">The ROT is a globally accessible look-up table that keeps track of running objects.</span></span> <span data-ttu-id="e0a6c-111">物件是在 ROT 中依標記註冊。</span><span class="sxs-lookup"><span data-stu-id="e0a6c-111">Objects are registered in the ROT by moniker.</span></span> <span data-ttu-id="e0a6c-112">若要連接到圖形，GraphEdit 會在 ROT 搜尋其顯示名稱符合特定格式的名字：</span><span class="sxs-lookup"><span data-stu-id="e0a6c-112">To connect to the graph, GraphEdit searches the ROT for monikers whose display name matches a particular format:</span></span>


```C++
!FilterGraph X pid Y
```



<span data-ttu-id="e0a6c-113">其中 *X* 是篩選圖形管理員的十六進位位址，而 *Y* 是處理序識別碼，也是十六進位。</span><span class="sxs-lookup"><span data-stu-id="e0a6c-113">where *X* is the hexadecimal address of the Filter Graph Manager, and *Y* is the process id, also in hexadecimal.</span></span>

<span data-ttu-id="e0a6c-114">當您的應用程式第一次建立篩選圖形時，請呼叫下列函數：</span><span class="sxs-lookup"><span data-stu-id="e0a6c-114">When your application first creates the filter graph, call the following function:</span></span>


```C++
HRESULT AddToRot(IUnknown *pUnkGraph, DWORD *pdwRegister) 
{
    IMoniker * pMoniker = NULL;
    IRunningObjectTable *pROT = NULL;

    if (FAILED(GetRunningObjectTable(0, &pROT))) 
    {
        return E_FAIL;
    }
    
    const size_t STRING_LENGTH = 256;

    WCHAR wsz[STRING_LENGTH];
 
   StringCchPrintfW(
        wsz, STRING_LENGTH, 
        L"FilterGraph %08x pid %08x", 
        (DWORD_PTR)pUnkGraph, 
        GetCurrentProcessId()
        );
    
    HRESULT hr = CreateItemMoniker(L"!", wsz, &pMoniker);
    if (SUCCEEDED(hr)) 
    {
        hr = pROT->Register(ROTFLAGS_REGISTRATIONKEEPSALIVE, pUnkGraph,
            pMoniker, pdwRegister);
        pMoniker->Release();
    }
    pROT->Release();
    
    return hr;
}
```



<span data-ttu-id="e0a6c-115">此函數會建立篩選圖形的標記和新的 ROT 專案。</span><span class="sxs-lookup"><span data-stu-id="e0a6c-115">This function creates a moniker and a new ROT entry for the filter graph.</span></span> <span data-ttu-id="e0a6c-116">第一個參數是篩選圖形的指標。</span><span class="sxs-lookup"><span data-stu-id="e0a6c-116">The first parameter is a pointer to the filter graph.</span></span> <span data-ttu-id="e0a6c-117">第二個參數會接收可識別新的 ROT 專案的值。</span><span class="sxs-lookup"><span data-stu-id="e0a6c-117">The second parameter receives a value that identifies the new ROT entry.</span></span> <span data-ttu-id="e0a6c-118">在應用程式釋放篩選圖形之前，呼叫下列函式以移除 ROT 專案。</span><span class="sxs-lookup"><span data-stu-id="e0a6c-118">Before the application releases the filter graph, call the following function to remove the ROT entry.</span></span> <span data-ttu-id="e0a6c-119">*PdwRegister* 參數是 AddToRot 函數所傳回的識別碼。</span><span class="sxs-lookup"><span data-stu-id="e0a6c-119">The *pdwRegister* parameter is the identifier returned by the AddToRot function.</span></span>


```C++
void RemoveFromRot(DWORD pdwRegister)
{
    IRunningObjectTable *pROT;
    if (SUCCEEDED(GetRunningObjectTable(0, &pROT))) {
        pROT->Revoke(pdwRegister);
        pROT->Release();
    }
}
```



<span data-ttu-id="e0a6c-120">下列程式碼範例顯示如何呼叫這些函式。</span><span class="sxs-lookup"><span data-stu-id="e0a6c-120">The following code example shows how to call these functions.</span></span> <span data-ttu-id="e0a6c-121">在此範例中，會有條件地編譯加入和移除 ROT 專案的程式碼，使其只包含在 debug 組建中。</span><span class="sxs-lookup"><span data-stu-id="e0a6c-121">In this example, the code that adds and removes ROT entries is conditionally compiled, so that it is included only in debug builds.</span></span>


```C++
IGraphBuilder *pGraph;
DWORD dwRegister;
    
// Create the filter graph manager.
CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER,
                        IID_IGraphBuilder, (void **)&pGraph);
#ifdef _DEBUG
hr = AddToRot(pGraph, &dwRegister);
#endif

// Rest of the application (not shown).

#ifdef _DEBUG
RemoveFromRot(dwRegister);
#endif
pGraph->Release();
```



<span data-ttu-id="e0a6c-122">若要在 GraphEdit 中查看篩選圖形，請同時執行您的應用程式和 GraphEdit。</span><span class="sxs-lookup"><span data-stu-id="e0a6c-122">To view the filter graph in GraphEdit, run your application and GraphEdit at the same time.</span></span> <span data-ttu-id="e0a6c-123">在 **[GraphEdit 檔案** ] 功能表中，按一下 [連線 **到遠端圖形** ]。在 [ **連接到圖形** ] 對話方塊中，選取應用程式的處理序識別碼 (pid) ，然後按一下 **[確定]**。</span><span class="sxs-lookup"><span data-stu-id="e0a6c-123">In the GraphEdit **File** menu, click **Connect to Remote Graph...** In the **Connect To Graph** dialog box, select the process id (pid) of your application and click **OK**.</span></span> <span data-ttu-id="e0a6c-124">GraphEdit 會載入篩選圖形並顯示它。</span><span class="sxs-lookup"><span data-stu-id="e0a6c-124">GraphEdit loads the filter graph and displays it.</span></span> <span data-ttu-id="e0a6c-125">請勿在此圖形上使用任何其他 GraphEdit 功能，這可能會導致非預期的結果。</span><span class="sxs-lookup"><span data-stu-id="e0a6c-125">Don't use any other GraphEdit features on this graph—it might cause unexpected results.</span></span> <span data-ttu-id="e0a6c-126">例如，不要新增或移除篩選，或停止和啟動圖形。</span><span class="sxs-lookup"><span data-stu-id="e0a6c-126">For example, don't add or remove filters, or stop and start the graph.</span></span> <span data-ttu-id="e0a6c-127">結束您的應用程式之前，請關閉 GraphEdit。</span><span class="sxs-lookup"><span data-stu-id="e0a6c-127">Close GraphEdit before exiting your application.</span></span>

> [!Note]  
> <span data-ttu-id="e0a6c-128">當您的應用程式結束時，可能會遇到各種判斷提示。</span><span class="sxs-lookup"><span data-stu-id="e0a6c-128">Your application might hit various asserts when it exits.</span></span> <span data-ttu-id="e0a6c-129">您可以忽略這些錯誤。</span><span class="sxs-lookup"><span data-stu-id="e0a6c-129">You can ignore these.</span></span>

 

<span data-ttu-id="e0a6c-130">下圖顯示 [ **連接到圖形** ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="e0a6c-130">The following illustration shows the **Connect To Graph** dialog box.</span></span>

![連接至圖形](images/gedit-spy.png)

<span data-ttu-id="e0a6c-132">當 GraphEdit 載入圖形時，它會在目標應用程式的內容中執行。</span><span class="sxs-lookup"><span data-stu-id="e0a6c-132">When GraphEdit loads the graph, it executes in the context of the target application.</span></span> <span data-ttu-id="e0a6c-133">因此，GraphEdit 可能會封鎖，因為它正在等候執行緒。</span><span class="sxs-lookup"><span data-stu-id="e0a6c-133">Therefore, GraphEdit might block because it is waiting for the thread.</span></span> <span data-ttu-id="e0a6c-134">例如，如果您在偵錯工具中逐步執行程式碼，就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="e0a6c-134">For example, this can occur if you are stepping through your code in the debugger.</span></span>

<span data-ttu-id="e0a6c-135">這項功能僅適用于應用程式的 debug 組建，而非零售組建，因為它可讓其他應用程式查看或控制篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="e0a6c-135">This feature should be used only in debug builds of your application, not retail builds, because it enables other applications to view or control the filter graph.</span></span>

## <a name="connecting-to-a-remote-graph-from-the-command-line"></a><span data-ttu-id="e0a6c-136">從命令列連接至遠端圖形</span><span class="sxs-lookup"><span data-stu-id="e0a6c-136">Connecting to a Remote Graph from the Command Line</span></span>

<span data-ttu-id="e0a6c-137">GraphEdit 支援命令列選項，可在啟動時自動載入遠端圖形。</span><span class="sxs-lookup"><span data-stu-id="e0a6c-137">GraphEdit supports a command-line option to load a remote graph automatically on startup.</span></span> <span data-ttu-id="e0a6c-138">語法為：</span><span class="sxs-lookup"><span data-stu-id="e0a6c-138">The syntax is:</span></span>


```C++
GraphEdt -a moniker
```



<span data-ttu-id="e0a6c-139">其中的 *名字* 標記是使用 AddToRot 函式建立的標記，如先前所述。</span><span class="sxs-lookup"><span data-stu-id="e0a6c-139">where *moniker* is a moniker created using the AddToRot function, described previously.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e0a6c-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="e0a6c-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0a6c-141">使用 GraphEdit 模擬圖表建立</span><span class="sxs-lookup"><span data-stu-id="e0a6c-141">Simulating Graph Building with GraphEdit</span></span>](simulating-graph-building-with-graphedit.md)
</dt> </dl>

 

 



