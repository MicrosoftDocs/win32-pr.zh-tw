---
title: interface 屬性
description: Interface 關鍵字會指定介面的名稱。 IDL 檔案和 ACF 中都必須提供介面名稱。
ms.assetid: 239b782e-57de-493c-b2f4-310d1859a9ae
keywords:
- 介面屬性 MIDL
topic_type:
- apiref
api_name:
- interface
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 852c29b2ba7b43e9d8b15863e60db8ad2fbde33f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842156"
---
# <a name="interface-attribute"></a><span data-ttu-id="3d5e6-105">interface 屬性</span><span class="sxs-lookup"><span data-stu-id="3d5e6-105">interface attribute</span></span>

<span data-ttu-id="3d5e6-106">**Interface** 關鍵字會指定介面的名稱。</span><span class="sxs-lookup"><span data-stu-id="3d5e6-106">The **interface** keyword specifies the name of the interface.</span></span> <span data-ttu-id="3d5e6-107">IDL 檔案和 ACF 中都必須提供介面名稱。</span><span class="sxs-lookup"><span data-stu-id="3d5e6-107">The interface name must be provided in both the IDL file and the ACF.</span></span>

``` syntax
[ 
    interface-attribute-list 
] 
interface interface-name [ : base-interface ]
{
}

typedef interface interface-name declarator-list
```

## <a name="parameters"></a><span data-ttu-id="3d5e6-108">參數</span><span class="sxs-lookup"><span data-stu-id="3d5e6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d5e6-109">*介面屬性清單*</span><span class="sxs-lookup"><span data-stu-id="3d5e6-109">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="3d5e6-110">指定套用至整個介面的屬性。</span><span class="sxs-lookup"><span data-stu-id="3d5e6-110">Specifies attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="3d5e6-111">IDL 檔案的有效介面屬性包括 **\[** [**endpoint**](endpoint.md) **\]** 、 **\[** [**local**](local.md) **\]** 、 **\[** [**object**](object.md) **\]** 、 **\[** [**指標 \_ default**](pointer-default.md) **\]** 、 **\[** [**uuid**](uuid.md) **\]** 和 **\[** [**version**](version.md) **\]** 。</span><span class="sxs-lookup"><span data-stu-id="3d5e6-111">Valid interface attributes for an IDL file include **\[**[**endpoint**](endpoint.md)**\]**, **\[**[**local**](local.md)**\]**, **\[**[**object**](object.md)**\]**, **\[**[**pointer\_default**](pointer-default.md)**\]**, **\[**[**uuid**](uuid.md)**\]**, and **\[**[**version**](version.md)**\]**.</span></span> <span data-ttu-id="3d5e6-112">ACF 的有效介面屬性包括 **\[** [**編碼**](encode.md) **\]** 、解碼 **\[** [](decode.md) **\]** 、 **\[** [**自動 \_ 處理**](auto-handle.md) **\]** 或 **\[** [**隱含 \_ 控制碼**](implicit-handle.md) **\]** ，以及程式 **\[** [**代碼**](code.md) **\]** 或 **\[** [**了 nocode**](nocode.md) **\]** 。</span><span class="sxs-lookup"><span data-stu-id="3d5e6-112">Valid interface attributes for an ACF include **\[**[**encode**](encode.md)**\]**, **\[**[**decode**](decode.md)**\]**, either **\[**[**auto\_handle**](auto-handle.md)**\]** or **\[**[**implicit\_handle**](implicit-handle.md)**\]**, and either **\[**[**code**](code.md)**\]** or **\[**[**nocode**](nocode.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="3d5e6-113">*介面-名稱*</span><span class="sxs-lookup"><span data-stu-id="3d5e6-113">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="3d5e6-114">指定介面的名稱。</span><span class="sxs-lookup"><span data-stu-id="3d5e6-114">Specifies the name of the interface.</span></span> <span data-ttu-id="3d5e6-115">介面名稱必須是唯一的名稱，且開頭必須是字母或底線字元。</span><span class="sxs-lookup"><span data-stu-id="3d5e6-115">The interface name must be a unique name and must start with an alphabetic or underscore character.</span></span>

</dd> <dt>

<span data-ttu-id="3d5e6-116">*基底介面*</span><span class="sxs-lookup"><span data-stu-id="3d5e6-116">*base-interface*</span></span> 
</dt> <dd>

<span data-ttu-id="3d5e6-117">指定此衍生介面繼承成員函式、狀態碼和介面屬性之介面的名稱。</span><span class="sxs-lookup"><span data-stu-id="3d5e6-117">Specifies the name of an interface from which this derived interface inherits member functions, status codes, and interface attributes.</span></span> <span data-ttu-id="3d5e6-118">衍生介面不會繼承型別定義。</span><span class="sxs-lookup"><span data-stu-id="3d5e6-118">The derived interface does not inherit type definitions.</span></span> <span data-ttu-id="3d5e6-119">若要這樣做，請使用 [**import**](import.md) 關鍵字匯入基底介面的 IDL 檔案。</span><span class="sxs-lookup"><span data-stu-id="3d5e6-119">To do this, use the [**import**](import.md) keyword to import the IDL file of the base interface.</span></span>

</dd> <dt>

<span data-ttu-id="3d5e6-120">*宣告子清單*</span><span class="sxs-lookup"><span data-stu-id="3d5e6-120">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="3d5e6-121">指定標準的 C 宣告子，例如識別碼、指標宣告子，以及陣列宣告子。</span><span class="sxs-lookup"><span data-stu-id="3d5e6-121">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="3d5e6-122">如需詳細 [**資訊，請**](arrays-1.md)參閱 [陣列和 Sized-Pointer 屬性](array-and-sized-pointer-attributes.md)、陣列和 [陣列和指標](/windows/desktop/Rpc/arrays-and-pointers)。</span><span class="sxs-lookup"><span data-stu-id="3d5e6-122">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md)., and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="3d5e6-123">宣告子清單包含一或多個宣告子， *並* 以逗號分隔。</span><span class="sxs-lookup"><span data-stu-id="3d5e6-123">The *declarator-list* consists of one or more declarators, separated by commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3d5e6-124">備註</span><span class="sxs-lookup"><span data-stu-id="3d5e6-124">Remarks</span></span>

<span data-ttu-id="3d5e6-125">IDL 檔案和 ACF 中的介面名稱必須相同，除非您使用 MIDL 編譯器參數 [**/acf**](-acf.md)。</span><span class="sxs-lookup"><span data-stu-id="3d5e6-125">The interface names in the IDL file and ACF must be the same, except when you use the MIDL compiler switch [**/acf**](-acf.md).</span></span>

<span data-ttu-id="3d5e6-126">介面名稱會形成介面控制碼資料結構名稱的第一個部分，這是 RPC 執行時間函數的參數。</span><span class="sxs-lookup"><span data-stu-id="3d5e6-126">The interface name forms the first part of the name of interface-handle data structures that are parameters to the RPC run-time functions.</span></span> <span data-ttu-id="3d5e6-127">如需詳細資訊，請參閱 [**RPC \_ IF \_ 控制碼**](/windows/desktop/Rpc/rpc-if-handle)。</span><span class="sxs-lookup"><span data-stu-id="3d5e6-127">For more information, see [**RPC\_IF\_HANDLE**](/windows/desktop/Rpc/rpc-if-handle).</span></span>

<span data-ttu-id="3d5e6-128">如果介面標頭包含 **\[** [](object.md) **\]** 用來指出 COM 介面的物件屬性，它也必須包含 **\[** [**uuid**](uuid.md) **\]** 屬性，而且必須指定從中衍生的基底 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="3d5e6-128">If the interface header includes the **\[**[**object**](object.md)**\]** attribute to indicate a COM interface, it must also include the **\[**[**uuid**](uuid.md)**\]** attribute and must specify the base COM interface from which it is derived.</span></span> <span data-ttu-id="3d5e6-129">如需 COM 介面的詳細資訊，請參閱 **\[** [**物件**](object.md) **\]** 。</span><span class="sxs-lookup"><span data-stu-id="3d5e6-129">For more information about COM interfaces, see **\[**[**object**](object.md)**\]**.</span></span>

<span data-ttu-id="3d5e6-130">您也可以使用 **interface** 關鍵字搭配 [**typedef**](typedef.md) 關鍵字來定義介面資料類型。</span><span class="sxs-lookup"><span data-stu-id="3d5e6-130">You can also use the **interface** keyword with the [**typedef**](typedef.md) keyword to define an interface data type.</span></span>

## <a name="examples"></a><span data-ttu-id="3d5e6-131">範例</span><span class="sxs-lookup"><span data-stu-id="3d5e6-131">Examples</span></span>

``` syntax
/* use of interface keyword in IDL file for an RPC interface */ 
[ 
    uuid (00000000-0000-0000-0000-000000000000), 
    version (1.0) 
] 
interface remote_if_2 
{  
    // Interface definition statements.
} 
 
/* use of interface keyword in ACF for an RPC interface */ 
[
    implicit_handle( handle_t xa_bhandle ) 
] 
interface remote_if_2 
{ 
    // Attribute configuration statements.
} 
 
/* use of interface keyword in IDL file for a COM interface */ 
[ 
    object, uuid (00000000-0000-0000-0000-000000000000) 
] 
interface IDerivedInterface : IBaseInterface 
{  
    import "base.idl" 
    Save(); 
} 
 
/* use of interface keyword to define an interface pointer type */ 
typedef interface IStorage *LPSTORAGE;
```

## <a name="see-also"></a><span data-ttu-id="3d5e6-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3d5e6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d5e6-133">應用程式佈建檔 (ACF) </span><span class="sxs-lookup"><span data-stu-id="3d5e6-133">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="3d5e6-134">**端點**</span><span class="sxs-lookup"><span data-stu-id="3d5e6-134">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="3d5e6-135"> (IDL) 檔案的介面定義</span><span class="sxs-lookup"><span data-stu-id="3d5e6-135">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="3d5e6-136">**當地**</span><span class="sxs-lookup"><span data-stu-id="3d5e6-136">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="3d5e6-137">**物件**</span><span class="sxs-lookup"><span data-stu-id="3d5e6-137">**object**</span></span>](object.md)
</dt> <dt>

[<span data-ttu-id="3d5e6-138">**指標 \_ 預設值**</span><span class="sxs-lookup"><span data-stu-id="3d5e6-138">**pointer\_default**</span></span>](pointer-default.md)
</dt> <dt>

[<span data-ttu-id="3d5e6-139">**RPC \_ IF \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="3d5e6-139">**RPC\_IF\_HANDLE**</span></span>](/windows/desktop/Rpc/rpc-if-handle)
</dt> <dt>

[<span data-ttu-id="3d5e6-140">**著**</span><span class="sxs-lookup"><span data-stu-id="3d5e6-140">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="3d5e6-141">**uuid**</span><span class="sxs-lookup"><span data-stu-id="3d5e6-141">**uuid**</span></span>](uuid.md)
</dt> <dt>

[<span data-ttu-id="3d5e6-142">**版本**</span><span class="sxs-lookup"><span data-stu-id="3d5e6-142">**version**</span></span>](version.md)
</dt> </dl>

 

 