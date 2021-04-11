---
title: 適用于更佳介面和方法設計的 IDL 技術
description: 當您開發的 RPC 介面和方法都能處理一致和變化的資料時，請考慮使用下列 IDL 特定技術來改善安全性和效能。
ms.assetid: 651bdb5c-ad56-4526-9b7d-7165141e7ceb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b897d8d1f2f5e1c11a5328fb095341871e3689e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372109"
---
# <a name="idl-techniques-for-better-interface-and-method-design"></a><span data-ttu-id="160f7-103">適用于更佳介面和方法設計的 IDL 技術</span><span class="sxs-lookup"><span data-stu-id="160f7-103">IDL Techniques for Better Interface and Method Design</span></span>

<span data-ttu-id="160f7-104">當您開發的 RPC 介面和方法都能處理一致和變化的資料時，請考慮使用下列 IDL 特定技術來改善安全性和效能。</span><span class="sxs-lookup"><span data-stu-id="160f7-104">Consider using the following IDL-specific techniques to improve security and performance when you are developing RPC interfaces and methods that handle both conformant and variant data.</span></span> <span data-ttu-id="160f7-105">本主題所參考的屬性是在方法參數上設定的 IDL 屬性，這些屬性會處理一致的資料 (例如， \[ **大小 \_ 為**， \] 而 \[ **最大值 \_ 為** \] 屬性) 或 variant 資料 (例如， \[ **長度 \_ 為**， \]) 為 \[ **字串** \] 屬性。</span><span class="sxs-lookup"><span data-stu-id="160f7-105">The attributes referred to in this topic are the IDL attributes set on method parameters that handle either conformant data (for example, the \[**size\_is**\] and \[**max\_is**\] attributes) or variant data (for example, the \[**length\_is**\] and \[**string**\] attributes).</span></span>

## <a name="using-the-range-attribute-with-conformant-data-parameters"></a><span data-ttu-id="160f7-106">使用 \[ \] 具有一致資料參數的範圍屬性</span><span class="sxs-lookup"><span data-stu-id="160f7-106">Using the \[range\] Attribute with Conformant Data Parameters</span></span>

<span data-ttu-id="160f7-107">\[**範圍** \] 屬性會指示 RPC 執行時間在資料封送處理常式期間執行額外的大小驗證。</span><span class="sxs-lookup"><span data-stu-id="160f7-107">The \[**range**\] attribute instructs the RPC run-time to perform additional size validation during the data unmarshaling process.</span></span> <span data-ttu-id="160f7-108">具體而言，它會驗證所提供的資料大小是否以關聯參數形式傳遞至指定的範圍內。</span><span class="sxs-lookup"><span data-stu-id="160f7-108">Specifically, it verifies that the supplied size of the data passed as the associated parameter is within the specified range.</span></span>

<span data-ttu-id="160f7-109">\[**範圍** \] 屬性不會影響電傳格式。</span><span class="sxs-lookup"><span data-stu-id="160f7-109">The \[**range**\] attribute does not affect wire format.</span></span>

<span data-ttu-id="160f7-110">如果網路上的值超出允許的範圍，RPC 將會擲回 RPC \_ x 無效系結 \_ \_ 或 rpc \_ x \_ 錯誤的 \_ 存根 \_ 資料例外狀況。</span><span class="sxs-lookup"><span data-stu-id="160f7-110">If the value on wire is outside of the allowed range, RPC will throw an RPC\_X\_INVALID\_BOUND or RPC\_X\_BAD\_STUB\_DATA exception.</span></span> <span data-ttu-id="160f7-111">這可提供額外層級的資料驗證，並且有助於防止常見的安全性錯誤，例如緩衝區溢位。</span><span class="sxs-lookup"><span data-stu-id="160f7-111">This provides an additional level of data validation, and can help prevent common security errors like buffer overruns.</span></span> <span data-ttu-id="160f7-112">同樣地，使用 \[ **範圍** \] 可以改善應用程式效能，因為以其標示的一致資料具有明確定義的條件約束，可供 RPC 服務考慮。</span><span class="sxs-lookup"><span data-stu-id="160f7-112">Likewise, using \[**range**\] can improve application performance, since conformant data marked with it has clearly-defined constraints available for consideration by the RPC service.</span></span>

## <a name="rpc-server-stub-memory-management-rules"></a><span data-ttu-id="160f7-113">RPC 伺服器 Stub 記憶體管理規則</span><span class="sxs-lookup"><span data-stu-id="160f7-113">RPC Server Stub Memory Management Rules</span></span>

<span data-ttu-id="160f7-114">針對啟用 RPC 的應用程式建立 IDL 檔案時，請務必瞭解 RPC 伺服器 stub 記憶體管理規則。</span><span class="sxs-lookup"><span data-stu-id="160f7-114">It is important to understand RPC server stub memory management rules when creating the IDL files for an RPC-enabled application.</span></span> <span data-ttu-id="160f7-115">應用程式可以使用與上述相符的資料搭配使用的範圍，來改善伺服器資源的使用方式，以及刻意 \[  \] 避免將可變長度的資料 IDL 屬性（例如 \[ **長度 \_** ）應用在 \] 符合標準的資料。</span><span class="sxs-lookup"><span data-stu-id="160f7-115">Applications can improve server resource utilization by using \[**range**\] in conjunction with conformant data as indicated above, as well as deliberately avoiding the application of variable-length data IDL attributes like like \[**length\_is**\] to conformant data.</span></span>

<span data-ttu-id="160f7-116">不建議將 \[ **長度 \_** 的應用程式 \] 設為 IDL 檔案中定義的資料結構欄位。</span><span class="sxs-lookup"><span data-stu-id="160f7-116">The application of \[**length\_is**\] to data structure fields defined in an IDL file is not recommended.</span></span>

## <a name="best-practices-for-variable-length-data-parameters"></a><span data-ttu-id="160f7-117">可變長度資料參數的最佳作法</span><span class="sxs-lookup"><span data-stu-id="160f7-117">Best Practices for Variable-length Data Parameters</span></span>

<span data-ttu-id="160f7-118">以下是針對可變大小的資料結構、方法參數和欄位定義 IDL 屬性時，所要考慮的幾個最佳作法。</span><span class="sxs-lookup"><span data-stu-id="160f7-118">The following are several best practices to consider when defining the IDL attributes for variable-sized data structures, method parameters and fields.</span></span>

-   <span data-ttu-id="160f7-119">使用早期關聯性。</span><span class="sxs-lookup"><span data-stu-id="160f7-119">Use early correlation.</span></span> <span data-ttu-id="160f7-120">通常最好是定義變數大小參數或欄位，使其在控制整數型別之後立即發生。</span><span class="sxs-lookup"><span data-stu-id="160f7-120">It is generally better to define the variable size parameter or field such that it occurs immediately after the controlling integral type.</span></span>

    <span data-ttu-id="160f7-121">例如，</span><span class="sxs-lookup"><span data-stu-id="160f7-121">For example,</span></span>

    ``` syntax
    earlyCorr
    (
    [in, range(MIN_COUNT, MAX_COUNT)] long size, 
    [in,size_is(size)] char *pv
    );
    ```

    <span data-ttu-id="160f7-122">勝過</span><span class="sxs-lookup"><span data-stu-id="160f7-122">is better than</span></span>

    ``` syntax
    lateCorr
    (
    [in,size_is(size)] char *pv, 
    [in, range(MIN_COUNT, MAX_COUNT)] long size)
    );
    ```

    <span data-ttu-id="160f7-123">其中 **earlyCorr** 會在可變長度資料參數的正後方宣告 size 參數，而 **lateCorr** 會在它之後宣告 size 參數。</span><span class="sxs-lookup"><span data-stu-id="160f7-123">wherein **earlyCorr** declares the size parameter immediately before the variable-length data parameter, and **lateCorr** declares the size parameter after it.</span></span> <span data-ttu-id="160f7-124">使用早期對應可改善整體效能，特別是在經常呼叫方法的情況下。</span><span class="sxs-lookup"><span data-stu-id="160f7-124">Using early correspondence improves performance overall, especially in cases where the method is called frequently.</span></span>

-   <span data-ttu-id="160f7-125">針對標記為 out 的參數 \[ **，大小 \_ 為** \] 屬性元組，而且在用戶端上或用戶端具有合理上限的情況下，方法定義在參數屬性和順序方面應該類似下列內容：</span><span class="sxs-lookup"><span data-stu-id="160f7-125">For parameters marked with the \[**out, size\_is**\] attribute tuple, and where the data length is known on the client side or where the client has a reasonable upper bound, the method definition should be similar to the following in terms of parameter attribution and sequence:</span></span>

    ``` syntax
    outKnownSize
    (
    [in,range(MIN_COUNT, MAX_COUNT)] long lSize,
    [out,size_is(lSize)] UserDataType * pArr
    );
    ```

    <span data-ttu-id="160f7-126">在此情況下，用戶端會針對 *pArr* 提供固定大小的緩衝區，讓伺服器端 RPC 服務能夠以良好的保證配置合理大小的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="160f7-126">In this case, the client provides a fixed size buffer for *pArr*, allowing the server-side RPC service to allocate a reasonably-sized buffer with a good degree of assurance.</span></span> <span data-ttu-id="160f7-127">請注意，在此範例中，資料是從伺服器收到 \[ **(的** \]) 。</span><span class="sxs-lookup"><span data-stu-id="160f7-127">Note that in the example the data is received from the server (\[**out**\]).</span></span> <span data-ttu-id="160f7-128">在 \[) **中** 傳遞給伺服器 (的資料定義類似 \] 。</span><span class="sxs-lookup"><span data-stu-id="160f7-128">The definition is similar for data passed to the server (\[**in**\]).</span></span>

-   <span data-ttu-id="160f7-129">在 RPC 應用程式的伺服器端元件決定資料長度的情況下，方法定義應該如下所示：</span><span class="sxs-lookup"><span data-stu-id="160f7-129">For situations where the server-side component of an RPC application decides the data length, the method definition should be similar to the following:</span></span>

    ``` syntax
    typedef [range(MIN_COUNT,MAX_COUNT)] long RANGED_LONG;

    outUnknownSize
    (
    [out] RANGED_LONG *pSize,
    [out,size_is(,*pSize)] UserDataType **ppArr
    );
    ```

    <span data-ttu-id="160f7-130">**範圍 \_LONG** 是定義給用戶端和伺服器存根的型別，以及指定的大小，用戶端可以正確預測。</span><span class="sxs-lookup"><span data-stu-id="160f7-130">**RANGED\_LONG** is a type defined for both the client and server stubs, and of a specified size the client can correctly anticipate.</span></span> <span data-ttu-id="160f7-131">在此範例中，用戶端會將 *ppArr* 傳遞為 **Null**，而且 RPC 伺服器應用程式元件會配置正確的記憶體量。</span><span class="sxs-lookup"><span data-stu-id="160f7-131">In the example, the client passes *ppArr* as **NULL**, and the RPC server application component allocates the correct amount of memory.</span></span> <span data-ttu-id="160f7-132">傳回時，用戶端上的 RPC 服務會為傳回的資料配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="160f7-132">Upon return, the RPC service on the client side allocates the memory for the returned data.</span></span>

-   <span data-ttu-id="160f7-133">如果用戶端想要將大型符合標準的陣列子集傳送至伺服器，應用程式可以指定子集的大小，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="160f7-133">If the client wants to send a subset of a large conformant array to the server, the application can specify the size of the subset as demonstrated in the following example:</span></span>

    ``` syntax
    inConformantVaryingArray
    (
    [in,range(MIN_COUNT,MAX_COUNT)] long lSize,
    [in] long lLength, 
    [in,size_is(lSize), length_is(lLength)] UserDataType *pArr
    );
    ```

    <span data-ttu-id="160f7-134">如此一來，RPC 就只會在網路上傳輸陣列的 *lLength* 元素。</span><span class="sxs-lookup"><span data-stu-id="160f7-134">This way RPC will only transmit *lLength* elements of the array across the wire.</span></span> <span data-ttu-id="160f7-135">不過，此定義會強制 RPC 服務在伺服器端配置 *lSize* 大小的記憶體。</span><span class="sxs-lookup"><span data-stu-id="160f7-135">However, this definition forces the RPC service to allocate memory of size *lSize* on the server side.</span></span>

-   <span data-ttu-id="160f7-136">如果用戶端應用程式元件判斷伺服器可以傳回的陣列大小上限，但允許伺服器傳送該陣列的子集，則應用程式可以藉由定義 IDL 來指定這類行為，如下例所示：</span><span class="sxs-lookup"><span data-stu-id="160f7-136">If the client application component determines the maximum size of an array the server can return, but allows the server to transmit a subset of that array, the application can specify such a behavior by defining the IDL similar to the following example:</span></span>

    ``` syntax
    inMaxSizeOutLength
    (
    [in, range(MIN_COUNT, MAX_COUNT)] long lSize,
    [out] long *pLength,
    [out,size_is(lSize), length_is(*pLength)] UserDataType *pArr
    );
    ```

    <span data-ttu-id="160f7-137">用戶端應用程式元件會指定陣列的大小上限，而伺服器會指定傳回用戶端的元素數目。</span><span class="sxs-lookup"><span data-stu-id="160f7-137">The client application component specifies the maximum size of the array, and the server specifies how many elements it transmits back to the client.</span></span>

-   <span data-ttu-id="160f7-138">如果伺服器應用程式元件需要將字串傳回給用戶端應用程式元件，而且如果用戶端知道要從伺服器傳回的大小上限，則應用程式可以使用符合標準的字串類型，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="160f7-138">If the server application component needs to return a string to the client application component, and if the client knows the maximum size to be returned from the server, the application can use a conformant string type as demonstrated in the following example:</span></span>

    ``` syntax
    outStringKnownSize
    (
    [in,range(MIN_COUNT, MAX_STRING)] long lSize,
    [out,size_is(lSize),string] wchar_t *pString
    );
    ```

-   <span data-ttu-id="160f7-139">如果用戶端應用程式元件不應控制字元串的大小，則 RPC 服務可以特別配置記憶體，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="160f7-139">If the client application component should not control the size of the string, the RPC service can specifically allocate the memory as demonstrated in the following example:</span></span>

    ``` syntax
    outStringUnknownSize
    (
    [out] LPWSTR *ppStr
    );
    ```

    <span data-ttu-id="160f7-140">呼叫 RPC 方法時，用戶端應用程式元件必須將 *ppStr* 設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="160f7-140">The client application component must set *ppStr* to **NULL** on when calling the RPC method.</span></span>

 

 




