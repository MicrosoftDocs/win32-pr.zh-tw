---
description: 資料表的檔案群組包含所有與檔案相關的 Windows Installer 資料表。
ms.assetid: 8f56328e-ed58-41a1-94b6-266e9c117246
title: 檔案資料表群組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2667a1b9fe2bd9d2f8260523e2386bf7751dce8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974363"
---
# <a name="file-tables-group"></a><span data-ttu-id="4be76-103">檔案資料表群組</span><span class="sxs-lookup"><span data-stu-id="4be76-103">File Tables Group</span></span>

![檔案資料表群組](images/filegrp.png)

<span data-ttu-id="4be76-105">如需此圖表的詳細資訊，請參閱 [實體關聯性圖表圖例](entity-relationship-diagram-legend.md)。</span><span class="sxs-lookup"><span data-stu-id="4be76-105">For more information about this diagram, see the [entity relationship diagram legend](entity-relationship-diagram-legend.md).</span></span>

<span data-ttu-id="4be76-106">安裝程式套件開發人員應該考慮在將應用程式分解成 [元件和功能](components-and-features.md) 之後，以及擴展 [核心資料表群組](core-tables-group.md)之後，填入資料表的檔案資料表群組。</span><span class="sxs-lookup"><span data-stu-id="4be76-106">An installer package developer should consider populating the file table group of tables after breaking the application into [components and features](components-and-features.md) and after populating the [core tables group](core-tables-group.md).</span></span> <span data-ttu-id="4be76-107">檔案資料表群組包含所有屬於安裝的檔案，而且這些檔案大部分都列在檔案 [資料表](file-table.md)中。</span><span class="sxs-lookup"><span data-stu-id="4be76-107">The file table group contains all of the files belonging to the installation and most of these files are listed in the [File table](file-table.md).</span></span> <span data-ttu-id="4be76-108">[目錄資料表](directory-table.md)未顯示在圖中，但與檔案資料表群組密切相關。</span><span class="sxs-lookup"><span data-stu-id="4be76-108">The [Directory table](directory-table.md) is not shown in the figure but is closely related to the file table group.</span></span> <span data-ttu-id="4be76-109">目錄資料表提供安裝的目錄結構。</span><span class="sxs-lookup"><span data-stu-id="4be76-109">The Directory table gives the directory structure of the installation.</span></span>

<span data-ttu-id="4be76-110">資料表的檔案群組包含與檔案相關的所有資料表。</span><span class="sxs-lookup"><span data-stu-id="4be76-110">The file group of tables contains all of the tables that are related to files.</span></span>

-   <span data-ttu-id="4be76-111">[File 資料表](file-table.md)會列出屬於安裝的檔案。</span><span class="sxs-lookup"><span data-stu-id="4be76-111">The [File table](file-table.md) lists files belonging to the installation.</span></span> <span data-ttu-id="4be76-112">檔案資料表中未列出的檔案包含 [媒體] 表格中所列的磁片檔案。</span><span class="sxs-lookup"><span data-stu-id="4be76-112">Files that are not listed in the File table include disk files, which are listed in Media table.</span></span> <span data-ttu-id="4be76-113">因為每個檔案都屬於某個元件，所以檔案資料表在元件資料表中有外部索引鍵。</span><span class="sxs-lookup"><span data-stu-id="4be76-113">Because every file belongs to a component, the File table has an external key into the Component table.</span></span>
-   <span data-ttu-id="4be76-114">[RemoveFile 資料表](removefile-table.md)包含[RemoveFiles 動作](removefiles-action.md)要移除的檔案清單。</span><span class="sxs-lookup"><span data-stu-id="4be76-114">The [RemoveFile table](removefile-table.md) contains a list of files to be removed by the [RemoveFiles action](removefiles-action.md).</span></span>
-   <span data-ttu-id="4be76-115">[字型表](font-table.md)會列出要向系統註冊的字型檔案。</span><span class="sxs-lookup"><span data-stu-id="4be76-115">The [Font table](font-table.md) lists font files to be registered with the system.</span></span>
-   <span data-ttu-id="4be76-116">[SelfReg 資料表](selfreg-table.md)會列出自行註冊之安裝的模組檔案。</span><span class="sxs-lookup"><span data-stu-id="4be76-116">The [SelfReg table](selfreg-table.md) lists module files of the installation that are self-registered.</span></span>
-   <span data-ttu-id="4be76-117">[媒體資料表](media-table.md)會列出屬於安裝的來源媒體和磁片。</span><span class="sxs-lookup"><span data-stu-id="4be76-117">The [Media table](media-table.md) lists the source media and disks belonging to the installation.</span></span>
-   <span data-ttu-id="4be76-118">[BindImage 資料表](bindimage-table.md)會列出系結至可執行檔所匯入之 dll 的檔案。</span><span class="sxs-lookup"><span data-stu-id="4be76-118">The [BindImage table](bindimage-table.md) lists files that are bound to DLLs imported by executables.</span></span>
-   <span data-ttu-id="4be76-119">[MoveFile 資料表](movefile-table.md)會指定在安裝期間要移動的檔案。</span><span class="sxs-lookup"><span data-stu-id="4be76-119">The [MoveFile table](movefile-table.md) specifies which files are moved during the installation.</span></span>
-   <span data-ttu-id="4be76-120">[DuplicateFile 資料表](duplicatefile-table.md)會指定在安裝期間複製的檔案。</span><span class="sxs-lookup"><span data-stu-id="4be76-120">The [DuplicateFile table](duplicatefile-table.md) specifies which files are duplicated during the installation.</span></span>
-   <span data-ttu-id="4be76-121">[IniFile 資料表](inifile-table.md)會列出 .ini 檔案，以及應用程式必須在檔案中設定的資訊。</span><span class="sxs-lookup"><span data-stu-id="4be76-121">The [IniFile table](inifile-table.md) lists the .ini files and the information that the application needs to set in the file.</span></span>
-   <span data-ttu-id="4be76-122">[RemoveIniFile 資料表](removeinifile-table.md)包含應用程式從 .ini 檔案刪除所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="4be76-122">The [RemoveIniFile table](removeinifile-table.md) contains the information an application needs to delete from a .ini file.</span></span>
-   <span data-ttu-id="4be76-123">[環境資料表](environment-table.md)是用來設定環境變數的值。</span><span class="sxs-lookup"><span data-stu-id="4be76-123">The [Environment table](environment-table.md) is used to set the values of environment variables.</span></span>
-   <span data-ttu-id="4be76-124">[圖示表格](icon-table.md)提供在產品公告中複製到檔案的圖示資訊。</span><span class="sxs-lookup"><span data-stu-id="4be76-124">The [Icon table](icon-table.md) provides icon information which is copied to a file as a part of product advertisement.</span></span>
-   <span data-ttu-id="4be76-125">[FileSFPCatalog 資料表](filesfpcatalog-table.md)會將指定的檔案與系統檔案保護類別目錄檔案產生關聯。</span><span class="sxs-lookup"><span data-stu-id="4be76-125">The [FileSFPCatalog table](filesfpcatalog-table.md) associates specified files with system file protection catalog files.</span></span>

    <span data-ttu-id="4be76-126">**Windows Vista、Windows Server 2003 和 WINDOWS XP：** 不支援。</span><span class="sxs-lookup"><span data-stu-id="4be76-126">**Windows Vista, Windows Server 2003 and Windows XP:** Not supported.</span></span>

-   <span data-ttu-id="4be76-127">[SFPCatalog 資料表](sfpcatalog-table.md)包含系統檔案保護目錄。</span><span class="sxs-lookup"><span data-stu-id="4be76-127">The [SFPCatalog table](sfpcatalog-table.md) contains system file protection catalogs.</span></span>

    <span data-ttu-id="4be76-128">**Windows Vista、Windows Server 2003 和 WINDOWS XP：** 不支援。</span><span class="sxs-lookup"><span data-stu-id="4be76-128">**Windows Vista, Windows Server 2003 and Windows XP:** Not supported.</span></span>

-   <span data-ttu-id="4be76-129">[MsiFileHash 資料表](msifilehash-table.md)是用來儲存 Windows Installer 封裝所提供之原始程式檔的128位雜湊。</span><span class="sxs-lookup"><span data-stu-id="4be76-129">The [MsiFileHash table](msifilehash-table.md) is used to store a 128-bit hash of a source file provided by the Windows Installer package.</span></span>

 

 



