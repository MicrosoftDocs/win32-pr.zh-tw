---
description: Windows Installer 可以在安裝期間搜尋特定的檔案或目錄。 檔案或目錄搜尋可用來判斷使用者是否已安裝應用程式的版本。
ms.assetid: a78ca652-c730-4231-80f2-60cf0bad5b02
title: 搜尋現有的應用程式、檔案、登錄專案或 .ini 檔案專案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a41d0ebf8943d1fb82b7c0901a62230e6befdcba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106986398"
---
# <a name="searching-for-existing-applications-files-registry-entries-or-ini-file-entries"></a><span data-ttu-id="972e8-104">搜尋現有的應用程式、檔案、登錄專案或 .ini 檔案專案</span><span class="sxs-lookup"><span data-stu-id="972e8-104">Searching for Existing Applications, Files, Registry Entries or .ini File Entries</span></span>

<span data-ttu-id="972e8-105">Windows Installer 可以在安裝期間搜尋特定的檔案或目錄。</span><span class="sxs-lookup"><span data-stu-id="972e8-105">Windows Installer can search for a specific file or directory during an installation.</span></span> <span data-ttu-id="972e8-106">檔案或目錄搜尋可用來判斷使用者是否已安裝應用程式的版本。</span><span class="sxs-lookup"><span data-stu-id="972e8-106">File or directory searches are used to determine whether a user has already installed a version of an application.</span></span>

<span data-ttu-id="972e8-107">[AppSearch 動作](appsearch-action.md) 會在使用者系統中搜尋 [AppSearch 資料表](appsearch-table.md)中指定的檔案簽章。</span><span class="sxs-lookup"><span data-stu-id="972e8-107">[AppSearch Action](appsearch-action.md) searches a user system for file signatures that are specified in the [AppSearch Table](appsearch-table.md).</span></span> <span data-ttu-id="972e8-108">如果 AppSearch 動作找到具有指定簽章的已安裝檔案或目錄，它會將對應的屬性（也會在 AppSearch 資料表中指定）設定為檔案或目錄的位置。</span><span class="sxs-lookup"><span data-stu-id="972e8-108">If the AppSearch action finds an installed file or directory with the specified signature, it sets a corresponding property, also specified in the AppSearch Table, to the location of the file or directory.</span></span> <span data-ttu-id="972e8-109">搜尋檔案時，檔案簽章也必須列在簽章 [資料表](signature-table.md)中。</span><span class="sxs-lookup"><span data-stu-id="972e8-109">When searching for a file, the file signature must also be listed in the [Signature Table](signature-table.md).</span></span> <span data-ttu-id="972e8-110">如果檔案簽章列在 AppSearch 資料表中，而且未列于簽章資料表中，則搜尋會尋找目錄、登錄專案或 .ini 檔案專案。</span><span class="sxs-lookup"><span data-stu-id="972e8-110">If a file signature is listed in the AppSearch Table and is not listed in the Signature Table, the search looks for a directory, registry entry, or .ini file entry.</span></span>

<span data-ttu-id="972e8-111">為了加速搜尋使用者電腦，安裝程式會依所列的順序來查詢下列定位器資料庫資料表，以取得建議的搜尋位置：</span><span class="sxs-lookup"><span data-stu-id="972e8-111">To expedite the search of a user computer, the Installer queries the following locator database tables in the order listed for a suggested search location:</span></span>

-   <span data-ttu-id="972e8-112">如果檔案簽章列在 [CompLocator 資料表](complocator-table.md)中，建議的搜尋位置是元件的金鑰路徑。</span><span class="sxs-lookup"><span data-stu-id="972e8-112">If the file signature is listed in the [CompLocator Table](complocator-table.md), the suggested search location is the key path of a component.</span></span> <span data-ttu-id="972e8-113">如果簽章未列在此資料表中，或未安裝在建議的位置，則安裝程式會查詢 [RegLocator 資料表](reglocator-table.md) 中的建議位置。</span><span class="sxs-lookup"><span data-stu-id="972e8-113">If the signature is not listed in this table or not installed at the suggested location, the Installer queries the [RegLocator Table](reglocator-table.md) for a suggested location.</span></span>
-   <span data-ttu-id="972e8-114">如果檔案簽章列在 [RegLocator 資料表](reglocator-table.md)中，建議的搜尋位置是在使用者登錄中寫入的金鑰路徑。</span><span class="sxs-lookup"><span data-stu-id="972e8-114">If the file signature is listed in the [RegLocator Table](reglocator-table.md), the suggested search location is a key path written in the user registry.</span></span> <span data-ttu-id="972e8-115">如果簽章未列在此資料表中，或未安裝在建議的位置，則安裝程式會查詢 [IniLocator 資料表](inilocator-table.md) 中的建議位置。</span><span class="sxs-lookup"><span data-stu-id="972e8-115">If the signature is not listed in this table or not installed at the suggested location, the Installer queries the [IniLocator Table](inilocator-table.md) for a suggested location.</span></span>
-   <span data-ttu-id="972e8-116">如果檔案簽章列在 [IniLocator 資料表](inilocator-table.md)中，建議的搜尋位置是寫入 .ini 檔案的金鑰路徑，該檔案存在於使用者系統的預設 Windows 目錄中。</span><span class="sxs-lookup"><span data-stu-id="972e8-116">If the file signature is listed in the [IniLocator Table](inilocator-table.md), the suggested search location is a key path written in an .ini file present in the default Windows directory of a user system.</span></span> <span data-ttu-id="972e8-117">如果簽章未列在此資料表中，或未安裝在建議的位置，則安裝程式會查詢 [DrLocator 資料表](drlocator-table.md) 中的建議位置。</span><span class="sxs-lookup"><span data-stu-id="972e8-117">If the signature is not listed in this table or not installed at the suggested location, the Installer queries the [DrLocator Table](drlocator-table.md) for a suggested location.</span></span>
-   <span data-ttu-id="972e8-118">如果檔案簽章列在 [DrLocator 資料表](drlocator-table.md)中，建議的搜尋位置是使用者目錄樹狀結構中的路徑。</span><span class="sxs-lookup"><span data-stu-id="972e8-118">If the file signature is listed in the [DrLocator Table](drlocator-table.md), the suggested search location is a path in the user directory tree.</span></span> <span data-ttu-id="972e8-119">下表也會指定在此位置底下搜尋的子目錄層級深度。</span><span class="sxs-lookup"><span data-stu-id="972e8-119">The depth of subdirectory levels to search below this location is also specified in this table.</span></span>

<span data-ttu-id="972e8-120">當安裝程式第一次在建議的位置找到檔案簽章時，它會停止搜尋此檔案或目錄，並在 [AppSearch 資料表](appsearch-table.md)中設定對應的屬性。</span><span class="sxs-lookup"><span data-stu-id="972e8-120">The first time the Installer finds the file signature at a suggested location, it stops searching for this file or directory, and sets the corresponding property in the [AppSearch Table](appsearch-table.md).</span></span> <span data-ttu-id="972e8-121">如需詳細資訊，請參閱下列：</span><span class="sxs-lookup"><span data-stu-id="972e8-121">For more information, see the following:</span></span>

-   [<span data-ttu-id="972e8-122">搜尋檔案的所有固定磁片磁碟機</span><span class="sxs-lookup"><span data-stu-id="972e8-122">Searching All Fixed Drives for a File</span></span>](searching-all-fixed-drives-for-a-file.md)
-   [<span data-ttu-id="972e8-123">搜尋目錄和目錄中的檔案</span><span class="sxs-lookup"><span data-stu-id="972e8-123">Searching for a Directory and a File in the Directory</span></span>](searching-for-a-directory-and-a-file-in-the-directory.md)
-   [<span data-ttu-id="972e8-124">搜尋檔案並建立保存檔案路徑的屬性</span><span class="sxs-lookup"><span data-stu-id="972e8-124">Searching for a File and Creating a Property Holding the File's Path</span></span>](searching-for-a-file-and-creating-a-property-holding-the-file-s-path.md)
-   [<span data-ttu-id="972e8-125">搜尋特定位置中的檔案</span><span class="sxs-lookup"><span data-stu-id="972e8-125">Searching for a File in a Specific Location</span></span>](searching-for-a-file-in-a-specific-location.md)
-   [<span data-ttu-id="972e8-126">搜尋登錄專案，並建立保存登錄值的屬性</span><span class="sxs-lookup"><span data-stu-id="972e8-126">Searching for a Registry Entry and Creating a Property Holding the Value of the Registry</span></span>](searching-for-a-registry-entry-and-creating-a-property-holding-the-value-of-the-registry.md)

 

 



