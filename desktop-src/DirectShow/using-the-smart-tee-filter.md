---
description: 使用智慧的 t a 濾波器
ms.assetid: d2828269-6841-41a8-8d45-f864c7e85857
title: 使用智慧的 t a 濾波器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5260469634c613fe05c25eb9f55e24e108e8c434
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997813"
---
# <a name="using-the-smart-tee-filter"></a>使用智慧的 t a 濾波器

如果「捕捉」篩選器有個別的「捕捉」和「預覽」 pin，您可以從另一個瀏覽器進行預覽。 但是，如果篩選沒有預覽 pin，您可以在圖形中包含 [智慧型](smart-tee-filter.md) 指標篩選來進行相同的動作。 此篩選器會將資料從 capture 釘選分割成兩個相同的資料流程，一個用於 capture，另一個用於預覽。 下圖說明此程序。

![具有智慧型 t i 濾波器的捕獲圖表](images/vidcap05.png)

[**ICaptureGraphBuilder2：： RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream)方法會自動插入智慧的 t a 篩選準則（如果需要的話）。 但是，如果您使用 **IGraphBuilder** 方法來建立您的圖形，而不是 **RenderStream**，您可能需要插入智慧的 t a 濾波器。

在捕獲篩選器上轉譯釘選之前，請檢查篩選準則是否有預覽 pin 或影片埠 pin。 如果不是，而且您想要預覽，請將智慧型指標篩選器新增至圖形，並將它連接到 capture 篩選器上的捕獲 pin。

> [!Note]  
> 您可以將影片埠 (VP) 釘選為一種預覽 pin，因此具有 VP 釘選的篩選器不需要 Smart t 濾波器。 不過，VP 釘有一些其他特殊需求。 如需詳細資訊，請參閱 [影片埠 pin](video-port-pins.md)。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Advanced Capture 主題](advanced-capture-topics.md)
</dt> <dt>

[結合影片捕獲和預覽](combining-video-capture-and-preview.md)
</dt> <dt>

[使用 Pin 類別](working-with-pin-categories.md)
</dt> </dl>

 

 



