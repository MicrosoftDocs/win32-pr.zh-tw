---
description: 檔案捕捉中的影片埠 Pin
ms.assetid: 0fa6d88e-3c64-487f-b007-8c65bf47211d
title: 檔案捕捉中的影片埠 Pin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cab348c7e378f4130b43eef45f2cf4ddd079b0e85a77397b767cadddde5a7d0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049378"
---
# <a name="video-port-pins-in-file-capture"></a>檔案捕捉中的影片埠 Pin

如果捕捉裝置有影片埠，則即使您只想要捕捉至檔案，影片埠 pin 也必須連接到影片轉譯器。

如果您使用值 **釘選 \_ 類別 \_ 捕獲** 來呼叫 [**ICaptureGraphBuilder2：： RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) ，且裝置有影片埠 pin，則 CAPTURE Graph Builder 會自動將視訊連接埠 pin 連接到重迭 [Mixer](overlay-mixer-filter.md)篩選，並將重迭 Mixer 連接到影片轉譯器。 「Capture Graph 產生器」會藉由呼叫 [**IVideoWindow：:p 出現 \_**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow)值 **OAFALSE** 來隱藏影片視窗。 如果應用程式稍後以釘選 **\_ 類別 \_ 預覽** 來呼叫 **RenderStream** ，Capture Graph Builder **呼叫 \_ 會以值** **OATRUE** 顯示，以便顯示影片視窗。

使用 **PIN \_ 類別 \_ 捕獲** 來呼叫 **RenderStream** 之後，您可以藉由查詢 [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow)介面的篩選 Graph 管理員，檢查它是否已新增影片轉譯器。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[將影片捕獲至檔案](capturing-video-to-a-file.md)
</dt> </dl>

 

 



