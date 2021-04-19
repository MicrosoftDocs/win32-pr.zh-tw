---
description: 合併模組提供標準的方法，讓您提供共用的 Windows Installer 元件，並將設定邏輯傳遞給應用程式。
ms.assetid: 63ced106-12e3-4483-8bfe-22c54fe7a204
title: 使用 Automation 將合併模組合併至資料庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3e28b8cfc1716cdbb296fd0a1410787ae55bb62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977185"
---
# <a name="using-automation-to-merge-a-merge-module-into-a-database"></a><span data-ttu-id="5bba0-103">使用 Automation 將合併模組合併至資料庫</span><span class="sxs-lookup"><span data-stu-id="5bba0-103">Using Automation to Merge a Merge Module into a Database</span></span>

<span data-ttu-id="5bba0-104">[合併模組](merge-modules.md) 提供標準的方法，讓您提供共用的 Windows Installer [*元件*](c-gly.md)，並將設定邏輯傳遞給應用程式。</span><span class="sxs-lookup"><span data-stu-id="5bba0-104">[Merge Modules](merge-modules.md) provide a standard method for you to deliver shared Windows Installer [*components*](c-gly.md), and setup logic to applications.</span></span>

<span data-ttu-id="5bba0-105">合併模組必須使用合併工具合併為安裝套件。</span><span class="sxs-lookup"><span data-stu-id="5bba0-105">Merge modules must be merged into an installation package by using a merge tool.</span></span> <span data-ttu-id="5bba0-106">最佳做法是取得自由散發的合併工具，或購買可從獨立軟體廠商取得的其中一個合併工具，例如，您可以使用 [Mergemod.dll](merge-module-automation.md)。</span><span class="sxs-lookup"><span data-stu-id="5bba0-106">The best practice is to obtain a freely distributed merge tool, or purchase one of the merge tools that are available from independent software vendors, for example, you can use [Mergemod.dll](merge-module-automation.md).</span></span>

<span data-ttu-id="5bba0-107">下列程式示範如何使用 [合併模組自動化](merge-module-automation.md)，將合併模組合併到 Windows Installer 資料庫。</span><span class="sxs-lookup"><span data-stu-id="5bba0-107">The following procedure shows you how to merge a merge module into a Windows Installer database by using [Merge Module Automation](merge-module-automation.md).</span></span>

<span data-ttu-id="5bba0-108">**將模組合併至資料庫**</span><span class="sxs-lookup"><span data-stu-id="5bba0-108">**To merge a module into a database**</span></span>

1.  <span data-ttu-id="5bba0-109">使用 [**OpenLog**](merge-openlog.md) 方法來開啟記錄檔。</span><span class="sxs-lookup"><span data-stu-id="5bba0-109">Open a log file by using the [**OpenLog**](merge-openlog.md) method.</span></span>

    <span data-ttu-id="5bba0-110">只有當您需要建立記錄檔，或為合併進程附加現有的記錄檔時，才需要執行此步驟。</span><span class="sxs-lookup"><span data-stu-id="5bba0-110">This step is required only if you need to create a log file, or append an existing log file for the merge process.</span></span>

2.  <span data-ttu-id="5bba0-111">使用 [**Merge 物件**](merge-object.md)的 [**OpenDatabase**](merge-opendatabase.md)方法，開啟 [.msi](windows-installer-file-extensions.md)安裝資料庫。</span><span class="sxs-lookup"><span data-stu-id="5bba0-111">Open the [.msi](windows-installer-file-extensions.md) installation database by using the [**OpenDatabase**](merge-opendatabase.md) method of the [**Merge Object**](merge-object.md).</span></span>

    <span data-ttu-id="5bba0-112">這是必要步驟。</span><span class="sxs-lookup"><span data-stu-id="5bba0-112">This step is required.</span></span>

    <span data-ttu-id="5bba0-113">您所開啟的資料庫是您想要接收合併模組的資料庫。</span><span class="sxs-lookup"><span data-stu-id="5bba0-113">The database that you open is the one that you want to receive the merge module.</span></span>

3.  <span data-ttu-id="5bba0-114">使用 [**OpenModule**](merge-openmodule.md)方法來開啟 [.msm](windows-installer-file-extensions.md)合併模組。</span><span class="sxs-lookup"><span data-stu-id="5bba0-114">Open the [.msm](windows-installer-file-extensions.md) merge module by using the [**OpenModule**](merge-openmodule.md) method.</span></span>

    <span data-ttu-id="5bba0-115">這是必要步驟。</span><span class="sxs-lookup"><span data-stu-id="5bba0-115">This step is required.</span></span>

    <span data-ttu-id="5bba0-116">這是合併到資料庫的合併模組。</span><span class="sxs-lookup"><span data-stu-id="5bba0-116">This is the merge module that is being merged into the database.</span></span> <span data-ttu-id="5bba0-117">必須先開啟模組，才能與安裝資料庫合併。</span><span class="sxs-lookup"><span data-stu-id="5bba0-117">A module must be opened before it can be merged with an installation database.</span></span>

4.  <span data-ttu-id="5bba0-118">藉由呼叫 [**merge**](merge-object.md) 方法或 [**MergeEx**](merge-mergeex.md) 方法，將模組合併至安裝資料庫。</span><span class="sxs-lookup"><span data-stu-id="5bba0-118">Merge the module into the installation database by calling the [**Merge**](merge-object.md) method or [**MergeEx**](merge-mergeex.md) method.</span></span>

    <span data-ttu-id="5bba0-119">這是必要步驟。</span><span class="sxs-lookup"><span data-stu-id="5bba0-119">This step is required.</span></span>

    <span data-ttu-id="5bba0-120">[**Merge**](merge-object.md)方法或 [**MergeEx**](merge-mergeex.md)方法只能呼叫一次，以便合併 [.msi](windows-installer-file-extensions.md)和 .msm 檔案的特定組合。</span><span class="sxs-lookup"><span data-stu-id="5bba0-120">The [**Merge**](merge-object.md) method or [**MergeEx**](merge-mergeex.md) method can only be called one time to merge a specific combination of [.msi](windows-installer-file-extensions.md) and .msm files.</span></span>

    > [!Note]  
    > <span data-ttu-id="5bba0-121">[**MergeEx**](merge-mergeex.md)方法只能在 [Mergemod.dll 2.0 版](merge-module-automation.md)或更新版本中使用，而且只有在使用 [**IMsmMerge2**](/windows/desktop/api/Mergemod/nn-mergemod-imsmmerge2)介面時才可使用。</span><span class="sxs-lookup"><span data-stu-id="5bba0-121">The [**MergeEx**](merge-mergeex.md) method is only available in [Mergemod.dll version 2.0](merge-module-automation.md) or later, and only when using the [**IMsmMerge2**](/windows/desktop/api/Mergemod/nn-mergemod-imsmmerge2) interface.</span></span>

     

5.  <span data-ttu-id="5bba0-122">抓取 [**Errors**](merge-errors.md) 屬性，並檢查它針對合併衝突或其他錯誤所傳回之 [**錯誤**](error-object.md) 物件的集合。</span><span class="sxs-lookup"><span data-stu-id="5bba0-122">Retrieve the [**Errors**](merge-errors.md) property and examine the collection of [**Error**](error-object.md) objects it returns for merge conflicts or other errors.</span></span>

    <span data-ttu-id="5bba0-123">您必須解決任何錯誤。</span><span class="sxs-lookup"><span data-stu-id="5bba0-123">You must resolve any errors.</span></span>

    <span data-ttu-id="5bba0-124">抓取是非破壞性的，而且可以藉由重複讀取 [**Errors**](merge-errors.md) 屬性來抓取錯誤集合的多個實例。</span><span class="sxs-lookup"><span data-stu-id="5bba0-124">The retrieval is nondestructive, and multiple instances of the error collection can be retrieved by repeatedly reading the [**Errors**](merge-errors.md) property.</span></span>

6.  <span data-ttu-id="5bba0-125">使用 [**Connect**](merge-connect.md) 方法將 merge 模組的元件與功能產生關聯。</span><span class="sxs-lookup"><span data-stu-id="5bba0-125">Associate the components of the merge module with the features by using the [**Connect**](merge-connect.md) method.</span></span>

    <span data-ttu-id="5bba0-126">只有當您有現有的功能，而且想要新增功能以合併至安裝資料庫時，才需要執行此步驟。</span><span class="sxs-lookup"><span data-stu-id="5bba0-126">This step is only required if you have existing features and you want to add features to merge into the installation database.</span></span>

    <span data-ttu-id="5bba0-127">在您呼叫這個方法之前，必須先有一項功能。</span><span class="sxs-lookup"><span data-stu-id="5bba0-127">A feature must exist before you call this method.</span></span> <span data-ttu-id="5bba0-128">如需詳細資訊，請參閱將 [合併模組連接至多個功能](connecting-a-merge-module-to-multiple-features.md)。</span><span class="sxs-lookup"><span data-stu-id="5bba0-128">For more information, see [Connecting a Merge Module to Multiple Features](connecting-a-merge-module-to-multiple-features.md).</span></span>

7.  <span data-ttu-id="5bba0-129">如有必要，請執行下列一或多個動作，以從模組中解壓縮原始程式檔：</span><span class="sxs-lookup"><span data-stu-id="5bba0-129">If necessary, extract source files from the module by doing one or more of the following:</span></span>
    -   <span data-ttu-id="5bba0-130">使用 [**ExtractFiles**](merge-extractfiles.md) 或 [**ExtractFilesEx**](merge-extractfilesex.md) 從內嵌的 .cab 檔解壓縮檔案，然後複製到指定的目錄中。</span><span class="sxs-lookup"><span data-stu-id="5bba0-130">Use [**ExtractFiles**](merge-extractfiles.md) or [**ExtractFilesEx**](merge-extractfilesex.md) to extract files from an embedded .cab file and then copy into a specified directory.</span></span>
        > [!Note]  
        > <span data-ttu-id="5bba0-131">[**ExtractFilesEx**](merge-extractfilesex.md) 需要 [Mergemod.dll 2.0 版](merge-module-automation.md) 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="5bba0-131">[**ExtractFilesEx**](merge-extractfilesex.md) requires [Mergemod.dll version 2.0](merge-module-automation.md) or later.</span></span>

         

    -   <span data-ttu-id="5bba0-132">使用 [**ExtractCAB**](merge-extractcab.md) 從內嵌的 .cab 檔案解壓縮檔案，然後儲存在指定的檔案中。</span><span class="sxs-lookup"><span data-stu-id="5bba0-132">Use [**ExtractCAB**](merge-extractcab.md) to extract files from an embedded .cab file, and then save in a specified file.</span></span>
    -   <span data-ttu-id="5bba0-133">使用 [**CreateSourceImage**](merge-createsourceimage.md) 從模組解壓縮檔案，然後在合併之後，複製到磁片上的來源映射。</span><span class="sxs-lookup"><span data-stu-id="5bba0-133">Use [**CreateSourceImage**](merge-createsourceimage.md) to extract files from a module, and then after the merge, copy to a source image on disk.</span></span>
        > [!Note]  
        > <span data-ttu-id="5bba0-134">[**CreateSourceImage**](merge-createsourceimage.md) 僅適用于 [Mergemod.dll 2.0 版](merge-module-automation.md) 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="5bba0-134">[**CreateSourceImage**](merge-createsourceimage.md) is only available in [Mergemod.dll version 2.0](merge-module-automation.md) or later.</span></span>

         
8.  <span data-ttu-id="5bba0-135">使用 [**CloseModule**](merge-closemodule.md) 方法，關閉目前的開啟合併模組。</span><span class="sxs-lookup"><span data-stu-id="5bba0-135">Close the current open merge module by using the [**CloseModule**](merge-closemodule.md) method.</span></span>

    <span data-ttu-id="5bba0-136">這是必要步驟。</span><span class="sxs-lookup"><span data-stu-id="5bba0-136">This step is required.</span></span>

9.  <span data-ttu-id="5bba0-137">使用 [**CloseDatabase**](merge-closedatabase.md) 方法來關閉開啟的安裝資料庫。</span><span class="sxs-lookup"><span data-stu-id="5bba0-137">Close the open installation database by using the [**CloseDatabase**](merge-closedatabase.md) method.</span></span>

    <span data-ttu-id="5bba0-138">這是必要步驟。</span><span class="sxs-lookup"><span data-stu-id="5bba0-138">This step is required.</span></span>

    <span data-ttu-id="5bba0-139">關閉資料庫會清除所有相依性資訊，但不會影響任何未取出的錯誤。</span><span class="sxs-lookup"><span data-stu-id="5bba0-139">Closing a database clears all dependency information, but does not affect any errors that are not retrieved.</span></span>

10. <span data-ttu-id="5bba0-140">使用 [**CloseLog**](merge-closelog.md) 方法來關閉目前的記錄檔。</span><span class="sxs-lookup"><span data-stu-id="5bba0-140">Close the current log file by using the [**CloseLog**](merge-closelog.md) method.</span></span>

    <span data-ttu-id="5bba0-141">如果您有開啟的記錄檔，則需要此步驟。</span><span class="sxs-lookup"><span data-stu-id="5bba0-141">This step is required if you have an open log file.</span></span>

<span data-ttu-id="5bba0-142">使用 [Mergemod.dll](merge-module-automation.md)將模組合併到資料庫之後，必須更新 [媒體資料表](media-table.md) 以描述所需的來源影像版面配置。</span><span class="sxs-lookup"><span data-stu-id="5bba0-142">After the module has been merged into the database using [Mergemod.dll](merge-module-automation.md), the [Media Table](media-table.md) must be updated to describe the desired source image layout.</span></span> <span data-ttu-id="5bba0-143">Mergemod.dll 提供的合併處理不會更新媒體資料表，因為合併模組的取用者可以選取各種配置來源影像的方式。</span><span class="sxs-lookup"><span data-stu-id="5bba0-143">The merge process provided by Mergemod.dll does not update the Media Table because the consumer of the merge module can select various ways to layout the source image.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5bba0-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="5bba0-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5bba0-145">已發行的版本、工具和可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="5bba0-145">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



