---
title: typedef 屬性
description: IDL typedef 關鍵字允許與 C 語言 typedef 宣告非常類似的 typedef 宣告。
ms.assetid: 995a233e-0d07-4051-9f00-d1dc0b563f8f
keywords:
- typedef 屬性 MIDL
topic_type:
- apiref
api_name:
- typedef
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecfce98e5a83f8d2a5e2499a5ceceba755e68f2c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103681818"
---
# <a name="typedef-attribute"></a><span data-ttu-id="e3d0a-104">typedef 屬性</span><span class="sxs-lookup"><span data-stu-id="e3d0a-104">typedef attribute</span></span>

<span data-ttu-id="e3d0a-105">IDL **typedef** 關鍵字允許與 C 語言 **typedef** 宣告非常類似的 **typedef** 宣告。</span><span class="sxs-lookup"><span data-stu-id="e3d0a-105">The IDL **typedef** keyword allows **typedef** declarations that are very similar to C-language **typedef** declarations.</span></span>

``` syntax
/* IDL file typedef syntax */
typedef [[ [ idl-type-attribute-list ] ]] type-specifier declarator-list;

/* ACF typedef syntax */
typedef [ acf-type-attribute-list ] typename;
```

## <a name="parameters"></a><span data-ttu-id="e3d0a-106">參數</span><span class="sxs-lookup"><span data-stu-id="e3d0a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3d0a-107">*idl-類型-屬性清單*</span><span class="sxs-lookup"><span data-stu-id="e3d0a-107">*idl-type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="e3d0a-108">指定套用至類型的一或多個屬性。</span><span class="sxs-lookup"><span data-stu-id="e3d0a-108">Specifies one or more attributes that apply to the type.</span></span> <span data-ttu-id="e3d0a-109">IDL 檔案中的有效類型屬性包括 **\[** [**控制碼**](handle.md) **\]** 、 **\[** [**切換 \_ 類型**](switch-type.md) **\]** 、 **\[** [**傳輸 \_ 為**](transmit-as.md) **\]** ; 指標屬性 **\[** [**ref**](ref.md) **\]** 、 **\[** [**unique**](unique.md) **\]** 或 **\[** [**ptr**](ptr.md) **\]** ; 以及使用方式屬性 **\[** [**內容 \_ 控制碼**](context-handle.md) **\]** 、 **\[** [**字串**](string.md)和 **\]** **\[** [**忽略**](ignore.md) **\]** 。</span><span class="sxs-lookup"><span data-stu-id="e3d0a-109">Valid type attributes in an IDL file include **\[**[**handle**](handle.md)**\]**, **\[**[**switch\_type**](switch-type.md)**\]**, **\[**[**transmit\_as**](transmit-as.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**context\_handle**](context-handle.md)**\]**, **\[**[**string**](string.md)**\]**, and **\[**[**ignore**](ignore.md)**\]**.</span></span> <span data-ttu-id="e3d0a-110">以逗號分隔多個屬性。</span><span class="sxs-lookup"><span data-stu-id="e3d0a-110">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="e3d0a-111">*類型規範*</span><span class="sxs-lookup"><span data-stu-id="e3d0a-111">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="e3d0a-112">指定 [基底類型](midl-base-types.md)、[**結構**](struct.md)、[**等位、**](union.md)[**列舉**](enum.md)類型或類型識別碼。</span><span class="sxs-lookup"><span data-stu-id="e3d0a-112">Specifies a [base type](midl-base-types.md), [**struct**](struct.md), [**union**](union.md), [**enum**](enum.md) type, or type identifier.</span></span> <span data-ttu-id="e3d0a-113">選擇性的儲存規格可以在 *類型* 規範之前。</span><span class="sxs-lookup"><span data-stu-id="e3d0a-113">An optional storage specification can precede *type-specifier*.</span></span> <span data-ttu-id="e3d0a-114">[**Const**](const.md)關鍵字可以在 *類型規範* 之前。</span><span class="sxs-lookup"><span data-stu-id="e3d0a-114">The [**const**](const.md) keyword can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="e3d0a-115">*宣告子清單*</span><span class="sxs-lookup"><span data-stu-id="e3d0a-115">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="e3d0a-116">指定標準 MIDL 宣告子，例如識別碼、指標宣告子，以及陣列宣告子。</span><span class="sxs-lookup"><span data-stu-id="e3d0a-116">Specifies standard MIDL declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="e3d0a-117">如需詳細資訊，請參閱 [陣列和 Sized-Pointer 屬性](array-and-sized-pointer-attributes.md) [**、陣列、陣列和**](arrays-1.md)[指標](/windows/desktop/Rpc/arrays-and-pointers)。</span><span class="sxs-lookup"><span data-stu-id="e3d0a-117">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="e3d0a-118">宣告子清單包含一或多個宣告子， *並* 以逗號分隔。</span><span class="sxs-lookup"><span data-stu-id="e3d0a-118">The *declarator-list* consists of one or more declarators, separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="e3d0a-119">*acf-type-attribute-list*</span><span class="sxs-lookup"><span data-stu-id="e3d0a-119">*acf-type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="e3d0a-120">指定套用至類型的一或多個屬性。</span><span class="sxs-lookup"><span data-stu-id="e3d0a-120">Specifies one or more attributes that apply to the type.</span></span> <span data-ttu-id="e3d0a-121">ACF 中的有效類型屬性包括 **\[** [**配置**](allocate.md) **\]** 、 **\[** [**編碼**](encode.md) **\]** 和解碼 **\[** [](decode.md) **\]** 。</span><span class="sxs-lookup"><span data-stu-id="e3d0a-121">Valid type attributes in an ACF include **\[**[**allocate**](allocate.md)**\]**, **\[**[**encode**](encode.md)**\]**, and **\[**[**decode**](decode.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="e3d0a-122">*typename*</span><span class="sxs-lookup"><span data-stu-id="e3d0a-122">*typename*</span></span> 
</dt> <dd>

<span data-ttu-id="e3d0a-123">指定 IDL 檔案中定義的類型。</span><span class="sxs-lookup"><span data-stu-id="e3d0a-123">Specifies a type defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e3d0a-124">備註</span><span class="sxs-lookup"><span data-stu-id="e3d0a-124">Remarks</span></span>

<span data-ttu-id="e3d0a-125">IDL **typedef** 宣告已增強，可讓您將類型屬性與定義的類型產生關聯。</span><span class="sxs-lookup"><span data-stu-id="e3d0a-125">The IDL **typedef** declaration is augmented to allow you to associate type attributes with the defined types.</span></span> <span data-ttu-id="e3d0a-126">有效的型別屬性包括 **\[** [**控制碼**](handle.md) **\]** 、 **\[** [**切換 \_ 類型**](switch-type.md) **\]** 、 **\[** [**傳輸 \_ 為**](transmit-as.md) **\]** ; 指標屬性 **\[** [**ref**](ref.md) **\]** 、 **\[** [**unique**](unique.md) **\]** 或 **\[** [**ptr**](ptr.md) **\]** ; 以及使用方式屬性 **\[** [**內容 \_ 控制碼**](context-handle.md) **\]** 、 **\[** [**字串**](string.md) **\]** 和 **\[** [**略**](ignore.md)過 **\]** 。</span><span class="sxs-lookup"><span data-stu-id="e3d0a-126">Valid type attributes include **\[**[**handle**](handle.md)**\]**, **\[**[**switch\_type**](switch-type.md)**\]**, **\[**[**transmit\_as**](transmit-as.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**context\_handle**](context-handle.md)**\]**, **\[**[**string**](string.md)**\]**, and **\[**[**ignore**](ignore.md)**\]**.</span></span>

<span data-ttu-id="e3d0a-127">ACF 中的 **typedef** 關鍵字會將屬性套用至對應 IDL 檔案中所定義的類型。</span><span class="sxs-lookup"><span data-stu-id="e3d0a-127">The **typedef** keyword in an ACF applies attributes to types that are defined in the corresponding IDL file.</span></span> <span data-ttu-id="e3d0a-128">例如，[ [**配置**](allocate.md) 類型] 屬性可讓您自訂應用程式和存根的記憶體配置和解除配置。</span><span class="sxs-lookup"><span data-stu-id="e3d0a-128">For example, the [**allocate**](allocate.md) type attribute allows you to customize memory allocation and deallocation by both the application and the stubs.</span></span>

<span data-ttu-id="e3d0a-129">ACF **typedef** 語句會顯示為 ACF 主體的一部分。</span><span class="sxs-lookup"><span data-stu-id="e3d0a-129">The ACF **typedef** statement appears as part of the ACF body.</span></span> <span data-ttu-id="e3d0a-130">請注意，ACF **typedef** 語法與 IDL **Typedef** 語法和 C 語言 **typedef** 語法不同。</span><span class="sxs-lookup"><span data-stu-id="e3d0a-130">Note that the ACF **typedef** syntax is different from the IDL **typedef** syntax and the C-language **typedef** syntax.</span></span> <span data-ttu-id="e3d0a-131">ACF 中不會引進任何新的類型。</span><span class="sxs-lookup"><span data-stu-id="e3d0a-131">No new types can be introduced in the ACF.</span></span>

## <a name="see-also"></a><span data-ttu-id="e3d0a-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e3d0a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3d0a-133">應用程式佈建檔 (ACF) </span><span class="sxs-lookup"><span data-stu-id="e3d0a-133">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="e3d0a-134">**分配**</span><span class="sxs-lookup"><span data-stu-id="e3d0a-134">**allocate**</span></span>](allocate.md)
</dt> <dt>

[<span data-ttu-id="e3d0a-135">**陣 列**</span><span class="sxs-lookup"><span data-stu-id="e3d0a-135">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="e3d0a-136">**const**</span><span class="sxs-lookup"><span data-stu-id="e3d0a-136">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="e3d0a-137">**內容 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="e3d0a-137">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="e3d0a-138">**解碼**</span><span class="sxs-lookup"><span data-stu-id="e3d0a-138">**decode**</span></span>](decode.md)
</dt> <dt>

[<span data-ttu-id="e3d0a-139">**編碼**</span><span class="sxs-lookup"><span data-stu-id="e3d0a-139">**encode**</span></span>](encode.md)
</dt> <dt>

[<span data-ttu-id="e3d0a-140">**枚舉**</span><span class="sxs-lookup"><span data-stu-id="e3d0a-140">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="e3d0a-141">**處理**</span><span class="sxs-lookup"><span data-stu-id="e3d0a-141">**handle**</span></span>](handle.md)
</dt> <dt>

[<span data-ttu-id="e3d0a-142"> (IDL) 檔案的介面定義</span><span class="sxs-lookup"><span data-stu-id="e3d0a-142">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="e3d0a-143">**忽略**</span><span class="sxs-lookup"><span data-stu-id="e3d0a-143">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="e3d0a-144">**ptr**</span><span class="sxs-lookup"><span data-stu-id="e3d0a-144">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="e3d0a-145">**ref**</span><span class="sxs-lookup"><span data-stu-id="e3d0a-145">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="e3d0a-146">**字串**</span><span class="sxs-lookup"><span data-stu-id="e3d0a-146">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="e3d0a-147">**結構**</span><span class="sxs-lookup"><span data-stu-id="e3d0a-147">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="e3d0a-148">**切換 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="e3d0a-148">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="e3d0a-149">**傳輸 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="e3d0a-149">**transmit\_as**</span></span>](transmit-as.md)
</dt> <dt>

[<span data-ttu-id="e3d0a-150">**聯盟**</span><span class="sxs-lookup"><span data-stu-id="e3d0a-150">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="e3d0a-151">**獨特**</span><span class="sxs-lookup"><span data-stu-id="e3d0a-151">**unique**</span></span>](unique.md)
</dt> </dl>

 

 