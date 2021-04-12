---
title: code 屬性
description: '\ Code \ ACF 屬性會產生遠端函式的用戶端 stub 程式碼。'
ms.assetid: 735a8c25-29d4-4073-a2db-88bc8615ccc1
keywords:
- code 屬性 MIDL
topic_type:
- apiref
api_name:
- code
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa041859c0bffca2771695b7055105b8ae846221
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104313029"
---
# <a name="code-attribute"></a><span data-ttu-id="666bd-104">code 屬性</span><span class="sxs-lookup"><span data-stu-id="666bd-104">code attribute</span></span>

<span data-ttu-id="666bd-105">**\[ Code \]** ACF 屬性會為遠端函式產生用戶端 stub 程式碼。</span><span class="sxs-lookup"><span data-stu-id="666bd-105">The **\[code\]** ACF attribute causes client stub code to be generated for remote functions.</span></span>

``` syntax
[
    code [ , ACF-interface-attributes ] 
] 
interface interface-name
{
  [ include filename-list ; ]
  [ typedef [type-attribute-list] typenam; ]
  [ [code [ , ACF-function-attributes ]] function-name (
            [ ACF-parameter-attributes ] parameter-name,
        ...);
  ]
    ...
}
```

## <a name="parameters"></a><span data-ttu-id="666bd-106">參數</span><span class="sxs-lookup"><span data-stu-id="666bd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="666bd-107">*ACF-介面-屬性*</span><span class="sxs-lookup"><span data-stu-id="666bd-107">*ACF-interface-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="666bd-108">指定套用至整個介面的一或多個屬性清單。</span><span class="sxs-lookup"><span data-stu-id="666bd-108">Specifies a list of one or more attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="666bd-109">有效的屬性包括 [**\[ auto \_ 句 \] 柄**](auto-handle.md)或 [**\[ 隱含 \_ \] 控制碼**](implicit-handle.md)，以及程式 **\[ 代碼 \]**、 [**\[ 了 nocode \]**](nocode.md)或 [**\[ optimize \]**](optimize.md)。</span><span class="sxs-lookup"><span data-stu-id="666bd-109">Valid attributes include either [**\[auto\_handle\]**](auto-handle.md) or [**\[implicit\_handle\]**](implicit-handle.md) and either **\[code\]**, [**\[nocode\]**](nocode.md), or [**\[optimize\]**](optimize.md).</span></span> <span data-ttu-id="666bd-110">當有兩個或多個介面屬性存在時，它們必須以逗號分隔。</span><span class="sxs-lookup"><span data-stu-id="666bd-110">When two or more interface attributes are present, they must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="666bd-111">*介面-名稱*</span><span class="sxs-lookup"><span data-stu-id="666bd-111">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="666bd-112">指定介面的名稱。</span><span class="sxs-lookup"><span data-stu-id="666bd-112">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="666bd-113">*檔案名-清單*</span><span class="sxs-lookup"><span data-stu-id="666bd-113">*filename-list*</span></span> 
</dt> <dd>

<span data-ttu-id="666bd-114">指定一或多個 C 標頭檔名稱的清單（以逗號分隔）。</span><span class="sxs-lookup"><span data-stu-id="666bd-114">Specifies a list of one or more C-header file names, separated by commas.</span></span> <span data-ttu-id="666bd-115">您必須提供完整的檔案名，包括副檔名。</span><span class="sxs-lookup"><span data-stu-id="666bd-115">You must supply the full file name, including the extension.</span></span>

</dd> <dt>

<span data-ttu-id="666bd-116">*type-attribute-list*</span><span class="sxs-lookup"><span data-stu-id="666bd-116">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="666bd-117">指定套用至指定類型的一或多個屬性清單（以逗號分隔）。</span><span class="sxs-lookup"><span data-stu-id="666bd-117">Specifies a list of one or more attributes, separated by commas, that apply to the specified type.</span></span> <span data-ttu-id="666bd-118">有效的型別屬性包括將 [**\[ \] 配置**](allocate.md)和 [**\[ 表示 \_ 為 \]**](represent-as.md)。</span><span class="sxs-lookup"><span data-stu-id="666bd-118">Valid type attributes include [**\[allocate\]**](allocate.md) and [**\[represent\_as\]**](represent-as.md).</span></span>

</dd> <dt>

<span data-ttu-id="666bd-119">*typename*</span><span class="sxs-lookup"><span data-stu-id="666bd-119">*typename*</span></span> 
</dt> <dd>

<span data-ttu-id="666bd-120">指定 IDL 檔案中定義的類型。</span><span class="sxs-lookup"><span data-stu-id="666bd-120">Specifies a type defined in the IDL file.</span></span> <span data-ttu-id="666bd-121">ACF 中的 Type 屬性只能套用至 IDL 檔案中先前定義的類型。</span><span class="sxs-lookup"><span data-stu-id="666bd-121">Type attributes in the ACF can be applied only to types previously defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="666bd-122">*ACF 函式-屬性*</span><span class="sxs-lookup"><span data-stu-id="666bd-122">*ACF-function-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="666bd-123">指定套用至整個函式的零或多個屬性，例如 [**\[ 通訊 \_ 狀態 \]**](comm-status.md)。</span><span class="sxs-lookup"><span data-stu-id="666bd-123">Specifies zero or more attributes that apply to the function as a whole, such as [**\[comm\_status\]**](comm-status.md).</span></span> <span data-ttu-id="666bd-124">函數屬性以方括弧括住。</span><span class="sxs-lookup"><span data-stu-id="666bd-124">Function attributes are enclosed in square brackets.</span></span> <span data-ttu-id="666bd-125">以逗號分隔多個函式屬性。</span><span class="sxs-lookup"><span data-stu-id="666bd-125">Separate multiple function attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="666bd-126">*函數名稱*</span><span class="sxs-lookup"><span data-stu-id="666bd-126">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="666bd-127">指定 IDL 檔案中所定義的函式名稱。</span><span class="sxs-lookup"><span data-stu-id="666bd-127">Specifies the name of the function as defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="666bd-128">*ACF-參數-屬性*</span><span class="sxs-lookup"><span data-stu-id="666bd-128">*ACF-parameter-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="666bd-129">指定適用于參數的 ACF 屬性。</span><span class="sxs-lookup"><span data-stu-id="666bd-129">Specifies ACF attributes that apply to a parameter.</span></span> <span data-ttu-id="666bd-130">請注意，您可以將零個、一個或多個屬性套用至參數。</span><span class="sxs-lookup"><span data-stu-id="666bd-130">Note that zero, one, or more attributes can be applied to the parameter.</span></span> <span data-ttu-id="666bd-131">以逗號分隔多個參數屬性。</span><span class="sxs-lookup"><span data-stu-id="666bd-131">Separate multiple parameter attributes with commas.</span></span> <span data-ttu-id="666bd-132">ACF 參數屬性以方括弧括住。</span><span class="sxs-lookup"><span data-stu-id="666bd-132">ACF parameter attributes are enclosed in square brackets.</span></span>

</dd> <dt>

<span data-ttu-id="666bd-133">*參數-名稱*</span><span class="sxs-lookup"><span data-stu-id="666bd-133">*parameter-name*</span></span> 
</dt> <dd>

<span data-ttu-id="666bd-134">指定 IDL 檔案中定義之函式的參數。</span><span class="sxs-lookup"><span data-stu-id="666bd-134">Specifies a parameter of the function as defined in the IDL file.</span></span> <span data-ttu-id="666bd-135">函數的每個參數都必須以相同的順序指定，並且與 IDL 檔案中定義的名稱相同。</span><span class="sxs-lookup"><span data-stu-id="666bd-135">Each parameter for the function must be specified in the same sequence and with the same name as defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="666bd-136">備註</span><span class="sxs-lookup"><span data-stu-id="666bd-136">Remarks</span></span>

<span data-ttu-id="666bd-137">**\[ Code \]** 屬性可以出現在 ACF 標頭中，或套用至個別的函式。</span><span class="sxs-lookup"><span data-stu-id="666bd-137">The **\[code\]** attribute can appear in the ACF header or be applied to an individual function.</span></span>

<span data-ttu-id="666bd-138">當程式 **\[ 代碼 \]** 屬性出現在 ACF 標頭時，會針對沒有 [**\[ 了 nocode \]**](nocode.md)函數屬性的所有遠端函式產生用戶端 stub 程式碼。</span><span class="sxs-lookup"><span data-stu-id="666bd-138">When the **\[code\]** attribute appears in the ACF header, client stub code is generated for all remote functions that do not have the [**\[nocode\]**](nocode.md) function attribute.</span></span> <span data-ttu-id="666bd-139">您可以藉由將 **\[ 了 nocode \]** 屬性指定為函數屬性，來覆寫個別函式標頭中的程式 **\[ 代碼 \]** 屬性。</span><span class="sxs-lookup"><span data-stu-id="666bd-139">You can override the **\[code\]** attribute in the header for an individual function by specifying the **\[nocode\]** attribute as a function attribute.</span></span>

<span data-ttu-id="666bd-140">當程式 **\[ 代碼 \]** 屬性出現在遠端函式的屬性清單時，就會為函式產生用戶端 stub 程式碼。</span><span class="sxs-lookup"><span data-stu-id="666bd-140">When the **\[code\]** attribute appears in the remote function's attribute list, client stub code is generated for the function.</span></span> <span data-ttu-id="666bd-141">當下列情況時，不會產生用戶端 stub 程式碼：</span><span class="sxs-lookup"><span data-stu-id="666bd-141">Client stub code is not generated when:</span></span>

-   <span data-ttu-id="666bd-142">ACF 標頭包含 [**\[ 了 nocode \]**](nocode.md)屬性。</span><span class="sxs-lookup"><span data-stu-id="666bd-142">The ACF header includes the [**\[nocode\]**](nocode.md) attribute.</span></span>
-   <span data-ttu-id="666bd-143">[**\[ 了 nocode \]**](nocode.md)屬性會套用至函數。</span><span class="sxs-lookup"><span data-stu-id="666bd-143">The [**\[nocode\]**](nocode.md) attribute is applied to the function.</span></span>
-   <span data-ttu-id="666bd-144">[**\[ Local \]**](local.md)屬性會套用至介面檔中的函式。</span><span class="sxs-lookup"><span data-stu-id="666bd-144">The [**\[local\]**](local.md) attribute applies to the function in the interface file.</span></span>

<span data-ttu-id="666bd-145">程式 **\[ 代碼 \]** 或 [**\[ 了 nocode \]**](nocode.md)可以出現在 [介面] 或 [函式] 屬性清單中，但您選擇的只會在清單中顯示一次。</span><span class="sxs-lookup"><span data-stu-id="666bd-145">Either **\[code\]** or [**\[nocode\]**](nocode.md) can appear in the interface or function attribute list, but the one you choose can appear only once in the list.</span></span>

## <a name="see-also"></a><span data-ttu-id="666bd-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="666bd-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="666bd-147">應用程式佈建檔 (ACF) </span><span class="sxs-lookup"><span data-stu-id="666bd-147">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="666bd-148">**分配**</span><span class="sxs-lookup"><span data-stu-id="666bd-148">**allocate**</span></span>](allocate.md)
</dt> <dt>

[<span data-ttu-id="666bd-149">**自動 \_ 處理**</span><span class="sxs-lookup"><span data-stu-id="666bd-149">**auto\_handle**</span></span>](auto-handle.md)
</dt> <dt>

[<span data-ttu-id="666bd-150">**通訊 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="666bd-150">**comm\_status**</span></span>](comm-status.md)
</dt> <dt>

[<span data-ttu-id="666bd-151">**隱含 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="666bd-151">**implicit\_handle**</span></span>](implicit-handle.md)
</dt> <dt>

[<span data-ttu-id="666bd-152">**當地**</span><span class="sxs-lookup"><span data-stu-id="666bd-152">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="666bd-153">**了 nocode**</span><span class="sxs-lookup"><span data-stu-id="666bd-153">**nocode**</span></span>](nocode.md)
</dt> <dt>

[<span data-ttu-id="666bd-154">**優化**</span><span class="sxs-lookup"><span data-stu-id="666bd-154">**optimize**</span></span>](optimize.md)
</dt> <dt>

[<span data-ttu-id="666bd-155">**表示 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="666bd-155">**represent\_as**</span></span>](represent-as.md)
</dt> </dl>

 

 




