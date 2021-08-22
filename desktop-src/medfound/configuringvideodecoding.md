---
description: 設定影片解碼
ms.assetid: 897b8e2d-9827-428d-91ae-632038c4c8c0
title: '設定影片解碼 (Microsoft 媒體基礎) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e7c49d42b47b4b6745731287e2b0bf0ee2d21c1eb503ed561274a5fb4cc8b15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035336"
---
# <a name="configuring-video-decoding-microsoft-media-foundation"></a>設定影片解碼 (Microsoft 媒體基礎) 

解碼基本上與編碼方式相反，因為設定方面。 此解碼器支援極少的屬性，而且不需要它們。 將輸入類型設定為用於解碼器輸出的類型 (包括編解碼器私用資料) 。 然後，將輸出設定為所需的未壓縮格式、設定 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) 結構以反映適當的框架大小，以及開始處理範例。

您必須提供具有媒體類型的解碼器，其中包含緊接在 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) 結構後面的編解碼器私用資料。 如果沒有此資料，則無法將內容解碼。 此解碼器所執行的格式驗證不會驗證私用資料。 如果編解碼器私用資料遺失或不正確，則編碼器會以位資料流程損毀的方式回應。 如需詳細資訊，請參閱 [使用影片編解碼器私用資料](usingvideocodecprivatedata.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用影片編解碼器私用資料](usingvideocodecprivatedata.md)
</dt> <dt>

[使用影片](workingwithvideo.md)
</dt> </dl>

 

 
