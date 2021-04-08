---
title: 變更輔助 Audio-Devices 的數量
description: 變更輔助 Audio-Devices 的數量
ms.assetid: d7357900-132c-4758-8bc2-a890aead01c3
keywords:
- 波形音訊，變更輔助音訊裝置音量
- 變更輔助音訊裝置音量
- 輔助音訊，變更裝置音量
- 輔助音訊介面
- 輔助音訊裝置，變更音量
- 輔助音訊、介面
- 輔助音訊、裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f80c499f18b60f0919214c91eeec834ed72c3e1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103682362"
---
# <a name="changing-the-volume-of-auxiliary-audio-devices"></a>變更輔助 Audio-Devices 的數量

Windows 提供下列功能來查詢及設定輔助音訊裝置的磁片區。



| 函式                             | 描述                                                                    |
|--------------------------------------|--------------------------------------------------------------------------------|
| [**auxGetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetvolume) | 抓取指定之輔助輸出裝置的目前磁片區設定。 |
| [**auxSetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-auxsetvolume) | 設定指定之輔助輸出裝置的磁片區。                      |



 

並非所有輔助音訊裝置都支援磁片區變更。 某些裝置可支援左側和右側通道上的個別磁片區變更。

磁片區是以雙聲道值指定，如同波形-音訊和 MIDI 音量控制功能。 當音訊格式為身歷聲時，上層16位會指定右聲道的相對磁片區，而較低的16位則會指定左邊通道的相對音量。 對於不支援左和右聲道音量控制的裝置，較低的16位會指定磁片區層級，而會忽略前16位。

磁片區層級值的範圍是從 0x0 (無聲) 至 0xFFFF (最大磁片區) ，而且會 logarithmically。 將磁片區層級從0x5000 增加至0x6000 時，觀察到的磁片區增加是相同的，因為它是從0x4000 到0x5000。

 

 