---
title: 使用內容控制碼進行介面開發
description: 一般而言，您會在 \_ IDL 檔案中的類型定義上指定 \ 內容控制碼 \ 屬性，以建立內容控制碼。
ms.assetid: e4caf91f-f92d-4aef-a20f-0a3073230640
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8474d533b27ba1543a9d522dfa4478d306b33cf2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682860"
---
# <a name="interface-development-using-context-handles"></a><span data-ttu-id="95e60-103">使用內容控制碼進行介面開發</span><span class="sxs-lookup"><span data-stu-id="95e60-103">Interface Development Using Context Handles</span></span>

<span data-ttu-id="95e60-104">一般而言，您會在 \[ IDL 檔案中的類型定義上指定 [**內容 \_ 控制碼**](/windows/desktop/Midl/context-handle)屬性，藉以建立內容控制碼 \] 。</span><span class="sxs-lookup"><span data-stu-id="95e60-104">Typically, you create a context handle by specifying the \[[**context\_handle**](/windows/desktop/Midl/context-handle)\] attribute on a type definition in the IDL file.</span></span> <span data-ttu-id="95e60-105">型別定義也會隱含地指定必須提供的內容執行常式。</span><span class="sxs-lookup"><span data-stu-id="95e60-105">The type definition also implicitly specifies a context run-down routine, which you must provide.</span></span> <span data-ttu-id="95e60-106">如果用戶端與伺服器之間的通訊中斷，伺服器執行時間會叫用此常式來執行任何所需的清除。</span><span class="sxs-lookup"><span data-stu-id="95e60-106">If communication between the client and server breaks down, the server run time invokes this routine to perform any needed cleanup.</span></span> <span data-ttu-id="95e60-107">如需內容執行程式的詳細資訊，請參閱 [伺服器內容運行時常式](server-context-run-down-routine.md)。</span><span class="sxs-lookup"><span data-stu-id="95e60-107">For more information on context run-down routines, see [Server Context Run-down Routine](server-context-run-down-routine.md).</span></span>

<span data-ttu-id="95e60-108">使用內容控制碼的介面必須具有初始系結的系結控制碼，而此控制碼必須在伺服器可以傳回內容控制碼之前發生。</span><span class="sxs-lookup"><span data-stu-id="95e60-108">An interface that uses a context handle must have a binding handle for the initial binding, which has to take place before the server can return a context handle.</span></span> <span data-ttu-id="95e60-109">您可以使用自動、隱含或明確的系結控制碼，建立系結並建立內容。</span><span class="sxs-lookup"><span data-stu-id="95e60-109">You can use an automatic, implicit, or explicit binding handle to create the binding and establish the context.</span></span>

<span data-ttu-id="95e60-110">內容控制碼必須是 [**void \***](/windows/desktop/Midl/void)型別，或是解析成 [**void \***](/windows/desktop/Midl/void)的型別。</span><span class="sxs-lookup"><span data-stu-id="95e60-110">A context handle must be of the [**void \***](/windows/desktop/Midl/void) type, or a type that resolves to [**void \***](/windows/desktop/Midl/void).</span></span> <span data-ttu-id="95e60-111">伺服器程式會將它轉換成所需的型別。</span><span class="sxs-lookup"><span data-stu-id="95e60-111">The server program casts it to the required type.</span></span>

> [!Note]  
> <span data-ttu-id="95e60-112">\[除非關閉內容控制碼的常式，否則不建議使用 [**in**](/windows/desktop/Midl/in)、 [**out**](/windows/desktop/Midl/out-idl) \] for coNtext handles 參數。</span><span class="sxs-lookup"><span data-stu-id="95e60-112">The use of \[[**in**](/windows/desktop/Midl/in), [**out**](/windows/desktop/Midl/out-idl)\] for context handle parameters is discouraged except for routines that close context handles.</span></span> <span data-ttu-id="95e60-113">如果內容處理標記 \[ [**在中**](/windows/desktop/Midl/in)的 [](/windows/desktop/Midl/out-idl)參數， \] 則會使用 out，請勿將 **Null** 或未初始化的內容控制碼從用戶端傳遞至伺服器。</span><span class="sxs-lookup"><span data-stu-id="95e60-113">If context handles parameters marked \[[**in**](/windows/desktop/Midl/in), [**out**](/windows/desktop/Midl/out-idl)\] are used, do not pass a **NULL** or uninitialized context handle from the client to the server.</span></span> <span data-ttu-id="95e60-114">應改為傳遞內容控制碼的 **Null** 指標。</span><span class="sxs-lookup"><span data-stu-id="95e60-114">A **NULL** pointer to a context handle should be passed instead.</span></span> <span data-ttu-id="95e60-115">請注意，在中標示的內容控制碼參數 \[ [](/windows/desktop/Midl/in) \] 不接受 **Null** 指標。</span><span class="sxs-lookup"><span data-stu-id="95e60-115">Please note, context handle parameters marked \[[**in**](/windows/desktop/Midl/in)\] do not accept **NULL** pointers.</span></span>

 

<span data-ttu-id="95e60-116">下列範例介面定義的片段會顯示分散式應用程式如何使用內容控制碼來開啟伺服器，並更新每個用戶端的資料檔案。</span><span class="sxs-lookup"><span data-stu-id="95e60-116">The following fragment of a sample interface definition shows how a distributed application can use a context handle to have a server open and update a data file for each client.</span></span>

<span data-ttu-id="95e60-117">介面必須包含用來初始化控制碼的遠端程序呼叫，並將它設定為非 **null** 值。</span><span class="sxs-lookup"><span data-stu-id="95e60-117">The interface must contain a remote procedure call to initialize the handle and set it to a non-**null** value.</span></span> <span data-ttu-id="95e60-118">在此範例中，RemoteOpen 函數會執行這項作業。</span><span class="sxs-lookup"><span data-stu-id="95e60-118">In this example, the RemoteOpen function performs this operation.</span></span> <span data-ttu-id="95e60-119">它會以 \[ [**out**](/windows/desktop/Midl/out-idl)方向屬性指定內容控制碼 \] 。</span><span class="sxs-lookup"><span data-stu-id="95e60-119">It specifies the context handle with an \[[**out**](/windows/desktop/Midl/out-idl)\] directional attribute.</span></span> <span data-ttu-id="95e60-120">或者，您可以將內容控制碼傳回為程式的傳回值。</span><span class="sxs-lookup"><span data-stu-id="95e60-120">Alternatively, you could return the context handle as the procedure's return value.</span></span> <span data-ttu-id="95e60-121">不過，在此範例中，我們會透過參數清單傳遞內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="95e60-121">However in this example, we'll pass the context handle out through the parameter list.</span></span>

<span data-ttu-id="95e60-122">在此範例中，內容資訊為檔案控制代碼。</span><span class="sxs-lookup"><span data-stu-id="95e60-122">In this example, the context information is a file handle.</span></span> <span data-ttu-id="95e60-123">它會持續追蹤檔案中的目前位置。</span><span class="sxs-lookup"><span data-stu-id="95e60-123">It keeps track of the current location in the file.</span></span> <span data-ttu-id="95e60-124">介面會將檔案控制代碼封裝為內容處理常式，並將它當作參數傳遞給遠端程序呼叫。</span><span class="sxs-lookup"><span data-stu-id="95e60-124">The interface packages the file handle as a context handle and passes it as a parameter to remote procedure calls.</span></span> <span data-ttu-id="95e60-125">結構包含檔案名和檔案控制代碼。</span><span class="sxs-lookup"><span data-stu-id="95e60-125">A structure contains the file name and the file handle.</span></span>

``` syntax
/* file: cxhndl.idl (fragment of interface definition file) */
typedef [context_handle] void * PCONTEXT_HANDLE_TYPE;
typedef [ref] PCONTEXT_HANDLE_TYPE * PPCONTEXT_HANDLE_TYPE;
 
short RemoteOpen([out] PPCONTEXT_HANDLE_TYPE pphContext,
    [in, string] unsigned char * pszFile);
 
void RemoteRead(
    [in] PCONTEXT_HANDLE_TYPE phContext,
    [out, size_is(cbBuf)] unsigned char achBuf[],
    [in, out] short *pcbBuf);
 
short RemoteClose([in, out] PPCONTEXT_HANDLE_TYPE pphContext);
```

<span data-ttu-id="95e60-126">RemoteOpen 函式會建立有效的非 **null** 內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="95e60-126">The RemoteOpen function creates a valid, non-**null** context handle.</span></span> <span data-ttu-id="95e60-127">它會將內容控制碼傳遞給用戶端。</span><span class="sxs-lookup"><span data-stu-id="95e60-127">It passes the context handle to the client.</span></span> <span data-ttu-id="95e60-128">後續的遠端程序呼叫（例如 RemoteRead）會使用內容控制碼做為 in 指標。</span><span class="sxs-lookup"><span data-stu-id="95e60-128">Subsequent remote procedure calls, such as RemoteRead, use the context handle as an in pointer.</span></span>

<span data-ttu-id="95e60-129">除了初始化內容控制碼的遠端程式之外，介面還必須包含釋放伺服器內容的程式，並將內容控制碼設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="95e60-129">In addition to the remote procedure that initializes the context handle, the interface must contain a procedure that frees the server context and sets context handle to **NULL**.</span></span> <span data-ttu-id="95e60-130">在上述範例中，RemoteClose 函數會執行這項作業。</span><span class="sxs-lookup"><span data-stu-id="95e60-130">In the preceding example, the RemoteClose function performs this operation.</span></span>

 

 