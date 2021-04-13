---
title: error_status_t 屬性
description: 錯誤 \_ 狀態 \_ t 關鍵字會指定物件的類型，該物件包含通訊狀態或錯誤狀態資訊。
ms.assetid: 7eff0d20-c058-4f16-a3db-0b4c82303135
keywords:
- error_status_t 屬性 MIDL
topic_type:
- apiref
api_name:
- error_status_t
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0d017b4eaf460b5d5b7ecb8a0bd79201ac8bdee
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312218"
---
# <a name="error_status_t-attribute"></a><span data-ttu-id="0bac7-104">錯誤 \_ 狀態 \_ t 屬性</span><span class="sxs-lookup"><span data-stu-id="0bac7-104">error\_status\_t attribute</span></span>

<span data-ttu-id="0bac7-105">**錯誤 \_ 狀態 \_ t** 關鍵字會指定物件的類型，該物件包含通訊狀態或錯誤狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="0bac7-105">The **error\_status\_t** keyword designates a type for an object that contains communication-status or fault-status information.</span></span>

``` syntax
[ [ , ACF-function-attributes ] ] error_status_t function-name(
        [ [ ACF-parameter-attributes ] ] parameter-name
        , ...);

[ [ ACF-function-attributes ] ] function-name(
    [ [ ACF-parameter-attributes ] ] error_status_t parameter-name
    , ...);
```

## <a name="parameters"></a><span data-ttu-id="0bac7-106">參數</span><span class="sxs-lookup"><span data-stu-id="0bac7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0bac7-107">*ACF 函式-屬性*</span><span class="sxs-lookup"><span data-stu-id="0bac7-107">*ACF-function-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="0bac7-108">指定零個或多個 ACF 函數屬性，例如， **\[** [**comm \_ status**](comm-status.md) **\]** 、 **\[** [**fault \_ status**](fault-status.md) **\]** 或 **\[** [**了 nocode**](nocode.md) **\]** 。</span><span class="sxs-lookup"><span data-stu-id="0bac7-108">Specifies zero or more ACF function attributes, such as **\[**[**comm\_status**](comm-status.md)**\]**, **\[**[**fault\_status**](fault-status.md)**\]**, or **\[**[**nocode**](nocode.md)**\]**.</span></span> <span data-ttu-id="0bac7-109">函數屬性以方括弧括住。</span><span class="sxs-lookup"><span data-stu-id="0bac7-109">Function attributes are enclosed in square brackets.</span></span> <span data-ttu-id="0bac7-110">有零或多個屬性可以套用至函數。</span><span class="sxs-lookup"><span data-stu-id="0bac7-110">Zero or more attributes can be applied to a function.</span></span> <span data-ttu-id="0bac7-111">以逗號分隔多個函式屬性。</span><span class="sxs-lookup"><span data-stu-id="0bac7-111">Separate multiple function attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="0bac7-112">*函數名稱*</span><span class="sxs-lookup"><span data-stu-id="0bac7-112">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="0bac7-113">指定 IDL 檔案中所定義的函式名稱。</span><span class="sxs-lookup"><span data-stu-id="0bac7-113">Specifies the name of the function as defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="0bac7-114">*ACF-參數-屬性*</span><span class="sxs-lookup"><span data-stu-id="0bac7-114">*ACF-parameter-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="0bac7-115">指定適用于參數的屬性。</span><span class="sxs-lookup"><span data-stu-id="0bac7-115">Specifies attributes that apply to a parameter.</span></span> <span data-ttu-id="0bac7-116">請注意，您可以將零個、一個或多個屬性套用至參數。</span><span class="sxs-lookup"><span data-stu-id="0bac7-116">Note that zero, one, or more attributes can be applied to the parameter.</span></span> <span data-ttu-id="0bac7-117">以逗號分隔多個參數屬性。</span><span class="sxs-lookup"><span data-stu-id="0bac7-117">Separate multiple parameter attributes with commas.</span></span> <span data-ttu-id="0bac7-118">參數屬性以方括弧括住。</span><span class="sxs-lookup"><span data-stu-id="0bac7-118">Parameter attributes are enclosed in square brackets.</span></span> <span data-ttu-id="0bac7-119">ACF 中不允許 IDL 參數屬性（例如方向屬性）。</span><span class="sxs-lookup"><span data-stu-id="0bac7-119">IDL parameter attributes, such as directional attributes, are not allowed in the ACF.</span></span>

</dd> <dt>

<span data-ttu-id="0bac7-120">*參數-名稱*</span><span class="sxs-lookup"><span data-stu-id="0bac7-120">*parameter-name*</span></span> 
</dt> <dd>

<span data-ttu-id="0bac7-121">指定 IDL 檔案中定義之函數的參數。</span><span class="sxs-lookup"><span data-stu-id="0bac7-121">Specifies the parameter for the function as defined in the IDL file.</span></span> <span data-ttu-id="0bac7-122">函數的每個參數都必須以相同的順序指定，且使用與 IDL 檔案中所定義的相同名稱。</span><span class="sxs-lookup"><span data-stu-id="0bac7-122">Each parameter for the function must be specified in the same sequence, using the same name as defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0bac7-123">備註</span><span class="sxs-lookup"><span data-stu-id="0bac7-123">Remarks</span></span>

<span data-ttu-id="0bac7-124">**錯誤 \_ 狀態 \_ t** 類型會當做 IDL 中例外狀況處理架構的一部分來使用。</span><span class="sxs-lookup"><span data-stu-id="0bac7-124">The **error\_status\_t** type is used as a part of the exception handling architecture in IDL.</span></span> <span data-ttu-id="0bac7-125">此類型對應到不 [**帶正負**](unsigned.md)號的 [**long**](long.md)。</span><span class="sxs-lookup"><span data-stu-id="0bac7-125">This type maps to an [**unsigned**](unsigned.md) [**long**](long.md).</span></span> <span data-ttu-id="0bac7-126">捕捉錯誤情況的應用程式具有 **\[** [](out-idl.md) **\]** 指定為 **錯誤 \_ 狀態 \_ t** 之程式的 OUT 參數或傳回類型，並使用 ACF 中的 [通訊狀態] 或 [錯誤狀態] 屬性來限定 **錯誤 \_ 狀態 \_ t** **\[** [**\_**](comm-status.md) **\]** **\[** [**\_**](fault-status.md) **\]** 。</span><span class="sxs-lookup"><span data-stu-id="0bac7-126">Applications that catch error situations have an **\[**[**out**](out-idl.md)**\]** parameter or a return type of a procedure specified as **error\_status\_t**, and qualify the **error\_status\_t** with the **\[**[**comm\_status**](comm-status.md)**\]** or **\[**[**fault\_status**](fault-status.md)**\]** attributes in the ACF.</span></span> <span data-ttu-id="0bac7-127">如果參數或傳回型別未以 **\[ comm \_ 狀態 \]** 或 **\[ 錯誤 \_ 狀態 \]** 屬性限定，則參數的運作方式就如同不帶正負號的 long。</span><span class="sxs-lookup"><span data-stu-id="0bac7-127">If the parameter or return type was not qualified with the **\[comm\_status\]** or **\[fault\_status\]** attributes, then the parameter operates as though it were an unsigned long.</span></span>

<span data-ttu-id="0bac7-128">從2.0 版開始，MIDL 編譯器會產生包含適當錯誤處理架構的存根。</span><span class="sxs-lookup"><span data-stu-id="0bac7-128">Beginning with version 2.0, the MIDL compiler generates stubs that contain the proper error handling architecture.</span></span> <span data-ttu-id="0bac7-129">不過，舊版 MIDL 編譯器會處理參數或傳回 **錯誤 \_ 狀態 \_ t** 的型別，如同已套用的 **\[** [**通訊 \_ 狀態**](comm-status.md) **\]** 和 **\[** [**錯誤 \_ 狀態**](fault-status.md) **\]** 屬性一樣，即使它們不是也是一樣。</span><span class="sxs-lookup"><span data-stu-id="0bac7-129">However, earlier versions of the MIDL compiler handled a parameter or return type of **error\_status\_t** as though the **\[**[**comm\_status**](comm-status.md)**\]** and **\[**[**fault\_status**](fault-status.md)**\]** attributes were applied, even if they were not.</span></span> <span data-ttu-id="0bac7-130">使用 MIDL 2.0 或更新版本時，您必須明確地將 **\[ 通訊 \_ 狀態 \]** 和 **\[ 錯誤 \_ 狀態 \]** 屬性套用至 ACF 中的參數或程式。</span><span class="sxs-lookup"><span data-stu-id="0bac7-130">With MIDL 2.0 or later, you must explicitly apply the **\[comm\_status\]** and **\[fault\_status\]** attributes to the parameter or procedure in the ACF.</span></span>

<span data-ttu-id="0bac7-131">**錯誤 \_ 狀態 \_ t** 類型是其中一種預先定義的介面定義語言類型。</span><span class="sxs-lookup"><span data-stu-id="0bac7-131">The **error\_status\_t** type is one of the predefined types of the interface definition language.</span></span> <span data-ttu-id="0bac7-132">預先定義的型別可以在 [**typedef**](typedef.md) 宣告中顯示為類型指定名稱，在一般宣告中，也可以在函式宣告子中做為函式的傳回型別或) 的參數類型指定名稱， (。</span><span class="sxs-lookup"><span data-stu-id="0bac7-132">Predefined types can appear as type specifiers in [**typedef**](typedef.md) declarations, in general declarations, and in function declarators (either as the function-return-type or as parameter-type specifiers).</span></span>

## <a name="see-also"></a><span data-ttu-id="0bac7-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0bac7-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bac7-134">**通訊 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="0bac7-134">**comm\_status**</span></span>](comm-status.md)
</dt> <dt>

[<span data-ttu-id="0bac7-135">**錯誤 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="0bac7-135">**fault\_status**</span></span>](fault-status.md)
</dt> <dt>

[<span data-ttu-id="0bac7-136"> (IDL) 檔案的介面定義</span><span class="sxs-lookup"><span data-stu-id="0bac7-136">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="0bac7-137">**long**</span><span class="sxs-lookup"><span data-stu-id="0bac7-137">**long**</span></span>](long.md)
</dt> <dt>

[<span data-ttu-id="0bac7-138">**擴展**</span><span class="sxs-lookup"><span data-stu-id="0bac7-138">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="0bac7-139">**著**</span><span class="sxs-lookup"><span data-stu-id="0bac7-139">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="0bac7-140">**符號**</span><span class="sxs-lookup"><span data-stu-id="0bac7-140">**unsigned**</span></span>](unsigned.md)
</dt> </dl>

 

 




