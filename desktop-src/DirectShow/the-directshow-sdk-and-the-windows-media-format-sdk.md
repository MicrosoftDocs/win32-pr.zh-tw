---
description: DirectShow SDK 和 Windows 媒體格式 SDK
ms.assetid: d9ac89cc-0d55-4c51-ae0a-592422d97383
title: DirectShow SDK 和 Windows 媒體格式 SDK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 993f7ea0c9ac47861547cc08662fcb7916c3587c566445960505fe05a5c3d37a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118651755"
---
# <a name="the-directshow-sdk-and-the-windows-media-format-sdk"></a>DirectShow SDK 和 Windows 媒體格式 SDK

DirectShow 和 Windows 媒體格式 SDK 提供互補的解決方案，以撰寫可建立及播放 Windows 媒體格式資料流程的應用程式。 如需詳細資訊，請參閱 MSDN Library 的「[音訊和影片](../audio-and-video.md)」一節。

ASF 寫入器篩選器會接受任意數量的輸入資料流程，並建立一個 ASF 檔。 此篩選器會使用 Windows 媒體格式 SDK，將未壓縮的音訊或影片檔案轉換成 Windows 媒體內容。 然後，壓縮的內容會以 ASF 容器格式儲存。 如果內容只是音訊，則會將檔案指定為 .wma 副檔名，而且稱為 Windows Media 音訊檔案。 如果內容只是影片或影片和音訊，則會將檔案指定為 .wmv 副檔名，並將其稱為 Windows Media 視訊檔案。 這兩種檔案類型也可以包含中繼資料。

您可以在各種案例中使用 WM ASF 寫入器，包括數位視訊 (DV) 捕捉、音訊 recompression，以及 Audio-Video 交錯式 (AVI) 或 MPEG 多媒體檔案的轉換，以進行網路串流處理。 此篩選器提供的唯一方法，是在) Windows Media 視訊中建立 Microsoft® Windows 媒體™音訊 (WMA (和) WMV DirectShow 檔案。 篩選也可以建立受數位 Rights Management (DRM) 保護的檔案，也可以使用 Microsoft MPEG-2 編碼器建立 MPEG 4 內容。 此內容會儲存為 ASF 容器格式。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[在 DirectShow 中建立 ASF 檔案](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 
