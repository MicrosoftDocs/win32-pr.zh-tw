---
title: 變更 Sequencer 同步處理
description: 變更 Sequencer 同步處理
ms.assetid: 5c3acb47-e6cc-4957-a306-7039ec110827
keywords:
- MCI_SET 命令訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bffdc1606624f63fa05a9cc03c68fe64781620f
ms.sourcegitcommit: 8276af9231bdbf5a7334299f0d13fc8ff069a065
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/12/2021
ms.locfileid: "106982121"
---
# <a name="changing-sequencer-synchronization"></a>變更 Sequencer 同步處理

> [!NOTE]
> 無偏差的通訊-Microsoft 支援多樣化且 inclusionary 的環境。  本檔中有 ' 從屬 ' 這個字的參考。 Microsoft 的 [Bias-Free 通訊樣式指南](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) 會將此視為排他性行為單字。  這種用語是用來做為軟體內所使用的用語。 為求一致，本檔包含此字。 從軟體移除此字組時，我們會將此檔修正為一致。

若要變更 sequencer 裝置的同步處理模式，請使用 [**mci \_ set**](mci-set.md) 命令訊息與 mci \_ SEQ \_ set \_ MASTER 和 mci \_ seq \_ set \_ 從屬旗標。 [**MCI \_ SEQ \_ SET \_ PARMS**](mci-seq-set-parms.md) structure （ **dwMaster** 和 **dwSlave**）中的兩個成員是用來指定主要和次級同步處理模式。

主要同步處理模式會控制 sequencer 傳送至輸出埠的同步處理資訊。 以下是 **dwMaster** 成員的常數及其對應的主要同步處理模式。



| 常數        | 同步處理模式                                                                             |
|-----------------|--------------------------------------------------------------------------------------------------|
| MCI \_ SEQ \_ MIDI  | MIDI 同步處理。 使用 MIDI 計時時鐘訊息將計時資訊傳送至輸出埠。   |
| MCI \_ SEQ \_ SMPTE | SMPTE 同步處理。 使用 MIDI 四分之一框架訊息將計時資訊傳送至輸出埠。 |
| MCI \_ SEQ \_ 無  | 無同步處理。 不傳送任何時間資訊。                                                  |



 

次級同步處理模式會控制 sequencer 取得其計時資訊以播放 MIDI 檔案的位置。 以下是 **dwSlave** 成員及其對應次級同步處理模式的常數。



| 常數        | 同步處理模式                                                                                                                               |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| MCI \_ SEQ \_ 檔案  | 檔案同步處理。 從 MIDI 檔案取得計時資訊。                                                                                       |
| MCI \_ SEQ \_ MIDI  | MIDI 同步處理。 使用 MIDI 計時時鐘訊息從輸入埠取得計時資訊。                                                     |
| MCI \_ SEQ \_ SMPTE | SMPTE 同步處理。 使用 MIDI 四分之一框架訊息從輸入埠取得計時資訊。                                                   |
| MCI \_ SEQ \_ 無  | 無同步處理。 只取得來自 MCI 命令的計時資訊，並忽略時間資訊 (例如，MIDI 檔案中) 的節奏變更。 |



 

> [!Note]  
> 目前，在主要同步處理中，MCI MIDI sequencer 僅支援 (MCI \_ SEQ NONE) 的無同步處理模式 \_ 。 針對次級同步處理，它只支援 (MCI seq 檔案的檔案同步處理模式， \_ \_) 和沒有任何同步處理模式 (MCI \_ seq \_ 無) 。

 

 

 




