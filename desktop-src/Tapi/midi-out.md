---
description: Midi/out 裝置類別包含用於輸出的 MIDI sequencers。 您可以使用「平臺軟體發展工具組」 (SDK) 中所述的 MIDI 功能來存取這些裝置。
ms.assetid: 398119ec-2d08-4c37-a993-a9b5ce52bcc8
title: midi/輸出
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4c0199cc7918ab9aeacb3210b6f98d5ff03fc3bca90624bee00d864727ae0fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119518608"
---
# <a name="midiout"></a>midi/輸出

Midi/out 裝置類別包含用於輸出的 MIDI sequencers。 您可以使用「平臺軟體發展工具組」 (SDK) 中所述的 MIDI 功能來存取這些裝置。

[**LineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid)和 [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid)函式會填滿 [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring)結構、將 **dwStringFormat** 成員設定為 STRINGFORMAT \_ 二進位值，並附加這個額外的成員：

``` syntax
DWORD DeviceId;  // identifier of MIDI device
```

**DeviceId** 成員是封閉式 MIDI 裝置的識別碼。 您可以在 [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) 函式的呼叫中使用此識別碼來開啟裝置以進行輸出。 您可以使用產生的裝置控制碼，線上路或電話裝置上播放 MIDI 資料。

如需有關 MIDI 功能的詳細資訊，請參閱 [**多媒體功能**](../multimedia/multimedia-functions.md)。

 

 
