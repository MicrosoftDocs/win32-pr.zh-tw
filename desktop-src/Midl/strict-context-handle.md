---
title: strict_coNtext_handle 屬性
description: '\ Strict \_ 內容 \_ 控制碼 \ ACF 屬性會設定內容控制碼的限制。'
ms.assetid: c34f9018-d519-4a75-ad6f-70d386a20817
keywords:
- strict_coNtext_handle 屬性 MIDL
topic_type:
- apiref
api_name:
- strict_context_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8e66fd0754ec82de2354983e10e23ffc6329569
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933113"
---
# <a name="strict_context_handle-attribute"></a><span data-ttu-id="73fb6-104">strict \_ 內容 \_ 控制碼屬性</span><span class="sxs-lookup"><span data-stu-id="73fb6-104">strict\_context\_handle attribute</span></span>

<span data-ttu-id="73fb6-105">**\[ Strict \_ 內容 \_ 控制碼 \]** ACF 屬性會設定內容控制碼的限制。</span><span class="sxs-lookup"><span data-stu-id="73fb6-105">The **\[strict\_context\_handle\]** ACF attribute sets restrictions on context handles.</span></span>

``` syntax
[ 
    strict_context_handle 
    [, interface-attribute-list] 
] 
interface interface-name
{
    interface-definition-statements
}
```

## <a name="parameters"></a><span data-ttu-id="73fb6-106">參數</span><span class="sxs-lookup"><span data-stu-id="73fb6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73fb6-107">*介面屬性清單*</span><span class="sxs-lookup"><span data-stu-id="73fb6-107">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="73fb6-108">適用于整個介面的其他 ACF 屬性。</span><span class="sxs-lookup"><span data-stu-id="73fb6-108">Other ACF attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="73fb6-109">有效的屬性 [**包括 \_ 自動控制碼**](auto-handle.md)、 [**隱含 \_ 控制碼**](implicit-handle.md)、 [**明確 \_ 控制碼**](explicit-handle.md)和 [**優化**](optimize.md)、程式 [**代碼**](code.md)或 [**了 nocode**](nocode.md)。</span><span class="sxs-lookup"><span data-stu-id="73fb6-109">Valid attributes include [**auto\_handle**](auto-handle.md), [**implicit\_handle**](implicit-handle.md), [**explicit\_handle**](explicit-handle.md), and [**optimize**](optimize.md), [**code**](code.md), or [**nocode**](nocode.md).</span></span> <span data-ttu-id="73fb6-110">以逗號分隔多個屬性。</span><span class="sxs-lookup"><span data-stu-id="73fb6-110">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="73fb6-111">*介面-名稱*</span><span class="sxs-lookup"><span data-stu-id="73fb6-111">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="73fb6-112">介面的名稱。</span><span class="sxs-lookup"><span data-stu-id="73fb6-112">The name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="73fb6-113">*介面定義語句*</span><span class="sxs-lookup"><span data-stu-id="73fb6-113">*interface-definition-statements*</span></span> 
</dt> <dd>

<span data-ttu-id="73fb6-114">定義 [**介面**](interface.md)元素的一或多個 MIDL 語句。</span><span class="sxs-lookup"><span data-stu-id="73fb6-114">One or more MIDL statements that define the elements of the [**interface**](interface.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="73fb6-115">備註</span><span class="sxs-lookup"><span data-stu-id="73fb6-115">Remarks</span></span>

<span data-ttu-id="73fb6-116">一般來說，當呼叫介面方法產生內容控制碼時，該控制碼會變成可供任何其他介面免費使用。</span><span class="sxs-lookup"><span data-stu-id="73fb6-116">Normally, when a call to an interface method generates a context handle, that handle becomes freely available to any other interface.</span></span> <span data-ttu-id="73fb6-117">當您使用 **\[ strict \_ 內容 \_ 控制碼 \]** 屬性時，您保證該介面中的方法只會接受從相同介面中的方法所建立的內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="73fb6-117">When you use the **\[strict\_context\_handle\]** attribute you guarantee that the methods in that interface will only accept context handles that were created by a method from the same interface.</span></span> <span data-ttu-id="73fb6-118">不使用 **\[ strict \_ 內容 \_ 控制碼 \]** 編譯的介面無法接受在以 **\[ strict \_ 內容 \_ 控制碼 \]** 編譯之介面上建立的內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="73fb6-118">Interfaces compiled without **\[strict\_context\_handle\]** cannot accept context handles created on interfaces compiled with **\[strict\_context\_handle\]**.</span></span>

## <a name="see-also"></a><span data-ttu-id="73fb6-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="73fb6-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73fb6-120">應用程式佈建檔 (ACF) </span><span class="sxs-lookup"><span data-stu-id="73fb6-120">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="73fb6-121">**代碼**</span><span class="sxs-lookup"><span data-stu-id="73fb6-121">**code**</span></span>](code.md)
</dt> <dt>

[<span data-ttu-id="73fb6-122">內容控制碼</span><span class="sxs-lookup"><span data-stu-id="73fb6-122">Context Handles</span></span>](/windows/desktop/Rpc/context-handles)
</dt> <dt>

[<span data-ttu-id="73fb6-123">**內容 \_ 控制碼 \_ 序列化**</span><span class="sxs-lookup"><span data-stu-id="73fb6-123">**context\_handle\_serialize**</span></span>](context-handle-serialize.md)
</dt> <dt>

[<span data-ttu-id="73fb6-124">**內容 \_ 控制碼 \_ noserialize**</span><span class="sxs-lookup"><span data-stu-id="73fb6-124">**context\_handle\_noserialize**</span></span>](context-handle-noserialize.md)
</dt> <dt>

[<span data-ttu-id="73fb6-125">**明確 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="73fb6-125">**explicit\_handle**</span></span>](explicit-handle.md)
</dt> <dt>

[<span data-ttu-id="73fb6-126">**隱含 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="73fb6-126">**implicit\_handle**</span></span>](implicit-handle.md)
</dt> <dt>

[<span data-ttu-id="73fb6-127">**了 nocode**</span><span class="sxs-lookup"><span data-stu-id="73fb6-127">**nocode**</span></span>](nocode.md)
</dt> <dt>

[<span data-ttu-id="73fb6-128">**優化**</span><span class="sxs-lookup"><span data-stu-id="73fb6-128">**optimize**</span></span>](optimize.md)
</dt> <dt>

[<span data-ttu-id="73fb6-129">輸入 \_ strict \_ 內容 \_ 控制碼</span><span class="sxs-lookup"><span data-stu-id="73fb6-129">type\_strict\_context\_handle</span></span>](type-strict-context-handle.md)
</dt> </dl>

 

 