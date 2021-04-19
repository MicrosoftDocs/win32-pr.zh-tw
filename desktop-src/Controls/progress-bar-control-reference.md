---
title: 進度列
description: 本章節包含與進度列控制項搭配使用之程式設計項目的相關資訊。
ms.assetid: vs|controls|~\controls\progbar\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08b99a31bbbd3b80de0d528d5232c79c28af1e1f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967611"
---
# <a name="progress-bar"></a><span data-ttu-id="3c07e-103">進度列</span><span class="sxs-lookup"><span data-stu-id="3c07e-103">Progress Bar</span></span>

<span data-ttu-id="3c07e-104">本章節包含與進度列控制項搭配使用之程式設計項目的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3c07e-104">This section contains information about the programming elements used with progress bar controls.</span></span>

### <a name="overviews"></a><span data-ttu-id="3c07e-105">概觀</span><span class="sxs-lookup"><span data-stu-id="3c07e-105">Overviews</span></span>



| <span data-ttu-id="3c07e-106">主題</span><span class="sxs-lookup"><span data-stu-id="3c07e-106">Topic</span></span>                                            | <span data-ttu-id="3c07e-107">目錄</span><span class="sxs-lookup"><span data-stu-id="3c07e-107">Contents</span></span>                                                                                                           |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3c07e-108">進度列控制項</span><span class="sxs-lookup"><span data-stu-id="3c07e-108">Progress Bar Control</span></span>](progress-bar-control.md) | <span data-ttu-id="3c07e-109">進度列是一種視窗，可讓應用程式用來指出冗長作業的進度。</span><span class="sxs-lookup"><span data-stu-id="3c07e-109">A progress bar is a window that an application can use to indicate the progress of a lengthy operation.</span></span><br/> |



 

### <a name="messages"></a><span data-ttu-id="3c07e-110">訊息</span><span class="sxs-lookup"><span data-stu-id="3c07e-110">Messages</span></span>



| <span data-ttu-id="3c07e-111">主題</span><span class="sxs-lookup"><span data-stu-id="3c07e-111">Topic</span></span>                                       | <span data-ttu-id="3c07e-112">目錄</span><span class="sxs-lookup"><span data-stu-id="3c07e-112">Contents</span></span>                                                                                                                                                                                                                                                              |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3c07e-113">**PBM \_ DELTAPOS**</span><span class="sxs-lookup"><span data-stu-id="3c07e-113">**PBM\_DELTAPOS**</span></span>](pbm-deltapos.md)       | <span data-ttu-id="3c07e-114">依指定的遞增量將進度列的目前位置往前移，並重新繪製橫條以反映新的位置。</span><span class="sxs-lookup"><span data-stu-id="3c07e-114">Advances the current position of a progress bar by a specified increment and redraws the bar to reflect the new position.</span></span> <br/>                                                                                                                                 |
| [<span data-ttu-id="3c07e-115">**PBM \_ GETBARCOLOR**</span><span class="sxs-lookup"><span data-stu-id="3c07e-115">**PBM\_GETBARCOLOR**</span></span>](pbm-getbarcolor.md) | <span data-ttu-id="3c07e-116">取得進度列的色彩。</span><span class="sxs-lookup"><span data-stu-id="3c07e-116">Gets the color of the progress bar.</span></span><br/>                                                                                                                                                                                                                        |
| [<span data-ttu-id="3c07e-117">**PBM \_ GETBKCOLOR**</span><span class="sxs-lookup"><span data-stu-id="3c07e-117">**PBM\_GETBKCOLOR**</span></span>](pbm-getbkcolor.md)   | <span data-ttu-id="3c07e-118">取得進度列的背景色彩。</span><span class="sxs-lookup"><span data-stu-id="3c07e-118">Gets the background color of the progress bar.</span></span><br/>                                                                                                                                                                                                             |
| [<span data-ttu-id="3c07e-119">**PBM \_ GETPOS**</span><span class="sxs-lookup"><span data-stu-id="3c07e-119">**PBM\_GETPOS**</span></span>](pbm-getpos.md)           | <span data-ttu-id="3c07e-120">抓取進度列的目前位置。</span><span class="sxs-lookup"><span data-stu-id="3c07e-120">Retrieves the current position of the progress bar.</span></span> <br/>                                                                                                                                                                                                       |
| [<span data-ttu-id="3c07e-121">**PBM \_ GETRANGE**</span><span class="sxs-lookup"><span data-stu-id="3c07e-121">**PBM\_GETRANGE**</span></span>](pbm-getrange.md)       | <span data-ttu-id="3c07e-122">抓取指定進度列控制項目前最高和最低限制的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3c07e-122">Retrieves information about the current high and low limits of a given progress bar control.</span></span> <br/>                                                                                                                                                              |
| [<span data-ttu-id="3c07e-123">**PBM \_ >GETSTATE**</span><span class="sxs-lookup"><span data-stu-id="3c07e-123">**PBM\_GETSTATE**</span></span>](pbm-getstate.md)       | <span data-ttu-id="3c07e-124">取得進度列的狀態。</span><span class="sxs-lookup"><span data-stu-id="3c07e-124">Gets the state of the progress bar.</span></span><br/>                                                                                                                                                                                                                        |
| [<span data-ttu-id="3c07e-125">**PBM \_ GETSTEP**</span><span class="sxs-lookup"><span data-stu-id="3c07e-125">**PBM\_GETSTEP**</span></span>](pbm-getstep.md)         | <span data-ttu-id="3c07e-126">捕獲進度列的步驟增量。</span><span class="sxs-lookup"><span data-stu-id="3c07e-126">Retrieves the step increment for a progress bar.</span></span> <span data-ttu-id="3c07e-127">步驟遞增是進度列在收到 [**PBM \_ STEPIT**](pbm-stepit.md) 訊息時，增加其目前位置的數量。</span><span class="sxs-lookup"><span data-stu-id="3c07e-127">The step increment is the amount by which the progress bar increases its current position whenever it receives a [**PBM\_STEPIT**](pbm-stepit.md) message.</span></span><br/>                                               |
| [<span data-ttu-id="3c07e-128">**PBM \_ SETBARCOLOR**</span><span class="sxs-lookup"><span data-stu-id="3c07e-128">**PBM\_SETBARCOLOR**</span></span>](pbm-setbarcolor.md) | <span data-ttu-id="3c07e-129">在進度列控制項中設定進度指標列的色彩。</span><span class="sxs-lookup"><span data-stu-id="3c07e-129">Sets the color of the progress indicator bar in the progress bar control.</span></span> <br/>                                                                                                                                                                                 |
| [<span data-ttu-id="3c07e-130">**PBM \_ SETBKCOLOR**</span><span class="sxs-lookup"><span data-stu-id="3c07e-130">**PBM\_SETBKCOLOR**</span></span>](pbm-setbkcolor.md)   | <span data-ttu-id="3c07e-131">設定進度列中的背景色彩。</span><span class="sxs-lookup"><span data-stu-id="3c07e-131">Sets the background color in the progress bar.</span></span> <br/>                                                                                                                                                                                                            |
| [<span data-ttu-id="3c07e-132">**PBM \_ SETMARQUEE**</span><span class="sxs-lookup"><span data-stu-id="3c07e-132">**PBM\_SETMARQUEE**</span></span>](pbm-setmarquee.md)   | <span data-ttu-id="3c07e-133">設定捲軸模式的進度列。</span><span class="sxs-lookup"><span data-stu-id="3c07e-133">Sets the progress bar to marquee mode.</span></span> <span data-ttu-id="3c07e-134">這會使進度列像字幕一樣移動。</span><span class="sxs-lookup"><span data-stu-id="3c07e-134">This causes the progress bar to move like a marquee.</span></span><br/>                                                                                                                                                                |
| [<span data-ttu-id="3c07e-135">**PBM \_ SETPOS**</span><span class="sxs-lookup"><span data-stu-id="3c07e-135">**PBM\_SETPOS**</span></span>](pbm-setpos.md)           | <span data-ttu-id="3c07e-136">設定進度列的目前位置，並重新繪製橫條以反映新的位置。</span><span class="sxs-lookup"><span data-stu-id="3c07e-136">Sets the current position for a progress bar and redraws the bar to reflect the new position.</span></span> <br/>                                                                                                                                                             |
| [<span data-ttu-id="3c07e-137">**PBM \_ SETRANGE**</span><span class="sxs-lookup"><span data-stu-id="3c07e-137">**PBM\_SETRANGE**</span></span>](pbm-setrange.md)       | <span data-ttu-id="3c07e-138">設定進度列的最小值和最大值，並重新繪製橫條以反映新的範圍。</span><span class="sxs-lookup"><span data-stu-id="3c07e-138">Sets the minimum and maximum values for a progress bar and redraws the bar to reflect the new range.</span></span><br/>                                                                                                                                                       |
| [<span data-ttu-id="3c07e-139">**PBM \_ SETRANGE32**</span><span class="sxs-lookup"><span data-stu-id="3c07e-139">**PBM\_SETRANGE32**</span></span>](pbm-setrange32.md)   | <span data-ttu-id="3c07e-140">將進度列控制項的範圍設定為32位值。</span><span class="sxs-lookup"><span data-stu-id="3c07e-140">Sets the range of a progress bar control to a 32-bit value.</span></span> <br/>                                                                                                                                                                                               |
| [<span data-ttu-id="3c07e-141">**PBM \_ SETSTATE**</span><span class="sxs-lookup"><span data-stu-id="3c07e-141">**PBM\_SETSTATE**</span></span>](pbm-setstate.md)       | <span data-ttu-id="3c07e-142">設定進度列的狀態。</span><span class="sxs-lookup"><span data-stu-id="3c07e-142">Sets the state of the progress bar.</span></span><br/>                                                                                                                                                                                                                        |
| [<span data-ttu-id="3c07e-143">**PBM \_ SETSTEP**</span><span class="sxs-lookup"><span data-stu-id="3c07e-143">**PBM\_SETSTEP**</span></span>](pbm-setstep.md)         | <span data-ttu-id="3c07e-144">指定進度列的步驟增量。</span><span class="sxs-lookup"><span data-stu-id="3c07e-144">Specifies the step increment for a progress bar.</span></span> <span data-ttu-id="3c07e-145">步驟遞增是進度列在收到 [**PBM \_ STEPIT**](pbm-stepit.md) 訊息時，增加其目前位置的數量。</span><span class="sxs-lookup"><span data-stu-id="3c07e-145">The step increment is the amount by which the progress bar increases its current position whenever it receives a [**PBM\_STEPIT**](pbm-stepit.md) message.</span></span> <span data-ttu-id="3c07e-146">依預設，步驟遞增會設定為10。</span><span class="sxs-lookup"><span data-stu-id="3c07e-146">By default, the step increment is set to 10.</span></span> <br/> |
| [<span data-ttu-id="3c07e-147">**PBM \_ STEPIT**</span><span class="sxs-lookup"><span data-stu-id="3c07e-147">**PBM\_STEPIT**</span></span>](pbm-stepit.md)           | <span data-ttu-id="3c07e-148">將進度列的目前位置往前移，並重新繪製橫條以反映新的位置。</span><span class="sxs-lookup"><span data-stu-id="3c07e-148">Advances the current position for a progress bar by the step increment and redraws the bar to reflect the new position.</span></span> <span data-ttu-id="3c07e-149">應用程式會藉由傳送 [**PBM \_ SETSTEP**](pbm-setstep.md) 訊息來設定步驟增量。</span><span class="sxs-lookup"><span data-stu-id="3c07e-149">An application sets the step increment by sending the [**PBM\_SETSTEP**](pbm-setstep.md) message.</span></span> <br/>                                |



 

### <a name="structures"></a><span data-ttu-id="3c07e-150">結構</span><span class="sxs-lookup"><span data-stu-id="3c07e-150">Structures</span></span>



| <span data-ttu-id="3c07e-151">主題</span><span class="sxs-lookup"><span data-stu-id="3c07e-151">Topic</span></span>                      | <span data-ttu-id="3c07e-152">目錄</span><span class="sxs-lookup"><span data-stu-id="3c07e-152">Contents</span></span>                                                                                                                                                                 |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3c07e-153">**PBRANGE**</span><span class="sxs-lookup"><span data-stu-id="3c07e-153">**PBRANGE**</span></span>](/windows/desktop/api/Commctrl/ns-commctrl-pbrange) | <span data-ttu-id="3c07e-154">包含進度列控制項的最高和最低限制的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3c07e-154">Contains information about the high and low limits of a progress bar control.</span></span> <span data-ttu-id="3c07e-155">此結構會與 [**PBM \_ GETRANGE**](pbm-getrange.md) 訊息搭配使用。</span><span class="sxs-lookup"><span data-stu-id="3c07e-155">This structure is used with the [**PBM\_GETRANGE**](pbm-getrange.md) message.</span></span> <br/> |



 

### <a name="constants"></a><span data-ttu-id="3c07e-156">常數</span><span class="sxs-lookup"><span data-stu-id="3c07e-156">Constants</span></span>



| <span data-ttu-id="3c07e-157">主題</span><span class="sxs-lookup"><span data-stu-id="3c07e-157">Topic</span></span>                                                          | <span data-ttu-id="3c07e-158">目錄</span><span class="sxs-lookup"><span data-stu-id="3c07e-158">Contents</span></span>                                                                            |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="3c07e-159">進度列控制項樣式</span><span class="sxs-lookup"><span data-stu-id="3c07e-159">Progress Bar Control Styles</span></span>](progress-bar-control-styles.md) | <span data-ttu-id="3c07e-160">**進度** 列控制項支援下列控制項樣式：</span><span class="sxs-lookup"><span data-stu-id="3c07e-160">The following control styles are supported by **Progress Bar** controls:</span></span><br/> |



 

 

 





