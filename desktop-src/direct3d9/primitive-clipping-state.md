---
description: 部分位於 (或完全外部的原始物件) 視圖的截斷可以裁剪，如此就只會轉譯基本專案的可見部分。
ms.assetid: 096683a4-2d8f-49d3-b1a0-832150907f11
title: " (Direct3D 9) 的基本剪切狀態"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e5a305118d8db5c71e0e3cfa97132052777be68
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385837"
---
# <a name="primitive-clipping-state-direct3d-9"></a><span data-ttu-id="46d6b-103"> (Direct3D 9) 的基本剪切狀態</span><span class="sxs-lookup"><span data-stu-id="46d6b-103">Primitive Clipping State (Direct3D 9)</span></span>

<span data-ttu-id="46d6b-104">部分位於 (或完全外部的原始物件) [視圖](viewports-and-clipping.md) 的截斷可以裁剪，如此就只會轉譯基本專案的可見部分。</span><span class="sxs-lookup"><span data-stu-id="46d6b-104">Primitives that lie partially inside (or completely outside) the [view frustum](viewports-and-clipping.md) can be clipped so that only the visible portion of the primitive will be rendered.</span></span> <span data-ttu-id="46d6b-105">裁剪會減少只針對可見的基本或部分基本專案所完成的工作量。</span><span class="sxs-lookup"><span data-stu-id="46d6b-105">Clipping reduces the amount of work that is done to only those primitives or portions of a primitive that will be visible.</span></span>

<span data-ttu-id="46d6b-106">若要使用管線進行裁剪，請將 D3DRS \_ 剪切轉譯狀態設為 **TRUE** (預設值) 啟用剪切，或設定為 **FALSE** 以停用 Direct3D 剪切。</span><span class="sxs-lookup"><span data-stu-id="46d6b-106">To use the pipeline for clipping, set the D3DRS\_CLIPPING render state to **TRUE** (the default value) to enable clipping, or to **FALSE** to disable Direct3D clipping.</span></span>

## <a name="related-topics"></a><span data-ttu-id="46d6b-107">相關主題</span><span class="sxs-lookup"><span data-stu-id="46d6b-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46d6b-108">轉譯狀態</span><span class="sxs-lookup"><span data-stu-id="46d6b-108">Render States</span></span>](render-states.md)
</dt> </dl>

 

 



