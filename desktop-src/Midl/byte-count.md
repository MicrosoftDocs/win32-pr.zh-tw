---
title: byte_count 屬性
description: '\ Byte \_ count \ ACF 屬性是一個參數屬性，可將大小（以位元組為單位）與指標所指示的記憶體區域產生關聯。'
ms.assetid: 7e146888-fe7c-461c-8615-70da1e3b12cd
keywords:
- byte_count 屬性 MIDL
topic_type:
- apiref
api_name:
- byte_count
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d82d34a60ea736d10c8ec5ee8a001370c6b64c6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312849"
---
# <a name="byte_count-attribute"></a><span data-ttu-id="ddeaa-104">byte \_ count 屬性</span><span class="sxs-lookup"><span data-stu-id="ddeaa-104">byte\_count attribute</span></span>

<span data-ttu-id="ddeaa-105">**\[ Byte \_ count \]** ACF 屬性是一個參數屬性，可將大小（以位元組為單位）與指標所指示的記憶體區域產生關聯。</span><span class="sxs-lookup"><span data-stu-id="ddeaa-105">The **\[byte\_count\]** ACF attribute is a parameter attribute that associates a size, in bytes, with the memory area indicated by the pointer.</span></span>

``` syntax
[ function-attribute-list ] function-name(
    [byte_count(length-variable-name)] parameter-name);
    ...);
```

## <a name="parameters"></a><span data-ttu-id="ddeaa-106">參數</span><span class="sxs-lookup"><span data-stu-id="ddeaa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ddeaa-107">*函數-屬性清單*</span><span class="sxs-lookup"><span data-stu-id="ddeaa-107">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="ddeaa-108">指定零個或多個 ACF 函數屬性。</span><span class="sxs-lookup"><span data-stu-id="ddeaa-108">Specifies zero or more ACF function attributes.</span></span>

</dd> <dt>

<span data-ttu-id="ddeaa-109">*函數名稱*</span><span class="sxs-lookup"><span data-stu-id="ddeaa-109">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="ddeaa-110">指定 IDL 檔案中定義之函數的名稱。</span><span class="sxs-lookup"><span data-stu-id="ddeaa-110">Specifies the name of the function defined in the IDL file.</span></span> <span data-ttu-id="ddeaa-111">需要函數名稱。</span><span class="sxs-lookup"><span data-stu-id="ddeaa-111">The function name is required.</span></span>

</dd> <dt>

<span data-ttu-id="ddeaa-112">*長度-變數名稱*</span><span class="sxs-lookup"><span data-stu-id="ddeaa-112">*length-variable-name*</span></span> 
</dt> <dd>

<span data-ttu-id="ddeaa-113">指定 *參數* 名稱所參考的記憶體區域大小 [**（以位元組 \[ \]**](in.md)為單位），指定僅限指定的參數名稱。</span><span class="sxs-lookup"><span data-stu-id="ddeaa-113">Specifies the name of the [**\[in\]**](in.md)-only parameter that specifies the size, in bytes, of the memory area referenced by *parameter-name*.</span></span>

</dd> <dt>

<span data-ttu-id="ddeaa-114">*參數-名稱*</span><span class="sxs-lookup"><span data-stu-id="ddeaa-114">*parameter-name*</span></span> 
</dt> <dd>

<span data-ttu-id="ddeaa-115">指定 IDL 檔案中所定義之 [**\[ out \]**](out-idl.md)指標參數的名稱。</span><span class="sxs-lookup"><span data-stu-id="ddeaa-115">Specifies the name of the [**\[out\]**](out-idl.md)-only pointer parameter defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ddeaa-116">備註</span><span class="sxs-lookup"><span data-stu-id="ddeaa-116">Remarks</span></span>

<span data-ttu-id="ddeaa-117">ACF 屬性 **\[ 位元組 \_ 計數 \]** 表示 MICROSOFT 的延伸至 DCE IDL 的延伸模組。</span><span class="sxs-lookup"><span data-stu-id="ddeaa-117">The ACF attribute **\[byte\_count\]** represents a Microsoft extension to DCE IDL.</span></span> <span data-ttu-id="ddeaa-118">因此，當您使用 MIDL 編譯器參數 [**/osf**](-osf.md)時，就無法使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="ddeaa-118">Therefore, this attribute is not available when you use the MIDL compiler switch [**/osf**](-osf.md).</span></span>

> [!Note]  
> <span data-ttu-id="ddeaa-119">因為估計所有 [**\[ out \]**](out-idl.md)參數所需的大小，所以 NDR64 語法不再支援 **\[ byte count \]** 屬性。</span><span class="sxs-lookup"><span data-stu-id="ddeaa-119">The **\[byte count\]** attribute is no longer supported in NDR64 syntax due to the difficulty in estimating the size required for all [**\[out\]**](out-idl.md) parameters.</span></span>

 

<span data-ttu-id="ddeaa-120">指標參數所參考的記憶體是連續的，而且不會由用戶端存根配置或釋放。</span><span class="sxs-lookup"><span data-stu-id="ddeaa-120">Memory referenced by the pointer parameter is contiguous and is not allocated or freed by the client stubs.</span></span> <span data-ttu-id="ddeaa-121">[ **\[ 位元組 \_ 計數 \]** ] 屬性的這項功能可讓您在用戶端記憶體中建立持續性緩衝區區域，以便在多個遠端程序呼叫期間重複使用。</span><span class="sxs-lookup"><span data-stu-id="ddeaa-121">This feature of the **\[byte\_count\]** attribute lets you create a persistent buffer area in client memory that can be reused during more than one call to the remote procedure.</span></span>

<span data-ttu-id="ddeaa-122">關閉用戶端 stub 記憶體配置的能力可讓您調整應用程式的效率。</span><span class="sxs-lookup"><span data-stu-id="ddeaa-122">The ability to turn off the client stub memory allocation lets you tune the application for efficiency.</span></span> <span data-ttu-id="ddeaa-123">例如，使用 Microsoft RPC 的服務提供者函數可使用 **\[ byte \_ count \]** 屬性。</span><span class="sxs-lookup"><span data-stu-id="ddeaa-123">For example, the **\[byte\_count\]** attribute can be used by service-provider functions that use Microsoft RPC.</span></span> <span data-ttu-id="ddeaa-124">當使用者應用程式呼叫服務提供者 API 並將指標傳送至緩衝區時，服務提供者可以將緩衝區指標傳遞至遠端函式。</span><span class="sxs-lookup"><span data-stu-id="ddeaa-124">When a user application calls the service-provider API and sends a pointer to a buffer, the service provider can pass the buffer pointer on to the remote function.</span></span> <span data-ttu-id="ddeaa-125">服務提供者可以在多個遠端呼叫期間重複使用緩衝區，而不會強制使用者重新配置記憶體區域。</span><span class="sxs-lookup"><span data-stu-id="ddeaa-125">The service provider can reuse the buffer during multiple remote calls without forcing the user to reallocate the memory area.</span></span>

<span data-ttu-id="ddeaa-126">記憶體區域可以包含包含多個指標的複雜資料結構。</span><span class="sxs-lookup"><span data-stu-id="ddeaa-126">The memory area can contain complex data structures that consist of multiple pointers.</span></span> <span data-ttu-id="ddeaa-127">因為記憶體區域是連續的，所以應用程式不需要進行數個呼叫來個別釋放每個指標和結構。</span><span class="sxs-lookup"><span data-stu-id="ddeaa-127">Because the memory area is contiguous, the application does not have to make several calls to individually free each pointer and structure.</span></span> <span data-ttu-id="ddeaa-128">相反地，它可以透過呼叫記憶體配置或免費常式來配置或釋放記憶體區域。</span><span class="sxs-lookup"><span data-stu-id="ddeaa-128">Instead, it can allocate or free the memory area with one call to the memory allocation or free routine.</span></span>

<span data-ttu-id="ddeaa-129">緩衝區必須是 [**\[ \] out**](out-idl.md)參數，而緩衝區長度（以位元組為單位） [**\[ \] 必須是僅供使用的**](in.md)參數。</span><span class="sxs-lookup"><span data-stu-id="ddeaa-129">The buffer must be an [**\[out\]**](out-idl.md)-only parameter, while the buffer length in bytes must be an [**\[in\]**](in.md)-only parameter.</span></span>

<span data-ttu-id="ddeaa-130">指定夠大的緩衝區，以包含所有 [**\[ out \]**](out-idl.md)參數。</span><span class="sxs-lookup"><span data-stu-id="ddeaa-130">Specify a buffer that is large enough to contain all the [**\[out\]**](out-idl.md) parameters.</span></span> <span data-ttu-id="ddeaa-131">由於隱藏填補的原因，請使用 overestimates，而不是確切的計數。</span><span class="sxs-lookup"><span data-stu-id="ddeaa-131">Because of hidden padding, use overestimates rather than exact counts.</span></span> <span data-ttu-id="ddeaa-132">例如，4位元組指標會在32位平臺上以4位元組對齊的界限，以及64位平臺上8位元組界限上的8位元組指標取消封送。</span><span class="sxs-lookup"><span data-stu-id="ddeaa-132">For example, 4-byte pointers are unmarshaled on a 4-byte aligned boundary on 32-bit platforms and 8-byte pointers on an 8-byte boundary on 64-bit platforms.</span></span> <span data-ttu-id="ddeaa-133">因此，必須在緩衝區的空間中考慮存根要執行的對齊填補。</span><span class="sxs-lookup"><span data-stu-id="ddeaa-133">Therefore, the alignment padding the stubs will perform must be accounted for in the space for the buffer.</span></span> <span data-ttu-id="ddeaa-134">此外，C 語言編譯期間使用的封裝層級可能會有所不同。</span><span class="sxs-lookup"><span data-stu-id="ddeaa-134">In addition, packing levels used during C-language compilation can vary.</span></span> <span data-ttu-id="ddeaa-135">使用 [位元組計數] 值，以針對 C 語言編譯期間所使用的封裝層級新增額外的封裝位元組。</span><span class="sxs-lookup"><span data-stu-id="ddeaa-135">Use a byte count value that accounts for additional packing bytes added for the packing level used during C-language compilation.</span></span> <span data-ttu-id="ddeaa-136">涵蓋32位平臺和64位平臺的安全做法，是假設每個進入海量儲存體區塊的物件都是從屬於8的倍數的位址開始。</span><span class="sxs-lookup"><span data-stu-id="ddeaa-136">A safe practice that covers both 32 bit platforms and 64 bit platforms is to assume that each object going into the big memory block starts at an address that is a multiple of 8.</span></span>

## <a name="examples"></a><span data-ttu-id="ddeaa-137">範例</span><span class="sxs-lookup"><span data-stu-id="ddeaa-137">Examples</span></span>

``` syntax
/* IDL file */ 
HRESULT proc1([in] unsigned long length, 
              [out] struct my_struct * pMyStruct); 
 
/* ACF file */ 
proc1([byte_count(length)] pMyStruct);
```

## <a name="see-also"></a><span data-ttu-id="ddeaa-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ddeaa-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddeaa-139">應用程式佈建檔 (ACF) </span><span class="sxs-lookup"><span data-stu-id="ddeaa-139">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="ddeaa-140">**在**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-140">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="ddeaa-141">**長度 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-141">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="ddeaa-142">**/osf**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-142">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="ddeaa-143">**擴展**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-143">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="ddeaa-144">**大小 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="ddeaa-144">**size\_is**</span></span>](size-is.md)
</dt> </dl>

 

 




