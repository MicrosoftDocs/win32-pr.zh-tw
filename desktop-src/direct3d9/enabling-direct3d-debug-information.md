---
description: 您是否想要在 debug 期間找出有關 Direct3D 物件的詳細資訊？ 例如，下列螢幕擷取畫面顯示當您在 [監看式] 視窗中查看 Direct3D 介面時，通常會看到的內容。
ms.assetid: 365451f8-e93e-4cc4-b688-2e668518c245
title: " (Direct3D 9) 啟用 Direct3D 調試資訊"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17bb46cf8658d0417d021faa6bdbefd10822d1dd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108404"
---
# <a name="enabling-direct3d-debug-information-direct3d-9"></a><span data-ttu-id="9e451-104"> (Direct3D 9) 啟用 Direct3D 調試資訊</span><span class="sxs-lookup"><span data-stu-id="9e451-104">Enabling Direct3D Debug Information (Direct3D 9)</span></span>

<span data-ttu-id="9e451-105">您是否想要在 debug 期間找出有關 Direct3D 物件的詳細資訊？</span><span class="sxs-lookup"><span data-stu-id="9e451-105">Are you trying to find out more information about Direct3D objects during debug?</span></span> <span data-ttu-id="9e451-106">例如，下列螢幕擷取畫面顯示當您在 [監看式] 視窗中查看 Direct3D 介面時，通常會看到的內容。</span><span class="sxs-lookup"><span data-stu-id="9e451-106">For instance, the following screen shot shows what you typically see when you look at a Direct3D interface in the watch window.</span></span>

![[監看式] 視窗中的 direct3d 介面螢幕擷取畫面](images/d3d-debug-info1.png)

<span data-ttu-id="9e451-108">您可以啟用核心 debug 物件，以便在 [監看式] 視窗中，可以看到包含物件之所有屬性的鏡像物件。</span><span class="sxs-lookup"><span data-stu-id="9e451-108">You can enable the core debug objects so that a mirrored object which contains all of the properties of the object can be viewed in the watch window.</span></span> <span data-ttu-id="9e451-109">在 \# D3D9 .h 檔案之前的程式碼中，只需包含下列定義：</span><span class="sxs-lookup"><span data-stu-id="9e451-109">Simply include the following \#define in your code before the D3D9.h file:</span></span>


```
#define D3D_DEBUG_INFO
```



<span data-ttu-id="9e451-110">若要啟用 debug 資訊， \# 必須在 D3D9 .h 檔案之前建立定義， (任何使用 DXUT 的程式，在 \_ \_ 編譯器以進行 debug) 時，會自動啟用 D3D debug 資訊。</span><span class="sxs-lookup"><span data-stu-id="9e451-110">To enable debug information, the \#define must get built before the D3D9.h file (Any program using DXUT will automatically enable D3D\_DEBUG\_INFO when the program is compiled for debug).</span></span> <span data-ttu-id="9e451-111">如果您執行的是 SDK 範例，您可以在 DXStdAfx 中看到此 (，這會影響所有) 的 c + + 範例。</span><span class="sxs-lookup"><span data-stu-id="9e451-111">If you are running a SDK sample, you can see this in DXStdAfx.h (which affects all the C++ samples).</span></span> <span data-ttu-id="9e451-112">您也必須執行 debug Direct3D 執行時間 (如果必要) ，可以從主控台啟用。</span><span class="sxs-lookup"><span data-stu-id="9e451-112">You must also be running the debug Direct3D runtime (which can be enabled from the Control Panel if necessary).</span></span>

<span data-ttu-id="9e451-113">以下是使用 [BasicHLSL 範例](https://msdn.microsoft.com/library/Ee416223(v=VS.85).aspx)的範例。</span><span class="sxs-lookup"><span data-stu-id="9e451-113">Here's an example using the [BasicHLSL Sample](https://msdn.microsoft.com/library/Ee416223(v=VS.85).aspx).</span></span>

1.  <span data-ttu-id="9e451-114">在 \# 37 行之前，將定義新增至 Dxstdafx .h 檔案。</span><span class="sxs-lookup"><span data-stu-id="9e451-114">Add the \#define to the Dxstdafx.h file before line 37.</span></span>
2.  <span data-ttu-id="9e451-115">建立 debug 專案。</span><span class="sxs-lookup"><span data-stu-id="9e451-115">Build a debug project.</span></span>
3.  <span data-ttu-id="9e451-116">在 BasicHLSL 的第307行設定中斷點</span><span class="sxs-lookup"><span data-stu-id="9e451-116">Set a breakpoint at line 307 in BasicHLSL.cpp</span></span>
4.  <span data-ttu-id="9e451-117">執行偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="9e451-117">Run the debugger.</span></span>

<span data-ttu-id="9e451-118">下列螢幕擷取畫面顯示您可以從 [監看式] 視窗取得 Direct3D 材質物件的詳細資訊類型。</span><span class="sxs-lookup"><span data-stu-id="9e451-118">The following screen shot shows the kind of detailed information you can get about a Direct3D texture object from the watch window.</span></span>

![[監看式] 視窗中 direct3d 材質物件的螢幕擷取畫面](images/d3d-debug-info2.png)

> [!Note]
>
> <span data-ttu-id="9e451-120">物件屬性名稱是可見的，只有在啟用偵錯工具執行時間時，這些值才是正確的。</span><span class="sxs-lookup"><span data-stu-id="9e451-120">The object property names are visible and the values are correct only when the debug runtime is enabled.</span></span> <span data-ttu-id="9e451-121">針對零售版執行時間執行時，值無效。</span><span class="sxs-lookup"><span data-stu-id="9e451-121">When running against the retail runtime, the values are invalid.</span></span>

 

## <a name="use-the-call-stack-for-extended-debug"></a><span data-ttu-id="9e451-122">使用呼叫堆疊進行擴充的偵錯工具</span><span class="sxs-lookup"><span data-stu-id="9e451-122">Use the Call Stack for Extended Debug</span></span>

<span data-ttu-id="9e451-123">啟用 Direct3D debug 之後，您也可以在每次建立物件時查看呼叫堆疊。</span><span class="sxs-lookup"><span data-stu-id="9e451-123">With Direct3D debug enabled, you can also look at a call stack each time an object is created.</span></span> <span data-ttu-id="9e451-124">這會讓您的應用程式變得非常緩慢，但是可以用來檢查資源流失。</span><span class="sxs-lookup"><span data-stu-id="9e451-124">This will make your application very slow, but can be used to check for resource leaks.</span></span> <span data-ttu-id="9e451-125">若要寫出呼叫堆疊，請將下列登錄機碼設定為1：</span><span class="sxs-lookup"><span data-stu-id="9e451-125">To write out the call stack, set the following registry key to 1:</span></span>


```
\\HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\Direct3D\\
D3D9Debugging\\EnableCreationStack
```



<span data-ttu-id="9e451-126">使用啟用偵錯工具建立您的應用程式，可讓您存取這個額外的變數：</span><span class="sxs-lookup"><span data-stu-id="9e451-126">Building your application with debug enabled will give you access to this additional variable:</span></span>


```
  LPCWSTR CreationCallStack;
```



<span data-ttu-id="9e451-127">此變數會在每次建立物件時儲存呼叫堆疊。</span><span class="sxs-lookup"><span data-stu-id="9e451-127">This variable will store the call stack each time that an object is created.</span></span> <span data-ttu-id="9e451-128">這會讓您的應用程式變得非常緩慢，但是可以用來偵測資源流失。</span><span class="sxs-lookup"><span data-stu-id="9e451-128">This will make your application very slow, but can be used to debug resource leaks.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9e451-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="9e451-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e451-130">程式設計秘訣</span><span class="sxs-lookup"><span data-stu-id="9e451-130">Programming Tips</span></span>](programming-tips.md)
</dt> </dl>

 

 



