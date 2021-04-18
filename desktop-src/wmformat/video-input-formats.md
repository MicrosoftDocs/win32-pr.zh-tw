---
title: 影片輸入格式
description: 影片輸入格式
ms.assetid: 0f1ec15d-328e-4c07-bf58-fd4ecb483549
keywords:
- Windows Media Format SDK、影片輸入格式
- Advanced Systems Format (ASF) 、影片輸入格式
- ASF (Advanced 系統格式) 、影片輸入格式
- 影片輸入格式
- Windows Media Format SDK、影片格式
- Advanced Systems Format (ASF) 、影片格式
- ASF (Advanced Systems Format) 、影片格式
- 影片格式
- Windows Media 視訊9編解碼器、影片輸入格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c5113ee3cbd9c9235104f858968db20ebc29e3a
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "106965224"
---
# <a name="video-input-formats"></a>影片輸入格式

寫入器接受下列影片格式，做為使用 Windows Media 視訊9編解碼器壓縮的輸入：

-   WMMEDIASUBTYPE \_ IYUV
-   WMMEDIASUBTYPE \_ I420
-   WMMEDIASUBTYPE \_ YV12
-   WMMEDIASUBTYPE \_ YUY2
-   WMMEDIASUBTYPE \_ UYVY
-   WMMEDIASUBTYPE \_ YVYU
-   WMMEDIASUBTYPE \_ YVU9
-   WMMEDIASUBTYPE \_ RGB32
-   WMMEDIASUBTYPE \_ RGB24
-   WMMEDIASUBTYPE \_ RGB565
-   WMMEDIASUBTYPE \_ RGB555
-   WMMEDIASUBTYPE \_ RGB8

您應該一律使用 [**IWMWriter：： GetInputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformatcount) 和 [**IWMWriter：： GetInputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformat) 來列舉可用的輸入格式，並取得所需格式的輸入媒體屬性物件。 您必須變更影片輸入媒體屬性物件，以反映輸入媒體的框架大小和畫面播放速率。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**媒體類型識別碼**](media-type-identifiers.md)
</dt> <dt>

[**媒體類型**](media-types.md)
</dt> </dl>

 

 




