---
title: /n 參數
description: /N 參數會指定撰寫中繼資料檔案的組合深度。
ms.assetid: 7A1F8A9E-B3CC-4BB2-BF50-5662D4560280
keywords:
- /n 參數 MIDL
topic_type:
- apiref
api_name:
- /n
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78197c0f79c6bbe21ae4eb883620b95e6f0bd4c0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993619"
---
# <a name="n-switch"></a><span data-ttu-id="b807e-104">/n 參數</span><span class="sxs-lookup"><span data-stu-id="b807e-104">/n switch</span></span>

<span data-ttu-id="b807e-105">**/N** 參數會指定撰寫中繼資料檔案的組合深度。</span><span class="sxs-lookup"><span data-stu-id="b807e-105">The **/n** switch specifies the composition depth for composing metadata files.</span></span>

``` syntax
mdmerge /n namespace_depth
```

## <a name="switch-options"></a><span data-ttu-id="b807e-106">切換選項</span><span class="sxs-lookup"><span data-stu-id="b807e-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="b807e-107">*命名空間 \_ 深度*</span><span class="sxs-lookup"><span data-stu-id="b807e-107">*namespace\_depth*</span></span> 
</dt> <dd>

<span data-ttu-id="b807e-108">指定要組成單一中繼資料檔案的命名空間深度。</span><span class="sxs-lookup"><span data-stu-id="b807e-108">Specifies the namespace depth to compose into a single metadata file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b807e-109">備註</span><span class="sxs-lookup"><span data-stu-id="b807e-109">Remarks</span></span>

<span data-ttu-id="b807e-110">以下是您可以使用 **/n** 參數指定的可能值格式。</span><span class="sxs-lookup"><span data-stu-id="b807e-110">Here are the possible value formats that you can specify with the **/n** switch.</span></span>



| <span data-ttu-id="b807e-111">值格式</span><span class="sxs-lookup"><span data-stu-id="b807e-111">Value format</span></span>                   | <span data-ttu-id="b807e-112">Description</span><span class="sxs-lookup"><span data-stu-id="b807e-112">Description</span></span>                                                                     |
|--------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="b807e-113">Int32 > 0</span><span class="sxs-lookup"><span data-stu-id="b807e-113">Int32 > 0</span></span>                   | <span data-ttu-id="b807e-114">在參數中指定的命名空間深度撰寫所有類型。</span><span class="sxs-lookup"><span data-stu-id="b807e-114">Compose all types at the namespace depth specified in the switch.</span></span>               |
| <span data-ttu-id="b807e-115">-1</span><span class="sxs-lookup"><span data-stu-id="b807e-115">-1</span></span>                             | <span data-ttu-id="b807e-116">將所有類型撰寫為每個命名空間一個 IDL 檔案。</span><span class="sxs-lookup"><span data-stu-id="b807e-116">Compose all types into one IDL file per namespace.</span></span>                              |
| <span data-ttu-id="b807e-117"><namespace>： Int32 > 0</span><span class="sxs-lookup"><span data-stu-id="b807e-117"><namespace>:Int32 > 0</span></span> | <span data-ttu-id="b807e-118">在參數中指定的深度，撰寫具有相符命名空間的所有類型。</span><span class="sxs-lookup"><span data-stu-id="b807e-118">Compose all types with matching namespace at the depth specified in the switch.</span></span> |
| <span data-ttu-id="b807e-119"><namespace>：-1</span><span class="sxs-lookup"><span data-stu-id="b807e-119"><namespace>:-1</span></span>           | <span data-ttu-id="b807e-120">使用相符的命名空間，將所有類型組成每個命名空間的一個檔案。</span><span class="sxs-lookup"><span data-stu-id="b807e-120">Compose all types with matching namespace into one file per namespace.</span></span>          |



 

<span data-ttu-id="b807e-121">下表顯示使用這些命名空間的不同 **/n** 參數組合的結果。</span><span class="sxs-lookup"><span data-stu-id="b807e-121">The following table shows the results from different combinations of the **/n** switch working on these namespaces.</span></span>

-   <span data-ttu-id="b807e-122">Iiterable<t>。</span><span class="sxs-lookup"><span data-stu-id="b807e-122">Windows.Foundation.Collections.IIterable</span></span>
-   <span data-ttu-id="b807e-123">DirectUI. Button （控制項）</span><span class="sxs-lookup"><span data-stu-id="b807e-123">Windows.UI.DirectUI.Controls.Button</span></span>
-   <span data-ttu-id="b807e-124">DirectUI （ListView）</span><span class="sxs-lookup"><span data-stu-id="b807e-124">Windows.UI.DirectUI.Controls.ListView</span></span>
-   <span data-ttu-id="b807e-125">PlayTo. Target （應用程式）</span><span class="sxs-lookup"><span data-stu-id="b807e-125">Windows.UI.Immersive.Application.PlayTo.Target</span></span>
-   <span data-ttu-id="b807e-126">Web.config。 RSS</span><span class="sxs-lookup"><span data-stu-id="b807e-126">Windows.Web.Syndication.RSS</span></span>



| <span data-ttu-id="b807e-127">交換器</span><span class="sxs-lookup"><span data-stu-id="b807e-127">Switches</span></span>                         | <span data-ttu-id="b807e-128">結果</span><span class="sxs-lookup"><span data-stu-id="b807e-128">Result</span></span>                                                                                                                                                                                                                                                       | <span data-ttu-id="b807e-129">說明</span><span class="sxs-lookup"><span data-stu-id="b807e-129">Explanation</span></span>                                                                                                                                                                                                                                                                                                                        |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b807e-130">**/n：-1**  /**n：1**</span><span class="sxs-lookup"><span data-stu-id="b807e-130">**/n:-1** /**n:1**</span></span>               | <span data-ttu-id="b807e-131">Windows.winmd</span><span class="sxs-lookup"><span data-stu-id="b807e-131">Windows.winmd</span></span>                                                                                                                                                                                                                                                | <span data-ttu-id="b807e-132">最後一個/n 參數會覆寫所有先前的-n 參數。</span><span class="sxs-lookup"><span data-stu-id="b807e-132">The last /n switch overrides all previous –n switches.</span></span>                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="b807e-133">**/n：-1/n： Windows。 UI：2**</span><span class="sxs-lookup"><span data-stu-id="b807e-133">**/n:-1/n:Windows.UI:2**</span></span>         | <dl> <span data-ttu-id="b807e-134"><dt>Windows</dt> <dt>. winmd.</dt> <dt>...</dt> .。</span><span class="sxs-lookup"><span data-stu-id="b807e-134"><dt>Windows.Foundation.winmd</dt> <dt>Windows.UI.winmd</dt> <dt>Windows.Web.Syndication.winmd</dt></span></span> </dl> | <dl> <span data-ttu-id="b807e-135"><dt>**Windows Foundation** 一律是在-n:2. 上撰寫</dt></span><span class="sxs-lookup"><span data-stu-id="b807e-135"><dt>**Windows.Foundation** is always composed at –n:2.</dt></span></span> <span data-ttu-id="b807e-136"><dt>**Windows. UI** 類型為群組。</dt></span><span class="sxs-lookup"><span data-stu-id="b807e-136"><dt>**Windows.UI** types are grouped.</dt></span></span> <span data-ttu-id="b807e-137"><dt>**Web.config** 的組成 n:-1。</dt></span><span class="sxs-lookup"><span data-stu-id="b807e-137"><dt>**Windows.Web.Syndication** is composed at n:-1.</dt></span></span> </dl>       |
| <span data-ttu-id="b807e-138">**/n： 1/n： DirectUI：3**</span><span class="sxs-lookup"><span data-stu-id="b807e-138">**/n:1/n:Windows.UI.DirectUI:3**</span></span> | <dl> <span data-ttu-id="b807e-139"><dt>Windows.Foundation.winmd</dt> <dt>Windows.UI.DirectUI.winmd </dt> <dt>Windows.winmd</dt></span><span class="sxs-lookup"><span data-stu-id="b807e-139"><dt>Windows.Foundation.winmd</dt> <dt>Windows.UI.DirectUI.winmd </dt> <dt>Windows.winmd</dt></span></span> </dl>       | <dl> <span data-ttu-id="b807e-140"><dt>**Windows Foundation** 一律是在-n:2. 上撰寫</dt></span><span class="sxs-lookup"><span data-stu-id="b807e-140"><dt>**Windows.Foundation** is always composed at –n:2.</dt></span></span> <span data-ttu-id="b807e-141"><dt>**DirectUI** 是在層級3撰寫。</dt></span><span class="sxs-lookup"><span data-stu-id="b807e-141"><dt>**Windows.UI.DirectUI** is composed at level 3.</dt></span></span> <span data-ttu-id="b807e-142"><dt>所有其他類型都是在層級1上組成。</dt></span><span class="sxs-lookup"><span data-stu-id="b807e-142"><dt>All other types are composed at level 1.</dt></span></span> </dl> |



 

<span data-ttu-id="b807e-143">以下是處理 **/n** 參數之多個實例的規則。</span><span class="sxs-lookup"><span data-stu-id="b807e-143">Here are the rules for handling multiple instances of the **/n** switch.</span></span>

-   <span data-ttu-id="b807e-144">最特定的實例准。</span><span class="sxs-lookup"><span data-stu-id="b807e-144">The most specific instance prevails.</span></span> <span data-ttu-id="b807e-145">例如，如果您指定 **– n:A.B.C：4– n:A.B： 5**，MDMERGE 會在第4層解析 .c，因為 b. c 比 A.B. 更明確</span><span class="sxs-lookup"><span data-stu-id="b807e-145">For example, if you specify **–n:A.B.C:4–n:A.B:5**, MDMERGE resolves A.B.C.D at level 4, because A.B.C is more specific than A.B.</span></span> <span data-ttu-id="b807e-146">B. f. 會在深度5中解析，因為它符合 A B 但未 A.B.C。</span><span class="sxs-lookup"><span data-stu-id="b807e-146">A.B.E.F resolves at depth 5, because it matches A.B but not A.B.C.</span></span>
-   <span data-ttu-id="b807e-147">最後一個實例准。</span><span class="sxs-lookup"><span data-stu-id="b807e-147">The last instance prevails.</span></span> <span data-ttu-id="b807e-148">例如，如果您指定 **– n:5 – n:2**，則類型會在層級2組成。</span><span class="sxs-lookup"><span data-stu-id="b807e-148">For example, if you specify **–n:5–n:2**, the types are composed at level 2.</span></span>
-   <span data-ttu-id="b807e-149">這兩個規則都適用。</span><span class="sxs-lookup"><span data-stu-id="b807e-149">Both of these rules apply.</span></span> <span data-ttu-id="b807e-150">如果您指定– n:A.B.C：4– n:A.B.C：1，namespace A. C 會由層級1組成。</span><span class="sxs-lookup"><span data-stu-id="b807e-150">If you specify –n:A.B.C:4 –n:A.B.C:1, namespace A.B.C is composed at level 1.</span></span>

## <a name="examples"></a><span data-ttu-id="b807e-151">範例</span><span class="sxs-lookup"><span data-stu-id="b807e-151">Examples</span></span>

<span data-ttu-id="b807e-152">**mdmerge.exe 中繼資料 \_ dir $ (SDK \_ 中繼資料 \_ 路徑) -i $ (內部 \_ SDK \_ 中繼資料 \_ 路徑) -o $ (OBJ \_ 路徑) \\ $O \\ SystemMetadata-v-n:-1-n:Windows.Foundation：2**</span><span class="sxs-lookup"><span data-stu-id="b807e-152">**mdmerge.exe -metadata\_dir $(SDK\_METADATA\_PATH) -i $(INTERNAL\_SDK\_METADATA\_PATH) -o $(OBJ\_PATH)\\$O\\SystemMetadata -v -n:-1 -n:Windows.Foundation:2**</span></span>

## <a name="requirements"></a><span data-ttu-id="b807e-153">規格需求</span><span class="sxs-lookup"><span data-stu-id="b807e-153">Requirements</span></span>



| <span data-ttu-id="b807e-154">需求</span><span class="sxs-lookup"><span data-stu-id="b807e-154">Requirement</span></span> | <span data-ttu-id="b807e-155">值</span><span class="sxs-lookup"><span data-stu-id="b807e-155">Value</span></span> |
|-------------------|--------------------------------|
| <span data-ttu-id="b807e-156">用戶端</span><span class="sxs-lookup"><span data-stu-id="b807e-156">Client</span></span><br/> | <span data-ttu-id="b807e-157">Windows 8</span><span class="sxs-lookup"><span data-stu-id="b807e-157">Windows 8</span></span><br/>           |
| <span data-ttu-id="b807e-158">伺服器</span><span class="sxs-lookup"><span data-stu-id="b807e-158">Server</span></span><br/> | <span data-ttu-id="b807e-159">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b807e-159">Windows Server 2012</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b807e-160">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b807e-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b807e-161">一般 MIDL 命令列語法</span><span class="sxs-lookup"><span data-stu-id="b807e-161">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> </dl>

 

 





