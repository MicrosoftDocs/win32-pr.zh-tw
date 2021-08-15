---
title: 接收 Running-Status 訊息
description: 接收 Running-Status 訊息
ms.assetid: 4f2e8e41-89f6-45e3-ae16-47b856f0e63e
keywords:
- 音樂檢測數位介面 (MIDI) ，執行狀態
- MIDI (音樂檢測數位介面) ，執行狀態
- 正在錄製 MIDI 音訊，執行狀態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f4d782e1e25c718ddd177d1d9baf471d0715d70680b65920052e85d6fffc551
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118371343"
---
# <a name="receiving-running-status-messages"></a>接收 Running-Status 訊息

*標準的 MIDI 檔案 1.0* 規格允許在訊息與先前的訊息具有相同的狀態位元組時，使用執行中的 *狀態*。 使用執行狀態時，可以省略後續訊息的狀態位元組。 所有的 MIDI 輸入裝置磁碟機都需要將使用執行中狀態的訊息擴充到完整的訊息中，如此一來，您一律會收到來自 MIDI 輸入裝置磁碟機的完整 MIDI 訊息。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[錄製 MIDI 音訊](recording-midi-audio.md)
</dt> </dl>

 

 




