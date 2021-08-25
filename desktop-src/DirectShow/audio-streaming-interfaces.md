---
description: 音訊串流介面
ms.assetid: eaf510ef-a6a3-45e0-8f0a-281a44b0ff6f
title: 音訊串流介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1087ab127258fcd4f587cdd029d4604c35524689b5f0877476e1137e2ed924eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119824468"
---
# <a name="audio-streaming-interfaces"></a>音訊串流介面

> [!Note]  
> 這些 Api 已被取代。 應用程式應該使用 [**範例捕獲**](sample-grabber-filter.md)篩選器或執行自訂篩選，以從 DirectShow 的篩選圖形取得資料。

 



| 介面                                        | 描述                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAudioMediaStream**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiomediastream)   | 控制音訊媒體資料流程。 這個介面繼承自 [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) 介面，用來建立一或多個 [**IAudioStreamSample**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample) 物件。 它也可用來設定和取出資料流程資料的目前格式。                                                                                                            |
| [**IAudioStreamSample**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample) | 從基礎 [**IAudioData**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata) 資料物件中抓取資訊。                                                                                                                                                                                                                                                                                                        |
| [**IMemoryData**](/previous-versions/windows/desktop/api/austream/nn-austream-imemorydata)               | 包含的方法可設定和取出音訊資料物件上的記憶體資料。 音訊資料物件提供資料流程範例存取的基礎資料。 這個介面提供一種方法來初始化記憶體緩衝區，並在物件中設定實際的音訊資料量。 此外， [**IMemoryData：： GetInfo**](/previous-versions/windows/desktop/api/austream/nf-austream-imemorydata-getinfo) 方法可以用來取出音訊記憶體資料。 |
| [**IAudioData**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata)                 | 提供可讓應用程式設定和取得音訊串流將會參考之基礎音訊資料的方法。 音訊資料格式設定于 [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) 結構中。                                                                                                                                                                                       |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[多媒體串流介面的清單](list-of-multimedia-streaming-interfaces.md)
</dt> </dl>

 

 
