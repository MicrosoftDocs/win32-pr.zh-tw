---
description: MsiPatchHeaders 資料表會保存用於修補程式驗證的二進位修補標頭資料流程。
ms.assetid: aefdd365-1681-43e4-8470-04a5d6efd993
title: MsiPatchHeaders 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a3fa4e037a31f3e913f13ff9c96735ed6760dc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193103"
---
# <a name="msipatchheaders-table"></a><span data-ttu-id="dcea3-103">MsiPatchHeaders 資料表</span><span class="sxs-lookup"><span data-stu-id="dcea3-103">MsiPatchHeaders Table</span></span>

<span data-ttu-id="dcea3-104">MsiPatchHeaders 資料表會保存用於修補程式驗證的二進位修補標頭資料流程。</span><span class="sxs-lookup"><span data-stu-id="dcea3-104">The MsiPatchHeaders table holds the binary patch header streams used for patch validation.</span></span>

<span data-ttu-id="dcea3-105">當長檔案 [資料表](file-table.md) 索引鍵導致無法在 [patch 資料表](patch-table.md)中產生 patch 標頭資料流程時，就會使用 MsiPatchHeaders 資料表。</span><span class="sxs-lookup"><span data-stu-id="dcea3-105">The MsiPatchHeaders table is used when long [File table](file-table.md) keys result in a failure to generate the patch header stream in the [Patch table](patch-table.md).</span></span> <span data-ttu-id="dcea3-106">這可能是因為資料流程的 [OLE 限制](ole-limitations-on-streams.md)中所述的資料流程名稱限制所致。</span><span class="sxs-lookup"><span data-stu-id="dcea3-106">This can be due to the stream name limitation described in [OLE Limitations on Streams](ole-limitations-on-streams.md).</span></span> <span data-ttu-id="dcea3-107">在此情況下，Patch 資料表可以參考 MsiPatchHeaders 資料表，以建立 Patch 標頭資料流程。</span><span class="sxs-lookup"><span data-stu-id="dcea3-107">In this case, the Patch table can reference the MsiPatchHeaders table to create the patch header stream.</span></span>

<span data-ttu-id="dcea3-108">MsiPatchHeaders 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="dcea3-108">The MsiPatchHeaders table has the following columns.</span></span>



| <span data-ttu-id="dcea3-109">Column</span><span class="sxs-lookup"><span data-stu-id="dcea3-109">Column</span></span>    | <span data-ttu-id="dcea3-110">類型</span><span class="sxs-lookup"><span data-stu-id="dcea3-110">Type</span></span>                         | <span data-ttu-id="dcea3-111">答案</span><span class="sxs-lookup"><span data-stu-id="dcea3-111">Key</span></span> | <span data-ttu-id="dcea3-112">Nullable</span><span class="sxs-lookup"><span data-stu-id="dcea3-112">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="dcea3-113">StreamRef</span><span class="sxs-lookup"><span data-stu-id="dcea3-113">StreamRef</span></span> | [<span data-ttu-id="dcea3-114">識別碼</span><span class="sxs-lookup"><span data-stu-id="dcea3-114">Identifier</span></span>](identifier.md) | <span data-ttu-id="dcea3-115">Y</span><span class="sxs-lookup"><span data-stu-id="dcea3-115">Y</span></span>   | <span data-ttu-id="dcea3-116">N</span><span class="sxs-lookup"><span data-stu-id="dcea3-116">N</span></span>        |
| <span data-ttu-id="dcea3-117">標頭</span><span class="sxs-lookup"><span data-stu-id="dcea3-117">Header</span></span>    | [<span data-ttu-id="dcea3-118">二進位</span><span class="sxs-lookup"><span data-stu-id="dcea3-118">Binary</span></span>](binary.md)         | <span data-ttu-id="dcea3-119">N</span><span class="sxs-lookup"><span data-stu-id="dcea3-119">N</span></span>   | <span data-ttu-id="dcea3-120">N</span><span class="sxs-lookup"><span data-stu-id="dcea3-120">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="dcea3-121">資料行</span><span class="sxs-lookup"><span data-stu-id="dcea3-121">Columns</span></span>

<dl> <dt>

<span data-ttu-id="dcea3-122"><span id="StreamRef"></span><span id="streamref"></span><span id="STREAMREF"></span>StreamRef</span><span class="sxs-lookup"><span data-stu-id="dcea3-122"><span id="StreamRef"></span><span id="streamref"></span><span id="STREAMREF"></span>StreamRef</span></span>
</dt> <dd>

<span data-ttu-id="dcea3-123">可唯一識別特定 patch 標頭之資料表的主要索引鍵。</span><span class="sxs-lookup"><span data-stu-id="dcea3-123">The primary key for the table that uniquely identifies a particular patch header.</span></span>

</dd> <dt>

<span data-ttu-id="dcea3-124"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>頭</span><span class="sxs-lookup"><span data-stu-id="dcea3-124"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>Header</span></span>
</dt> <dd>

<span data-ttu-id="dcea3-125">此資料行是用於修補驗證的二進位資料流程修補程式標頭。</span><span class="sxs-lookup"><span data-stu-id="dcea3-125">This column is the binary stream patch header used for patch validation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dcea3-126">備註</span><span class="sxs-lookup"><span data-stu-id="dcea3-126">Remarks</span></span>

<span data-ttu-id="dcea3-127">此資料表是由 [PatchFiles 動作](patchfiles-action.md)處理。</span><span class="sxs-lookup"><span data-stu-id="dcea3-127">This table is processed by the [PatchFiles action](patchfiles-action.md).</span></span> <span data-ttu-id="dcea3-128">此資料表通常會透過修補套件的轉換新增至安裝套件。</span><span class="sxs-lookup"><span data-stu-id="dcea3-128">This table is usually added to the install package by a transform from a patch package.</span></span> <span data-ttu-id="dcea3-129">它通常不會直接撰寫到安裝套件中。</span><span class="sxs-lookup"><span data-stu-id="dcea3-129">It is usually not authored directly into an installation package.</span></span>

## <a name="validation"></a><span data-ttu-id="dcea3-130">驗證</span><span class="sxs-lookup"><span data-stu-id="dcea3-130">Validation</span></span>

<dl>

[<span data-ttu-id="dcea3-131">ICE03</span><span class="sxs-lookup"><span data-stu-id="dcea3-131">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="dcea3-132">ICE06</span><span class="sxs-lookup"><span data-stu-id="dcea3-132">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="dcea3-133">ICE29</span><span class="sxs-lookup"><span data-stu-id="dcea3-133">ICE29</span></span>](ice29.md)  
</dl>

 

 



