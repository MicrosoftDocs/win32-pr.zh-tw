---
description: 若要產生修補程式套件，建議您使用修補程式建立工具，例如 Msimsp.exe 和 Patchwiz.dll。
ms.assetid: aca3bbd2-440a-405f-bddc-5f9cc831b811
title: Patchwiz.dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6dc1135a9e2c09bb8a96e041f77bae39f0057ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195265"
---
# <a name="patchwizdll"></a><span data-ttu-id="49f4e-103">Patchwiz.dll</span><span class="sxs-lookup"><span data-stu-id="49f4e-103">Patchwiz.dll</span></span>

<span data-ttu-id="49f4e-104">若要產生修補程式套件，建議您使用修補程式建立工具，例如 [Msimsp.exe](msimsp-exe.md) 和 Patchwiz.dll。</span><span class="sxs-lookup"><span data-stu-id="49f4e-104">To generate a patch package, it is recommended that you use a patch creation tool such as [Msimsp.exe](msimsp-exe.md) and Patchwiz.dll.</span></span> <span data-ttu-id="49f4e-105">Patchwiz.dll 版本4.0 與使用舊版 Patchwiz.dll 撰寫的套件和修補程式相容。</span><span class="sxs-lookup"><span data-stu-id="49f4e-105">Patchwiz.dll version 4.0 is compatible with packages and patches that were authored using earlier versions of the Patchwiz.dll.</span></span> <span data-ttu-id="49f4e-106">Patchwiz.dll 工具僅適用于 [Windows Installer 開發人員 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)。</span><span class="sxs-lookup"><span data-stu-id="49f4e-106">The Patchwiz.dll tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

<span data-ttu-id="49f4e-107">Patchwiz.dll 4.0 版有一個新的函式（ [UiCreatePatchPackageEx (Patchwiz.dll) ](uicreatepatchpackageex--patchwiz-dll-.md)），可延伸 [UiCreatePatchPackage (Patchwiz.dll) ](uicreatepatchpackage-patchwiz-dll-.md)的功能。</span><span class="sxs-lookup"><span data-stu-id="49f4e-107">Patchwiz.dll version 4.0 has one new function, [UiCreatePatchPackageEx (Patchwiz.dll)](uicreatepatchpackageex--patchwiz-dll-.md), that extends the functionality of [UiCreatePatchPackage (Patchwiz.dll)](uicreatepatchpackage-patchwiz-dll-.md).</span></span> <span data-ttu-id="49f4e-108">這些函式會取得修補程式建立屬性檔 ( pcp 檔案) 並產生安裝 [程式修補套件](patch-packages.md)。</span><span class="sxs-lookup"><span data-stu-id="49f4e-108">These functions take a patch creation properties file (.pcp file) and generate an installer [Patch Package](patch-packages.md).</span></span>

<span data-ttu-id="49f4e-109">Pcp 檔案是二進位資料庫檔案，其格式與 Windows Installer 資料庫 ( .msi 檔案) 相同，但使用不同的資料庫架構。</span><span class="sxs-lookup"><span data-stu-id="49f4e-109">The .pcp file is a binary database file with the same format as a Windows Installer database (.msi file), but with a different database schema.</span></span> <span data-ttu-id="49f4e-110">因此，您可以使用安裝程式資料庫所使用的相同工具來撰寫 pcp 檔案。</span><span class="sxs-lookup"><span data-stu-id="49f4e-110">Therefore a .pcp file can be authored by using the same tools used for an installer database.</span></span>

<span data-ttu-id="49f4e-111">您可以使用資料表編輯器（例如 [Orca.exe](orca-exe.md) ）來建立 pcp 檔案，並將資訊輸入 Windows Installer SDK 所提供的 pcp 資料庫 pcp。</span><span class="sxs-lookup"><span data-stu-id="49f4e-111">You can create a .pcp file by using a table editor such as [Orca.exe](orca-exe.md) to enter information into the blank .pcp database provided with the Windows Installer SDK, Template.pcp.</span></span> <span data-ttu-id="49f4e-112">如需詳細資訊，請參閱 [小型更新修補範例](a-small-update-patching-example.md)。</span><span class="sxs-lookup"><span data-stu-id="49f4e-112">For more information, see [A Small Update Patching Example](a-small-update-patching-example.md).</span></span>

<span data-ttu-id="49f4e-113">每個 pcp 檔案都需要下列資料庫資料表：</span><span class="sxs-lookup"><span data-stu-id="49f4e-113">The following database tables are required in every .pcp file:</span></span>

-   [<span data-ttu-id="49f4e-114">屬性資料表 (Patchwiz.dll) </span><span class="sxs-lookup"><span data-stu-id="49f4e-114">Properties Table (Patchwiz.dll)</span></span>](properties-table-patchwiz-dll-.md)
-   [<span data-ttu-id="49f4e-115">ImageFamilies 資料表 (Patchwiz.dll) </span><span class="sxs-lookup"><span data-stu-id="49f4e-115">ImageFamilies Table (Patchwiz.dll)</span></span>](imagefamilies-table-patchwiz-dll-.md)
-   [<span data-ttu-id="49f4e-116">UpgradedImages 資料表 (Patchwiz.dll) </span><span class="sxs-lookup"><span data-stu-id="49f4e-116">UpgradedImages Table (Patchwiz.dll)</span></span>](upgradedimages-table-patchwiz-dll-.md)
-   [<span data-ttu-id="49f4e-117">TargetImages 資料表 (Patchwiz.dll) </span><span class="sxs-lookup"><span data-stu-id="49f4e-117">TargetImages Table (Patchwiz.dll)</span></span>](targetimages-table-patchwiz-dll-.md)

<span data-ttu-id="49f4e-118">下列資料庫資料表是選擇性的：</span><span class="sxs-lookup"><span data-stu-id="49f4e-118">The following database tables are optional:</span></span>

-   [<span data-ttu-id="49f4e-119">UpgradedFiles \_ OptionalData 資料表 (Patchwiz.dll) </span><span class="sxs-lookup"><span data-stu-id="49f4e-119">UpgradedFiles\_OptionalData Table (Patchwiz.dll)</span></span>](upgradedfiles-optionaldata-table-patchwiz-dll-.md)
-   [<span data-ttu-id="49f4e-120">FamilyFileRanges 資料表 (Patchwiz.dll) </span><span class="sxs-lookup"><span data-stu-id="49f4e-120">FamilyFileRanges Table (Patchwiz.dll)</span></span>](familyfileranges-table-patchwiz-dll-.md)
-   [<span data-ttu-id="49f4e-121">TargetFiles \_ OptionalData 資料表 (Patchwiz.dll) </span><span class="sxs-lookup"><span data-stu-id="49f4e-121">TargetFiles\_OptionalData Table (Patchwiz.dll)</span></span>](targetfiles-optionaldata-table-patchwiz-dll-.md)
-   [<span data-ttu-id="49f4e-122">ExternalFiles 資料表 (Patchwiz.dll) </span><span class="sxs-lookup"><span data-stu-id="49f4e-122">ExternalFiles Table (Patchwiz.dll)</span></span>](externalfiles-table-patchwiz-dll-.md)
-   [<span data-ttu-id="49f4e-123">UpgradedFilesToIgnore 資料表 (Patchwiz.dll) </span><span class="sxs-lookup"><span data-stu-id="49f4e-123">UpgradedFilesToIgnore Table (Patchwiz.dll)</span></span>](upgradedfilestoignore-table-patchwiz-dll-.md)

<span data-ttu-id="49f4e-124">在 pcp 檔案中，如果 MinimumRequiredMsiVersion 等於 [屬性](properties-table-patchwiz-dll-.md) 表中的300，則需要下表。</span><span class="sxs-lookup"><span data-stu-id="49f4e-124">The following table is required in .pcp files that have a MinimumRequiredMsiVersion equal to 300 in the [Properties](properties-table-patchwiz-dll-.md) table.</span></span>

-   [<span data-ttu-id="49f4e-125">PatchMetadata 資料表 (Patchwiz.dll) </span><span class="sxs-lookup"><span data-stu-id="49f4e-125">PatchMetadata Table (Patchwiz.dll)</span></span>](patchmetadata-table--patchwiz-dll-.md)

> [!Note]  
> <span data-ttu-id="49f4e-126">如果 MinimumRequiredMsiVersion 不等於300，則資料表是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="49f4e-126">The table is optional if MinimumRequiredMsiVersion is not equal to 300.</span></span>

 

<span data-ttu-id="49f4e-127">使用 Windows Installer 3.0 發行的 Patchwiz.dll 版本可以自動產生修補程式順序資訊，並將其新增至新修補程式的 [MsiPatchSequence 資料表](msipatchsequence-table.md) 。</span><span class="sxs-lookup"><span data-stu-id="49f4e-127">The version of Patchwiz.dll released with Windows Installer 3.0 can automatically generate patch sequencing information and add it to the [MsiPatchSequence Table](msipatchsequence-table.md) of a new patch.</span></span> <span data-ttu-id="49f4e-128">您可以使用 [PatchSequence 資料表](patchsequence-table--patchwiz-dll-.md) ，以手動方式將修補程式排序資訊新增至 MsiPatchSequence 資料表。</span><span class="sxs-lookup"><span data-stu-id="49f4e-128">The [PatchSequence Table](patchsequence-table--patchwiz-dll-.md) can be used to manually add patch sequencing information the MsiPatchSequence Table.</span></span> <span data-ttu-id="49f4e-129">如需詳細資訊，請參閱 [產生修補程式順序資訊](generating-patch-sequence-information---patchwiz-dll-.md)。</span><span class="sxs-lookup"><span data-stu-id="49f4e-129">For more information, see [Generating Patch Sequence Information](generating-patch-sequence-information---patchwiz-dll-.md).</span></span>

<span data-ttu-id="49f4e-130">從 Patchwiz.dll 版本2.0 開始，您可以使用 [修補資訊快取 (Patchwiz.dll) ](patch-information-caching-patchwiz-dll-.md)來提高後續修補建立的速度。</span><span class="sxs-lookup"><span data-stu-id="49f4e-130">Beginning with Patchwiz.dll version 2.0, you can increase the speed of subsequent patch creation by using [Patch Information Caching (Patchwiz.dll)](patch-information-caching-patchwiz-dll-.md).</span></span>

<span data-ttu-id="49f4e-131">針對您的目標和升級映射二進位檔使用公用符號，可減少大約一半的二進位修補程式大小。</span><span class="sxs-lookup"><span data-stu-id="49f4e-131">Using public symbols for your target and upgrade image binaries can reduce binary patch sizes by approximately one half.</span></span> <span data-ttu-id="49f4e-132">如需詳細資訊，請參閱 [使用符號來減少二進位修補程式大小](using-symbols-to-reduce-binary-patch-size.md)。</span><span class="sxs-lookup"><span data-stu-id="49f4e-132">For more information, see [Using Symbols to Reduce Binary Patch Size](using-symbols-to-reduce-binary-patch-size.md).</span></span>

<span data-ttu-id="49f4e-133">您可以指定要保留目標檔案的特定區域，使其在修補期間遭到覆寫，並保留這些區域中的資訊。</span><span class="sxs-lookup"><span data-stu-id="49f4e-133">You can specify that certain regions of the target file be preserved from being overwritten during patching and that the information in those regions be retained.</span></span> <span data-ttu-id="49f4e-134">如需詳細資訊，請參閱 [修補檔案的選取區域](patching-selected-regions-of-a-file.md)。</span><span class="sxs-lookup"><span data-stu-id="49f4e-134">For more information, see [Patching Selected Regions of a File](patching-selected-regions-of-a-file.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="49f4e-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="49f4e-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49f4e-136">已發行的版本、工具和可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="49f4e-136">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



