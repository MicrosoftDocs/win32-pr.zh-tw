---
description: 本節包含 InkPicture 控制項的方法。
ms.assetid: 5691e595-f264-4547-9db6-f984483005e8
title: InkPicture 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b28d15c61105e9cb5aa690860a0362aac826f019
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320935"
---
# <a name="inkpicture-methods"></a><span data-ttu-id="be2b5-103">InkPicture 方法</span><span class="sxs-lookup"><span data-stu-id="be2b5-103">InkPicture Methods</span></span>

<span data-ttu-id="be2b5-104">本節包含 InkPicture 控制項的方法。</span><span class="sxs-lookup"><span data-stu-id="be2b5-104">This section contains Methods for the InkPicture Control.</span></span>



| <span data-ttu-id="be2b5-105">方法</span><span class="sxs-lookup"><span data-stu-id="be2b5-105">Method</span></span>                                                                                   | <span data-ttu-id="be2b5-106">描述</span><span class="sxs-lookup"><span data-stu-id="be2b5-106">Description</span></span>                                                                                                                                                                      |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="be2b5-107">**GetEventInterest 方法**</span><span class="sxs-lookup"><span data-stu-id="be2b5-107">**GetEventInterest Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-geteventinterest)                           | <span data-ttu-id="be2b5-108">抓取值，指出 [InkPicture](inkpicture-control-reference.md) 控制項是否對特定事件感興趣。</span><span class="sxs-lookup"><span data-stu-id="be2b5-108">Retrieves a value that indicates whether the [InkPicture](inkpicture-control-reference.md) control has interest in a particular event.</span></span><br/>                               |
| [<span data-ttu-id="be2b5-109">**GetGestureStatus**</span><span class="sxs-lookup"><span data-stu-id="be2b5-109">**GetGestureStatus**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-getgesturestatus)                                  | <span data-ttu-id="be2b5-110">抓取值，指出 [InkPicture](inkpicture-control-reference.md) 控制項是否對特定應用程式手勢感興趣。</span><span class="sxs-lookup"><span data-stu-id="be2b5-110">Retrieves a value that indicates whether the [InkPicture](inkpicture-control-reference.md) control has interest in a particular application gesture.</span></span><br/>                 |
| [<span data-ttu-id="be2b5-111">**GetWindowInputRectangle 方法**</span><span class="sxs-lookup"><span data-stu-id="be2b5-111">**GetWindowInputRectangle Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-getwindowinputrectangle)             | <span data-ttu-id="be2b5-112">傳回用來繪製筆墨的視窗矩形（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="be2b5-112">Returns the window rectangle, in pixels, within which ink is drawn.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="be2b5-113">**HitTestSelection**</span><span class="sxs-lookup"><span data-stu-id="be2b5-113">**HitTestSelection**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-hittestselection)                                  | <span data-ttu-id="be2b5-114">抓取 [**SelectionHitResult**](/windows/desktop/api/msinkaut/ne-msinkaut-selectionhitresult) 列舉的成員，此列舉會指定點擊測試期間遇到的部分（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="be2b5-114">Retrieves a member of the [**SelectionHitResult**](/windows/desktop/api/msinkaut/ne-msinkaut-selectionhitresult) enumeration, which specifies which part of a selection, if any, was hit during a hit test.</span></span><br/> |
| [<span data-ttu-id="be2b5-115">**SetAllTabletsMode 方法**</span><span class="sxs-lookup"><span data-stu-id="be2b5-115">**SetAllTabletsMode Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setalltabletsmode)                         | <span data-ttu-id="be2b5-116">讓 [InkPicture](inkpicture-control-reference.md) 控制項從任何連接到 tablet PC 的平板電腦收集筆跡。</span><span class="sxs-lookup"><span data-stu-id="be2b5-116">Enables the [InkPicture](inkpicture-control-reference.md) control to collect ink from any tablet attached to the Tablet PC.</span></span><br/>                                          |
| [<span data-ttu-id="be2b5-117">**SetEventInterest 方法**</span><span class="sxs-lookup"><span data-stu-id="be2b5-117">**SetEventInterest Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-seteventinterest)                           | <span data-ttu-id="be2b5-118">修改值，指出 [InkPicture](inkpicture-control-reference.md) 控制項是否對指定的事件感興趣。</span><span class="sxs-lookup"><span data-stu-id="be2b5-118">Modifies a value that indicates whether an [InkPicture](inkpicture-control-reference.md) control has interest in a specified event.</span></span><br/>                                  |
| [<span data-ttu-id="be2b5-119">**SetGestureStatus 方法**</span><span class="sxs-lookup"><span data-stu-id="be2b5-119">**SetGestureStatus Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setgesturestatus)                           | <span data-ttu-id="be2b5-120">修改指定應用程式手勢中 [InkPicture](inkpicture-control-reference.md) 物件的感興趣。</span><span class="sxs-lookup"><span data-stu-id="be2b5-120">Modifies the interest of the [InkPicture](inkpicture-control-reference.md) object in a specified application gesture.</span></span><br/>                                                |
| [<span data-ttu-id="be2b5-121">**SetSingleTabletIntegratedMode 方法**</span><span class="sxs-lookup"><span data-stu-id="be2b5-121">**SetSingleTabletIntegratedMode Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setsingletabletintegratedmode) | <span data-ttu-id="be2b5-122">修改 [InkPicture](inkpicture-control-reference.md) 控制項，以從一台連接到 tablet PC 的平板電腦收集筆跡。</span><span class="sxs-lookup"><span data-stu-id="be2b5-122">Modifies the [InkPicture](inkpicture-control-reference.md) control to collect ink from only one tablet attached to the Tablet PC.</span></span> <span data-ttu-id="be2b5-123">其他平板電腦的筆墨會被忽略。</span><span class="sxs-lookup"><span data-stu-id="be2b5-123">Ink from other tablets is ignored.</span></span><br/> |
| [<span data-ttu-id="be2b5-124">**SetWindowInputRectangle 方法**</span><span class="sxs-lookup"><span data-stu-id="be2b5-124">**SetWindowInputRectangle Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setwindowinputrectangle)             | <span data-ttu-id="be2b5-125">指定視窗座標中要設定的視窗矩形，以在其中繪製筆墨。</span><span class="sxs-lookup"><span data-stu-id="be2b5-125">Specifies the window rectangle to set, in window coordinates, within which ink is drawn.</span></span><br/>                                                                              |



 

 

 




