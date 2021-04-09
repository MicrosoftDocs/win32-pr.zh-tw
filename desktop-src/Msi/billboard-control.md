---
description: 佈告欄控制項顯示常用的控制項，這些控制項是透過控制項來加入和移除對話方塊中。
ms.assetid: c4c0ed5a-2518-499f-805f-dcbe0b0f9393
title: 佈告欄控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e056a764ec4a71c3ce6785acf331b4bc1ff95ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848956"
---
# <a name="billboard-control"></a><span data-ttu-id="acbb1-103">佈告欄控制項</span><span class="sxs-lookup"><span data-stu-id="acbb1-103">Billboard Control</span></span>

<span data-ttu-id="acbb1-104">佈告欄控制項顯示常用的控制項，這些控制項是透過控制項來加入和移除對話方塊中。</span><span class="sxs-lookup"><span data-stu-id="acbb1-104">The Billboard control displays commonly used controls that are added and removed from the dialog box by ControlEvents.</span></span> <span data-ttu-id="acbb1-105">只有未與屬性相關聯的控制項（例如 [文字](text-control.md)、 [點陣圖](bitmap-control.md)或 [圖示](icon-control.md)）或自訂控制項才能放置在佈告欄上。</span><span class="sxs-lookup"><span data-stu-id="acbb1-105">Only controls that are not associated with a property, such as [Text](text-control.md), [Bitmap](bitmap-control.md), or [Icon](icon-control.md), or custom controls can be placed on a billboard.</span></span> <span data-ttu-id="acbb1-106">佈告欄控制項通常會顯示進度訊息。</span><span class="sxs-lookup"><span data-stu-id="acbb1-106">Billboard controls most typically display progress messages.</span></span>

## <a name="control-attributes"></a><span data-ttu-id="acbb1-107">控制項屬性</span><span class="sxs-lookup"><span data-stu-id="acbb1-107">Control Attributes</span></span>

<span data-ttu-id="acbb1-108">您可以將下列屬性與佈告欄控制項搭配使用。</span><span class="sxs-lookup"><span data-stu-id="acbb1-108">You can use the following attributes with the Billboard control.</span></span> <span data-ttu-id="acbb1-109">若要使用事件來變更屬性的值，請將控制項訂閱至 [EventMapping 資料表](eventmapping-table.md) 中的 ControlEvent，並在 [屬性] 資料行中列出屬性的識別碼。</span><span class="sxs-lookup"><span data-stu-id="acbb1-109">To change the value of an attribute using an event, subscribe the control to a ControlEvent in the [EventMapping table](eventmapping-table.md) and list the attribute's identifier in the Attribute column.</span></span> <span data-ttu-id="acbb1-110">在 [事件] 資料行中輸入 ControlEvent 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="acbb1-110">Enter the identifier of the ControlEvent in the Event column.</span></span>



| <span data-ttu-id="acbb1-111">屬性識別碼</span><span class="sxs-lookup"><span data-stu-id="acbb1-111">Attribute identifier</span></span>                                 | <span data-ttu-id="acbb1-112">十六進位位</span><span class="sxs-lookup"><span data-stu-id="acbb1-112">Hexadecimal bit</span></span>                  | <span data-ttu-id="acbb1-113">Description</span><span class="sxs-lookup"><span data-stu-id="acbb1-113">Description</span></span>                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="acbb1-114">BillboardName</span><span class="sxs-lookup"><span data-stu-id="acbb1-114">BillboardName</span></span>](billboardname-control-attribute.md) |                                  | <span data-ttu-id="acbb1-115">目前佈告欄的名稱。</span><span class="sxs-lookup"><span data-stu-id="acbb1-115">Name of the current billboard.</span></span> <span data-ttu-id="acbb1-116">在 [BBControl 資料表](bbcontrol-table.md)的 [佈告欄] 資料行中輸入佈告欄的識別碼。</span><span class="sxs-lookup"><span data-stu-id="acbb1-116">Enter the billboard's identifier in the Billboard column of the [BBControl table](bbcontrol-table.md).</span></span><br/>                                                                                                                                                                            |
| [<span data-ttu-id="acbb1-117">位置</span><span class="sxs-lookup"><span data-stu-id="acbb1-117">Position</span></span>](position-control-attribute.md)           |                                  | <span data-ttu-id="acbb1-118">對話方塊中的控制項位置。</span><span class="sxs-lookup"><span data-stu-id="acbb1-118">Position of control in the dialog box.</span></span> <span data-ttu-id="acbb1-119">將控制項左上角的控制項寬度、高度和座標，輸入至 [BBControl 資料表](bbcontrol-table.md)的 Width、Height、X 和 Y 資料行中。</span><span class="sxs-lookup"><span data-stu-id="acbb1-119">Enter the control's width, height, and coordinates of the control's left corner into the Width, Height, X, and Y columns of the [BBControl table](bbcontrol-table.md).</span></span> <span data-ttu-id="acbb1-120">使用 [安裝程式單位](installer-units.md) 來表示長度和距離。</span><span class="sxs-lookup"><span data-stu-id="acbb1-120">Use [installer units](installer-units.md) for length and distance.</span></span><br/>                                |
| [<span data-ttu-id="acbb1-121">Visible</span><span class="sxs-lookup"><span data-stu-id="acbb1-121">Visible</span></span>](visible-control-attribute.md)             | <span data-ttu-id="acbb1-122">0x00000000 0x00000001</span><span class="sxs-lookup"><span data-stu-id="acbb1-122">0x00000000 0x00000001</span></span><br/> | <span data-ttu-id="acbb1-123">隱藏的控制項。</span><span class="sxs-lookup"><span data-stu-id="acbb1-123">Hidden control.</span></span> <span data-ttu-id="acbb1-124">可見的控制項。</span><span class="sxs-lookup"><span data-stu-id="acbb1-124">Visible control.</span></span><br/> <span data-ttu-id="acbb1-125">在 [BBControl 資料表](bbcontrol-table.md) 的 [屬性] 資料行的位字組中包含這個位，讓控制項在建立時顯示或隱藏。</span><span class="sxs-lookup"><span data-stu-id="acbb1-125">Include this bit in the bit word of the Attributes column in the [BBControl table](bbcontrol-table.md) to make the control visible or hidden upon its creation.</span></span><br/> <span data-ttu-id="acbb1-126">使用 [ControlCondition 資料表](controlcondition-table.md)隱藏或顯示控制項。</span><span class="sxs-lookup"><span data-stu-id="acbb1-126">Hide or show a control by using the [ControlCondition table](controlcondition-table.md).</span></span><br/> |
| [<span data-ttu-id="acbb1-127">沉沒</span><span class="sxs-lookup"><span data-stu-id="acbb1-127">Sunken</span></span>](sunken-control-attribute.md)               | <span data-ttu-id="acbb1-128">0x00000000 0x00000004</span><span class="sxs-lookup"><span data-stu-id="acbb1-128">0x00000000 0x00000004</span></span><br/> | <span data-ttu-id="acbb1-129">顯示預設的視覺化樣式。</span><span class="sxs-lookup"><span data-stu-id="acbb1-129">Displays the default visual style.</span></span> <span data-ttu-id="acbb1-130">顯示具有凹陷、立體、外觀的控制項。</span><span class="sxs-lookup"><span data-stu-id="acbb1-130">Displays the control with a sunken, 3-D, look.</span></span><br/> <span data-ttu-id="acbb1-131">在 [控制項資料表](control-table.md)的 [屬性] 資料行中，將這些位包含在位字中。</span><span class="sxs-lookup"><span data-stu-id="acbb1-131">Include these bits in the bit word in the Attributes column of the [Control table](control-table.md).</span></span><br/>                                                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="acbb1-132">備註</span><span class="sxs-lookup"><span data-stu-id="acbb1-132">Remarks</span></span>

<span data-ttu-id="acbb1-133">此控制項沒有自己的視窗。</span><span class="sxs-lookup"><span data-stu-id="acbb1-133">This control has no window of its own.</span></span>

<span data-ttu-id="acbb1-134">出現在完整使用者介面中的佈告欄控制項會列在 [佈告欄資料表](billboard-table.md)中。</span><span class="sxs-lookup"><span data-stu-id="acbb1-134">Billboard controls that appear in the full user interface are listed in the [Billboard table](billboard-table.md).</span></span>

<span data-ttu-id="acbb1-135">位於佈告欄的控制項必須列在 [BBControl 資料表](bbcontrol-table.md) 中，而不是 [控制資料表](control-table.md)中。</span><span class="sxs-lookup"><span data-stu-id="acbb1-135">Controls that are located on a billboard must be listed in the [BBControl table](bbcontrol-table.md) rather than the [Control table](control-table.md).</span></span>

 

 




