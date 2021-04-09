---
title: fault_status 屬性
description: '\ 錯誤 \_ 狀態 \ ACF 屬性指定錯誤 \_ 狀態 t 的錯誤碼 \_ 指出遠端程式失敗，而不是其他類型的問題，例如通訊錯誤。'
ms.assetid: 9da7bd3d-cef0-4ad4-b2a4-3f8aa156e8e0
keywords:
- fault_status 屬性 MIDL
topic_type:
- apiref
api_name:
- fault_status
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 134d9772e167fe63e133d569b9985a7735668d3c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678251"
---
# <a name="fault_status-attribute"></a><span data-ttu-id="ddd9f-104">錯誤 \_ 狀態屬性</span><span class="sxs-lookup"><span data-stu-id="ddd9f-104">fault\_status attribute</span></span>

<span data-ttu-id="ddd9f-105">錯誤 **\[ \_ 狀態 \]** ACF 屬性指定錯誤 [**\_ 狀態 \_ t**](error-status-t.md)的錯誤碼指出遠端程式失敗，而不是其他類型的問題，例如通訊錯誤。</span><span class="sxs-lookup"><span data-stu-id="ddd9f-105">The **\[fault\_status\]** ACF attribute specifies that an error code of type [**error\_status\_t**](error-status-t.md) indicates a failure of the remote procedure, rather than other types of problems such as communication errors.</span></span>

``` syntax
[fault_status [ , ACF-function-attributes ] ] function-name(
    [ [ ACF-parameter-attributes ] ] parameter-name
    , ... );

[ [ ACF-function-attributes ] ] function-name(
    [fault_status [ , ACF-parameter-attributes ] ] parameter-name
    , ... );
```

## <a name="parameters"></a><span data-ttu-id="ddd9f-106">參數</span><span class="sxs-lookup"><span data-stu-id="ddd9f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ddd9f-107">*ACF 函式-屬性*</span><span class="sxs-lookup"><span data-stu-id="ddd9f-107">*ACF-function-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="ddd9f-108">指定零個或多個 ACF 函數屬性，例如 **\[ 錯誤 \_ 狀態 \]** 和 **\[** [**了 nocode**](nocode.md) **\]** 。</span><span class="sxs-lookup"><span data-stu-id="ddd9f-108">Specifies zero or more ACF function attributes such as **\[fault\_status\]** and **\[**[**nocode**](nocode.md)**\]**.</span></span> <span data-ttu-id="ddd9f-109">函數屬性以方括弧括住。</span><span class="sxs-lookup"><span data-stu-id="ddd9f-109">Function attributes are enclosed in square brackets.</span></span> <span data-ttu-id="ddd9f-110">請注意，零或多個屬性可以套用至函式。</span><span class="sxs-lookup"><span data-stu-id="ddd9f-110">Note that zero or more attributes can be applied to a function.</span></span> <span data-ttu-id="ddd9f-111">以逗號分隔多個函式屬性。</span><span class="sxs-lookup"><span data-stu-id="ddd9f-111">Separate multiple function attributes with commas.</span></span> <span data-ttu-id="ddd9f-112">另請注意，如果 **\[ 錯誤 \_ 狀態 \]** 顯示為函式屬性，它也不能顯示為參數屬性。</span><span class="sxs-lookup"><span data-stu-id="ddd9f-112">Also note that if **\[fault\_status\]** appears as a function attribute, it cannot also appear as a parameter attribute.</span></span>

</dd> <dt>

<span data-ttu-id="ddd9f-113">*函數名稱*</span><span class="sxs-lookup"><span data-stu-id="ddd9f-113">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="ddd9f-114">指定 IDL 檔案中所定義的函式名稱。</span><span class="sxs-lookup"><span data-stu-id="ddd9f-114">Specifies the name of the function as defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="ddd9f-115">*ACF-參數-屬性*</span><span class="sxs-lookup"><span data-stu-id="ddd9f-115">*ACF-parameter-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="ddd9f-116">指定適用于參數的屬性。</span><span class="sxs-lookup"><span data-stu-id="ddd9f-116">Specifies attributes that apply to a parameter.</span></span> <span data-ttu-id="ddd9f-117">請注意，您可以將零個或更多屬性套用至參數。</span><span class="sxs-lookup"><span data-stu-id="ddd9f-117">Note that zero or more attributes can be applied to the parameter.</span></span> <span data-ttu-id="ddd9f-118">參數屬性以方括弧括住。</span><span class="sxs-lookup"><span data-stu-id="ddd9f-118">Parameter attributes are enclosed in square brackets.</span></span> <span data-ttu-id="ddd9f-119">以逗號分隔多個參數屬性。</span><span class="sxs-lookup"><span data-stu-id="ddd9f-119">Separate multiple parameter attributes with commas.</span></span> <span data-ttu-id="ddd9f-120">ACF 中不允許 IDL 參數屬性（例如方向屬性）。</span><span class="sxs-lookup"><span data-stu-id="ddd9f-120">IDL parameter attributes, such as directional attributes, are not allowed in the ACF.</span></span> <span data-ttu-id="ddd9f-121">請注意，如果 **\[ 錯誤 \_ 狀態 \]** 顯示為參數屬性，它也不能顯示為函數屬性。</span><span class="sxs-lookup"><span data-stu-id="ddd9f-121">Note that if **\[fault\_status\]** appears as a parameter attribute, it cannot also appear as a function attribute.</span></span>

</dd> <dt>

<span data-ttu-id="ddd9f-122">*參數-名稱*</span><span class="sxs-lookup"><span data-stu-id="ddd9f-122">*parameter-name*</span></span> 
</dt> <dd>

<span data-ttu-id="ddd9f-123">指定 IDL 檔案中定義之函數的參數。</span><span class="sxs-lookup"><span data-stu-id="ddd9f-123">Specifies the parameter for the function as defined in the IDL file.</span></span> <span data-ttu-id="ddd9f-124">函數的每個參數都必須以相同的順序指定，且使用與 IDL 檔案中所定義的相同名稱。</span><span class="sxs-lookup"><span data-stu-id="ddd9f-124">Each parameter for the function must be specified in the same sequence, using the same name as defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ddd9f-125">備註</span><span class="sxs-lookup"><span data-stu-id="ddd9f-125">Remarks</span></span>

<span data-ttu-id="ddd9f-126">**\[ 錯誤 \_ 狀態 \]** 屬性可以當做函數屬性或參數屬性使用，但每個函數只能出現一次。</span><span class="sxs-lookup"><span data-stu-id="ddd9f-126">The **\[fault\_status\]** attribute can be used as either a function attribute or as a parameter attribute, but it can appear only once per function.</span></span> <span data-ttu-id="ddd9f-127">它可以套用至函式本身或每個函數中的一個參數。</span><span class="sxs-lookup"><span data-stu-id="ddd9f-127">It can be applied either to the function itself or to one parameter in each function.</span></span>

<span data-ttu-id="ddd9f-128">**\[ 錯誤 \_ 狀態 \]** 屬性只能套用至傳回類型 [**錯誤 \_ 狀態 \_ t**](error-status-t.md)的函式。</span><span class="sxs-lookup"><span data-stu-id="ddd9f-128">The **\[fault\_status\]** attribute can be applied only to functions that return the type [**error\_status\_t**](error-status-t.md).</span></span> <span data-ttu-id="ddd9f-129">當遠端程式失敗，導致傳回錯誤 PDU 時，會傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="ddd9f-129">When the remote procedure fails in a way that causes a fault PDU to be returned, an error code is returned.</span></span>

<span data-ttu-id="ddd9f-130">當 **\[ 錯誤 \_ 狀態 \]** 當做參數屬性使用時，參數必須是 **\[** [](out-idl.md) **\]** [**錯誤 \_ 狀態 \_ t**](error-status-t.md)類型的 out 參數。</span><span class="sxs-lookup"><span data-stu-id="ddd9f-130">When **\[fault\_status\]** is used as a parameter attribute, the parameter must be an **\[**[**out**](out-idl.md)**\]** parameter of type [**error\_status\_t**](error-status-t.md).</span></span> <span data-ttu-id="ddd9f-131">如果發生伺服器錯誤，參數會設定為錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="ddd9f-131">If a server error occurs, the parameter is set to the error code.</span></span> <span data-ttu-id="ddd9f-132">當遠端呼叫順利完成時，程式會設定此值。</span><span class="sxs-lookup"><span data-stu-id="ddd9f-132">When the remote call is successfully completed, the procedure sets the value.</span></span>

<span data-ttu-id="ddd9f-133">與 **\[ 錯誤 \_ 狀態 \]** 屬性相關聯的參數，不需要在 IDL 檔案中指定。</span><span class="sxs-lookup"><span data-stu-id="ddd9f-133">The parameter associated with the **\[fault\_status\]** attribute does not have to be specified in the IDL file.</span></span> <span data-ttu-id="ddd9f-134">如果未指定參數，則會在 DCE IDL 檔案中定義的最後一個參數之後，產生型 [**\_ 別錯誤狀態 \_ t**](error-status-t.md)的新 [**out**](out-idl.md)參數。</span><span class="sxs-lookup"><span data-stu-id="ddd9f-134">When the parameter is not specified, a new [**out**](out-idl.md) parameter of type [**error\_status\_t**](error-status-t.md) is generated following the last parameter defined in the DCE IDL file.</span></span>

<span data-ttu-id="ddd9f-135">**\[ 錯誤 \_ 狀態 \]** 和 **\[** 屬性（attribute） [**\_ 狀態**](comm-status.md) **\]** 屬性（attribute）可能會以函數屬性或參數屬性（attribute）的形式出現在單一函式中。</span><span class="sxs-lookup"><span data-stu-id="ddd9f-135">It is possible for both the **\[fault\_status\]** and **\[**[**comm\_status**](comm-status.md)**\]** attributes to appear in a single function, either as function attributes or parameter attributes.</span></span> <span data-ttu-id="ddd9f-136">如果這兩個屬性都是函數屬性，或它們套用至相同參數但未發生任何錯誤，則函數或參數的值 **錯誤 \_ 狀態為 \_ [確定]**。</span><span class="sxs-lookup"><span data-stu-id="ddd9f-136">If both attributes are function attributes, or if they apply to the same parameter and no error occurs, the function or parameter has the value **error\_status\_ok**.</span></span> <span data-ttu-id="ddd9f-137">否則，它會包含適當的狀態碼值。</span><span class="sxs-lookup"><span data-stu-id="ddd9f-137">Otherwise, it contains the appropriate status code value.</span></span> <span data-ttu-id="ddd9f-138">因為針對 **\[ 錯誤 \_ 狀態 \]** 傳回的值與針對 [ **\[ 通訊 \_ 狀態 \]**] 傳回的值不同，所以會立即解讀傳回的值。</span><span class="sxs-lookup"><span data-stu-id="ddd9f-138">Because values returned for **\[fault\_status\]** are different from the values returned for **\[comm\_status\]**, the returned values are readily interpreted.</span></span>

## <a name="see-also"></a><span data-ttu-id="ddd9f-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ddd9f-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddd9f-140">應用程式佈建檔 (ACF) </span><span class="sxs-lookup"><span data-stu-id="ddd9f-140">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="ddd9f-141">**通訊 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="ddd9f-141">**comm\_status**</span></span>](comm-status.md)
</dt> <dt>

[<span data-ttu-id="ddd9f-142">**錯誤 \_ 狀態 \_ t**</span><span class="sxs-lookup"><span data-stu-id="ddd9f-142">**error\_status\_t**</span></span>](error-status-t.md)
</dt> <dt>

[<span data-ttu-id="ddd9f-143">**了 nocode**</span><span class="sxs-lookup"><span data-stu-id="ddd9f-143">**nocode**</span></span>](nocode.md)
</dt> <dt>

[<span data-ttu-id="ddd9f-144">**擴展**</span><span class="sxs-lookup"><span data-stu-id="ddd9f-144">**out**</span></span>](out-idl.md)
</dt> </dl>

 

 




