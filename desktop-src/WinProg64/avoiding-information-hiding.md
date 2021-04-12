---
title: 避免資訊隱藏
description: 有時候，程式會刻意或不慎隱藏 RPC 封送處理引擎的資訊。
ms.assetid: 016b9221-092d-4c25-a396-4f41dcdfb3cf
keywords:
- 回溯相容性64位 Windows 程式設計
- 相容性問題 64-位 Windows 程式設計
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f4b9e4ba7ed5165378beb93005243af03f9e469
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375840"
---
# <a name="avoiding-information-hiding"></a><span data-ttu-id="421c1-105">避免資訊隱藏</span><span class="sxs-lookup"><span data-stu-id="421c1-105">Avoiding Information Hiding</span></span>

<span data-ttu-id="421c1-106">有時候，程式會刻意或不慎隱藏 RPC 封送處理引擎的資訊。</span><span class="sxs-lookup"><span data-stu-id="421c1-106">Occasionally, programs deliberately or inadvertently hide information from the RPC marshaling engine.</span></span> <span data-ttu-id="421c1-107">部分範例如下：</span><span class="sxs-lookup"><span data-stu-id="421c1-107">Some examples are as follows:</span></span>

-   <span data-ttu-id="421c1-108">以位元組的無差異區塊形式傳送資料結構</span><span class="sxs-lookup"><span data-stu-id="421c1-108">Sending a data structure as an undifferentiated block of bytes</span></span>
-   <span data-ttu-id="421c1-109">利用方法中的副作用，在網路上透過通道傳送額外資料來利用效能</span><span class="sxs-lookup"><span data-stu-id="421c1-109">Leveraging performance by using a side effect from a method to channel additional data across the wire</span></span>
-   <span data-ttu-id="421c1-110">嘗試以 **DWORD** 或 **ULONG** 的形式傳遞控制碼來進行偽裝</span><span class="sxs-lookup"><span data-stu-id="421c1-110">Attempting to disguise a handle by passing it as a **DWORD** or a **ULONG**</span></span>

<span data-ttu-id="421c1-111">這些技術幾乎保證會在您將應用程式移植到64位 Windows 之前引進相容性問題。</span><span class="sxs-lookup"><span data-stu-id="421c1-111">These techniques are almost guaranteed to introduce compatibility problems even before you port your application to 64-bit Windows.</span></span>

<span data-ttu-id="421c1-112">您可以使用內容控制碼，為代表用戶端的伺服器內容提供不透明的控制碼，而不是在標準遠端程序呼叫中傳送伺服器內容做為 **DWORD** 。</span><span class="sxs-lookup"><span data-stu-id="421c1-112">Instead of sending a server context as a **DWORD** in a standard remote procedure call, use a context handle to provide an opaque handle to a server context that is held on behalf of a client.</span></span> <span data-ttu-id="421c1-113">當伺服器建立用戶端的內容控制碼時，由 RPC 執行時間所定義的 Guid 會識別內容。</span><span class="sxs-lookup"><span data-stu-id="421c1-113">Contexts are identified by GUIDs defined by the RPC run time when a server creates a context handle for a client.</span></span> <span data-ttu-id="421c1-114">不透過網路使用指標，且在32或64位界限之間的作業完全透明。</span><span class="sxs-lookup"><span data-stu-id="421c1-114">No pointer is used over the wire and the operation is completely transparent across 32- or 64-bit boundaries.</span></span> <span data-ttu-id="421c1-115">如需使用內容控制碼的詳細資訊，請參閱 [內容控制碼](/windows/desktop/Rpc/context-handles)。</span><span class="sxs-lookup"><span data-stu-id="421c1-115">For more information on using context handles, see [Context Handles](/windows/desktop/Rpc/context-handles).</span></span>

<span data-ttu-id="421c1-116">DCOM 介面無法使用內容控制碼，因為 COM 會提供自己的內容管理。</span><span class="sxs-lookup"><span data-stu-id="421c1-116">DCOM interfaces cannot use context handles because COM provides its own context management.</span></span> <span data-ttu-id="421c1-117">您可以將介面指標傳遞給 COM 物件，而不是建立內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="421c1-117">Instead of creating a context handle, you can pass an interface pointer to the COM object.</span></span> <span data-ttu-id="421c1-118">然後，您可以直接透過介面指標呼叫方法，或將指標放在其他呼叫中。</span><span class="sxs-lookup"><span data-stu-id="421c1-118">Then you can call the methods directly through the interface pointer or place the pointer inside other calls.</span></span> <span data-ttu-id="421c1-119">若要釋放伺服器物件，用戶端會透過介面指標呼叫介面的 **發行** 方法。</span><span class="sxs-lookup"><span data-stu-id="421c1-119">To release the server object, the client calls the interface's **Release** method through the interface pointer.</span></span>

<span data-ttu-id="421c1-120">同樣地，有時候您可能無法變更正在移植之程式碼的原始設計。</span><span class="sxs-lookup"><span data-stu-id="421c1-120">Again, there may be times when you cannot change the original design of the code that you are porting.</span></span> <span data-ttu-id="421c1-121">如果無法避免將指標以 **dword** 的形式傳送到網路上，您就必須在 **dword** 值和指標之間執行某種形式的伺服器端對應。</span><span class="sxs-lookup"><span data-stu-id="421c1-121">If there is no way to avoid sending a pointer across the wire as a **DWORD**, you will have to implement some form of server-side mapping between **DWORD** values and pointers.</span></span> <span data-ttu-id="421c1-122">其中一種方式是將用戶端應用程式中的指標變更為指標精確度類型，例如 **ULONG \_ Ptr** 或 **DWORD \_** 指標。</span><span class="sxs-lookup"><span data-stu-id="421c1-122">One way to do this is to change the pointers in the client side application to pointer-precision types, such as **ULONG\_PTR** or **DWORD\_PTR**.</span></span> <span data-ttu-id="421c1-123">然後使用 MIDL \[ [**呼叫 \_ 做為**](/windows/desktop/Midl/call-as) \] 屬性，將指標放在網路上作為 **DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="421c1-123">Then use the MIDL \[[**call\_as**](/windows/desktop/Midl/call-as)\] attribute to put the pointers on the wire as **DWORD** values.</span></span> <span data-ttu-id="421c1-124">用戶端包裝函式只需要一併傳遞引數。</span><span class="sxs-lookup"><span data-stu-id="421c1-124">The client-side wrapper need only pass the arguments along.</span></span> <span data-ttu-id="421c1-125">伺服器端包裝函式會處理兩種類型之間的對應。</span><span class="sxs-lookup"><span data-stu-id="421c1-125">The server-side wrapper handles the mapping between both types.</span></span> <span data-ttu-id="421c1-126">以類似的方式，您可以使用 [ \[ [**傳輸 \_ 為**](/windows/desktop/Midl/transmit-as)] \] 屬性或 [ \[ [**表示 \_ 為**](/windows/desktop/Midl/represent-as)] 屬性，將 \] 您的資料轉換成與與舊版相容的線路表示格式。</span><span class="sxs-lookup"><span data-stu-id="421c1-126">In a similar way, you can use either the \[[**transmit\_as**](/windows/desktop/Midl/transmit-as)\] attribute or the \[[**represent\_as**](/windows/desktop/Midl/represent-as)\] attribute to convert your data to a backward-compatible format for wire representation.</span></span>

<span data-ttu-id="421c1-127">如果回溯相容性不是問題，或控制碼不是用於遠端呼叫，而您確定 32-和64位進程之間的遠端呼叫永遠不會發生，您可以將引數重新定義為 **ULONG64**。</span><span class="sxs-lookup"><span data-stu-id="421c1-127">If backward-wire compatibility is not an issue or if the handle is not used for remote calls and you are sure that remote calls between 32- and 64-bit processes will never happen, you can redefine an argument as a **ULONG64**.</span></span> <span data-ttu-id="421c1-128">如有必要，您可以修改32位應用程式，以將 **DWORD** 傳遞給使用者。</span><span class="sxs-lookup"><span data-stu-id="421c1-128">If necessary, you can modify the 32-bit application to pass a **DWORD** to the user.</span></span> <span data-ttu-id="421c1-129">或者，您可以使用32位 Windows 上的 **DWORD** 和64位 windows 上的 **ULONG64** ，在每個平臺的個別 IDL 檔案中建立個別的存根。</span><span class="sxs-lookup"><span data-stu-id="421c1-129">Alternatively, you can build separate stubs from separate IDL files for each platform using a **DWORD** on 32-bit Windows and a **ULONG64** on 64-bit Windows.</span></span>

 

 