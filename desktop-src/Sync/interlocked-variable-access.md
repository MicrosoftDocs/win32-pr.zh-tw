---
description: 應用程式必須同步存取多個執行緒所共用的變數。
ms.assetid: 729c0e68-ef52-4d6c-b771-a89043a937e6
title: 連鎖變數存取
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b298dffe45d1a0de655e225c8a240dd72be15a0fff7e4d6eac25ebb0a1130ad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126318"
---
# <a name="interlocked-variable-access"></a>連鎖變數存取

應用程式必須同步存取多個執行緒所共用的變數。 應用程式也必須確保這些變數上的作業會以不可部分完成的方式執行， (完全或完全不執行。 ) 

簡單的讀取和寫入，以正確對齊的32位變數是不可部分完成的作業。 換句話說，您最後不會有一個已更新的變數部分。所有位都會以不可部分完成的方式更新。 但是，不保證會同步存取。 如果有兩個執行緒從相同的變數讀取和寫入，您就無法判斷某個執行緒是否會在另一個執行緒執行寫入作業之前，先執行它的讀取作業。

對適當對齊的64位變數進行簡單的讀取和寫入，在64位 Windows 上是不可部分完成的。 64位值的讀取和寫入不保證在32位 Windows 上是不可部分完成的。 在任何平臺上，讀取和寫入其他大小的變數不一定是不可部分完成的。

## <a name="the-interlocked-api"></a>連鎖 API

連鎖函數提供簡單的機制，可同步處理多個執行緒所共用之變數的存取。 它們也會以不可部分完成的方式執行變數的作業。 如果變數位於共用記憶體中，則不同進程的執行緒可以使用這些函數。

[**InterlockedIncrement**](/windows/win32/api/winnt/nf-winnt-interlockedincrement)和 [**InterlockedDecrement**](/windows/win32/api/winnt/nf-winnt-interlockeddecrement)函式結合了將變數遞增或遞減至不可部分完成作業的相關步驟。 這項功能在多工作業系統中相當有用，因為系統可以中斷線程的執行，以將處理器時間的配量授與另一個執行緒。 如果沒有這類同步處理，兩個執行緒可以讀取相同的值、將它遞增1，然後將新值儲存為總計增加1而不是2。 連鎖變數存取函式會防止這種錯誤。

[**InterlockedExchange**](/windows/win32/api/winnt/nf-winnt-interlockedexchange)和 [**InterlockedExchangePointer**](/windows/win32/api/winnt/nf-winnt-interlockedexchangepointer)函式會以不可部分完成的方式交換指定之變數的值。 [**InterlockedExchangeAdd**](/windows/win32/api/winnt/nf-winnt-interlockedexchangeadd)函式會結合兩個作業：將兩個變數相加，並將結果儲存在其中一個變數中。

[**InterlockedCompareExchange**](/windows/win32/api/winnt/nf-winnt-interlockedcompareexchange)、 [**InterlockedCompare64Exchange128**](/previous-versions/windows/desktop/legacy/ms683553(v=vs.85))和 [**InterlockedCompareExchangePointer**](/windows/win32/api/winnt/nf-winnt-interlockedcompareexchangepointer)函數會結合兩個作業：比較兩個值，並根據比較結果將第三個值儲存在其中一個變數中。

[**InterlockedAnd**](/windows/win32/api/winnt/nf-winnt-interlockedand)、 [**InterlockedOr**](/windows/win32/api/winnt/nf-winnt-interlockedor)和 [**InterlockedXor**](/windows/win32/api/winnt/nf-winnt-interlockedxor)函式會以原子方式分別執行 and、OR 和 XOR 作業。

有一些函式是專為在64位記憶體值和位址上執行連鎖變數存取而設計的，並已針對64位 Windows 進行優化。 這些函式中的每一個都包含名稱中的 "64";例如， [**InterlockedDecrement64**](/windows/win32/api/winnt/nf-winnt-interlockeddecrement64) 和 [**InterlockedCompareExchangeAcquire64**](/previous-versions/windows/desktop/legacy/ms683566(v=vs.85))。

大部分的連鎖函式在所有 Windows 平臺上都提供完整的記憶體障礙。 此外，也有一些函數可結合基本連鎖變數存取作業，以及特定處理器所支援的取得和釋放記憶體順序的語法。 這些函式中的每一個都會在其名稱中包含 "取得" 或 "Release" 這個字。例如， [**InterlockedDecrementAcquire**](/previous-versions/windows/desktop/legacy/ms683583(v=vs.85)) 和 [**InterlockedDecrementRelease**](/previous-versions/windows/desktop/legacy/ms683586(v=vs.85))。 取得記憶體語義：指定在嘗試任何其他記憶體作業之前，目前線程所執行的記憶體作業將會顯示。 釋放記憶體語義：指定完成其他所有記憶體作業之後，目前線程所執行的記憶體作業將會顯示。 這些語義可讓您強制以特定循序執行記憶體作業。 在輸入受保護的區域時，請使用取得語義，並在離開時使用該語義。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[編譯器內建函式](/cpp/intrinsics/compiler-intrinsics?view=vs-2019)
</dt> <dt>

[同步處理和多處理器問題](synchronization-and-multiprocessor-issues.md)
</dt> </dl>

 

 
