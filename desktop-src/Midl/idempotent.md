---
title: 等冪屬性
description: '\ 等冪 \ 屬性指定作業在每次執行時都不會修改狀態資訊並傳回相同的結果。 執行常式一次以上，其效果與執行一次相同。'
ms.assetid: 876a40b5-8165-4b5c-bd62-9c43a9eb4b2b
keywords:
- 等冪屬性 MIDL
topic_type:
- apiref
api_name:
- idempotent
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82364c6222f6b566ef6aacb5b71a72b49c213f5a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104507536"
---
# <a name="idempotent-attribute"></a><span data-ttu-id="646d1-105">等冪屬性</span><span class="sxs-lookup"><span data-stu-id="646d1-105">idempotent attribute</span></span>

<span data-ttu-id="646d1-106">**\[ 等冪 \]** 屬性指定作業在每次執行時都不會修改狀態資訊，並傳回相同的結果。</span><span class="sxs-lookup"><span data-stu-id="646d1-106">The **\[idempotent\]** attribute specifies that an operation does not modify state information and returns the same results each time it is performed.</span></span> <span data-ttu-id="646d1-107">執行常式一次以上，其效果與執行一次相同。</span><span class="sxs-lookup"><span data-stu-id="646d1-107">Performing the routine more than once has the same effect as performing it once.</span></span>

``` syntax
[
    interface-attribute-list
] 
interface interface-name 
{
    [idempotent [, attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a><span data-ttu-id="646d1-108">參數</span><span class="sxs-lookup"><span data-stu-id="646d1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="646d1-109">*介面屬性清單*</span><span class="sxs-lookup"><span data-stu-id="646d1-109">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="646d1-110">指定套用至整個介面的零或多個 IDL 屬性清單。</span><span class="sxs-lookup"><span data-stu-id="646d1-110">Specifies a list of zero or more IDL attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="646d1-111">當有兩個或多個介面屬性存在時，它們必須以逗號分隔。</span><span class="sxs-lookup"><span data-stu-id="646d1-111">When two or more interface attributes are present, they must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="646d1-112">*介面-名稱*</span><span class="sxs-lookup"><span data-stu-id="646d1-112">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="646d1-113">指定介面的名稱。</span><span class="sxs-lookup"><span data-stu-id="646d1-113">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="646d1-114">*屬性清單*</span><span class="sxs-lookup"><span data-stu-id="646d1-114">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="646d1-115">指定要套用至函數的其他屬性。</span><span class="sxs-lookup"><span data-stu-id="646d1-115">Specifies additional attributes to be applied to the function.</span></span> <span data-ttu-id="646d1-116">以逗號分隔多個屬性。</span><span class="sxs-lookup"><span data-stu-id="646d1-116">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="646d1-117">*returntype*</span><span class="sxs-lookup"><span data-stu-id="646d1-117">*returntype*</span></span> 
</dt> <dd>

<span data-ttu-id="646d1-118">指定函式的傳回型別。</span><span class="sxs-lookup"><span data-stu-id="646d1-118">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="646d1-119">*函數名稱*</span><span class="sxs-lookup"><span data-stu-id="646d1-119">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="646d1-120">指定將套用 **\[ 等冪 \]** 屬性的函式名稱。</span><span class="sxs-lookup"><span data-stu-id="646d1-120">Specifies the name of the function to which the **\[idempotent\]** attribute will be applied.</span></span>

</dd> <dt>

<span data-ttu-id="646d1-121">*params*</span><span class="sxs-lookup"><span data-stu-id="646d1-121">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="646d1-122">函數參數清單。</span><span class="sxs-lookup"><span data-stu-id="646d1-122">Function parameter list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="646d1-123">備註</span><span class="sxs-lookup"><span data-stu-id="646d1-123">Remarks</span></span>

<span data-ttu-id="646d1-124">RPC 支援兩種類型的遠端呼叫語義：具有 **\[ 等 \] 冪** 屬性之作業的呼叫，以及呼叫作業 (*等* 冪運算) 不具 **\[ 等冪 \]** 屬性 (*非等* 冪的作業) 。</span><span class="sxs-lookup"><span data-stu-id="646d1-124">RPC supports two types of remote call semantics: calls to operations with the **\[idempotent\]** attribute and calls to operations (*idempotent* operations) without the **\[idempotent\]** attribute (*non-idempotent* operations).</span></span> <span data-ttu-id="646d1-125">等冪運算可以執行一次以上，而且不會有任何不良影響。</span><span class="sxs-lookup"><span data-stu-id="646d1-125">An idempotent operation can be carried out more than once with no ill effect.</span></span> <span data-ttu-id="646d1-126">相反地，無法執行一次非等冪運算，因為它會每次都會傳回不同的結果，或因為它會修改某些狀態。</span><span class="sxs-lookup"><span data-stu-id="646d1-126">Conversely, a non-idempotent operation cannot be executed more than once because it will either return different results each time or because it modifies some state.</span></span>

<span data-ttu-id="646d1-127">若要確保在呼叫未完成時，會自動重新執行程式，請使用 **\[ 等冪 \]** 屬性。</span><span class="sxs-lookup"><span data-stu-id="646d1-127">To ensure that a procedure is automatically re-executed if the call does not complete, use the **\[idempotent\]** attribute.</span></span> <span data-ttu-id="646d1-128">如果 **\[ 等冪 \]**、 **\[** [**廣播**](broadcast.md) **\]** 或 **\[** [**可能**](maybe.md)的 **\]** 屬性不存在，則此程式預設會使用非等冪的語法。</span><span class="sxs-lookup"><span data-stu-id="646d1-128">If the **\[idempotent\]**, **\[**[**broadcast**](broadcast.md)**\]**, or **\[**[**maybe**](maybe.md)**\]** attributes are not present, the procedure will use non-idempotent semantics by default.</span></span> <span data-ttu-id="646d1-129">在此情況下，作業只會執行一次。</span><span class="sxs-lookup"><span data-stu-id="646d1-129">In this case, the operation is executed only once.</span></span>

## <a name="see-also"></a><span data-ttu-id="646d1-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="646d1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="646d1-131">**廣播**</span><span class="sxs-lookup"><span data-stu-id="646d1-131">**broadcast**</span></span>](broadcast.md)
</dt> <dt>

[<span data-ttu-id="646d1-132"> (IDL) 檔案的介面定義</span><span class="sxs-lookup"><span data-stu-id="646d1-132">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="646d1-133">**也許**</span><span class="sxs-lookup"><span data-stu-id="646d1-133">**maybe**</span></span>](maybe.md)
</dt> </dl>

 

 




