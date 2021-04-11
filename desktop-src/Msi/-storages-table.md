---
description: '[ \_ 儲存體] 資料表會列出內嵌的 OLE 資料儲存體。 這是臨時表，只有在 SQL 語句參考時才會建立。'
ms.assetid: b2f2907d-6966-4b63-9589-c1580f8db574
title: _Storages 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27995dd61c7d25100fc0e1ae2297695e361f44f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849006"
---
# <a name="_storages-table"></a><span data-ttu-id="5a23c-104">\_儲存體資料表</span><span class="sxs-lookup"><span data-stu-id="5a23c-104">\_Storages Table</span></span>

<span data-ttu-id="5a23c-105">[ \_ 儲存體] 資料表會列出內嵌的 OLE 資料儲存體。</span><span class="sxs-lookup"><span data-stu-id="5a23c-105">The \_Storages table lists embedded OLE data storages.</span></span> <span data-ttu-id="5a23c-106">這是臨時表，只有在 SQL 語句參考時才會建立。</span><span class="sxs-lookup"><span data-stu-id="5a23c-106">This is a temporary table, created only when referenced by a SQL statement.</span></span>



| <span data-ttu-id="5a23c-107">Column</span><span class="sxs-lookup"><span data-stu-id="5a23c-107">Column</span></span> | <span data-ttu-id="5a23c-108">類型</span><span class="sxs-lookup"><span data-stu-id="5a23c-108">Type</span></span>                 | <span data-ttu-id="5a23c-109">答案</span><span class="sxs-lookup"><span data-stu-id="5a23c-109">Key</span></span> | <span data-ttu-id="5a23c-110">Nullable</span><span class="sxs-lookup"><span data-stu-id="5a23c-110">Nullable</span></span> |
|--------|----------------------|-----|----------|
| <span data-ttu-id="5a23c-111">Name</span><span class="sxs-lookup"><span data-stu-id="5a23c-111">Name</span></span>   | [<span data-ttu-id="5a23c-112">Text</span><span class="sxs-lookup"><span data-stu-id="5a23c-112">Text</span></span>](text.md)     | <span data-ttu-id="5a23c-113">Y</span><span class="sxs-lookup"><span data-stu-id="5a23c-113">Y</span></span>   | <span data-ttu-id="5a23c-114">N</span><span class="sxs-lookup"><span data-stu-id="5a23c-114">N</span></span>        |
| <span data-ttu-id="5a23c-115">資料</span><span class="sxs-lookup"><span data-stu-id="5a23c-115">Data</span></span>   | [<span data-ttu-id="5a23c-116">二進位</span><span class="sxs-lookup"><span data-stu-id="5a23c-116">Binary</span></span>](binary.md) | <span data-ttu-id="5a23c-117">N</span><span class="sxs-lookup"><span data-stu-id="5a23c-117">N</span></span>   | <span data-ttu-id="5a23c-118">Y</span><span class="sxs-lookup"><span data-stu-id="5a23c-118">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="5a23c-119">資料行</span><span class="sxs-lookup"><span data-stu-id="5a23c-119">Columns</span></span>

<dl> <dt>

<span data-ttu-id="5a23c-120"><span id="Name"></span><span id="name"></span><span id="NAME"></span>名字</span><span class="sxs-lookup"><span data-stu-id="5a23c-120"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="5a23c-121">識別儲存體的唯一索引鍵。</span><span class="sxs-lookup"><span data-stu-id="5a23c-121">A unique key that identifies the storage.</span></span> <span data-ttu-id="5a23c-122">名稱的長度上限是31個字元。</span><span class="sxs-lookup"><span data-stu-id="5a23c-122">The maximum length of Name is 31 characters.</span></span>

</dd> <dt>

<span data-ttu-id="5a23c-123"><span id="Data"></span><span id="data"></span><span id="DATA"></span>資料</span><span class="sxs-lookup"><span data-stu-id="5a23c-123"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Data</span></span>
</dt> <dd>

<span data-ttu-id="5a23c-124">未格式化的二進位資料。</span><span class="sxs-lookup"><span data-stu-id="5a23c-124">The unformatted binary data.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5a23c-125">備註</span><span class="sxs-lookup"><span data-stu-id="5a23c-125">Remarks</span></span>

<span data-ttu-id="5a23c-126">若要將 OLE 儲存體加入至資料庫，請在 [儲存體] 資料表中建立新記錄，並在 [名稱] 資料 \_ 行中輸入儲存體的名稱。</span><span class="sxs-lookup"><span data-stu-id="5a23c-126">To add an OLE storage to a database, create a new record in the \_Storages table and enter the name of the storage into the Name column.</span></span> <span data-ttu-id="5a23c-127">使用 [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) 將資料複製到此記錄的資料行。</span><span class="sxs-lookup"><span data-stu-id="5a23c-127">Use [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) to copy data into the Data column of this record.</span></span> <span data-ttu-id="5a23c-128">最後，使用 [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) 將記錄插入至 [ \_ 儲存體] 資料表。</span><span class="sxs-lookup"><span data-stu-id="5a23c-128">Finally, use [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) to insert the record into the \_Storages table.</span></span>

<span data-ttu-id="5a23c-129">無法從儲存體資料表讀取資料 \_ 。</span><span class="sxs-lookup"><span data-stu-id="5a23c-129">Data cannot be read from the \_Storages table.</span></span> <span data-ttu-id="5a23c-130">不過，您 \_ 可以查詢儲存體資料表來檢查特定儲存體是否存在。</span><span class="sxs-lookup"><span data-stu-id="5a23c-130">However, the \_Storages table can be queried to check for the existence of a specific storage.</span></span> <span data-ttu-id="5a23c-131">這表示，您無法將 OLE 儲存體從某個資料庫移至另一個資料庫。</span><span class="sxs-lookup"><span data-stu-id="5a23c-131">This means that it is not possible to move an OLE storage from one database to another.</span></span> <span data-ttu-id="5a23c-132">您必須改為將原始儲存體檔案匯入至新的資料庫。若要刪除 OLE 儲存區，請提取包含二進位資料的記錄，將儲存資料表中的資料行設定 \_ 為 null，然後更新記錄。</span><span class="sxs-lookup"><span data-stu-id="5a23c-132">You must instead import the original storage file into the new database.To delete an OLE storage, fetch the record containing the binary data, set the Data column in the \_Storages table to null, and then update the record.</span></span> <span data-ttu-id="5a23c-133">替代方法是只使用 [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) 或一般 SQL 查詢來刪除記錄。</span><span class="sxs-lookup"><span data-stu-id="5a23c-133">An alternative method is to simply delete the record using either [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) or a plain SQL query.</span></span>

<span data-ttu-id="5a23c-134">若要重新命名 OLE 儲存區，請更新記錄的名稱資料行。</span><span class="sxs-lookup"><span data-stu-id="5a23c-134">To rename an OLE storage, update the Name column of the record.</span></span>

<span data-ttu-id="5a23c-135">如果使用 SQL (ALTER TABLE 將保留放在此資料表上</span><span class="sxs-lookup"><span data-stu-id="5a23c-135">If a hold is placed on this table using SQL (ALTER TABLE</span></span> <table> <span data-ttu-id="5a23c-136">保留) 或加入具有保留的資料行，必須使用免費發行資料表。</span><span class="sxs-lookup"><span data-stu-id="5a23c-136">HOLD) or a column is added with HOLD, the table must be released using FREE.</span></span> <span data-ttu-id="5a23c-137">在資料表發行或認可之前，不會寫入儲存體。</span><span class="sxs-lookup"><span data-stu-id="5a23c-137">Storages are not written until the table has been released or committed.</span></span>

 

 



