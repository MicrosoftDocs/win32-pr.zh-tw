---
title: type_strict_coNtext_handle 屬性
description: 在 ACF 檔案中，使用 \ 類型 \_ strict \_ 內容 \_ 控制碼 \ 來設定內容控制碼的限制。
ms.assetid: b67caad2-e87d-4eba-8555-8f347aadd515
keywords:
- type_strict_coNtext_handle 屬性 MIDL
topic_type:
- apiref
api_name:
- type_strict_context_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e16c9ae74d618b1b0cafef2c5bf618085d79284
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104462981"
---
# <a name="type_strict_context_handle-attribute"></a><span data-ttu-id="0c370-104">輸入 \_ strict \_ 內容 \_ 控制碼屬性</span><span class="sxs-lookup"><span data-stu-id="0c370-104">type\_strict\_context\_handle attribute</span></span>

<span data-ttu-id="0c370-105">在 ACF 檔案中使用 **\[ 類型 \_ strict \_ 內容 \_ 控制碼 \]** ，以設定內容控制碼的限制。</span><span class="sxs-lookup"><span data-stu-id="0c370-105">Use the **\[type\_strict\_context\_handle\]** in an ACF file to set restrictions on context handles.</span></span>

``` syntax
[ 
    type_strict_context_handle 
    [, interface-attribute-list] 
] 
interface interface-name
{
    interface-definition-statements
}
```

## <a name="parameters"></a><span data-ttu-id="0c370-106">參數</span><span class="sxs-lookup"><span data-stu-id="0c370-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c370-107">*介面屬性清單*</span><span class="sxs-lookup"><span data-stu-id="0c370-107">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="0c370-108">適用于整個介面的其他 ACF 屬性。</span><span class="sxs-lookup"><span data-stu-id="0c370-108">Other ACF attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="0c370-109">有效的屬性 [**包括 \_ 自動控制碼**](auto-handle.md)、 [**隱含 \_ 控制碼**](implicit-handle.md)、 [**明確 \_ 控制碼**](explicit-handle.md)和 [**優化**](optimize.md)、程式 [**代碼**](code.md)或 [**了 nocode**](nocode.md)。</span><span class="sxs-lookup"><span data-stu-id="0c370-109">Valid attributes include [**auto\_handle**](auto-handle.md), [**implicit\_handle**](implicit-handle.md), [**explicit\_handle**](explicit-handle.md), and [**optimize**](optimize.md), [**code**](code.md), or [**nocode**](nocode.md).</span></span> <span data-ttu-id="0c370-110">以逗號分隔多個屬性。</span><span class="sxs-lookup"><span data-stu-id="0c370-110">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="0c370-111">*介面-名稱*</span><span class="sxs-lookup"><span data-stu-id="0c370-111">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="0c370-112">介面的名稱。</span><span class="sxs-lookup"><span data-stu-id="0c370-112">The name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="0c370-113">*介面定義語句*</span><span class="sxs-lookup"><span data-stu-id="0c370-113">*interface-definition-statements*</span></span> 
</dt> <dd>

<span data-ttu-id="0c370-114">定義 [**介面**](interface.md)元素的一或多個 MIDL 語句。</span><span class="sxs-lookup"><span data-stu-id="0c370-114">One or more MIDL statements that define the elements of the [**interface**](interface.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0c370-115">備註</span><span class="sxs-lookup"><span data-stu-id="0c370-115">Remarks</span></span>

<span data-ttu-id="0c370-116">若要使用這個屬性，在執行 midl.exe 時，必須將-target 旗標設為 NT60 (或更高的) 。</span><span class="sxs-lookup"><span data-stu-id="0c370-116">In order to use this attribute, the -target flag must be set to NT60 (or higher) when running midl.exe.</span></span>

<span data-ttu-id="0c370-117">\[型別 \_ strict \_ 內容 \_ 控制碼 \] 是 \[ strict \_ 內容 \_ 控制碼的功能超集合 \] 。</span><span class="sxs-lookup"><span data-stu-id="0c370-117">\[type\_strict\_context\_handle\] is a functional superset of \[strict\_context\_handle\].</span></span> <span data-ttu-id="0c370-118">在 \[ strict \_ 內容 \_ 控制碼中 \] ，控制碼的型別識別碼一律為0，而在 \[ 型別 \_ STRICT \_ 內容 \_ 控制碼中 \] ，MIDL 編譯器會指派唯一的型別識別碼。</span><span class="sxs-lookup"><span data-stu-id="0c370-118">In \[strict\_context\_handle\], the type ID of the handle is always 0; in \[type\_strict\_context\_handle\], a unique type ID is assigned by the MIDL compiler.</span></span>

<span data-ttu-id="0c370-119">建議使用 \[ 類型 \_ strict \_ 內容 \_ 控制碼， \] 而不是 \[ strict \_ 內容 \_ 控制碼 \] 。</span><span class="sxs-lookup"><span data-stu-id="0c370-119">It is recommended to use \[type\_strict\_context\_handle\] rather than \[strict\_context\_handle\].</span></span> <span data-ttu-id="0c370-120">內容控制碼預設不會與特定類型相關聯。</span><span class="sxs-lookup"><span data-stu-id="0c370-120">Context handles are not associated with a specific type by default.</span></span> <span data-ttu-id="0c370-121">在相同的進程中使用多種類型的內容控制碼時，惡意用戶端可能會傳遞內容控制碼來取代另一個，以產生不想要的結果。</span><span class="sxs-lookup"><span data-stu-id="0c370-121">When multiple types of context handles are used in the same process, it is possible for a malicious client to pass a context handle in place of another to produce undesirable results.</span></span> <span data-ttu-id="0c370-122">使用 \[ 類型 \_ strict \_ 內容 \_ 控制碼 \] 可讓應用程式強制執行內容控制碼類型一致性，並防止任何不相符的內容控制碼類型使用方式。</span><span class="sxs-lookup"><span data-stu-id="0c370-122">The use of \[type\_strict\_context\_handle\] allows applications to enforce context handle type consistency and prevent any mismatched context handle type usage.</span></span>

<span data-ttu-id="0c370-123">具有型別 strict 內容控制碼之屬性的內容控制碼， \[ \_ \_ \_ \] 也不能以 \[ strict 內容控制碼進行屬性化 \_ \_ \] 。</span><span class="sxs-lookup"><span data-stu-id="0c370-123">A context handle attributed with \[type\_strict\_context\_handle\] cannot also be attributed with \[strict\_context\_handle\].</span></span>

## <a name="see-also"></a><span data-ttu-id="0c370-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0c370-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c370-125">應用程式佈建檔 (ACF) </span><span class="sxs-lookup"><span data-stu-id="0c370-125">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="0c370-126">**代碼**</span><span class="sxs-lookup"><span data-stu-id="0c370-126">**code**</span></span>](code.md)
</dt> <dt>

[<span data-ttu-id="0c370-127">內容控制碼</span><span class="sxs-lookup"><span data-stu-id="0c370-127">Context Handles</span></span>](/windows/desktop/Rpc/context-handles)
</dt> <dt>

[<span data-ttu-id="0c370-128">**內容 \_ 控制碼 \_ 序列化**</span><span class="sxs-lookup"><span data-stu-id="0c370-128">**context\_handle\_serialize**</span></span>](context-handle-serialize.md)
</dt> <dt>

[<span data-ttu-id="0c370-129">**內容 \_ 控制碼 \_ noserialize**</span><span class="sxs-lookup"><span data-stu-id="0c370-129">**context\_handle\_noserialize**</span></span>](context-handle-noserialize.md)
</dt> <dt>

[<span data-ttu-id="0c370-130">**明確 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="0c370-130">**explicit\_handle**</span></span>](explicit-handle.md)
</dt> <dt>

[<span data-ttu-id="0c370-131">**隱含 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="0c370-131">**implicit\_handle**</span></span>](implicit-handle.md)
</dt> <dt>

[<span data-ttu-id="0c370-132">**了 nocode**</span><span class="sxs-lookup"><span data-stu-id="0c370-132">**nocode**</span></span>](nocode.md)
</dt> <dt>

[<span data-ttu-id="0c370-133">**優化**</span><span class="sxs-lookup"><span data-stu-id="0c370-133">**optimize**</span></span>](optimize.md)
</dt> <dt>

[<span data-ttu-id="0c370-134">strict \_ 內容 \_ 控制碼</span><span class="sxs-lookup"><span data-stu-id="0c370-134">strict\_context\_handle</span></span>](strict-context-handle.md)
</dt> </dl>

 

 