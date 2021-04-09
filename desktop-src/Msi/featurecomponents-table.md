---
description: FeatureComponents 資料表會定義功能和元件之間的關聯性。 針對每個功能，此表格會列出構成該功能的所有元件。
ms.assetid: aff16483-a9ed-4675-8e87-8adf695605ee
title: FeatureComponents 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6c93a7c020f179843916b063b48e2e4d19f7bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691791"
---
# <a name="featurecomponents-table"></a><span data-ttu-id="192a1-104">FeatureComponents 資料表</span><span class="sxs-lookup"><span data-stu-id="192a1-104">FeatureComponents Table</span></span>

<span data-ttu-id="192a1-105">FeatureComponents 資料表會定義功能和元件之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="192a1-105">The FeatureComponents table defines the relationship between features and components.</span></span> <span data-ttu-id="192a1-106">針對每個功能，此表格會列出構成該功能的所有元件。</span><span class="sxs-lookup"><span data-stu-id="192a1-106">For each feature, this table lists all the components that make up that feature.</span></span>

<span data-ttu-id="192a1-107">FeatureComponents 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="192a1-107">The FeatureComponents table has the following columns.</span></span>



| <span data-ttu-id="192a1-108">Column</span><span class="sxs-lookup"><span data-stu-id="192a1-108">Column</span></span>      | <span data-ttu-id="192a1-109">類型</span><span class="sxs-lookup"><span data-stu-id="192a1-109">Type</span></span>                         | <span data-ttu-id="192a1-110">答案</span><span class="sxs-lookup"><span data-stu-id="192a1-110">Key</span></span> | <span data-ttu-id="192a1-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="192a1-111">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="192a1-112">功能\_</span><span class="sxs-lookup"><span data-stu-id="192a1-112">Feature\_</span></span>   | [<span data-ttu-id="192a1-113">識別碼</span><span class="sxs-lookup"><span data-stu-id="192a1-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="192a1-114">Y</span><span class="sxs-lookup"><span data-stu-id="192a1-114">Y</span></span>   | <span data-ttu-id="192a1-115">N</span><span class="sxs-lookup"><span data-stu-id="192a1-115">N</span></span>        |
| <span data-ttu-id="192a1-116">元件\_</span><span class="sxs-lookup"><span data-stu-id="192a1-116">Component\_</span></span> | [<span data-ttu-id="192a1-117">識別碼</span><span class="sxs-lookup"><span data-stu-id="192a1-117">Identifier</span></span>](identifier.md) | <span data-ttu-id="192a1-118">Y</span><span class="sxs-lookup"><span data-stu-id="192a1-118">Y</span></span>   | <span data-ttu-id="192a1-119">N</span><span class="sxs-lookup"><span data-stu-id="192a1-119">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="192a1-120">資料行</span><span class="sxs-lookup"><span data-stu-id="192a1-120">Columns</span></span>

<dl> <dt>

<span data-ttu-id="192a1-121"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>特徵\_</span><span class="sxs-lookup"><span data-stu-id="192a1-121"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Feature\_</span></span>
</dt> <dd>

<span data-ttu-id="192a1-122">功能 [資料表](feature-table.md)第一個資料行中的外部索引鍵。</span><span class="sxs-lookup"><span data-stu-id="192a1-122">An external key into the first column of the Feature [table](feature-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="192a1-123"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>元件\_</span><span class="sxs-lookup"><span data-stu-id="192a1-123"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="192a1-124">[元件資料表](component-table.md)的第一個資料行中的外部索引鍵。</span><span class="sxs-lookup"><span data-stu-id="192a1-124">An external key into the first column of the [Component table](component-table.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="192a1-125">備註</span><span class="sxs-lookup"><span data-stu-id="192a1-125">Remarks</span></span>

<span data-ttu-id="192a1-126">每項功能有1600個元件的最大限制。</span><span class="sxs-lookup"><span data-stu-id="192a1-126">There is a maximum limit of 1600 components per feature.</span></span>

<span data-ttu-id="192a1-127">元件可以由兩個以上的功能共用，也就是相同元件可由多項功能參考。</span><span class="sxs-lookup"><span data-stu-id="192a1-127">Components can be shared by two or more features, that is, the same component can be referred to by more than one feature.</span></span>

<span data-ttu-id="192a1-128">當執行 [PublishFeatures 動作](publishfeatures-action.md) 或 [UnpublishFeatures 動作](unpublishfeatures-action.md) 時，就會參考此資料表。</span><span class="sxs-lookup"><span data-stu-id="192a1-128">This table is referred to when the [PublishFeatures action](publishfeatures-action.md) or the [UnpublishFeatures action](unpublishfeatures-action.md) is executed.</span></span>

## <a name="validation"></a><span data-ttu-id="192a1-129">驗證</span><span class="sxs-lookup"><span data-stu-id="192a1-129">Validation</span></span>

<dl>

[<span data-ttu-id="192a1-130">ICE03</span><span class="sxs-lookup"><span data-stu-id="192a1-130">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="192a1-131">ICE06</span><span class="sxs-lookup"><span data-stu-id="192a1-131">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="192a1-132">ICE21</span><span class="sxs-lookup"><span data-stu-id="192a1-132">ICE21</span></span>](ice21.md)  
[<span data-ttu-id="192a1-133">ICE22</span><span class="sxs-lookup"><span data-stu-id="192a1-133">ICE22</span></span>](ice22.md)  
[<span data-ttu-id="192a1-134">ICE32</span><span class="sxs-lookup"><span data-stu-id="192a1-134">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="192a1-135">ICE41</span><span class="sxs-lookup"><span data-stu-id="192a1-135">ICE41</span></span>](ice41.md)  
[<span data-ttu-id="192a1-136">ICE47</span><span class="sxs-lookup"><span data-stu-id="192a1-136">ICE47</span></span>](ice47.md)  
[<span data-ttu-id="192a1-137">ICE59</span><span class="sxs-lookup"><span data-stu-id="192a1-137">ICE59</span></span>](ice59.md)  
[<span data-ttu-id="192a1-138">ICE62</span><span class="sxs-lookup"><span data-stu-id="192a1-138">ICE62</span></span>](ice62.md)  
[<span data-ttu-id="192a1-139">ICE69</span><span class="sxs-lookup"><span data-stu-id="192a1-139">ICE69</span></span>](ice69.md)  
</dl>

 

 



