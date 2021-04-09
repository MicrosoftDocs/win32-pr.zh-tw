---
description: 線條控制項是水平線條。
ms.assetid: 8b180b71-1e80-47c0-bb44-d5fcecabaed2
title: 線條控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba3b7374574e2a0087e7dae8d0ffa9f097be9f45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692487"
---
# <a name="line-control"></a><span data-ttu-id="03fb3-103">線條控制項</span><span class="sxs-lookup"><span data-stu-id="03fb3-103">Line Control</span></span>

<span data-ttu-id="03fb3-104">線條控制項是水平線條。</span><span class="sxs-lookup"><span data-stu-id="03fb3-104">The Line control is a horizontal line.</span></span>

## <a name="control-attributes"></a><span data-ttu-id="03fb3-105">控制項屬性</span><span class="sxs-lookup"><span data-stu-id="03fb3-105">Control Attributes</span></span>

<span data-ttu-id="03fb3-106">您可以將下列屬性與這個控制項搭配使用。</span><span class="sxs-lookup"><span data-stu-id="03fb3-106">You can use the following attributes with this control.</span></span> <span data-ttu-id="03fb3-107">若要使用事件來變更屬性的值，請將控制項訂閱至 [EventMapping 資料表](eventmapping-table.md) 中的 ControlEvent，並在 [屬性] 資料行中列出屬性的識別碼。</span><span class="sxs-lookup"><span data-stu-id="03fb3-107">To change the value of an attribute using an event, subscribe the control to a ControlEvent in the [EventMapping table](eventmapping-table.md) and list the attribute's identifier in the Attribute column.</span></span> <span data-ttu-id="03fb3-108">在 [事件] 資料行中輸入 ControlEvent 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="03fb3-108">Enter the identifier of the ControlEvent in the Event column.</span></span>



| <span data-ttu-id="03fb3-109">屬性識別碼</span><span class="sxs-lookup"><span data-stu-id="03fb3-109">Attribute identifier</span></span>                       | <span data-ttu-id="03fb3-110">十六進位位</span><span class="sxs-lookup"><span data-stu-id="03fb3-110">Hexadecimal bit</span></span>                  | <span data-ttu-id="03fb3-111">Description</span><span class="sxs-lookup"><span data-stu-id="03fb3-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="03fb3-112">位置</span><span class="sxs-lookup"><span data-stu-id="03fb3-112">Position</span></span>](position-control-attribute.md) |                                  | <span data-ttu-id="03fb3-113">對話方塊中控制項的位置。</span><span class="sxs-lookup"><span data-stu-id="03fb3-113">Position of the control in the dialog box.</span></span> <span data-ttu-id="03fb3-114">將控制項左上角的寬度、高度和 Y 座標，輸入控制項 [資料表](control-table.md) 或 [BBControl 資料表](bbcontrol-table.md)的 Width、Height、X 和 Y 資料行中。</span><span class="sxs-lookup"><span data-stu-id="03fb3-114">Enter the control's width, height, and coordinates of the control's left corner into the Width, Height, X, and Y columns of the [Control table](control-table.md) or [BBControl table](bbcontrol-table.md).</span></span> <span data-ttu-id="03fb3-115">使用 [安裝程式單位](installer-units.md) 來表示長度和距離。</span><span class="sxs-lookup"><span data-stu-id="03fb3-115">Use [installer units](installer-units.md) for length and distance.</span></span><br/>                                         |
| [<span data-ttu-id="03fb3-116">Visible</span><span class="sxs-lookup"><span data-stu-id="03fb3-116">Visible</span></span>](visible-control-attribute.md)   | <span data-ttu-id="03fb3-117">0x00000000 0x00000001</span><span class="sxs-lookup"><span data-stu-id="03fb3-117">0x00000000 0x00000001</span></span><br/> | <span data-ttu-id="03fb3-118">隱藏的控制項。</span><span class="sxs-lookup"><span data-stu-id="03fb3-118">Hidden control.</span></span> <span data-ttu-id="03fb3-119">可見的控制項。</span><span class="sxs-lookup"><span data-stu-id="03fb3-119">Visible control.</span></span><br/> <span data-ttu-id="03fb3-120">請在 [control table](control-table.md) 或 [BBControl 資料表](bbcontrol-table.md) 中的 Attributes 資料行的位字組中包含這個位，讓控制項在建立時可見或隱藏。</span><span class="sxs-lookup"><span data-stu-id="03fb3-120">Include this bit in the bit word of the Attributes column in the [Control table](control-table.md) or [BBControl table](bbcontrol-table.md) to make the control visible or hidden upon its creation.</span></span><br/> <span data-ttu-id="03fb3-121">您也可以使用 [ControlCondition 資料表](controlcondition-table.md)來隱藏或顯示控制項。</span><span class="sxs-lookup"><span data-stu-id="03fb3-121">You can also hide or show a control by using the [ControlCondition table](controlcondition-table.md).</span></span><br/> |
| [<span data-ttu-id="03fb3-122">沉沒</span><span class="sxs-lookup"><span data-stu-id="03fb3-122">Sunken</span></span>](sunken-control-attribute.md)     | <span data-ttu-id="03fb3-123">0x00000000 0x00000004</span><span class="sxs-lookup"><span data-stu-id="03fb3-123">0x00000000 0x00000004</span></span><br/> | <span data-ttu-id="03fb3-124">顯示預設的視覺化樣式。</span><span class="sxs-lookup"><span data-stu-id="03fb3-124">Displays the default visual style.</span></span> <span data-ttu-id="03fb3-125">顯示具有凹陷、立體外觀的控制項。</span><span class="sxs-lookup"><span data-stu-id="03fb3-125">Displays the control with a sunken, 3-D look.</span></span><br/> <span data-ttu-id="03fb3-126">在 [控制項資料表](control-table.md)的 [屬性] 資料行中，將這些位包含在位字中。</span><span class="sxs-lookup"><span data-stu-id="03fb3-126">Include these bits in the bit word in the Attributes column of the [Control table](control-table.md).</span></span><br/>                                                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="03fb3-127">備註</span><span class="sxs-lookup"><span data-stu-id="03fb3-127">Remarks</span></span>

<span data-ttu-id="03fb3-128">您可以使用 [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) 函數，從靜態類別建立這個控制項。</span><span class="sxs-lookup"><span data-stu-id="03fb3-128">This control can be created from the STATIC class by using the [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function.</span></span> <span data-ttu-id="03fb3-129">它有 **ss \_ ETCHEDHORZ** 和 **ss 的 \_ 凹陷** 樣式。</span><span class="sxs-lookup"><span data-stu-id="03fb3-129">It has the **SS\_ETCHEDHORZ** and **SS\_SUNKEN** styles.</span></span>

 

 
