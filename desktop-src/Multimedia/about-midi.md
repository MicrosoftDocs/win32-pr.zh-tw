---
title: 關於 MIDI
description: 關於 MIDI
ms.assetid: 32030c98-e513-4ee3-bbd0-ba41fceadd57
keywords:
- 'Windows 多媒體、音樂檢測數位介面 (MIDI) '
- '多媒體、音樂檢測數位介面 (MIDI) '
- '多媒體音訊、音樂檢測數位介面 (MIDI) '
- '音訊、音樂檢測數位介面 (MIDI) '
- 音樂檢測數位介面 (MIDI) ，關於
- MIDI (的音樂檢測數位介面) ，關於
- '音樂檢測數位介面 (MIDI) 、媒體控制介面 (MCI) '
- 'MIDI (的音樂檢測數位介面) 、媒體控制介面 (MCI) '
- 音樂檢測數位介面 (MIDI) 、串流緩衝區
- MIDI (音樂檢測數位介面) 、串流緩衝區
- 音樂檢測數位介面 (MIDI) 、MIDI 服務
- MIDI (的音樂檢測數位介面) 、MIDI 服務
- '媒體控制介面 (MCI) 、音樂檢測數位介面 (MIDI) '
- 'MCI (媒體控制介面) 、音樂檢測數位介面 (MIDI) '
- 串流緩衝區，關於
- MIDI 服務，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43c476807f750f9e90788377588f6c9af96561aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672151"
---
# <a name="about-midi"></a>關於 MIDI

Microsoft Win32 應用程式開發介面 (API) 提供下列方法讓應用程式使用 MIDI 資料：

-    (MCI) 的媒體控制介面。 雖然播放 MIDI 檔案最簡單的方式是使用 MCIWnd 視窗類別，您也可以使用 MCI 命令來建立 MIDI 裝置的自訂介面。 如需 MCIWnd 視窗類別的詳細資訊，請參閱 [MCIWnd 視窗類別](mciwnd-window-class.md)。 如需 MCI 的詳細 [資訊，請參閱 mci](mci.md)或 [Media CONTROL Interface (mci) ](media-control-interface--mci.md)。
-   [資料流程緩衝區](stream-buffers.md)。 此格式可讓應用程式操作時間戳記之 MIDI 資料的緩衝區以進行播放。 串流緩衝區適用于需要比 MCI 提供更精確控制輸出的應用程式。
-   [MIDI 服務](midi-services.md)。 需要最精確控制 MIDI 資料的應用程式通常會使用這些低層級的服務。

下列主題將討論這些方法的每一種，並提供 MIDI 對應程式的總覽。

-   [MIDI 對應程式](the-midi-mapper.md)
-   [ (MCI) 的 Media Control 介面 ](media-control-interface--mci.md)
-   [資料流程緩衝區](stream-buffers.md)
-   [MIDI 服務](midi-services.md)
-   [播放 MIDI 檔案](playing-midi-files.md)
-   [錄製 MIDI 音訊](recording-midi-audio.md)
-   [處理來自兩個 MIDI 來源的 MIDI 資料](processing-midi-data-from-two-midi-sources.md)
-   [建立 MIDI 檔案](creating-midi-files.md)

 

 




