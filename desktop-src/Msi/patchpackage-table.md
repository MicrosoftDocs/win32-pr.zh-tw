---
description: PatchPackage 資料表會描述已套用至此產品的所有修補程式套件。 針對每個修補套件，會提供修補程式的唯一識別碼，以及修補程式所在之媒體映射的相關資訊。
ms.assetid: 212d99dd-c80c-42ca-9dfa-819ae1813006
title: PatchPackage 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b13bf9fc03012ca54a0b2144e97c828c968c68da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195266"
---
# <a name="patchpackage-table"></a><span data-ttu-id="90632-104">PatchPackage 資料表</span><span class="sxs-lookup"><span data-stu-id="90632-104">PatchPackage Table</span></span>

<span data-ttu-id="90632-105">PatchPackage 資料表會描述已套用至此產品的所有修補程式套件。</span><span class="sxs-lookup"><span data-stu-id="90632-105">The PatchPackage table describes all patch packages that have been applied to this product.</span></span> <span data-ttu-id="90632-106">針對每個修補套件，會提供修補程式的唯一識別碼，以及修補程式所在之媒體映射的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="90632-106">For each patch package, the unique identifier for the patch is provided along with information about the media image the on which the patch is located.</span></span>

<span data-ttu-id="90632-107">PatchPackage 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="90632-107">The PatchPackage table has the following columns.</span></span>



| <span data-ttu-id="90632-108">Column</span><span class="sxs-lookup"><span data-stu-id="90632-108">Column</span></span>  | <span data-ttu-id="90632-109">類型</span><span class="sxs-lookup"><span data-stu-id="90632-109">Type</span></span>                   | <span data-ttu-id="90632-110">答案</span><span class="sxs-lookup"><span data-stu-id="90632-110">Key</span></span> | <span data-ttu-id="90632-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="90632-111">Nullable</span></span> |
|---------|------------------------|-----|----------|
| <span data-ttu-id="90632-112">PatchId</span><span class="sxs-lookup"><span data-stu-id="90632-112">PatchId</span></span> | [<span data-ttu-id="90632-113">GUID</span><span class="sxs-lookup"><span data-stu-id="90632-113">GUID</span></span>](guid.md)       | <span data-ttu-id="90632-114">Y</span><span class="sxs-lookup"><span data-stu-id="90632-114">Y</span></span>   | <span data-ttu-id="90632-115">N</span><span class="sxs-lookup"><span data-stu-id="90632-115">N</span></span>        |
| <span data-ttu-id="90632-116">媒體\_</span><span class="sxs-lookup"><span data-stu-id="90632-116">Media\_</span></span> | [<span data-ttu-id="90632-117">整數</span><span class="sxs-lookup"><span data-stu-id="90632-117">Integer</span></span>](integer.md) | <span data-ttu-id="90632-118">N</span><span class="sxs-lookup"><span data-stu-id="90632-118">N</span></span>   | <span data-ttu-id="90632-119">N</span><span class="sxs-lookup"><span data-stu-id="90632-119">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="90632-120">資料行</span><span class="sxs-lookup"><span data-stu-id="90632-120">Columns</span></span>

<dl> <dt>

<span data-ttu-id="90632-121"><span id="PatchId"></span><span id="patchid"></span><span id="PATCHID"></span>PatchId</span><span class="sxs-lookup"><span data-stu-id="90632-121"><span id="PatchId"></span><span id="patchid"></span><span id="PATCHID"></span>PatchId</span></span>
</dt> <dd>

<span data-ttu-id="90632-122">此資料行包含此特定修補程式的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="90632-122">This column contains a unique identifier for this particular patch.</span></span>

</dd> <dt>

<span data-ttu-id="90632-123"><span id="Media_"></span><span id="media_"></span><span id="MEDIA_"></span>媒體\_</span><span class="sxs-lookup"><span data-stu-id="90632-123"><span id="Media_"></span><span id="media_"></span><span id="MEDIA_"></span>Media\_</span></span>
</dt> <dd>

<span data-ttu-id="90632-124">此資料行是 [媒體資料表](media-table.md) 中 DiskId 資料行的外鍵，表示包含修補程式套件的磁片。</span><span class="sxs-lookup"><span data-stu-id="90632-124">This column is a foreign key to the DiskId column of the [Media Table](media-table.md) and indicates the disk containing the patch package.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="90632-125">備註</span><span class="sxs-lookup"><span data-stu-id="90632-125">Remarks</span></span>

<span data-ttu-id="90632-126">每個修補封裝都需要 PatchPackage 資料表。</span><span class="sxs-lookup"><span data-stu-id="90632-126">The PatchPackage table is required in every patch package.</span></span> <span data-ttu-id="90632-127">如果資料表遺失，嘗試安裝修補程式會失敗，並出現「錯誤2768： patch 封裝中的轉換無效」。</span><span class="sxs-lookup"><span data-stu-id="90632-127">If the table is missing, attempts to install the patch fail with "Error 2768: Transform in patch package is invalid."</span></span> <span data-ttu-id="90632-128">此資料表通常會透過修補套件的轉換新增至安裝套件。</span><span class="sxs-lookup"><span data-stu-id="90632-128">This table is usually added to the install package by a transform from a patch package.</span></span> <span data-ttu-id="90632-129">它通常不會直接撰寫到安裝套件中。</span><span class="sxs-lookup"><span data-stu-id="90632-129">It is usually not authored directly into an install package.</span></span>

## <a name="validation"></a><span data-ttu-id="90632-130">驗證</span><span class="sxs-lookup"><span data-stu-id="90632-130">Validation</span></span>

<dl>

[<span data-ttu-id="90632-131">ICE03</span><span class="sxs-lookup"><span data-stu-id="90632-131">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="90632-132">ICE06</span><span class="sxs-lookup"><span data-stu-id="90632-132">ICE06</span></span>](ice06.md)  
</dl>

 

 



