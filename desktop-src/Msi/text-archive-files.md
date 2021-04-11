---
description: 您可以使用 MsiDatabaseExport 或 Database 物件的 Export 方法，將 Windows Installer 資料庫資料表匯出到 ASCII 文字檔。
ms.assetid: 49210242-bd32-4e5c-b782-a132d670fdfe
title: 壓縮檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8baba814fd182a7da5e13fbb26eec257be96ab1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849628"
---
# <a name="text-archive-files"></a><span data-ttu-id="c9b9c-103">壓縮檔案</span><span class="sxs-lookup"><span data-stu-id="c9b9c-103">Text Archive Files</span></span>

<span data-ttu-id="c9b9c-104">您可以使用 [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta)或 [**Database**](database-object.md)物件的 [**Export**](database-export.md)方法，將 Windows Installer 資料庫資料表匯出到 ASCII 文字檔。</span><span class="sxs-lookup"><span data-stu-id="c9b9c-104">The Windows Installer database tables can be exported to ASCII text files by using [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) or the [**Export**](database-export.md) method of the [**Database**](database-object.md) object.</span></span> <span data-ttu-id="c9b9c-105">然後，您可以使用 [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)或 **Database** 物件的 [Import](database-import.md)方法，將這些文字封存檔案中的資訊匯入回 Windows Installer 資料庫。</span><span class="sxs-lookup"><span data-stu-id="c9b9c-105">The information in these text archive files can then be imported back into a Windows Installer database using [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) or the [Import](database-import.md) method of the **Database** object.</span></span>

<span data-ttu-id="c9b9c-106">[msidb.exe](msidb-exe.md)之類的工具都可以匯出和匯入文字保存檔案。</span><span class="sxs-lookup"><span data-stu-id="c9b9c-106">Tools such as [msidb.exe](msidb-exe.md) are capable of exporting and importing text archive files.</span></span> <span data-ttu-id="c9b9c-107">如需可從資料庫匯出及匯入文字封存檔案的[Windows Installer 腳本範例](windows-installer-scripting-examples.md)，請參閱[匯出](export-files.md)檔案和匯[入](import-files.md)檔案。</span><span class="sxs-lookup"><span data-stu-id="c9b9c-107">See [Export Files](export-files.md) and [Import Files](import-files.md) for [Windows Installer Scripting Examples](windows-installer-scripting-examples.md) that can export and import text archive files from a database.</span></span>

> [!Note]  
> <span data-ttu-id="c9b9c-108">文字封存檔案並非用來做為編輯安裝資料庫的方式。</span><span class="sxs-lookup"><span data-stu-id="c9b9c-108">Text archive files are not intended as a means to edit the installation database.</span></span> <span data-ttu-id="c9b9c-109">您應該使用 Windows Installer 表編輯工具（例如 [Orca](orca-exe.md) 或協力廠商工具）來建立和修改安裝套件。</span><span class="sxs-lookup"><span data-stu-id="c9b9c-109">You should use a Windows Installer table editing tool, such as [Orca](orca-exe.md) or a third-party tool, to create and modify an installation package.</span></span>

 

<span data-ttu-id="c9b9c-110">文字封存檔案可用於下列用途。</span><span class="sxs-lookup"><span data-stu-id="c9b9c-110">Text archive files can be used for the following purposes.</span></span>

-   <span data-ttu-id="c9b9c-111">文字封存檔案可以與版本控制系統搭配使用。</span><span class="sxs-lookup"><span data-stu-id="c9b9c-111">Text archive files can be used with version control systems.</span></span>
-   <span data-ttu-id="c9b9c-112">移除浪費的儲存空間，並減少 .msi 檔案的最終大小。</span><span class="sxs-lookup"><span data-stu-id="c9b9c-112">To remove wasted storage space and reduce the final size of .msi files.</span></span> <span data-ttu-id="c9b9c-113">請參閱 [減少 .msi 檔案的大小](reducing-the-size-of-an--msi-file.md)。</span><span class="sxs-lookup"><span data-stu-id="c9b9c-113">See [Reducing the Size of an .msi File](reducing-the-size-of-an--msi-file.md).</span></span>
-   <span data-ttu-id="c9b9c-114">將當地語系化資訊新增至安裝資料庫。</span><span class="sxs-lookup"><span data-stu-id="c9b9c-114">To add localization information to an installation database.</span></span> <span data-ttu-id="c9b9c-115">如需詳細資訊，請參閱匯 [入和匯出資料表的字碼頁處理](code-page-handling-of-imported-and-exported-tables.md)。</span><span class="sxs-lookup"><span data-stu-id="c9b9c-115">For more information, see [Code Page Handling of Imported and Exported Tables](code-page-handling-of-imported-and-exported-tables.md).</span></span>

-   <span data-ttu-id="c9b9c-116">判斷資料庫的字碼頁。</span><span class="sxs-lookup"><span data-stu-id="c9b9c-116">To determine the code page of a database.</span></span> <span data-ttu-id="c9b9c-117">請參閱 [判斷安裝資料庫的字碼頁](determining-an-installation-database-s-code-page.md)。</span><span class="sxs-lookup"><span data-stu-id="c9b9c-117">See [Determining an Installation Database's Code Page](determining-an-installation-database-s-code-page.md).</span></span>
-   <span data-ttu-id="c9b9c-118">若要設定資料庫的字碼頁。</span><span class="sxs-lookup"><span data-stu-id="c9b9c-118">To set the code page of a database.</span></span> <span data-ttu-id="c9b9c-119">請參閱 [設定資料庫的字碼頁](setting-the-code-page-of-a-database.md)。</span><span class="sxs-lookup"><span data-stu-id="c9b9c-119">See [Setting the code page of a database](setting-the-code-page-of-a-database.md).</span></span>
-   <span data-ttu-id="c9b9c-120">提高資料庫資料行的限制。</span><span class="sxs-lookup"><span data-stu-id="c9b9c-120">To increase the limit of a database column.</span></span> <span data-ttu-id="c9b9c-121">使用 [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta)匯出資料表、編輯匯出的 idt 檔案，然後使用 [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)匯入資料表。</span><span class="sxs-lookup"><span data-stu-id="c9b9c-121">Export the table using [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta), edit the exported .idt file, and then import the table using [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta).</span></span> <span data-ttu-id="c9b9c-122">作者無法變更標準資料表中任何資料行的資料行資料類型、null 屬性或當地語系化屬性。</span><span class="sxs-lookup"><span data-stu-id="c9b9c-122">Authors cannot change the column data types, nullability, or localization attributes of any columns in standard tables.</span></span> <span data-ttu-id="c9b9c-123">另請參閱 [撰寫大型套件](authoring-a-large-package.md)。</span><span class="sxs-lookup"><span data-stu-id="c9b9c-123">See also [Authoring a Large Package](authoring-a-large-package.md).</span></span>

<span data-ttu-id="c9b9c-124">下列頁面會解說文字保存頁面及其格式。</span><span class="sxs-lookup"><span data-stu-id="c9b9c-124">The following pages describe text archive pages and their formats.</span></span>

-   [<span data-ttu-id="c9b9c-125">封存檔案格式</span><span class="sxs-lookup"><span data-stu-id="c9b9c-125">Archive File Format</span></span>](archive-file-format.md)
-   [<span data-ttu-id="c9b9c-126">壓縮檔案中的 ASCII 資料</span><span class="sxs-lookup"><span data-stu-id="c9b9c-126">ASCII Data in Text Archive Files</span></span>](ascii-data-in-text-archive-files.md)
-   [<span data-ttu-id="c9b9c-127">\_ForceCodepage</span><span class="sxs-lookup"><span data-stu-id="c9b9c-127">\_ForceCodepage</span></span>](-forcecodepage.md)
-   [<span data-ttu-id="c9b9c-128">\_SummaryInformation</span><span class="sxs-lookup"><span data-stu-id="c9b9c-128">\_SummaryInformation</span></span>](-summaryinformation.md)

 

 



