---
title: 變更 Waveform-Audio 播放的音量
description: 變更 Waveform-Audio 播放的音量
ms.assetid: 814daa35-7905-47a2-ab08-29f20493af1e
keywords:
- 波形音訊，變更播放音量
- 波形-音訊介面，變更播放音量
- 波形音訊，播放音量
- 波形-音訊介面、播放音量
- 變更波形-音訊播放音量
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e59bca6dbc168d2c327c46e4d934d4abb3afa73cc8ef2cae8b1a6c283bd92c81
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807988"
---
# <a name="changing-the-volume-of-waveform-audio-playback"></a>變更 Waveform-Audio 播放的音量

Windows 提供下列功能來查詢及設定波形音訊輸出裝置的音量層級。



| 函式                                     | 描述                                                                       |
|----------------------------------------------|-----------------------------------------------------------------------------------|
| [**waveOutGetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetvolume) | 抓取指定之波形音訊輸出裝置的目前磁片區層級。 |
| [**waveOutSetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetvolume) | 設定指定之波形音訊輸出裝置的音量層級。              |



 

並非所有波形音訊裝置都支援磁片區變更。 某些裝置支援左右通道上的個別音量控制。 如需如何判斷波形音訊裝置的音量控制功能的相關資訊，請參閱 [裝置和資料類型](devices-and-data-types.md)。

有些應用程式可讓使用者控制系統中所有音訊裝置的磁片區。  (此類型的許多應用程式都使用音訊混音器服務;如需詳細資訊，請參閱 [音訊 Mixers](audio-mixers.md)。 ) 除非您的應用程式能夠使用這種主要音量控制，否則您應該先開啟音訊裝置，再變更其磁片區。 您也應該在變更磁片區層級之前先進行查詢，並儘快將磁片區層級還原至先前的層級。

磁片區是以雙量值指定。 當音訊格式為身歷聲時，上層16位會指定右聲道的相對磁片區，而較低的16位則會指定左邊通道的相對音量。 對於不支援左和右聲道音量控制的裝置，較低的16位會指定磁片區層級，而會忽略前16位。

磁片區層級值的範圍是從 0x0 (無聲) 至 0xFFFF (最大磁片區) ，而且會 logarithmically。 將磁片區層級從0x5000 增加至0x6000 時，觀察到的磁片區增加是相同的，因為它是從0x4000 到0x5000。

 

 