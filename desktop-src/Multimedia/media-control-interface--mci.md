---
title: " (MCI) 的 Media Control 介面"
description: " (MCI) 的 Media Control 介面"
ms.assetid: e22f23b5-0fa6-4957-bbbf-b1b3a4c8bd31
keywords:
- 'Windows 多媒體、媒體控制介面 (MCI) '
- '多媒體、媒體控制介面 (MCI) '
- '多媒體音訊、媒體控制介面 (MCI) '
- '音訊、媒體控制介面 (MCI) '
- '音樂檢測數位介面 (MIDI) 、媒體控制介面 (MCI) '
- 'MIDI (的音樂檢測數位介面) 、媒體控制介面 (MCI) '
- '媒體控制介面 (MCI) 、音樂檢測數位介面 (MIDI) '
- 'MCI (媒體控制介面) 、音樂檢測數位介面 (MIDI) '
- 媒體控制介面 (MCI) 、MIDI sequencer
- MCI (媒體控制介面) 、MIDI sequencer
- MCI MIDI sequencer，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00aaf582f625c4411a2400ee381ec5c17d4d8ae7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021373"
---
# <a name="media-control-interface-mci"></a> (MCI) 的 Media Control 介面

MCI MIDI sequencer 是播放 MIDI 檔案的 MCI 系統元件。 應用程式可以使用 MCI 輕鬆地播放 MIDI 檔案，但 MCI 對 MIDI 功能有下列限制：

-   MCI 僅支援 MIDI 輸出。
-   MCI 不允許在 MIDI 事件與其他即時事件之間進行關閉同步處理 (例如影片) 。

如果您需要精確的 MIDI 同步處理，您必須使用串流緩衝區或 MIDI 服務。 如果您需要 MIDI 輸入功能，您必須使用 MIDI 服務。

MCI MIDI sequencer 會播放標準的 MIDI 檔案和資源交換檔案格式 (RIFF) 的 MIDI 檔，稱為 RMID 檔案。 標準 MIDI 檔案符合標準的 [midi 檔案 1.0](creating-midi-files.md) 規格。 因為 RMID 檔案是具有 RIFF 標頭的標準 MIDI 檔案，所以標準 MIDI 檔案的相關資訊也適用于 RMID 檔案。 如需 RIFF 檔的詳細資訊，請參閱 [資源交換檔案格式服務](resource-interchange-file-format-services.md)。

雖然目前有三種標準的 MIDI 檔案，但 MCI sequencer 只會播放其中兩個： Format 0 和 Format 1 MIDI 檔。

如需控制多媒體裝置 (包括使用 MCI 命令的 sequencers) 的詳細資訊，請參閱 [mci](mci.md)。

 

 




