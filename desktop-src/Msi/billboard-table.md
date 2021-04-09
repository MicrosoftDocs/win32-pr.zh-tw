---
description: 佈告欄資料表列出完整使用者介面中顯示的佈告欄控制項。
ms.assetid: bb8c1d7c-aa1d-43cc-9fb4-3a0ad75c4615
title: 佈告欄資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65a561eb629e07b25437d6e5ce12b58bb0d7dd20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944000"
---
# <a name="billboard-table"></a><span data-ttu-id="fbf25-103">佈告欄資料表</span><span class="sxs-lookup"><span data-stu-id="fbf25-103">Billboard Table</span></span>

<span data-ttu-id="fbf25-104">佈告欄資料表列出完整使用者介面中顯示的 [佈告欄控制項](billboard-control.md) 。</span><span class="sxs-lookup"><span data-stu-id="fbf25-104">The Billboard table lists the [Billboard controls](billboard-control.md) displayed in the full user interface.</span></span>

<span data-ttu-id="fbf25-105">佈告欄資料表有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="fbf25-105">The Billboard table has the following columns.</span></span>



| <span data-ttu-id="fbf25-106">Column</span><span class="sxs-lookup"><span data-stu-id="fbf25-106">Column</span></span>    | <span data-ttu-id="fbf25-107">類型</span><span class="sxs-lookup"><span data-stu-id="fbf25-107">Type</span></span>                         | <span data-ttu-id="fbf25-108">答案</span><span class="sxs-lookup"><span data-stu-id="fbf25-108">Key</span></span> | <span data-ttu-id="fbf25-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="fbf25-109">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="fbf25-110">廣告 牌</span><span class="sxs-lookup"><span data-stu-id="fbf25-110">Billboard</span></span> | [<span data-ttu-id="fbf25-111">識別碼</span><span class="sxs-lookup"><span data-stu-id="fbf25-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="fbf25-112">Y</span><span class="sxs-lookup"><span data-stu-id="fbf25-112">Y</span></span>   | <span data-ttu-id="fbf25-113">N</span><span class="sxs-lookup"><span data-stu-id="fbf25-113">N</span></span>        |
| <span data-ttu-id="fbf25-114">功能\_</span><span class="sxs-lookup"><span data-stu-id="fbf25-114">Feature\_</span></span> | [<span data-ttu-id="fbf25-115">識別碼</span><span class="sxs-lookup"><span data-stu-id="fbf25-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="fbf25-116">N</span><span class="sxs-lookup"><span data-stu-id="fbf25-116">N</span></span>   | <span data-ttu-id="fbf25-117">N</span><span class="sxs-lookup"><span data-stu-id="fbf25-117">N</span></span>        |
| <span data-ttu-id="fbf25-118">動作</span><span class="sxs-lookup"><span data-stu-id="fbf25-118">Action</span></span>    | [<span data-ttu-id="fbf25-119">識別碼</span><span class="sxs-lookup"><span data-stu-id="fbf25-119">Identifier</span></span>](identifier.md) | <span data-ttu-id="fbf25-120">N</span><span class="sxs-lookup"><span data-stu-id="fbf25-120">N</span></span>   | <span data-ttu-id="fbf25-121">Y</span><span class="sxs-lookup"><span data-stu-id="fbf25-121">Y</span></span>        |
| <span data-ttu-id="fbf25-122">排序</span><span class="sxs-lookup"><span data-stu-id="fbf25-122">Ordering</span></span>  | [<span data-ttu-id="fbf25-123">整數</span><span class="sxs-lookup"><span data-stu-id="fbf25-123">Integer</span></span>](integer.md)       | <span data-ttu-id="fbf25-124">N</span><span class="sxs-lookup"><span data-stu-id="fbf25-124">N</span></span>   | <span data-ttu-id="fbf25-125">Y</span><span class="sxs-lookup"><span data-stu-id="fbf25-125">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="fbf25-126">資料行</span><span class="sxs-lookup"><span data-stu-id="fbf25-126">Columns</span></span>

<dl> <dt>

<span data-ttu-id="fbf25-127"><span id="Billboard"></span><span id="billboard"></span><span id="BILLBOARD"></span>廣告 牌</span><span class="sxs-lookup"><span data-stu-id="fbf25-127"><span id="Billboard"></span><span id="billboard"></span><span id="BILLBOARD"></span>Billboard</span></span>
</dt> <dd>

<span data-ttu-id="fbf25-128">[佈告欄控制項](billboard-control.md)的名稱。</span><span class="sxs-lookup"><span data-stu-id="fbf25-128">Name of the [Billboard control](billboard-control.md).</span></span>

</dd> <dt>

<span data-ttu-id="fbf25-129"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>特徵\_</span><span class="sxs-lookup"><span data-stu-id="fbf25-129"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Feature\_</span></span>
</dt> <dd>

<span data-ttu-id="fbf25-130">[功能資料表](feature-table.md)第一個資料行的外部索引鍵。</span><span class="sxs-lookup"><span data-stu-id="fbf25-130">An external key to the first column of the [Feature table](feature-table.md).</span></span> <span data-ttu-id="fbf25-131">只有在安裝這項功能時，才會顯示此佈告欄。</span><span class="sxs-lookup"><span data-stu-id="fbf25-131">The billboard is displayed only if this feature is being installed.</span></span>

</dd> <dt>

<span data-ttu-id="fbf25-132"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>行動</span><span class="sxs-lookup"><span data-stu-id="fbf25-132"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="fbf25-133">動作的名稱。</span><span class="sxs-lookup"><span data-stu-id="fbf25-133">The name of an action.</span></span> <span data-ttu-id="fbf25-134">這個佈告欄會在從此動作收到的進度訊息期間顯示。</span><span class="sxs-lookup"><span data-stu-id="fbf25-134">The billboard is displayed during the progress messages received from this action.</span></span>

</dd> <dt>

<span data-ttu-id="fbf25-135"><span id="Ordering"></span><span id="ordering"></span><span id="ORDERING"></span>訂購</span><span class="sxs-lookup"><span data-stu-id="fbf25-135"><span id="Ordering"></span><span id="ordering"></span><span id="ORDERING"></span>Ordering</span></span>
</dt> <dd>

<span data-ttu-id="fbf25-136">如果有一個以上的佈告欄對應到某個動作，則會依此資料行所定義的順序來顯示。</span><span class="sxs-lookup"><span data-stu-id="fbf25-136">If there is more than one billboard corresponding to an action, then they are displayed in the order defined by this column.</span></span> <span data-ttu-id="fbf25-137">此數位必須為非負數。</span><span class="sxs-lookup"><span data-stu-id="fbf25-137">This number must be non-negative.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="fbf25-138">驗證</span><span class="sxs-lookup"><span data-stu-id="fbf25-138">Validation</span></span>

<dl>

[<span data-ttu-id="fbf25-139">ICE03</span><span class="sxs-lookup"><span data-stu-id="fbf25-139">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="fbf25-140">ICE06</span><span class="sxs-lookup"><span data-stu-id="fbf25-140">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="fbf25-141">ICE32</span><span class="sxs-lookup"><span data-stu-id="fbf25-141">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="fbf25-142">ICE95</span><span class="sxs-lookup"><span data-stu-id="fbf25-142">ICE95</span></span>](ice95.md)  
</dl>

 

 



