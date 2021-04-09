---
title: Waveform-Audio 錯誤
description: Waveform-Audio 錯誤
ms.assetid: c898552a-a60a-4deb-ab4a-ed74b08a7d05
keywords:
- MCIERR 傳回值、波形-音訊錯誤
- 多媒體參考、波形-音訊錯誤
- 多媒體的參考，波形-音訊錯誤
- 媒體控制介面 (MCI) 、波形-音訊錯誤
- MCI (媒體控制介面) 、波形-音訊錯誤
- MCI 的參考、波形-音訊錯誤
- MCI 參考、波形-音訊錯誤
- 媒體控制介面 (MCI) ，錯誤
- MCI (媒體控制介面) ，錯誤
- MCI 的參考，錯誤
- MCI 參考，錯誤
- 波形-音訊錯誤
- MCI 波形-音訊錯誤
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faf64e8cd4ec6d061422bcf14d17dfb4c4317ee4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021043"
---
# <a name="waveform-audio-errors"></a>Waveform-Audio 錯誤

下列額外的傳回值是針對 MCI 波形-音訊裝置所定義：



| 值                             | 意義                                                                                                                                                             |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MCIERR \_ WAVE \_ INPUTSINUSE         | 可以用目前格式記錄檔案的所有波形裝置都在使用中。 等到其中一個裝置是免費的，然後再試一次。                              |
| MCIERR \_ WAVE \_ INPUTSUNSUITABLE    | 沒有任何已安裝的波形裝置可以記錄目前格式的檔案。 使用主控台的 [驅動程式] 選項來安裝適當的波形錄製裝置。 |
| MCIERR \_ WAVE \_ INPUTUNSPECIFIED    | 您可以指定任何相容的波形錄製裝置。                                                                                                           |
| MCIERR \_ WAVE \_ OUTPUTSINUSE        | 所有可播放目前格式之檔案的波形裝置皆為使用中。 等到其中一個裝置是免費的，然後再試一次。                                |
| MCIERR \_ WAVE \_ OUTPUTSUNSUITABLE   | 沒有任何已安裝的波形裝置可以播放目前格式的檔案。 使用主控台的 [驅動程式] 選項來安裝適當的波形裝置。             |
| MCIERR \_ WAVE \_ OUTPUTUNSPECIFIED   | 您可以指定任何相容的波形播放裝置。                                                                                                            |
| MCIERR \_ WAVE \_ SETINPUTINUSE       | 目前的波形裝置正在使用中。 等待裝置免費;然後，再試一次設定裝置以進行錄製。                                              |
| MCIERR \_ WAVE \_ SETINPUTUNSUITABLE  | 您用來錄製波形的裝置無法辨識資料格式。                                                                                     |
| MCIERR \_ WAVE \_ SETOUTPUTINUSE      | 目前的波形裝置正在使用中。 等待裝置免費;然後，再試一次設定裝置以進行播放。                                               |
| MCIERR \_ WAVE \_ SETOUTPUTUNSUITABLE | 您用來播放波形的裝置無法辨識資料格式。                                                                                   |



 

 

 




