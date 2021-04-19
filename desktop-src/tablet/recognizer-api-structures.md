---
description: 本節說明辨識器結構。
ms.assetid: 4c17391f-7af4-42ab-b77f-e3c39cadc0b6
title: 辨識器結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: addaccf3e69f35b99379710d681fe8ac45559ea1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997575"
---
# <a name="recognizer-structures"></a><span data-ttu-id="f395d-103">辨識器結構</span><span class="sxs-lookup"><span data-stu-id="f395d-103">Recognizer Structures</span></span>

<span data-ttu-id="f395d-104">本節說明辨識器結構。</span><span class="sxs-lookup"><span data-stu-id="f395d-104">This section describes the recognizer structures.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f395d-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="f395d-105">In This Section</span></span>



| <span data-ttu-id="f395d-106">結構</span><span class="sxs-lookup"><span data-stu-id="f395d-106">Structure</span></span>                                                    | <span data-ttu-id="f395d-107">Description</span><span class="sxs-lookup"><span data-stu-id="f395d-107">Description</span></span>                                                                                                                                                   |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f395d-108">**字元 \_ 範圍**</span><span class="sxs-lookup"><span data-stu-id="f395d-108">**CHARACTER\_RANGE**</span></span>](/windows/win32/api/rectypes/ns-rectypes-character_range)                  | <span data-ttu-id="f395d-109">指定 Unicode 點的範圍 (字元) 。</span><span class="sxs-lookup"><span data-stu-id="f395d-109">Specifies a range of Unicode points (characters).</span></span><br/>                                                                                                  |
| [<span data-ttu-id="f395d-110">**>LATTICE \_ 計量**</span><span class="sxs-lookup"><span data-stu-id="f395d-110">**LATTICE\_METRICS**</span></span>](/windows/win32/api/rectypes/ns-rectypes-lattice_metrics)                  | <span data-ttu-id="f395d-111">描述基準和中線高度。</span><span class="sxs-lookup"><span data-stu-id="f395d-111">Describes the baseline and the midline height.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="f395d-112">**線段 \_**</span><span class="sxs-lookup"><span data-stu-id="f395d-112">**LINE\_SEGMENT**</span></span>](/windows/win32/api/rectypes/ns-rectypes-line_segment)                        | <span data-ttu-id="f395d-113">描述線條辨識區段的起點和終點，例如基準或中線。</span><span class="sxs-lookup"><span data-stu-id="f395d-113">Describes the start and end points of a line recognition segment, such as the baseline or midline.</span></span><br/>                                                 |
| [<span data-ttu-id="f395d-114">**封包 \_ 描述**</span><span class="sxs-lookup"><span data-stu-id="f395d-114">**PACKET\_DESCRIPTION**</span></span>](/windows/desktop/api/tpcshrd/ns-tpcshrd-packet_description)            | <span data-ttu-id="f395d-115">描述特定 tablet 內容的封包內容。</span><span class="sxs-lookup"><span data-stu-id="f395d-115">Describes the content of the packet for a particular tablet context.</span></span><br/>                                                                               |
| [<span data-ttu-id="f395d-116">**封包 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="f395d-116">**PACKET\_PROPERTY**</span></span>](/windows/desktop/api/tpcshrd/ns-tpcshrd-packet_property)                  | <span data-ttu-id="f395d-117">描述 tablet 驅動程式所報告的封包屬性。</span><span class="sxs-lookup"><span data-stu-id="f395d-117">Describes a packet property that is reported by the tablet driver.</span></span><br/>                                                                                 |
| [<span data-ttu-id="f395d-118">**屬性 \_ 度量**</span><span class="sxs-lookup"><span data-stu-id="f395d-118">**PROPERTY\_METRICS**</span></span>](/windows/desktop/api/tpcshrd/ns-tpcshrd-property_metrics)                | <span data-ttu-id="f395d-119">定義封包屬性的範圍和解析度。</span><span class="sxs-lookup"><span data-stu-id="f395d-119">Defines the range and resolution of a packet property.</span></span><br/>                                                                                             |
| [<span data-ttu-id="f395d-120">**辨識 \_ ATTRS**</span><span class="sxs-lookup"><span data-stu-id="f395d-120">**RECO\_ATTRS**</span></span>](/windows/win32/api/rectypes/ns-rectypes-reco_attrs)                            | <span data-ttu-id="f395d-121">抓取辨識器的屬性，或指定當您搜尋已安裝的辨識器時要使用的屬性。</span><span class="sxs-lookup"><span data-stu-id="f395d-121">Retrieves the attributes of a recognizer or specifies which attributes to use when you search for an installed recognizer.</span></span><br/>                         |
| [<span data-ttu-id="f395d-122">**辨識 \_ 指南**</span><span class="sxs-lookup"><span data-stu-id="f395d-122">**RECO\_GUIDE**</span></span>](/windows/win32/api/rectypes/ns-rectypes-reco_guide)                            | <span data-ttu-id="f395d-123">將筆墨的界限定義到辨識器。</span><span class="sxs-lookup"><span data-stu-id="f395d-123">Defines the boundaries of the ink to the recognizer.</span></span><br/>                                                                                               |
| [<span data-ttu-id="f395d-124">**辨識 \_ >LATTICE**</span><span class="sxs-lookup"><span data-stu-id="f395d-124">**RECO\_LATTICE**</span></span>](/windows/win32/api/rectypes/ns-rectypes-reco_lattice)                        | <span data-ttu-id="f395d-125">作為 >lattice 的進入點。</span><span class="sxs-lookup"><span data-stu-id="f395d-125">Serves as the entry point into a lattice.</span></span><br/>                                                                                                          |
| [<span data-ttu-id="f395d-126">**辨識 \_ >LATTICE 資料 \_ 行**</span><span class="sxs-lookup"><span data-stu-id="f395d-126">**RECO\_LATTICE\_COLUMN**</span></span>](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_column)         | <span data-ttu-id="f395d-127">表示 >lattice 中的資料行。</span><span class="sxs-lookup"><span data-stu-id="f395d-127">Represents a column in the lattice.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="f395d-128">**辨識 \_ >LATTICE \_ 元素**</span><span class="sxs-lookup"><span data-stu-id="f395d-128">**RECO\_LATTICE\_ELEMENT**</span></span>](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_element)       | <span data-ttu-id="f395d-129">對應到一個單字或一個東亞字元，通常是：不過，專案也可以對應至筆勢、圖形或其他程式碼。</span><span class="sxs-lookup"><span data-stu-id="f395d-129">Corresponds to one word or one East Asian character, typically; however, an element may also correspond to a gesture, a shape, or some other code.</span></span><br/> |
| [<span data-ttu-id="f395d-130">**辨識 \_ >LATTICE \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="f395d-130">**RECO\_LATTICE\_PROPERTIES**</span></span>](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_properties) | <span data-ttu-id="f395d-131">包含屬性結構指標的陣列。</span><span class="sxs-lookup"><span data-stu-id="f395d-131">Contains an array of pointers to property structures.</span></span><br/>                                                                                              |
| [<span data-ttu-id="f395d-132">**辨識 \_ >LATTICE \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="f395d-132">**RECO\_LATTICE\_PROPERTY**</span></span>](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_property)     | <span data-ttu-id="f395d-133">包含 >lattice 中所使用的屬性。</span><span class="sxs-lookup"><span data-stu-id="f395d-133">Contains a property used in the lattice.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="f395d-134">**辨識 \_ 範圍**</span><span class="sxs-lookup"><span data-stu-id="f395d-134">**RECO\_RANGE**</span></span>](/windows/win32/api/rectypes/ns-rectypes-reco_range)                            | <span data-ttu-id="f395d-135">識別結果字串中的字元範圍。</span><span class="sxs-lookup"><span data-stu-id="f395d-135">Identifies a range of characters in the result string.</span></span><br/>                                                                                             |
| [<span data-ttu-id="f395d-136">**筆劃 \_ 範圍**</span><span class="sxs-lookup"><span data-stu-id="f395d-136">**STROKE\_RANGE**</span></span>](/windows/win32/api/tpcshrd/ns-tpcshrd-stroke_range)                        | <span data-ttu-id="f395d-137">在 [**InkDisp**](inkdisp-class.md) 物件中指定筆劃的範圍。</span><span class="sxs-lookup"><span data-stu-id="f395d-137">Specifies a range of strokes in the [**InkDisp**](inkdisp-class.md) object.</span></span><br/>                                                                       |



 

 

 




