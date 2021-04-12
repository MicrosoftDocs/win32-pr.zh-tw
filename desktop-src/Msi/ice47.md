---
description: ICE47 會檢查功能和 FeatureComponents 資料表，以取得具有1600或更多元件的功能。
ms.assetid: e3101569-4d0b-48c9-8ba2-6f0de0c39e74
title: ICE47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baa04c2df52571f56612242d2dc7da8b5a91647c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192656"
---
# <a name="ice47"></a><span data-ttu-id="4956e-103">ICE47</span><span class="sxs-lookup"><span data-stu-id="4956e-103">ICE47</span></span>

<span data-ttu-id="4956e-104">ICE47 會檢查 [功能](feature-table.md) 和 [FeatureComponents](featurecomponents-table.md) 資料表，以取得具有1600或更多元件的功能。</span><span class="sxs-lookup"><span data-stu-id="4956e-104">ICE47 checks the [Feature](feature-table.md) and [FeatureComponents](featurecomponents-table.md) tables for features with 1600 or more components.</span></span>

## <a name="result"></a><span data-ttu-id="4956e-105">結果</span><span class="sxs-lookup"><span data-stu-id="4956e-105">Result</span></span>

<span data-ttu-id="4956e-106">如果功能超過每項功能1600個元件的上限，ICE47 會張貼錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="4956e-106">ICE47 posts an error message if a feature exceeds the maximum limit of 1600 components per feature.</span></span>

## <a name="example"></a><span data-ttu-id="4956e-107">範例</span><span class="sxs-lookup"><span data-stu-id="4956e-107">Example</span></span>

<span data-ttu-id="4956e-108">ICE47 會報告下列警告：</span><span class="sxs-lookup"><span data-stu-id="4956e-108">ICE47 would report the following warning:</span></span>

``` syntax
Feature 'Feature1' has 1600 components. This could cause 
    problems on Win9X systems. You should try to have less 
    than 800 components per feature."
```

<span data-ttu-id="4956e-109">[功能表](feature-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="4956e-109">[Feature Table](feature-table.md) (partial)</span></span>



| <span data-ttu-id="4956e-110">功能</span><span class="sxs-lookup"><span data-stu-id="4956e-110">Feature</span></span>  |
|----------|
| <span data-ttu-id="4956e-111">Feature1</span><span class="sxs-lookup"><span data-stu-id="4956e-111">Feature1</span></span> |



 

<span data-ttu-id="4956e-112">[FeatureComponents 資料表](featurecomponents-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="4956e-112">[FeatureComponents Table](featurecomponents-table.md) (partial)</span></span>



| <span data-ttu-id="4956e-113">動作</span><span class="sxs-lookup"><span data-stu-id="4956e-113">Action</span></span>   | <span data-ttu-id="4956e-114">條件</span><span class="sxs-lookup"><span data-stu-id="4956e-114">Condition</span></span>     |
|----------|---------------|
| <span data-ttu-id="4956e-115">Feature1</span><span class="sxs-lookup"><span data-stu-id="4956e-115">Feature1</span></span> | <span data-ttu-id="4956e-116">Component1</span><span class="sxs-lookup"><span data-stu-id="4956e-116">Component1</span></span>    |
| <span data-ttu-id="4956e-117">Feature1</span><span class="sxs-lookup"><span data-stu-id="4956e-117">Feature1</span></span> | <span data-ttu-id="4956e-118">Component1600</span><span class="sxs-lookup"><span data-stu-id="4956e-118">Component1600</span></span> |



 

<span data-ttu-id="4956e-119">若要修正此警告，請嘗試將功能分割成數個功能</span><span class="sxs-lookup"><span data-stu-id="4956e-119">To fix this warning, try splitting the feature into several features</span></span>

## <a name="related-topics"></a><span data-ttu-id="4956e-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="4956e-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4956e-121">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="4956e-121">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



