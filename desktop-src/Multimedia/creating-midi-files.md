---
title: 建立 MIDI 檔案
description: 建立 MIDI 檔案
ms.assetid: 2fca3b41-14f9-4eaf-9fdb-8f952c834302
keywords:
- Windows 多媒體，建立 MIDI 檔案
- 多媒體，建立 MIDI 檔案
- 多媒體音訊，建立 MIDI 檔
- 音訊，建立 MIDI 檔案
- " (MIDI) 的音樂檢測數位介面，建立檔案"
- MIDI (的音樂檢測數位介面) ，建立檔案
- 建立 MIDI 檔案，關於
- " (MMA) 的 MIDI 製造商關聯"
- 'MMA (MIDI 製造商關聯) '
- MIDI 詳細規格
- 標準 MIDI 檔案規格
- 一般 MIDI (GM) 規格
- GM (一般 MIDI) 規格
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e36ccc25e73d6a28afc9001f2862870f1fa1a9ef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021168"
---
# <a name="creating-midi-files"></a>建立 MIDI 檔案

樂器數位介面 (的 MIDI) 規格是由所發佈，而且是「MIDI 製造商」關聯 (MMA) 的受著作權保護的內容。 下列清單描述最大的一般興趣規格：

## <a name="midi-detailed-specification"></a>MIDI 詳細規格

MIDI 詳細規格說明了 MIDI 硬體和軟體通訊協定。 這對開發多媒體應用程式很有用，這些應用程式會使用 MIDI 功能來錄製、編輯及/或播放 MIDI 資料，以實行 MIDI 支援。

## <a name="standard-midi-files-10"></a>標準 MIDI 檔案1。0

標準 MIDI 檔案規格定義了一種方法，可在相同或不同硬體平臺上的不同應用程式之間交換時間戳記的 MIDI 資料。 這對於撰寫應用程式以讀取和剖析包含 MIDI 資料的磁片檔案，以及/或將 MIDI 資料檔案寫入磁片的應用程式很有用。

## <a name="general-midi-system---level-1"></a>一般 MIDI 系統-層級1

一般 MIDI (GM) 規格會定義「一般 MIDI 系統」的最小 MIDI 設定。 這個系統是由一種特定的 MIDI 播放裝置類別所組成，而且對撰寫 MIDI 檔案的多媒體開發人員而言也很感興趣。 現今製造的大部分電腦音效卡和 MIDI 合成者都與 GM 規格相容。 針對 GM 規格所撰寫的 MIDI 檔案，通常應該會因為其預定音效而音效，無論是在哪一個 GM 相容裝置上播放。

為了讓 MIDI 檔案成為在多媒體運算中代表音樂的可行格式，Windows 會遵循一般的 MIDI 系統層級1規格。 下列主題提供其他的 MIDI 撰寫指導方針：

-   [適用于 MIDI 檔案的撰寫指導方針](authoring-guidelines-for-midi-files.md)
-   [標準 MIDI 修補程式指派](standard-midi-patch-assignments.md)
-   [標準 MIDI 金鑰指派](standard-midi-key-assignments.md)

 

 




