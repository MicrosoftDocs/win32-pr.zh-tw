---
description: 多媒體串流物件和介面階層
ms.assetid: dbb6dc3b-b55e-4f6c-918f-068308e2dba9
title: 多媒體串流物件和介面階層
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52339644730139af22fd21fa2c24b8448a1afaf3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "103853495"
---
# <a name="multimedia-streaming-object-and-interface-hierarchy"></a>多媒體串流物件和介面階層

> [!Note]  
> 這些 Api 已被取代。 應用程式應該使用 [**範例捕獲**](sample-grabber-filter.md) 篩選器或執行自訂篩選，以從 DirectShow 篩選圖形取得資料。

 

下圖顯示多媒體串流中使用的物件階層。

![multimediastreaming 物件階層](images/mmstream02.png)

多媒體串流架構會定義三種一般類型的物件：

-   **AMMultimediaStream** 物件會公開 [**IAMMultiMediaStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream)介面。 就內部而言，此物件會包裝 DirectShow 篩選圖形。
-   *媒體資料流程* 物件會公開 [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) 介面，並且是特定資料。 AMMultimediaStream 物件包含一或多個媒體資料流程。
-   *Stream 範例* 物件包含特定資料流程的資料。

支援下列媒體資料流程物件：

-   音訊串流。 公開 [**IAudioMediaStream**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiomediastream) 介面。
-   DirectDraw 資料流程。 表示轉譯為 DirectDraw 表面的影片資料流程。 公開 [**IDirectDrawMediaStream**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream) 介面。
-   媒體類型資料流程。 代表任意資料。 公開 [**IAMMediaTypeStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypestream) 介面。

每個媒體資料流程物件都會建立自己的資料流程範例物件：

-   音訊串流會建立可公開 [**IAudioStreamSample**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample) 介面的音訊範例。
-   DirectDraw 資料流程會建立 DirectDraw 範例，以公開 [**IDirectDrawStreamSample**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample) 介面。
-   媒體類型資料流程會建立可公開 [**IAMMediaTypeSample**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypesample) 介面的媒體類型範例。

下圖顯示先前所列介面的介面階層：

![multimediastreaming 介面階層](images/mmstream01.png)

 

 



