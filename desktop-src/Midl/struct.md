---
title: struct 屬性
description: Struct 關鍵字用於結構類型規範中。
ms.assetid: 89e18f0e-185a-408e-812d-3d11f228b473
keywords:
- struct 屬性 MIDL
topic_type:
- apiref
api_name:
- struct
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5c97ca9a2dbbfeddc5416b517e85e0926434c5d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106976336"
---
# <a name="struct-attribute"></a><span data-ttu-id="69b2a-104">struct 屬性</span><span class="sxs-lookup"><span data-stu-id="69b2a-104">struct attribute</span></span>

<span data-ttu-id="69b2a-105">**Struct** 關鍵字用於結構類型規範中。</span><span class="sxs-lookup"><span data-stu-id="69b2a-105">The **struct** keyword is used in a structure type specifier.</span></span>

``` syntax
struct [[ struct-tag ]] 
{
  [[ [ field-attribute-list ] ]] type-specifier declarator-list;
    ...
};
```

## <a name="parameters"></a><span data-ttu-id="69b2a-106">參數</span><span class="sxs-lookup"><span data-stu-id="69b2a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69b2a-107">*結構標記*</span><span class="sxs-lookup"><span data-stu-id="69b2a-107">*struct-tag*</span></span> 
</dt> <dd>

<span data-ttu-id="69b2a-108">指定結構的選擇性標記。</span><span class="sxs-lookup"><span data-stu-id="69b2a-108">Specifies an optional tag for the structure.</span></span>

</dd> <dt>

<span data-ttu-id="69b2a-109">*欄位屬性清單*</span><span class="sxs-lookup"><span data-stu-id="69b2a-109">*field-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="69b2a-110">指定套用至結構成員的零或多個欄位屬性。</span><span class="sxs-lookup"><span data-stu-id="69b2a-110">Specifies zero or more field attributes that apply to the structure member.</span></span> <span data-ttu-id="69b2a-111">有效的欄位屬性包括 **\[** [**first \_**](first-is.md) **\]** 、 **\[** [**last \_**](last-is.md) **\]** 、 **\[** [**length、 \_ length**](length-is.md) **\]** 、 **\[** [**max \_ 為**](max-is.md) **\]** 和 **\[** [**size、 \_**](size-is.md) **\]** usage 屬性 **\[** [**字串**](string.md) **\]** 和 **\[** [**ignore**](ignore.md)、 **\]** 指標屬性 **\[** [**ref**](ref.md) **\]** 、 **\[** [**unique**](unique.md) **\]** 或 **\[** [**ptr**](ptr.md) **\]** ; 以及 union 屬性 **\[** [**參數 \_ 類型**](switch-type.md) **\]** 。</span><span class="sxs-lookup"><span data-stu-id="69b2a-111">Valid field attributes include **\[**[**first\_is**](first-is.md)**\]**, **\[**[**last\_is**](last-is.md)**\]**, **\[**[**length\_is**](length-is.md)**\]**, **\[**[**max\_is**](max-is.md)**\]**, and **\[**[**size\_is**](size-is.md)**\]**; the usage attributes **\[**[**string**](string.md)**\]** and **\[**[**ignore**](ignore.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the union attribute **\[**[**switch\_type**](switch-type.md)**\]**.</span></span> <span data-ttu-id="69b2a-112">以逗號分隔多個欄位屬性。</span><span class="sxs-lookup"><span data-stu-id="69b2a-112">Separate multiple field attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="69b2a-113">*類型規範*</span><span class="sxs-lookup"><span data-stu-id="69b2a-113">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="69b2a-114">指定 [基底類型](midl-base-types.md)、 **結構**、 [**等**](union.md)位或 [**列舉**](enum.md) 類型或類型識別碼。</span><span class="sxs-lookup"><span data-stu-id="69b2a-114">Specifies a [base type](midl-base-types.md), **struct**, [**union**](union.md), or [**enum**](enum.md) type or type identifier.</span></span> <span data-ttu-id="69b2a-115">選擇性的儲存規格可以在 *類型* 規範之前。</span><span class="sxs-lookup"><span data-stu-id="69b2a-115">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="69b2a-116">*宣告子清單*</span><span class="sxs-lookup"><span data-stu-id="69b2a-116">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="69b2a-117">指定一或多個標準 C 宣告子，例如識別碼、指標宣告子和陣列宣告子。</span><span class="sxs-lookup"><span data-stu-id="69b2a-117">Specifies one or more standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="69b2a-118">在遠端程序呼叫中傳輸的結構中，不允許 (函式宣告子和位欄位宣告。</span><span class="sxs-lookup"><span data-stu-id="69b2a-118">(Function declarators and bit-field declarations are not allowed in structures that are transmitted in remote procedure calls.</span></span> <span data-ttu-id="69b2a-119">未傳輸的結構中允許這些宣告子。 ) 以逗號分隔多個宣告子。</span><span class="sxs-lookup"><span data-stu-id="69b2a-119">These declarators are allowed in structures that are not transmitted.) Separate multiple declarators with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="69b2a-120">備註</span><span class="sxs-lookup"><span data-stu-id="69b2a-120">Remarks</span></span>

<span data-ttu-id="69b2a-121">IDL 結構類型規範（ **struct**）與標準 C 類型規範的差異如下：</span><span class="sxs-lookup"><span data-stu-id="69b2a-121">The IDL structure type specifier, **struct**, differs from the standard C type specifier in the following ways:</span></span>

-   <span data-ttu-id="69b2a-122">每個結構成員都可以與選擇性欄位屬性相關聯，這些屬性會描述該結構成員的特性，以供遠端程序呼叫之用。</span><span class="sxs-lookup"><span data-stu-id="69b2a-122">Each structure member can be associated with optional field attributes that describe characteristics of that structure member for the purposes of a remote procedure call.</span></span>
-   <span data-ttu-id="69b2a-123">在遠端程序呼叫中使用的結構中不允許使用位欄位和函數宣告子。</span><span class="sxs-lookup"><span data-stu-id="69b2a-123">Bit fields and function declarators are not allowed in structures that are used in remote procedure calls.</span></span> <span data-ttu-id="69b2a-124">只有當結構不是在網路上傳輸時，才能使用這些標準 C 宣告子結構。</span><span class="sxs-lookup"><span data-stu-id="69b2a-124">These standard C declarator constructs can be used only if the structure is not transmitted on the network.</span></span>

<span data-ttu-id="69b2a-125">結構的形狀在各平臺之間必須相同，以確保互連能力。</span><span class="sxs-lookup"><span data-stu-id="69b2a-125">The shape of structures must be the same across platforms to ensure interconnectivity.</span></span>

## <a name="examples"></a><span data-ttu-id="69b2a-126">範例</span><span class="sxs-lookup"><span data-stu-id="69b2a-126">Examples</span></span>

``` syntax
typedef struct _PITCHER_RECORD_TYPE 
{ 
    short flag; 
    [switch_is(flag)] union PITCHER_STATISTICS_TYPE p; 
} PITCHER_RECORD_TYPE;
```

## <a name="see-also"></a><span data-ttu-id="69b2a-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="69b2a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69b2a-128">**陣 列**</span><span class="sxs-lookup"><span data-stu-id="69b2a-128">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="69b2a-129">陣列和指標</span><span class="sxs-lookup"><span data-stu-id="69b2a-129">Arrays and Pointers</span></span>](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[<span data-ttu-id="69b2a-130">陣列和 Sized-Pointer 屬性</span><span class="sxs-lookup"><span data-stu-id="69b2a-130">Array and Sized-Pointer Attributes</span></span>](array-and-sized-pointer-attributes.md)
</dt> <dt>

[<span data-ttu-id="69b2a-131">MIDL 基底類型</span><span class="sxs-lookup"><span data-stu-id="69b2a-131">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="69b2a-132">**/c \_ ext**</span><span class="sxs-lookup"><span data-stu-id="69b2a-132">**/c\_ext**</span></span>](-c-ext.md)
</dt> <dt>

[<span data-ttu-id="69b2a-133">**內容 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="69b2a-133">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="69b2a-134">**枚舉**</span><span class="sxs-lookup"><span data-stu-id="69b2a-134">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="69b2a-135">**第一個 \_ 是**</span><span class="sxs-lookup"><span data-stu-id="69b2a-135">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="69b2a-136"> (IDL) 檔案的介面定義</span><span class="sxs-lookup"><span data-stu-id="69b2a-136">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="69b2a-137">**忽略**</span><span class="sxs-lookup"><span data-stu-id="69b2a-137">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="69b2a-138">**last \_**</span><span class="sxs-lookup"><span data-stu-id="69b2a-138">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="69b2a-139">**長度 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="69b2a-139">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="69b2a-140">**最大值 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="69b2a-140">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="69b2a-141">**/osf**</span><span class="sxs-lookup"><span data-stu-id="69b2a-141">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="69b2a-142">**ptr**</span><span class="sxs-lookup"><span data-stu-id="69b2a-142">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="69b2a-143">**ref**</span><span class="sxs-lookup"><span data-stu-id="69b2a-143">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="69b2a-144">**大小 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="69b2a-144">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="69b2a-145">**字串**</span><span class="sxs-lookup"><span data-stu-id="69b2a-145">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="69b2a-146">**切換 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="69b2a-146">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="69b2a-147">**聯盟**</span><span class="sxs-lookup"><span data-stu-id="69b2a-147">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="69b2a-148">**獨特**</span><span class="sxs-lookup"><span data-stu-id="69b2a-148">**unique**</span></span>](unique.md)
</dt> </dl>

 

 