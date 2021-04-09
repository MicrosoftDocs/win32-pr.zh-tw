---
description: 包含筆記本便箋中個別頁面的詳細資料。
ms.assetid: 8cada667-188b-42f9-8602-34e23d512b82
title: JournalPage 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e7223818de8200f2ff7748edd7eb472f49e92e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850659"
---
# <a name="journalpage-element"></a><span data-ttu-id="61623-103">JournalPage 元素</span><span class="sxs-lookup"><span data-stu-id="61623-103">JournalPage Element</span></span>

<span data-ttu-id="61623-104">包含筆記本便箋中個別頁面的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="61623-104">Contains the details about an individual page in a Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="61623-105">定義</span><span class="sxs-lookup"><span data-stu-id="61623-105">Definition</span></span>

``` syntax
<xs:element name="JournalPage" type="JournalPageType" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a><span data-ttu-id="61623-106">父項目</span><span class="sxs-lookup"><span data-stu-id="61623-106">Parent Elements</span></span>

[<span data-ttu-id="61623-107">**JournalDocument**</span><span class="sxs-lookup"><span data-stu-id="61623-107">**JournalDocument**</span></span>](journaldocument-element.md)

## <a name="child-elements"></a><span data-ttu-id="61623-108">子元素</span><span class="sxs-lookup"><span data-stu-id="61623-108">Child Elements</span></span>

[<span data-ttu-id="61623-109">**靜止**</span><span class="sxs-lookup"><span data-stu-id="61623-109">**Stationary**</span></span>](stationery-element.md)

[<span data-ttu-id="61623-110">**DocImage**</span><span class="sxs-lookup"><span data-stu-id="61623-110">**DocImage**</span></span>](docimage-element.md)

[<span data-ttu-id="61623-111">**TitleInfo**</span><span class="sxs-lookup"><span data-stu-id="61623-111">**TitleInfo**</span></span>](titleinfo-element.md)

[<span data-ttu-id="61623-112">**內容**</span><span class="sxs-lookup"><span data-stu-id="61623-112">**Content**</span></span>](content-element--journal-reader.md)

## <a name="attributes"></a><span data-ttu-id="61623-113">屬性</span><span class="sxs-lookup"><span data-stu-id="61623-113">Attributes</span></span>



| <span data-ttu-id="61623-114">屬性</span><span class="sxs-lookup"><span data-stu-id="61623-114">Attribute</span></span>      | <span data-ttu-id="61623-115">類型</span><span class="sxs-lookup"><span data-stu-id="61623-115">Type</span></span>                      | <span data-ttu-id="61623-116">必要</span><span class="sxs-lookup"><span data-stu-id="61623-116">Required</span></span> | <span data-ttu-id="61623-117">描述</span><span class="sxs-lookup"><span data-stu-id="61623-117">Description</span></span>                                                                        | <span data-ttu-id="61623-118">可能的值</span><span class="sxs-lookup"><span data-stu-id="61623-118">Possible Values</span></span>                                          |
|----------------|---------------------------|----------|------------------------------------------------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="61623-119">**Number**</span><span class="sxs-lookup"><span data-stu-id="61623-119">**Number**</span></span>     | <span data-ttu-id="61623-120">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="61623-120">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="61623-121">必要</span><span class="sxs-lookup"><span data-stu-id="61623-121">Required</span></span> | <span data-ttu-id="61623-122">在日誌檔中，從一個 (1) 開始的頁面序數。</span><span class="sxs-lookup"><span data-stu-id="61623-122">The ordinal number of the page within the Journal document, starting with one (1).</span></span> | <span data-ttu-id="61623-123">任何非負整數。</span><span class="sxs-lookup"><span data-stu-id="61623-123">Any non-negative integer.</span></span>                                |
| <span data-ttu-id="61623-124">**寬度**</span><span class="sxs-lookup"><span data-stu-id="61623-124">**Width**</span></span>      | <span data-ttu-id="61623-125">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="61623-125">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="61623-126">必要</span><span class="sxs-lookup"><span data-stu-id="61623-126">Required</span></span> | <span data-ttu-id="61623-127">頁面的寬度。</span><span class="sxs-lookup"><span data-stu-id="61623-127">The width of the page.</span></span>                                                             | <span data-ttu-id="61623-128">任何非負整數。</span><span class="sxs-lookup"><span data-stu-id="61623-128">Any non-negative integer.</span></span>                                |
| <span data-ttu-id="61623-129">**高度**</span><span class="sxs-lookup"><span data-stu-id="61623-129">**Height**</span></span>     | <span data-ttu-id="61623-130">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="61623-130">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="61623-131">必要</span><span class="sxs-lookup"><span data-stu-id="61623-131">Required</span></span> | <span data-ttu-id="61623-132">頁面的高度。</span><span class="sxs-lookup"><span data-stu-id="61623-132">The height of the page.</span></span>                                                            | <span data-ttu-id="61623-133">任何非負整數。</span><span class="sxs-lookup"><span data-stu-id="61623-133">Any non-negative integer.</span></span>                                |
| <span data-ttu-id="61623-134">**LineHeight**</span><span class="sxs-lookup"><span data-stu-id="61623-134">**LineHeight**</span></span> | <span data-ttu-id="61623-135">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="61623-135">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="61623-136">選擇性</span><span class="sxs-lookup"><span data-stu-id="61623-136">Optional</span></span> | <span data-ttu-id="61623-137">頁面上所使用之線條的高度。</span><span class="sxs-lookup"><span data-stu-id="61623-137">The height of the line used on the page.</span></span>                                           | <span data-ttu-id="61623-138">任何非負整數。</span><span class="sxs-lookup"><span data-stu-id="61623-138">Any non-negative integer.</span></span>                                |
| <span data-ttu-id="61623-139">**LanguageId**</span><span class="sxs-lookup"><span data-stu-id="61623-139">**LanguageId**</span></span> | <span data-ttu-id="61623-140">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="61623-140">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="61623-141">選擇性</span><span class="sxs-lookup"><span data-stu-id="61623-141">Optional</span></span> | <span data-ttu-id="61623-142">用於頁面的語言識別項。</span><span class="sxs-lookup"><span data-stu-id="61623-142">The language id used for the page.</span></span>                                                 | <span data-ttu-id="61623-143">代表有效語言識別項的非負整數。</span><span class="sxs-lookup"><span data-stu-id="61623-143">A non-negative integer representing a valid language id.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="61623-144">項目資訊</span><span class="sxs-lookup"><span data-stu-id="61623-144">Element Information</span></span>



|              |                                                                     |
|--------------|---------------------------------------------------------------------|
| <span data-ttu-id="61623-145">項目類型</span><span class="sxs-lookup"><span data-stu-id="61623-145">Element type</span></span> | <span data-ttu-id="61623-146">[**JournalPageType**](journalpagetype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="61623-146">[**JournalPageType**](journalpagetype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="61623-147">命名空間</span><span class="sxs-lookup"><span data-stu-id="61623-147">Namespace</span></span>    | <span data-ttu-id="61623-148">urn：架構-microsoft-com：平板電腦： richink</span><span class="sxs-lookup"><span data-stu-id="61623-148">urn:schemas-microsoft-com:tabletpc:richink</span></span>                          |
| <span data-ttu-id="61623-149">結構描述名稱</span><span class="sxs-lookup"><span data-stu-id="61623-149">Schema name</span></span>  | <span data-ttu-id="61623-150">日誌讀者</span><span class="sxs-lookup"><span data-stu-id="61623-150">Journal Reader</span></span>                                                      |



 

 

 



