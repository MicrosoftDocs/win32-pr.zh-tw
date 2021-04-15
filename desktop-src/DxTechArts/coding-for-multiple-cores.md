---
title: 在 Xbox 360 和 Windows 上針對多核心撰寫程式碼
description: 本主題提供一些有關如何開始使用多執行緒程式設計的建議。
ms.assetid: 661f13a6-c73d-8513-2bad-0ef9d1a361a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75899dacdfba829fc1a83e9393e6aa58574c9f30
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/21/2020
ms.locfileid: "104383242"
---
# <a name="coding-for-multicore-on-xbox-360-and-windows"></a>在 Xbox 360 和 Windows 上針對多核心撰寫程式碼

多年來，處理器的效能不斷增加，而遊戲和其他程式已 reaped 這種增加的能力，而不需要執行任何特殊動作。

規則已變更。 如果有的話，單處理器核心的效能現在會變得非常緩慢。 不過，一般電腦或主控台中提供的運算能力仍會持續成長。 差別在於，大部分的效能提升現在都是在單一機器中具有多個處理器核心，通常是在單一晶片中。 Xbox 360 CPU 在一個晶片上有三個處理器核心，而2006中所售出的電腦處理器大約70% 是多核心。

可用處理能力的增加與過去一樣明顯，但現在開發人員必須撰寫多執行緒程式碼，才能使用此功能。 多執行緒程式設計帶來了新的設計和程式設計挑戰。 本主題提供一些有關如何開始使用多執行緒程式設計的建議。

## <a name="the-importance-of-good-design"></a>良好設計的重要性

良好的多執行緒程式設計很重要，但可能很困難。 如果您 haphazardly 將主要遊戲系統移至不同的執行緒，您可能會發現每個執行緒的大部分時間都花費在等候其他執行緒。 這種類型的設計會導致複雜性和大量的調試工作變得更複雜，幾乎沒有效能提升。

每次執行緒必須同步處理或共用資料時，就可能會發生資料損毀、同步處理額外負荷、鎖死和複雜度。 因此，您的多執行緒設計需要清楚地記錄每個同步處理和通訊點，而且應該盡可能將這些點最小化。 當執行緒需要進行通訊時，程式碼撰寫工作將會增加，如果影響到太多的原始程式碼，則會降低生產力。

多執行緒的最簡單設計目標是將程式碼分解成大型的獨立片段。 如果您接著將這些部分限制在每個畫面上進行幾次通訊，您就會看到從多執行緒的速度大幅提升，而不會產生過度的複雜性。

## <a name="typical-threaded-tasks"></a>一般執行緒工作

有幾種類型的工作已證明適合要放在不同的執行緒上。 下列清單並非詳盡的，但應該提供一些想法。

### <a name="rendering"></a>轉譯

轉譯（可能包括將場景圖形（可能是只呼叫 D3D 函式）的工作，通常會有50% 或更多 CPU 時間的帳戶。 因此，將轉譯移至另一個執行緒可能會有很大的好處。 Update 執行緒可以填入某種轉譯描述緩衝區，讓轉譯執行緒可以處理它。

遊戲更新執行緒在轉譯執行緒之前一律為一個畫面格，這表示它會在畫面上顯示使用者動作之前，採用兩個畫面格。 雖然這樣的延遲可能會造成問題，但是分割工作負載的成長畫面播放速率通常會讓延遲總計保持可接受。

在大多數情況下，所有轉譯仍會在單一執行緒上進行，但它是與遊戲更新不同的執行緒。

D3DCREATE \_ 多執行緒旗標有時會用來允許在其他執行緒上的單一線程和資源上進行轉譯; 在 Xbox 360 上會忽略此旗標，而您應避免在 Windows 上使用此旗標。 在 Windows 上，指定此旗標會強制 D3D 花很長的時間來同步處理，因此會減緩轉譯執行緒的速度。

### <a name="file-decompression"></a>檔案解壓縮

載入時間一律太長，並將資料串流至記憶體，而不會影響畫面播放速率，可能是一項挑戰。 如果磁片上的所有資料都是主動壓縮的，則硬碟或光碟的資料傳送速率比較不可能是限制因素。 在單一執行緒處理器上，通常沒有足夠的處理器時間可進行壓縮，以協助載入時間。 不過，在多處理器的系統上，檔案解壓縮會使用其他會浪費的 CPU 週期;它可改善載入時間和串流;它會節省光碟上的空間。

請勿使用檔案解壓縮來取代在生產期間應完成的處理。 比方說，如果您在層級載入期間投入額外的執行緒來剖析 XML 資料，您就不會使用多執行緒來改善播放程式的體驗。

使用檔案解壓縮執行緒時，您仍然應該使用非同步檔案 i/o 和大型讀取，以便將資料讀取效率最大化。

### <a name="graphics-fluff"></a>圖形寫錯字

有許多圖形 niceties 可改善遊戲的外觀，但不是絕對必要的。 這些專案包括 cti 所產生的雲端動畫、軟線和線模擬、程式化、程式性植被指數、更多粒子或非遊戲物理。

因為這些效果不會影響遊戲，所以它們不會造成複雜的同步處理問題，它們可以在每個框架或較少的時候與其他執行緒進行同步處理。 此外，在 Windows 遊戲中，這些效果可以為具有多核心 Cpu 的玩家帶來價值，同時在單一核心電腦上以無訊息方式省略，因此可讓您輕鬆地在各種功能之間進行調整。

### <a name="physics"></a>物理特性

物理通常不能放在另一個執行緒上，以與遊戲更新平行執行，因為遊戲更新通常需要立即計算物理計算的結果。 多執行緒物理的替代方案是在多個處理器上執行。 雖然可以完成這項作業，但這是一項複雜的工作，需要經常存取共用資料結構。 如果您可以讓物理工作負載夠低，使其符合主執行緒，您的作業將會比較簡單。

支援在多個執行緒上執行物理的程式庫可供使用。 不過，這可能會導致問題：當您的遊戲在物理上執行時，它會使用許多執行緒，但其餘的時間則不會使用。 在多個執行緒上執行物理將需要定址，如此一來，工作負載就會平均分散在整個框架中。 如果您撰寫多執行緒物理引擎，您必須特別注意所有的資料結構、同步處理點和負載平衡。

## <a name="example-multithreaded-designs"></a>多執行緒設計範例

Windows 遊戲需要在 CPU 核心數目不同的電腦上執行。 大部分的遊戲電腦仍舊只有一個核心，雖然兩核心機器的數目很快就會成長。 Windows 的典型遊戲可能會將其工作負載分成一個執行緒進行更新和轉譯，以及選擇性的背景工作執行緒來新增額外的功能。 此外，也可能會使用一些執行檔案 i/o 和網路的背景執行緒。 [圖 1] 顯示執行緒，以及主要的資料傳輸點。

**圖1。Windows 遊戲中的執行緒設計**

![windows 遊戲中的執行緒設計](images/coding-for-multiple-cores-1.gif)

一般的 Xbox 360 遊戲可以使用額外的 CPU 密集軟體執行緒，因此它可能會將其工作負載分解為更新執行緒、轉譯執行緒和三個背景工作執行緒，如圖2所示。

**[圖 2]Xbox 360 遊戲中的執行緒設計**

![xbox 360 遊戲中的執行緒設計](images/coding-for-multiple-cores-2.gif)

除了檔案 i/o 和網路功能之外，這些工作都有可能耗用大量 CPU，足以受益于自己的硬體執行緒。 這些工作也有可能會有足夠的獨立性，可在不進行通訊的情況下對整個框架執行。

遊戲更新執行緒管理控制器輸入、AI 和物理，並準備其他四個執行緒的指示。 這些指示會放入遊戲更新執行緒所擁有的緩衝區中，因此在產生指示時不需要進行同步處理。

在框架的結尾，遊戲更新執行緒將指令緩衝區交給其他四個執行緒，然後開始處理下一個畫面格，並填入另一組指令緩衝區。

因為更新和轉譯執行緒會彼此密集建置，所以它們的通訊緩衝區只會進行雙重緩衝處理：在任何指定的時間，更新執行緒會在轉譯執行緒從另一個緩衝區讀取時填滿一個緩衝區。

其他背景工作執行緒不一定會與畫面播放速率相關聯。 將資料解壓縮可能會比框架少很多，或可能需要很多的畫面格。 即使是抹布和線的模擬，也可能不需要完全以畫面播放速率執行，因為較不頻繁的更新可能會很容易接受。 因此，這三個執行緒需要不同的資料結構來與更新執行緒和轉譯執行緒通訊。 它們每個都需要可保存工作要求的輸入佇列，而轉譯執行緒需要可保存執行緒所產生之結果的資料佇列。 在每個框架的結尾，更新執行緒會將工作要求區塊新增至背景工作執行緒的佇列。 只要針對每個畫面格加入清單一次，即可確保 update 執行緒能將同步處理額外負荷降到最低。 每個背景工作執行緒都會使用如下所示的迴圈，盡可能快速地從工作佇列提取指派：


```C++
for(;;)
{
    while( WorkQueueNotEmpty() )
    {
        RemoveWorkItemFromWorkQueue();
        ProcessWorkItem();
        PutResultInDataQueue();
    }
    WaitForSingleObject( hWorkSemaphore ); 
}
```



因為資料會從更新執行緒移至背景工作執行緒，然後再到轉譯執行緒，所以在某些動作將它移至螢幕之前，可能會有三個或更多的框架延遲。 但是，如果您將延遲容錯工作指派給背景工作執行緒，這應該不會造成問題。

另一種設計是讓多個背景工作執行緒都從相同的工作佇列中繪製。 這會提供自動負載平衡，讓所有工作者執行緒更有可能保持忙碌。

遊戲更新執行緒必須小心，不要對工作者執行緒提供太多工作，否則工作佇列可能會持續成長。 更新執行緒管理此作業的方式，取決於背景工作執行緒所執行的工作類型。

## <a name="simultaneous-multithreading-and-number-of-threads"></a>同步多執行緒和執行緒數目

所有線程都不會建立相等的。 兩個硬體執行緒可能位於不同晶片、相同晶片或甚至相同核心上。 遊戲程式設計人員要注意的最重要設定是一個核心上的兩個硬體執行緒—同時多執行緒 (SMT) 或 Hyper-Threading 技術 (HT 技術) 。

SMT 或 HT 技術執行緒共用 CPU 核心的資源。 因為它們共用執行單位，所以從執行兩個執行緒而不是一個執行緒的最大速度通常是10到20%，而不是兩個獨立硬體執行緒可能的100%。

更明顯地來說，SMT 或 HT 技術執行緒共用 L1 指令和資料快取。 如果它們的記憶體存取模式不相容，它們可能會在快取上進行對抗，並導致許多快取遺漏。 在最糟的情況下，CPU 核心的整體效能可能會在第二個執行緒執行時實際減少。 在 Xbox 360 上，這是相當簡單的問題。 已知 Xbox 360 的設定：三個 CPU 核心各有兩個硬體執行緒，而開發人員將其軟體執行緒指派給特定的 CPU 執行緒，並可進行測量以查看其執行緒設計是否可提供額外的效能。

在 Windows 上，情況更為複雜。 執行緒和其設定的數目會因電腦而異，且判斷設定會很複雜。 函數 [**GetLogicalProcessorInformation**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformation) 會提供不同硬體執行緒之間關聯性的相關資訊，而此函式可在 windows Vista、windows 7 和 WINDOWS XP SP3 上取得。 因此，現在您必須使用 CPUID 指令和 Intel 和 AMD 提供的演算法，以決定您可以使用的「實際」執行緒數目。 如需詳細資訊，請參閱參考。

DirectX SDK 中的 CoreDetection 範例包含範例程式碼，該程式碼會使用 [**GetLogicalProcessorInformation**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformation) 函數或 CPUID 指令來傳回 CPU 核心拓撲。 如果目前的平臺不支援 **GetLogicalProcessorInformation** ，則會使用 CPUID 指令。 您可以在下列位置找到 CoreDetection：

<dl> <dt>

<span id="Source_"></span><span id="source_"></span><span id="SOURCE_"></span>源：
</dt> <dd>

*DIRECTX SDK 根目錄* \\範例 \\ c + + \\ 其他 \\ CoreDetection

</dd> <dt>

<span id="Executable_"></span><span id="executable_"></span><span id="EXECUTABLE_"></span>可執行：
</dt> <dd>

*DIRECTX SDK 根目錄* \\範例 \\ c + + \\ 其他 \\ Bin \\CoreDetection.exe

</dd> </dl>

最安全的假設是每個 CPU 核心不需要超過一個 CPU 密集型執行緒。 擁有比 CPU 核心更多的需要大量 CPU 的執行緒沒有任何好處，並帶來額外的額外負荷和其他執行緒的複雜度。

## <a name="creating-threads"></a>建立執行緒

建立執行緒是相當簡單的作業，但是有許多可能的錯誤。 下列程式碼顯示適當的方式來建立執行緒、等候它終止，然後清除。


```C++
const int stackSize = 65536;
HANDLE hThread = (HANDLE)_beginthreadex( 0, stackSize,
            ThreadFunction, 0, 0, 0 );
// Do work on main thread here.
// Wait for child thread to complete
WaitForSingleObject( hThread, INFINITE );
CloseHandle( hThread );

...

unsigned __stdcall ThreadFunction( void* data )
{
#if _XBOX_VER >= 200
    // On Xbox 360 you must explicitly assign
    // software threads to hardware threads.
    XSetThreadProcessor( GetCurrentThread(), 2 );
#endif
    // Do child thread work here.
    return 0;
}
```



當您建立執行緒時，您可以選擇指定子執行緒的堆疊大小，或指定零，在這種情況下，子執行緒將會繼承父執行緒的堆疊大小。 在 Xbox 360 上，當執行緒啟動時，堆疊會完全認可，而指定零可能會浪費大量的記憶體，因為許多子執行緒不需要像父系一樣多的堆疊。 在 Xbox 360 也請務必將堆疊大小設為 64-KB 的倍數。

如果您使用 [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) 函式來建立執行緒，則 C/c + + 執行時間 (CRT) 將無法在 Windows 上正確地初始化。 我們建議您改用 CRT [**\_ beginthreadex**](https://msdn.microsoft.com/library/ms397047(v=VS.70).aspx)函數。

[**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread)或 [**\_ beginthreadex**](https://msdn.microsoft.com/library/ms397047(v=VS.70).aspx)的傳回值是執行緒控制碼。 您可以使用這個執行緒來等候子執行緒終止，這比檢查執行緒狀態的迴圈中的旋轉更簡單且更有效率。 若要等候執行緒終止，只要以執行緒控制碼呼叫 [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) 即可。

線上程終止且執行緒控制碼已關閉之前，將不會釋放執行緒的資源。 因此，當您完成時，請務必使用 [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) 來關閉執行緒控制碼。 如果您將等待中的執行緒使用 [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject)來終止，請務必在等候完成之前關閉控制碼。

在 Xbox 360 上，您必須使用 **XSetThreadProcessor** 明確地將軟體執行緒指派給特定的硬體執行緒。 否則，所有子執行緒都會保持在與父系相同的硬體執行緒上。 在 Windows 上，您可以使用 [**SetThreadAffinityMask**](/windows/win32/api/winbase/nf-winbase-setthreadaffinitymask) ，強烈建議使用您的執行緒應該在哪個硬體執行緒上執行的作業系統。 由於您不知道系統上可能執行了哪些其他進程，因此通常應該避免在 Windows 上執行這項技術。 通常最好是讓 Windows 排程器將您的執行緒指派給閒置的硬體執行緒。

建立執行緒是昂貴的作業。 執行緒應該建立和終結很少。 如果您發現自己想要經常建立和終結執行緒，請改用等候工作的執行緒集區。

## <a name="synchronizing-threads"></a>同步處理執行緒

若要讓多個執行緒一起運作，您必須能夠同步處理執行緒、傳遞訊息，以及要求資源的獨佔存取權。 Windows 和 Xbox 360 隨附一組豐富的同步處理原始物件。 如需這些同步處理原始物件的完整詳細資訊，請參閱平臺檔。

### <a name="exclusive-access"></a>獨佔存取權

取得資源、資料結構或程式碼路徑的獨佔存取權，是常見的需求。 取得獨佔存取權的其中一個選項是 mutex，其一般使用方式如下所示。


```C++
// Initialize
HANDLE mutex = CreateMutex( 0, FALSE, 0 );

// Use
void ManipulateSharedData()
{
    WaitForSingleObject( mutex, INFINITE );
    // Manipulate stuff...
    ReleaseMutex( mutex );
}

// Destroy
CloseHandle( mutex );
The kernel guarantees that, for a particular mutex, only one thread at a time can 
acquire it.
The main disadvantage to mutexes is that they are relatively expensive to acquire 
and release. A faster alternative is a critical section.
// Initialize
CRITICAL_SECTION cs;
InitializeCriticalSection( &cs );

// Use
void ManipulateSharedData()
{
    EnterCriticalSection( &cs );
    // Manipulate stuff...
    LeaveCriticalSection( &cs );
}

// Destroy
DeleteCriticalSection( &cs );
```



重要區段與 mutex 具有類似的語法，但是它們只能在進程內進行同步處理，而不是在進程之間進行同步處理。 其主要優點是它們執行的速度大約比 mutex 快20倍。

### <a name="events"></a>事件

如果有兩個執行緒（可能是更新執行緒和轉譯執行緒）正在使用一對轉譯描述緩衝區，則它們需要一種方式來指出何時使用其特定緩衝區完成。 這可以藉由將使用 [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa)) 配置的事件 (與每個緩衝區產生關聯來完成。 當執行緒以緩衝區完成時，它可以使用 [**SetEvent**](/windows/win32/api/synchapi/nf-synchapi-setevent) 來表示這一點，然後在另一個緩衝區的事件上呼叫 [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) 。 這項技術可輕鬆據此資源的三倍緩衝。

### <a name="semaphores"></a>信號燈

信號是用來控制可執行檔執行緒數目，通常用來執行工作佇列。 其中一個執行緒會將工作新增至佇列，並在每次將新的專案加入至佇列時使用 [**ReleaseSemaphore**](/windows/win32/api/synchapi/nf-synchapi-releasesemaphore) 。 這可讓一個背景工作執行緒從等候中的執行緒集區中釋放。 工作者執行緒只會呼叫 [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject)，當它傳回時，他們知道佇列中有一個工作專案。 此外，必須使用重要區段或其他同步處理技術，才能保證共用工作佇列的安全存取。

### <a name="avoid-suspendthread"></a>避免 SuspendThread

有時候，當您想要讓執行緒停止正在執行的工作時，使用 [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) ，而不是正確的同步處理原始物件會很有吸引力。 這一律是不良的概念，而且可能很容易導致鎖死和其他問題。 **SuspendThread** 也會與 Visual Studio 偵錯工具不正確互動。 避免 **SuspendThread**。 請改用 [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) 。

### <a name="waitforsingleobject-and-waitformultipleobjects"></a>WaitForSingleObject 和 WaitForMultipleObjects

函數 [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) 是最常用的同步處理函數。 不過，有時候您會想要讓執行緒等候數個條件，或符合一組條件的其中一個條件。 在此情況下，您應該使用 [**WaitForMultipleObjects**](/windows/win32/api/synchapi/nf-synchapi-waitformultipleobjects)。

### <a name="interlocked-functions-and-lockless-programming"></a>連鎖函數和 Lockless 程式設計

有一系列函數可執行簡單的安全線程作業，而不需要使用鎖定。 這些是連鎖的函式系列，例如 [**InterlockedIncrement**](/windows/win32/api/winnt/nf-winnt-interlockedincrement)。 這些函式和其他使用旗標旗標的技巧，統稱為 lockless 程式設計。 Lockless 程式設計很難正確運作，而且在 Xbox 360 上比在 Windows 上更為困難。

如需無鎖定程式設計的詳細資訊，請參閱 [Xbox 360 和 Microsoft Windows 的程式設計考慮 Lockless](./lockless-programming.md)。

### <a name="minimizing-synchronization"></a>最小化同步處理

某些同步處理方法會比其他方法更快。 不過，您不需要藉由選擇最快的同步處理技術來優化您的程式碼，通常較不常進行同步處理。 這比太頻繁地進行同步處理的速度更快，而且可讓更簡單的程式碼更容易進行 debug 錯。

某些作業（例如記憶體配置）可能必須使用同步處理原始物件才能正確運作。 因此，從預設共用堆積進行頻繁的配置將會導致頻繁的同步處理，這會浪費一些效能。 \_ \_ 如果您使用 HeapCreate) 可以避免發生此隱藏同步處理，則使用堆積不會序列化，以避免頻繁的配置或使用每個執行緒的堆積 (。

隱藏同步處理的另一個原因是 D3DCREATE \_ 多執行緒，這會導致 Windows 上的 D3D 在許多作業上使用同步處理。  (Xbox 360 上會忽略旗標。 ) 

每個執行緒的資料（也稱為執行緒區域儲存區）可能是避免同步處理的重要方式。 Visual C++ 可讓您使用 **\_ \_ declspec (執行緒)** 語法，將全域變數宣告為每個執行緒。


```C++
__declspec( thread ) int tls_i = 1;
```



這會讓進程中的每個執行緒都有自己的 tls \_ i 複本，而且可以安全且有效率地參考，而不需要進行同步處理。

**\_ \_ Declspec (thread)** 技術無法使用動態載入的 dll。 如果您使用動態載入的 Dll，您將需要使用 TLSAlloc 系列的函式來執行執行緒區域儲存區。

## <a name="destroying-threads"></a>終結執行緒

終結執行緒的唯一安全方法是讓執行緒本身結束，方法是從主執行緒函式傳回，或讓執行緒呼叫 [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread)或 [**\_ endthreadex**](https://msdn.microsoft.com/library/hw264s73(v=VS.71).aspx)。 如果使用 [**\_ beginthreadex**](https://msdn.microsoft.com/library/ms397047(v=VS.70).aspx)建立執行緒，則應該使用 **\_ endthreadex** 或從主執行緒函式傳回，因為使用 **ExitThread** 無法正確地釋放 CRT 資源。 請勿呼叫 [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread) 函式，因為執行緒將不會正確地清除。 執行緒應該一律認可自殺，永遠不會 murdered。

## <a name="openmp"></a>OpenMP

OpenMP 是一種語言延伸模組，可讓您使用 pragma 來引導平行迴圈中的編譯器，以將多執行緒加入至您的程式。 Windows 和 Xbox 360 上的 Visual C++ 2005 支援 OpenMP，並且可以與手動執行緒管理一起使用。 OpenMP 可能是您程式碼多執行緒元件的便利方法，但不太可能是理想的解決方案，特別是針對遊戲。 OpenMP 可能更適用于長時間執行的生產工作，例如處理圖片和其他資源。 如需詳細資訊，請參閱 Visual C++ 檔或移至 OpenMP [網站](https://www.openmp.org/)。

## <a name="profiling"></a>程式碼剖析

多執行緒分析很重要。 很容易就會很久，因為執行緒會彼此等候。 這些延遲可能難以尋找和診斷。 若要協助識別它們，請考慮將檢測新增至同步處理呼叫。 取樣分析工具也可以協助識別這些問題，因為它可以記錄計時資訊，而不會大幅改變。

## <a name="timing"></a>計時

Rdtsc 指令是取得 Windows 精確計時資訊的一種方式。 可惜的是，rdtsc 有多個問題，使其成為出貨標題的不良選擇。 Cpu 之間不一定要同步處理 rdtsc 計數器，因此當您的執行緒在硬體執行緒之間移動時，可能會得到很大的正面或負面差異。 根據電源管理設定，rdtsc 計數器的遞增頻率也可能會隨著遊戲執行而變更。 為了避免這些問題，您應該偏好 [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) 和 [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) ，以在出貨遊戲中進行高精確度的時間。 如需計時的詳細資訊，請參閱 [遊戲時間和多核心處理器](./game-timing-and-multicore-processors.md)。

## <a name="debugging"></a>偵錯

Visual Studio 完全支援 Windows 和 Xbox 360 的多執行緒偵錯工具。 Visual Studio 執行緒] 視窗可讓您線上程之間切換，以便查看不同的呼叫堆疊和區域變數。 [執行緒] 視窗也可讓您凍結和解除凍結特定的執行緒。

在 Xbox 360 上，您可以使用 [監看式] 視窗中的 [ **\@ hwthread** ] 元變數，顯示目前選取的軟體執行緒執行所在的硬體執行緒。

如果您將執行緒命名為有意義的名稱，[執行緒] 視窗會更容易使用。 Visual Studio 和其他 Microsoft 偵錯工具都可讓您為執行緒命名。 執行下列 **SetThreadName** 函式，並在每個執行緒啟動時呼叫它。


```C++
typedef struct tagTHREADNAME_INFO
{
    DWORD dwType;     // must be 0x1000
    LPCSTR szName;    // pointer to name (in user address space)
    DWORD dwThreadID; // thread ID (-1 = caller thread)
    DWORD dwFlags;    // reserved for future use, must be zero
} THREADNAME_INFO;

void SetThreadName( DWORD dwThreadID, LPCSTR szThreadName )
{
    THREADNAME_INFO info;
    info.dwType = 0x1000;
    info.szName = szThreadName;
    info.dwThreadID = dwThreadID;
    info.dwFlags = 0;

    __try
    {
        RaiseException( 0x406D1388, 0,
                    sizeof(info) / sizeof(DWORD),
            (DWORD*)&info );
    }
    __except( EXCEPTION_CONTINUE_EXECUTION ) {
    }
}

// Example usage:
SetThreadName(-1, "Main thread");
```



內核偵錯工具 (KD) 和 WinDBG 也支援多執行緒的偵錯工具。

## <a name="testing"></a>測試

多執行緒程式設計很難處理，而某些多執行緒 bug 只會顯示很少，因此難以尋找和修正。 清除這些電腦的其中一個最佳方式，就是在各式各樣的電腦上進行測試，特別是有四個以上處理器的電腦。 在單一執行緒電腦上完美運作的多執行緒程式碼，可能會在四個處理器的電腦上立即失敗。 AMD 和 Intel Cpu 的效能與時間特性有很大的差異，因此請務必根據兩個廠商的 Cpu，在多處理器電腦上進行測試。

## <a name="windows-vista-and-windows-7-improvements"></a>Windows Vista 和 Windows 7 的增強功能

針對以較新版本的 Windows 為目標的遊戲，有許多 Api 可簡化可擴充多執行緒應用程式的建立。 這特別適用于新的 ThreadPool API 和一些額外的 syncrhonziation 基本專案 (條件變數、超薄讀取/寫入器鎖定，以及一次性的初始化) 。 您可以在下列 MSDN 雜誌文章中找到這些技術的總覽：

-   [使用新的執行緒集區 Api 改進擴充性](/archive/msdn-magazine/2007/october/pooled-threads-improve-scalability-with-new-thread-pool-apis)
-   [Windows Vista 新的同步處理基本專案](/archive/msdn-magazine/2007/june/concurrency-synchronization-primitives-new-to-windows-vista)

在這些作業系統上使用 [Direct3D 11 功能](../direct3d11/direct3d-11-features.md) 的應用程式，也可以利用新的並行物件建立和延後內容命令清單的設計，為多執行緒轉譯提供更好的擴充性。

## <a name="summary"></a>總結

藉由將執行緒之間的互動降至最低的仔細設計，您可以從多執行緒程式設計獲得大幅的效能提升，而不會增加程式碼的複雜度。 這可讓您的遊戲程式碼提供下一波的處理器改良功能，並提供更吸引人的遊戲體驗。

## <a name="references"></a>參考資料

-   Jim Beveridge & Robert Weiner， *Win32 中的多執行緒應用程式*，Addison-Wesley，1997
-   Chuck Walbourn、 [遊戲計時和多核心處理器](./game-timing-and-multicore-processors.md)、Microsoft Corporation、2005
-   MSDN Library： [ **GetLogicalProcessorInformation**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformation)
-   [OpenMP](https://www.openmp.org/)

 

 