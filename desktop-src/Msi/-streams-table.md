---
description: '\_資料流程資料表會列出內嵌的 OLE 資料流程。 這是臨時表，只有在 SQL 語句參考時才會建立。'
ms.assetid: 1e30472d-6ba5-410a-a81b-07ed225dcb69
title: _Streams 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9607097b32acc8a3c2350a00db0b9721a4aa353
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107000274"
---
# <a name="_streams-table"></a><span data-ttu-id="a4e23-104">\_資料流程資料表</span><span class="sxs-lookup"><span data-stu-id="a4e23-104">\_Streams Table</span></span>

<span data-ttu-id="a4e23-105">\_資料流程資料表會列出內嵌的 OLE 資料流程。</span><span class="sxs-lookup"><span data-stu-id="a4e23-105">The \_Streams table lists embedded OLE data streams.</span></span> <span data-ttu-id="a4e23-106">這是臨時表，只有在 SQL 語句參考時才會建立。</span><span class="sxs-lookup"><span data-stu-id="a4e23-106">This is a temporary table, created only when referenced by a SQL statement.</span></span>



| <span data-ttu-id="a4e23-107">Column</span><span class="sxs-lookup"><span data-stu-id="a4e23-107">Column</span></span> | <span data-ttu-id="a4e23-108">類型</span><span class="sxs-lookup"><span data-stu-id="a4e23-108">Type</span></span>                 | <span data-ttu-id="a4e23-109">答案</span><span class="sxs-lookup"><span data-stu-id="a4e23-109">Key</span></span> | <span data-ttu-id="a4e23-110">Nullable</span><span class="sxs-lookup"><span data-stu-id="a4e23-110">Nullable</span></span> |
|--------|----------------------|-----|----------|
| <span data-ttu-id="a4e23-111">Name</span><span class="sxs-lookup"><span data-stu-id="a4e23-111">Name</span></span>   | [<span data-ttu-id="a4e23-112">Text</span><span class="sxs-lookup"><span data-stu-id="a4e23-112">Text</span></span>](text.md)     | <span data-ttu-id="a4e23-113">Y</span><span class="sxs-lookup"><span data-stu-id="a4e23-113">Y</span></span>   | <span data-ttu-id="a4e23-114">N</span><span class="sxs-lookup"><span data-stu-id="a4e23-114">N</span></span>        |
| <span data-ttu-id="a4e23-115">資料</span><span class="sxs-lookup"><span data-stu-id="a4e23-115">Data</span></span>   | [<span data-ttu-id="a4e23-116">二進位</span><span class="sxs-lookup"><span data-stu-id="a4e23-116">Binary</span></span>](binary.md) | <span data-ttu-id="a4e23-117">N</span><span class="sxs-lookup"><span data-stu-id="a4e23-117">N</span></span>   | <span data-ttu-id="a4e23-118">Y</span><span class="sxs-lookup"><span data-stu-id="a4e23-118">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="a4e23-119">資料行</span><span class="sxs-lookup"><span data-stu-id="a4e23-119">Columns</span></span>

<dl> <dt>

<span data-ttu-id="a4e23-120"><span id="Name"></span><span id="name"></span><span id="NAME"></span>名字</span><span class="sxs-lookup"><span data-stu-id="a4e23-120"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="a4e23-121">識別資料流程的唯一索引鍵。</span><span class="sxs-lookup"><span data-stu-id="a4e23-121">A unique key that identifies the stream.</span></span> <span data-ttu-id="a4e23-122">名稱的長度上限為62個字元。</span><span class="sxs-lookup"><span data-stu-id="a4e23-122">The maximum length of Name is 62 characters.</span></span>

</dd> <dt>

<span data-ttu-id="a4e23-123"><span id="Data"></span><span id="data"></span><span id="DATA"></span>資料</span><span class="sxs-lookup"><span data-stu-id="a4e23-123"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Data</span></span>
</dt> <dd>

<span data-ttu-id="a4e23-124">未格式化的二進位資料。</span><span class="sxs-lookup"><span data-stu-id="a4e23-124">The unformatted binary data.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a4e23-125">備註</span><span class="sxs-lookup"><span data-stu-id="a4e23-125">Remarks</span></span>

<span data-ttu-id="a4e23-126">若要複製 OLE 資料流程 (例如， [二進位](binary.md) 資料類型的物件) 從檔案複製到資料庫、在資料流程資料表中建立記錄，並將資料流程的 \_ 名稱輸入此記錄的名稱資料行中，然後使用 [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama)將資料從檔案複製到資料行。</span><span class="sxs-lookup"><span data-stu-id="a4e23-126">To copy an OLE data stream (for example, an object of the [Binary](binary.md) data type) from a file into a database, create a record in the \_Streams table and enter the name of the data stream into the Name column of this record and copy the data from the file into the Data column using [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama).</span></span> <span data-ttu-id="a4e23-127">使用 [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) 將新的記錄插入資料表中。</span><span class="sxs-lookup"><span data-stu-id="a4e23-127">Use [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) to insert the new record into the table.</span></span>

<span data-ttu-id="a4e23-128">若要讀取內嵌于資料庫中的二進位資料串流，請使用 SQL 查詢來尋找並提取包含二進位資料的記錄。</span><span class="sxs-lookup"><span data-stu-id="a4e23-128">To read a binary data stream embedded in a database, use a SQL query to find and to fetch the record containing the binary data.</span></span> <span data-ttu-id="a4e23-129">使用 [**MsiRecordReadStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordreadstream) 將二進位資料讀入緩衝區。</span><span class="sxs-lookup"><span data-stu-id="a4e23-129">Use [**MsiRecordReadStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordreadstream) to read the binary data into a buffer.</span></span>

<span data-ttu-id="a4e23-130">若要將二進位資料流程從某個資料庫移至另一個資料庫，請先將資料匯出到檔案。</span><span class="sxs-lookup"><span data-stu-id="a4e23-130">To move a binary data stream from one database to another, first export the data to a file.</span></span> <span data-ttu-id="a4e23-131">使用 SQL 查詢來尋找檔案中的資料流程，並使用 [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) 將檔案中的資料複製到 \_ 第二個資料庫之資料流程資料表的資料行。</span><span class="sxs-lookup"><span data-stu-id="a4e23-131">Use a SQL query to find the data stream in the file and use [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) to copy the data from the file into Data column of \_Streams table of the second database.</span></span> <span data-ttu-id="a4e23-132">這可確保每個資料庫都有自己的二進位資料複本。</span><span class="sxs-lookup"><span data-stu-id="a4e23-132">This ensures that each database has its own copy of the binary data.</span></span> <span data-ttu-id="a4e23-133">您無法將二進位資料從某個資料庫移至另一個資料庫，只要使用第一個資料庫的資料提取記錄，然後將它插入第二個資料庫即可。</span><span class="sxs-lookup"><span data-stu-id="a4e23-133">You cannot move binary data from one database to another simply by fetching a record with the data from the first database and inserting it into the second database.</span></span>

<span data-ttu-id="a4e23-134">若要刪除資料流程，請先提取記錄，並將資料行設定為 null，然後再更新記錄。</span><span class="sxs-lookup"><span data-stu-id="a4e23-134">To delete a data stream, fetch the record and set the Data column to null before updating the record.</span></span> <span data-ttu-id="a4e23-135">另一種方法是從資料表中移除記錄，使用 [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) 或一般 SQL 查詢來刪除記錄。</span><span class="sxs-lookup"><span data-stu-id="a4e23-135">Another method is to remove the record from the table, deleting it using either [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) or a plain SQL query.</span></span> <span data-ttu-id="a4e23-136">如果資料流程已從資料表中刪除，則不應將資料流程提取到記錄中。</span><span class="sxs-lookup"><span data-stu-id="a4e23-136">A stream should not be fetched into a record if the stream is deleted from the table.</span></span>

<span data-ttu-id="a4e23-137">若要重新命名 OLE 資料流程，請更新記錄的 [名稱] 資料行。</span><span class="sxs-lookup"><span data-stu-id="a4e23-137">To rename an OLE data stream, update the 'Name' column of the record.</span></span>

<span data-ttu-id="a4e23-138">如果使用 SQL (ALTER TABLE 將保留放在此資料表上</span><span class="sxs-lookup"><span data-stu-id="a4e23-138">If a hold is placed on this table using SQL (ALTER TABLE</span></span> <table> <span data-ttu-id="a4e23-139">保留) 或加入具有保留的資料行，必須使用免費發行資料表。</span><span class="sxs-lookup"><span data-stu-id="a4e23-139">HOLD) or a column is added with HOLD, the table must be released using FREE.</span></span> <span data-ttu-id="a4e23-140">在資料表發行或認可之前，不會寫入資料流程。</span><span class="sxs-lookup"><span data-stu-id="a4e23-140">Streams are not written until the table has been released or committed.</span></span>

 

 



