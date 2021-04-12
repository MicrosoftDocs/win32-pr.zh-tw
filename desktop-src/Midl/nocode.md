---
title: 了 nocode 屬性
description: '\ 了 nocode \ 屬性用於 ACF 標頭或個別的函式，以防止產生用戶端 stub 程式碼。'
ms.assetid: d3b6e4c8-103c-4ea2-8748-11d844fdda97
keywords:
- 了 nocode 屬性 MIDL
topic_type:
- apiref
api_name:
- nocode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64f5138dc1794e9b2714e5f64762c1af17b47fb2
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312212"
---
# <a name="nocode-attribute"></a><span data-ttu-id="14baa-104">了 nocode 屬性</span><span class="sxs-lookup"><span data-stu-id="14baa-104">nocode attribute</span></span>

<span data-ttu-id="14baa-105">**\[ 了 nocode \]** 屬性可用於 ACF 標頭或個別的函式，以防止產生用戶端 stub 程式碼。</span><span class="sxs-lookup"><span data-stu-id="14baa-105">The **\[nocode\]** attribute is used in ACF headers or with individual functions to prevent the generation of client stub code.</span></span>

``` syntax
[ 
    nocode 
    [ , ACF-interface-attributes ] 
] 
interface interface-name
{
  [ include filename-list ; ]
  [ typedef [type-attribute-list] typename; ] 
  [ [ nocode [ , ACF-function-attributes ] ] function-name (
        [ ACF-parameter-attributes ] parameter-name ;
        ...);
  ]
    ...
}
```

## <a name="parameters"></a><span data-ttu-id="14baa-106">參數</span><span class="sxs-lookup"><span data-stu-id="14baa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14baa-107">*ACF-介面-屬性*</span><span class="sxs-lookup"><span data-stu-id="14baa-107">*ACF-interface-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="14baa-108">指定套用至整個介面的一或多個屬性清單。</span><span class="sxs-lookup"><span data-stu-id="14baa-108">Specifies a list of one or more attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="14baa-109">有效的屬性包括 **\[** [**auto \_ 控制碼**](auto-handle.md) **\]** 或 **\[** [**隱含 \_ 控制碼**](implicit-handle.md) **\]** ，以及程式 **\[** [**代碼**](code.md) **\]** 或 **\[ \] 了 nocode**。</span><span class="sxs-lookup"><span data-stu-id="14baa-109">Valid attributes include either **\[**[**auto\_handle**](auto-handle.md)**\]** or **\[**[**implicit\_handle**](implicit-handle.md)**\]** and either **\[**[**code**](code.md)**\]** or **\[nocode\]**.</span></span> <span data-ttu-id="14baa-110">當有兩個或多個介面屬性存在時，它們必須以逗號分隔。</span><span class="sxs-lookup"><span data-stu-id="14baa-110">When two or more interface attributes are present, they must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="14baa-111">*介面-名稱*</span><span class="sxs-lookup"><span data-stu-id="14baa-111">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="14baa-112">指定介面的名稱。</span><span class="sxs-lookup"><span data-stu-id="14baa-112">Specifies the name of the interface.</span></span> <span data-ttu-id="14baa-113">在 DCE 相容性模式中，介面名稱必須符合 IDL 檔案中指定的介面名稱。</span><span class="sxs-lookup"><span data-stu-id="14baa-113">In DCE-compatibility mode, the interface name must match the name of the interface specified in the IDL file.</span></span> <span data-ttu-id="14baa-114">當您使用 MIDL 編譯器參數 [**/acf**](-acf.md)時，acf 中的介面名稱和 IDL 檔案中的介面名稱可能會不同。</span><span class="sxs-lookup"><span data-stu-id="14baa-114">When you use the MIDL compiler switch [**/acf**](-acf.md), the interface name in the ACF and the interface name in the IDL file can be different.</span></span>

</dd> <dt>

<span data-ttu-id="14baa-115">*檔案名-清單*</span><span class="sxs-lookup"><span data-stu-id="14baa-115">*filename-list*</span></span> 
</dt> <dd>

<span data-ttu-id="14baa-116">指定一或多個 C 語言標頭檔名稱的清單（以逗號分隔）。</span><span class="sxs-lookup"><span data-stu-id="14baa-116">Specifies a list of one or more C-language header file names, separated by commas.</span></span> <span data-ttu-id="14baa-117">必須提供完整的檔案名（包括副檔名）。</span><span class="sxs-lookup"><span data-stu-id="14baa-117">The full file name, including the extension, must be supplied.</span></span>

</dd> <dt>

<span data-ttu-id="14baa-118">*type-attribute-list*</span><span class="sxs-lookup"><span data-stu-id="14baa-118">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="14baa-119">指定套用至指定類型的一或多個屬性清單（以逗號分隔）。</span><span class="sxs-lookup"><span data-stu-id="14baa-119">Specifies a list of one or more attributes, separated by commas, that apply to the specified type.</span></span> <span data-ttu-id="14baa-120">有效的類型屬性包括 [ **\[** [**配置**](allocate.md)] **\]** 。</span><span class="sxs-lookup"><span data-stu-id="14baa-120">Valid type attributes include **\[**[**allocate**](allocate.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="14baa-121">*typename*</span><span class="sxs-lookup"><span data-stu-id="14baa-121">*typename*</span></span> 
</dt> <dd>

<span data-ttu-id="14baa-122">指定 IDL 檔案中定義的類型。</span><span class="sxs-lookup"><span data-stu-id="14baa-122">Specifies a type defined in the IDL file.</span></span> <span data-ttu-id="14baa-123">ACF 中的類型屬性只能套用至 IDL 檔案中先前定義的類型。</span><span class="sxs-lookup"><span data-stu-id="14baa-123">Type attributes in the ACF can only be applied to types previously defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="14baa-124">*ACF 函式-屬性*</span><span class="sxs-lookup"><span data-stu-id="14baa-124">*ACF-function-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="14baa-125">指定套用至整個函數的屬性，例如， **\[** [**通訊 \_ 狀態**](comm-status.md) **\]** 。</span><span class="sxs-lookup"><span data-stu-id="14baa-125">Specifies attributes that apply to the function as a whole, such as **\[**[**comm\_status**](comm-status.md)**\]**.</span></span> <span data-ttu-id="14baa-126">函數屬性以方括弧括住。</span><span class="sxs-lookup"><span data-stu-id="14baa-126">Function attributes are enclosed in square brackets.</span></span> <span data-ttu-id="14baa-127">以逗號分隔多個函式屬性。</span><span class="sxs-lookup"><span data-stu-id="14baa-127">Separate multiple function attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="14baa-128">*函數名稱*</span><span class="sxs-lookup"><span data-stu-id="14baa-128">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="14baa-129">指定 IDL 檔案中所定義的函式名稱。</span><span class="sxs-lookup"><span data-stu-id="14baa-129">Specifies the name of the function as defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="14baa-130">*ACF-參數-屬性*</span><span class="sxs-lookup"><span data-stu-id="14baa-130">*ACF-parameter-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="14baa-131">指定適用于參數的 ACF 屬性。</span><span class="sxs-lookup"><span data-stu-id="14baa-131">Specifies ACF attributes that apply to a parameter.</span></span> <span data-ttu-id="14baa-132">請注意，您可以將零個或更多屬性套用至參數。</span><span class="sxs-lookup"><span data-stu-id="14baa-132">Note that zero or more attributes can be applied to the parameter.</span></span> <span data-ttu-id="14baa-133">以逗號分隔多個參數屬性。</span><span class="sxs-lookup"><span data-stu-id="14baa-133">Separate multiple parameter attributes with commas.</span></span> <span data-ttu-id="14baa-134">ACF 參數屬性以方括弧括住。</span><span class="sxs-lookup"><span data-stu-id="14baa-134">ACF parameter attributes are enclosed in square brackets.</span></span>

</dd> <dt>

<span data-ttu-id="14baa-135">*參數-名稱*</span><span class="sxs-lookup"><span data-stu-id="14baa-135">*parameter-name*</span></span> 
</dt> <dd>

<span data-ttu-id="14baa-136">指定 IDL 檔案中定義之函式的參數。</span><span class="sxs-lookup"><span data-stu-id="14baa-136">Specifies a parameter of the function as defined in the IDL file.</span></span> <span data-ttu-id="14baa-137">函數的每個參數都必須以相同的順序指定，並且使用 IDL 檔案中所定義的相同名稱。</span><span class="sxs-lookup"><span data-stu-id="14baa-137">Each parameter for the function must be specified in the same sequence and using the same name as defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="14baa-138">備註</span><span class="sxs-lookup"><span data-stu-id="14baa-138">Remarks</span></span>

<span data-ttu-id="14baa-139">**\[ 了 nocode \]** 屬性可以出現在 ACF 標頭中，也可以套用至個別的函式。</span><span class="sxs-lookup"><span data-stu-id="14baa-139">The **\[nocode\]** attribute can appear in the ACF header, or it can be applied to an individual function.</span></span>

<span data-ttu-id="14baa-140">如果 **\[ 了 nocode \]** 屬性出現在 ACF 標頭中，則不會為任何遠端函式產生用戶端 stub 程式碼，除非它有 **\[** [**code**](code.md) **\]** function 屬性。</span><span class="sxs-lookup"><span data-stu-id="14baa-140">When the **\[nocode\]** attribute appears in the ACF header, client stub code is not generated for any remote function unless it has the **\[**[**code**](code.md)**\]** function attribute.</span></span> <span data-ttu-id="14baa-141">您可以藉由將程式 **\[ 代碼 \]** 屬性指定為函數屬性，來覆寫個別函式標頭中的 **\[ 了 nocode \]** 屬性。</span><span class="sxs-lookup"><span data-stu-id="14baa-141">You can override the **\[nocode\]** attribute in the header for an individual function by specifying the **\[code\]** attribute as a function attribute.</span></span>

<span data-ttu-id="14baa-142">當 **\[ 了 nocode \]** 屬性出現在函式的屬性清單中時，不會為函式產生任何用戶端 stub 程式碼。</span><span class="sxs-lookup"><span data-stu-id="14baa-142">When the **\[nocode\]** attribute appears in the function's attribute list, no client stub code is generated for the function.</span></span>

<span data-ttu-id="14baa-143">當下列情況時，不會產生用戶端 stub 程式碼：</span><span class="sxs-lookup"><span data-stu-id="14baa-143">Client stub code is not generated when:</span></span>

-   <span data-ttu-id="14baa-144">ACF 標頭包含 **\[ 了 nocode \]** 屬性。</span><span class="sxs-lookup"><span data-stu-id="14baa-144">The ACF header includes the **\[nocode\]** attribute.</span></span>
-   <span data-ttu-id="14baa-145">**\[ 了 nocode \]** 屬性會套用至函數。</span><span class="sxs-lookup"><span data-stu-id="14baa-145">The **\[nocode\]** attribute is applied to the function.</span></span>
-   <span data-ttu-id="14baa-146">**\[** [**Local**](local.md) **\]** 屬性會套用至介面檔中的函式。</span><span class="sxs-lookup"><span data-stu-id="14baa-146">The **\[**[**local**](local.md)**\]** attribute applies to the function in the interface file.</span></span>

<span data-ttu-id="14baa-147">程式 **\[** [**代碼**](code.md) **\]** 或 **\[ 了 nocode \]** 可以出現在函式的屬性清單中，而您所選擇的只會出現一次。</span><span class="sxs-lookup"><span data-stu-id="14baa-147">Either **\[**[**code**](code.md)**\]** or **\[nocode\]** can appear in a function's attribute list, and the one you choose can appear exactly once.</span></span>

<span data-ttu-id="14baa-148">當伺服器 stub 產生時，會忽略 **\[ 了 nocode \]** 屬性。</span><span class="sxs-lookup"><span data-stu-id="14baa-148">The **\[nocode\]** attribute is ignored when server stubs are generated.</span></span> <span data-ttu-id="14baa-149">當您在 DCE 相容性模式中產生伺服器 stub 時，不能套用此應用。</span><span class="sxs-lookup"><span data-stu-id="14baa-149">You cannot apply it when generating server stubs in DCE-compatibility mode.</span></span>

## <a name="see-also"></a><span data-ttu-id="14baa-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="14baa-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14baa-151">應用程式佈建檔 (ACF) </span><span class="sxs-lookup"><span data-stu-id="14baa-151">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="14baa-152">**/acf**</span><span class="sxs-lookup"><span data-stu-id="14baa-152">**/acf**</span></span>](-acf.md)
</dt> <dt>

[<span data-ttu-id="14baa-153">**分配**</span><span class="sxs-lookup"><span data-stu-id="14baa-153">**allocate**</span></span>](allocate.md)
</dt> <dt>

[<span data-ttu-id="14baa-154">**自動 \_ 處理**</span><span class="sxs-lookup"><span data-stu-id="14baa-154">**auto\_handle**</span></span>](auto-handle.md)
</dt> <dt>

[<span data-ttu-id="14baa-155">**代碼**</span><span class="sxs-lookup"><span data-stu-id="14baa-155">**code**</span></span>](code.md)
</dt> <dt>

[<span data-ttu-id="14baa-156">**通訊 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="14baa-156">**comm\_status**</span></span>](comm-status.md)
</dt> <dt>

[<span data-ttu-id="14baa-157">**隱含 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="14baa-157">**implicit\_handle**</span></span>](implicit-handle.md)
</dt> </dl>

 

 




