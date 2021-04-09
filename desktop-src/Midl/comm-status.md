---
title: comm_status 屬性
description: '\_當函式執行期間發生通訊錯誤時，\ 通訊狀態 \ ACF 屬性會導致傳回錯誤碼。'
ms.assetid: 3ea9ce62-8bd4-40fe-b838-bfebd52b5a15
keywords:
- comm_status 屬性 MIDL
topic_type:
- apiref
api_name:
- comm_status
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd4952d03a80dbbffb135043d024b0c0eb18966f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678719"
---
# <a name="comm_status-attribute"></a><span data-ttu-id="57d37-104">comm \_ status 屬性</span><span class="sxs-lookup"><span data-stu-id="57d37-104">comm\_status attribute</span></span>

<span data-ttu-id="57d37-105">當函數執行期間發生通訊錯誤時，[ **\[ 通訊 \_ 狀態 \]** ACF] 屬性會導致傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="57d37-105">The **\[comm\_status\]** ACF attribute causes an error code to be returned when a communication error occurs during the execution of a function.</span></span>

``` syntax
[comm_status [ , ACF-function-attributes ] ] 
    error_status_t function-name(
        [ [ ACF-parameter-attributes ] ] parameter-name
        , ...);

[ [ ACF-function-attributes ] ] function-name(
    [comm_status [ , ACF-parameter-attributes ] ] error_status_t name
    , ...);
```

## <a name="parameters"></a><span data-ttu-id="57d37-106">參數</span><span class="sxs-lookup"><span data-stu-id="57d37-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57d37-107">*ACF 函式-屬性*</span><span class="sxs-lookup"><span data-stu-id="57d37-107">*ACF-function-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="57d37-108">指定零個或多個 ACF 函數屬性，例如， **\[ comm \_ status \]** 和 **\[** [**了 nocode**](nocode.md) **\]** 。</span><span class="sxs-lookup"><span data-stu-id="57d37-108">Specifies zero or more ACF function attributes, such as **\[comm\_status\]** and **\[**[**nocode**](nocode.md)**\]**.</span></span> <span data-ttu-id="57d37-109">函數屬性以方括弧括住。</span><span class="sxs-lookup"><span data-stu-id="57d37-109">Function attributes are enclosed in square brackets.</span></span> <span data-ttu-id="57d37-110">有零或多個屬性可以套用至函數。</span><span class="sxs-lookup"><span data-stu-id="57d37-110">Zero or more attributes can be applied to a function.</span></span> <span data-ttu-id="57d37-111">以逗號分隔多個函式屬性。</span><span class="sxs-lookup"><span data-stu-id="57d37-111">Separate multiple function attributes with commas.</span></span> <span data-ttu-id="57d37-112">請注意，如果 **\[ 通訊 \_ 狀態 \]** 顯示為函式屬性，它也不能顯示為參數屬性。</span><span class="sxs-lookup"><span data-stu-id="57d37-112">Note that if **\[comm\_status\]** appears as a function attribute, it cannot also appear as a parameter attribute.</span></span>

</dd> <dt>

<span data-ttu-id="57d37-113">*函數名稱*</span><span class="sxs-lookup"><span data-stu-id="57d37-113">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="57d37-114">指定 IDL 檔案中所定義的函式名稱。</span><span class="sxs-lookup"><span data-stu-id="57d37-114">Specifies the name of the function as defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="57d37-115">*ACF-參數-屬性*</span><span class="sxs-lookup"><span data-stu-id="57d37-115">*ACF-parameter-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="57d37-116">指定適用于參數的屬性。</span><span class="sxs-lookup"><span data-stu-id="57d37-116">Specifies attributes that apply to a parameter.</span></span> <span data-ttu-id="57d37-117">請注意，您可以將零個、一個或多個屬性套用至參數。</span><span class="sxs-lookup"><span data-stu-id="57d37-117">Note that zero, one, or more attributes can be applied to the parameter.</span></span> <span data-ttu-id="57d37-118">以逗號分隔多個參數屬性。</span><span class="sxs-lookup"><span data-stu-id="57d37-118">Separate multiple parameter attributes with commas.</span></span> <span data-ttu-id="57d37-119">參數屬性以方括弧括住。</span><span class="sxs-lookup"><span data-stu-id="57d37-119">Parameter attributes are enclosed in square brackets.</span></span> <span data-ttu-id="57d37-120">ACF 中不允許 IDL 參數屬性（例如方向屬性）。</span><span class="sxs-lookup"><span data-stu-id="57d37-120">IDL parameter attributes, such as directional attributes, are not allowed in the ACF.</span></span> <span data-ttu-id="57d37-121">請注意，如果 **\[ 通訊 \_ 狀態 \]** 顯示為參數屬性，它也不能顯示為函式屬性。</span><span class="sxs-lookup"><span data-stu-id="57d37-121">Note that if **\[comm\_status\]** appears as a parameter attribute, it cannot also appear as a function attribute.</span></span>

</dd> <dt>

<span data-ttu-id="57d37-122">*參數-名稱*</span><span class="sxs-lookup"><span data-stu-id="57d37-122">*parameter-name*</span></span> 
</dt> <dd>

<span data-ttu-id="57d37-123">指定 IDL 檔案中定義之函數的參數。</span><span class="sxs-lookup"><span data-stu-id="57d37-123">Specifies the parameter for the function as defined in the IDL file.</span></span> <span data-ttu-id="57d37-124">函數的每個參數都必須以相同的順序指定，且使用與 IDL 檔案中所定義的相同名稱。</span><span class="sxs-lookup"><span data-stu-id="57d37-124">Each parameter for the function must be specified in the same sequence, using the same name as defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="57d37-125">備註</span><span class="sxs-lookup"><span data-stu-id="57d37-125">Remarks</span></span>

<span data-ttu-id="57d37-126">您可以使用 [ **\[ comm \_ status \]** ] 屬性做為函數屬性或參數屬性，但每個函式只能出現一次。</span><span class="sxs-lookup"><span data-stu-id="57d37-126">The **\[comm\_status\]** attribute can be used as either a function attribute or as a parameter attribute, but it can appear only once per function.</span></span> <span data-ttu-id="57d37-127">它可以套用至函式或每個函式中的一個參數。</span><span class="sxs-lookup"><span data-stu-id="57d37-127">It can be applied either to the function or to one parameter in each function.</span></span>

<span data-ttu-id="57d37-128">[ **\[ Comm \_ status \]** ] 屬性只能套用至傳回型 [**\_ 別錯誤狀態 \_ t**](error-status-t.md)的函式。</span><span class="sxs-lookup"><span data-stu-id="57d37-128">The **\[comm\_status\]** attribute can be applied only to functions that return the type [**error\_status\_t**](error-status-t.md).</span></span> <span data-ttu-id="57d37-129">在函數執行期間發生通訊錯誤時，會傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="57d37-129">When a communication error occurs during the execution of the function, an error code is returned.</span></span>

<span data-ttu-id="57d37-130">當使用訊息 **\[ \_ \] 狀態** 做為參數屬性時，參數必須在 IDL 檔案中定義，而且必須是 **\[** [](out-idl.md) **\]** 類型 [**錯誤 \_ 狀態 \_ t**](error-status-t.md)的 out 參數。</span><span class="sxs-lookup"><span data-stu-id="57d37-130">When **\[comm\_status\]** is used as a parameter attribute, the parameter must be defined in the IDL file and must be an **\[**[**out**](out-idl.md)**\]** parameter of type [**error\_status\_t**](error-status-t.md).</span></span> <span data-ttu-id="57d37-131">當函數執行期間發生通訊錯誤時，參數會設定為錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="57d37-131">When a communication error occurs during the execution of the function, the parameter is set to the error code.</span></span> <span data-ttu-id="57d37-132">當遠端呼叫順利完成時，程式會設定此值。</span><span class="sxs-lookup"><span data-stu-id="57d37-132">When the remote call is completed successfully, the procedure sets the value.</span></span>

<span data-ttu-id="57d37-133">**\[ 通訊 \_ 狀態 \]** 和 **\[** [**錯誤 \_ 狀態**](fault-status.md) **\]** 屬性可能會以函數屬性或參數屬性的形式出現在單一函式中。</span><span class="sxs-lookup"><span data-stu-id="57d37-133">It is possible for both the **\[comm\_status\]** and **\[**[**fault\_status**](fault-status.md)**\]** attributes to appear in a single function, either as function attributes or parameter attributes.</span></span> <span data-ttu-id="57d37-134">如果這兩個屬性都是函數屬性，或它們套用至相同參數但未發生任何錯誤，則函數或參數的值 **錯誤 \_ 狀態為 \_ [確定]**。</span><span class="sxs-lookup"><span data-stu-id="57d37-134">If both attributes are function attributes or if they apply to the same parameter and no error occurs, the function or parameter has the value **error\_status\_ok**.</span></span> <span data-ttu-id="57d37-135">否則，它會包含適當的 **\[ 通訊 \_ 狀態 \]** 或 **\[ 錯誤 \_ 狀態值 \]** 。</span><span class="sxs-lookup"><span data-stu-id="57d37-135">Otherwise, it contains the appropriate **\[comm\_status\]** or **\[fault\_status\]** value.</span></span> <span data-ttu-id="57d37-136">由於針對 [狀態] **\[ \_ 狀態 \]** 傳回的值與 **\[ 錯誤 \_ \] 狀態** 傳回的值不同，因此會立即解讀傳回的值。</span><span class="sxs-lookup"><span data-stu-id="57d37-136">Because values returned for **\[comm\_status\]** are different from the values returned for **\[fault\_status\]**, the returned values are readily interpreted.</span></span>

## <a name="see-also"></a><span data-ttu-id="57d37-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="57d37-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57d37-138">應用程式佈建檔 (ACF) </span><span class="sxs-lookup"><span data-stu-id="57d37-138">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="57d37-139">**錯誤 \_ 狀態 \_ t**</span><span class="sxs-lookup"><span data-stu-id="57d37-139">**error\_status\_t**</span></span>](error-status-t.md)
</dt> <dt>

[<span data-ttu-id="57d37-140">**錯誤 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="57d37-140">**fault\_status**</span></span>](fault-status.md)
</dt> <dt>

[<span data-ttu-id="57d37-141">**了 nocode**</span><span class="sxs-lookup"><span data-stu-id="57d37-141">**nocode**</span></span>](nocode.md)
</dt> <dt>

[<span data-ttu-id="57d37-142">**擴展**</span><span class="sxs-lookup"><span data-stu-id="57d37-142">**out**</span></span>](out-idl.md)
</dt> </dl>

 

 




