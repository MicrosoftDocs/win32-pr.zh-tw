---
description: 如果已設定可見的控制項位，則會在對話方塊中顯示控制項。 如果未設定此位，則會在對話方塊中隱藏控制項。 Visible 控制項屬性的可見或隱藏狀態可以稍後由控制項事件變更。
ms.assetid: 77d3164c-ea8a-4dcf-afd5-02bb2c2568c6
title: Visible 控制項屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 550513f6bd0e40e58694c2c15a9986b5b02f289c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970156"
---
# <a name="visible-control-attribute"></a><span data-ttu-id="541c8-105">Visible 控制項屬性</span><span class="sxs-lookup"><span data-stu-id="541c8-105">Visible Control Attribute</span></span>

<span data-ttu-id="541c8-106">如果已設定可見的控制項位，則會在對話方塊中顯示控制項。</span><span class="sxs-lookup"><span data-stu-id="541c8-106">If the Visible Control bit is set, the control is visible on the dialog box.</span></span> <span data-ttu-id="541c8-107">如果未設定此位，則會在對話方塊中隱藏控制項。</span><span class="sxs-lookup"><span data-stu-id="541c8-107">If this bit is not set, the control is hidden on the dialog box.</span></span> <span data-ttu-id="541c8-108">Visible 控制項屬性的可見或隱藏狀態可以稍後由 [控制項事件](control-events.md)變更。</span><span class="sxs-lookup"><span data-stu-id="541c8-108">The visible or hidden state of the Visible control attribute can be later changed by a [Control Event](control-events.md).</span></span>

## <a name="valid-controls"></a><span data-ttu-id="541c8-109">有效的控制項</span><span class="sxs-lookup"><span data-stu-id="541c8-109">Valid Controls</span></span>

<span data-ttu-id="541c8-110">所有控制項。</span><span class="sxs-lookup"><span data-stu-id="541c8-110">All controls.</span></span>

## <a name="value"></a><span data-ttu-id="541c8-111">值</span><span class="sxs-lookup"><span data-stu-id="541c8-111">Value</span></span>



| <span data-ttu-id="541c8-112">Decimal</span><span class="sxs-lookup"><span data-stu-id="541c8-112">Decimal</span></span> | <span data-ttu-id="541c8-113">十六進位</span><span class="sxs-lookup"><span data-stu-id="541c8-113">Hexadecimal</span></span> | <span data-ttu-id="541c8-114">常數</span><span class="sxs-lookup"><span data-stu-id="541c8-114">Constant</span></span>                          |
|---------|-------------|-----------------------------------|
| <span data-ttu-id="541c8-115">1</span><span class="sxs-lookup"><span data-stu-id="541c8-115">1</span></span>       | <span data-ttu-id="541c8-116">0x00000001</span><span class="sxs-lookup"><span data-stu-id="541c8-116">0x00000001</span></span>  | <span data-ttu-id="541c8-117">**msidbControlAttributesVisible**</span><span class="sxs-lookup"><span data-stu-id="541c8-117">**msidbControlAttributesVisible**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="541c8-118">備註</span><span class="sxs-lookup"><span data-stu-id="541c8-118">Remarks</span></span>

<span data-ttu-id="541c8-119">您可以使用 [ControlCondition 資料表](controlcondition-table.md) ，根據屬性或條件陳述式的值來顯示或隱藏控制項。</span><span class="sxs-lookup"><span data-stu-id="541c8-119">You can use the [ControlCondition table](controlcondition-table.md) to show or hide a control according to the value of a property or conditional statement.</span></span> <span data-ttu-id="541c8-120">您也可以藉由將控制項訂閱至 [ControlEvent](control-events.md)來顯示或隱藏控制項。</span><span class="sxs-lookup"><span data-stu-id="541c8-120">You can also show or hide a control by subscribing the control to a [ControlEvent](control-events.md).</span></span> <span data-ttu-id="541c8-121">在 [屬性] 資料行中輸入屬性的識別碼，並在 [EventMapping 資料表](eventmapping-table.md)的事件資料行中輸入事件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="541c8-121">Enter the attribute's identifier in the Attribute column and the event's identifier in the Event column of the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="541c8-122">請參閱 [控制項屬性](control-attributes.md) 和 [控制項](controls.md)。</span><span class="sxs-lookup"><span data-stu-id="541c8-122">See [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



