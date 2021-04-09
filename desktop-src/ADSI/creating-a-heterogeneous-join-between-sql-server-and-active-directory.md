---
title: 在 SQL Server & Active Directory 之間建立異類聯結
description: Fabrikam corporation 的所有員工都會每隔六個月檢查一次。
ms.assetid: 16f605ae-7f6c-4429-a379-47686618b15d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93e4e6b7f3bfd9c853d9ff262365d49c1f3a8d5c
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "103932953"
---
# <a name="creating-a-heterogeneous-join-between-sql-server--active-directory"></a><span data-ttu-id="ac534-103">在 SQL Server & Active Directory 之間建立異類聯結</span><span class="sxs-lookup"><span data-stu-id="ac534-103">Creating a Heterogeneous Join between SQL Server & Active Directory</span></span>

<span data-ttu-id="ac534-104">Fabrikam corporation 的所有員工都會每隔六個月檢查一次。</span><span class="sxs-lookup"><span data-stu-id="ac534-104">All employees at the Fabrikam corporation are reviewed every six months.</span></span> <span data-ttu-id="ac534-105">審核分級會儲存在「人力資源」資料庫的 SQL Server 中。</span><span class="sxs-lookup"><span data-stu-id="ac534-105">Review ratings are stored in the Human Resource database in SQL Server.</span></span> <span data-ttu-id="ac534-106">若要建立此資料的視圖，Joe Worden 企業系統管理員必須先建立員工效能審核表。</span><span class="sxs-lookup"><span data-stu-id="ac534-106">To create a view of this data, Joe Worden, the enterprise administrator, must first create an employee performance review table.</span></span>

<span data-ttu-id="ac534-107">在 SQL Query Analyzer 中，Joe 將建立一個稱為 EMP \_ 評論的表格，其中包含三個數據行來保存員工名稱、評論日期，以及員工所收到的評等。</span><span class="sxs-lookup"><span data-stu-id="ac534-107">In the SQL Query Analyzer, Joe is going to create a table called EMP\_REVIEW that will contain three columns to hold the name of the employee, the date of the review, and the rating that the employee received.</span></span>


```sql
CREATE TABLE EMP_REVIEW
(
userName varChar(40),
reviewDate datetime,
rating decimal 
)
```



<span data-ttu-id="ac534-108">Joe 接著可以插入一些記錄。</span><span class="sxs-lookup"><span data-stu-id="ac534-108">Joe can then insert a few records.</span></span>


```sql
INSERT EMP_REVIEW VALUES('Julie Adam', '2/15/1999', 4 )
INSERT EMP_REVIEW VALUES('Julie Bankert', '7/15/1999', 5 )
INSERT EMP_REVIEW VALUES('Chris Gray', '2/15/1999', 3 )
INSERT EMP_REVIEW VALUES('Chris Gray', '7/15/1999', 4 )
```



<span data-ttu-id="ac534-109">現在 Joe 可以將 Active Directory 的使用者物件加入 SQL Server 資料表中。</span><span class="sxs-lookup"><span data-stu-id="ac534-109">Now Joe can join the Active Directory user objects to the SQL Server table.</span></span>

<span data-ttu-id="ac534-110">在此範例中， [SELECT](https://msdn.microsoft.com/library/Aa259187.aspx) 語句包含將從目錄服務取得並 SQL Server 的資料清單。</span><span class="sxs-lookup"><span data-stu-id="ac534-110">In this example, the [SELECT](https://msdn.microsoft.com/library/Aa259187.aspx) statement contains the list of data that will be obtained from the directory service and SQL Server.</span></span> <span data-ttu-id="ac534-111">[From](https://msdn.microsoft.com/library/Aa258869.aspx)語句包含連結目錄伺服器的名稱，此資訊將從中取得，在此案例中為 viewADUsers。</span><span class="sxs-lookup"><span data-stu-id="ac534-111">The [FROM](https://msdn.microsoft.com/library/Aa258869.aspx) statement contains the name of the linked directory server where this information will be obtained from, in this case, viewADUsers.</span></span> <span data-ttu-id="ac534-112">[WHERE](https://msdn.microsoft.com/library/Aa260674.aspx)語句會提供搜尋條件。</span><span class="sxs-lookup"><span data-stu-id="ac534-112">The [WHERE](https://msdn.microsoft.com/library/Aa260674.aspx) statement provides the search conditions.</span></span> <span data-ttu-id="ac534-113">在此範例中，它會依目錄服務中的名稱進行搜尋，此服務會設定為上一個工作中所輸入的 SQL 使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="ac534-113">In this example, it is searching by the name in the directory service, which is set to the SQL userName entered in the previous task.</span></span>


```sql
SELECT ADsPath, userName, title, ReviewDate, Rating 
FROM EMP_REVIEW, viewADUsers
WHERE userName = Name
```



<span data-ttu-id="ac534-114">上一個命令會取得 SQL Server 和 Active Directory 的結果。</span><span class="sxs-lookup"><span data-stu-id="ac534-114">The previous command gets the result from both SQL Server and Active Directory.</span></span> <span data-ttu-id="ac534-115">AdsPath 和 title 來自 Active Directory，而 userName、>reviewdate 和評等則來自 SQL 資料表。</span><span class="sxs-lookup"><span data-stu-id="ac534-115">AdsPath and title are from Active Directory, whereas userName, ReviewDate, and Rating are from the SQL table.</span></span> <span data-ttu-id="ac534-116">他甚至可以為此聯結建立另一個 view。</span><span class="sxs-lookup"><span data-stu-id="ac534-116">He can even create another view for this join.</span></span>


```sql
CREATE VIEW reviewReport
AS
SELECT ADsPath, userName, title, ReviewDate, Rating 
FROM EMP_REVIEW, viewADUsers
WHERE userName = Name
GO
SELECT * FROM reviewReport
```



 

 




