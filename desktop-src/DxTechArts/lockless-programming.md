---
title: Xbox 360 和 Microsoft Windows 的 Lockless 程式設計考量
description: 本文概述在嘗試使用 lockless 的程式設計技術時，應考慮的一些問題。
ms.assetid: 44700352-a791-7ef7-0858-146214b0e3da
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23bf8d66cada8aff00735fe6d6ac2d4f1369bc32
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/21/2020
ms.locfileid: "103933712"
---
# <a name="lockless-programming-considerations-for-xbox-360-and-microsoft-windows"></a>Xbox 360 和 Microsoft Windows 的 Lockless 程式設計考量

Lockless 程式設計是在多個執行緒之間安全共用變更資料的一種方式，而不需要取得和釋放鎖定的成本。 這聽起來像是萬靈丹，但是 lockless 程式設計很複雜而且很微妙，有時也不會提供它所保證的優點。 Lockless 程式設計在 Xbox 360 上特別複雜。

Lockless 程式設計是一種適用于多執行緒程式設計的有效技術，但不應輕量使用。 在使用它之前，您必須先瞭解複雜性，而且應該謹慎地進行測量，以確定它確實提供您預期的提升。 在許多情況下，有更簡單且更快速的解決方案，例如較不頻繁地共用資料，應該改用。

正確且安全地使用 lockless 程式設計需要對硬體和編譯器有很大的瞭解。 本文概述在嘗試使用 lockless 的程式設計技術時，應考慮的一些問題。

## <a name="programming-with-locks"></a>使用鎖定進行程式設計

撰寫多執行緒程式碼時，通常必須線上程之間共用資料。 如果有多個執行緒同時讀取和寫入共用資料結構，可能會發生記憶體損毀。 解決此問題最簡單的方法是使用鎖定。 比方說，如果 ManipulateSharedData 一次只能由一個執行緒執行，則 \_ 可以使用重要區段來保證這一點，如下列程式碼所示：

``` syntax
// Initialize
CRITICAL_SECTION cs;
InitializeCriticalSection(&cs);

// Use
void ManipulateSharedData()
{
    EnterCriticalSection(&cs);
    // Manipulate stuff...
    LeaveCriticalSection(&cs);
}

// Destroy
DeleteCriticalSection(&cs);
```

這段程式碼相當簡單簡單明瞭，很容易就能看出它是正確的。 不過，使用鎖定進行程式設計有幾個可能的缺點。 例如，如果兩個執行緒嘗試取得相同的兩個鎖定，但以不同的順序取得它們，您可能會收到鎖死。 如果程式的鎖定時間太長（因為設計不佳）或執行緒已由較高優先順序的執行緒交換，則可能會有很長的時間封鎖其他執行緒。 這項風險特別適用于 Xbox 360，因為軟體執行緒是由開發人員指派硬體執行緒，而作業系統不會將它們移至另一個硬體執行緒，即使某個執行緒閒置也一樣。 Xbox 360 也不會對優先順序反轉進行保護，其中高優先順序的執行緒會在等候低優先順序的執行緒釋放鎖定時，在迴圈中旋轉。 最後，如果延遲程序呼叫或插斷服務常式嘗試取得鎖定，您可能會收到鎖死。

儘管有這些問題，同步處理原始物件（例如重要區段）通常是協調多個執行緒的最佳方式。 如果同步處理原始物件的速度太慢，最好的解決方案通常較不常使用。 不過，對於可以承受額外複雜性的人，另一個選項是 lockless 程式設計。

## <a name="lockless-programming"></a>Lockless 程式設計

顧名思義，Lockless 程式設計是一系列的技術，可安全地操控共用資料，而不需要使用鎖定。 有 lockless 演算法可用於傳遞訊息、共用清單和資料佇列，以及其他工作。

進行 lockless 程式設計時，您必須處理兩個挑戰：非不可部分完成的作業和重新排列。

## <a name="non-atomic-operations"></a>不可部分完成的作業

不可部分完成的作業是一種不可分割，也就是在執行一半時，其他執行緒保證永遠不會看到作業。 不可部分完成的作業對 lockless 程式設計很重要，因為如果沒有這些作業，其他執行緒可能會看到半寫入值，或狀態不一致。

在所有新式處理器上，您可以假設自然對齊原生類型的讀取和寫入是不可部分完成的。 只要記憶體匯流排的寬度至少與所讀取或寫入的類型相同，CPU 就會在單一總線交易中讀取並寫入這些類型，讓其他執行緒無法以半完成狀態來查看它們。 在 x86 和 x64 上，無法保證大於8個位元組的讀取和寫入都是不可部分完成的。 這表示以16位元組的方式讀取和寫入串流 SIMD 延伸模組 (SSE) 暫存器和字串作業，可能不是不可部分完成的。

未自然對齊的類型（例如，寫入跨四位元組界限的 Dword）的讀取和寫入不保證是不可部分完成的。 CPU 可能必須以多個匯流排交易的形式來進行這些讀取和寫入作業，這可能會讓另一個執行緒在讀取或寫入的中間修改或查看資料。

複合作業（例如在遞增共用變數時所發生的讀寫寫入順序）不是不可部分完成的。 在 Xbox 360 中，這些作業會實作為多個指示 (lwz、addi 和 stw) ，而執行緒可以透過序列交換中途。 在 x86 和 x64 上，有單一的指令 (inc) 可用來遞增記憶體中的變數。 如果您使用此指令，則在單處理器系統上遞增變數是不可部分完成的，但在多處理器系統上仍然是不可部分完成的。 在 x86 和 x64 型的多處理器系統上讓 inc. 不可部分完成，需要使用鎖定前置詞，以防止另一個處理器在 inc 指令的讀取和寫入之間進行讀取-修改-寫入順序。

下列程式碼提供了一些範例：

``` syntax
// This write is not atomic because it is not natively aligned.
DWORD* pData = (DWORD*)(pChar + 1);
*pData = 0;

// This is not atomic because it is three separate operations.
++g_globalCounter;

// This write is atomic.
g_alignedGlobal = 0;

// This read is atomic.
DWORD local = g_alignedGlobal;
```

## <a name="guaranteeing-atomicity"></a>保證不可部分完成性

您可以透過下列組合，確定您使用的是不可部分完成的作業：

-   自然不可部分完成的作業
-   用來包裝複合作業的鎖定
-   執行常用複合作業之不可部分完成版本的作業系統函式

遞增變數不是不可部分完成的作業，而且如果在多個執行緒上執行，則遞增可能會導致資料損毀。

``` syntax
// This will be atomic.
g_globalCounter = 0;

// This is not atomic and gives undefined behavior
// if executed on multiple threads
++g_globalCounter;
```

Win32 隨附一系列的函式，可為數個常見作業提供不可部分完成的讀寫版本。 這些是 InterlockedXxx 系列的函式。 如果共用變數的所有修改都使用這些函數，則修改將會是安全線程。

``` syntax
// Incrementing our variable in a safe lockless way.
InterlockedIncrement(&g_globalCounter);
```

## <a name="reordering"></a>重組

重新排列更微妙的問題。 讀取和寫入不一定會按照您在程式碼中撰寫它們的順序來進行，而這可能會導致令人混淆的問題。 在許多多執行緒演算法中，執行緒會寫入一些資料，然後寫入旗標，告知其他執行緒資料已就緒。 這就是所謂的寫入發行。 如果寫入已重新排序，其他執行緒可能會看到旗標已設定，然後才可以看到寫入的資料。

同樣地，在許多情況下，執行緒會從旗標讀取，然後在旗標指出執行緒已取得共用資料的存取權時，讀取一些共用資料。 這稱為「讀取取得」。 如果已重新排序讀取，則可能會在旗標之前從共用儲存區讀取資料，而且所見的值可能不是最新狀態。

編譯器和處理器都可以完成讀取和寫入的重新排列。 編譯器和處理器已完成這幾年的重新排列，但在單處理器電腦上，這不是問題。 這是因為單處理器電腦上的讀取和寫入的 CPU 重新排列，在不屬於設備磁碟機) 一部分的非設備磁碟機程式碼 (中不可見，而且讀取和寫入的編譯器重新排列不太可能會在單處理器電腦上造成問題。

如果編譯器或 CPU 重新排列下列程式碼中所示的寫入，另一個執行緒可能會看到已設定作用旗標，但仍看到 x 或 y 的舊值。 讀取時可能會發生類似的重新排列。

在此程式碼中，一個執行緒會將新的專案新增至 sprite 陣列：

``` syntax
// Create a new sprite by writing its position into an empty
// entry and then setting the ‘alive' flag. If ‘alive' is
// written before x or y then errors may occur.
g_sprites[nextSprite].x = x;
g_sprites[nextSprite].y = y;
g_sprites[nextSprite].alive = true;
```

在下一個程式碼區塊中，另一個執行緒會從 sprite 陣列讀取：

``` syntax
// Draw all sprites. If the reads of x and y are moved ahead of
// the read of ‘alive' then errors may occur.
for( int i = 0; i < numSprites; ++i )
{
    if( g_sprites[nextSprite].alive )
    {
        DrawSprite( g_sprites[nextSprite].x,
                g_sprites[nextSprite].y );
    }
}
```

為了讓這個 sprite 系統的安全，我們需要防止編譯器和 CPU 重新排序讀取和寫入。

### <a name="understanding-cpu-rearrangement-of-writes"></a>瞭解寫入的 CPU 重新排列

某些 Cpu 會重新排列寫入，讓其他處理器或裝置以非程式順序對它們進行外部顯示。 單一執行緒的非驅動程式程式碼看不到這項重新排列功能，但是在多執行緒程式碼中可能會造成問題。

### <a name="xbox-360"></a>Xbox 360

雖然 Xbox 360 的 CPU 不會重新排序指令，但它會重新排列寫入作業，這會在指示本身之後完成。 這項寫入重新排列是由 PowerPC 記憶體模型明確允許。

Xbox 360 上的寫入不會直接移至 L2 快取。 相反地，若要改善 L2 快取寫入頻寬，則會經歷存放區佇列，然後再流覽至存放區集合的緩衝區。 存放區收集緩衝區可在一項作業中，將64位元組區塊寫入 L2 快取中。 有八個存放區收集的緩衝區，可有效率地寫入數個不同的記憶體區域。

存放區收集緩衝區通常會以先進先出的 (FIFO) 順序寫入 L2 快取中。 但是，如果寫入的目標快取行不在 L2 快取中，則在從記憶體提取快取行時，可能會延遲寫入。

即使以嚴格的 FIFO 順序將商店收集的緩衝區寫入 L2 快取，但這並不保證會依序將個別寫入寫入 L2 快取中。 比方說，假設 CPU 寫入至位置0x1000，然後到位置0x2000，再到位置0x1004。 第一個寫入會配置存放區收集緩衝區，並將其放在佇列的前方。 第二個寫入會配置另一個存放區收集緩衝區，並將它放在佇列中的下一個。 第三個寫入會將其資料新增至第一個存放區收集的緩衝區，這會保留在佇列的前端。 因此，第三個寫入最後會在第二次寫入之前進入 L2 快取。

存放區收集緩衝區所造成的重新排列原因基本上是無法預期的，特別是因為核心上的兩個執行緒共用存放區收集的緩衝區，讓存放區集合的配置和清空變得非常不定。

這是如何重新排序寫入的其中一個範例。 可能還有其他可能性。

### <a name="x86-and-x64"></a>x86 和 x64

即使 x86 和 x64 Cpu 會重新排序指令，但它們通常不會重新排列寫入作業相對於其他寫入的順序。 寫入合併記憶體有一些例外狀況。 此外，字串作業 (MOVS 和 STOS) 和16位元組的 SSE 寫入可在內部重新排列，但是不會重新排序寫入。

### <a name="understanding-cpu-rearrangement-of-reads"></a>瞭解讀取的 CPU 重新排列

某些 Cpu 會重新排列讀取，如此它們就能以非程式順序從共用儲存區來進行。 單一執行緒的非驅動程式程式碼看不到這項重新排列，但可能會在多執行緒程式碼中造成問題。

### <a name="xbox-360"></a>Xbox 360

快取遺漏可能會導致某些讀取延遲，這會有效地導致讀取不按照順序來自共用的記憶體，而這些快取遺漏的時間根本是無法預期的。 預先提取和分支預測也可能會導致資料從共用記憶體中不按照順序。 這些只是幾個範例，說明如何將讀取重新排序。 可能還有其他可能性。 PowerPC 記憶體模型特別允許這項讀取重新排列。

### <a name="x86-and-x64"></a>x86 和 x64

即使 x86 和 x64 Cpu 會重新排序指令，但它們通常不會將讀取作業重新排序為與其他讀取相關。 字串作業 (MOVS 和 STOS) 和16位元組的 SSE 讀取可以在內部重新排序，但是讀取不會重新排序。

### <a name="other-reordering"></a>其他重新排列

即使 x86 和 x64 Cpu 不會重新排列寫入相對於其他寫入的順序，或重新排列讀取相對於其他讀取的順序，它們也可以重新排列相對於寫入的讀取順序。 具體來說，如果程式寫入至某個位置，然後從不同的位置讀取，則讀取資料可能會在寫入的資料變成該處之前來自共用記憶體。 重新排列可能會中斷某些演算法，例如 Dekker 的相互排除演算法。 在 Dekker 的演算法中，每個執行緒都會設定一個旗標，表示它想要輸入重要區域，然後檢查另一個執行緒的旗標，以查看其他執行緒是否位於關鍵區域或嘗試輸入它。 初始程式碼如下所示。

``` syntax
volatile bool f0 = false;
volatile bool f1 = false;

void P0Acquire()
{
    // Indicate intention to enter critical region
    f0 = true;
    // Check for other thread in or entering critical region
    while (f1)
    {
        // Handle contention.
    }
    // critical region
    ...
}


void P1Acquire()
{
    // Indicate intention to enter critical region
    f1 = true;
    // Check for other thread in or entering critical region
    while (f0)
    {
        // Handle contention.
    }
    // critical region
    ...
}
```

問題在於，P0Acquire 中的 f1 讀取可以在寫入 f0 使其成為共用儲存體之前讀取共用存放裝置。 同時，P1Acquire 中的 f0 讀取可以先從共用存放裝置讀取，然後再寫入至 f1，使其成為共用存放裝置。 最後的結果就是兩個執行緒都會將其旗標設定為 TRUE，而這兩個執行緒都會將另一個執行緒的旗標視為 FALSE，因此兩者都輸入重要區域。 因此，雖然在 x86 和 x64 型系統上重新排序的問題，在 Xbox 360 上並不常見，但仍有可能發生這種情況。 在這些平臺上，Dekker 的演算法將無法運作，而不會有硬體記憶體阻礙。

x86 和 x64 Cpu 將不會重新排序先前讀取之前的寫入。 x86 和 x64 Cpu 只會在以不同的位置為目標時，重新排序先前寫入之前的讀取。

PowerPC Cpu 可以在寫入之前重新排列讀取的順序，並可在讀取前重新排序寫入，只要它們是不同的位址即可。

### <a name="reordering-summary"></a>重新排列摘要

Xbox 360 的 CPU 比起 x86 和 x64 Cpu 更積極地重新排序記憶體作業，如下表所示。 如需詳細資訊，請參閱處理器檔。



| 重新排列活動           | x86 和 x64 | Xbox 360 |
|-------------------------------|-------------|----------|
| 讀取在讀取前移動   | 否          | 是      |
| 寫入在寫入之前移動 | 否          | 是      |
| 寫入在讀取前移動  | 否          | 是      |
| 讀取在寫入之前移動  | 是         | 是      |



 

## <a name="read-acquire-and-write-release-barriers"></a>Read-Acquire 和 Write-Release 阻礙

用來防止讀取和寫入重新排序的主要結構稱為讀取取得和寫入釋放屏障。 「讀取取得」是讀取旗標或其他變數以取得資源的擁有權，並結合了屏障以進行重新排序。 同樣地，寫入版本是一個旗標或其他變數的寫入，以提供資源的擁有權，並與阻礙重新排序。

Herb Sutter 的正式定義如下：

-   讀取器會在依照程式順序追蹤的相同執行緒上執行之前的所有讀取和寫入之前執行。
-   寫入發行會在程式順序中的相同執行緒之前的所有讀取和寫入之後執行。

當您的程式碼取得某些記憶體的擁有權時，可能是藉由取得鎖定，或從共用連結清單中提取專案， (沒有鎖定) 的情況下，一律會有相關的讀取-測試旗標或指標，以查看是否已取得記憶體的擁有權。 這項讀取可能是 **InterlockedXxx** 作業的一部分，在這種情況下，它牽涉到讀取和寫入，但它是指出是否已取得擁有權的讀取。 取得記憶體的擁有權之後，通常會從記憶體讀取或寫入值，而且在取得擁有權之後，這些讀取和寫入都必須執行。 讀取取得關卡可保證這一點。

當部分記憶體的擁有權釋出（藉由釋放鎖定或將專案推送至共用連結清單）時，一律會產生寫入，以通知其他執行緒現在可使用記憶體。 雖然您的程式碼具有記憶體的擁有權，但它可能會對其進行讀取或寫入，因此在釋放擁有權之前，這些讀取和寫入都必須先執行。 寫入發行關卡可保證這一點。

最簡單的方式是將讀取取得和寫入發行的屏障視為單一作業。 不過，有時必須從兩個部分進行建立：讀取或寫入，以及不允許讀取或寫入在其上移動的屏障。 在此情況下，屏障的位置非常重要。 針對讀取取得關卡，旗標的讀取會先出現，然後是屏障，然後讀取和寫入共用資料。 針對寫入發行關卡，共用資料的讀取和寫入會先出現，然後是屏障，然後寫入旗標。

``` syntax
// Read that acquires the data.
if( g_flag )
{
    // Guarantee that the read of the flag executes before
    // all reads and writes that follow in program order.
    BarrierOfSomeSort();

    // Now we can read and write the shared data.
    int localVariable = sharedData.y;
    sharedData.x = 0;

    // Guarantee that the write to the flag executes after all
    // reads and writes that precede it in program order.
    BarrierOfSomeSort();
    
    // Write that releases the data.
    g_flag = false;
}
```

讀取取得和寫入發行之間的唯一差異在於記憶體屏障的位置。 讀取取得會在鎖定作業之後具有關卡，而寫入版本則具有關卡。 在這兩種情況下，屏障都介於鎖定記憶體的參考與鎖定的參考之間。

若要瞭解在取得和釋出資料時，為什麼需要阻礙，最好是最好的 (以及最準確的) 將這些阻礙視為可保證與共享記憶體的同步處理，而不是其他處理器。 如果有一個處理器使用寫入發行將資料結構釋出至共用記憶體，而另一個處理器使用讀取取得來從共用記憶體存取該資料結構，則程式碼會正常運作。 如果其中一種處理器未使用適當的關卡，資料共用可能會失敗。

使用適當的關卡來防止編譯器和您的平臺重新調整 CPU 的關鍵。

使用作業系統所提供的同步處理原始物件的優點之一，就是它們都包含適當的記憶體阻礙。

## <a name="preventing-compiler-reordering"></a>防止編譯器重新排列

編譯器的工作是將您的程式碼積極地優化，以便改善效能。 這包括重新排列指示的位置，以及不會變更行為的位置。 因為 c + + 標準絕對不會提及多執行緒，而且因為編譯器不知道哪些程式碼必須是安全線程，所以編譯器會假設您的程式碼在決定可安全重排所以的情況下，會有單一執行緒。 因此，當不允許編譯器重新排序讀取和寫入時，您需要告訴編譯器。

使用 Visual C++ 您可以使用編譯器內建 [**\_ ReadWriteBarrier**](https://msdn.microsoft.com/library/f20w0x5e(v=VS.71).aspx)，以防止編譯器重新排列。 當您在程式碼中插入 **\_ ReadWriteBarrier** 時，編譯器不會在其上移動讀取和寫入。

``` syntax
#if _MSC_VER < 1400
    // With VC++ 2003 you need to declare _ReadWriteBarrier
    extern "C" void _ReadWriteBarrier();
#else
    // With VC++ 2005 you can get the declaration from intrin.h
#include <intrin.h>
#endif
// Tell the compiler that this is an intrinsic, not a function.
#pragma intrinsic(_ReadWriteBarrier)

// Create a new sprite by filling in a previously empty entry.
g_sprites[nextSprite].x = x;
g_sprites[nextSprite].y = y;
// Write-release, barrier followed by write.
// Guarantee that the compiler leaves the write to the flag
// after all reads and writes that precede it in program order.
_ReadWriteBarrier();
g_sprites[nextSprite].alive = true;
```

在下列程式碼中，另一個執行緒會從 sprite 陣列讀取：

``` syntax
// Draw all sprites.
for( int i = 0; i < numSprites; ++i )
{

    // Read-acquire, read followed by barrier.
    if( g_sprites[nextSprite].alive )
    {
    
        // Guarantee that the compiler leaves the read of the flag
        // before all reads and writes that follow in program order.
        _ReadWriteBarrier();
        DrawSprite( g_sprites[nextSprite].x,
                g_sprites[nextSprite].y );
    }
}
```

請務必瞭解， [**\_ ReadWriteBarrier**](https://msdn.microsoft.com/library/f20w0x5e(v=VS.71).aspx)不會插入任何額外的指示，也不會防止 CPU 重新排列讀取和寫入，它只會防止編譯器重新排列讀取和寫入。 因此，當您在 x86 和 x64 (上實行寫入發行屏障時， **\_ ReadWriteBarrier** 便已足夠，因為 x86 和 x64 不會重新排列寫入的順序，而一般寫入足以釋出鎖定) ，但在大部分的情況下，也必須防止 CPU 重新排序讀取和寫入。

當您寫入至無法快取的寫入組合記憶體時，也可以使用 [**\_ ReadWriteBarrier**](https://msdn.microsoft.com/library/f20w0x5e(v=VS.71).aspx) ，以防止寫入重新排序。 在此情況下， **\_ ReadWriteBarrier** 藉由保證寫入會以處理器的慣用線性順序進行，有助於改善效能。

您也可以使用 [**\_ ReadBarrier**](https://msdn.microsoft.com/library/z055s48f(v=VS.80).aspx)和 [**\_ WriteBarrier**](https://msdn.microsoft.com/library/65tt87y8(v=VS.80).aspx)內建函式來更精確地控制編譯器重新排列。 編譯器不會跨 **\_ ReadBarrier** 移動讀取，且不會在 **\_ WriteBarrier** 之間移動寫入。

## <a name="preventing-cpu-reordering"></a>防止 CPU 重新排序

重新調整 CPU 比編譯器重新排列更為微妙。 您看不到直接發生的情況，只是看到 inexplicable 的錯誤。 為了防止 CPU 重新排序讀取和寫入，您必須在某些處理器上使用記憶體屏障指令。 Xbox 360 和 Windows 上的記憶體屏障指令的所有用途名稱都是 [**system.threading.thread.memorybarrier**](/windows/win32/api/winnt/nf-winnt-memorybarrier)。 此宏會針對每個平臺適當地執行。

在 Xbox 360 上， [**system.threading.thread.memorybarrier**](/windows/win32/api/winnt/nf-winnt-memorybarrier)定義為 **lwsync** (輕量同步) ，也可透過 **\_ \_ lwsync** 內建（定義于 ppcintrinsics 中）來使用。 **\_ \_ lwsync** 也可作為編譯器記憶體屏障，以防止編譯器重新排列讀取和寫入。

**Lwsync** 指令是 Xbox 360 上的記憶體屏障，可同步處理一個處理器核心與 L2 快取。 它可確保在 **lwsync** 之前的所有寫入都先將其寫入至 L2 快取，然後再執行任何寫入。 它也可保證遵循 **lwsync** 的任何讀取，都不會從 L2 取得比先前讀取更舊的資料。 它不會防止的一種重新排列類型，就是在寫入至不同位址之前讀取的移動。 因此， **lwsync** 會強制執行符合 x86 和 x64 處理器上預設記憶體順序的記憶體順序。 若要取得完整的記憶體順序，需要較昂貴的同步指令 (也稱為重量級同步) ，但在大部分情況下，則不需要這麼做。 下表顯示 Xbox 360 上的記憶體重新排列選項。



| 重新排列 Xbox 360           | 無同步處理 | lwsync | sync |
|-------------------------------|---------|--------|------|
| 讀取在讀取前移動   | 是     | 否     | 否   |
| 寫入在寫入之前移動 | 是     | 否     | 否   |
| 寫入在讀取前移動  | 是     | 否     | 否   |
| 讀取在寫入之前移動  | 是     | 是    | 否   |



 

PowerPC 也有同步處理指示 **isync** 和 **eieio** (，可用來控制重新排列至快取-抑制記憶體) 。 一般同步處理用途不需要這些同步處理指示。

在 Windows 上， [**system.threading.thread.memorybarrier**](/windows/win32/api/winnt/nf-winnt-memorybarrier) 是在 Winnt 中定義，並根據您要針對 x86 或 x64 編譯而提供不同的記憶體屏障指令。 記憶體關卡指令可做為完整的關卡，防止所有屏障的讀取和寫入重新排列。 因此，Windows 上的 **system.threading.thread.memorybarrier** 提供比 Xbox 360 更強的重新排序保證。

在 Xbox 360 以及許多其他 Cpu 上，都有一種額外的方式可以防止 CPU 進行讀取重新排列。 如果您讀取指標，然後使用該指標載入其他資料，CPU 可保證讀取指標的次數不會比讀取指標還舊。 如果您的鎖定旗標是指標，且共用資料的所有讀取都不是指標，則可以省略 [**system.threading.thread.memorybarrier**](/windows/win32/api/winnt/nf-winnt-memorybarrier) ，以節省適度的效能。

``` syntax
Data* localPointer = g_sharedPointer;
if( localPointer )
{
    // No import barrier is needed--all reads off of localPointer
    // are guaranteed to not be reordered past the read of
    // localPointer.
    int localVariable = localPointer->y;
    // A memory barrier is needed to stop the read of g_global
    // from being speculatively moved ahead of the read of
    // g_sharedPointer.
    int localVariable2 = g_global;
}
```

[**System.threading.thread.memorybarrier**](/windows/win32/api/winnt/nf-winnt-memorybarrier)指令只會防止將讀取和寫入重新排序為可快取的記憶體。 如果您將記憶體配置為頁面 \_ NOCACHE 或頁面 \_ WRITECOMBINE，則裝置驅動程式作者和遊戲開發人員在 Xbox 360 上的常見技術， **system.threading.thread.memorybarrier** 不會影響此記憶體的存取。 大部分的開發人員都不需要同步處理無法快取的記憶體。 這已超出本文的範圍。

## <a name="interlocked-functions-and-cpu-reordering"></a>連鎖函數和 CPU 重新排列

有時會使用其中一個 **InterlockedXxx** 函數來取得或釋放資源的讀取或寫入。 在 Windows 中，這可簡化專案;因為在 Windows 上， **InterlockedXxx** 函式都是完全記憶體的阻礙。 它們在前後都有一個 CPU 記憶體屏障，這表示它們本身是完整的讀取或寫入發行關卡。

在 Xbox 360 上， **InterlockedXxx** 函數不會包含 CPU 記憶體阻礙。 它們可防止編譯器重新排序讀取和寫入，而不會重新排列 CPU。 因此，在大部分情況下，在 Xbox 360 上使用 **InterlockedXxx** 函式時，您應該在其前面或後面加上 **\_ \_ lwsync**，使其成為讀取或寫入發行關卡。 為了方便起見，而且更容易閱讀，有許多 **InterlockedXxx** 函式的 **取得** 和 **發行** 版。 這些都有內建的記憶體屏障。 例如， [**InterlockedIncrementAcquire**](/previous-versions/windows/desktop/legacy/ms683618(v=vs.85))會執行連鎖的遞增，後面接著 **\_ \_ lwsync** 的記憶體屏障，以提供完整的讀取取得功能。

建議您使用 **InterlockedXxx** 函式的 **取得** 和 **發行** 版 (大多數都可在 Windows 上使用，但不會對效能造成負面影響) 讓您的意圖更加明顯，並讓您更輕鬆地在正確的位置取得記憶體關卡指令。 在 Xbox 360 上使用 **InterlockedXxx** 時，若沒有記憶體屏障，則應謹慎檢查，因為這通常是錯誤。

這個範例會示範一個執行緒如何使用 **InterlockedXxxSList** 函式的 **取得** 和 **發行** 版，將工作或其他資料傳遞到另一個執行緒。 **InterlockedXxxSList** 函式是一系列的函式，用來維護共用的單向連結清單，而不需要鎖定。 請注意，這些函式的 **取得** 和 **版本** 變體在 windows 上無法使用，但這些函式的一般版本是 windows 上的完整記憶體屏障。

``` syntax
// Declarations for the Task class go here.

// Add a new task to the list using lockless programming.
void AddTask( DWORD ID, DWORD data )
{
    Task* newItem = new Task( ID, data );
    InterlockedPushEntrySListRelease( g_taskList, newItem );
}

// Remove a task from the list, using lockless programming.
// This will return NULL if there are no items in the list.
Task* GetTask()
{
    Task* result = (Task*)
        InterlockedPopEntrySListAcquire( g_taskList );
    return result;
}
```

## <a name="volatile-variables-and-reordering"></a>Volatile 變數和重新排列

C + + 標準指出無法快取 volatile 變數的讀取、volatile 寫入無法延遲，而且無法將變動性讀取和寫入移到彼此的之後。 這就足以與硬體裝置進行通訊，這是 c + + 標準中 volatile 關鍵字的用途。

但是，標準的保證並不足以針對多執行緒使用 volatile。 C + + 標準不會阻止編譯器重新排列相對於 volatile 讀取和寫入的非暫時性讀取和寫入，且不會顯示任何關於防止重新調整 CPU 的資訊。

Visual C++ 2005 超越標準 c + +，以針對 volatile 變數存取定義多執行緒易懂的語法。 從 Visual C++ 2005 開始，會將 volatile 變數的讀取定義為具有讀取取得的語法，而 volatile 變數的寫入則定義為具有寫入發行語義。 這表示編譯器將不會重新排列任何超出它們的讀取和寫入，而在 Windows 上，則會確保 CPU 不會執行這項作業。

請務必瞭解這些新的保證只適用于 Visual C++ 2005 和未來版本的 Visual C++。 其他廠商的編譯器通常會執行不同的語法，而不會有 Visual C++ 2005 的額外保證。 此外，在 Xbox 360 上，編譯器不會插入任何指示，以防止 CPU 重新排序讀取和寫入。

## <a name="example-of-a-lock-free-data-pipe"></a>Lock-Free 資料管道的範例

管道是一種結構，可讓一個或多個執行緒寫入資料，然後由其他執行緒讀取。 管道的 lockless 版本可以是一種簡潔且有效率的方式，將工作從執行緒傳遞給執行緒。 DirectX SDK 提供 **LockFreePipe**，這是可在 DXUTLockFreePipe 中使用的單一讀取器、單一寫入器 lockless 管道。 相同的 **LockFreePipe** 可在 AtgLockFreePipe 的 Xbox 360 SDK 中使用。

當兩個執行緒有生產者/取用者關聯性時，可以使用 **LockFreePipe** 。 生產者執行緒可以將資料寫入管道，讓取用者執行緒在日後進行處理，而不會遭到封鎖。 如果管道填滿，寫入會失敗，而生產者執行緒必須稍後再試一次，但只有在產生生產者執行緒時，才會發生這種情況。 如果管道清空，讀取會失敗，而取用者執行緒將必須稍後再試一次，但只有在沒有工作可供取用者執行緒執行時，才會發生這種情況。 如果兩個執行緒都是妥善平衡的，且管道夠大，管道可讓它們順暢地傳遞資料，而不會有延遲或區塊。

## <a name="xbox-360-performance"></a>Xbox 360 效能

Xbox 360 上的同步處理指示和函式的效能，會隨著其他程式碼的執行而有所不同。 如果另一個執行緒目前擁有鎖定，取得鎖定將需要更長的時間。 如果有其他執行緒寫入相同的快取行， [**InterlockedIncrement**](/windows/win32/api/winnt/nf-winnt-interlockedincrement)和重要區段作業將需要更長的時間。 存放區佇列的內容也會影響效能。 因此，所有這些數位只是近似值，從非常簡單的測試產生：

-   **lwsync** 已測量為採用33-48 週期。
-   [**InterlockedIncrement**](/windows/win32/api/winnt/nf-winnt-interlockedincrement) 已測量為採用225-260 週期。
-   取得或釋出重要區段的測量是大約大約345週期。
-   取得或釋放 mutex 的測量是大約大約2350迴圈。

## <a name="windows-performance"></a>Windows 效能

Windows 上的同步處理指示和函式的效能，會隨著處理器類型和設定，以及其他哪些程式碼正在執行而有很大的差異。 多核心和多通訊端系統通常需要較長的時間來執行同步處理指示，而如果另一個執行緒目前擁有鎖定，取得鎖定的時間會更長。

但是，即使是從非常簡單的測試產生的一些測量也很有説明：

-   [**System.threading.thread.memorybarrier**](/windows/win32/api/winnt/nf-winnt-memorybarrier) 已測量為採用20-90 週期。
-   [**InterlockedIncrement**](/windows/win32/api/winnt/nf-winnt-interlockedincrement) 已測量為採用36-90 週期。
-   取得或釋放重要區段的測量是採用40-100 週期。
-   取得或釋放 mutex 的測量是大約大約750-2500 迴圈。

這些測試是在 Windows XP 上的各種不同處理器上完成。 在單處理器電腦上會有較短的時間，而在多處理器電腦上則是較長的時間。

雖然取得和釋放鎖定的成本比使用 lockless 程式設計更高，但更能更頻繁地共用資料，進而避免成本。

## <a name="performance-thoughts"></a>效能想法

取得或釋出重要區段包含記憶體屏障、 **InterlockedXxx** 作業，以及一些額外檢查來處理遞迴，以及切換回 mutex （如有必要）。 您應該要謹慎地實行您自己的重要區段，因為在等候鎖定的迴圈中旋轉（等候鎖定是免費的），而不會回到 mutex，所以會浪費大量的效能。 對於嚴重爭用但未長期保留的重要區段，您應該考慮使用 [**InitializeCriticalSectionAndSpinCount**](/windows/win32/api/synchapi/nf-synchapi-initializecriticalsectionandspincount) ，如此一來，當您嘗試取得重要區段時，作業系統會在等候重要區段的時候旋轉一段時間，而不是立即延遲至 mutex。 為了識別可受益于微調計數的重要區段，您必須測量一般等候特定鎖定的長度。

如果共用堆積用於記憶體配置（預設行為），則每個記憶體配置和免費都需要取得鎖定。 當執行緒的數目和配置數量增加時，效能層級會關閉，且最終會開始減少。 使用每個執行緒堆積或減少配置數目，可避免此鎖定瓶頸。

如果有一個執行緒正在產生資料，而另一個執行緒正在使用資料，它們可能會經常共用資料。 如果有一個執行緒正在載入資源，而另一個執行緒正在轉譯場景，就會發生這種情況。 如果轉譯執行緒參考每個繪製呼叫上的共用資料，則鎖定的額外負荷會很高。 如果每個執行緒都有私用資料結構，然後在每個框架或更短的時間內進行同步處理，則可以實現更好的效能

Lockless 演算法不保證會比使用鎖定的演算法更快。 您應該先查看鎖定是否真的會造成問題，然後再嘗試避免它們，而且您應該測量以查看您的 lockless 程式碼是否真的能改善效能。

## <a name="platform-differences-summary"></a>平臺差異摘要

-   **InterlockedXxx** 函式會防止在 Windows 上重新排列 CPU 的讀取/寫入，而不是 Xbox 360。
-   使用 Visual Studio c + + 2005 讀取和寫入 volatile 變數，可避免在 Windows 上重新排列 CPU 的讀取/寫入，但是在 Xbox 360 上，它只會防止編譯器的讀取/寫入重新排列。
-   寫入會在 Xbox 360 上重新排序，但不會在 x86 或 x64 上重新排序。
-   讀取會在 Xbox 360 上重新排序，但是在 x86 或 x64 上，它們只會重新排列相對於寫入的順序，而且只有在讀取和寫入目標不同位置時才會重新排序。

## <a name="recommendations"></a>建議

-   盡可能使用鎖定，因為它們比較容易使用。
-   避免鎖定太頻繁，因此鎖定成本不會變得很明顯。
-   避免將鎖定保留太久，以避免長時間停止。
-   適當時，請使用 lockless 程式設計，但請確定這些增益會證明複雜度。
-   在禁止其他鎖定的情況下使用 lockless 程式設計或旋轉鎖定，例如在延遲程序呼叫和一般程式碼之間共用資料時。
-   只使用已證明正確的標準 lockless 程式設計演算法。
-   進行 lockless 程式設計時，請務必視需要使用 volatile 旗標變數和記憶體關卡指令。
-   在 Xbox 360 上使用 **InterlockedXxx** 時，請使用 **取得** 和 **釋放** 變異。

## <a name="references"></a>參考資料

-   MSDN Library。 「[**volatile (c + +)**](https://msdn.microsoft.com/library/12a04hfd(v=VS.71).aspx)」。 C + + 語言參考。
-   Vance Morrison。 「[瞭解多執行緒應用程式中 Low-Lock 技術的影響](/archive/msdn-magazine/2005/october/understanding-low-lock-techniques-in-multithreaded-apps)」。 2005年10月的 MSDN 雜誌。
-   Lyons，Michael。 「[PowerPC 儲存體模型與 AIX 程式設計](https://www-128.ibm.com/developerworks/eserver/articles/powerpc.mdl)」。 IBM developerWorks，16 11 月2005日。
-   McKenney，Paul E. "[新式微處理器中的記憶體順序，第二部分](https://www.linuxjournal.com/article/8212)。" Linux 日誌，2005年9月。 \[本文有一些 x86 詳細資料。\]
-   Intel Corporation。 「[Intel®64架構記憶體順序](https://www.cs.cmu.edu/~410-f10/doc/Intel_Reordering_318147.pdf)」。 2007年8月。 \[適用于 IA-32 和 Intel 64 處理器。\]
-   Niebler、Eric。 「[旅程報表： c + + 中線程](https://www.artima.com/cppsource/threads_meeting.html)的臨機操作會議」。 C + + 來源，2006 10 月17日。
-   Hart，Thomas E. 2006。 「[快速進行 Lockless 同步處理：記憶體回收的效能影響](https://www.cs.toronto.edu/~tomhart/papers/hart_ipdps06.pdf)」。 2006國際平行和分散式處理 Symposium (IPDPS 2006) 、Rhodes 島、希臘、4月2006。

 

 