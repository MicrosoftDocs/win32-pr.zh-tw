---
description: 本主題說明如何建立、識別、設定和刪除計時器。
ms.assetid: 509a6fc4-ddee-4ff4-88a2-25dad4c48c2f
title: 關於計時器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3163dbfd5357de516e0202665cd76d017335593
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945347"
---
# <a name="about-timers"></a>關於計時器

本主題說明如何建立、識別、設定和刪除計時器。 應用程式會在經過指定的時間之後，使用計時器來排程視窗的事件。 每次指定的間隔 (或超時時間值) 用於計時器時，系統會通知與計時器相關聯的視窗。 因為計時器的精確度取決於系統時鐘率，以及應用程式從訊息佇列中抓取訊息的頻率，所以超時值只是近似。

本主題包含下列各節。

-   [計時器作業](#timer-operations)
-   [高解析度計時器](#high-resolution-timer)
-   [可等候計時器物件](#waitable-timer-objects)
-   [相關主題](#related-topics)

## <a name="timer-operations"></a>計時器作業

應用程式會使用 [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) 函數來建立計時器。 新的計時器會在建立間隔時立即開始計時。 應用程式可以使用 **SetTimer** 來變更計時器的超時值，而且可以使用 [**KillTimer**](/windows/win32/api/winuser/nf-winuser-killtimer) 函數來終結計時器。 若要有效率地使用系統資源，應用程式應該銷毀不再需要的計時器。

每個計時器都有唯一的識別碼。 建立計時器時，應用程式可以指定識別碼或讓系統建立唯一值。 [**WM \_ 計時器**](wm-timer.md)訊息的第一個參數包含張貼訊息之計時器的識別碼。

如果您在呼叫 [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer)時指定視窗控制碼，則應用程式會將計時器與該視窗產生關聯。 每當計時器的超時值過期時，系統會將 [**WM \_ 計時器**](wm-timer.md) 訊息張貼至與計時器相關聯的視窗。 如果未在 **SetTimer** 的呼叫中指定視窗控制碼，則建立計時器的應用程式必須監視其 **WM \_ 計時器** 訊息的訊息佇列，並將其分派至適當的視窗。 如果您指定 [**TimerProc**](/windows/win32/api/winuser/nc-winuser-timerproc) 回呼函式，則預設視窗程式會在處理 **WM \_ 計時器** 時呼叫回呼函式。 因此，即使您使用 **TimerProc** 而不是處理 **WM \_ 計時器**，也必須在呼叫執行緒中分派訊息。

如果您需要在計時器過期時收到通知，請使用可等候計時器。 如需詳細資訊，請參閱 [可等候計時器物件](/windows/desktop/Sync/waitable-timer-objects)。

## <a name="high-resolution-timer"></a>High-Resolution 計時器

計數器是在程式設計中用來參考遞增變數的一般詞彙。 某些系統包含高解析度效能計數器，可提供高解析度的經過時間。

如果系統上有高解析度的效能計數器，您可以使用 [**QueryPerformanceFrequency**](/windows/desktop/api/profileapi/nf-profileapi-queryperformancefrequency) 函式來表示頻率（以每秒計數）。 計數的值與處理器相依。 例如，在某些處理器上，計數可能是處理器時鐘的迴圈速率。

[**QueryPerformanceCounter**](/windows/desktop/api/profileapi/nf-profileapi-queryperformancecounter)函式會捕獲高解析度效能計數器的目前值。 藉由在程式碼區段的開頭和結尾呼叫這個函數，應用程式基本上會使用計數器作為高解析度計時器。 例如，假設 [**QueryPerformanceFrequency**](/windows/desktop/api/profileapi/nf-profileapi-queryperformancefrequency) 指出高解析度效能計數器的頻率是每秒50000個計數。 如果應用程式在程式碼區段之前和之後立即呼叫 **QueryPerformanceCounter** ，則計數器值可能分別為1500計數和3500計數。 這些值會指出在程式碼執行期間，.04 的秒數 (2000) 經過的時間。

## <a name="waitable-timer-objects"></a>可等候計時器物件

可等候計時器物件是一種同步處理物件，其狀態會在指定的到期時間到達時設為已發出信號。 您可以建立兩種類型的可等候計時器：手動重設和同步處理。 這兩種類型的計時器也可以是週期性計時器。

執行緒使用 [**CreateWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw) 或 [**CreateWaitableTimerEx**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerexw) 函數來建立計時器物件。 建立執行緒會指定計時器是手動重設計時器或同步處理計時器。 建立執行緒可以指定計時器物件的名稱。 其他進程中的執行緒可以藉由在 [**OpenWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-openwaitabletimerw) 函式的呼叫中指定其名稱，來開啟現有計時器的控制碼。 任何具有計時器物件之控制碼的執行緒都可以使用其中一個等候函式來等候計時器狀態設定為已發出信號。

如需有關使用可等候計時器物件進行執行緒同步處理的詳細資訊，請參閱 [可等候計時器物件](/windows/desktop/Sync/waitable-timer-objects)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用計時器](using-timers.md)
</dt> </dl>

 

 
