---
description: 包含筆記本便箋中個別頁面的詳細資料。
ms.assetid: 8cada667-188b-42f9-8602-34e23d512b82
title: JournalPage 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0939194585b067525fa841d6d41674180a40adb9
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432140"
---
# <a name="journalpage-element"></a><span data-ttu-id="cae52-103">JournalPage 元素</span><span class="sxs-lookup"><span data-stu-id="cae52-103">JournalPage Element</span></span>

<span data-ttu-id="cae52-104">包含筆記本便箋中個別頁面的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="cae52-104">Contains the details about an individual page in a Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="cae52-105">定義</span><span class="sxs-lookup"><span data-stu-id="cae52-105">Definition</span></span>

``` syntax
<xs:element name="JournalPage" type="JournalPageType" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a><span data-ttu-id="cae52-106">父項目</span><span class="sxs-lookup"><span data-stu-id="cae52-106">Parent Elements</span></span>

[<span data-ttu-id="cae52-107">**JournalDocument**</span><span class="sxs-lookup"><span data-stu-id="cae52-107">**JournalDocument**</span></span>](journaldocument-element.md)

## <a name="child-elements"></a><span data-ttu-id="cae52-108">子元素</span><span class="sxs-lookup"><span data-stu-id="cae52-108">Child Elements</span></span>

[<span data-ttu-id="cae52-109">**靜止**</span><span class="sxs-lookup"><span data-stu-id="cae52-109">**Stationary**</span></span>](stationery-element.md)

[<span data-ttu-id="cae52-110">**DocImage**</span><span class="sxs-lookup"><span data-stu-id="cae52-110">**DocImage**</span></span>](docimage-element.md)

[<span data-ttu-id="cae52-111">**TitleInfo**</span><span class="sxs-lookup"><span data-stu-id="cae52-111">**TitleInfo**</span></span>](titleinfo-element.md)

[<span data-ttu-id="cae52-112">**內容**</span><span class="sxs-lookup"><span data-stu-id="cae52-112">**Content**</span></span>](content-element--journal-reader.md)

## <a name="attributes"></a><span data-ttu-id="cae52-113">屬性</span><span class="sxs-lookup"><span data-stu-id="cae52-113">Attributes</span></span>



| <span data-ttu-id="cae52-114">屬性</span><span class="sxs-lookup"><span data-stu-id="cae52-114">Attribute</span></span>      | <span data-ttu-id="cae52-115">類型</span><span class="sxs-lookup"><span data-stu-id="cae52-115">Type</span></span>                      | <span data-ttu-id="cae52-116">必要</span><span class="sxs-lookup"><span data-stu-id="cae52-116">Required</span></span> | <span data-ttu-id="cae52-117">描述</span><span class="sxs-lookup"><span data-stu-id="cae52-117">Description</span></span>                                                                        | <span data-ttu-id="cae52-118">可能的值</span><span class="sxs-lookup"><span data-stu-id="cae52-118">Possible Values</span></span>                                          |
|----------------|---------------------------|----------|------------------------------------------------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="cae52-119">**Number**</span><span class="sxs-lookup"><span data-stu-id="cae52-119">**Number**</span></span>     | <span data-ttu-id="cae52-120">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="cae52-120">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="cae52-121">必要</span><span class="sxs-lookup"><span data-stu-id="cae52-121">Required</span></span> | <span data-ttu-id="cae52-122">在日誌檔中，從一個 (1) 開始的頁面序數。</span><span class="sxs-lookup"><span data-stu-id="cae52-122">The ordinal number of the page within the Journal document, starting with one (1).</span></span> | <span data-ttu-id="cae52-123">任何非負整數。</span><span class="sxs-lookup"><span data-stu-id="cae52-123">Any non-negative integer.</span></span>                                |
| <span data-ttu-id="cae52-124">**寬度**</span><span class="sxs-lookup"><span data-stu-id="cae52-124">**Width**</span></span>      | <span data-ttu-id="cae52-125">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="cae52-125">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="cae52-126">必要</span><span class="sxs-lookup"><span data-stu-id="cae52-126">Required</span></span> | <span data-ttu-id="cae52-127">頁面的寬度。</span><span class="sxs-lookup"><span data-stu-id="cae52-127">The width of the page.</span></span>                                                             | <span data-ttu-id="cae52-128">任何非負整數。</span><span class="sxs-lookup"><span data-stu-id="cae52-128">Any non-negative integer.</span></span>                                |
| <span data-ttu-id="cae52-129">**高度**</span><span class="sxs-lookup"><span data-stu-id="cae52-129">**Height**</span></span>     | <span data-ttu-id="cae52-130">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="cae52-130">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="cae52-131">必要</span><span class="sxs-lookup"><span data-stu-id="cae52-131">Required</span></span> | <span data-ttu-id="cae52-132">頁面的高度。</span><span class="sxs-lookup"><span data-stu-id="cae52-132">The height of the page.</span></span>                                                            | <span data-ttu-id="cae52-133">任何非負整數。</span><span class="sxs-lookup"><span data-stu-id="cae52-133">Any non-negative integer.</span></span>                                |
| <span data-ttu-id="cae52-134">**LineHeight**</span><span class="sxs-lookup"><span data-stu-id="cae52-134">**LineHeight**</span></span> | <span data-ttu-id="cae52-135">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="cae52-135">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="cae52-136">選用</span><span class="sxs-lookup"><span data-stu-id="cae52-136">Optional</span></span> | <span data-ttu-id="cae52-137">頁面上所使用之線條的高度。</span><span class="sxs-lookup"><span data-stu-id="cae52-137">The height of the line used on the page.</span></span>                                           | <span data-ttu-id="cae52-138">任何非負整數。</span><span class="sxs-lookup"><span data-stu-id="cae52-138">Any non-negative integer.</span></span>                                |
| <span data-ttu-id="cae52-139">**LanguageId**</span><span class="sxs-lookup"><span data-stu-id="cae52-139">**LanguageId**</span></span> | <span data-ttu-id="cae52-140">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="cae52-140">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="cae52-141">選用</span><span class="sxs-lookup"><span data-stu-id="cae52-141">Optional</span></span> | <span data-ttu-id="cae52-142">用於頁面的語言識別項。</span><span class="sxs-lookup"><span data-stu-id="cae52-142">The language id used for the page.</span></span>                                                 | <span data-ttu-id="cae52-143">代表有效語言識別項的非負整數。</span><span class="sxs-lookup"><span data-stu-id="cae52-143">A non-negative integer representing a valid language id.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="cae52-144">項目資訊</span><span class="sxs-lookup"><span data-stu-id="cae52-144">Element Information</span></span>



|  <span data-ttu-id="cae52-145">元素</span><span class="sxs-lookup"><span data-stu-id="cae52-145">Element</span></span>     | <span data-ttu-id="cae52-146">值</span><span class="sxs-lookup"><span data-stu-id="cae52-146">Value</span></span>                                                     |
|--------------|---------------------------------------------------------------------|
| <span data-ttu-id="cae52-147">項目類型</span><span class="sxs-lookup"><span data-stu-id="cae52-147">Element type</span></span> | <span data-ttu-id="cae52-148">[**JournalPageType**](journalpagetype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="cae52-148">[**JournalPageType**](journalpagetype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="cae52-149">命名空間</span><span class="sxs-lookup"><span data-stu-id="cae52-149">Namespace</span></span>    | <span data-ttu-id="cae52-150">urn：架構-microsoft-com：平板電腦： richink</span><span class="sxs-lookup"><span data-stu-id="cae52-150">urn:schemas-microsoft-com:tabletpc:richink</span></span>                          |
| <span data-ttu-id="cae52-151">結構描述名稱</span><span class="sxs-lookup"><span data-stu-id="cae52-151">Schema name</span></span>  | <span data-ttu-id="cae52-152">日誌讀者</span><span class="sxs-lookup"><span data-stu-id="cae52-152">Journal Reader</span></span>                                                      |



 

 

 



