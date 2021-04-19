---
description: ICE41 會驗證類別和延伸資料表中的專案會參考元件資料表中的專案，該專案會執行元件的類別物件或延伸模組。
ms.assetid: 43572322-ba23-4f99-be34-e572d4c6e3eb
title: ICE41
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4bc6c0a8bb634706750810484963e56b6d6e0ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987653"
---
# <a name="ice41"></a><span data-ttu-id="8dbba-103">ICE41</span><span class="sxs-lookup"><span data-stu-id="8dbba-103">ICE41</span></span>

<span data-ttu-id="8dbba-104">ICE41 會驗證 [類別](class-table.md) 和 [延伸](extension-table.md) 資料表中的專案會參考 [元件資料表](component-table.md) 中的專案，該專案會執行元件的類別物件或延伸模組。</span><span class="sxs-lookup"><span data-stu-id="8dbba-104">ICE41 validates that the entries in the [Class](class-table.md) and [Extension](extension-table.md) tables refer to entries in the [Component table](component-table.md) that implement the class object or extension of the component.</span></span>

## <a name="result"></a><span data-ttu-id="8dbba-105">結果</span><span class="sxs-lookup"><span data-stu-id="8dbba-105">Result</span></span>

<span data-ttu-id="8dbba-106">如果有一項功能不包含執行類別物件或延伸模組的元件，ICE41 會張貼錯誤。</span><span class="sxs-lookup"><span data-stu-id="8dbba-106">ICE41 posts an error if there is a feature that does not contain the component implementing the class object or extension.</span></span>

## <a name="example"></a><span data-ttu-id="8dbba-107">範例</span><span class="sxs-lookup"><span data-stu-id="8dbba-107">Example</span></span>

<span data-ttu-id="8dbba-108">ICE41 會針對所顯示的範例報告下列錯誤。</span><span class="sxs-lookup"><span data-stu-id="8dbba-108">ICE41 reports the following errors for the example shown.</span></span>



| <span data-ttu-id="8dbba-109">ICE41 錯誤</span><span class="sxs-lookup"><span data-stu-id="8dbba-109">ICE41 error</span></span>                                                                                                                                                                                    | <span data-ttu-id="8dbba-110">Description</span><span class="sxs-lookup"><span data-stu-id="8dbba-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8dbba-111">類別 {00000000-0000-0000-0000-0000000000000} 參考功能 Feature2 和元件 Component1，但該元件與 FeatureComponents 資料表中的該功能沒有關聯。</span><span class="sxs-lookup"><span data-stu-id="8dbba-111">Class {00000000-0000-0000-0000-0000000000000} references feature Feature2 and component Component1, but the that Component is not associated with that Feature in the FeatureComponents table.</span></span> | <span data-ttu-id="8dbba-112">有一項功能不包含執行類別物件的元件。</span><span class="sxs-lookup"><span data-stu-id="8dbba-112">There is a feature that does not contain the component implementing the class object.</span></span> <span data-ttu-id="8dbba-113">這表示安裝程式不會安裝具有此功能的元件，而且廣告可能無法如預期般運作。</span><span class="sxs-lookup"><span data-stu-id="8dbba-113">This means that the installer does not install the component with the feature and that advertising may not work as expected.</span></span> <span data-ttu-id="8dbba-114">若要修正這個錯誤，請將 [類別表] 專案的 [功能] 資料行中的專案變更 \_ 為參考安裝元件資料行中所列之元件的功能， [](class-table.md) \_ 或變更[FeatureComponents 資料表](featurecomponents-table.md)中相關聯的功能和元件。</span><span class="sxs-lookup"><span data-stu-id="8dbba-114">To fix this error, change the entry in the Feature\_ column of the [Class table](class-table.md) entry to reference a feature that installs component listed in the Component\_ column or change the feature and component associated in the [FeatureComponents table](featurecomponents-table.md).</span></span><br/>          |
| <span data-ttu-id="8dbba-115">Yip 會參考 feature Feature1 和 component Component2，但是該元件不會與 FeatureComponents 資料表中的該功能相關聯。</span><span class="sxs-lookup"><span data-stu-id="8dbba-115">Extension .yip references feature Feature1 and component Component2, but the that Component is not associated with that Feature in the FeatureComponents table.</span></span>                                | <span data-ttu-id="8dbba-116">有一項功能不包含執行擴充功能的元件。</span><span class="sxs-lookup"><span data-stu-id="8dbba-116">There is a feature that does not contain the component implementing the extension.</span></span> <span data-ttu-id="8dbba-117">這表示安裝程式不會安裝具有此功能的元件，而且廣告可能無法如預期般運作。</span><span class="sxs-lookup"><span data-stu-id="8dbba-117">This means that the installer does not install the component with the feature and that advertising may not work as expected.</span></span> <span data-ttu-id="8dbba-118">若要修正這個錯誤，請變更擴充功能資料表專案的 [功能] 資料行中的專案， \_ 以參考安裝元件資料行中所列元件的功能[](extension-table.md) ， \_ 或變更[FeatureComponents 資料表](featurecomponents-table.md)中相關聯的功能和元件。</span><span class="sxs-lookup"><span data-stu-id="8dbba-118">To fix this error, change the entry in the Feature\_ column of the [Extension table](extension-table.md) entry to reference a feature that installs the component listed in the Component\_ column or change the feature and component associated in the [FeatureComponents table](featurecomponents-table.md).</span></span><br/> |



 

<span data-ttu-id="8dbba-119">[FeatureComponents 資料表](featurecomponents-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="8dbba-119">[FeatureComponents Table](featurecomponents-table.md) (partial)</span></span>



| <span data-ttu-id="8dbba-120">功能\_</span><span class="sxs-lookup"><span data-stu-id="8dbba-120">Feature\_</span></span> |
|-----------|
| <span data-ttu-id="8dbba-121">Feature1</span><span class="sxs-lookup"><span data-stu-id="8dbba-121">Feature1</span></span>  |
| <span data-ttu-id="8dbba-122">Feature2</span><span class="sxs-lookup"><span data-stu-id="8dbba-122">Feature2</span></span>  |



 

<span data-ttu-id="8dbba-123">[類別表](class-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="8dbba-123">[Class Table](class-table.md) (partial)</span></span>



| <span data-ttu-id="8dbba-124">CLSID</span><span class="sxs-lookup"><span data-stu-id="8dbba-124">CLSID</span></span>                                  | <span data-ttu-id="8dbba-125">元件\_</span><span class="sxs-lookup"><span data-stu-id="8dbba-125">Component\_</span></span> | <span data-ttu-id="8dbba-126">功能\_</span><span class="sxs-lookup"><span data-stu-id="8dbba-126">Feature\_</span></span> |
|----------------------------------------|-------------|-----------|
| {00000000-0000-0000-0000-000000000000} | <span data-ttu-id="8dbba-127">Component1</span><span class="sxs-lookup"><span data-stu-id="8dbba-127">Component1</span></span>  | <span data-ttu-id="8dbba-128">Feature2</span><span class="sxs-lookup"><span data-stu-id="8dbba-128">Feature2</span></span>  |



 

<span data-ttu-id="8dbba-129">[類別表](class-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="8dbba-129">[Class Table](class-table.md) (partial)</span></span>



| <span data-ttu-id="8dbba-130">分機</span><span class="sxs-lookup"><span data-stu-id="8dbba-130">Extension</span></span> | <span data-ttu-id="8dbba-131">元件\_</span><span class="sxs-lookup"><span data-stu-id="8dbba-131">Component\_</span></span> | <span data-ttu-id="8dbba-132">功能\_</span><span class="sxs-lookup"><span data-stu-id="8dbba-132">Feature\_</span></span> |
|-----------|-------------|-----------|
| <span data-ttu-id="8dbba-133">. yip</span><span class="sxs-lookup"><span data-stu-id="8dbba-133">.yip</span></span>      | <span data-ttu-id="8dbba-134">Component2</span><span class="sxs-lookup"><span data-stu-id="8dbba-134">Component2</span></span>  | <span data-ttu-id="8dbba-135">Feature1</span><span class="sxs-lookup"><span data-stu-id="8dbba-135">Feature1</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="8dbba-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="8dbba-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8dbba-137">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="8dbba-137">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




