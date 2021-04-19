---
description: 在 Windows Installer 安裝期間，安裝程式可以搜尋目錄和該目錄中的檔案。
ms.assetid: ddf624f9-6f85-4ef6-8dfc-8635a25915d0
title: 搜尋目錄和目錄中的檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b4821a53ef0c3f063e943f1f5821b043791dd44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978000"
---
# <a name="searching-for-a-directory-and-a-file-in-the-directory"></a><span data-ttu-id="07927-103">搜尋目錄和目錄中的檔案</span><span class="sxs-lookup"><span data-stu-id="07927-103">Searching for a Directory and a File in the Directory</span></span>

<span data-ttu-id="07927-104">**搜尋目錄和該目錄中的檔案**</span><span class="sxs-lookup"><span data-stu-id="07927-104">**To search for a directory and then a file in that directory**</span></span>

1.  <span data-ttu-id="07927-105">先搜尋目錄。</span><span class="sxs-lookup"><span data-stu-id="07927-105">First search for the directory.</span></span>

    <span data-ttu-id="07927-106">AppDir 必須定義為目錄的有效簽章。</span><span class="sxs-lookup"><span data-stu-id="07927-106">AppDir must be defined as the valid signature of the directory.</span></span> <span data-ttu-id="07927-107">如果 AppDir 未定義為有效的簽章，AppSearch 就不會有尋找檔案的位置，例如，如果搜尋是針對 c： \\ MyDir \\MyApp.exe，則 AppDir 應定義為 c： \\ MyDir。</span><span class="sxs-lookup"><span data-stu-id="07927-107">If AppDir is not defined as a valid signature, AppSearch does not have a place to find the file, for example, if the search is for c:\\MyDir\\MyApp.exe, AppDir should be defined as c:\\MyDir.</span></span> <span data-ttu-id="07927-108">AppDir 可能是藉由在 [DrLocator 資料表](drlocator-table.md)中包含記錄，或由其他方法來定義。</span><span class="sxs-lookup"><span data-stu-id="07927-108">AppDir might be defined by including a record in the [DrLocator Table](drlocator-table.md), or by some other method.</span></span> <span data-ttu-id="07927-109">目錄搜尋的簽章 [資料表](signature-table.md) 中不會包含任何記錄。</span><span class="sxs-lookup"><span data-stu-id="07927-109">No record is included in the [Signature Table](signature-table.md) for the directory search.</span></span> <span data-ttu-id="07927-110">針對檔案搜尋，列出簽章和簽章資料表中的名稱。</span><span class="sxs-lookup"><span data-stu-id="07927-110">For the file search, list the file signature and name in the Signature Table.</span></span> <span data-ttu-id="07927-111">此記錄中的其餘欄位可以是 null，以搜尋任何版本的 MyApp.exe。</span><span class="sxs-lookup"><span data-stu-id="07927-111">The remaining fields in this record can be null to search for any version of MyApp.exe.</span></span>

    <span data-ttu-id="07927-112">[簽名表](signature-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="07927-112">[Signature Table](signature-table.md) (partial)</span></span>

    

    | <span data-ttu-id="07927-113">簽名</span><span class="sxs-lookup"><span data-stu-id="07927-113">Signature</span></span>          | <span data-ttu-id="07927-114">檔案名稱</span><span class="sxs-lookup"><span data-stu-id="07927-114">File Name</span></span>            |
    |--------------------|----------------------|
    | <span data-ttu-id="07927-115">AppFile</span><span class="sxs-lookup"><span data-stu-id="07927-115">AppFile</span></span><br/> | <span data-ttu-id="07927-116">MyApp.exe</span><span class="sxs-lookup"><span data-stu-id="07927-116">MyApp.exe</span></span><br/> |

    

     

2.  <span data-ttu-id="07927-117">使用 [AppSearch 資料表](appsearch-table.md)。</span><span class="sxs-lookup"><span data-stu-id="07927-117">Use the [AppSearch Table](appsearch-table.md).</span></span>

    <span data-ttu-id="07927-118">如果已安裝 AppDir 簽章的目錄，請輸入安裝程式要設定的屬性。</span><span class="sxs-lookup"><span data-stu-id="07927-118">Enter the property that the Installer is to set if the directory with the signature AppDir is installed.</span></span> <span data-ttu-id="07927-119">如果安裝程式發現已安裝此目錄，它會將 MYDIR 設定為目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="07927-119">If the Installer finds this directory is installed, it sets MYDIR to the directory path.</span></span> <span data-ttu-id="07927-120">如果已安裝 MyApp.exe，請輸入安裝程式要設定的屬性。</span><span class="sxs-lookup"><span data-stu-id="07927-120">Enter the property that the Installer is to set if MyApp.exe is installed.</span></span>

    <span data-ttu-id="07927-121">[AppSearch 資料表](appsearch-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="07927-121">[AppSearch Table](appsearch-table.md) (partial)</span></span>

    

    | <span data-ttu-id="07927-122">屬性</span><span class="sxs-lookup"><span data-stu-id="07927-122">Property</span></span>         | <span data-ttu-id="07927-123">簽名</span><span class="sxs-lookup"><span data-stu-id="07927-123">Signature</span></span>          |
    |------------------|--------------------|
    | <span data-ttu-id="07927-124">MYDIR</span><span class="sxs-lookup"><span data-stu-id="07927-124">MYDIR</span></span><br/> | <span data-ttu-id="07927-125">AppDir</span><span class="sxs-lookup"><span data-stu-id="07927-125">AppDir</span></span><br/>  |
    | <span data-ttu-id="07927-126">MYAPP</span><span class="sxs-lookup"><span data-stu-id="07927-126">MYAPP</span></span><br/> | <span data-ttu-id="07927-127">AppFile</span><span class="sxs-lookup"><span data-stu-id="07927-127">AppFile</span></span><br/> |

    

     

3.  <span data-ttu-id="07927-128">使用 [DrLocator 資料表](drlocator-table.md)。</span><span class="sxs-lookup"><span data-stu-id="07927-128">Use the [DrLocator Table](drlocator-table.md).</span></span>

    <span data-ttu-id="07927-129">在父資料行中，輸入定義為目錄路徑的 AppDir 簽章。</span><span class="sxs-lookup"><span data-stu-id="07927-129">Enter in the Parent column the signature, AppDir, that is defined as the path of the directory.</span></span> <span data-ttu-id="07927-130">在 [深度] 資料行中指定要在此目錄中搜尋的子目錄層級數目。</span><span class="sxs-lookup"><span data-stu-id="07927-130">Specify in the Depth column the number of subdirectory levels to search in this directory.</span></span> <span data-ttu-id="07927-131">AppDir 必須定義為目錄簽章。</span><span class="sxs-lookup"><span data-stu-id="07927-131">AppDir must be defined as the directory signature.</span></span> <span data-ttu-id="07927-132">AppDir 可透過如下所示的記錄來定義，或由其他方法來定義。</span><span class="sxs-lookup"><span data-stu-id="07927-132">AppDir may be defined by including a record as shown here or by another method.</span></span>

    [<span data-ttu-id="07927-133">DrLocator 資料表</span><span class="sxs-lookup"><span data-stu-id="07927-133">DrLocator Table</span></span>](drlocator-table.md)

    

    | <span data-ttu-id="07927-134">簽名</span><span class="sxs-lookup"><span data-stu-id="07927-134">Signature</span></span> | <span data-ttu-id="07927-135">父代</span><span class="sxs-lookup"><span data-stu-id="07927-135">Parent</span></span> | <span data-ttu-id="07927-136">路徑</span><span class="sxs-lookup"><span data-stu-id="07927-136">Path</span></span>      | <span data-ttu-id="07927-137">深度</span><span class="sxs-lookup"><span data-stu-id="07927-137">Depth</span></span> |
    |-----------|--------|-----------|-------|
    | <span data-ttu-id="07927-138">AppDir</span><span class="sxs-lookup"><span data-stu-id="07927-138">AppDir</span></span>    |        | <span data-ttu-id="07927-139">C： \\ MyDir</span><span class="sxs-lookup"><span data-stu-id="07927-139">C:\\MyDir</span></span> | <span data-ttu-id="07927-140">0</span><span class="sxs-lookup"><span data-stu-id="07927-140">0</span></span>     |
    | <span data-ttu-id="07927-141">AppFile</span><span class="sxs-lookup"><span data-stu-id="07927-141">AppFile</span></span>   | <span data-ttu-id="07927-142">AppDir</span><span class="sxs-lookup"><span data-stu-id="07927-142">AppDir</span></span> |           | <span data-ttu-id="07927-143">0</span><span class="sxs-lookup"><span data-stu-id="07927-143">0</span></span>     |

    

     

4.  <span data-ttu-id="07927-144">在動作順序中包含 AppSearch 動作。</span><span class="sxs-lookup"><span data-stu-id="07927-144">Include the AppSearch action in the action sequence.</span></span>

    <span data-ttu-id="07927-145">如果在 AppDir 中找到要安裝的 MyApp.exe，安裝程式會將屬性 MYAPP 設定為檔案的位置。</span><span class="sxs-lookup"><span data-stu-id="07927-145">If MyApp.exe is found to be installed in AppDir, the Installer sets the property MYAPP to the location of file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="07927-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="07927-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07927-147">搜尋現有的應用程式、檔案、登錄專案或 .ini 檔案專案</span><span class="sxs-lookup"><span data-stu-id="07927-147">Searching for Existing Applications, Files, Registry Entries or .ini File Entries</span></span>](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)
</dt> </dl>

 

 




