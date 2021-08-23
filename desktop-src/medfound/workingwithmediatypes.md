---
description: 使用 DMO 媒體類型
ms.assetid: 1aaf7554-1a5f-439a-afb1-a031607e1a1e
title: 使用 DMO 媒體類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48a75d7eb65e92a89d5d413d8cc04a7dbb9f1891d6b23a9cc3c1242fbae46f1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119100913"
---
# <a name="working-with-dmo-media-types"></a>使用 DMO 媒體類型

編解碼器 DMOs 所使用的輸入和輸出媒體類型是使用 [**DMO \_ 媒體 \_ 類型**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type)結構來定義。 此結構等同于 Windows 媒體格式 SDK 中定義的 [**WM \_ 媒體 \_ 類型**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type)，以及在 Microsoft DirectShow®中定義的 [**\_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type)。 視您的應用程式而定，您可以使用定義為這三種類型之一的變數。 將指標轉換成另一個媒體類型結構的指標是安全的。 例如：


```
    DMO_MEDIA_TYPE MediaType;
    WM_MEDIA_TYPE* pMedia = NULL;
    pMedia = (WM_MEDIA_TYPE*)&MediaType;
```



編解碼器所使用的格式類型通常會限制為 **VIDEOINFOHEADER** 和 **WAVEFORMATEX** 結構所描述的格式類型。 為了方便起見，這些格式類型的常數會包含在 wmcodecconst 標頭檔中。 常數名稱分別為 WMCFORMAT \_ VideoInfo 和 WMCFORMAT \_ WaveFormatEx。 音訊編解碼器在某些情況下可以使用 **WAVEFORMATEXTENSIBLE** 結構，而且必須在其他環境中使用。 不過， **DMO 的 \_ 媒體 \_ 類型。 formattype** 會設定為與 **WAVEFORMATEX** 相同的值。 如需使用 **WAVEFORMATEXTENSIBLE** 的詳細資訊，請參閱 [使用 High-Definition 音訊](usinghighdefinitionaudio.md)。

> [!Note]  
>    您必須在用來儲存壓縮資料的任何容器中包含用來當做編碼器輸出的格式類型結構。 這些解碼器需要原始格式結構才能將內容解壓縮。 除了結構的成員之外，壓縮的 Windows Media 音訊和影片類型還需要額外的格式資訊，這些資訊會附加至結構。 如需詳細資訊，請參閱使用 [音訊](workingwithaudio.md) 和使用 [影片](workingwithvideo.md)。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用編解碼器 DMOs](workingwithcodecdmos.md)
</dt> </dl>

 

 
