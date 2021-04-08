---
title: 要求時間格式
description: 要求時間格式
ms.assetid: 3492dfe3-ed54-405a-aa4f-b17abbd1e07f
keywords:
- " (MIDI) ，時間格式的音樂檢測數位介面"
- MIDI (的音樂檢測數位介面) ，時間格式
- MIDI 服務，時間格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf191c857c45896c916ace4656d33bd3dd558f04
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103681734"
---
# <a name="requesting-time-formats"></a>要求時間格式

Windows 會使用 [**MMTIME**](/previous-versions//dd757347(v=vs.85)) 結構以一或多個不同的格式來表示時間，包括毫秒、範例、SMPTE 和 MIDI 歌曲指標格式。 **WType** 成員會指定時間格式。

[**MidiStreamPosition**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamposition)函數會使用 **MMTIME** 結構。 在呼叫此函式之前，您必須先設定 **wType** 成員，以指出您所要求的時間格式。 若要查看是否支援要求的時間格式，請在呼叫後檢查 **wType** 。 如果不支援要求的時間格式，則會以設備磁碟機所選取的替代時間格式來指定時間，而 **wType** 成員會變更以指出選取的時間格式。

如需 **MMTIME** 結構的詳細資訊，請參閱 [多媒體計時器](multimedia-timers.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[MIDI 服務](midi-services.md)
</dt> </dl>

 

 