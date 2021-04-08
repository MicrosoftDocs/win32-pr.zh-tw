---
title: 關於多媒體計時器
description: 關於多媒體計時器
ms.assetid: 42101923-3f46-4234-bfcf-a0d06c382fa1
keywords:
- Windows 多媒體，計時器
- 多媒體、計時器
- 多媒體輸入，計時器
- 多媒體計時器，關於
- 計時器，關於
- 多媒體計時器，排程事件
- 計時器，排程事件
- 排程計時器事件
- 高解析度計時
- SetTimer 函式
- CreateWaitableTimer 函式
- WM_TIMER 訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c36e5f19a92b6b47a3b1976bd85aadef88ab3ec
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023413"
---
# <a name="about-multimedia-timers"></a>關於多媒體計時器

多媒體計時器服務可讓應用程式以最高解析度 (或硬體平臺的精確度) 來排程計時器事件。 這些多媒體計時器服務可讓您以比其他計時器服務更高的解析度來排程計時器事件。

這些計時器服務適用于需要高解析度時間的應用程式。 例如，MIDI sequencer 需要高解析度計時器，因為它必須維持在1毫秒的解決範圍內之 MIDI 事件的步調。

未使用高解析度時間的應用程式應該使用 [SetTimer](/windows/win32/api/winuser/nf-winuser-settimer) 函式，而不是多媒體計時器服務。 **SetTimer** 提供的計時器服務會將 [WM \_ 計時器](../winmsg/wm-timer.md)訊息張貼到訊息佇列，而多媒體計時器服務會呼叫回呼函數。 需要可等候計時器的應用程式應該使用 [CreateWaitableTimer](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw) 函數。

 

 