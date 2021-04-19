---
description: ICE22 會使用 FeatureComponents 資料表來驗證 PublishComponent 資料表中所參考的功能和元件的對應。
ms.assetid: 1aa3e2e6-3f05-411e-829f-aeddbb53445d
title: ICE22
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26574b11f9d908026d901a74632766998246d31a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987654"
---
# <a name="ice22"></a><span data-ttu-id="3949d-103">ICE22</span><span class="sxs-lookup"><span data-stu-id="3949d-103">ICE22</span></span>

<span data-ttu-id="3949d-104">ICE22 會使用 [FeatureComponents 資料表](featurecomponents-table.md) 來驗證 [PublishComponent 資料表](publishcomponent-table.md)中所參考的功能和元件的對應。</span><span class="sxs-lookup"><span data-stu-id="3949d-104">ICE22 uses the [FeatureComponents table](featurecomponents-table.md) to validate the mapping of features and components referenced in the [PublishComponent table](publishcomponent-table.md).</span></span>

## <a name="result"></a><span data-ttu-id="3949d-105">結果</span><span class="sxs-lookup"><span data-stu-id="3949d-105">Result</span></span>

<span data-ttu-id="3949d-106">如果功能和元件在 [PublishComponent 資料表](publishcomponent-table.md)中的對應不正確，ICE22 會張貼錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="3949d-106">ICE22 posts an error message if the features and components are mapped incorrectly in the [PublishComponent table](publishcomponent-table.md).</span></span>

## <a name="example"></a><span data-ttu-id="3949d-107">範例</span><span class="sxs-lookup"><span data-stu-id="3949d-107">Example</span></span>

<span data-ttu-id="3949d-108">在下列範例中，ICE22 會張貼沒有 {00000003-0004-0000-0000-624474732465} 功能和元件資料行之正確對應的錯誤 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="3949d-108">For the following example ICE22 posts an error that {00000003-0004-0000-0000-624474732465} does not have the correct mapping for the Feature\_ and Component\_ columns.</span></span>

<span data-ttu-id="3949d-109">[PublishComponent 資料表](publishcomponent-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="3949d-109">[PublishComponent Table](publishcomponent-table.md) (partial)</span></span>



| <span data-ttu-id="3949d-110">ComponentId</span><span class="sxs-lookup"><span data-stu-id="3949d-110">ComponentId</span></span>                            | <span data-ttu-id="3949d-111">功能\_</span><span class="sxs-lookup"><span data-stu-id="3949d-111">Feature\_</span></span> | <span data-ttu-id="3949d-112">元件\_</span><span class="sxs-lookup"><span data-stu-id="3949d-112">Component\_</span></span> |
|----------------------------------------|-----------|-------------|
| {00000002-0003-0000-0000-624474736554} | <span data-ttu-id="3949d-113">Feat1</span><span class="sxs-lookup"><span data-stu-id="3949d-113">Feat1</span></span>     | <span data-ttu-id="3949d-114">Comp1</span><span class="sxs-lookup"><span data-stu-id="3949d-114">Comp1</span></span>       |
| {00000003-0004-0000-0000-624474732465} | <span data-ttu-id="3949d-115">Feat1</span><span class="sxs-lookup"><span data-stu-id="3949d-115">Feat1</span></span>     | <span data-ttu-id="3949d-116">Comp2</span><span class="sxs-lookup"><span data-stu-id="3949d-116">Comp2</span></span>       |



 

<span data-ttu-id="3949d-117">[FeatureComponents 資料表](featurecomponents-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="3949d-117">[FeatureComponents Table](featurecomponents-table.md) (partial)</span></span>



| <span data-ttu-id="3949d-118">功能\_</span><span class="sxs-lookup"><span data-stu-id="3949d-118">Feature\_</span></span> | <span data-ttu-id="3949d-119">元件\_</span><span class="sxs-lookup"><span data-stu-id="3949d-119">Component\_</span></span> |
|-----------|-------------|
| <span data-ttu-id="3949d-120">Feat1</span><span class="sxs-lookup"><span data-stu-id="3949d-120">Feat1</span></span>     | <span data-ttu-id="3949d-121">Comp1</span><span class="sxs-lookup"><span data-stu-id="3949d-121">Comp1</span></span>       |



 

## <a name="related-topics"></a><span data-ttu-id="3949d-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="3949d-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3949d-123">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="3949d-123">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



