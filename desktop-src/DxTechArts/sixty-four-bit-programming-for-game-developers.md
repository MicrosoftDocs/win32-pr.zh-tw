---
title: 適用于遊戲開發人員的64位程式設計
description: 本文說明相容性和移植問題，並協助開發人員輕鬆轉換至64位平臺。
ms.assetid: 23a7ed41-6637-0607-327e-983b622e9104
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 439db3173e18206cb04875ab9c4422dbcedc7230508c8e98cf09b7fe27bfb9f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042428"
---
# <a name="64-bit-programming-for-game-developers"></a>適用于遊戲開發人員的64位程式設計

處理器製造商在其桌上型電腦中會以獨佔方式出貨64位處理器，甚至是大多數膝上型電腦的晶片組都支援 x64 技術。 重要的是，遊戲開發人員必須利用64位處理器提供的改良功能與其新應用程式，並確保其先前的應用程式在新的處理器和64位版本的 Windows Vista 和 Windows 7 上正確執行。 本文說明相容性和移植問題，並協助開發人員輕鬆轉換至64位平臺。

Microsoft 目前有下列64位作業系統：

-   Windows Server 2003 Service Pack 1
-   WindowsXP Professional x64 Edition (可供 oem 和開發人員透過 MSDN 取得) 
-   Windows Vista
-   Windows Server 2008
-   Windows 7
-   Windows Server 2008 R2

> [!Note]  
> WindowsServer 2008 R2 僅提供64位版本。

 

-   [可定址記憶體的差異](#differences-in-addressable-memory)
-   [在建立時指定大型位址感知](#specifying-large-address-aware-when-building)
-   [64位平臺上32位應用程式的相容性](#compatibility-of-32-bit-applications-on-64-bit-platforms)
    -   [潛在的相容性陷阱](#potential-compatibility-pitfalls)
-   [將應用程式移植到64位平臺](#porting-applications-to-64-bit-platforms)
-   [移植應用程式的程式碼剖析和優化](#profiling-and-optimization-of-ported-applications)
-   [64位作業系統上的 Managed 程式碼](#managed-code-on-a-64-bit-operating-system)
-   [執行64位作業系統的效能含意](#performance-implications-of-running-a-64-bit-operating-system)
-   [總結](#summary)

## <a name="differences-in-addressable-memory"></a>可定址記憶體的差異

大部分的開發人員都會注意到，64位處理器提供可處理的實體和虛擬記憶體數量的巨大飛躍。

-   32位平臺上的32位應用程式最多可以處理 2 GB。
-   以/LARGEADDRESSAWARE： YES 連結器旗標在32位上建立的32位應用程式 Windows XP 或 Windows Server 2003 with 特殊的/3gb 開機選項最多可處理 3 GB。 這會將核心限制為 1 GB，這可能會導致某些驅動程式和（或）服務失敗。
-   以/LARGEADDRESSAWARE： YES 連結器旗標在 Windows Vista 的32位版本上建立的32位應用程式，Windows Server 2008 和 Windows 7 可將記憶體定址到開機設定資料 (BCD) 元素 IncreaseUserVa 所指定的數目。 IncreaseUserVa 的值範圍從2048（預設值）到 3072 (，符合 Windows XP) 上的/3gb 開機選項所設定的記憶體數量。 4 GB 的其餘部分會配置給核心，而且可能會導致驅動程式和服務設定失敗。

    如需有關 BCD 的詳細資訊，請參閱 MSDN 上的 [開機設定資料](https://msdn.microsoft.com/library/aa362692.aspx) 。

-   64位平臺上的32位應用程式最多可處理 2 GB，或最多可達 4 GB 的/LARGEADDRESSAWARE： YES 連結器旗標。
-   64位應用程式使用43位進行定址，為應用程式提供 8 TB 的虛擬位址，並為核心保留 8 TB。

除了記憶體以外，使用記憶體對應檔 i/o 的64位應用程式，也會因為增加的虛擬位址空間而大幅受益。 64位架構也已改善浮點效能，且更快速地傳遞參數。 64位處理器具有兩倍的暫存器數目，也就是一般用途和串流 SIMD 延伸模組 (SSE) 類型，以及 SSE 和 SSE2 指令集的支援;許多64位處理器甚至支援 SSE3 指令集。

## <a name="specifying-large-address-aware-when-building"></a>在建立時指定大型位址感知

當您建立32位應用程式時，請使用連結器旗標/LARGEADDRESSAWARE 來指定大型位址感知，即使應用程式不是用於64位平臺，也是很好的作法，因為這是免費取得的優點。 如先前所述，針對組建啟用此旗標，可讓32位程式在32位 OS 或64位作業系統上以特殊開機選項存取更多記憶體。 不過，開發人員必須小心不要進行指標假設，例如假設在32位指標中絕對沒有設定過高位。 一般而言，啟用/LARGEADDRESSAWARE 旗標是不錯的作法。

具有大型位址感知的32位應用程式，可以在執行時間使用目前作業系統設定（藉由呼叫 [**GlobalMemoryStatusEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-globalmemorystatusex)）來判斷其可用的虛擬位址空間總數。 UllTotalVirtual 結果的範圍是從2147352576個位元組 (2 GB) 到4294836224個位元組 (4 GB) 。 大於 3221094400 (3 GB) 的值只能在64位版本的 Windows 上取得。 例如，如果 IncreaseUserVa 的值為2560，則結果會是 ullTotalVirtual，其值為2684223488位元組。

## <a name="compatibility-of-32-bit-applications-on-64-bit-platforms"></a>64位平臺上32位應用程式的相容性

64位 Windows 作業系統與 IA32 架構相容，而且32位應用程式使用的大部分 api 都可透過 Windows 64 位 Emulator、WOW64 上的 Windows 32 位取得。 WOW64 有助於確保這些 Api 能如預期運作。

WOW64 具有處理32位資料之封送處理的執行層。 WOW64 會重新導向 DLL 檔案要求、重新導向32位應用程式的一些登錄分支，並反映32和64位應用程式的一些登錄分支。

如需有關 WOW64 的詳細資訊，請參閱 MSDN 上的 [Wow64 執行詳細資料](/windows/desktop/WinProg64/wow64-implementation-details) 。 如需建立在 WOW64 上執行之應用程式的最佳作法，請參閱 Windows 硬體開發人員中心上[的 WOW64 最佳做法](https://www.microsoft.com/whdc/system/platform/64bit/WoW64_bestprac.mspx)。

### <a name="potential-compatibility-pitfalls"></a>潛在的相容性陷阱

大部分針對32位平臺開發的應用程式，在64位平臺上都不會有任何問題。 有些應用程式可能會有問題，可能包含下列各項：

-   64位版 Windows 作業系統的所有驅動程式都必須是64位版本。 需要新的64位驅動程式會影響依賴舊驅動程式的禁止複製配置。 請注意，核心模式驅動程式必須經過 Authenticode 簽署，才能由64位版本的 Windows 載入。
-   64位進程無法載入32位的 Dll，而32位進程無法載入64位 Dll。 開發人員必須先確定協力廠商 Dll 的64位版本可供使用，再繼續進行開發。 如果您必須在64位進程中使用32位 DLL，則可以使用 Windows 處理序間通訊 (IPC) 。 COM 元件也可以利用跨進程伺服器和封送處理，在界限之間進行通訊，但這麼做可能會導致效能降低。
-   許多 x64 處理器也是多核心處理器，而開發人員需要測試這對其繼承應用程式的影響。 多核心處理器的詳細資訊，以及遊戲應用程式的含意可在 [遊戲時間和](/windows/desktop/DxTechArts/game-timing-and-multicore-processors)多核心處理器中找到。
-   應用程式也應該呼叫 [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) 來探索檔案路徑，因為某些資料夾名稱在某些情況下已變更。 例如，CSIDL \_ PROGRAM \_ files 會 \\ 針對在64位平臺上執行的32位應用程式（而不是 "c： program files"）傳回 "c： program files (x86) " \\ 。 開發人員必須留意 WOW64 模擬器的重新導向和反映功能的運作方式。

此外，開發人員必須謹慎使用可能仍在使用的16位程式。 WOW64 無法處理16位應用程式;這包括舊的安裝程式和所有 MS-DOS 程式。

> [!Note]  
> 最常見的相容性問題是安裝程式，它會執行16位程式碼，而不會有禁止複製配置的64位驅動程式。

 

下一節將討論有關將程式碼移植到64位原生的問題，而開發人員想要確保其舊版程式可在64位平臺上運作。 這也適用于不熟悉64位程式設計的開發人員。

## <a name="porting-applications-to-64-bit-platforms"></a>將應用程式移植到64位平臺

擁有適當的工具和程式庫將有助於簡化從32位到64位開發的轉換。 DirectX 9 SDK 具有可支援 x86 和 x64 型專案的程式庫。 Microsoft Visual Studio 2005 和 Visual Studio 2008 都支援 x86 和 x64 的程式碼產生，而且它們隨附的程式庫已針對產生 x64 程式碼而優化。 不過，開發人員也需要將 Visual C 執行時間與應用程式一起散發。 請注意，Visual Studio 2005 和 Visual Studio 2008 的 Express 版本不包含 x64 編譯器，但 Standard、Professional 和 Team System 版本都是如此。

以32位平臺為目標的開發人員可以為64位開發做好準備，以便在稍後更輕鬆地進行轉換。 編譯32位專案時，開發人員應該使用/Wp64 旗標，這會導致產生會影響可攜性之問題的警告。 切換至64位工具和程式庫一開始可能會產生許多新的組建錯誤;因此，建議您在切換至64位組建之前，先切換位中立的工具和程式庫，並更正任何警告。

不過，變更工具、變更程式庫及使用某些編譯器旗標並不會足夠。 您必須重新評估程式碼標準的假設，以確保目前的編碼標準不允許可攜性問題。 可攜性問題包括指標截斷、資料類型的大小和對齊、依賴32位 Dll、使用舊版 Api、元件程式碼，以及舊的二進位檔案。

> [!Note]  
> Visual C++ 2010 包括 stdint.h .h 和 cstdint C99 標頭，這些標頭會定義標準可攜性類型 int32 \_ t、uint32 \_ t、int64 \_ t、uint64 \_ t、intptr \_ t 和 uintptr \_ t。 搭配標準 ptrdiff \_ t 和 size \_ t 資料類型使用這些資料類型，可能會進行到以下用來改善程式碼可攜性的 Windows portabilty 類型。

 

主要移植問題包括下列各項：

<dl> <dt>

<span id="Pointer_Truncation"></span><span id="pointer_truncation"></span><span id="POINTER_TRUNCATION"></span>**指標截斷**
</dt> <dd>

指標是64位 OS 上的64位，因此將指標轉換成其他資料類型可能會導致截斷，指標算術可能會導致損毀。 使用/Wp64 旗標通常會提供有關這類問題的警告，但是在轉換指標類型時，使用多型型別 (INT \_ ptr、DWORD \_ PTR、SIZE \_ T、UINT ptr 等等) ，在 \_ 轉換指標類型時，最好避免這個問題。 由於指標在新的平臺上是64位，因此開發人員應該檢查指標的順序以及類別和結構中的資料類型，以減少或消除填補。

</dd> <dt>

<span id="Data_Types_and_Binary_Files"></span><span id="data_types_and_binary_files"></span><span id="DATA_TYPES_AND_BINARY_FILES"></span>**資料類型和二進位檔案**
</dt> <dd>

當64位平臺上的指標從32位增加到64時，其他資料類型則否。 固定精確度資料類型 (DWORD32、DWORD64、INT32、INT64、LONG32、LONG64、UINT32、UINT64) 可用於資料類型大小必須已知的位置;例如，在二進位檔案結構中。 指標大小和資料對齊的變更需要進行特殊處理，以確保32位到64位的相容性。 如需詳細資訊，請參閱[準備開始64位 Windows：新的資料類型](/windows/desktop/WinProg64/the-new-data-types)。

</dd> <dt>

<span id="Older_Win32_APIs_and_Data_Alignment"></span><span id="older_win32_apis_and_data_alignment"></span><span id="OLDER_WIN32_APIS_AND_DATA_ALIGNMENT"></span>**舊版 Win32 Api 和資料對齊**
</dt> <dd>

某些 Win32 Api 已被取代，並以更多中立的 API 呼叫（例如 SetWindowLongPtr 取代 SetWindowLong）取代。

在 x64 平臺上，非對齊存取的效能會受到更大的影響，而不是 x86 平臺。 類型 \_ 對齊 (t) 和欄位 \_ 位移 (t，成員) 宏可用來判斷可直接由程式碼使用的對齊資訊。 正確使用這些上述的宏應該消除潛在的未對齊存取罰款。

您 \_ \_ 可以在64位 Windows 程式設計中找到類型對齊宏、欄位位移宏和一般64位程式設計資訊的詳細資訊[：遷移提示：其他考慮](/windows/desktop/WinProg64/additional-considerations)和[準備使用64位 Windows：使用指標的規則](/windows/desktop/WinProg64/rules-for-using-pointers)。

</dd> <dt>

<span id="Assembly_Code"></span><span id="assembly_code"></span><span id="ASSEMBLY_CODE"></span>**元件碼**
</dt> <dd>

在64位平臺上不支援內嵌組譯程式碼，且需要加以取代。 架構中的變更可能會有變更的應用程式瓶頸，而 C/c + + 或內建函式可使用更容易閱讀的程式碼來達成類似的結果。 最建議的作法是將所有元件程式碼切換至 C 或 c + +。 內建函式可以用來取代元件程式碼，但只應在執行完整分析和分析之後使用。

X87、MMX 和3DNow！ 指令集已在64位模式中被取代。 針對32位模式的回溯相容性，仍然有指示集存在;不過，為了避免未來的相容性問題，建議您在目前和未來的專案中使用它們。

</dd> <dt>

<span id="Deprecated_APIs"></span><span id="deprecated_apis"></span><span id="DEPRECATED_APIS"></span>**已淘汰的 Api**
</dt> <dd>

針對64位原生應用程式，已卸載一些較舊的 DirectX Api： DirectPlay 4 和更早版本、DirectDraw 6 及更早版本、Direct3D 8 和更早版本，以及 DirectInput 7 及更早版本。 此外，DirectMusic 的核心 API 也可供原生64位應用程式使用，但效能層和 DirectMusic 生產者已被取代。

Visual Studio 會發出淘汰警告，而且這些變更不是使用最新 api 之開發人員的問題。

</dd> </dl>

## <a name="profiling-and-optimization-of-ported-applications"></a>移植應用程式的程式碼剖析和優化

所有開發人員都需要重新分析即將移植到新架構的任何應用程式。 許多正在移植到64位平臺的應用程式，其32位版本會有不同的效能設定檔。 開發人員必須先執行64位效能測試，才能評估需要優化的內容。 這就是很好的消息，那就是許多傳統的優化都能在64位平臺上運作。 此外，64位編譯器也可以使用編譯器旗標和程式碼提示的正確用法來執行許多優化。

某些結構可能會重新排序其內部資料類型，以節省記憶體空間並改善快取。 在某些情況下，可以使用陣列索引，而不是完整的64位指標。 /Fp： fast 旗標可改善浮點優化和向量化。 使用 \_ \_ restrict、declspec (restrict) ，以及 declspec (noalias) 可協助編譯器解析別名並改善登錄檔案的使用。

如需/fp： fast 的詳細資訊，請參閱 [/fp (指定 Floating-Point 行為) ](/cpp/build/reference/fp-specify-floating-point-behavior)。

有關限制的詳細資訊 \_ \_ 可在[Microsoft 專有的](/cpp/cpp/microsoft-specific-modifiers)修飾詞中找到。

如需 declspec (限制) 的詳細資訊，請參閱 [優化最佳做法](/cpp/build/optimization-best-practices)。

如需 declspec (noalias) 的詳細資訊，請參閱[ \_ \_ declspec (noalias) ](https://msdn.microsoft.com/library/k649tyc7(VS.80).aspx)。

## <a name="managed-code-on-a-64-bit-operating-system"></a>64位作業系統上的 Managed 程式碼

許多遊戲開發人員會在其工具鏈中使用受控碼，因此瞭解它在64位作業系統上的行為可能會很有説明。 Managed 程式碼是指令集中性的，因此當您在64位作業系統上執行 managed 應用程式時，Common Language Runtime (CLR) 可以將它當作32位或64位進程來執行。 根據預設，CLR 會以64位的形式執行受控應用程式，而且不會有任何問題就能正常運作。 但是，如果您的應用程式相依于原生32位的 DLL，則當應用程式嘗試呼叫此 DLL 時，您的應用程式將會失敗。 64位進程需要完全64位的程式碼，而且無法從64位進程呼叫32位的 DLL。 最佳的長期解決方案是將您的機器碼編譯為64位，但完全合理的短期解決方案是只使用/platform： x86 build 旗標將您的受控應用程式標示為僅適用于 x86。

## <a name="performance-implications-of-running-a-64-bit-operating-system"></a>執行64位作業系統的效能含意

因為具有 AMD64 和 Intel 64 架構的處理器可以原生執行32位的指示，所以即使是在64的作業系統上，它們仍能以完整的速度執行32位應用程式。 在呼叫作業系統函式時，在32位和64位之間轉換參數的成本很低，但這項成本通常是可忽略的。 這表示在64位作業系統上執行32位應用程式時，您應該不會看到任何緩慢的情況。

當您將應用程式編譯為64位時，計算會變得更複雜。 64位程式使用64位指標，而其指示稍微放大，因此記憶體需求會稍微增加。 這可能會導致效能稍微下降。 另一方面，擁有兩倍的暫存器，並且能夠在單一指令中進行64位整數計算，通常會比補償更多。 最後的結果是，64位應用程式的執行速度可能會比編譯為32位的應用程式稍微慢一點，但其執行速度通常會稍微快一點。

## <a name="summary"></a>摘要

64位架構可讓開發人員將遊戲的外觀、音效和玩的限制推播。 不過，從32位程式設計轉換至64位程式設計並不重要。 藉由瞭解兩者間的差異，以及藉由使用最新的工具，轉換至64位平臺可以更輕鬆且更快速。

如需有關64位程式設計的詳細資訊，請參閱 [Visual C++ 開發人員中心：64位程式設計](https://msdn.microsoft.com/vstudio//aa336463.aspx)。

 

 