---
title: 伺服器 Stub 記憶體管理
description: 伺服器 Stub 記憶體管理
ms.assetid: 99e3ee56-5adb-4b25-bcf2-316d1bbdbdba
keywords:
- 伺服器 Stub 記憶體管理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6e052df6da999e5371ac498a1d39852b4be2b5e
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/08/2020
ms.locfileid: "103842827"
---
# <a name="server-stub-memory-management"></a><span data-ttu-id="d0e5a-104">伺服器 Stub 記憶體管理</span><span class="sxs-lookup"><span data-stu-id="d0e5a-104">Server Stub Memory Management</span></span>

## <a name="an-introduction-to-server-stub-memory-management"></a><span data-ttu-id="d0e5a-105">Server-Stub 記憶體管理簡介</span><span class="sxs-lookup"><span data-stu-id="d0e5a-105">An Introduction to Server-Stub Memory Management</span></span>

<span data-ttu-id="d0e5a-106">MIDL 產生的存根可作為用戶端進程與伺服器進程之間的介面。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-106">MIDL-generated stubs act as the interface between a client process and a server process.</span></span> <span data-ttu-id="d0e5a-107">用戶端 stub 會封送處理傳遞給以 [**\[ in \]**](../midl/in.md)屬性標記之參數的所有資料，並將它傳送至伺服器 stub。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-107">A client stub marshals all data passed to parameters marked with the [**\[in\]**](../midl/in.md) attribute, and sends it to the server stub.</span></span> <span data-ttu-id="d0e5a-108">伺服器 stub （接收此資料時）會重建呼叫堆疊，然後執行對應的使用者執行伺服器函數。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-108">The server stub, upon receiving this data, reconstructs the call stack, and then executes the corresponding user-implemented server function.</span></span> <span data-ttu-id="d0e5a-109">伺服器 stub 也會封送處理以 [**\[ out \]**](../midl/out-idl.md)屬性標記的參數資料，並將其傳回給用戶端應用程式。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-109">The server stub also marshals the parameter data marked with the [**\[out\]**](../midl/out-idl.md) attribute and returns it to the client application.</span></span>

<span data-ttu-id="d0e5a-110">MSRPC 使用的32位的封送處理資料格式，是 (NDR) 傳輸語法的網路資料表示的相容版本。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-110">The 32-bit marshaled data format used by MSRPC is a compliant version of the Network Data Representation (NDR) transfer syntax.</span></span> <span data-ttu-id="d0e5a-111">如需此格式的詳細資訊，請參閱 [Open Group 網站](https://www.opengroup.org/)。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-111">For more information about this format, see [The Open Group website](https://www.opengroup.org/).</span></span> <span data-ttu-id="d0e5a-112">針對64位平臺，可使用 Microsoft 64 位延伸模組（稱為 NDR64 的 NDR 傳輸語法）來提升效能。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-112">For 64-bit platforms, a Microsoft 64-bit extension to NDR transfer syntax called NDR64 can be used for better performance.</span></span>

## <a name="unmarshaling-inbound-data"></a><span data-ttu-id="d0e5a-113">封送輸入資料</span><span class="sxs-lookup"><span data-stu-id="d0e5a-113">Unmarshaling Inbound Data</span></span>

<span data-ttu-id="d0e5a-114">在 MSRPC 中，用戶端 stub 會將標記為 [**\[ 的 \]**](../midl/in.md)所有參數資料封送處理成一個連續緩衝區，以傳輸到伺服器 stub。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-114">In MSRPC, the client stub marshals all of the parameter data tagged as [**\[in\]**](../midl/in.md) in one continuous buffer for transmission to the server stub.</span></span> <span data-ttu-id="d0e5a-115">同樣地，伺服器存根會將以 [**\[ out \]**](../midl/out-idl.md)屬性標記的所有資料封送處理為傳回用戶端存根的連續緩衝區。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-115">Likewise, the server stub marshals all data marked with the [**\[out\]**](../midl/out-idl.md) attribute in a continuous buffer for return to the client stub.</span></span> <span data-ttu-id="d0e5a-116">雖然 RPC 底下的網路通訊協定層可以分割和 packetize 緩衝區以進行傳輸，但對 RPC 存根而言，片段是透明的。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-116">While the network protocol layer beneath RPC can fragment and packetize the buffer for transmission, the fragmentation is transparent to the RPC stubs.</span></span>

<span data-ttu-id="d0e5a-117">建立伺服器呼叫框架的記憶體配置可能是昂貴的作業。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-117">Memory allocation for creating the server call frame can be an expensive operation.</span></span> <span data-ttu-id="d0e5a-118">伺服器 stub 會盡可能將不必要的記憶體使用量降到最低，並假設伺服器常式不會釋放或重新配置標示為 [**\[ in \]**](../midl/in.md)或 **\[ in、out \]** 屬性的資料。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-118">The server stub will attempt to minimize unnecessary memory usage when possible, and it is assumed that the server routine will not free or reallocate data marked with the [**\[in\]**](../midl/in.md) or **\[in, out\]** attributes.</span></span> <span data-ttu-id="d0e5a-119">伺服器 stub 會嘗試盡可能重複使用緩衝區中的資料，以避免不必要的重複。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-119">The server stub attempts to reuse data in the buffer whenever possible to avoid unnecessary duplication.</span></span> <span data-ttu-id="d0e5a-120">一般規則是，如果封送處理的資料格式與記憶體格式相同，RPC 將會使用封送處理資料的指標，而不是針對相同的格式化資料配置額外的記憶體。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-120">The general rule is that if the marshaled data format is the same as the memory format, RPC will use pointers to the marshalled data instead of allocating additional memory for identically formatted data.</span></span>

<span data-ttu-id="d0e5a-121">例如，下列 RPC 呼叫的定義結構，其封送處理格式與記憶體內部格式相同。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-121">For example, the following RPC call is defined with a structure whose marshaled format is identical to its in-memory format.</span></span>

``` syntax
typedef struct RpcStructure
{
    long val;
    long val2;
}

void ProcessRpcStructure
(
    [in]  RpcStructure *plInStructure;
    [out] RpcStructure *plOutStructure;
);
```

<span data-ttu-id="d0e5a-122">在此情況下，RPC 不會為 *plInStructure* 所參考的資料配置額外的記憶體;相反地，它只會將已封送處理的資料指標傳遞至伺服器端函式的執行。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-122">In this case, RPC does not allocate additional memory for the data referenced by *plInStructure*; rather, it simply passes the pointer to the marshaled data to the server-side function implementation.</span></span> <span data-ttu-id="d0e5a-123">如果使用「-穩固」旗標來編譯存根，則 RPC 伺服器 stub 會在封送處理期間驗證緩衝區 (這是 MIDL 編譯器) 的 nmost 最新版本中的預設設定。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-123">The RPC server stub verifies the buffer during the unmarshaling process if the stub is compiled using the "-robust" flag (which is a default setting in the nmost recent version of the MIDL compiler).</span></span> <span data-ttu-id="d0e5a-124">RPC 保證傳遞至伺服器端函式的資料是有效的。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-124">RPC guarantees that the data passed to the server-side function implementation is valid.</span></span>

<span data-ttu-id="d0e5a-125">請注意，記憶體會配置給 *plOutStructure*，因為它不會將任何資料傳遞給伺服器。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-125">Be aware that memory is allocated for *plOutStructure*, since no data is passed to the server for it.</span></span>

## <a name="memory-allocation-for-inbound-data"></a><span data-ttu-id="d0e5a-126">輸入資料的記憶體配置</span><span class="sxs-lookup"><span data-stu-id="d0e5a-126">Memory Allocation for Inbound Data</span></span>

<span data-ttu-id="d0e5a-127">當伺服器 stub 針對標記為 [**\[ in \]**](../midl/in.md)或 **\[ in、out \]** 屬性的參數資料配置記憶體時，可能會發生案例。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-127">Cases can arise where the server stub allocates memory for parameter data marked with the [**\[in\]**](../midl/in.md) or **\[in, out\]** attributes.</span></span> <span data-ttu-id="d0e5a-128">當封送處理的資料格式與記憶體格式不同，或組成封送處理資料的結構相當複雜且必須由 RPC 伺服器 stub 以原子方式讀取時，就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-128">This occurs when the marshaled data format differs from the memory format, or when the structures that comprise the marshaled data are sufficient complex and must be read atomically by the RPC server stub.</span></span> <span data-ttu-id="d0e5a-129">以下是幾個常見的情況：必須配置記憶體給伺服器 stub 所收到的資料。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-129">Listed below are several common cases when memory must be allocated for data received by the server stub.</span></span>

-   <span data-ttu-id="d0e5a-130">資料是不同的陣列或一致的不同陣列。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-130">The data is a varying array or a conformant varying array.</span></span> <span data-ttu-id="d0e5a-131">這些是陣列 (或陣列指標) [**\[ 長度 \_ () \]**](../midl/length-is.md)或優先于其上設定 [**\[ \_ \] ()**](../midl/first-is.md)屬性的陣列。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-131">These are arrays (or pointers to arrays) that have the [**\[length\_is()\]**](../midl/length-is.md) or [**\[first\_is()\]**](../midl/first-is.md) attribute set on them.</span></span> <span data-ttu-id="d0e5a-132">在 NDR 中，只會封送處理和傳輸這些陣列的第一個元素。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-132">In NDR, only the first element of these arrays are marshaled and transmitted.</span></span> <span data-ttu-id="d0e5a-133">例如，在下列程式碼片段中，傳遞至參數的資料 *pv* 會配置給它的記憶體。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-133">For example, in the code snippet below, the data passed in the parameter *pv* will have memory allocated for it.</span></span>

    ``` syntax
    void RpcFunction
    (
        [in] long size,
        [in, out] long *pLength,
        [in, out, size_is(size), length_is(*pLength)] long *pv
    );
    ```

-   <span data-ttu-id="d0e5a-134">資料是大小字串或不符合標準的字串。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-134">The data is a sized string or non-conformant string.</span></span> <span data-ttu-id="d0e5a-135">這些字串通常是標記為的字元資料指標，其 [**\[ 大小 \_ 為 \] ()**](../midl/size-is.md)屬性。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-135">These strings are usually pointers to character data tagged with the [**\[size\_is()\]**](../midl/size-is.md) attribute.</span></span> <span data-ttu-id="d0e5a-136">在下列範例中，傳遞至 **SizedString** 伺服器端函式的字串會配置記憶體，而傳遞至 **NormalString** 函式的字串則會重複使用。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-136">In the example below, the string passed to the **SizedString** server-side function will have memory allocated, whereas the string passed to the **NormalString** function will be reused.</span></span>

    ``` syntax
    void SizedString
    (
        [in] long size,
        [in, size_is(size), string] char *str
    );

    void NormalString
    (
        [in, string] char str
    );
    ```

-   <span data-ttu-id="d0e5a-137">資料是一種簡單的類型，其記憶體大小與其經過封送處理的大小不同，例如 **enum16** 和 **\_ \_ int3264**。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-137">The data is a simple type whose memory size differs from its marshaled size, such as **enum16** and **\_\_int3264**.</span></span>
-   <span data-ttu-id="d0e5a-138">資料是由其記憶體對齊小於自然對齊的結構所定義、包含上述任何一種資料類型，或具有尾端的位元組填補。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-138">The data is defined by a structure whose memory alignment is smaller than the natural alignment, contains any of the above data types, or has trailing byte padding.</span></span> <span data-ttu-id="d0e5a-139">例如，下列複雜資料結構具有強制的2位元組對齊，並在結尾處有填補。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-139">For example, the following complex data structure has forced 2-byte alignment and has padding at the end.</span></span>

    ``` syntax
#pragma pack(2)
    typedef struct ComplexPackedStructure
    {
        char c;  
        long l;   // alignment is forced at the second byte
        char c2;  // there will be a trailing one-byte pad to keep 2-byte alignment
    }
    ```

-   <span data-ttu-id="d0e5a-140">資料包含必須依欄位封送處理欄位的結構。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-140">The data contains a structure that must be marshaled field by field.</span></span> <span data-ttu-id="d0e5a-141">這些欄位包含在 DCOM 介面中定義的介面指標;忽略的指標;使用 [**\[ 範圍 \]**](../midl/range.md)屬性設定的整數值; 陣列的元素，以連接 [**\[ \_ 封送 \]**](../midl/wire-marshal.md)處理、 [**\[ 使用者 \_ 封送 \]**](../midl/user-marshal.md)處理、 [**\[ 傳輸 \_ 為 \]**](../midl/transmit-as.md)和 [**\[ 表示 \_ 為 \]**](../midl/represent-as.md)屬性，以及內嵌複雜資料結構。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-141">These fields include interface pointers defined in DCOM interfaces; ignored pointers; integer values set with the [**\[range\]**](../midl/range.md) attribute; elements of arrays defined with the [**\[wire\_marshal\]**](../midl/wire-marshal.md), [**\[user\_marshal\]**](../midl/user-marshal.md), [**\[transmit\_as\]**](../midl/transmit-as.md) and [**\[represent\_as\]**](../midl/represent-as.md) attributes; and embedded complex data structures.</span></span>
-   <span data-ttu-id="d0e5a-142">資料包含聯集、包含聯集的結構，或等位陣列。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-142">The data contains a union, a structure containing a union, or an array of unions.</span></span> <span data-ttu-id="d0e5a-143">只會在網路上封送處理聯集的特定分支。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-143">Only the specific branch of the union is marshaled on the wire.</span></span>
-   <span data-ttu-id="d0e5a-144">資料包含具有多維度一致性陣列且至少有一個非固定維度的結構。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-144">The data contains a structure with a multidimensional conformant array that has at least one non-fixed dimension.</span></span>
-   <span data-ttu-id="d0e5a-145">資料包含複雜結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-145">The data contains an array of complex structures.</span></span>
-   <span data-ttu-id="d0e5a-146">資料包含單一資料型別（例如 **enum16** 和 **\_ \_ int3264**）的陣列。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-146">The data contains an array of simple data types such as **enum16** and **\_\_int3264**.</span></span>
-   <span data-ttu-id="d0e5a-147">資料包含 ref 和介面指標的陣列。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-147">The data contains an array of ref and interface pointers.</span></span>
-   <span data-ttu-id="d0e5a-148">資料有套用至指標的 [**\[ 強制 \_ 配置 \]**](../midl/force-allocate.md)屬性。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-148">The data has a [**\[force\_allocate\]**](../midl/force-allocate.md) attribute applied to a pointer.</span></span>
-   <span data-ttu-id="d0e5a-149">資料有一個 [**\[ 配置 (所有 \_ 節點 \]**](../midl/allocate.md)套用至指標的) 屬性。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-149">The data has a [**\[allocate(all\_nodes)\]**](../midl/allocate.md) attribute applied to a pointer.</span></span>
-   <span data-ttu-id="d0e5a-150">資料會將 [**\[ byte \_ count \]**](../midl/byte-count.md)屬性套用至指標。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-150">The data has a [**\[byte\_count\]**](../midl/byte-count.md) attribute applied to a pointer.</span></span>

## <a name="64-bit-data-and-ndr64-transfer-syntax"></a><span data-ttu-id="d0e5a-151">64位資料和 NDR64 傳輸語法</span><span class="sxs-lookup"><span data-stu-id="d0e5a-151">64-bit Data and NDR64 Transfer Syntax</span></span>

<span data-ttu-id="d0e5a-152">如先前所述，64位的資料會使用稱為 NDR64 的特定64位傳輸語法進行封送處理。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-152">As mentioned previously, 64-bit data is marshalled using a specific 64-bit transfer syntax called NDR64.</span></span> <span data-ttu-id="d0e5a-153">此傳輸語法的開發目的是要解決在32位的 NDR 下將指標封送處理，並傳輸至64位平臺上的伺服器 stub 時所發生的特定問題。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-153">This transfer syntax was developed to address the specific issue that arises when pointers are marshaled under 32-bit NDR and transmitted to a server-stub on a 64-bit platform.</span></span> <span data-ttu-id="d0e5a-154">在此情況下，封送處理的32位資料指標不符合64位，而且一定會發生記憶體配置。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-154">In this case, a marshaled 32-bit data pointer does not match a 64-bit one, and memory allocation will invariably occur.</span></span> <span data-ttu-id="d0e5a-155">為了在64位平臺上建立更一致的行為，Microsoft 開發了稱為 NDR64 的新傳輸語法。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-155">To create a more consistent behavior on 64-bit platforms, Microsoft developed a new transfer syntax called NDR64.</span></span>

<span data-ttu-id="d0e5a-156">說明此問題的範例如下所示：</span><span class="sxs-lookup"><span data-stu-id="d0e5a-156">An example illustrating this problem is as follows:</span></span>


```C++
typedef struct PtrStruct
{
  long l;
  long *pl;
}
```



<span data-ttu-id="d0e5a-157">當封送處理時，這個結構會由32位系統上的伺服器存根重複使用。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-157">This structure, when marshaled, will be reused by the server stub on a 32-bit system.</span></span> <span data-ttu-id="d0e5a-158">但是，如果伺服器 stub 位於64位系統上，則以 NDR 封送處理的資料長度為4個位元組，但所需的記憶體大小將會是8。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-158">However, if the server stub resides on a 64-bit system, the NDR-marshaled data is 4 bytes in length, but the required memory size will be 8.</span></span> <span data-ttu-id="d0e5a-159">如此一來，就會強制執行記憶體配置，而且很少會發生緩衝區重複使用。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-159">As a result, memory allocation is forced, and buffer reuse will rarely occur.</span></span> <span data-ttu-id="d0e5a-160">NDR64 藉由將指標的封送處理大小設為64位，來解決這個問題。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-160">NDR64 addresses this problem by making the marshaled size of a pointer 64-bit.</span></span>

<span data-ttu-id="d0e5a-161">相較于32位的 NDR，簡單的資料 tyes （例如 **enum16** 和 **\_ \_ int3264** ）不會在 NDR64 下使結構或陣列變得複雜。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-161">In contrast with 32-bit NDR, simple data tyes such as **enum16** and **\_\_int3264** do not make a structure or array complex under NDR64.</span></span> <span data-ttu-id="d0e5a-162">同樣地，尾端的填充值也不會讓結構變得複雜。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-162">Likewise, trailing pad values do not make a structure complex.</span></span> <span data-ttu-id="d0e5a-163">介面指標會被視為最上層的唯一指標;因此，包含介面指標的結構和陣列不會被視為複雜，也不需要特定的記憶體配置以供其使用。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-163">Interface pointers are treated as unique pointers at the top level; as a result, structures and arrays containing interface pointers are not considered complex and will not require specific memory allocation for their use.</span></span>

## <a name="initializing-outbound-data"></a><span data-ttu-id="d0e5a-164">正在初始化輸出資料</span><span class="sxs-lookup"><span data-stu-id="d0e5a-164">Initializing Outbound Data</span></span>

<span data-ttu-id="d0e5a-165">Unmarshalled 所有的輸入資料之後，伺服器 stub 需要初始化以 [**\[ out \]**](../midl/out-idl.md)屬性標記的輸出指標。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-165">After all of the inbound data has been unmarshalled, the server stub needs to initialize the outbound-only pointers marked with the [**\[out\]**](../midl/out-idl.md) attribute.</span></span>


```C++
typedef struct RpcStructure
{
    long val;
    long val2;
}

void ProcessRpcStructure
(
    [in]  RpcStructure *plInStructure;
    [out] RpcStructure *plOutStructure;
);
```



<span data-ttu-id="d0e5a-166">在上述呼叫中，伺服器 stub 必須將 *plOutStructure* 初始化，因為封送處理的資料中沒有它，而且它是必須提供給伺服器函數執行的隱含 [**\[ ref \]**](../midl/ref.md)指標。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-166">In the above call, the server stub must initialize *plOutStructure* because it was not present in the marshaled data, and it is an implied [**\[ref\]**](../midl/ref.md) pointer that must be made available to the server function implementation.</span></span> <span data-ttu-id="d0e5a-167">RPC 伺服器 stub 會初始化和零出具有 [**\[ out \]**](../midl/out-idl.md)屬性的最上層參考指標。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-167">The RPC server stub initializes and zeroes out any top-level reference-only pointers with the [**\[out\]**](../midl/out-idl.md) attribute.</span></span> <span data-ttu-id="d0e5a-168">它底下的任何 **\[ out \]** 參考指標也會以遞迴方式初始化。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-168">Any **\[out\]** reference pointers beneath it are recursively initialized as well.</span></span> <span data-ttu-id="d0e5a-169">遞迴會在其上設定 [**\[ unique \]**](../midl/unique.md)或 [**\[ ptr \]**](../midl/ptr.md)屬性的任何指標上停止。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-169">The recursion stops at any pointers with the [**\[unique\]**](../midl/unique.md) or [**\[ptr\]**](../midl/ptr.md) attributes set on them.</span></span>

<span data-ttu-id="d0e5a-170">伺服器函式的執行不能直接改變最上層的指標值，因此無法重新配置它們。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-170">The server function implementation cannot directly alter top-level pointer values, and thus cannot reallocate them.</span></span> <span data-ttu-id="d0e5a-171">例如，在上述 **ProcessRpcStructure** 的執行中，下列程式碼無效：</span><span class="sxs-lookup"><span data-stu-id="d0e5a-171">For example, in the implementation of **ProcessRpcStructure** above, the following code is invalid:</span></span>


```C++
void ProcessRpcStructure(RpcStructure *plInStructure, rpcStructure *plOutStructure)
{
    plOutStructure = MIDL_user_allocate(sizeof(RpcStructure));
    Process(plOutStructure);
}
```



<span data-ttu-id="d0e5a-172">*plOutStructure* 是堆疊值，且其變更不會傳播回 RPC。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-172">*plOutStructure* is a stack value and its change is not propagated back to RPC.</span></span> <span data-ttu-id="d0e5a-173">伺服器函式的執行可以嘗試釋放 *plOutStructure* 來避免配置，這可能會導致記憶體損毀。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-173">The server function implementation can attempt to avoid allocation by attempting to free *plOutStructure*, which may result in memory corruption.</span></span> <span data-ttu-id="d0e5a-174">然後，伺服器 stub 會在指標對指標的大小寫) 中，為最上層 (指標配置空間，而在堆疊上的大小為最上層的簡單結構，其大小會小於預期。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-174">The server stub will then allocate space for the top-level pointer in memory (in the pointer-to-pointer case) and a top-level simple structure whose size on the stack is smaller than expected.</span></span>

<span data-ttu-id="d0e5a-175">在特定情況下，用戶端可以指定伺服器端的記憶體配置大小。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-175">The client can, under certain circumstances, specify the memory allocation size of the server side.</span></span> <span data-ttu-id="d0e5a-176">在下列範例中，用戶端會在輸入 *大小* 參數中指定輸出資料的大小。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-176">In the following example, the client specifies the size of the outbound data in the inbound *size* parameter.</span></span>

``` syntax
void VariableSizeData
(
    [in] long size,
    [out, size_is(size)] char *pv
);
```

<span data-ttu-id="d0e5a-177">在 unmarshalling 輸入資料（包括 *大小*）後，伺服器 stub 會配置大小為 "sizeof (char) size" 的 *pv* 的緩衝區 \* 。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-177">After unmarshalling the inbound data, including *size*, the server stub allocates a buffer for *pv* with a size of "sizeof(char)\*size".</span></span> <span data-ttu-id="d0e5a-178">配置空間之後，伺服器存根會將緩衝區零出。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-178">After the space has been allocated, the server stub zeroes out the buffer.</span></span> <span data-ttu-id="d0e5a-179">請注意，在這個特殊情況下，存根會使用 **MIDL \_ 使用者 \_ 配置 () 配置** 記憶體，因為緩衝區的大小是在執行時間決定。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-179">Note that in this particular case, the stub allocates the memory with **MIDL\_user\_allocate()**, since the size of the buffer is determined at runtime.</span></span>

<span data-ttu-id="d0e5a-180">請注意，在 DCOM 介面的情況下，如果用戶端和伺服器共用相同的 COM 單元，或 **ICallFrame** 執行時，MIDL 產生的存根可能完全不會參與。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-180">Be aware that in the case of DCOM interfaces, MIDL-generated stubs may not be involved at all if the client and server share the same COM apartment, or if **ICallFrame** is implemented.</span></span> <span data-ttu-id="d0e5a-181">在此情況下，伺服器無法相依于配置行為，而且需要獨立確認用戶端大小的記憶體。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-181">In this case, the server cannot depend on the allocation behavior, and needs to independently verify client-sized memory.</span></span>

## <a name="server-side-function-implementations-and-outbound-data-marshaling"></a><span data-ttu-id="d0e5a-182">伺服器端函數執行和輸出資料封送處理</span><span class="sxs-lookup"><span data-stu-id="d0e5a-182">Server-side Function Implementations and Outbound Data Marshaling</span></span>

<span data-ttu-id="d0e5a-183">在輸入資料的 unmarshalling 和配置給包含輸出資料的記憶體初始化之後，RPC 伺服器 stub 會立即執行用戶端所呼叫之函式的伺服器端實作為。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-183">Immediately subsequent to the unmarshalling on inbound data and the initialization of the memory allocated to contain outbound data, the RPC server stub executes the server-side implementation of the function called by the client.</span></span> <span data-ttu-id="d0e5a-184">此時，伺服器可以修改特別標示 **\[ in、out \]** 屬性的資料，而且可以填入配置給輸出資料的記憶體 (標記為 [**\[ out \]**](../midl/out-idl.md)) 的資料。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-184">At this time, the server can modify the data specifically marked with the **\[in, out\]** attribute, and it can populate the memory allocated for outbound-only data (the data tagged with [**\[out\]**](../midl/out-idl.md)).</span></span>

<span data-ttu-id="d0e5a-185">處理已封送處理之參數資料的一般規則很簡單：伺服器只能配置新的記憶體，或修改由伺服器存根特別配置的記憶體。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-185">The general rules for the manipulation of marshalled parameter data are simple: the server can only allocate new memory or modify the memory specifically allocated by the server stub.</span></span> <span data-ttu-id="d0e5a-186">重新配置或釋放現有記憶體的資料可能會對函式呼叫的結果和效能造成負面影響，而且可能很難進行調試。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-186">Reallocating or releasing existing memory for data can have a negative impact on the results and performance of the function call, and can be very difficult to debug.</span></span>

<span data-ttu-id="d0e5a-187">邏輯上來說，RPC 伺服器與用戶端位於不同的位址空間，而且通常會假設它們不共用記憶體。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-187">Logically, the RPC server lives in a different address space than the client, and it can generally be assumed that they do not share memory.</span></span> <span data-ttu-id="d0e5a-188">如此一來，伺服器函式的執行就可以安全地使用以 [**\[ in \]**](../midl/in.md)屬性標示的資料做為「暫存」記憶體，而不會影響用戶端記憶體位址。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-188">As a result, it is safe for the server function implementation to use the data marked with the [**\[in\]**](../midl/in.md) attribute as "scratch" memory without affecting the client memory addresses.</span></span> <span data-ttu-id="d0e5a-189">話雖如此，伺服器應該不會嘗試重新配置或 **\[ 釋放 \] 資料**，而是將這些空間的控制權留給 RPC 伺服器 stub 本身。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-189">That said, the server should not attempt to reallocate or release **\[in\]** data, leaving the control of those spaces to the RPC server stub itself.</span></span>

<span data-ttu-id="d0e5a-190">一般來說，伺服器函式的執行不需要重新配置或釋放 **\[ 以 in、out \]** 屬性標記的資料。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-190">Generally, the server function implementation does not need to reallocate or release data marked with the **\[in, out\]** attribute.</span></span> <span data-ttu-id="d0e5a-191">針對固定大小的資料，函式執行邏輯可以直接修改資料。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-191">For fixed size data, the function implementation logic can directly modify the data.</span></span> <span data-ttu-id="d0e5a-192">同樣地，對於可變大小的資料，函式的執行不能修改提供給大小的域值 [**\[ \_ 是 \] ()**](../midl/size-is.md)屬性。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-192">Likewise, for variable-sized data, the function implementation must not modify the field value supplied to the [**\[size\_is()\]**](../midl/size-is.md) attribute, either.</span></span> <span data-ttu-id="d0e5a-193">變更用來將資料大小調整為較小或較大的緩衝區傳回給用戶端的域值，可能無法處理異常長度。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-193">Change the field value used to size the data results in a smaller or larger buffer returned to the client which may be ill-equipped to deal with the abnormal length.</span></span>

<span data-ttu-id="d0e5a-194">如果發生的情況是伺服器常式必須重新配置標示為 **\[ in、out \]** 屬性的資料所使用的記憶體，則伺服器端函式的執行方式可能不知道存根提供的指標是否為使用 **MIDL \_ 使用者 \_ 配置 ()** 或封送處理的網路緩衝區所配置的記憶體。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-194">If circumstances occur where the server routine has to reallocate the memory used by data marked with the **\[in, out\]** attribute, it is entirely possible that the server-side function implementation will not know if the pointer provided by the stub is to memory allocated with **MIDL\_user\_allocate()** or the marshaled wire buffer.</span></span> <span data-ttu-id="d0e5a-195">若要解決這個問題，MS RPC 可以確保在資料上設定 [**\[ force \_ allocate \]**](../midl/force-allocate.md)屬性時，不會發生記憶體遺漏或損毀。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-195">To work around this problem, MS RPC can ensure that no memory leak or corruption occurs if the [**\[force\_allocate\]**](../midl/force-allocate.md) attribute is set on the data.</span></span> <span data-ttu-id="d0e5a-196">設定 **\[ 強制 \_ 配置 \]** 時，伺服器 stub 一律會配置指標的記憶體，但要注意的是，每次使用時，效能會降低。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-196">When **\[force\_allocate\]** is set, the server stub will always allocate memory for the pointer, although the caveat is that performance will decrease for every use of it.</span></span>

<span data-ttu-id="d0e5a-197">當呼叫從伺服器端函式執行傳回時，伺服器存根會將標記為 [**\[ out \]**](../midl/out-idl.md)屬性的資料封送處理，並傳送至用戶端。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-197">When the call returns from the server-side function implementation, the server stub marshals the data marked with the [**\[out\]**](../midl/out-idl.md) attribute and sends it to the client.</span></span> <span data-ttu-id="d0e5a-198">請注意，如果伺服器端函數的執行擲回例外狀況，則存根不會封送處理資料。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-198">Be aware that the stub does not marshal the data if the server-side function implementation throws an exception.</span></span>

## <a name="releasing-allocated-memory"></a><span data-ttu-id="d0e5a-199">釋放配置的記憶體</span><span class="sxs-lookup"><span data-stu-id="d0e5a-199">Releasing Allocated Memory</span></span>

<span data-ttu-id="d0e5a-200">從伺服器端函式傳回呼叫之後，RPC 伺服器 stub 會釋放堆疊記憶體，不論是否發生例外狀況。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-200">The RPC server stub will release the stack memory after the call has returned from the server-side function, whether an exception occurs or not.</span></span> <span data-ttu-id="d0e5a-201">伺服器 stub 會釋放存根所配置的所有記憶體，以及任何使用 **MIDL \_ 使用者 \_ 配置 () 配置** 的記憶體。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-201">The server stub frees all memory allocated by the stub as well as any memory allocated with **MIDL\_user\_allocate()**.</span></span> <span data-ttu-id="d0e5a-202">伺服器端函式的執行必須一律讓 RPC 成為一致的狀態，方法是擲回例外狀況或傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-202">The server-side function implementation must always give RPC a consistent state, either by throwing an exception or returning an error code.</span></span> <span data-ttu-id="d0e5a-203">如果函式在擴展複雜的資料結構期間失敗，則必須確保所有指標都指向有效的資料，或設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-203">If the function fails during the population of complicated data structures, it must ensure that all pointers point to valid data or are set to **NULL**.</span></span>

<span data-ttu-id="d0e5a-204">在這個階段中，伺服器 stub 會釋出不屬於封送處理之緩衝區（包含 [**\[ in \]**](../midl/in.md)資料）的所有記憶體。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-204">During this pass, the server stub frees all memory that is not part of the marshaled buffer containing the [**\[in\]**](../midl/in.md) data.</span></span> <span data-ttu-id="d0e5a-205">這種行為的唯一例外狀況是具有 [**\[ 配置 (不 \_ \]**](../midl/allocate.md)會在其上設定) 屬性的資料-伺服器 stub 不會釋放與這些指標相關聯的任何記憶體。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-205">One exception to this behavior is data with the [**\[allocate(dont\_free)\]**](../midl/allocate.md) attribute set on them - the server stub does not free any memory associated with these pointers.</span></span>

<span data-ttu-id="d0e5a-206">在伺服器 stub 釋出 stub 和函式執行所配置的記憶體之後，如果特定資料指定了 [**\[ 通知 \_ 旗 \]**](../midl/notify-flag.md)標屬性，存根就會呼叫特定的通知函數。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-206">After the server stub releases the memory allocated by the stub and the function implementation, the stub calls a specific notification function if the [**\[notify\_flag\]**](../midl/notify-flag.md) attribute is specified for particular data.</span></span>

## <a name="marshalling-a-linked-list-over-rpc----an-example"></a><span data-ttu-id="d0e5a-207">透過 RPC 封送處理連結清單--範例</span><span class="sxs-lookup"><span data-stu-id="d0e5a-207">Marshalling a Linked List over RPC -- An Example</span></span>


```C++
typedef struct _LINKEDLIST
{
    long lSize;
    [size_is(lSize)] char *pData;
    struct _LINKEDLIST *pNext;
} LINKEDLIST, *PLINKEDLIST;

void Test
(
    [in] LINKEDLIST *pIn,
    [in, out] PLINKEDLIST *pInOut,
    [out] LINKEDLIST *pOut
);
```



<span data-ttu-id="d0e5a-208">在上述範例中， **LINKEDLIST** 的記憶體格式將與封送的電傳格式相同。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-208">In the above example, the memory format for **LINKEDLIST** will be identical to the marshaled wire format.</span></span> <span data-ttu-id="d0e5a-209">如此一來，伺服器存根就不會為 *pIn* 下的整個資料指標鏈配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-209">As a result, the server stub does not allocate memory for the entire chain of data pointers under *pIn*.</span></span> <span data-ttu-id="d0e5a-210">相反地，RPC 會針對整個連結清單重複使用網路緩衝區。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-210">Rather, RPC reuses the wire buffer for the entire linked list.</span></span> <span data-ttu-id="d0e5a-211">同樣地，存根不會配置 *針腳* 的記憶體，而是會重複使用用戶端所封送的網路緩衝區。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-211">Similarly, the stub does not allocate memory for *pInOut*, but instead reuses the wire buffer marshaled by the client.</span></span>

<span data-ttu-id="d0e5a-212">因為函式簽章包含輸出參數 *不悅*，所以伺服器 stub 會配置記憶體以包含傳回的資料。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-212">Because the function signature contains an outbound parameter, *pOut*, the server stub allocates memory to contain the returned data.</span></span> <span data-ttu-id="d0e5a-213">配置的記憶體一開始會是零，且 **pNext** 設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-213">The allocated memory is initially zeroes out, with **pNext** set to **NULL**.</span></span> <span data-ttu-id="d0e5a-214">應用程式可以為新的連結清單配置記憶體，並將 *不悅* -> **pNext** 至該連結清單。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-214">The application can allocate the memory for a new linked list and point *pOut*->**pNext** to it.</span></span> <span data-ttu-id="d0e5a-215">*釘* 選和其包含的連結清單可以用來做為臨時區域，但應用程式不應該變更任何 pNext 指標。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-215">*pIn* and the linked list it contains can be used as a scratch area, but the application should not change any of the pNext pointers.</span></span>

<span data-ttu-id="d0e5a-216">應用程式可以自由變更接腳所指向之連結清單的內容，但它不能變更任何 **pNext** *指標，而* 只讓最上層連結本身。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-216">The application can freely change the content of the linked list pointed to by *pInOut*, but it must not change any of the **pNext** pointers, let alone the top-level link itself.</span></span> <span data-ttu-id="d0e5a-217">如果應用程式決定縮短連結清單，它就無法得知是否有任何指定的 **pNext** 指標連結為了 RPC 內部緩衝區，或是特別以 **MIDL \_ 使用者 \_ 配置 () 配置** 的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-217">If the application decides to shorten the linked list, it cannot know if any given **pNext** pointer links tto an RPC internal buffer or a buffer specifically allocated with **MIDL\_user\_allocate()**.</span></span> <span data-ttu-id="d0e5a-218">若要解決這個問題，您可以針對會強制使用者配置的連結清單指標新增特定類型宣告，如下列程式碼所示。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-218">To work around this issue, you add a specific type declaration for linked list pointers that forces user allocation, as seen in the code below.</span></span>

``` syntax
typedef [force_allocate] PLINKEDLIST;
```

<span data-ttu-id="d0e5a-219">這個屬性會強制服務器 stub 個別配置連結清單的每個節點，而且應用程式可以呼叫 **MIDL \_ 使用者 \_ free ()**，釋放連結清單的縮寫部分。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-219">This attribute forces the server stub to allocate each node of the linked list separately, and the application can free the shortened part of the linked list by calling **MIDL\_user\_free()**.</span></span> <span data-ttu-id="d0e5a-220">然後，應用程式可以安全地將新縮短連結清單結尾的 **pNext** 指標設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="d0e5a-220">The application can then safely set the **pNext** pointer at the end of the newly-shortened linked list to **NULL**.</span></span>

 

 