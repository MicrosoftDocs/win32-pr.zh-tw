---
title: 變更音調和播放速率
description: 變更音調和播放速率
ms.assetid: f0f5249b-ae2a-4f17-80ee-575f9f7963a7
keywords:
- 波形音訊、音調
- 波形-音訊介面、音調
- 波形音訊，播放速率
- 波形-音訊介面，播放速率
- 波形音訊，變更音調
- 波形-音訊介面，變更音調
- 波形音訊，變更播放速率
- 波形-音訊介面，變更播放速率
- 變更波形-音訊播放速率
- 變更波形-音訊音調
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99eec4e29ec1c38cddb5a5f92f27643e2c9c3e6c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463148"
---
# <a name="changing-pitch-and-playback-rate"></a>變更音調和播放速率

某些波形音訊輸出裝置可能會改變波形音訊資料的音調和播放速率。 並非所有波形音訊裝置都支援音調和播放速率變更。 如需如何判斷特定波形音訊裝置是否支援音調和播放速率變更的相關資訊，請參閱 [裝置和資料類型](devices-and-data-types.md)。

變更音調和播放速率之間的差異如下：

-   變更播放速率是由設備磁碟機所執行，不需要特製化硬體。 取樣率未變更，但驅動程式會略過或合成範例來進行插補。 例如，如果播放速率以二的因數變更，驅動程式會略過每個其他範例。
-   變更推銷需要特製化硬體。 播放速率和取樣率不會變更。

Windows 提供下列功能來查詢及設定波形-音訊音調和播放速率。



| 函式                                                 | 描述                                                                 |
|----------------------------------------------------------|-----------------------------------------------------------------------------|
| [**waveOutGetPitch**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetpitch)               | 抓取指定波形音訊輸出裝置的間距。         |
| [**waveOutGetPlaybackRate**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetplaybackrate) | 抓取指定波形音訊輸出裝置的播放速率。 |
| [**waveOutSetPitch**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetpitch)               | 設定指定之波形音訊輸出裝置的間距。              |
| [**waveOutSetPlaybackRate**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetplaybackrate) | 設定指定之波形音訊輸出裝置的播放速率。      |



 

音調和播放速率會以將固定點數位壓縮成雙字值指定的因素來變更。 上層16位會指定數位的整數部分;較低的16位會指定小數部分。 例如，值1.5 表示為0x00018000L。 值0.75 以0x0000C000L 表示。 值為 1.0 (0x00010000) 表示音調或播放速率未變更。

 

 