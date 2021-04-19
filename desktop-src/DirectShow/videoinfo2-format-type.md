---
description: VideoInfo2 格式類型
ms.assetid: edd2013a-f0c5-4176-ba3a-a3af719ce31d
title: VideoInfo2 格式類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74b0f435e0e2a1b5b1d948c42a881f19300a9c6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980731"
---
# <a name="videoinfo2-format-type"></a>VideoInfo2 格式類型

預覽 pin 的慣用媒體類型可能是具有 [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) 格式的類型。 此格式結構支援特殊功能，例如交錯式影片和圖片外觀比例。

VMR-7 和 VMR-9 都支援直接 [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) 。 當您將 VMR 連接到該解碼器時，它們將會協商最佳的格式。 不過，較舊的影片轉譯器篩選器不支援 **VIDEOINFOHEADER2**。 若要使用 **VIDEOINFOHEADER2** 格式類型搭配影片轉譯器篩選器，您必須將覆迭 [混音](overlay-mixer-filter.md) 器篩選插入圖形中。

1.  使用 [**IPin：： EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) 方法，在解碼器篩選器的輸出釘選上列舉慣用的媒體類型。
2.  檢查列舉順序中的第一個媒體類型。
3.  如果格式類型為 **\_ VideoInfo2 格式**，請將輸出釘選到重迭混音器。 然後將重迭混音器連線到影片轉譯器。  (查看 [影片埠釘](video-port-pins.md)選。 ) 

如果您不在意這些功能，就不需要使用重迭混音器。 將解碼器直接連接到影片轉譯器，它會改以 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) 格式連接。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Advanced Capture 主題](advanced-capture-topics.md)
</dt> <dt>

[使用影片捕獲中的重迭混音器](using-the-overlay-mixer-in-video-capture.md)
</dt> </dl>

 

 



