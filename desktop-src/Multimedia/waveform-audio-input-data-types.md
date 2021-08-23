---
title: Waveform-Audio 輸入資料類型
description: Waveform-Audio 輸入資料類型
ms.assetid: dfedcb93-edfb-4a25-8445-95d4aee55734
keywords:
- 波形音訊、輸入資料類型
- 波形-音訊介面、輸入資料類型
- 錄製波形音訊、輸入資料類型
- HWAVEIN 控制碼
- WAVEFORMATEX 結構
- WAVEHDR 結構
- WAVEINCAPS 結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e131e55c404fe658a0c8f60a8f816ff231f9eb9492bcf8641a4e38781bfa78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119892088"
---
# <a name="waveform-audio-input-data-types"></a>Waveform-Audio 輸入資料類型

下列資料類型是針對波形-音訊輸入函式所定義。



| 類型                                 | 描述                                                                                                                                                     |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **HWAVEIN**                          | 開啟波形音訊輸入裝置的控制碼。                                                                                                                  |
| [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) | 結構，指定特定波形音訊輸入裝置所支援的資料格式。 此結構也可用於波形音訊輸出裝置。 |
| [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr)           | 結構，用來做為波形音訊輸入資料區塊的標頭。 此結構也可用於波形音訊輸出裝置。                             |
| [**WAVEINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps)     | 用來查詢特定波形音訊輸入裝置功能的結構。                                                                   |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[錄製波形音訊](recording-waveform-audio.md)
</dt> </dl>

 

 