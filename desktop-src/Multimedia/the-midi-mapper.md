---
title: MIDI 對應程式
description: MIDI 對應程式
ms.assetid: 92cffc67-b4a4-4807-94d2-02fbbdba5abf
keywords:
- Windows 多媒體，MIDI 對應程式
- 多媒體，MIDI 對應程式
- 多媒體音訊、MIDI 對應程式
- 音訊、MIDI 對應程式
- 音樂檢測數位介面 (MIDI) 、MIDI 對應程式
- MIDI (的音樂檢測數位介面) 、MIDI 對應程式
- MIDI 對應程式，關於
- MIDI 對應程式，來源
- MIDI 對應程式，目的地
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3b360148c994c0ee6434fdf097ca5f393b23d49
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021274"
---
# <a name="the-midi-mapper"></a>MIDI 對應程式

MIDI 對應工具的標準修補程式服務可為應用程式提供與裝置無關的 MIDI 檔案播放。 MIDI 對應工具可以搭配使用 MCI MIDI sequencer 或低層級的 MIDI 輸出服務。

除非另有說明，否則所有對 MIDI 通道編號的參考都會使用邏輯通道編號1到16。 這些邏輯通道編號會對應至真正屬於 MIDI 訊息的實體通道編號0到15。 所有對 MIDI 程式-變更和索引鍵值的參考都會使用實體值0到127。 除非前面加上 "0x" 前置詞，否則所有數位都是十進位數，在這種情況下，它們是十六進位。

在 MIDI 對應工具的討論中，「 *來源* 」一詞是指 midi 對應程式的輸入端。 「 *目的地* 」一詞指的是 MIDI 對應程式的輸出端。 例如，來源通道是傳送至 MIDI 對應程式之訊息的 MIDI 通道，而目的地通道則是從 MIDI 對應程式傳送到輸出裝置之訊息的 MIDI 通道。

-   [MIDI 對應程式和 Windows](the-midi-mapper-and-windows.md)
-   [MIDI 對應程式架構](the-midi-mapper-architecture.md)
-   [通道對應](the-channel-map.md)
-   [修補程式對應](patch-maps.md)
-   [磁片區純量](the-volume-scalar.md)
-   [金鑰組應](key-maps.md)
-   [地圖和 MIDI 訊息的摘要](summary-of-maps-and-midi-messages.md)

 

 




