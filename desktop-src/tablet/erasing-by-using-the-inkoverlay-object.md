---
description: InkOverlay 物件可以附加至視窗控制項，用來啟用基本筆跡功能。
ms.assetid: c15d80dc-0cbf-48a2-9f5d-d94d521b1a8c
title: 使用 InkOverlay 物件進行清除
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cf85926f3566340cbde0d3202f3485e7c54cccf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690635"
---
# <a name="erasing-by-using-the-inkoverlay-object"></a><span data-ttu-id="0b626-103">使用 InkOverlay 物件進行清除</span><span class="sxs-lookup"><span data-stu-id="0b626-103">Erasing by Using the InkOverlay Object</span></span>

<span data-ttu-id="0b626-104">[**InkOverlay**](inkoverlay-class.md)物件可以附加至視窗控制項，用來啟用基本筆跡功能。</span><span class="sxs-lookup"><span data-stu-id="0b626-104">The [**InkOverlay**](inkoverlay-class.md) object can be attached to a window control and is used to enable basic ink capability.</span></span> <span data-ttu-id="0b626-105">您可以透過將 [**system.windows.controls.inkcanvas.editingmode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode)屬性設定為 [**刪除**]，來使用 **InkOverlay** 物件來清除筆墨。</span><span class="sxs-lookup"><span data-stu-id="0b626-105">You can use the **InkOverlay** object to erase ink by setting the [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode) property equal to **Delete**.</span></span> <span data-ttu-id="0b626-106">然後，您可以將 [**EraserMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode)屬性設定為 [**InkOverlayEraserMode**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayerasermode)的 **筆劃** 或 **點** 成員。</span><span class="sxs-lookup"><span data-stu-id="0b626-106">You can then set the [**EraserMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode) property to either the **Stroke** or **Point** members of [**InkOverlayEraserMode**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayerasermode).</span></span> <span data-ttu-id="0b626-107">將 [ **EraserMode** ] 屬性設定為 [ **筆觸** ] 會清除整個筆劃。</span><span class="sxs-lookup"><span data-stu-id="0b626-107">Setting the **EraserMode** property to **Stroke** erases entire strokes.</span></span> <span data-ttu-id="0b626-108">將 **EraserMode** 屬性設定為 **Point** 會清除游標所傳遞的筆墨。</span><span class="sxs-lookup"><span data-stu-id="0b626-108">Setting the **EraserMode** property to **Point** erases the ink that the cursor passes over.</span></span>

 

 



