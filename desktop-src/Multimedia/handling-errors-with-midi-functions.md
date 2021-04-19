---
title: 處理 MIDI 功能的錯誤
description: 處理 MIDI 功能的錯誤
ms.assetid: 7ea5db5e-34d7-4506-8157-c24adf5bcdda
keywords:
- 音樂檢測數位介面 (MIDI) ，錯誤
- MIDI (的音樂檢測數位介面) ，錯誤
- MIDI 服務，錯誤
- MIDI 錯誤
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9689fe30b9c4f598cfc9bea892ff3d4fe15d3a9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106967894"
---
# <a name="handling-errors-with-midi-functions"></a>處理 MIDI 功能的錯誤

MIDI 音訊函式會傳回非零的錯誤碼。 針對 MIDI 相關的錯誤， [**midiInGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-midiingeterrortext) 和 [**midiOutGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgeterrortext) 函式會取得錯誤碼的文字描述。 應用程式仍然必須查看錯誤值本身來判斷如何繼續，但它可以使用對話方塊中的錯誤描述來通知使用者發生錯誤狀況。

唯一不會傳回錯誤碼的 MIDI 函式是 [**midiInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetnumdevs) 和 [**midiOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetnumdevs) 函數。 如果系統中沒有任何裝置，或函數遇到任何錯誤，這些函式會傳回值零。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[MIDI 服務](midi-services.md)
</dt> </dl>

 

 