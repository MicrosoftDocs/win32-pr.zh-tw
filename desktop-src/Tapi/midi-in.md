---
description: Midi/in 裝置類別包含用於輸入的 MIDI sequencers。 您可以使用「平臺軟體發展工具組」 (SDK) 中所述的 MIDI 功能來存取這些裝置。
ms.assetid: 8997a391-bf61-4ec9-8ffc-fe3e6b92d63a
title: midi/in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d309fe510b08a1e86ef6a00b34a9e3d3282c993babe78eb45aeb6ebb0dab1eac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119659948"
---
# <a name="midiin"></a>midi/in

Midi/in 裝置類別包含用於輸入的 MIDI sequencers。 您可以使用「平臺軟體發展工具組」 (SDK) 中所述的 MIDI 功能來存取這些裝置。

[**LineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid)和 [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid)函式會填滿 [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring)結構、將 **dwStringFormat** 成員設定為 STRINGFORMAT \_ 二進位值，並附加這個額外的成員：

``` syntax
DWORD DeviceId;  // identifier of MIDI device
```

**DeviceId** 成員是封閉式 MIDI 裝置的識別碼。 在 [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) 函式的呼叫中，您可以使用此識別碼來開啟裝置以進行輸入。 您可以使用產生的裝置控制碼，從線路或電話裝置錄製 MIDI 資料。

如需有關 MIDI 功能的詳細資訊，請參閱 [**多媒體功能**](../multimedia/multimedia-functions.md)。

 

 
