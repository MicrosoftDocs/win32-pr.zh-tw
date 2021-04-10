---
description: 保留的 \_ 資料行名稱 RowState 代表與安裝程式資料庫資料表中的每個資料表資料列相關聯的非持續性狀態。
ms.assetid: ff570b47-7c16-47ae-b1c2-2ecad9266372
title: _RowState 資料行
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e61a2964d7d11c1c2429ad95e9de2b8bdb148954
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026650"
---
# <a name="_rowstate-column"></a><span data-ttu-id="4366f-103">\_RowState 資料行</span><span class="sxs-lookup"><span data-stu-id="4366f-103">\_RowState Column</span></span>

<span data-ttu-id="4366f-104">保留的 \_ 資料行名稱 RowState 代表與安裝程式資料庫資料表中的每個資料表資料列相關聯的非持續性狀態。</span><span class="sxs-lookup"><span data-stu-id="4366f-104">The reserved column name \_RowState represents the non-persistent state associated with each table row in an installer database table.</span></span> <span data-ttu-id="4366f-105">虛擬資料行的類型為 [整數](integer.md)，而值則由一組位旗標所組成。</span><span class="sxs-lookup"><span data-stu-id="4366f-105">The pseudo-column is of type [Integer](integer.md), and the value consists of a set of bit flags.</span></span> <span data-ttu-id="4366f-106">所有的位都是可讀取的，但只能設定使用者資訊和暫存位。</span><span class="sxs-lookup"><span data-stu-id="4366f-106">All the bits are readable, but only the UserInfo and Temporary bits can be set.</span></span> <span data-ttu-id="4366f-107">只有當資料表已鎖定或在使用中時，才可以使用此資料 (也就是說，包含資料表的視圖) 存在。</span><span class="sxs-lookup"><span data-stu-id="4366f-107">This data is available only as long as the tables are locked or in use (that is, while a view containing the tables exists).</span></span> <span data-ttu-id="4366f-108">下表顯示資料列可以有的屬性。</span><span class="sxs-lookup"><span data-stu-id="4366f-108">The following table shows the attributes a row can have.</span></span>



| <span data-ttu-id="4366f-109">Name</span><span class="sxs-lookup"><span data-stu-id="4366f-109">Name</span></span>           | <span data-ttu-id="4366f-110">值</span><span class="sxs-lookup"><span data-stu-id="4366f-110">Value</span></span> | <span data-ttu-id="4366f-111">意義</span><span class="sxs-lookup"><span data-stu-id="4366f-111">Meaning</span></span>                                                        |
|----------------|-------|----------------------------------------------------------------|
| <span data-ttu-id="4366f-112">iraUserInfo</span><span class="sxs-lookup"><span data-stu-id="4366f-112">iraUserInfo</span></span>    | <span data-ttu-id="4366f-113">0x01</span><span class="sxs-lookup"><span data-stu-id="4366f-113">0x01</span></span>  | <span data-ttu-id="4366f-114">屬性可供外部使用。</span><span class="sxs-lookup"><span data-stu-id="4366f-114">The attribute is for external use.</span></span> <span data-ttu-id="4366f-115">您可以更新此值。</span><span class="sxs-lookup"><span data-stu-id="4366f-115">This value can be updated.</span></span>  |
| <span data-ttu-id="4366f-116">iraTemporary</span><span class="sxs-lookup"><span data-stu-id="4366f-116">iraTemporary</span></span>   | <span data-ttu-id="4366f-117">0x02</span><span class="sxs-lookup"><span data-stu-id="4366f-117">0x02</span></span>  | <span data-ttu-id="4366f-118">資料列不是持續性。</span><span class="sxs-lookup"><span data-stu-id="4366f-118">The row is not persistent.</span></span> <span data-ttu-id="4366f-119">您可以更新此值。</span><span class="sxs-lookup"><span data-stu-id="4366f-119">This value can be updated.</span></span>          |
| <span data-ttu-id="4366f-120">iraModified</span><span class="sxs-lookup"><span data-stu-id="4366f-120">iraModified</span></span>    | <span data-ttu-id="4366f-121">0x04</span><span class="sxs-lookup"><span data-stu-id="4366f-121">0x04</span></span>  | <span data-ttu-id="4366f-122">已更新資料列。</span><span class="sxs-lookup"><span data-stu-id="4366f-122">A row has been updated.</span></span>                                        |
| <span data-ttu-id="4366f-123">iraInserted</span><span class="sxs-lookup"><span data-stu-id="4366f-123">iraInserted</span></span>    | <span data-ttu-id="4366f-124">0x08</span><span class="sxs-lookup"><span data-stu-id="4366f-124">0x08</span></span>  | <span data-ttu-id="4366f-125">已插入資料列。</span><span class="sxs-lookup"><span data-stu-id="4366f-125">A row has been inserted.</span></span>                                       |
| <span data-ttu-id="4366f-126">iraMergeFailed</span><span class="sxs-lookup"><span data-stu-id="4366f-126">iraMergeFailed</span></span> | <span data-ttu-id="4366f-127">0x0F</span><span class="sxs-lookup"><span data-stu-id="4366f-127">0x0F</span></span>  | <span data-ttu-id="4366f-128">嘗試合併不相同的非索引鍵資料。</span><span class="sxs-lookup"><span data-stu-id="4366f-128">An attempt was made to merge with non-identical, non-key data.</span></span> |



 

<span data-ttu-id="4366f-129">保留的位6到8。</span><span class="sxs-lookup"><span data-stu-id="4366f-129">Bits 6 through 8 are reserved.</span></span>

 

 



