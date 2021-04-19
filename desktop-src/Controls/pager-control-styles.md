---
title: " (CommCtrl 的呼機控制項樣式) "
description: 此區段會列出建立呼機控制項時使用的視窗樣式。
ms.assetid: 619fd8cc-e231-41af-8744-a29d14f2c6f8
topic_type:
- apiref
api_name:
- PGS_AUTOSCROLL
- PGS_DRAGNDROP
- PGS_HORZ
- PGS_VERT
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 496737f714ecb58c0d5a349207114cbf338e2c54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976067"
---
# <a name="pager-control-styles"></a><span data-ttu-id="383b1-103">呼機控制項樣式</span><span class="sxs-lookup"><span data-stu-id="383b1-103">Pager Control Styles</span></span>

<span data-ttu-id="383b1-104">此區段會列出建立呼機控制項時使用的視窗樣式。</span><span class="sxs-lookup"><span data-stu-id="383b1-104">This section lists the window styles used when creating pager controls.</span></span>



| <span data-ttu-id="383b1-105">常數</span><span class="sxs-lookup"><span data-stu-id="383b1-105">Constant</span></span>                                                                                                                                                         | <span data-ttu-id="383b1-106">描述</span><span class="sxs-lookup"><span data-stu-id="383b1-106">Description</span></span>                                                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PGS_AUTOSCROLL"></span><span id="pgs_autoscroll"></span><dl> <span data-ttu-id="383b1-107"><dt>**PG \_ AUTOSCROLL**</dt></span><span class="sxs-lookup"><span data-stu-id="383b1-107"><dt>**PGS\_AUTOSCROLL**</dt></span></span> </dl> | <span data-ttu-id="383b1-108">當使用者將滑鼠停留在其中一個捲軸按鈕上方時，就會滾動頁控制項。</span><span class="sxs-lookup"><span data-stu-id="383b1-108">The pager control will scroll when the user hovers the mouse over one of the scroll buttons.</span></span><br/>                                                                                                                     |
| <span id="PGS_DRAGNDROP"></span><span id="pgs_dragndrop"></span><dl> <span data-ttu-id="383b1-109"><dt>**PG \_ DRAGNDROP**</dt></span><span class="sxs-lookup"><span data-stu-id="383b1-109"><dt>**PGS\_DRAGNDROP**</dt></span></span> </dl>    | <span data-ttu-id="383b1-110">包含的視窗可以是拖放目標。</span><span class="sxs-lookup"><span data-stu-id="383b1-110">The contained window can be a drag-and-drop target.</span></span> <span data-ttu-id="383b1-111">如果從分頁外部將某個專案拖曳至其中一個捲軸按鈕，則會自動滾動頁控制項。</span><span class="sxs-lookup"><span data-stu-id="383b1-111">The pager control will automatically scroll if an item is dragged from outside the pager over one of the scroll buttons.</span></span><br/>                                     |
| <span id="PGS_HORZ"></span><span id="pgs_horz"></span><dl> <span data-ttu-id="383b1-112"><dt>**PG \_ HORZ**</dt></span><span class="sxs-lookup"><span data-stu-id="383b1-112"><dt>**PGS\_HORZ**</dt></span></span> </dl>                   | <span data-ttu-id="383b1-113">建立可水準滾動的呼機控制項。</span><span class="sxs-lookup"><span data-stu-id="383b1-113">Creates a pager control that can be scrolled horizontally.</span></span> <span data-ttu-id="383b1-114">這個樣式和 **pg \_ 垂直** 樣式是互斥的，無法合併。</span><span class="sxs-lookup"><span data-stu-id="383b1-114">This style and the **PGS\_VERT** style are mutually exclusive and cannot be combined.</span></span><br/>                                                                 |
| <span id="PGS_VERT"></span><span id="pgs_vert"></span><dl> <span data-ttu-id="383b1-115"><dt>**PG \_ 垂直**</dt></span><span class="sxs-lookup"><span data-stu-id="383b1-115"><dt>**PGS\_VERT**</dt></span></span> </dl>                   | <span data-ttu-id="383b1-116">建立可以垂直捲動的分頁控制項。</span><span class="sxs-lookup"><span data-stu-id="383b1-116">Creates a pager control that can be scrolled vertically.</span></span> <span data-ttu-id="383b1-117">如果未指定方向樣式，則這是預設方向。</span><span class="sxs-lookup"><span data-stu-id="383b1-117">This is the default direction if no direction style is specified.</span></span> <span data-ttu-id="383b1-118">這個樣式和 **pg \_ HORZ** 樣式互斥，而且無法合併。</span><span class="sxs-lookup"><span data-stu-id="383b1-118">This style and the **PGS\_HORZ** style are mutually exclusive and cannot be combined.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="383b1-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="383b1-119">Requirements</span></span>



| <span data-ttu-id="383b1-120">需求</span><span class="sxs-lookup"><span data-stu-id="383b1-120">Requirement</span></span> | <span data-ttu-id="383b1-121">值</span><span class="sxs-lookup"><span data-stu-id="383b1-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="383b1-122">標頭</span><span class="sxs-lookup"><span data-stu-id="383b1-122">Header</span></span><br/> | <dl> <span data-ttu-id="383b1-123"><dt>CommCtrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="383b1-123"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





