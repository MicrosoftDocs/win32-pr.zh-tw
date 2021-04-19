---
description: '\_SummaryInformation 資料表是與摘要資訊資料流程搭配使用的特殊資料表。 您可以藉由匯出或匯入名為 SummaryInformation. idt 的文字保存檔案，來取得或設定 Windows Installer 資料庫的摘要資訊串流 \_ 。'
ms.assetid: b1b42e03-7a05-46d4-9c42-b87906535adb
title: _SummaryInformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 803b89223db8b6fc8074336109221a8300f7c1ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106976851"
---
# <a name="_summaryinformation"></a><span data-ttu-id="8beeb-104">\_SummaryInformation</span><span class="sxs-lookup"><span data-stu-id="8beeb-104">\_SummaryInformation</span></span>

<span data-ttu-id="8beeb-105">\_SummaryInformation 資料表是與[摘要資訊資料流程](summary-information-stream.md)搭配使用的特殊資料表。</span><span class="sxs-lookup"><span data-stu-id="8beeb-105">The \_SummaryInformation table is a special table used with the [Summary Information Stream](summary-information-stream.md).</span></span> <span data-ttu-id="8beeb-106">您可以藉由匯出或匯入名為 SummaryInformation. idt 的 [文字保存](text-archive-files.md) 盤案，來取得或設定 Windows Installer 資料庫的摘要資訊串流 \_ 。</span><span class="sxs-lookup"><span data-stu-id="8beeb-106">You can get or set the Summary Information Stream of a Windows Installer database by exporting or importing a [text archive file](text-archive-files.md) named \_SummaryInformation.idt.</span></span>

<span data-ttu-id="8beeb-107">匯出之 SummaryInformation 資料表的 idt 檔案 \_ 具有下列格式。</span><span class="sxs-lookup"><span data-stu-id="8beeb-107">The .idt file of an exported \_SummaryInformation table has the following format.</span></span>

-   <span data-ttu-id="8beeb-108">第一個資料列包含以定位字元分隔的資料表資料行名稱： PropertyId 和 Value。</span><span class="sxs-lookup"><span data-stu-id="8beeb-108">The first row contains the table column names separated by tabs: PropertyId and Value.</span></span> <span data-ttu-id="8beeb-109">如需屬性及其識別碼的清單，請參閱 [摘要資訊資料流程屬性集](summary-information-stream-property-set.md) 主題 (PID) 。</span><span class="sxs-lookup"><span data-stu-id="8beeb-109">See the [Summary Information Stream Property Set](summary-information-stream-property-set.md) topic for a list of the properties and their ids (PID).</span></span>
-   <span data-ttu-id="8beeb-110">第二個數據列包含以定位字元分隔的資料行定義。</span><span class="sxs-lookup"><span data-stu-id="8beeb-110">The second row contains the column definitions separated by tabs.</span></span> <span data-ttu-id="8beeb-111">您可以用 idt 封存檔案 [格式](archive-file-format.md)的相同方式來指定資料行定義。</span><span class="sxs-lookup"><span data-stu-id="8beeb-111">The column definitions are specified in the same way as in the basic .idt [archive file format](archive-file-format.md).</span></span> <span data-ttu-id="8beeb-112">PropertyId 資料行可以是不可為 null 的短整數。</span><span class="sxs-lookup"><span data-stu-id="8beeb-112">The PropertyId column can be a non-nullable short integer.</span></span> <span data-ttu-id="8beeb-113">值資料行可以是不可為 null 的可當地語系化字串（長度為255個字元）。</span><span class="sxs-lookup"><span data-stu-id="8beeb-113">The Value column can be a non-nullable localizable string 255 characters long.</span></span>
-   <span data-ttu-id="8beeb-114">第三個數據列是資料表名稱，而主鍵資料行名稱是以 tab 分隔： \_ SummaryInformation 和 PropertyId。</span><span class="sxs-lookup"><span data-stu-id="8beeb-114">The third row is the table name and the primary key column name separated by tabs: \_SummaryInformation and PropertyId.</span></span>
-   <span data-ttu-id="8beeb-115">檔案中的其餘資料列代表 PID 和相關聯的值（以 tab 分隔）。</span><span class="sxs-lookup"><span data-stu-id="8beeb-115">The remaining rows in the file represent the PID and associated value, separated by tabs.</span></span> <span data-ttu-id="8beeb-116">SummaryInformation 中的日期和時間 \_ 格式如下： YYYY/MM/DD hh：： MM：： ss。</span><span class="sxs-lookup"><span data-stu-id="8beeb-116">Date and time in\_SummaryInformation are in the format: YYYY/MM/DD hh::mm::ss.</span></span> <span data-ttu-id="8beeb-117">例如，1999/03/22 15:25:45。</span><span class="sxs-lookup"><span data-stu-id="8beeb-117">For example, 1999/03/22 15:25:45.</span></span>

<span data-ttu-id="8beeb-118">下列是 idt 格式之資料庫的 [摘要資訊資料流程](summary-information-stream.md) 範例。</span><span class="sxs-lookup"><span data-stu-id="8beeb-118">The following is an example of the [Summary Information Stream](summary-information-stream.md) of a database in .idt format.</span></span>

``` syntax
PropertyId   Value
i2  l255
_SummaryInformation PropertyId
1   1252
2   Installation Database
3   Internal Quick Test
4   Microsoft Corporation
5   Installer,MSI,Database
6   Installer Internal Release Quick Test
7   Intel;1033
9   {00000002-0001-0000-0000-624474736554}
12  1999/06/21
14  110
15  1
18  Windows Installer
```

<span data-ttu-id="8beeb-119">當您使用 [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)或 [**Database**](database-object.md)物件的 [import](database-import.md)方法，將名為 SummaryInformation 的文字保存資料表匯入到 \_ 安裝程式資料庫時，您會在資料庫中寫入 "05SummaryInformation" 資料流程。</span><span class="sxs-lookup"><span data-stu-id="8beeb-119">When you use [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) or the [Import](database-import.md) method of the [**Database**](database-object.md) object to import a text archive table named \_SummaryInformation into an installer database, you write the "05SummaryInformation" stream in the database.</span></span>

 

 



