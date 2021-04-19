---
description: 若要重現範例修補程式套件，您需要能夠建立和編輯 Windows Installer 修補套件的軟體工具。
ms.assetid: 0653d8f6-89b0-4c56-ae51-3c7cb7df2909
title: 建立修補程式建立屬性檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2775f8521731b43264df315ae05a874e37dd3ffc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106986629"
---
# <a name="creating-a-patch-creation-properties-file"></a><span data-ttu-id="4a7df-103">建立修補程式建立屬性檔</span><span class="sxs-lookup"><span data-stu-id="4a7df-103">Creating a Patch Creation Properties File</span></span>

<span data-ttu-id="4a7df-104">若要重現範例修補程式套件，您需要能夠建立和編輯 Windows Installer 修補套件的軟體工具。</span><span class="sxs-lookup"><span data-stu-id="4a7df-104">To reproduce the sample patch package, you need a software tool capable of creating and editing a Windows Installer patch package.</span></span> <span data-ttu-id="4a7df-105">您可以從獨立軟體廠商取得數個修補套件建立工具。</span><span class="sxs-lookup"><span data-stu-id="4a7df-105">Several patch package creation tools are available from independent software vendors.</span></span> <span data-ttu-id="4a7df-106">下列各節所討論的範例會使用名為 Orca 的 Windows Installer 資料庫編輯器來撰寫修補程式建立屬性檔 (. pcp 延伸) 。</span><span class="sxs-lookup"><span data-stu-id="4a7df-106">The example discussed in the following sections uses a Windows Installer database editor called Orca to author a patch creation properties file (.pcp extension).</span></span> <span data-ttu-id="4a7df-107">Pcp 檔案可與公用程式 [Msimsp.exe](msimsp-exe.md) 和 [Patchwiz.dll](patchwiz-dll.md) 一起使用，以產生 Windows Installer 修補套件 ( .msp 延伸) 。</span><span class="sxs-lookup"><span data-stu-id="4a7df-107">The .pcp file may be used with the utilities [Msimsp.exe](msimsp-exe.md) and [Patchwiz.dll](patchwiz-dll.md) to generate a Windows Installer patch package (.msp extension).</span></span> <span data-ttu-id="4a7df-108">[Windows Installer 開發人員的 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)中會提供 Orca、Msimsp.exe 和 Patchwiz.dll。</span><span class="sxs-lookup"><span data-stu-id="4a7df-108">Orca, Msimsp.exe, and Patchwiz.dll are provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

<span data-ttu-id="4a7df-109">SDK 也會提供空白的 patch 建立屬性檔 pcp。</span><span class="sxs-lookup"><span data-stu-id="4a7df-109">A blank patch creation properties file, template.pcp, is also provided with the SDK.</span></span> <span data-ttu-id="4a7df-110">製作 pcp 的複本，並重新命名此複製 MNP2000. pcp。</span><span class="sxs-lookup"><span data-stu-id="4a7df-110">Make a copy of template.pcp and rename this copy MNP2000.pcp.</span></span> <span data-ttu-id="4a7df-111">使用 Orca 或其他資料庫編輯器，在 MNP2000. pcp 的 Properties 資料表中輸入下列資料。</span><span class="sxs-lookup"><span data-stu-id="4a7df-111">Use Orca or another database editor to enter the following data into the Properties table of MNP2000.pcp.</span></span> <span data-ttu-id="4a7df-112">Properties 資料表包含 patch 封裝的全域設定。</span><span class="sxs-lookup"><span data-stu-id="4a7df-112">The Properties table contains global settings for the patch package.</span></span>

[<span data-ttu-id="4a7df-113">Properties 資料表</span><span class="sxs-lookup"><span data-stu-id="4a7df-113">Properties Table</span></span>](properties-table-patchwiz-dll-.md)



| <span data-ttu-id="4a7df-114">Name</span><span class="sxs-lookup"><span data-stu-id="4a7df-114">Name</span></span>                               | <span data-ttu-id="4a7df-115">值</span><span class="sxs-lookup"><span data-stu-id="4a7df-115">Value</span></span>                                  |
|------------------------------------|----------------------------------------|
| <span data-ttu-id="4a7df-116">AllowProductCodeMismatches</span><span class="sxs-lookup"><span data-stu-id="4a7df-116">AllowProductCodeMismatches</span></span>         | <span data-ttu-id="4a7df-117">1</span><span class="sxs-lookup"><span data-stu-id="4a7df-117">1</span></span>                                      |
| <span data-ttu-id="4a7df-118">AllowProductVersionMajorMismatches</span><span class="sxs-lookup"><span data-stu-id="4a7df-118">AllowProductVersionMajorMismatches</span></span> | <span data-ttu-id="4a7df-119">1</span><span class="sxs-lookup"><span data-stu-id="4a7df-119">1</span></span>                                      |
| <span data-ttu-id="4a7df-120">ApiPatchingSymbolFlags</span><span class="sxs-lookup"><span data-stu-id="4a7df-120">ApiPatchingSymbolFlags</span></span>             | <span data-ttu-id="4a7df-121">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4a7df-121">0x00000000</span></span>                             |
| <span data-ttu-id="4a7df-122">DontRemoveTempFolderWhenFinished</span><span class="sxs-lookup"><span data-stu-id="4a7df-122">DontRemoveTempFolderWhenFinished</span></span>   | <span data-ttu-id="4a7df-123">1</span><span class="sxs-lookup"><span data-stu-id="4a7df-123">1</span></span>                                      |
| <span data-ttu-id="4a7df-124">IncludeWholeFilesOnly</span><span class="sxs-lookup"><span data-stu-id="4a7df-124">IncludeWholeFilesOnly</span></span>              | <span data-ttu-id="4a7df-125">0</span><span class="sxs-lookup"><span data-stu-id="4a7df-125">0</span></span>                                      |
| <span data-ttu-id="4a7df-126">ListOfPatchGUIDsToReplace</span><span class="sxs-lookup"><span data-stu-id="4a7df-126">ListOfPatchGUIDsToReplace</span></span>          |                                        |
| <span data-ttu-id="4a7df-127">ListOfTargetProductCodes</span><span class="sxs-lookup"><span data-stu-id="4a7df-127">ListOfTargetProductCodes</span></span>           | \*                                     |
| <span data-ttu-id="4a7df-128">PatchGUID</span><span class="sxs-lookup"><span data-stu-id="4a7df-128">PatchGUID</span></span>                          | <span data-ttu-id="4a7df-129">{5406B219-A1AC-4BC4-8695-72292C8195AC}</span><span class="sxs-lookup"><span data-stu-id="4a7df-129">{5406B219-A1AC-4BC4-8695-72292C8195AC}</span></span> |
| <span data-ttu-id="4a7df-130">PatchOutputPath</span><span class="sxs-lookup"><span data-stu-id="4a7df-130">PatchOutputPath</span></span>                    | <span data-ttu-id="4a7df-131">c： \\ .msp 輸出</span><span class="sxs-lookup"><span data-stu-id="4a7df-131">c:\\output.msp</span></span>                         |
| <span data-ttu-id="4a7df-132">PatchSourceList</span><span class="sxs-lookup"><span data-stu-id="4a7df-132">PatchSourceList</span></span>                    | <span data-ttu-id="4a7df-133">PatchSourceList</span><span class="sxs-lookup"><span data-stu-id="4a7df-133">PatchSourceList</span></span>                        |



 

<span data-ttu-id="4a7df-134">使用資料庫編輯器，將下列資料輸入 MNP2000. pcp 的 ImageFamilies 資料表中。</span><span class="sxs-lookup"><span data-stu-id="4a7df-134">Use the database editor to enter the following data into the ImageFamilies table of MNP2000.pcp.</span></span> <span data-ttu-id="4a7df-135">ImageFamilies 資料表包含修補期間要新增至 [媒體資料表](media-table.md) 的資訊。</span><span class="sxs-lookup"><span data-stu-id="4a7df-135">The ImageFamilies table contains information to be added to the [Media table](media-table.md) during patching.</span></span>

[<span data-ttu-id="4a7df-136">ImageFamilies 資料表</span><span class="sxs-lookup"><span data-stu-id="4a7df-136">ImageFamilies Table</span></span>](imagefamilies-table-patchwiz-dll-.md)



| <span data-ttu-id="4a7df-137">系列</span><span class="sxs-lookup"><span data-stu-id="4a7df-137">Family</span></span>  | <span data-ttu-id="4a7df-138">MediaSrcPropName</span><span class="sxs-lookup"><span data-stu-id="4a7df-138">MediaSrcPropName</span></span> | <span data-ttu-id="4a7df-139">MediaDiskId</span><span class="sxs-lookup"><span data-stu-id="4a7df-139">MediaDiskId</span></span> | <span data-ttu-id="4a7df-140">FileSequenceStart</span><span class="sxs-lookup"><span data-stu-id="4a7df-140">FileSequenceStart</span></span> | <span data-ttu-id="4a7df-141">DiskPrompt</span><span class="sxs-lookup"><span data-stu-id="4a7df-141">DiskPrompt</span></span> | <span data-ttu-id="4a7df-142">VolumeLabel</span><span class="sxs-lookup"><span data-stu-id="4a7df-142">VolumeLabel</span></span> |
|---------|------------------|-------------|-------------------|------------|-------------|
| <span data-ttu-id="4a7df-143">MNPapps</span><span class="sxs-lookup"><span data-stu-id="4a7df-143">MNPapps</span></span> | <span data-ttu-id="4a7df-144">MNPSrcPropName</span><span class="sxs-lookup"><span data-stu-id="4a7df-144">MNPSrcPropName</span></span>   | <span data-ttu-id="4a7df-145">2</span><span class="sxs-lookup"><span data-stu-id="4a7df-145">2</span></span>           | <span data-ttu-id="4a7df-146">1000</span><span class="sxs-lookup"><span data-stu-id="4a7df-146">1000</span></span>              |            |             |



 

<span data-ttu-id="4a7df-147">將下列資料輸入 MNP2000. pcp 的 UpgradedImages 資料表中。</span><span class="sxs-lookup"><span data-stu-id="4a7df-147">Enter the following data into the UpgradedImages table of MNP2000.pcp.</span></span> <span data-ttu-id="4a7df-148">UpgradedImages 資料表包含您在 [規劃小型更新修補程式](planning-a-small-update-patch.md)時所建立的升級映射相關資訊。</span><span class="sxs-lookup"><span data-stu-id="4a7df-148">The UpgradedImages table contains information about the Upgraded image you created in [Planning a Small Update Patch](planning-a-small-update-patch.md).</span></span>

[<span data-ttu-id="4a7df-149">UpgradedImages 資料表</span><span class="sxs-lookup"><span data-stu-id="4a7df-149">UpgradedImages Table</span></span>](upgradedimages-table-patchwiz-dll-.md)



| <span data-ttu-id="4a7df-150">已升級</span><span class="sxs-lookup"><span data-stu-id="4a7df-150">Upgraded</span></span>   | <span data-ttu-id="4a7df-151">MsiPath</span><span class="sxs-lookup"><span data-stu-id="4a7df-151">MsiPath</span></span>                                           | <span data-ttu-id="4a7df-152">PatchMsiPath</span><span class="sxs-lookup"><span data-stu-id="4a7df-152">PatchMsiPath</span></span> | <span data-ttu-id="4a7df-153">SymbolPaths</span><span class="sxs-lookup"><span data-stu-id="4a7df-153">SymbolPaths</span></span> | <span data-ttu-id="4a7df-154">系列</span><span class="sxs-lookup"><span data-stu-id="4a7df-154">Family</span></span>  |
|------------|---------------------------------------------------|--------------|-------------|---------|
| <span data-ttu-id="4a7df-155">已 \_ 修正的 MNP</span><span class="sxs-lookup"><span data-stu-id="4a7df-155">MNP\_fixed</span></span> | <span data-ttu-id="4a7df-156">C： \\ Note \_ Installer \\ 修補程式 \\ 升級 \\MNP2000.msi</span><span class="sxs-lookup"><span data-stu-id="4a7df-156">C:\\Note\_Installer\\Patch\\Upgraded\\MNP2000.msi</span></span> |              |             | <span data-ttu-id="4a7df-157">MNPapps</span><span class="sxs-lookup"><span data-stu-id="4a7df-157">MNPapps</span></span> |



 

<span data-ttu-id="4a7df-158">將下列資料輸入 MNP2000. pcp 的 TargetImages 資料表中。</span><span class="sxs-lookup"><span data-stu-id="4a7df-158">Enter the following data into the TargetImages table of MNP2000.pcp.</span></span> <span data-ttu-id="4a7df-159">TargetImages 資料表包含目標影像的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="4a7df-159">The TargetImages table contains information about the Target image.</span></span>

[<span data-ttu-id="4a7df-160">TargetImages 資料表</span><span class="sxs-lookup"><span data-stu-id="4a7df-160">TargetImages Table</span></span>](targetimages-table-patchwiz-dll-.md)



| <span data-ttu-id="4a7df-161">目標</span><span class="sxs-lookup"><span data-stu-id="4a7df-161">Target</span></span>     | <span data-ttu-id="4a7df-162">MsiPath</span><span class="sxs-lookup"><span data-stu-id="4a7df-162">MsiPath</span></span>                                         | <span data-ttu-id="4a7df-163">SymbolPaths</span><span class="sxs-lookup"><span data-stu-id="4a7df-163">SymbolPaths</span></span> | <span data-ttu-id="4a7df-164">已升級</span><span class="sxs-lookup"><span data-stu-id="4a7df-164">Upgraded</span></span>   | <span data-ttu-id="4a7df-165">單</span><span class="sxs-lookup"><span data-stu-id="4a7df-165">Order</span></span> | <span data-ttu-id="4a7df-166">ProductValidateFlags</span><span class="sxs-lookup"><span data-stu-id="4a7df-166">ProductValidateFlags</span></span> | <span data-ttu-id="4a7df-167">IgnoreMissingSrcFiles</span><span class="sxs-lookup"><span data-stu-id="4a7df-167">IgnoreMissingSrcFiles</span></span> |
|------------|-------------------------------------------------|-------------|------------|-------|----------------------|-----------------------|
| <span data-ttu-id="4a7df-168">MNP \_ 錯誤</span><span class="sxs-lookup"><span data-stu-id="4a7df-168">MNP\_error</span></span> | <span data-ttu-id="4a7df-169">C： \\ Note \_ Installer \\ 修補 \\ 目標 \\MNP2000.msi</span><span class="sxs-lookup"><span data-stu-id="4a7df-169">C:\\Note\_Installer\\Patch\\Target\\MNP2000.msi</span></span> |             | <span data-ttu-id="4a7df-170">已 \_ 修正的 MNP</span><span class="sxs-lookup"><span data-stu-id="4a7df-170">MNP\_fixed</span></span> | <span data-ttu-id="4a7df-171">1</span><span class="sxs-lookup"><span data-stu-id="4a7df-171">1</span></span>     |                      | <span data-ttu-id="4a7df-172">0</span><span class="sxs-lookup"><span data-stu-id="4a7df-172">0</span></span>                     |



 

<span data-ttu-id="4a7df-173">針對範例修補程式套件，請將下列資料表保留在 MNP2000 中。 pcp 空白。</span><span class="sxs-lookup"><span data-stu-id="4a7df-173">For the sample patch package, leave the following tables in MNP2000.pcp blank.</span></span>

[<span data-ttu-id="4a7df-174">UpgradedFiles \_ OptionalData 資料表</span><span class="sxs-lookup"><span data-stu-id="4a7df-174">UpgradedFiles\_OptionalData Table</span></span>](upgradedfiles-optionaldata-table-patchwiz-dll-.md)

[<span data-ttu-id="4a7df-175">FamilyFileRanges 資料表</span><span class="sxs-lookup"><span data-stu-id="4a7df-175">FamilyFileRanges Table</span></span>](familyfileranges-table-patchwiz-dll-.md)

[<span data-ttu-id="4a7df-176">TargetFiles \_ OptionalData 資料表</span><span class="sxs-lookup"><span data-stu-id="4a7df-176">TargetFiles\_OptionalData Table</span></span>](targetfiles-optionaldata-table-patchwiz-dll-.md)

[<span data-ttu-id="4a7df-177">ExternalFiles 資料表</span><span class="sxs-lookup"><span data-stu-id="4a7df-177">ExternalFiles Table</span></span>](externalfiles-table-patchwiz-dll-.md)

[<span data-ttu-id="4a7df-178">UpgradedFilesToIgnore 資料表</span><span class="sxs-lookup"><span data-stu-id="4a7df-178">UpgradedFilesToIgnore Table</span></span>](upgradedfilestoignore-table-patchwiz-dll-.md)

[<span data-ttu-id="4a7df-179">繼續</span><span class="sxs-lookup"><span data-stu-id="4a7df-179">Continue</span></span>](generating-a-patch-package.md)

 

 



