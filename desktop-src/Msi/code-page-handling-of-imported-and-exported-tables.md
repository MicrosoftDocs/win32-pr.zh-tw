---
description: 您可以使用 MsiDatabaseExport 和 MsiDatabaseImport 匯入和匯出 ASCII 文字封存檔案，以將當地語系化資訊新增至安裝資料庫。
ms.assetid: dc52313b-38e7-43cc-abfd-86966c836fce
title: 匯入和匯出資料表的字碼頁處理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b090bead1fa35b451ed12e0e0da0143b98b8918
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981146"
---
# <a name="code-page-handling-of-imported-and-exported-tables"></a><span data-ttu-id="fb7f1-103">匯入和匯出資料表的字碼頁處理</span><span class="sxs-lookup"><span data-stu-id="fb7f1-103">Code Page Handling of Imported and Exported Tables</span></span>

<span data-ttu-id="fb7f1-104">您可以使用 [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) 和 [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)匯入和匯出 ASCII 文字封存檔案，以將當地語系化資訊新增至安裝資料庫。</span><span class="sxs-lookup"><span data-stu-id="fb7f1-104">You can add localization information to an installation database by importing and exporting ASCII text archive files using [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) and [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta).</span></span> <span data-ttu-id="fb7f1-105">因為資料庫字串集區使用 ANSI 字碼頁，所以資料庫和匯出的 [文字](text-archive-files.md) 封存檔都具有字碼頁。</span><span class="sxs-lookup"><span data-stu-id="fb7f1-105">Because the database string pool uses an ANSI code page, both the database and exported [Text Archive Files](text-archive-files.md) have code pages.</span></span>

<span data-ttu-id="fb7f1-106">從資料庫匯出 [文字保存](text-archive-files.md) 盤案時，封存檔案的字碼頁與父資料庫相同。</span><span class="sxs-lookup"><span data-stu-id="fb7f1-106">When a [Text Archive File](text-archive-files.md) is exported from a database, the code page of the archive file is the same as the parent database.</span></span> <span data-ttu-id="fb7f1-107">如需數值字碼頁的清單，請參閱 [當地語系化錯誤和 ActionText 資料表](localizing-the-error-and-actiontext-tables.md)。</span><span class="sxs-lookup"><span data-stu-id="fb7f1-107">For a list of numeric code pages, see [Localizing the Error and ActionText Tables](localizing-the-error-and-actiontext-tables.md).</span></span>

> [!Note]  
> <span data-ttu-id="fb7f1-108">將資料表匯出到文字封存檔案會轉譯控制字元，以避免與檔案分隔符號發生衝突。</span><span class="sxs-lookup"><span data-stu-id="fb7f1-108">Exporting a table to a text archive file translates the control characters to avoid conflicts with file delimiters.</span></span>

 

## <a name="ascii-text-archive-files"></a><span data-ttu-id="fb7f1-109">ASCII 壓縮檔案</span><span class="sxs-lookup"><span data-stu-id="fb7f1-109">ASCII Text Archive Files</span></span>

<span data-ttu-id="fb7f1-110">[**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta)匯出的 ASCII [文字](text-archive-files.md)封存檔案會以下列格式說明：</span><span class="sxs-lookup"><span data-stu-id="fb7f1-110">The ASCII [Text Archive Files](text-archive-files.md) exported by [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) are explained in the following format:</span></span>

-   <span data-ttu-id="fb7f1-111">資料表資料行的名稱是寫入第一行。</span><span class="sxs-lookup"><span data-stu-id="fb7f1-111">The names of the table columns are written on the first line.</span></span>
-   <span data-ttu-id="fb7f1-112">資料行格式是在第二行寫入。</span><span class="sxs-lookup"><span data-stu-id="fb7f1-112">The column formats are written on the second line.</span></span>
-   <span data-ttu-id="fb7f1-113">如果資料表只包含 ASCII 資料，則文字檔的第三行是資料表名稱，後面接著主鍵清單。</span><span class="sxs-lookup"><span data-stu-id="fb7f1-113">If the table contains only ASCII data, the third line of the text file is the table name followed by a list of the primary keys.</span></span>
-   <span data-ttu-id="fb7f1-114">如果資料表包含非 ASCII 資料，而且資料庫是以數位字碼頁戳記，則字碼頁編號會出現在第三行的開頭。</span><span class="sxs-lookup"><span data-stu-id="fb7f1-114">If the table contains non-ASCII data and the database is stamped with a numeric code page, the code page number appears at the beginning of the third line.</span></span>
-   <span data-ttu-id="fb7f1-115">如果資料庫包含非 ASCII 資料，但資料庫未加上數位字碼頁的戳記，則會在第三行的開頭寫入目前的系統字碼頁編號。</span><span class="sxs-lookup"><span data-stu-id="fb7f1-115">If the database contains non-ASCII data, but the database is not stamped with the numeric code page, the current system code page number is written at the beginning of the third line.</span></span>
-   <span data-ttu-id="fb7f1-116">文字檔的其餘行是指定字碼頁中的資料。</span><span class="sxs-lookup"><span data-stu-id="fb7f1-116">The remaining lines of the text file are the data in the specified code page.</span></span>
-   <span data-ttu-id="fb7f1-117">如果資料表包含資料流程， [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) 會將資料表中的每個資料流程匯出至個別的檔案。</span><span class="sxs-lookup"><span data-stu-id="fb7f1-117">If a table contains streams, [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) exports each stream in the table to a separate file.</span></span>

### <a name="neutral-and-non-neutral-code-pages"></a><span data-ttu-id="fb7f1-118">中性和非中性字碼頁</span><span class="sxs-lookup"><span data-stu-id="fb7f1-118">Neutral and Non-Neutral Code Pages</span></span>

<span data-ttu-id="fb7f1-119">您可以從具有中性字碼頁的資料庫開始，以促進當地語系化：</span><span class="sxs-lookup"><span data-stu-id="fb7f1-119">You can facilitate localization by starting with a database that has a neutral code page:</span></span>

-   <span data-ttu-id="fb7f1-120">空白資料庫具有中性的字碼頁。</span><span class="sxs-lookup"><span data-stu-id="fb7f1-120">A blank database has a neutral code page.</span></span>
-   <span data-ttu-id="fb7f1-121">若資料庫不包含需要以 ASCII 表示之字碼頁的擴充字元，則會有中立的字碼頁。</span><span class="sxs-lookup"><span data-stu-id="fb7f1-121">A database that does not contain extended characters that require a code page to be represented in ASCII has a neutral code page.</span></span>

<span data-ttu-id="fb7f1-122">如需詳細資訊，請參閱 [使用中性程式碼建立資料庫頁面](creating-a-database-with-a-neutral-code-page.md)。</span><span class="sxs-lookup"><span data-stu-id="fb7f1-122">For more information, see [Creating a Database with a Neutral Code Page](creating-a-database-with-a-neutral-code-page.md).</span></span>

<span data-ttu-id="fb7f1-123">中性和非中性的字碼頁具有下列特性：</span><span class="sxs-lookup"><span data-stu-id="fb7f1-123">Neutral and non-neutral code pages have the following characteristics:</span></span>

-   <span data-ttu-id="fb7f1-124">如果將具有非中性字碼頁的 [文字](text-archive-files.md) 封存檔匯入至具有不同非特定字碼頁的資料庫，則在呼叫 [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) 時，安裝程式會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="fb7f1-124">If a [Text Archive File](text-archive-files.md) with a non-neutral code page is imported into a database that has a different non-neutral code page, the Installer returns an error when [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) is called.</span></span>
-   <span data-ttu-id="fb7f1-125">具有中性字碼頁的 [文字保存](text-archive-files.md) 盤案，可以匯入具有任何字碼頁的資料庫中。</span><span class="sxs-lookup"><span data-stu-id="fb7f1-125">A [Text Archive File](text-archive-files.md) that has a neutral code page can be imported into a database that has any code page.</span></span>
-   <span data-ttu-id="fb7f1-126">具有任何字碼頁的 [文字保存](text-archive-files.md) 盤案，可以匯入具有中性字碼頁的資料庫中。</span><span class="sxs-lookup"><span data-stu-id="fb7f1-126">A [Text Archive File](text-archive-files.md) that has any code page can be imported into a database that has a neutral code page.</span></span>
-   <span data-ttu-id="fb7f1-127">使用中性字碼頁將 [文字](text-archive-files.md) 封存檔匯入資料庫中，會將資料庫的字碼頁設定為 [封存檔案代碼] 頁面。</span><span class="sxs-lookup"><span data-stu-id="fb7f1-127">Importing a [Text Archive File](text-archive-files.md) into a database with a neutral code page sets the code page of the database to the archive file code page.</span></span> <span data-ttu-id="fb7f1-128">後續匯入資料庫的所有封存檔案都必須有與第一個檔案相同的字碼頁。</span><span class="sxs-lookup"><span data-stu-id="fb7f1-128">All archive files subsequently imported into the database must have the same code page as the first file.</span></span>

<span data-ttu-id="fb7f1-129">如需詳細資訊，請參閱 [判斷安裝資料庫字碼頁](determining-an-installation-database-s-code-page.md) 和 [設定資料庫的字碼頁](setting-the-code-page-of-a-database.md)。</span><span class="sxs-lookup"><span data-stu-id="fb7f1-129">For more information, see [Determining an Installation Database Code Page](determining-an-installation-database-s-code-page.md) and [Setting the Code Page of a Database](setting-the-code-page-of-a-database.md).</span></span>

<span data-ttu-id="fb7f1-130">[**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta)匯出的 [文字](text-archive-files.md)封存檔案可以與版本控制系統搭配使用。</span><span class="sxs-lookup"><span data-stu-id="fb7f1-130">The [Text Archive Files](text-archive-files.md) that are exported by [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) can be used with version control systems.</span></span> <span data-ttu-id="fb7f1-131">使用 [資料庫函數](database-functions.md) 或資料庫資料表編輯器來編輯資料庫。</span><span class="sxs-lookup"><span data-stu-id="fb7f1-131">Use the [Database Functions](database-functions.md) or a database table editor to edit the database.</span></span>

<span data-ttu-id="fb7f1-132">您可以使用資料庫資料表編輯器或 Windows Installer API，將當地語系化資訊加入至安裝資料庫。</span><span class="sxs-lookup"><span data-stu-id="fb7f1-132">You can add localization information to an installation database by using a database table editor or the Windows Installer API.</span></span> <span data-ttu-id="fb7f1-133">如需詳細資訊，請參閱 [參數字串的字碼頁處理](code-page-handling-of-parameter-strings.md)。</span><span class="sxs-lookup"><span data-stu-id="fb7f1-133">For more information, see [Code Page Handling of Parameter Strings](code-page-handling-of-parameter-strings.md).</span></span>

 

 



