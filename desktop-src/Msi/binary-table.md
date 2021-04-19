---
description: 二進位資料表會保存點陣圖、動畫和圖示等專案的二進位資料。 二進位資料表也用來儲存自訂動作的資料。 請參閱 OLE 對資料流程的限制。
ms.assetid: 44c56407-df2e-4cbe-b7a3-b22e8d97eb03
title: 二進位資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4069c7e684e7d90c94b4b04f3d5839058f3570a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106976845"
---
# <a name="binary-table"></a><span data-ttu-id="708a4-105">二進位資料表</span><span class="sxs-lookup"><span data-stu-id="708a4-105">Binary Table</span></span>

<span data-ttu-id="708a4-106">二進位資料表會保存點陣圖、動畫和圖示等專案的二進位資料。</span><span class="sxs-lookup"><span data-stu-id="708a4-106">The Binary table holds the binary data for items such as bitmaps, animations, and icons.</span></span> <span data-ttu-id="708a4-107">二進位資料表也用來儲存自訂動作的資料。</span><span class="sxs-lookup"><span data-stu-id="708a4-107">The binary table is also used to store data for custom actions.</span></span> <span data-ttu-id="708a4-108">請參閱 [OLE 對資料流程的限制](ole-limitations-on-streams.md)。</span><span class="sxs-lookup"><span data-stu-id="708a4-108">See [OLE Limitations on Streams](ole-limitations-on-streams.md).</span></span>

<span data-ttu-id="708a4-109">二進位資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="708a4-109">The Binary table has the following columns.</span></span>



| <span data-ttu-id="708a4-110">Column</span><span class="sxs-lookup"><span data-stu-id="708a4-110">Column</span></span> | <span data-ttu-id="708a4-111">類型</span><span class="sxs-lookup"><span data-stu-id="708a4-111">Type</span></span>                         | <span data-ttu-id="708a4-112">答案</span><span class="sxs-lookup"><span data-stu-id="708a4-112">Key</span></span> | <span data-ttu-id="708a4-113">Nullable</span><span class="sxs-lookup"><span data-stu-id="708a4-113">Nullable</span></span> |
|--------|------------------------------|-----|----------|
| <span data-ttu-id="708a4-114">Name</span><span class="sxs-lookup"><span data-stu-id="708a4-114">Name</span></span>   | [<span data-ttu-id="708a4-115">識別碼</span><span class="sxs-lookup"><span data-stu-id="708a4-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="708a4-116">Y</span><span class="sxs-lookup"><span data-stu-id="708a4-116">Y</span></span>   | <span data-ttu-id="708a4-117">N</span><span class="sxs-lookup"><span data-stu-id="708a4-117">N</span></span>        |
| <span data-ttu-id="708a4-118">資料</span><span class="sxs-lookup"><span data-stu-id="708a4-118">Data</span></span>   | [<span data-ttu-id="708a4-119">二進位</span><span class="sxs-lookup"><span data-stu-id="708a4-119">Binary</span></span>](binary.md)         | <span data-ttu-id="708a4-120">N</span><span class="sxs-lookup"><span data-stu-id="708a4-120">N</span></span>   | <span data-ttu-id="708a4-121">N</span><span class="sxs-lookup"><span data-stu-id="708a4-121">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="708a4-122">資料行</span><span class="sxs-lookup"><span data-stu-id="708a4-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="708a4-123"><span id="Name"></span><span id="name"></span><span id="NAME"></span>名字</span><span class="sxs-lookup"><span data-stu-id="708a4-123"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="708a4-124">識別特定二進位資料的唯一索引鍵。</span><span class="sxs-lookup"><span data-stu-id="708a4-124">A unique key that identifies the particular binary data.</span></span> <span data-ttu-id="708a4-125">如果二進位資料是針對控制項，則索引鍵會出現在 [控制項資料表](control-table.md)中相關聯控制項的文字資料行中。</span><span class="sxs-lookup"><span data-stu-id="708a4-125">If the binary data is for a control, the key appears in the Text column of the associated control in the [Control table](control-table.md).</span></span> <span data-ttu-id="708a4-126">此索引鍵在所有需要二進位資料的控制項中必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="708a4-126">This key must be unique among all controls requiring binary data.</span></span>

</dd> <dt>

<span data-ttu-id="708a4-127"><span id="Data"></span><span id="data"></span><span id="DATA"></span>資料</span><span class="sxs-lookup"><span data-stu-id="708a4-127"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Data</span></span>
</dt> <dd>

<span data-ttu-id="708a4-128">未格式化的二進位資料。</span><span class="sxs-lookup"><span data-stu-id="708a4-128">The unformatted binary data.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="708a4-129">驗證</span><span class="sxs-lookup"><span data-stu-id="708a4-129">Validation</span></span>

<dl>

[<span data-ttu-id="708a4-130">ICE03</span><span class="sxs-lookup"><span data-stu-id="708a4-130">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="708a4-131">ICE06</span><span class="sxs-lookup"><span data-stu-id="708a4-131">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="708a4-132">ICE17</span><span class="sxs-lookup"><span data-stu-id="708a4-132">ICE17</span></span>](ice17.md)  
[<span data-ttu-id="708a4-133">ICE29</span><span class="sxs-lookup"><span data-stu-id="708a4-133">ICE29</span></span>](ice29.md)  
</dl>

 

 



