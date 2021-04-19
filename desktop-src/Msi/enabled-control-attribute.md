---
description: 這個屬性會指定是否啟用或停用指定的控制項。 停用時，大部分的控制項會顯示為灰色。
ms.assetid: d84b1b55-34e1-4173-b945-39a809014d55
title: 啟用的控制項屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb7c5cbbbc12353fc07cf50404a1feae1d98f1b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977814"
---
# <a name="enabled-control-attribute"></a><span data-ttu-id="b4342-104">啟用的控制項屬性</span><span class="sxs-lookup"><span data-stu-id="b4342-104">Enabled Control Attribute</span></span>

<span data-ttu-id="b4342-105">這個屬性會指定是否啟用或停用指定的控制項。</span><span class="sxs-lookup"><span data-stu-id="b4342-105">This attribute specifies if the given control is enabled or disabled.</span></span> <span data-ttu-id="b4342-106">停用時，大部分的控制項會顯示為灰色。</span><span class="sxs-lookup"><span data-stu-id="b4342-106">Most controls appear gray when disabled.</span></span>

<span data-ttu-id="b4342-107">如果設定此位，則會建立啟用的控制項。</span><span class="sxs-lookup"><span data-stu-id="b4342-107">If this bit is set, the control is created as enabled.</span></span>

<span data-ttu-id="b4342-108">如果未設定此位，則會將控制項建立為停用。</span><span class="sxs-lookup"><span data-stu-id="b4342-108">If this bit is not set, the control is created as disabled.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="b4342-109">有效的控制項</span><span class="sxs-lookup"><span data-stu-id="b4342-109">Valid Controls</span></span>

<span data-ttu-id="b4342-110">所有控制項。</span><span class="sxs-lookup"><span data-stu-id="b4342-110">All controls.</span></span> <span data-ttu-id="b4342-111">某些與屬性沒有關聯的控制項（例如點陣圖和圖示）的外觀不受設定這個屬性的影響。</span><span class="sxs-lookup"><span data-stu-id="b4342-111">The appearance of some controls that are not associated with a property, such as Bitmaps and Icons, are unaffected by setting this attribute.</span></span>

## <a name="value"></a><span data-ttu-id="b4342-112">值</span><span class="sxs-lookup"><span data-stu-id="b4342-112">Value</span></span>



| <span data-ttu-id="b4342-113">Decimal</span><span class="sxs-lookup"><span data-stu-id="b4342-113">Decimal</span></span> | <span data-ttu-id="b4342-114">十六進位</span><span class="sxs-lookup"><span data-stu-id="b4342-114">Hexadecimal</span></span> | <span data-ttu-id="b4342-115">常數</span><span class="sxs-lookup"><span data-stu-id="b4342-115">Constant</span></span>                          |
|---------|-------------|-----------------------------------|
| <span data-ttu-id="b4342-116">2</span><span class="sxs-lookup"><span data-stu-id="b4342-116">2</span></span>       | <span data-ttu-id="b4342-117">0x00000002</span><span class="sxs-lookup"><span data-stu-id="b4342-117">0x00000002</span></span>  | <span data-ttu-id="b4342-118">**msidbControlAttributesEnabled**</span><span class="sxs-lookup"><span data-stu-id="b4342-118">**msidbControlAttributesEnabled**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="b4342-119">備註</span><span class="sxs-lookup"><span data-stu-id="b4342-119">Remarks</span></span>

<span data-ttu-id="b4342-120">您也可以使用 [ControlCondition 資料表](controlcondition-table.md) ，根據屬性或條件陳述式的值來停用或啟用控制項。</span><span class="sxs-lookup"><span data-stu-id="b4342-120">You can also use the [ControlCondition table](controlcondition-table.md) to disable or enable a control according to the value of a property or conditional statement.</span></span>

<span data-ttu-id="b4342-121">您也可以藉由將控制項訂閱至 [ControlEvent](control-events.md)來啟用或停用控制項。</span><span class="sxs-lookup"><span data-stu-id="b4342-121">You can also enable or disable a control by subscribing the control to a [ControlEvent](control-events.md).</span></span> <span data-ttu-id="b4342-122">在 [屬性] 資料行中輸入屬性的識別碼，並在 [EventMapping 資料表](eventmapping-table.md)的事件資料行中輸入事件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b4342-122">Enter the attribute's identifier in the Attribute column and the event's identifier in the Event column of the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="b4342-123">請參閱 [控制項屬性](control-attributes.md) 和您需要在 [控制項](controls.md)下建立的控制項。</span><span class="sxs-lookup"><span data-stu-id="b4342-123">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



