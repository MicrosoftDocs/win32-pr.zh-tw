---
description: VideoInfo2 格式類型
ms.assetid: edd2013a-f0c5-4176-ba3a-a3af719ce31d
title: VideoInfo2 格式類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a820ea6a53c457d2d000be8b4c0e8966213c1aeeb2b5f55a780c4801a4182907
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119071922"
---
# <a name="videoinfo2-format-type"></a>VideoInfo2 格式類型

預覽 pin 的慣用媒體類型可能是具有 [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) 格式的類型。 此格式結構支援特殊功能，例如交錯式影片和圖片外觀比例。

VMR-7 和 VMR-9 都支援直接 [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) 。 當您將 VMR 連接到該解碼器時，它們將會協商最佳的格式。 不過，較舊的影片轉譯器篩選器不支援 **VIDEOINFOHEADER2**。 若要使用 **VIDEOINFOHEADER2** 格式類型搭配影片轉譯器篩選器，您必須將覆迭 [Mixer](overlay-mixer-filter.md)篩選插入圖形中。

1.  使用 [**IPin：： EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) 方法，在解碼器篩選器的輸出釘選上列舉慣用的媒體類型。
2.  檢查列舉順序中的第一個媒體類型。
3.  如果格式類型為 **\_ VideoInfo2 格式**，請將輸出釘選到重迭 Mixer。 然後將重迭 Mixer 連接到影片轉譯器。  (查看 [影片埠釘](video-port-pins.md)選。 ) 

如果您不在意這些功能，就不需要使用覆迭 Mixer。 將 VIDEOINFOHEADER 直接連線至影片轉譯器，它會改以[](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)格式連接。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Advanced Capture 主題](advanced-capture-topics.md)
</dt> <dt>

[在影片捕獲中使用重迭 Mixer](using-the-overlay-mixer-in-video-capture.md)
</dt> </dl>

 

 



