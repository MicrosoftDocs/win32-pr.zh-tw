---
description: 原始產品 MNP2000 的協同功能檔案包含 Concert.txt 檔案中的錯誤。
ms.assetid: 4289bd0c-bdf3-4747-9287-94f737ce4f5c
title: 規劃小型更新修補程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f15f3667c6a18ab7a71e86997091bd76d4b15577
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "103853516"
---
# <a name="planning-a-small-update-patch"></a><span data-ttu-id="bd0e2-103">規劃小型更新修補程式</span><span class="sxs-lookup"><span data-stu-id="bd0e2-103">Planning a Small Update Patch</span></span>

<span data-ttu-id="bd0e2-104">原始產品 MNP2000 的協同功能檔案包含 Concert.txt 檔案中的錯誤。</span><span class="sxs-lookup"><span data-stu-id="bd0e2-104">The Concert feature file of the original product, MNP2000, contains an error in the Concert.txt file.</span></span> <span data-ttu-id="bd0e2-105">因為 Windows Installer 用於安裝和設定應用程式，所以應用程式的次要修正可能會藉由安裝小型更新修補程式套件來處理。</span><span class="sxs-lookup"><span data-stu-id="bd0e2-105">Because Windows Installer was used for the installation and setup of the application, minor fixes to the application may be handled by installing a small update patch package.</span></span> <span data-ttu-id="bd0e2-106">[小型更新](small-updates.md)會變更一或多個太小的應用程式檔，以變更產品代碼。</span><span class="sxs-lookup"><span data-stu-id="bd0e2-106">A [small update](small-updates.md) makes changes to one or more application files that are too minor to change the product code.</span></span> <span data-ttu-id="bd0e2-107">下列範例會示範如何建立 Windows Installer 修補程式套件，以套用小型更新並提供 MNP2000 產品的快速修正。</span><span class="sxs-lookup"><span data-stu-id="bd0e2-107">The following example shows you how to create a Windows Installer patch package that can apply the small update and provide a quick fix to the MNP2000 product.</span></span>

<span data-ttu-id="bd0e2-108">若要建立 small update，請先取得 MNP2000 產品的完整未壓縮映射，其中包含 Concert.txt 中的錯誤。</span><span class="sxs-lookup"><span data-stu-id="bd0e2-108">To create the small update first obtain a fully uncompressed image of the MNP2000 product that includes the error in Concert.txt.</span></span> <span data-ttu-id="bd0e2-109">映射必須包含 MNP2000.msi 以及 [規劃安裝](planning-the-installation.md)中所述的所有來源檔案。</span><span class="sxs-lookup"><span data-stu-id="bd0e2-109">The image must include MNP2000.msi and all the source files described in [Planning the Installation](planning-the-installation.md).</span></span> <span data-ttu-id="bd0e2-110">在以下討論中，這稱為目標映射。</span><span class="sxs-lookup"><span data-stu-id="bd0e2-110">In the following discussion this is called the Target image.</span></span> <span data-ttu-id="bd0e2-111">目標映射必須完整解壓縮，因為修補程式建立程式無法針對壓縮于封包中的檔案產生二進位修補程式。</span><span class="sxs-lookup"><span data-stu-id="bd0e2-111">The Target image must be fully uncompressed because the patch creation process is unable to generate binary patches for files compressed in cabinets.</span></span> <span data-ttu-id="bd0e2-112">將目標映射的 .msi 檔案和所有來源檔案放在名為 Target 的資料夾中。</span><span class="sxs-lookup"><span data-stu-id="bd0e2-112">Put the .msi file and all the source files of the Target image into a folder named Target.</span></span>

<span data-ttu-id="bd0e2-113">接下來，使用固定的 Concert.txt 檔案取得 MNP2000 產品的完整未壓縮映射。</span><span class="sxs-lookup"><span data-stu-id="bd0e2-113">Next, obtain a fully uncompressed image of the MNP2000 product with a Concert.txt file that is fixed.</span></span> <span data-ttu-id="bd0e2-114">這在下列討論中稱為升級的映射。</span><span class="sxs-lookup"><span data-stu-id="bd0e2-114">This is called the Upgraded image in the following discussion.</span></span> <span data-ttu-id="bd0e2-115">使用安裝資料庫編輯工具（例如 Orca）來更新 .msi 檔案。</span><span class="sxs-lookup"><span data-stu-id="bd0e2-115">Use an installation database editing tool, such as Orca, to update the .msi file.</span></span> <span data-ttu-id="bd0e2-116">例如，如果已更正 Concert.txt 的大小小於原始的大小，請務必在升級映射之 File 資料表的 [FileSize] 欄位中輸入新的大小。</span><span class="sxs-lookup"><span data-stu-id="bd0e2-116">For example, if the size of the corrected Concert.txt is smaller than the original, be sure to enter the new size in the FileSize field of the File table of the upgraded image.</span></span> <span data-ttu-id="bd0e2-117">請注意，由於套件已變更，您必須在 [ [**修訂編號摘要**](revision-number-summary.md) ] 屬性中指派新的封裝程式碼。</span><span class="sxs-lookup"><span data-stu-id="bd0e2-117">Note that because the package has changed you must assign a new package code in the [**Revision Number Summary**](revision-number-summary.md) Property.</span></span> <span data-ttu-id="bd0e2-118">將已升級影像的 .msi 檔案和所有原始程式檔放入名為 [已升級] 的資料夾中。</span><span class="sxs-lookup"><span data-stu-id="bd0e2-118">Put the .msi file and all the source files of the Upgraded image into a folder named Upgraded.</span></span>

<span data-ttu-id="bd0e2-119">基於此範例的目的，假設 Concert.txt 檔案的大小變更。</span><span class="sxs-lookup"><span data-stu-id="bd0e2-119">For the purposes of this example, assume that the size of the Concert.txt file changes.</span></span> <span data-ttu-id="bd0e2-120">這表示目標和升級資料庫之檔案資料表中的 FileSize 欄位包含不同的資料。</span><span class="sxs-lookup"><span data-stu-id="bd0e2-120">This means that FileSize fields in the File tables of the Target and Upgraded database contain different data.</span></span>

<span data-ttu-id="bd0e2-121">下列檔案 [資料表](file-table.md) 會從目標影像中識別記錄。</span><span class="sxs-lookup"><span data-stu-id="bd0e2-121">The following [File Table](file-table.md) identifies the record from the Target Image.</span></span>



| <span data-ttu-id="bd0e2-122">檔案</span><span class="sxs-lookup"><span data-stu-id="bd0e2-122">File</span></span>        | <span data-ttu-id="bd0e2-123">元件\_</span><span class="sxs-lookup"><span data-stu-id="bd0e2-123">Component\_</span></span> | <span data-ttu-id="bd0e2-124">FileName</span><span class="sxs-lookup"><span data-stu-id="bd0e2-124">FileName</span></span>    | <span data-ttu-id="bd0e2-125">FileSize</span><span class="sxs-lookup"><span data-stu-id="bd0e2-125">FileSize</span></span> | <span data-ttu-id="bd0e2-126">版本</span><span class="sxs-lookup"><span data-stu-id="bd0e2-126">Version</span></span> | <span data-ttu-id="bd0e2-127">語言</span><span class="sxs-lookup"><span data-stu-id="bd0e2-127">Language</span></span> | <span data-ttu-id="bd0e2-128">屬性</span><span class="sxs-lookup"><span data-stu-id="bd0e2-128">Attributes</span></span> | <span data-ttu-id="bd0e2-129">順序</span><span class="sxs-lookup"><span data-stu-id="bd0e2-129">Sequence</span></span> |
|-------------|-------------|-------------|----------|---------|----------|------------|----------|
| <span data-ttu-id="bd0e2-130">Concert.txt</span><span class="sxs-lookup"><span data-stu-id="bd0e2-130">Concert.txt</span></span> | <span data-ttu-id="bd0e2-131">演唱會</span><span class="sxs-lookup"><span data-stu-id="bd0e2-131">Concert</span></span>     | <span data-ttu-id="bd0e2-132">Concert.txt</span><span class="sxs-lookup"><span data-stu-id="bd0e2-132">Concert.txt</span></span> | <span data-ttu-id="bd0e2-133">1000</span><span class="sxs-lookup"><span data-stu-id="bd0e2-133">1000</span></span>     |         |          | <span data-ttu-id="bd0e2-134">0</span><span class="sxs-lookup"><span data-stu-id="bd0e2-134">0</span></span>          | <span data-ttu-id="bd0e2-135">1</span><span class="sxs-lookup"><span data-stu-id="bd0e2-135">1</span></span>        |



 

<span data-ttu-id="bd0e2-136">下列檔案資料表會從升級的映射中識別記錄。</span><span class="sxs-lookup"><span data-stu-id="bd0e2-136">The following File Table identifies the record from the Upgraded Image.</span></span>



| <span data-ttu-id="bd0e2-137">檔案</span><span class="sxs-lookup"><span data-stu-id="bd0e2-137">File</span></span>        | <span data-ttu-id="bd0e2-138">元件\_</span><span class="sxs-lookup"><span data-stu-id="bd0e2-138">Component\_</span></span> | <span data-ttu-id="bd0e2-139">FileName</span><span class="sxs-lookup"><span data-stu-id="bd0e2-139">FileName</span></span>    | <span data-ttu-id="bd0e2-140">FileSize</span><span class="sxs-lookup"><span data-stu-id="bd0e2-140">FileSize</span></span> | <span data-ttu-id="bd0e2-141">版本</span><span class="sxs-lookup"><span data-stu-id="bd0e2-141">Version</span></span> | <span data-ttu-id="bd0e2-142">語言</span><span class="sxs-lookup"><span data-stu-id="bd0e2-142">Language</span></span> | <span data-ttu-id="bd0e2-143">屬性</span><span class="sxs-lookup"><span data-stu-id="bd0e2-143">Attributes</span></span> | <span data-ttu-id="bd0e2-144">順序</span><span class="sxs-lookup"><span data-stu-id="bd0e2-144">Sequence</span></span> |
|-------------|-------------|-------------|----------|---------|----------|------------|----------|
| <span data-ttu-id="bd0e2-145">Concert.txt</span><span class="sxs-lookup"><span data-stu-id="bd0e2-145">Concert.txt</span></span> | <span data-ttu-id="bd0e2-146">演唱會</span><span class="sxs-lookup"><span data-stu-id="bd0e2-146">Concert</span></span>     | <span data-ttu-id="bd0e2-147">Concert.txt</span><span class="sxs-lookup"><span data-stu-id="bd0e2-147">Concert.txt</span></span> | <span data-ttu-id="bd0e2-148">900</span><span class="sxs-lookup"><span data-stu-id="bd0e2-148">900</span></span>      |         |          | <span data-ttu-id="bd0e2-149">0</span><span class="sxs-lookup"><span data-stu-id="bd0e2-149">0</span></span>          | <span data-ttu-id="bd0e2-150">1</span><span class="sxs-lookup"><span data-stu-id="bd0e2-150">1</span></span>        |



 

> [!Note]
> <span data-ttu-id="bd0e2-151">檔案在目標映射和更新的映射的檔案 [資料表](file-table.md) 中必須有相同的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="bd0e2-151">The file must have the same key in the [File Tables](file-table.md) of both the target image and the updated image.</span></span> <span data-ttu-id="bd0e2-152">這兩個數據表的 File 資料行中的字串值必須相同。</span><span class="sxs-lookup"><span data-stu-id="bd0e2-152">The string values in the File column of both tables must be identical.</span></span> <span data-ttu-id="bd0e2-153">大寫和小寫也必須相同。</span><span class="sxs-lookup"><span data-stu-id="bd0e2-153">Uppercase and lowercase must be identical also.</span></span>
> 
> <span data-ttu-id="bd0e2-154">遵循 [建立修補程式套件](creating-a-patch-package.md)中所述的指導方針。</span><span class="sxs-lookup"><span data-stu-id="bd0e2-154">Follow the guidelines described in [Creating a Patch Package](creating-a-patch-package.md).</span></span> <span data-ttu-id="bd0e2-155">請勿使用只有大小寫不同的檔案 [資料表](file-table.md) 索引鍵來撰寫套件，因為 [Msimsp.exe](msimsp-exe.md) 和 [Patchwiz.dll](patchwiz-dll.md) 呼叫 Makecab.exe （不區分大小寫且修補程式產生失敗）。</span><span class="sxs-lookup"><span data-stu-id="bd0e2-155">Do not author a package with [File Table](file-table.md) keys that differ only by case, because [Msimsp.exe](msimsp-exe.md) and [Patchwiz.dll](patchwiz-dll.md) call Makecab.exe, which is case-insensitive and patch generation fails.</span></span>

[<span data-ttu-id="bd0e2-156">繼續</span><span class="sxs-lookup"><span data-stu-id="bd0e2-156">Continue</span></span>](creating-a-patch-creation-properties-file.md)

 

 



