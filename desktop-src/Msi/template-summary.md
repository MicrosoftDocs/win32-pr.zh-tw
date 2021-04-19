---
description: 若為安裝套件，[範本摘要] 屬性會指出與此安裝資料庫相容的平臺和語言版本。
ms.assetid: a1015ddb-8d5c-40f7-97ac-4a1347644ae6
title: 範本摘要屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36b3949e7028fd0b1b5f9ff3112f1a3d03c9b87e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999163"
---
# <a name="template-summary-property"></a><span data-ttu-id="e9f8e-103">範本摘要屬性</span><span class="sxs-lookup"><span data-stu-id="e9f8e-103">Template Summary property</span></span>

<span data-ttu-id="e9f8e-104">若為安裝套件，[ **範本摘要** ] 屬性會指出與此安裝資料庫相容的平臺和語言版本。</span><span class="sxs-lookup"><span data-stu-id="e9f8e-104">For an installation package, the **Template Summary** property indicates the platform and language versions that are compatible with this installation database.</span></span> <span data-ttu-id="e9f8e-105">安裝資料庫之 **範本摘要** 屬性資訊的語法如下：</span><span class="sxs-lookup"><span data-stu-id="e9f8e-105">The syntax of the **Template Summary** property information for an installation database is the following:</span></span>

<span data-ttu-id="e9f8e-106">\[*platform 屬性* \] ; \[*語言識別項* \] \[ ，,...*語言識別項* \] \[ \] 。</span><span class="sxs-lookup"><span data-stu-id="e9f8e-106">\[*platform property*\];\[*language id*\]\[,*language id*\]\[,...\].</span></span>

<span data-ttu-id="e9f8e-107">下列範例是 **範本摘要** 屬性的有效值：</span><span class="sxs-lookup"><span data-stu-id="e9f8e-107">The following examples are valid values for the **Template Summary** property:</span></span>

-   <span data-ttu-id="e9f8e-108">x64; 1033</span><span class="sxs-lookup"><span data-stu-id="e9f8e-108">x64;1033</span></span>
-   <span data-ttu-id="e9f8e-109">Intel; 1033</span><span class="sxs-lookup"><span data-stu-id="e9f8e-109">Intel;1033</span></span>
-   <span data-ttu-id="e9f8e-110">Intel64; 1033</span><span class="sxs-lookup"><span data-stu-id="e9f8e-110">Intel64;1033</span></span>
-   <span data-ttu-id="e9f8e-111">; 1033</span><span class="sxs-lookup"><span data-stu-id="e9f8e-111">;1033</span></span>
-   <span data-ttu-id="e9f8e-112">Intel、1033、2046</span><span class="sxs-lookup"><span data-stu-id="e9f8e-112">Intel ;1033,2046</span></span>
-   <span data-ttu-id="e9f8e-113">Intel64; 1033，2046</span><span class="sxs-lookup"><span data-stu-id="e9f8e-113">Intel64;1033,2046</span></span>
-   <span data-ttu-id="e9f8e-114">Intel; 0</span><span class="sxs-lookup"><span data-stu-id="e9f8e-114">Intel;0</span></span>
-   <span data-ttu-id="e9f8e-115">Arm; 1033、2046</span><span class="sxs-lookup"><span data-stu-id="e9f8e-115">Arm;1033,2046</span></span>
-   <span data-ttu-id="e9f8e-116">Arm; 0</span><span class="sxs-lookup"><span data-stu-id="e9f8e-116">Arm;0</span></span>
-   <span data-ttu-id="e9f8e-117">Arm64; 1033，2046</span><span class="sxs-lookup"><span data-stu-id="e9f8e-117">Arm64;1033,2046</span></span>
-   <span data-ttu-id="e9f8e-118">Arm64; 0</span><span class="sxs-lookup"><span data-stu-id="e9f8e-118">Arm64;0</span></span>

<span data-ttu-id="e9f8e-119">轉換的 [ **範本摘要** ] 屬性會指出與轉換相容的平臺和語言版本。</span><span class="sxs-lookup"><span data-stu-id="e9f8e-119">The **Template Summary** property of a transform indicates the platform and language versions compatible with the transform.</span></span> <span data-ttu-id="e9f8e-120">在轉換檔中，只能指定一種語言。</span><span class="sxs-lookup"><span data-stu-id="e9f8e-120">In a transform file, only one language may be specified.</span></span> <span data-ttu-id="e9f8e-121">指定的平臺和語言會決定是否可以將轉換套用至特定的資料庫。</span><span class="sxs-lookup"><span data-stu-id="e9f8e-121">The specified platform and language determine whether a transform can be applied to a particular database.</span></span> <span data-ttu-id="e9f8e-122">如果沒有任何轉換限制依賴它們來驗證轉換，則 platform 屬性和 language 屬性可以保留空白。</span><span class="sxs-lookup"><span data-stu-id="e9f8e-122">The platform property and the language property can be left blank if no transform restriction relies on them to validate the transform.</span></span>

<span data-ttu-id="e9f8e-123">Patch 封裝的 [ **範本摘要** ] 屬性是可接受修補程式的產品代碼清單（以分號分隔）。</span><span class="sxs-lookup"><span data-stu-id="e9f8e-123">The **Template Summary** property of a patch package is a semicolon-delimited list of the product codes that can accept the patch.</span></span> <span data-ttu-id="e9f8e-124">如果您使用 [Msimsp.exe](msimsp-exe.md) 並 [Patchwiz.dll](patchwiz-dll.md) 來產生修補程式套件，則會從 Patch 建立檔案的 [TargetImages 資料表](targetimages-table-patchwiz-dll-.md) 中取得此清單。</span><span class="sxs-lookup"><span data-stu-id="e9f8e-124">If you use [Msimsp.exe](msimsp-exe.md) and [Patchwiz.dll](patchwiz-dll.md) to generate the patch package, this list is obtained from the [TargetImages table](targetimages-table-patchwiz-dll-.md) of the patch creation file.</span></span>

<span data-ttu-id="e9f8e-125">這是必要的摘要屬性。</span><span class="sxs-lookup"><span data-stu-id="e9f8e-125">This summary property is required.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9f8e-126">備註</span><span class="sxs-lookup"><span data-stu-id="e9f8e-126">Remarks</span></span>

<span data-ttu-id="e9f8e-127">如果目前的平臺不符合 **範本摘要** 屬性中所指定的其中一個平臺，安裝程式就不會處理封裝。</span><span class="sxs-lookup"><span data-stu-id="e9f8e-127">If the current platform does not match one of the platforms specified in the **Template Summary** property then the installer does not process the package.</span></span>

<span data-ttu-id="e9f8e-128">如果 **範本摘要** 屬性值中缺少平臺規格，則安裝程式會假設採用 Intel 架構。</span><span class="sxs-lookup"><span data-stu-id="e9f8e-128">If the platform specification is missing in the **Template Summary** property value, the installer assumes the Intel architecture.</span></span>

<span data-ttu-id="e9f8e-129">如果這是在 Intel64 (Itanium) 平臺上執行的64位 Windows Installer 套件，請在 [ **範本摘要** ] 屬性中輸入 Intel64。</span><span class="sxs-lookup"><span data-stu-id="e9f8e-129">If this is a 64-bit Windows Installer package being run on an Intel64 (Itanium) platform, enter Intel64 in the **Template Summary** property.</span></span>

<span data-ttu-id="e9f8e-130">如果這是在 x64 平臺上執行的64位 Windows Installer 套件，請在 [ **範本摘要** ] 屬性中輸入 x64。</span><span class="sxs-lookup"><span data-stu-id="e9f8e-130">If this is a 64-bit Windows Installer package being run on a x64 platform, enter x64 in the **Template Summary** property.</span></span>

<span data-ttu-id="e9f8e-131">如果這是在 Arm64 平臺上執行的64位 Windows Installer 套件，請在 [ **範本摘要** ] 屬性中輸入 Arm64。</span><span class="sxs-lookup"><span data-stu-id="e9f8e-131">If this is a 64-bit Windows Installer package being run on an Arm64 platform, enter Arm64 in the **Template Summary** property.</span></span>

<span data-ttu-id="e9f8e-132">Windows Installer 套件不可標示為支援 Intel64 和 x64;例如，Intel64，x64 的 **範本摘要** 屬性值無效。</span><span class="sxs-lookup"><span data-stu-id="e9f8e-132">A Windows Installer package cannot be marked as supporting both Intel64 and x64; for example, the **Template Summary** property value of Intel64,x64 is invalid.</span></span>

<span data-ttu-id="e9f8e-133">Windows Installer 套件不可標示為支援32位和64位平臺;例如，例如 Intel、x64 或 Intel、Intel64 等 **範本摘要** 屬性值無效。</span><span class="sxs-lookup"><span data-stu-id="e9f8e-133">A Windows Installer package cannot be marked as supporting both 32-bit and 64-bit platforms; for example, **Template Summary** property values such as Intel,x64 or Intel,Intel64 are invalid.</span></span>

<span data-ttu-id="e9f8e-134">在 [ **範本摘要** ] 屬性的 [語言識別項] 欄位中輸入 0 (零) ，或將這個欄位保留空白，表示封裝為非語言相關。</span><span class="sxs-lookup"><span data-stu-id="e9f8e-134">Entering 0 (zero) in the language ID field of the **Template Summary** property, or leaving this field empty, indicates that the package is language neutral.</span></span>

<span data-ttu-id="e9f8e-135">如果這是在 Windows RT 上執行 Windows Installer 套件，請在 [ **範本摘要** ] 屬性中輸入 Arm 的值。</span><span class="sxs-lookup"><span data-stu-id="e9f8e-135">If this is a Windows Installer package being run on Windows RT, enter the value Arm in the **Template Summary** property.</span></span>

<span data-ttu-id="e9f8e-136">合併模組是唯一可能具有多個語言的封裝。</span><span class="sxs-lookup"><span data-stu-id="e9f8e-136">Merge Modules are the only packages that may have multiple languages.</span></span> <span data-ttu-id="e9f8e-137">來源安裝程式資料庫中只能指定一種語言。</span><span class="sxs-lookup"><span data-stu-id="e9f8e-137">Only one language can be specified in a source installer database.</span></span> <span data-ttu-id="e9f8e-138">如需詳細資訊，請參閱 [多個語言合併模組](multiple-language-merge-modules.md)。</span><span class="sxs-lookup"><span data-stu-id="e9f8e-138">For more information, see [Multiple Language Merge Modules](multiple-language-merge-modules.md).</span></span>

<span data-ttu-id="e9f8e-139">Windows Installer 不支援 Alpha 平臺。</span><span class="sxs-lookup"><span data-stu-id="e9f8e-139">The Alpha platform is not supported by Windows Installer.</span></span>

<span data-ttu-id="e9f8e-140">**Windows Installer：** 不支援下列語法：</span><span class="sxs-lookup"><span data-stu-id="e9f8e-140">**Windows Installer:** The following syntax is not supported:</span></span>

<span data-ttu-id="e9f8e-141">\[*platform 屬性* \] \[ 、*platform 屬性* \] \[ \] ,... \[*語言識別項* \] \[ ，,...*語言識別項* \] \[ \] 。</span><span class="sxs-lookup"><span data-stu-id="e9f8e-141">\[*platform property*\]\[,*platform property*\]\[,...\]\[*language id*\]\[,*language id*\]\[,...\].</span></span>

<span data-ttu-id="e9f8e-142">下列範例不是 **範本摘要** 屬性的有效值：</span><span class="sxs-lookup"><span data-stu-id="e9f8e-142">The following examples are not valid values for the **Template Summary** property:</span></span>

-   <span data-ttu-id="e9f8e-143">Alpha、Intel、1033</span><span class="sxs-lookup"><span data-stu-id="e9f8e-143">Alpha,Intel;1033</span></span>
-   <span data-ttu-id="e9f8e-144">Intel、Alpha、1033</span><span class="sxs-lookup"><span data-stu-id="e9f8e-144">Intel,Alpha;1033</span></span>
-   <span data-ttu-id="e9f8e-145">Alpha; 1033</span><span class="sxs-lookup"><span data-stu-id="e9f8e-145">Alpha;1033</span></span>
-   <span data-ttu-id="e9f8e-146">Alpha、1033、2046</span><span class="sxs-lookup"><span data-stu-id="e9f8e-146">Alpha;1033,2046</span></span>

## <a name="requirements"></a><span data-ttu-id="e9f8e-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="e9f8e-147">Requirements</span></span>



| <span data-ttu-id="e9f8e-148">需求</span><span class="sxs-lookup"><span data-stu-id="e9f8e-148">Requirement</span></span> | <span data-ttu-id="e9f8e-149">值</span><span class="sxs-lookup"><span data-stu-id="e9f8e-149">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9f8e-150">版本</span><span class="sxs-lookup"><span data-stu-id="e9f8e-150">Version</span></span><br/> | <span data-ttu-id="e9f8e-151">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="e9f8e-151">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e9f8e-152">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="e9f8e-152">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e9f8e-153">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="e9f8e-153">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e9f8e-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e9f8e-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9f8e-155">摘要屬性描述</span><span class="sxs-lookup"><span data-stu-id="e9f8e-155">Summary Property Descriptions</span></span>](summary-property-descriptions.md)
</dt> </dl>

 

 




