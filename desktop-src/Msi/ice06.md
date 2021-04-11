---
description: ICE06 會檢查每個資料表，以驗證驗證資料表中所列的所有資料行 \_ 都存在於資料表中。 如果資料表不存在， \_ 則會忽略該資料表的任何驗證專案。
ms.assetid: 0c3f21ae-49ea-4cfe-b465-6fdc2b19cbb9
title: ICE06
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e9442d9b2c4089b88299106de875074bd7b0625
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944540"
---
# <a name="ice06"></a><span data-ttu-id="5d3e3-104">ICE06</span><span class="sxs-lookup"><span data-stu-id="5d3e3-104">ICE06</span></span>

<span data-ttu-id="5d3e3-105">ICE06 會檢查每個資料表，以驗證[ \_ 驗證資料表](-validation-table.md)中所列的所有資料行都存在於資料表中。</span><span class="sxs-lookup"><span data-stu-id="5d3e3-105">ICE06 checks every table to validate that all the columns listed in the [\_Validation table](-validation-table.md) are present in the table.</span></span> <span data-ttu-id="5d3e3-106">如果資料表不存在， \_ 則會忽略該資料表的任何驗證專案。</span><span class="sxs-lookup"><span data-stu-id="5d3e3-106">If a table does not exist, any \_Validation entries for that table are ignored.</span></span>

<span data-ttu-id="5d3e3-107">ICE06 的目的是要偵測作者嘗試使用新的 \_ 驗證資料表的實例，該資料表會反映具有尚未更新之舊資料庫的架構變更。</span><span class="sxs-lookup"><span data-stu-id="5d3e3-107">The purpose of ICE06 is to detect instances in which an author tries to use a new \_Validation table that reflects a schema change with an old database that has not been updated.</span></span> <span data-ttu-id="5d3e3-108">ICE06 也會偵測與已改變的資料庫搭配使用之舊驗證資料表的反向案例 \_ 。</span><span class="sxs-lookup"><span data-stu-id="5d3e3-108">ICE06 also detects the reverse case of an old \_Validation table being used with an altered database.</span></span>

<span data-ttu-id="5d3e3-109">請注意， [ICE03](ice03.md) 執行的內部驗證會攔截未在資料 \_ 行目錄中列出的驗證資料表中定義的資料表資料行實例。</span><span class="sxs-lookup"><span data-stu-id="5d3e3-109">Note that the internal validation performed by [ICE03](ice03.md) catches the instance of a table column not defined in the \_Validation table being listed in the columns catalog.</span></span> <span data-ttu-id="5d3e3-110">因此，使用 ICE03 和 ICE06，可確保資料庫中的每個資料行都經過測試。</span><span class="sxs-lookup"><span data-stu-id="5d3e3-110">The use of both ICE03 and ICE06 therefore ensures every column in the database is tested.</span></span>

## <a name="result"></a><span data-ttu-id="5d3e3-111">結果</span><span class="sxs-lookup"><span data-stu-id="5d3e3-111">Result</span></span>

<span data-ttu-id="5d3e3-112">當驗證資料表中定義的資料表資料行 \_ 未列于 Columns 資料表中時，ICE06 會張貼錯誤 \_ 。</span><span class="sxs-lookup"><span data-stu-id="5d3e3-112">ICE06 posts an error when there is a table column defined in the \_Validation table that is not listed in the \_Columns table.</span></span>

## <a name="example"></a><span data-ttu-id="5d3e3-113">範例</span><span class="sxs-lookup"><span data-stu-id="5d3e3-113">Example</span></span>

<span data-ttu-id="5d3e3-114">下列範例 ICE06 會張貼訊息</span><span class="sxs-lookup"><span data-stu-id="5d3e3-114">For the following example ICE06 posts the message</span></span>

<span data-ttu-id="5d3e3-115">資料行：資料表的版本： ModuleSignature 未定義于資料庫中。</span><span class="sxs-lookup"><span data-stu-id="5d3e3-115">Column: Version of Table: ModuleSignature is not defined in database.</span></span>

<span data-ttu-id="5d3e3-116">[ \_ 驗證資料表](-validation-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="5d3e3-116">[\_Validation Table](-validation-table.md) (partial)</span></span>



| <span data-ttu-id="5d3e3-117">資料表</span><span class="sxs-lookup"><span data-stu-id="5d3e3-117">Table</span></span>           | <span data-ttu-id="5d3e3-118">資料行</span><span class="sxs-lookup"><span data-stu-id="5d3e3-118">Column</span></span>   |
|-----------------|----------|
| <span data-ttu-id="5d3e3-119">ModuleSignature</span><span class="sxs-lookup"><span data-stu-id="5d3e3-119">ModuleSignature</span></span> | <span data-ttu-id="5d3e3-120">ModuleID</span><span class="sxs-lookup"><span data-stu-id="5d3e3-120">ModuleID</span></span> |
| <span data-ttu-id="5d3e3-121">ModuleSignature</span><span class="sxs-lookup"><span data-stu-id="5d3e3-121">ModuleSignature</span></span> | <span data-ttu-id="5d3e3-122">版本</span><span class="sxs-lookup"><span data-stu-id="5d3e3-122">Version</span></span>  |



 

<span data-ttu-id="5d3e3-123">[ \_ Columns 資料表](-columns-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="5d3e3-123">[\_Columns Table](-columns-table.md) (partial)</span></span>



| <span data-ttu-id="5d3e3-124">資料表</span><span class="sxs-lookup"><span data-stu-id="5d3e3-124">Table</span></span>           | <span data-ttu-id="5d3e3-125">Number</span><span class="sxs-lookup"><span data-stu-id="5d3e3-125">Number</span></span> | <span data-ttu-id="5d3e3-126">Name</span><span class="sxs-lookup"><span data-stu-id="5d3e3-126">Name</span></span>     |
|-----------------|--------|----------|
| <span data-ttu-id="5d3e3-127">ModuleSignature</span><span class="sxs-lookup"><span data-stu-id="5d3e3-127">ModuleSignature</span></span> | <span data-ttu-id="5d3e3-128">1</span><span class="sxs-lookup"><span data-stu-id="5d3e3-128">1</span></span>      | <span data-ttu-id="5d3e3-129">ModuleID</span><span class="sxs-lookup"><span data-stu-id="5d3e3-129">ModuleID</span></span> |



 

<span data-ttu-id="5d3e3-130">ModuleSignature 資料表的 [版本] 資料行不在資料庫中，或在 [資料行] 資料表中列出 \_ 。</span><span class="sxs-lookup"><span data-stu-id="5d3e3-130">The Version column of the ModuleSignature table is not in the database or listed in the \_Columns table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5d3e3-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="5d3e3-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d3e3-132">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="5d3e3-132">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



