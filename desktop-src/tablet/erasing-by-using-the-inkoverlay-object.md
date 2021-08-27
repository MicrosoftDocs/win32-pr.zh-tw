---
description: InkOverlay 物件可以附加至視窗控制項，用來啟用基本筆跡功能。
ms.assetid: c15d80dc-0cbf-48a2-9f5d-d94d521b1a8c
title: 使用 InkOverlay 物件進行清除
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb6d95e7939bc53c534d3bfc9a542e40b95fbce05234000e24b107f0f2625eae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110938"
---
# <a name="erasing-by-using-the-inkoverlay-object"></a>使用 InkOverlay 物件進行清除

[**InkOverlay**](inkoverlay-class.md)物件可以附加至視窗控制項，用來啟用基本筆跡功能。 您可以透過將 [**system.windows.controls.inkcanvas.editingmode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode)屬性設定為 [**刪除**]，來使用 **InkOverlay** 物件來清除筆墨。 然後，您可以將 [**EraserMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode)屬性設定為 [**InkOverlayEraserMode**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayerasermode)的 **筆劃** 或 **點** 成員。 將 [ **EraserMode** ] 屬性設定為 [ **筆觸** ] 會清除整個筆劃。 將 **EraserMode** 屬性設定為 **Point** 會清除游標所傳遞的筆墨。

 

 



