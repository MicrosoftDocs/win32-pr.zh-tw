---
description: 多媒體串流介面
ms.assetid: 53d639e2-8717-4552-b0d3-b8c500bd38a8
title: 多媒體串流介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b38200d98b0f01b7260508cbf7bd19c6e65efdfb3af78f2efff77be38294e8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118152954"
---
# <a name="multimedia-streaming-interfaces"></a>多媒體串流介面

> [!Note]  
> 這些 Api 已被取代。 應用程式應該使用 [**範例捕獲**](sample-grabber-filter.md)篩選器或執行自訂篩選，以從 DirectShow 的篩選圖形取得資料。

 

本節包含所有多媒體串流介面及其方法的參考專案，包括 Microsoft DirectShow 支援的專案。



| 介面                                                  | 描述                                                                                                                                             |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAMMediaStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediastream)                   | 在使用多媒體串流的應用程式中，處理 DirectShow 篩選和篩選圖形之間的內部連接。                            |
| [**IAMMediaTypeSample**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypesample)           | 包含使用任意媒體類型運算元據流範例的方法。                                                                            |
| [**IAMMediaTypeStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypestream)           | 包含用來建立具有任意媒體類型之多媒體資料流程的方法。                                                                            |
| [**IAMMultiMediaStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream)         | 公開多媒體串流開發人員的 DirectShow 功能。                                                                                       |
| [**IAudioData**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata)                           | 提供可讓應用程式設定和取得音訊串流將會參考之基礎音訊資料的方法。                                   |
| [**IAudioMediaStream**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiomediastream)             | 提供可設定和取得資料流程格式的方法，以控制音訊媒體資料流程。                                                                 |
| [**IAudioStreamSample**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample)           | 從基礎 [**IAudioData**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata) 資料物件中抓取資訊。                                                                |
| [**IDirectDrawMediaStream**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream)   | 控制出現在 Microsoft® DirectDraw®表面上的媒體串流。                                                                                  |
| [**IDirectDrawStreamSample**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample) | 提供方法，這些方法可設定和取出與目前資料流程範例相關聯的 DirectDraw 介面指標。                                    |
| [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream)                       | 提供媒體資料流程特性的存取權，例如資料流程的媒體類型和目的識別碼。 它也有建立資料範例的方法。 |
| [**IMediaStreamFilter**](/previous-versions/windows/desktop/api/amstream/nn-amstream-imediastreamfilter)           | 媒體資料流程篩選器支援，由多媒體資料流程物件在內部使用。 .                                                       |
| [**IMemoryData**](/previous-versions/windows/desktop/api/austream/nn-austream-imemorydata)                         | 包含的方法可設定和取出音訊資料物件上的記憶體資料。                                                                               |
| [**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream)             | 提供控制多媒體資料流程的方法，並提供其基礎媒體資料流程的存取權。                                                   |
| [**IStreamSample**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample)                     | 提供資料流程範例行為的控制權。                                                                                                   |



 

 

 



