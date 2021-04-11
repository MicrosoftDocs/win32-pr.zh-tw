---
description: 當僅包含 ASCII 字元的資料表匯出到文字封存檔案時，idt 檔案會遵守基本的封存檔案格式。
ms.assetid: 105d2b85-c6e1-4719-83b4-1693c14ef4f4
title: 壓縮檔案中的 ASCII 資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d43deeb7918b75a71770ab9d09535972f6e8bb4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848964"
---
# <a name="ascii-data-in-text-archive-files"></a><span data-ttu-id="9f25f-103">壓縮檔案中的 ASCII 資料</span><span class="sxs-lookup"><span data-stu-id="9f25f-103">ASCII Data in Text Archive Files</span></span>

<span data-ttu-id="9f25f-104">當僅包含 ASCII 字元的資料表匯出到 [文字](text-archive-files.md)封存檔案時，idt 檔案會遵守基本的封存檔案 [格式](archive-file-format.md)。</span><span class="sxs-lookup"><span data-stu-id="9f25f-104">When a table that contains only ASCII characters is exported to a [text archive file](text-archive-files.md), the .idt file adheres to the basic [archive file format](archive-file-format.md).</span></span> <span data-ttu-id="9f25f-105">如果資料表包含非 ASCII 資訊，封存檔案的格式會擴充以包含字碼頁資訊。</span><span class="sxs-lookup"><span data-stu-id="9f25f-105">If the table contains non-ASCII information, the format of the archive file is extended to include code page information.</span></span>

## <a name="text-archive-files-that-contain-only-ascii-characters"></a><span data-ttu-id="9f25f-106">只包含 ASCII 字元的壓縮檔案</span><span class="sxs-lookup"><span data-stu-id="9f25f-106">Text archive files that contain only ASCII characters</span></span>

<span data-ttu-id="9f25f-107">當僅包含 ASCII 字元的資料表匯出到封存檔案時，idt 檔案會是基本的封存 [檔案格式](archive-file-format.md)。</span><span class="sxs-lookup"><span data-stu-id="9f25f-107">When a table that contains only ASCII characters is exported to an archive file, the .idt file is in the basic [archive file format](archive-file-format.md).</span></span> <span data-ttu-id="9f25f-108">資料表中的每個資料流程都會匯出為副檔名為 ibd 的檔案。</span><span class="sxs-lookup"><span data-stu-id="9f25f-108">Each stream in the table is exported as a file with an .ibd file name extension.</span></span> <span data-ttu-id="9f25f-109">Ibd 檔案會儲存在與資料表同名的資料夾中。</span><span class="sxs-lookup"><span data-stu-id="9f25f-109">The .ibd files are stored in a folder with the same name as the table.</span></span> <span data-ttu-id="9f25f-110">例如，請考慮匯出下列 [二進位](binary-table.md) 資料表。</span><span class="sxs-lookup"><span data-stu-id="9f25f-110">For example, consider the export of the following [Binary](binary-table.md) table.</span></span>



| <span data-ttu-id="9f25f-111">Name</span><span class="sxs-lookup"><span data-stu-id="9f25f-111">Name</span></span>  | <span data-ttu-id="9f25f-112">資料</span><span class="sxs-lookup"><span data-stu-id="9f25f-112">Data</span></span>      |
|-------|-----------|
| <span data-ttu-id="9f25f-113">書籍</span><span class="sxs-lookup"><span data-stu-id="9f25f-113">Books</span></span> | <span data-ttu-id="9f25f-114">Ibd</span><span class="sxs-lookup"><span data-stu-id="9f25f-114">Books.ibd</span></span> |
| <span data-ttu-id="9f25f-115">Cars</span><span class="sxs-lookup"><span data-stu-id="9f25f-115">Cars</span></span>  | <span data-ttu-id="9f25f-116">車輛. ibd</span><span class="sxs-lookup"><span data-stu-id="9f25f-116">Cars.ibd</span></span>  |



 

<span data-ttu-id="9f25f-117">匯出此資料表之後的目錄結構如下所示。</span><span class="sxs-lookup"><span data-stu-id="9f25f-117">The directory structure after exporting this table is as follows.</span></span> <span data-ttu-id="9f25f-118">資料庫資料表中的資訊會匯出為 idt。</span><span class="sxs-lookup"><span data-stu-id="9f25f-118">The information in the database table is exported to Binary.idt.</span></span> <span data-ttu-id="9f25f-119">系統會將兩個二進位資料串流匯出至 ibd 和 ibd 儲存在名為 Binary 的資料夾中。</span><span class="sxs-lookup"><span data-stu-id="9f25f-119">The two streams of binary data are exported to Book.ibd and Cars.ibd saved in the folder named Binary.</span></span>

``` syntax
Binary.idt
[Binary]
    Books.ibd
    Cars.ibd
```

<span data-ttu-id="9f25f-120">Idt 封存檔案是基本的封存檔案 [格式](archive-file-format.md) ，看起來會如下所示。</span><span class="sxs-lookup"><span data-stu-id="9f25f-120">The Binary.idt archive file is in the basic [archive file format](archive-file-format.md) and would look as follows.</span></span>

``` syntax
Name Data
s72 v0
Binary  Name
Books   Books.ibd
Cars    Cars.ibd
```

## <a name="text-archive-files-that-contain-non--ascii-characters"></a><span data-ttu-id="9f25f-121">包含非 ASCII 字元的文字保存檔案</span><span class="sxs-lookup"><span data-stu-id="9f25f-121">Text archive files that contain non- ASCII characters</span></span>

<span data-ttu-id="9f25f-122">如果檔案包含非 ASCII 資料，則會擴充 idt 檔案的基本封存 [檔案格式](archive-file-format.md) ，以包含字碼頁資訊。</span><span class="sxs-lookup"><span data-stu-id="9f25f-122">If the file contains non-ASCII data, the basic [archive file format](archive-file-format.md) of the .idt file is extended to include code page information.</span></span> <span data-ttu-id="9f25f-123">Idt 資料表中的第三個數據列是數值字碼頁，後面接著以 tab 分隔的資料表名稱和主鍵資料行名稱。</span><span class="sxs-lookup"><span data-stu-id="9f25f-123">The third row in the .idt table is the numeric code page followed by the table name and primary key column names separated by tabs.</span></span>

> [!Note]  
> <span data-ttu-id="9f25f-124">包含非 ASCII 資訊的 idt 檔案應該以 ASCII 格式儲存。</span><span class="sxs-lookup"><span data-stu-id="9f25f-124">An .idt file that contains non-ASCII information should be saved in the ASCII format.</span></span> <span data-ttu-id="9f25f-125">例如，文字封存檔案可以包含編碼為 UTF-8 的資料行和資料表名稱，但封存檔案本身應該是 ASCII。</span><span class="sxs-lookup"><span data-stu-id="9f25f-125">For example, a text archive file can contain the column and table names encoded as UTF-8, but the archive file itself should be ASCII.</span></span>

 

<span data-ttu-id="9f25f-126">下列當地語系化為法文的 ActionText 資料表會包含非 ASCII 資訊。</span><span class="sxs-lookup"><span data-stu-id="9f25f-126">The following ActionText table localized into French would contain non-ASCII information.</span></span> <span data-ttu-id="9f25f-127">用於法文字串的數值字碼頁為1252。</span><span class="sxs-lookup"><span data-stu-id="9f25f-127">The numeric code page used for French strings is 1252.</span></span>



| <span data-ttu-id="9f25f-128">動作</span><span class="sxs-lookup"><span data-stu-id="9f25f-128">Action</span></span>    | <span data-ttu-id="9f25f-129">描述</span><span class="sxs-lookup"><span data-stu-id="9f25f-129">Description</span></span>                                  | <span data-ttu-id="9f25f-130">範本</span><span class="sxs-lookup"><span data-stu-id="9f25f-130">Template</span></span> |
|-----------|----------------------------------------------|----------|
| <span data-ttu-id="9f25f-131">通告</span><span class="sxs-lookup"><span data-stu-id="9f25f-131">ADVERTISE</span></span> | <span data-ttu-id="9f25f-132">發行集 d'informations sur l'application</span><span class="sxs-lookup"><span data-stu-id="9f25f-132">Publication d'informations sur l'application</span></span> |          |



 

<span data-ttu-id="9f25f-133">匯出的封存檔案（ActionText. idt）如下所示。</span><span class="sxs-lookup"><span data-stu-id="9f25f-133">The exported archive file, ActionText.idt, would be as follows.</span></span>

``` syntax
Action   Description Template
s72 L0  L0
1252    ActionText  Action
Advertise   Publication d'informations sur l'application
```

> [!Note]  
> <span data-ttu-id="9f25f-134">如果文字保存檔案包含非 ASCII 資料，封存檔案就會包含字碼頁資訊。</span><span class="sxs-lookup"><span data-stu-id="9f25f-134">If a text archive file contains non-ASCII data, the archive file includes code page information.</span></span> <span data-ttu-id="9f25f-135">具有字碼頁資訊的封存檔案只能匯回至該確切字碼頁的資料庫，或匯入至非語言相關的資料庫中。</span><span class="sxs-lookup"><span data-stu-id="9f25f-135">Archive files with code page information can only be imported back into a database of that exact code page or into a language neutral database.</span></span> <span data-ttu-id="9f25f-136">如果是中性語言的資料庫，則字碼頁會設定為封存檔案的字碼頁。</span><span class="sxs-lookup"><span data-stu-id="9f25f-136">In the case of a language neutral database, the code page is set to the code page of the archive file.</span></span> <span data-ttu-id="9f25f-137">如需 Windows Installer 如何處理字碼頁的詳細資訊，請參閱 [ (Windows Installer) 中的字碼頁處理 ](code-page-handling-windows-installer-.md)小節。</span><span class="sxs-lookup"><span data-stu-id="9f25f-137">For more information about how Windows Installer handles code pages see the section [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md).</span></span>

 

 

 



