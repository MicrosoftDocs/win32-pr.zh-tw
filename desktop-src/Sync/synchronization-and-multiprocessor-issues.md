---
description: 在多處理器系統上執行時，應用程式可能會遇到問題，因為它們只會在單處理器系統上有效。
ms.assetid: b20a1d2c-b795-4ed8-ac33-539a347020c8
title: 同步處理和多處理器問題
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3896dc240e76f1506bac2a6a2e95f101b05beca7
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/21/2021
ms.locfileid: "107000499"
---
# <a name="synchronization-and-multiprocessor-issues"></a>同步處理和多處理器問題

在多處理器系統上執行時，應用程式可能會遇到問題，因為它們只會在單處理器系統上有效。

## <a name="thread-priorities"></a>執行緒優先順序

請考慮具有兩個執行緒的程式，其優先順序高於另一個執行緒。 在單處理器系統上，較高優先順序的執行緒將不會放棄較低優先順序執行緒的控制權，因為排程器會提供優先權較高的執行緒。 在多處理器系統上，這兩個執行緒可以同時執行，每個都在自己的處理器上執行。

應用程式應該同步處理資料結構的存取，以避免競爭情形。 假設較高優先順序執行緒在不幹擾較低優先順序執行緒的情況下執行的程式碼，在多處理器系統上將會失敗。

## <a name="memory-ordering"></a>記憶體順序

當處理器寫入記憶體位置時，會快取此值以改善效能。 同樣地，處理器會嘗試滿足快取的讀取要求以改善效能。 此外，處理器在應用程式要求之前，會先從記憶體中提取值。 這種情況可能會發生在推理執行的過程中，或由於快取行的問題。

CPU 快取可以分割成可以平行存取的銀行。 這表示記憶體作業可以依序完成。 為了確保記憶體作業已依序完成，大部分處理器都會提供記憶體屏障指令。 *完整的記憶體屏障* 可確保記憶體屏障指令之前出現的記憶體讀取和寫入作業，會在記憶體關卡指令之後出現的任何記憶體讀取和寫入作業之前認可至記憶體。 「 *讀取記憶體」屏障* 只會排序記憶體讀取作業，而 *寫入記憶體屏障* 只會對記憶體寫入作業進行排序。 這些指示也可確保編譯器會停用任何可能在阻礙之間重新排列記憶體作業的優化。

處理器可以使用取得、釋放和隔離語義來支援記憶體障礙的指示。 這些語義會描述作業的結果可供使用的順序。 使用取得語義時，作業的結果會在程式碼中出現的任何作業結果之前提供。 使用發行語義時，作業的結果會在程式碼中出現的任何作業結果之後使用。 範圍語義結合了取得和發行的語法。 具有範圍語義之作業的結果，可以在程式碼中出現的任何作業之前，以及在它之前出現的任何作業之後使用。

在支援 SSE2 的 x86 和 x64 處理器上，這些指示 **mfence** (記憶體隔離) 、 **lfence** (負載隔離) ，以及 **sfence** (存放區隔離) 。 在 ARM 處理器上，instrutions 是 **.dmb** 和 **dsb**。 如需詳細資訊，請參閱處理器的檔。

下列同步處理函式會使用適當的阻礙來確保記憶體順序：

-   輸入或離開重要區段的函式
-   取得或釋放 SRW 鎖定的函式
-   一次性初始化開始和完成
-   **EnterSynchronizationBarrier** 函式
-   信號同步處理物件的函數
-   Wait 函式
-   連鎖函式 (除了具有 _NoFence_ 尾碼的函式之外，或具有 _\_ nf-e_ 尾碼的內建函式) 

## <a name="fixing-a-race-condition"></a>修正競爭條件

下列程式碼在多處理器系統上有競爭條件，因為 `CacheComputedValue` 第一次執行的處理器可能會在 `fValueHasBeenComputed` 寫入主儲存體之前寫入主儲存體 `iValue` 。 因此，在同一時間執行的第二個處理器 `FetchComputedValue` `fValueHasBeenComputed` 會讀取為 **TRUE**，但的新值 `iValue` 仍在第一個處理器的快取中，而且尚未寫入記憶體。

``` syntax
int iValue;
BOOL fValueHasBeenComputed = FALSE;
extern int ComputeValue();

void CacheComputedValue()
{
  if (!fValueHasBeenComputed) 
  {
    iValue = ComputeValue();
    fValueHasBeenComputed = TRUE;
  }
}
 
BOOL FetchComputedValue(int *piResult)
{
  if (fValueHasBeenComputed) 
  {
    *piResult = iValue;
    return TRUE;
  } 

  else return FALSE;
}
```

您可以使用 **volatile** 關鍵字或 [**InterlockedExchange**](/windows/desktop/api/winnt/nf-winnt-interlockedexchange.md) 函數來修復上述的這個競爭條件，以確保的值在 `iValue` `fValueHasBeenComputed` 設定為 **TRUE** 之前，所有處理器的值都已更新。

從 Visual Studio 2005 開始，如果在 **/volatile： ms** 模式中進行編譯，則編譯器會針對 **volatile** 變數使用取得語義，並針對 **volatile** 變數進行寫入作業的發行語義，在 CPU) 支援時 (。 因此，您可以更正此範例，如下所示：

``` syntax
volatile int iValue;
volatile BOOL fValueHasBeenComputed = FALSE;
extern int ComputeValue();

void CacheComputedValue()
{
  if (!fValueHasBeenComputed) 
  {
    iValue = ComputeValue();
    fValueHasBeenComputed = TRUE;
  }
}
 
BOOL FetchComputedValue(int *piResult)
{
  if (fValueHasBeenComputed) 
  {
    *piResult = iValue;
    return TRUE;
  } 

  else return FALSE;
}
```

使用 Visual Studio 2003 時， **volatile** 至 **volatile** 參考會被排序;編譯器不會重新排序 **volatile** 變數存取。 不過，這些作業可能會由處理器重新排序。 因此，您可以更正此範例，如下所示：

``` syntax
int iValue;
BOOL fValueHasBeenComputed = FALSE;
extern int ComputeValue();

void CacheComputedValue()
{
  if (InterlockedCompareExchange((LONG*)&fValueHasBeenComputed, 
          FALSE, FALSE)==FALSE) 
  {
    InterlockedExchange ((LONG*)&iValue, (LONG)ComputeValue());
    InterlockedExchange ((LONG*)&fValueHasBeenComputed, TRUE);
  }
}
 
BOOL FetchComputedValue(int *piResult)
{
  if (InterlockedCompareExchange((LONG*)&fValueHasBeenComputed, 
          TRUE, TRUE)==TRUE) 
  {
    InterlockedExchange((LONG*)piResult, (LONG)iValue);
    return TRUE;
  } 

  else return FALSE;
}
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[重要區段物件](critical-section-objects.md)
</dt> <dt>

[連鎖變數存取](interlocked-variable-access.md)
</dt> <dt>

[Wait 函式](wait-functions.md)
</dt> </dl>

 

 



