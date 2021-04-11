---
description: 針對筆記本檔中段落基準的起始點和結束點，提供 (x，y) 資訊。 這些值所使用的座標空間是 HIMETRIC。
ms.assetid: ff6a97ad-0e48-4128-8f94-24802b6ddc05
title: 基準元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b64986707eaa1b382d2f88851367b9147c59c5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191124"
---
# <a name="baseline-element"></a><span data-ttu-id="df5dc-104">基準元素</span><span class="sxs-lookup"><span data-stu-id="df5dc-104">Baseline Element</span></span>

<span data-ttu-id="df5dc-105">針對筆記本檔中段落基準的起始點和結束點，提供 (x，y) 資訊。</span><span class="sxs-lookup"><span data-stu-id="df5dc-105">Provides (x, y) information for the starting and ending points of the baseline of a paragraph in the Journal document.</span></span> <span data-ttu-id="df5dc-106">這些值所使用的座標空間是 **HIMETRIC**。</span><span class="sxs-lookup"><span data-stu-id="df5dc-106">The coordinate space used for these values is **HIMETRIC**.</span></span>

## <a name="definition"></a><span data-ttu-id="df5dc-107">定義</span><span class="sxs-lookup"><span data-stu-id="df5dc-107">Definition</span></span>

``` syntax
<xs:element name="Baseline" type="BaseLineType" />
```

## <a name="parent-elements"></a><span data-ttu-id="df5dc-108">父項目</span><span class="sxs-lookup"><span data-stu-id="df5dc-108">Parent Elements</span></span>

[<span data-ttu-id="df5dc-109">**ParagraphLineMetrics**</span><span class="sxs-lookup"><span data-stu-id="df5dc-109">**ParagraphLineMetrics**</span></span>](paragraphlinemetrics-element.md)

## <a name="child-elements"></a><span data-ttu-id="df5dc-110">子元素</span><span class="sxs-lookup"><span data-stu-id="df5dc-110">Child Elements</span></span>

<span data-ttu-id="df5dc-111">無。</span><span class="sxs-lookup"><span data-stu-id="df5dc-111">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="df5dc-112">屬性</span><span class="sxs-lookup"><span data-stu-id="df5dc-112">Attributes</span></span>



| <span data-ttu-id="df5dc-113">屬性</span><span class="sxs-lookup"><span data-stu-id="df5dc-113">Attribute</span></span>  | <span data-ttu-id="df5dc-114">類型</span><span class="sxs-lookup"><span data-stu-id="df5dc-114">Type</span></span>                      | <span data-ttu-id="df5dc-115">必要</span><span class="sxs-lookup"><span data-stu-id="df5dc-115">Required</span></span> | <span data-ttu-id="df5dc-116">描述</span><span class="sxs-lookup"><span data-stu-id="df5dc-116">Description</span></span>                                                      | <span data-ttu-id="df5dc-117">可能的值</span><span class="sxs-lookup"><span data-stu-id="df5dc-117">Possible Values</span></span>           |
|------------|---------------------------|----------|------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="df5dc-118">**StartX**</span><span class="sxs-lookup"><span data-stu-id="df5dc-118">**StartX**</span></span> | <span data-ttu-id="df5dc-119">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="df5dc-119">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="df5dc-120">必要</span><span class="sxs-lookup"><span data-stu-id="df5dc-120">Required</span></span> | <span data-ttu-id="df5dc-121">標示基準開頭的點 X 值。</span><span class="sxs-lookup"><span data-stu-id="df5dc-121">The X value for the point marking the beginning of the baseline.</span></span> | <span data-ttu-id="df5dc-122">任何非負整數。</span><span class="sxs-lookup"><span data-stu-id="df5dc-122">Any non-negative integer.</span></span> |
| <span data-ttu-id="df5dc-123">**StartY**</span><span class="sxs-lookup"><span data-stu-id="df5dc-123">**StartY**</span></span> | <span data-ttu-id="df5dc-124">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="df5dc-124">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="df5dc-125">必要</span><span class="sxs-lookup"><span data-stu-id="df5dc-125">Required</span></span> | <span data-ttu-id="df5dc-126">標示基準開頭的點 Y 值。</span><span class="sxs-lookup"><span data-stu-id="df5dc-126">The Y value for the point marking the beginning of the baseline.</span></span> | <span data-ttu-id="df5dc-127">任何非負整數。</span><span class="sxs-lookup"><span data-stu-id="df5dc-127">Any non-negative integer.</span></span> |
| <span data-ttu-id="df5dc-128">**EndX**</span><span class="sxs-lookup"><span data-stu-id="df5dc-128">**EndX**</span></span>   | <span data-ttu-id="df5dc-129">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="df5dc-129">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="df5dc-130">必要</span><span class="sxs-lookup"><span data-stu-id="df5dc-130">Required</span></span> | <span data-ttu-id="df5dc-131">標示基準結尾之點的 X 值。</span><span class="sxs-lookup"><span data-stu-id="df5dc-131">The X value for the point marking the end of the baseline.</span></span>       | <span data-ttu-id="df5dc-132">任何非負整數。</span><span class="sxs-lookup"><span data-stu-id="df5dc-132">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="df5dc-133">項目資訊</span><span class="sxs-lookup"><span data-stu-id="df5dc-133">Element Information</span></span>



|              |                                                               |
|--------------|---------------------------------------------------------------|
| <span data-ttu-id="df5dc-134">項目類型</span><span class="sxs-lookup"><span data-stu-id="df5dc-134">Element type</span></span> | <span data-ttu-id="df5dc-135">[**BaselineType**](baselinetype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="df5dc-135">[**BaselineType**](baselinetype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="df5dc-136">命名空間</span><span class="sxs-lookup"><span data-stu-id="df5dc-136">Namespace</span></span>    | <span data-ttu-id="df5dc-137">urn：架構-microsoft-com：平板電腦： richink</span><span class="sxs-lookup"><span data-stu-id="df5dc-137">urn:schemas-microsoft-com:tabletpc:richink</span></span>                    |
| <span data-ttu-id="df5dc-138">結構描述名稱</span><span class="sxs-lookup"><span data-stu-id="df5dc-138">Schema name</span></span>  | <span data-ttu-id="df5dc-139">日誌讀者</span><span class="sxs-lookup"><span data-stu-id="df5dc-139">Journal Reader</span></span>                                                |



 

 

 



