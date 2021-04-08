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
# <a name="erasing-by-using-the-inkoverlay-object"></a>使用 InkOverlay 物件進行清除

[**InkOverlay**](inkoverlay-class.md)物件可以附加至視窗控制項，用來啟用基本筆跡功能。 您可以透過將 [**system.windows.controls.inkcanvas.editingmode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode)屬性設定為 [**刪除**]，來使用 **InkOverlay** 物件來清除筆墨。 然後，您可以將 [**EraserMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode)屬性設定為 [**InkOverlayEraserMode**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayerasermode)的 **筆劃** 或 **點** 成員。 將 [ **EraserMode** ] 屬性設定為 [ **筆觸** ] 會清除整個筆劃。 將 **EraserMode** 屬性設定為 **Point** 會清除游標所傳遞的筆墨。

 

 



