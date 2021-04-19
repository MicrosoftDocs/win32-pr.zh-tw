---
description: ICE21 會驗證元件資料表中的每個元件都屬於某項功能。 它會使用 FeatureComponents 資料表來檢查此對應。
ms.assetid: 68983d6a-b807-4730-a645-378001e558ec
title: ICE21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c457d026b3dc57a718eabea704254a3448a3de26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996799"
---
# <a name="ice21"></a><span data-ttu-id="63da3-104">ICE21</span><span class="sxs-lookup"><span data-stu-id="63da3-104">ICE21</span></span>

<span data-ttu-id="63da3-105">ICE21 會驗證 [元件資料表](component-table.md) 中的每個元件都屬於某項功能。</span><span class="sxs-lookup"><span data-stu-id="63da3-105">ICE21 validates that every component in the [Component table](component-table.md) belongs to a feature.</span></span> <span data-ttu-id="63da3-106">它會使用 [FeatureComponents 資料表](featurecomponents-table.md) 來檢查此對應。</span><span class="sxs-lookup"><span data-stu-id="63da3-106">It uses the [FeatureComponents table](featurecomponents-table.md) to check for this mapping.</span></span>

## <a name="result"></a><span data-ttu-id="63da3-107">結果</span><span class="sxs-lookup"><span data-stu-id="63da3-107">Result</span></span>

<span data-ttu-id="63da3-108">如果安裝套件包含不屬於某項功能的元件，ICE21 會張貼錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="63da3-108">ICE21 posts an error message if the installation package contains a component that does not belong to a feature.</span></span>

## <a name="example"></a><span data-ttu-id="63da3-109">範例</span><span class="sxs-lookup"><span data-stu-id="63da3-109">Example</span></span>

<span data-ttu-id="63da3-110">在下列範例中，ICE21 會張貼一則錯誤訊息，指出元件 Comp1 未對應到任何功能。</span><span class="sxs-lookup"><span data-stu-id="63da3-110">For the following example, ICE21 posts an error message stating that the component Comp1 does not map to any feature.</span></span>

<span data-ttu-id="63da3-111">[元件資料表](component-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="63da3-111">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="63da3-112">元件</span><span class="sxs-lookup"><span data-stu-id="63da3-112">Component</span></span> |
|-----------|
| <span data-ttu-id="63da3-113">Comp1</span><span class="sxs-lookup"><span data-stu-id="63da3-113">Comp1</span></span>     |
| <span data-ttu-id="63da3-114">Comp2</span><span class="sxs-lookup"><span data-stu-id="63da3-114">Comp2</span></span>     |



 

<span data-ttu-id="63da3-115">[FeatureComponents 資料表](featurecomponents-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="63da3-115">[FeatureComponents Table](featurecomponents-table.md) (partial)</span></span>



| <span data-ttu-id="63da3-116">功能</span><span class="sxs-lookup"><span data-stu-id="63da3-116">Feature</span></span>  | <span data-ttu-id="63da3-117">元件</span><span class="sxs-lookup"><span data-stu-id="63da3-117">Component</span></span> |
|----------|-----------|
| <span data-ttu-id="63da3-118">Feature1</span><span class="sxs-lookup"><span data-stu-id="63da3-118">Feature1</span></span> | <span data-ttu-id="63da3-119">Comp2</span><span class="sxs-lookup"><span data-stu-id="63da3-119">Comp2</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="63da3-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="63da3-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63da3-121">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="63da3-121">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



