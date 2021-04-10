---
description: Midi/out 裝置類別包含用於輸出的 MIDI sequencers。 您可以使用「平臺軟體發展工具組」 (SDK) 中所述的 MIDI 功能來存取這些裝置。
ms.assetid: 398119ec-2d08-4c37-a993-a9b5ce52bcc8
title: midi/輸出
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d6ae6a3daba8fa0520fca666e6c43a8b3db86c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191113"
---
# <a name="midiout"></a>midi/輸出

Midi/out 裝置類別包含用於輸出的 MIDI sequencers。 您可以使用「平臺軟體發展工具組」 (SDK) 中所述的 MIDI 功能來存取這些裝置。

[**LineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid)和 [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid)函式會填滿 [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring)結構、將 **dwStringFormat** 成員設定為 STRINGFORMAT \_ 二進位值，並附加這個額外的成員：

``` syntax
DWORD DeviceId;  // identifier of MIDI device
```

**DeviceId** 成員是封閉式 MIDI 裝置的識別碼。 您可以在 [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) 函式的呼叫中使用此識別碼來開啟裝置以進行輸出。 您可以使用產生的裝置控制碼，線上路或電話裝置上播放 MIDI 資料。

如需有關 MIDI 功能的詳細資訊，請參閱 [**多媒體功能**](../multimedia/multimedia-functions.md)。

 

 
