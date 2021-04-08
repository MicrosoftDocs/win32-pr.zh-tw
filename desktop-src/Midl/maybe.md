---
title: 也許是屬性
description: 關鍵字 \ 可能會指出遠端程序呼叫不需要在每次呼叫時執行，而且用戶端不會預期回應。 請注意，\ 可能的 \ 通訊協定可確保不會傳遞，也不會完成呼叫。
ms.assetid: 163b9fd5-7dce-493e-95bc-63807f42a498
keywords:
- 可能是 MIDL 屬性
topic_type:
- apiref
api_name:
- maybe
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68704e19d421150444933d74f6b78fc5bada46f6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104022304"
---
# <a name="maybe-attribute"></a><span data-ttu-id="a7095-105">也許是屬性</span><span class="sxs-lookup"><span data-stu-id="a7095-105">maybe attribute</span></span>

<span data-ttu-id="a7095-106">關鍵字 **\[ 可能 \]** 指出遠端程序呼叫不需要在每次呼叫時執行，而且用戶端不會預期回應。</span><span class="sxs-lookup"><span data-stu-id="a7095-106">The keyword **\[maybe\]** indicates that the remote procedure call does not need to execute every time it is called and the client does not expect a response.</span></span> <span data-ttu-id="a7095-107">請注意， **\[ 可能 \]** 的通訊協定可確保未傳遞，也不會完成呼叫。</span><span class="sxs-lookup"><span data-stu-id="a7095-107">Note that the **\[maybe\]** protocol ensures neither delivery nor completion of the call.</span></span>

``` syntax
[
    interface-attribute-list
] 
interface interface-name 
{
    [maybe [, attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a><span data-ttu-id="a7095-108">參數</span><span class="sxs-lookup"><span data-stu-id="a7095-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7095-109">*介面屬性清單*</span><span class="sxs-lookup"><span data-stu-id="a7095-109">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="a7095-110">指定套用至整個介面的零或多個 IDL 屬性清單。</span><span class="sxs-lookup"><span data-stu-id="a7095-110">Specifies a list of zero or more IDL attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="a7095-111">當有兩個或多個介面屬性存在時，它們必須以逗號分隔。</span><span class="sxs-lookup"><span data-stu-id="a7095-111">When two or more interface attributes are present, they must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="a7095-112">*介面-名稱*</span><span class="sxs-lookup"><span data-stu-id="a7095-112">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="a7095-113">指定介面的名稱。</span><span class="sxs-lookup"><span data-stu-id="a7095-113">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="a7095-114">*屬性清單*</span><span class="sxs-lookup"><span data-stu-id="a7095-114">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="a7095-115">指定要套用至函數的其他屬性。</span><span class="sxs-lookup"><span data-stu-id="a7095-115">Specifies additional attributes to be applied to the function.</span></span> <span data-ttu-id="a7095-116">以逗號分隔多個屬性。</span><span class="sxs-lookup"><span data-stu-id="a7095-116">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="a7095-117">*returntype*</span><span class="sxs-lookup"><span data-stu-id="a7095-117">*returntype*</span></span> 
</dt> <dd>

<span data-ttu-id="a7095-118">指定函式的傳回型別。</span><span class="sxs-lookup"><span data-stu-id="a7095-118">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="a7095-119">*函數名稱*</span><span class="sxs-lookup"><span data-stu-id="a7095-119">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="a7095-120">指定 **\[ 可能 \]** 套用屬性之目標函數的名稱。</span><span class="sxs-lookup"><span data-stu-id="a7095-120">Specifies the name of the function to which the **\[maybe\]** attribute will be applied.</span></span>

</dd> <dt>

<span data-ttu-id="a7095-121">*params*</span><span class="sxs-lookup"><span data-stu-id="a7095-121">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="a7095-122">函數參數清單。</span><span class="sxs-lookup"><span data-stu-id="a7095-122">Function parameter list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a7095-123">備註</span><span class="sxs-lookup"><span data-stu-id="a7095-123">Remarks</span></span>

<span data-ttu-id="a7095-124">使用 **\[ 可能 \]** 屬性的呼叫不能包含輸出參數，而是隱含的 **\[** [**等冪**](idempotent.md) **\]** 呼叫。</span><span class="sxs-lookup"><span data-stu-id="a7095-124">A call with the **\[maybe\]** attribute cannot contain output parameters and is implicitly an **\[**[**idempotent**](idempotent.md)**\]** call.</span></span>

## <a name="see-also"></a><span data-ttu-id="a7095-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a7095-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7095-126">**廣播**</span><span class="sxs-lookup"><span data-stu-id="a7095-126">**broadcast**</span></span>](broadcast.md)
</dt> <dt>

[<span data-ttu-id="a7095-127">**idempotent**</span><span class="sxs-lookup"><span data-stu-id="a7095-127">**idempotent**</span></span>](idempotent.md)
</dt> <dt>

[<span data-ttu-id="a7095-128"> (IDL) 檔案的介面定義</span><span class="sxs-lookup"><span data-stu-id="a7095-128">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> </dl>

 

 




