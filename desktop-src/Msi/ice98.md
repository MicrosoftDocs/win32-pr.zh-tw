---
description: ICE98 會驗證 ODBC 資料來源之 ODBCDataSource 資料表的描述欄位。 它會使用 SQLValidDSN 函式來檢查只使用有效的字元，而且描述不超過允許的最大長度。
ms.assetid: ed78db96-10a1-4e42-9147-2309c9ca9c6e
title: ICE98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bf06e97341bd8f15502b1ea1fe43a975dc9cde2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193312"
---
# <a name="ice98"></a><span data-ttu-id="afa12-104">ICE98</span><span class="sxs-lookup"><span data-stu-id="afa12-104">ICE98</span></span>

<span data-ttu-id="afa12-105">ICE98 會驗證 ODBC 資料來源之 [ODBCDataSource 資料表](odbcdatasource-table.md) 的描述欄位。</span><span class="sxs-lookup"><span data-stu-id="afa12-105">ICE98 verifies the description field of the [ODBCDataSource Table](odbcdatasource-table.md) for an ODBC data source.</span></span> <span data-ttu-id="afa12-106">它會使用 **SQLValidDSN** 函式來檢查只使用有效的字元，而且描述不超過允許的最大長度。</span><span class="sxs-lookup"><span data-stu-id="afa12-106">It uses the **SQLValidDSN** function to check that only valid characters are used, and that the description does not exceed the maximum allowed length.</span></span>

## <a name="result"></a><span data-ttu-id="afa12-107">結果</span><span class="sxs-lookup"><span data-stu-id="afa12-107">Result</span></span>

<span data-ttu-id="afa12-108">ICE98 會張貼下列警告。</span><span class="sxs-lookup"><span data-stu-id="afa12-108">ICE98 posts the following warnings.</span></span>



| <span data-ttu-id="afa12-109">ICE98 警告</span><span class="sxs-lookup"><span data-stu-id="afa12-109">ICE98 warning</span></span>                    | <span data-ttu-id="afa12-110">Description</span><span class="sxs-lookup"><span data-stu-id="afa12-110">Description</span></span>                                                                                                                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="afa12-111">資料來源名稱無效。</span><span class="sxs-lookup"><span data-stu-id="afa12-111">The data source name is invalid.</span></span> | <span data-ttu-id="afa12-112">[ODBCDataSource 資料表](odbcdatasource-table.md)之 Description 資料行中的值可能包含不正確字元或太長，這表示它超過 SQL 的 \_ \_ DSN \_ 長度上限32。</span><span class="sxs-lookup"><span data-stu-id="afa12-112">The value in the Description column of the [ODBCDataSource Table](odbcdatasource-table.md) either contains invalid characters or is too long, which means that it exceeds the SQL\_MAX\_DSN\_LENGTH of 32.</span></span> |



 

## <a name="example"></a><span data-ttu-id="afa12-113">範例</span><span class="sxs-lookup"><span data-stu-id="afa12-113">Example</span></span>

<span data-ttu-id="afa12-114">ICE98 會報告下列範例警告：</span><span class="sxs-lookup"><span data-stu-id="afa12-114">ICE98 reports the following warnings for the example:</span></span>

``` syntax
The data source name is invalid: !
The data source name is invalid: <String of length > 32>
```

<span data-ttu-id="afa12-115">[ODBCDataSource 資料表](odbcdatasource-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="afa12-115">[ODBCDataSource Table](odbcdatasource-table.md) (partial)</span></span>



| <span data-ttu-id="afa12-116">DataSource</span><span class="sxs-lookup"><span data-stu-id="afa12-116">DataSource</span></span> | <span data-ttu-id="afa12-117">Description</span><span class="sxs-lookup"><span data-stu-id="afa12-117">Description</span></span>                      |
|------------|----------------------------------|
| <span data-ttu-id="afa12-118">BadChar</span><span class="sxs-lookup"><span data-stu-id="afa12-118">BadChar</span></span>    | <span data-ttu-id="afa12-119">!</span><span class="sxs-lookup"><span data-stu-id="afa12-119">!</span></span>                                |
| <span data-ttu-id="afa12-120">TooLong</span><span class="sxs-lookup"><span data-stu-id="afa12-120">TooLong</span></span>    | <span data-ttu-id="afa12-121"><String of length > 32></span><span class="sxs-lookup"><span data-stu-id="afa12-121"><String of length > 32></span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="afa12-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="afa12-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="afa12-123">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="afa12-123">ICE Reference</span></span>](ice-reference.md)
</dt> <dt>

[<span data-ttu-id="afa12-124">ODBCDataSource 資料表</span><span class="sxs-lookup"><span data-stu-id="afa12-124">ODBCDataSource Table</span></span>](odbcdatasource-table.md)
</dt> </dl>

 

 



