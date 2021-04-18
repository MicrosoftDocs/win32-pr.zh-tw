---
description: Windows 包含下列新的程式設計專案以進行同步處理。
ms.assetid: 16cd98d2-adc5-4a14-ad39-a0c5b4cc00cc
title: 同步處理的新功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4702ba10126d9c0eeeb85462195680b074918584
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104192931"
---
# <a name="whats-new-in-synchronization"></a>同步處理的新功能

Windows 包含下列新的程式設計專案以進行同步處理。

## <a name="windows-8"></a>Windows 8

### <a name="new-functions"></a>新函式

<dl> <dt>

[**DeleteSynchronizationBarrier**](/windows/desktop/api/SynchAPI/nf-synchapi-deletesynchronizationbarrier)
</dt> <dd>

刪除同步處理屏障。

</dd> <dt>

[**EnterSynchronizationBarrier**](/windows/desktop/api/synchapi/nf-synchapi-entersynchronizationbarrier)
</dt> <dd>

讓呼叫執行緒在同步處理屏障等候，直到執行緒的最大數目進入關卡為止。

</dd> <dt>

[**GetOverlappedResultEx**](/windows/desktop/api/Ioapiset/nf-ioapiset-getoverlappedresultex)
</dt> <dd>

在指定的逾時間隔內，針對指定的檔案、具名管道或通訊裝置，抓取重迭作業的結果。 呼叫執行緒可以執行可提供警示等候。

</dd> <dt>

[**InitializeSynchronizationBarrier**](/windows/desktop/api/synchapi/nf-synchapi-entersynchronizationbarrier)
</dt> <dd>

指定新同步處理屏障的執行緒數目上限和微調計數。

</dd> <dt>

[**WaitOnAddress**](/windows/desktop/api/SynchAPI/nf-synchapi-waitonaddress)
</dt> <dd>

等候指定之位址的值變更。

</dd> <dt>

[**WakeByAddressAll**](/windows/desktop/api/SynchAPI/nf-synchapi-wakebyaddressall)
</dt> <dd>

喚醒等候位址值變更的所有線程。

</dd> <dt>

[**WakeByAddressSingle**](/windows/desktop/api/SynchAPI/nf-synchapi-wakebyaddresssingle)
</dt> <dd>

喚醒一個等候位址值變更的執行緒。

</dd> </dl>

### <a name="new-interlocked-functions"></a>新的連鎖函數

<dl> <dt>

[**InterlockedAddNoFence**](/previous-versions/windows/desktop/legacy/hh972629(v=vs.85))
</dt> <dd>

在指定的 **LONG** 值上執行不可部分完成的加法運算。 作業會以程式方式執行，但不會使用記憶體阻礙。

</dd> <dt>

[**InterlockedAddNoFence64**](/previous-versions/windows/desktop/legacy/hh972630(v=vs.85))
</dt> <dd>

在指定的 **LONGLONG** 值上執行不可部分完成的加法運算。 作業會以程式方式執行，但不會使用記憶體阻礙。

</dd> <dt>

[**InterlockedAndNoFence**](/previous-versions/windows/desktop/legacy/hh972634(v=vs.85))
</dt> <dd>

在指定的 **LONG** 值上執行不可部分完成的運算。 作業會以程式方式執行，但不會使用記憶體阻礙。

</dd> <dt>

[**InterlockedAnd8NoFence**](/previous-versions/windows/desktop/legacy/hh972633(v=vs.85))
</dt> <dd>

在指定的 **char** 值上執行不可部分完成的運算。 作業會以程式方式執行，但不會使用記憶體阻礙。

</dd> <dt>

[**InterlockedAnd16NoFence**](/previous-versions/windows/desktop/legacy/hh972631(v=vs.85))
</dt> <dd>

對指定的 **短** 值執行不可部分完成的運算。 作業會以程式方式執行，但不會使用記憶體阻礙。

</dd> <dt>

[**InterlockedAnd64NoFence**](/previous-versions/windows/desktop/legacy/hh972632(v=vs.85))
</dt> <dd>

在指定的 **LONGLONG** 值上執行不可部分完成的運算。 作業會以程式方式執行，但不會使用記憶體阻礙。

</dd> <dt>

[**InterlockedBitTestAndComplement64**](/previous-versions/windows/desktop/legacy/hh972635(v=vs.85))
</dt> <dd>

測試指定之 **LONG64** 值的指定位，並加以補充。 此作業是不可部分完成的。

</dd> <dt>

[**InterlockedBitTestAndResetAcquire**](/previous-versions/windows/desktop/legacy/hh972636(v=vs.85))
</dt> <dd>

測試指定之 **LONG** 值的指定位並將它設定為0。 作業是不可部分完成的，而且會使用取得記憶體順序語義來執行。

</dd> <dt>

[**InterlockedBitTestAndResetRelease**](/previous-versions/windows/desktop/legacy/hh972637(v=vs.85))
</dt> <dd>

測試指定之 **LONG** 值的指定位並將它設定為0。 作業是不可部分完成的，而且會使用記憶體釋放語義來執行。

</dd> <dt>

[**InterlockedBitTestAndSetAcquire**](/previous-versions/windows/desktop/legacy/hh972638(v=vs.85))
</dt> <dd>

測試指定之 **LONG** 值的指定位並將它設定為1。 作業是不可部分完成的，而且會使用取得記憶體順序語義來執行。

</dd> <dt>

[**InterlockedBitTestAndSetRelease**](/previous-versions/windows/desktop/legacy/hh972639(v=vs.85))
</dt> <dd>

測試指定之 **LONG** 值的指定位並將它設定為1。 作業是不可部分完成的，而且會使用發行記憶體順序的語法來執行。

</dd> <dt>

[**InterlockedCompareExchangeNoFence**](/previous-versions/windows/desktop/legacy/hh972645(v=vs.85))
</dt> <dd>

在指定的值上執行不可部分完成的比較與交換作業。 函數會比較兩個指定的32位值，並根據比較結果與另一個32位值交換。 作業會以程式方式執行，但不會使用記憶體阻礙。

</dd> <dt>

[**InterlockedCompareExchange16**](/windows/desktop/api/Winnt/nf-winnt-interlockedcompareexchange16)
</dt> <dd>

在指定的值上執行不可部分完成的比較與交換作業。 函數會比較兩個指定的16位值，並根據比較結果與另一個16位值交換。

</dd> <dt>

[**InterlockedCompareExchange16Acquire**](/previous-versions/windows/desktop/legacy/hh972642(v=vs.85))
</dt> <dd>

在指定的值上執行不可部分完成的比較與交換作業。 函數會比較兩個指定的16位值，並根據比較結果與另一個16位值交換。 執行作業時，會使用取得記憶體順序的語法。

</dd> <dt>

[**InterlockedCompareExchange16Release**](/previous-versions/windows/desktop/legacy/hh972644(v=vs.85))
</dt> <dd>

在指定的值上執行不可部分完成的比較與交換作業。 函數會比較兩個指定的16位值，並根據比較結果與另一個16位值交換。 交換會以發行記憶體順序的語法來執行。

</dd> <dt>

[**InterlockedCompareExchange16NoFence**](/previous-versions/windows/desktop/legacy/hh972643(v=vs.85))
</dt> <dd>

在指定的值上執行不可部分完成的比較與交換作業。 函數會比較兩個指定的16位值，並根據比較結果與另一個16位值交換。 作業會以程式方式執行，但不會使用記憶體阻礙。

</dd> <dt>

[**InterlockedCompareExchangeNoFence64**](/previous-versions/windows/desktop/legacy/hh972646(v=vs.85))
</dt> <dd>

在指定的值上執行不可部分完成的比較與交換作業。 函數會比較兩個指定的64位值，並根據比較結果與另一個64位值交換。 作業會以程式方式執行，但不會使用記憶體阻礙。

</dd> <dt>

[**InterlockedCompareExchange128**](/windows/desktop/api/Winnt/nf-winnt-interlockedcompareexchange128)
</dt> <dd>

在指定的值上執行不可部分完成的比較與交換作業。 函數會比較兩個指定的128位值，並根據比較結果與另一個128位值交換。

</dd> <dt>

[**InterlockedCompareExchangePointerNoFence**](/previous-versions/windows/desktop/legacy/hh972647(v=vs.85))
</dt> <dd>

在指定的值上執行不可部分完成的比較與交換作業。 此函式會比較兩個指定的指標值，並根據比較結果與另一個指標值交換。 作業會以程式方式執行，但不會使用記憶體阻礙。

</dd> <dt>

[**InterlockedDecrementNoFence**](/previous-versions/windows/desktop/legacy/hh972652(v=vs.85))
</dt> <dd>

遞減 (會以一) 指定的32位變數值做為不可部分完成的作業來減少。 作業會以程式方式執行，但不會使用記憶體阻礙。

</dd> <dt>

[**InterlockedDecrement16**](/windows/desktop/api/Winnt/nf-winnt-interlockeddecrement16)
</dt> <dd>

遞減 (會將指定的16位變數值減少一) 為不可部分完成的作業。

</dd> <dt>

[**InterlockedDecrement16Acquire**](/previous-versions/windows/desktop/legacy/hh972649(v=vs.85))
</dt> <dd>

遞減 (會將指定的16位變數值減少一) 為不可部分完成的作業。 執行作業時，會使用取得記憶體順序的語法。

</dd> <dt>

[**InterlockedDecrement16Release**](/previous-versions/windows/desktop/legacy/hh972651(v=vs.85))
</dt> <dd>

遞減 (會將指定的16位變數值減少一) 為不可部分完成的作業。 作業會使用發行記憶體順序的語法來執行。

</dd> <dt>

[**InterlockedDecrement16NoFence**](/previous-versions/windows/desktop/legacy/hh972650(v=vs.85))
</dt> <dd>

遞減 (會將指定的16位變數值減少一) 為不可部分完成的作業。 作業會以程式方式執行，但不會使用記憶體阻礙。

</dd> <dt>

[**InterlockedDecrementNoFence64**](/previous-versions/windows/desktop/legacy/hh972653(v=vs.85))
</dt> <dd>

遞減 (會以一) 指定的64位變數值做為不可部分完成的作業來減少。 作業會以程式方式執行，但不會使用記憶體阻礙。

</dd> <dt>

[**InterlockedExchangeNoFence**](/previous-versions/windows/desktop/legacy/hh972659(v=vs.85))
</dt> <dd>

將64位變數設定為指定的值，作為不可部分完成的作業。 作業會以程式方式執行，但不會使用記憶體阻礙。

</dd> <dt>

[**InterlockedExchange8**](/windows/desktop/api/Winnt/nf-winnt-interlockedexchange8)
</dt> <dd>

將8位變數設定為指定的值，作為不可部分完成的作業。

</dd> <dt>

[**InterlockedExchange16Acquire**](/previous-versions/windows/desktop/legacy/hh972654(v=vs.85))
</dt> <dd>

將16位變數設定為指定的值，作為不可部分完成的作業。 作業是使用取得記憶體順序語義來執行。

</dd> <dt>

[**InterlockedExchange16NoFence**](/previous-versions/windows/desktop/legacy/hh972655(v=vs.85))
</dt> <dd>

將16位變數設定為指定的值，作為不可部分完成的作業。 作業會以程式方式執行，但不會使用記憶體阻礙。

</dd> <dt>

[**InterlockedExchangeNoFence64**](/previous-versions/windows/desktop/legacy/hh972660(v=vs.85))
</dt> <dd>

將64位變數設定為指定的值，作為不可部分完成的作業。 作業會以程式方式執行，但不會使用記憶體阻礙。

</dd> <dt>

[**InterlockedExchangePointerNoFence**](/previous-versions/windows/desktop/legacy/hh972661(v=vs.85))
</dt> <dd>

以不可部分完成的方式交換一對位址。 作業會以程式方式執行，但不會使用記憶體阻礙。

</dd> <dt>

[**InterlockedExchangeAddNoFence**](/previous-versions/windows/desktop/legacy/hh972657(v=vs.85))
</dt> <dd>

執行 2 32 位值的不可部分完成加法。 作業會以程式方式執行，但不會使用記憶體阻礙。

</dd> <dt>

[**InterlockedExchangeAddNoFence64**](/previous-versions/windows/desktop/legacy/hh972658(v=vs.85))
</dt> <dd>

執行 2 64 位值的不可部分完成加法。 作業會以程式方式執行，但不會使用記憶體阻礙。

</dd> <dt>

[**InterlockedIncrementNoFence**](/previous-versions/windows/desktop/legacy/hh972667(v=vs.85))
</dt> <dd>

遞增 (會以一) 指定的32位變數值為不可部分完成的作業增加。 作業會以程式方式執行，但不會使用記憶體阻礙。

</dd> <dt>

[**InterlockedIncrement16**](/windows/desktop/api/Winnt/nf-winnt-interlockedincrement16)
</dt> <dd>

遞增 (增加一個) 指定的16位變數值為不可部分完成的作業。

</dd> <dt>

[**InterlockedIncrement16Acquire**](/previous-versions/windows/desktop/legacy/hh972663(v=vs.85))
</dt> <dd>

遞增 (增加一個) 指定的16位變數值為不可部分完成的作業。 作業是使用取得記憶體順序語義來執行。

</dd> <dt>

[**InterlockedIncrement16Release**](/previous-versions/windows/desktop/legacy/hh972665(v=vs.85))
</dt> <dd>

遞增 (增加一個) 指定的16位變數值為不可部分完成的作業。 作業是使用發行記憶體順序的語法來執行。

</dd> <dt>

[**InterlockedIncrement16NoFence**](/previous-versions/windows/desktop/legacy/hh972664(v=vs.85))
</dt> <dd>

遞增 (增加一個) 指定的16位變數值為不可部分完成的作業。 作業會以程式方式執行，但不會使用記憶體阻礙。

</dd> <dt>

[**InterlockedIncrementNoFence64**](/previous-versions/windows/desktop/legacy/hh972668(v=vs.85))
</dt> <dd>

遞增 (會以一) 指定的64位變數值為不可部分完成的作業增加。 作業會以程式方式執行，但不會使用記憶體阻礙。

</dd> <dt>

[**InterlockedOrNoFence**](/previous-versions/windows/desktop/legacy/hh972672(v=vs.85))
</dt> <dd>

在指定的 **LONG** 值上執行不可部分完成的或運算。 作業會以程式方式執行，但不會使用記憶體阻礙。

</dd> <dt>

[**InterlockedOr8NoFence**](/previous-versions/windows/desktop/legacy/hh972671(v=vs.85))
</dt> <dd>

在指定的 **char** 值上執行不可部分完成的或運算。 作業會以程式方式執行，但不會使用記憶體阻礙。

</dd> <dt>

[**InterlockedOr16NoFence**](/previous-versions/windows/desktop/legacy/hh972669(v=vs.85))
</dt> <dd>

對指定的 **短** 值執行不可部分完成的或運算。 作業會以程式方式執行，但不會使用記憶體阻礙。

</dd> <dt>

[**InterlockedOr64NoFence**](/previous-versions/windows/desktop/legacy/hh972670(v=vs.85))
</dt> <dd>

在指定的 **LONGLONG** 值上執行不可部分完成的或運算。 作業會以程式方式執行，但不會使用記憶體阻礙。

</dd> <dt>

[**InterlockedPushListSListEx**](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushlistslistex)
</dt> <dd>

在另一個單一連結清單的前方插入單一連結清單。 系統會在多處理器系統上同步處理清單的存取。 此版本的方法不會使用[ \_ \_ fastcall](https://msdn.microsoft.com/library/6xa169sk(v=VS.71).aspx)呼叫慣例。

</dd> <dt>

[**InterlockedXorNoFence**](/previous-versions/windows/desktop/legacy/hh972677(v=vs.85))
</dt> <dd>

在指定的 **LONG** 值上執行不可部分完成 XOR 運算。 作業會以程式方式執行，但不會使用記憶體阻礙。

</dd> <dt>

[**InterlockedXor8NoFence**](/previous-versions/windows/desktop/legacy/hh972676(v=vs.85))
</dt> <dd>

在指定的 **char** 值上執行不可部分完成 XOR 運算。 作業會以程式方式執行，但不會使用記憶體阻礙。

</dd> <dt>

[**InterlockedXor16NoFence**](/previous-versions/windows/desktop/legacy/hh972674(v=vs.85))
</dt> <dd>

在指定的 **短** 值上執行不可部分完成的 XOR 運算。 作業會以程式方式執行，但不會使用記憶體阻礙。

</dd> <dt>

[**InterlockedXor64NoFence**](/previous-versions/windows/desktop/legacy/hh972675(v=vs.85))
</dt> <dd>

在指定的 **LONGLONG** 值上執行不可部分完成的 XOR 運算。 作業會以程式方式執行，但不會使用記憶體阻礙。

</dd> </dl>

## <a name="windows-7"></a>Windows 7

### <a name="new-functions"></a>新函式

<dl> <dt>

[**SetWaitableTimerEx**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimerex)
</dt> <dd>

啟用指定的可等候計時器，並提供計時器的內容資訊。

</dd> <dt>

[**TryAcquireSRWLockExclusive**](/windows/win32/api/synchapi/nf-synchapi-tryacquiresrwlockexclusive)
</dt> <dd>

嘗試取得超薄的讀取器/寫入器 (在獨佔模式中 SRW) 鎖定。 如果呼叫成功，呼叫的執行緒就會取得鎖定的擁有權。

</dd> <dt>

[**TryAcquireSRWLockShared**](/windows/win32/api/synchapi/nf-synchapi-tryacquiresrwlockshared)
</dt> <dd>

嘗試取得輕巧的讀取器/寫入器 (在共用模式中 SRW) 鎖定。 如果呼叫成功，呼叫的執行緒就會取得鎖定的擁有權。

</dd> </dl>

### <a name="new-structures"></a>新結構

<dl> <dt>

[**原因 \_ 內容**](/windows/win32/api/minwinbase/ns-minwinbase-reason_context)
</dt> <dd>

包含使用 [**SetWaitableTimerEx**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimerex)啟動之計時器的內容資訊。

</dd> </dl>

 

 
