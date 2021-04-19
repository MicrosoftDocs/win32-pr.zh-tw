---
description: 檔案捕捉中的影片埠 Pin
ms.assetid: 0fa6d88e-3c64-487f-b007-8c65bf47211d
title: 檔案捕捉中的影片埠 Pin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2361c5a7cdaa7640ece9724000963f39f3f77ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106996629"
---
# <a name="video-port-pins-in-file-capture"></a>檔案捕捉中的影片埠 Pin

如果捕捉裝置有影片埠，則即使您只想要捕捉至檔案，影片埠 pin 也必須連接到影片轉譯器。

如果您使用值 **釘選 \_ 類別 \_ 捕獲** 來呼叫 [**ICaptureGraphBuilder2：： RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) ，且裝置有影片埠 pin，則「捕獲圖形產生器」會自動將影片埠 pin 連接至重迭 [混音](overlay-mixer-filter.md)器篩選器，並將覆迭混音器連接至影片轉譯器。 「捕獲圖形產生器」會藉由呼叫 [**IVideoWindow：:p [ \_**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) **OAFALSE**] 來顯示值，以隱藏影片視窗。 如果應用程式稍後以釘選 **\_ 類別 \_ 預覽** 來呼叫 **RenderStream** ，「捕獲圖形產生器」會呼叫 **put \_ ，** 並顯示值 OATRUE，以便顯示影片視窗。

使用 **PIN \_ 類別 \_ 捕獲** 來呼叫 **RenderStream** 之後，您可以藉由查詢 [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow)介面的篩選圖形管理員來檢查它是否已新增影片轉譯器。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[將影片捕獲至檔案](capturing-video-to-a-file.md)
</dt> </dl>

 

 



