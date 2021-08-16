---
description: 音訊捕捉和呈現介面
ms.assetid: 79b42ffd-703a-4a7c-bb2d-5cfc2fbeb16c
title: 音訊捕捉和呈現介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3ffdf586ec8566abddadcb0b7109680664963a63071472a3ac7aa895981e643
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117824248"
---
# <a name="audio-capture-and-rendering-interfaces"></a>音訊捕捉和呈現介面

這些介面支援音訊捕獲和轉譯 DirectShow



| 介面                                              | 描述                                                                                                                                               |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer)       | 存取系統音效卡上的類比輸入，並調整特性，例如 mono 或身歷聲、混合層級、平移層級、音量、高音和低音。 |
| [**IAMAudioRendererStats**](/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats) | 取得有關音訊轉譯的統計效能資訊。                                                                                          |
| [**IAMBufferNegotiation**](/windows/desktop/api/Strmif/nn-strmif-iambuffernegotiation)   | 控制音訊捕獲篩選器如何配置緩衝區。                                                                                                   |
| [**IAMClockSlave**](/windows/desktop/api/Strmif/nn-strmif-iamclockslave)                 | 當音訊轉譯器符合其他時鐘的速率時，控制其容錯。                                                                      |
| [**IAMDirectSound**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound)               | 讓應用程式指定哪個視窗擁有控制 DirectSound 音訊播放的焦點。                                                      |
| [**IAMResourceControl**](/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol)       | 在需要時保存音訊裝置資源。                                                                                                        |
| [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig)             | 查詢並設定捕獲篩選器的輸出格式。                                                                                                         |
| [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio)                     | 設定音訊輸出音量和餘額。                                                                                                                      |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[介面](interfaces.md)
</dt> </dl>

 

 



