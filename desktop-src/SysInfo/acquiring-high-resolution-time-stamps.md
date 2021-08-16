---
description: Windows 提供 api，可讓您用來取得高解析度的時間戳記或測量時間間隔。
ms.assetid: D66E0FC2-3AF2-489B-B4B5-78648905B77B
title: 取得高解析度時間戳記
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e25c50cb602dd7e5c53c967c12321ec02a6ea68613767f4019b2def7f5793b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117764628"
---
# <a name="acquiring-high-resolution-time-stamps"></a>取得高解析度時間戳記

Windows 提供 api，可讓您用來取得高解析度的時間戳記或測量時間間隔。 原生程式碼的主要 API 是 [**QueryPerformanceCounter (QPC)**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)。 若為設備磁碟機，則會 [**KeQueryPerformanceCounter**](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-kequeryperformancecounter)核心模式 API。 針對 managed 程式碼， [**system.object**](/previous-versions/windows/) 類別會使用 **QPC** 做為精確的時間。

[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) 與無關，且不會同步處理至任何外部時間參考。 若要取出可同步處理至外部時間參考的時間戳記，例如，國際標準時間 (UTC) 以用於高解析度的當日時間測量，請使用 [**GetSystemTimePreciseAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime)。

時間戳記和時間間隔測量是電腦和網路效能測量的不可或缺部分。 這些效能測量作業包括計算回應時間、輸送量和延遲，以及分析程式碼執行。 每一項作業都牽涉到在時間間隔內發生的活動量測，此時間間隔是由 start 和 end 事件所定義，而該時間間隔可以與任何外部的日期時間參考無關。

[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) 通常是使用時間戳事件的最佳方法，並測量在相同系統或虛擬機器上發生的小時間間隔。 當您想要在多部電腦上使用時間戳事件時，請考慮使用 [**GetSystemTimePreciseAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime) ，前提是每台機器都參與時間同步處理配置，例如網路時間通訊協定 (NTP) 。 **QPC** 可協助您避免其他時間測量方法可能遇到的問題，例如直接讀取處理器的時間戳記計數器 (的 TSC) 。

-   [Windows 版本中的 QPC 支援](#qpc-support-in-windows-versions)
-   [取得時間戳記的指引](#guidance-for-acquiring-time-stamps)
    -   [虛擬化](#virtualization)
    -   [直接的 TSC 使用方式](#direct-tsc-usage)
    -   [取得時間戳記的範例](#examples-for-acquiring-time-stamps)
-   [關於 QPC 和 TSC 的一般常見問題](#general-faq-about-qpc-and-tsc)
-   [使用 QPC 和 TSC 進行程式設計的常見問題](#faq-about-programming-with-qpc-and-tsc)
-   [低層級硬體時鐘特性](#low-level-hardware-clock-characteristics)
    -   [絕對時鐘和差異時鐘](#absolute-clocks-and-difference-clocks)
    -   [解析度、有效位數、精確度和穩定性](#resolution-precision-accuracy-and-stability)
-   [硬體計時器資訊](#hardware-timer-info)

## <a name="qpc-support-in-windows-versions"></a>Windows 版本中的 QPC 支援

[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)是在 Windows 2000 和 Windows XP 中引進，並已發展成可充分利用硬體平臺和處理器的增強功能。 在這裡，我們將說明不同 Windows 版本的 **QPC** 特性，以協助您維護在這些 Windows 版本上執行的軟體。

### <a name="windows-xp-and-windows-2000"></a>WindowsXP 和 Windows 2000

[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)可在 Windows XP 和 Windows 2000 上取得，並且在大部分系統上都能順利運作。 不過，某些硬體系統的 BIOS 並未正確指出硬體 CPU 特性 (非不變異的 TSC) ，而某些多核心或多處理器系統使用的處理器與 TSCs 無法跨核心進行同步處理。 如果系統具有執行這些版本的 Windows 有瑕疵的系統，則在使用 TSC 作為 **QPC** 的基礎時，可能不會在不同的核心上提供相同的 **QPC** 讀取。

### <a name="windows-vista-and-windows-server-2008"></a>Windows Vista 與 Windows Server 2008

隨附于 Windows Vista 和 Windows Server 2008 的所有電腦都使用平臺計數器 (高精確度事件計時器 (HPET) ) 或 ACPI 電源管理計時器 (PM 計時器) 作為 [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)的基礎。 這類平臺計時器具有比 TSC 更高的存取延遲，而且會在多個處理器之間共用。 如果是從多個處理器同時呼叫，這會限制 **QPC** 的擴充性。

### <a name="windows-7-and-windows-server-2008-r2"></a>Windows 7 與 Windows Server 2008 R2

大部分的 Windows 7 和 Windows Server 2008 R2 電腦都有具有固定速率 TSCs 的處理器，並使用這些計數器作為 [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)的基礎。 TSCs 是高解析度的每個處理器硬體計數器，可利用非常低的延遲和額外負荷 (，視10s 或數百部機器週期的順序而定，這取決於處理器類型) 。 Windows 7 和 Windows Server 2008 R2 使用 TSCs 做為單一時鐘網域系統上的 **QPC** 基礎，其中作業系統 (或基礎程式) 能夠在系統初始化期間，在所有處理器之間緊密地同步處理個別 TSCs。 在這類系統上，相較于使用 platform 計數器的系統，讀取效能計數器的成本明顯較低。 此外，並行呼叫也不會有額外的負荷，而且使用者模式查詢通常會略過系統呼叫，進而減少額外負荷。 在未適用于 timekeeping 的系統上，Windows 會自動選取平臺計數器 (HPET 計時器或 ACPI PM 計時器) 做為 **QPC** 的基礎。

### <a name="windows-8-windows-81-windows-server-2012-and-windows-server-2012-r2"></a>Windows 8、Windows 8.1、Windows Server 2012 和 Windows Server 2012 R2

Windows 8、Windows 8.1、Windows Server 2012 和 Windows Server 2012 R2 使用 TSCs 做為效能計數器的基礎。 已大幅改善 TSC 同步處理演算法，以更妥善容納具有許多處理器的大型系統。 此外，也新增了新的精確時間 API 支援，可讓您從作業系統取得精確的時鐘時間戳記。 如需詳細資訊，請參閱 [**GetSystemTimePreciseAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime)。 在 Windows RT 電腦平臺上，效能計數器會以專屬平臺計數器或 Windows RT PC 一般計時器提供的系統計數器為基礎（如果平臺已有配備的話）。

## <a name="guidance-for-acquiring-time-stamps"></a>取得時間戳記的指引

Windows，並將繼續投資提供可靠且有效率的效能計數器。 當您需要以1微秒或更高解析度的時間戳記，而不需要將時間戳記同步處理至外部時間參考時，請選擇 [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)、 [**KeQueryPerformanceCounter**](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-kequeryperformancecounter)或 [**KeQueryInterruptTimePrecise**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-kequeryinterrupttimeprecise)。 當您需要解析為1微秒或更高的 UTC 同步處理時間戳記時，請選擇 [**GetSystemTimePreciseAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime) 或 [**KeQuerySystemTimePrecise**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-kequerysystemtimeprecise)。

在相對較少的平臺上，無法使用 TSC 註冊作為 [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) 基礎，例如，基於 [硬體計時器資訊](#hardware-timer-info)中所述的原因，取得高解析度的時間戳記可能會比取得較低解析度的時間戳記更昂貴。 如果10到16毫秒的解析已足夠，您可以使用 [**GetTickCount64**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount64)、 [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime)、 [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)、 [**KeQueryInterruptTime**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-kequeryinterrupttime)或 [**KeQueryUnbiasedInterruptTime**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-kequeryunbiasedinterrupttime) 來取得未同步處理至外部時間參考的時間戳記。 針對 UTC 同步處理的時間戳記，請使用 [**GetSystemTimeAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimeasfiletime) 或 [**KeQuerySystemTime**](/windows-hardware/drivers/ddi/wdm/nf-wdm-kequerysystemtime~r1)。 如果需要較高的解析度，您可以使用 [**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise)、 [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise)或 [**KeQueryInterruptTimePrecise**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-kequeryinterrupttimeprecise) 來改為取得時間戳記。

一般來說，即使是在不同的執行緒或進程上測量，效能計數器的結果仍會在多核心和多處理器系統中的所有處理器之間保持一致。 以下是此規則的一些例外狀況：

-   基於下列其中一個原因，在特定處理器上執行的預先 Windows Vista 作業系統可能會違反此一致性：

    -   硬體處理器具有不具變異的 TSC，BIOS 未正確指出此狀況。
    -   使用的 TSC 同步處理演算法不適用於具有大量處理器的系統。

-   當您比較從不同的執行緒取得的效能計數器結果時，請考慮±1刻度的不同值會有不明確的順序。 如果從相同的執行緒取得時間戳記，則不會套用此±1滴答不確定性。 在此內容中，「期限」一詞是指等於1÷的一段時間， (從 [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency)) 取得之效能計數器的頻率。

當您在具有多個時鐘網域的大型伺服器系統上使用效能計數器（這些系統未在硬體中同步處理）時，Windows 判斷該 TSC 無法用於時間用途，並選取平臺計數器作為 [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)的基礎。 雖然此案例仍會產生可靠的時間戳記，但存取延遲和擴充性會受到負面影響。 因此，如先前的使用指導方針所述，只有在需要這類解決方案時，才使用可提供1微秒或更佳解析度的 Api。 您可以使用 TSC 作為 **QPC** 在多時鐘網域系統上的基礎，包括所有處理器時鐘網域的硬體同步處理，因為這樣可有效地將它們當做單一時鐘網域系統運作。

效能計數器的頻率是在系統開機時固定的，且在所有處理器都是一致的，因此您只需要在應用程式初始化時從 [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) 查詢頻率，然後快取結果。

### <a name="virtualization"></a>虛擬化

效能計數器預期會可靠地在所有執行的虛擬機器上執行的虛擬機器上運作。 不過，符合程式管理版本1.0 介面和表面參考時間啟蒙的管理程式，可提供大幅較低的負荷。 如需有關管理程式介面和 enlightenments 的詳細資訊，請參閱 [虛擬程式規範](/virtualization/hyper-v-on-windows/reference/tlfs)。

### <a name="direct-tsc-usage"></a>直接的 TSC 使用方式

我們強烈建議使用 **RDTSC** 或 **RDTSCP** 處理器指令來直接查詢 TSC，因為您不會在某些版本的 Windows、跨虛擬機器的即時移轉，以及不具變異或緊密同步的 TSCs 的硬體系統上取得可靠的結果。 相反地，我們鼓勵您使用 [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) 來利用它所提供的抽象概念、一致性和可攜性。

### <a name="examples-for-acquiring-time-stamps"></a>取得時間戳記的範例

這些章節中的各種程式碼範例會示範如何取得時間戳記。

### <a name="using-qpc-in-native-code"></a>在原生程式碼中使用 QPC

此範例說明如何在 C 和 c + + 機器碼中使用 [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) 。


```C++
LARGE_INTEGER StartingTime, EndingTime, ElapsedMicroseconds;
LARGE_INTEGER Frequency;

QueryPerformanceFrequency(&Frequency); 
QueryPerformanceCounter(&StartingTime);

// Activity to be timed

QueryPerformanceCounter(&EndingTime);
ElapsedMicroseconds.QuadPart = EndingTime.QuadPart - StartingTime.QuadPart;


//
// We now have the elapsed number of ticks, along with the
// number of ticks-per-second. We use these values
// to convert to the number of elapsed microseconds.
// To guard against loss-of-precision, we convert
// to microseconds *before* dividing by ticks-per-second.
//

ElapsedMicroseconds.QuadPart *= 1000000;
ElapsedMicroseconds.QuadPart /= Frequency.QuadPart;
```



### <a name="acquiring-high-resolution-time-stamps-from-managed-code"></a>從受控碼取得高解析度的時間戳記

此範例示範如何使用 managed [**程式碼 system.object**](/previous-versions/windows/) 。


```CSharp
using System.Diagnostics;

long StartingTime = Stopwatch.GetTimestamp();

// Activity to be timed

long EndingTime  = Stopwatch.GetTimestamp();
long ElapsedTime = EndingTime - StartingTime;

double ElapsedSeconds = ElapsedTime * (1.0 / Stopwatch.Frequency);
```



System.servicemodel [**類別也**](/previous-versions/windows/) 提供數個方便的方法來執行時間間隔測量。

### <a name="using-qpc-from-kernel-mode"></a>使用核心模式的 QPC

Windows 核心透過 [**KeQueryPerformanceCounter**](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-kequeryperformancecounter) （可從中取得效能計數器和效能頻率）提供效能計數器的核心模式存取。 **KeQueryPerformanceCounter** 僅適用于核心模式，並提供給設備磁碟機和其他核心模式元件的寫入器。

此範例說明如何在 C 和 c + + 核心模式中使用 [**KeQueryPerformanceCounter**](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-kequeryperformancecounter) 。


```C++
LARGE_INTEGER StartingTime, EndingTime, ElapsedMicroseconds;
LARGE_INTEGER Frequency;

StartingTime = KeQueryPerformanceCounter(&Frequency);

// Activity to be timed

EndingTime = KeQueryPerformanceCounter(NULL);
ElapsedMicroseconds.QuadPart = EndingTime.QuadPart - StartingTime.QuadPart;
ElapsedMicroseconds.QuadPart *= 1000000;
ElapsedMicroseconds.QuadPart /= Frequency.QuadPart;
```



## <a name="general-faq-about-qpc-and-tsc"></a>關於 QPC 和 TSC 的一般常見問題

以下是一般 [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) 和 TSCs 常見問題的解答。

<dl> <dt>

<span id="Is_QueryPerformanceCounter___the_same_as_the_Win32_GetTickCount___or_________GetTickCount64___function_"></span><span id="is_queryperformancecounter___the_same_as_the_win32_gettickcount___or_________gettickcount64___function_"></span><span id="IS_QUERYPERFORMANCECOUNTER___THE_SAME_AS_THE_WIN32_GETTICKCOUNT___OR_________GETTICKCOUNT64___FUNCTION_"></span>**QueryPerformanceCounter () 與 Win32 GetTickCount () 或 GetTickCount64 () 函數相同嗎？**
</dt> <dd>

不會。 [**GetTickCount**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) 和 [**GetTickCount64**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount64) 與 [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)無關。 **GetTickCount** 和 **GetTickCount64** 會傳回系統啟動之後的毫秒數。

</dd> <dt>

<span id="Should_I_use_QPC_or_call_the_RDTSC__RDTSCP_instructions_directly_"></span><span id="should_i_use_qpc_or_call_the_rdtsc__rdtscp_instructions_directly_"></span><span id="SHOULD_I_USE_QPC_OR_CALL_THE_RDTSC__RDTSCP_INSTRUCTIONS_DIRECTLY_"></span>**我應該使用 QPC 或直接呼叫 RDTSC/RDTSCP 指示嗎？**
</dt> <dd>

為了避免 incorrectness 和可攜性問題，我們強烈建議您使用 [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) ，而不是使用 TSC 登錄或 **RDTSC** 或 **RDTSCP** 處理器指示。

</dd> <dt>

<span id="What_is_QPC_s_relation_to_an_external_time_epoch__Can_it_be_synchronized_to_an_________external_epoch_such_as_UTC_"></span><span id="what_is_qpc_s_relation_to_an_external_time_epoch__can_it_be_synchronized_to_an_________external_epoch_such_as_utc_"></span><span id="WHAT_IS_QPC_S_RELATION_TO_AN_EXTERNAL_TIME_EPOCH__CAN_IT_BE_SYNCHRONIZED_TO_AN_________EXTERNAL_EPOCH_SUCH_AS_UTC_"></span>**QPC 與外部時間 epoch 有何關聯？它是否可以同步處理至外部 epoch （例如 UTC）？**
</dt> <dd>

[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) 是以無法同步處理至外部時間參考的硬體計數器為基礎，例如 UTC。 如需可同步處理至外部 UTC 參考的精確日期時間戳記，請使用 [**GetSystemTimePreciseAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime)。

</dd> <dt>

<span id="Is_QPC_affected_by_daylight_savings_time__leap_seconds__time_zones__or_system_________time_changes_made_by_the_administrator_"></span><span id="is_qpc_affected_by_daylight_savings_time__leap_seconds__time_zones__or_system_________time_changes_made_by_the_administrator_"></span><span id="IS_QPC_AFFECTED_BY_DAYLIGHT_SAVINGS_TIME__LEAP_SECONDS__TIME_ZONES__OR_SYSTEM_________TIME_CHANGES_MADE_BY_THE_ADMINISTRATOR_"></span>**QPC 是否受日光節約時間、閏秒、時區或系統管理員所做的系統時間變更所影響？**
</dt> <dd>

不會。 [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) 與系統時間和 UTC 完全無關。

</dd> <dt>

<span id="Is_QPC_accuracy_affected_by_processor_frequency_changes_caused_by_power_________management_or_Turbo_Boost_technology_"></span><span id="is_qpc_accuracy_affected_by_processor_frequency_changes_caused_by_power_________management_or_turbo_boost_technology_"></span><span id="IS_QPC_ACCURACY_AFFECTED_BY_PROCESSOR_FREQUENCY_CHANGES_CAUSED_BY_POWER_________MANAGEMENT_OR_TURBO_BOOST_TECHNOLOGY_"></span>**QPC 的精確度是否受到電源管理或 Turbo 加速技術所造成的處理器頻率變更所影響？**
</dt> <dd>

不會。 如果處理器具有不變的 TSC，則 [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) 不會受到這類變更的影響。 如果處理器沒有不具變異的 TSC， **QPC** 會還原為平臺硬體計時器，而不會受到處理器頻率變更或 Turbo 加速技術的影響。

</dd> <dt>

<span id="Does_QPC_reliably_work_on_multi-processor_systems__multi-core_system__and_________systems_with_hyper-threading_"></span><span id="does_qpc_reliably_work_on_multi-processor_systems__multi-core_system__and_________systems_with_hyper-threading_"></span><span id="DOES_QPC_RELIABLY_WORK_ON_MULTI-PROCESSOR_SYSTEMS__MULTI-CORE_SYSTEM__AND_________SYSTEMS_WITH_HYPER-THREADING_"></span>**QPC 是否可在多處理器系統、多重核心系統以及具有超執行緒的系統上可靠地運作？**
</dt> <dd>

Yes

</dd> <dt>

<span id="How_do_I_determine_and_validate_that_QPC_works_on_my_machine_"></span><span id="how_do_i_determine_and_validate_that_qpc_works_on_my_machine_"></span><span id="HOW_DO_I_DETERMINE_AND_VALIDATE_THAT_QPC_WORKS_ON_MY_MACHINE_"></span>**如何? 判斷並驗證 QPC 是否可在我的電腦上運作？**
</dt> <dd>

您不需要執行這類檢查。

</dd> <dt>

<span id="Which_processors_have_non-invariant_TSCs__How_can_I_check_if_my_system_has_a_________non-invariant_TSC_"></span><span id="which_processors_have_non-invariant_tscs__how_can_i_check_if_my_system_has_a_________non-invariant_tsc_"></span><span id="WHICH_PROCESSORS_HAVE_NON-INVARIANT_TSCS__HOW_CAN_I_CHECK_IF_MY_SYSTEM_HAS_A_________NON-INVARIANT_TSC_"></span>**哪些處理器有非變異 TSCs？如何檢查我的系統是否有不具變異的 TSC？**
</dt> <dd>

您不需要自行執行這一檢查。 Windows 作業系統會在系統初始化期間執行數個檢查，以判斷 TSC 是否適合做為 [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)的基礎。 不過，基於參考目的，您可以使用下列其中一種方式，判斷您的處理器是否具有不變的 TSC：

-   Windows Sysinternals 的 Coreinfo.exe 公用程式
-   檢查與 TSC 特性相關的 CPUID 指令所傳回的值
-   處理器製造商的檔

以下顯示 Windows Sysinternals Coreinfo.exe 公用程式 ([www.sysinternals.com](https://www.sysinternals.com)) 提供的 TSC 非變異資訊。 星號表示 "True"。

``` syntax
> Coreinfo.exe 

Coreinfo v3.2 - Dump information on system CPU and memory topology
Copyright (C) 2008-2012 Mark Russinovich
Sysinternals - www.sysinternals.com

 <unrelated text removed>

RDTSCP          * Supports RDTSCP instruction
TSC             * Supports RDTSC instruction
TSC-DEADLINE    - Local APIC supports one-shot deadline timer
TSC-INVARIANT   * TSC runs at constant rate
```

</dd> <dt>

<span id="Does_QPC_work_reliably_on__hardware_platforms_"></span><span id="does_qpc_work_reliably_on__hardware_platforms_"></span><span id="DOES_QPC_WORK_RELIABLY_ON__HARDWARE_PLATFORMS_"></span>**QPC 是否能在 Windows RT PC 硬體平臺上可靠地工作？**
</dt> <dd>

Yes

</dd> <dt>

<span id="How_often_does_QPC_roll_over_"></span><span id="how_often_does_qpc_roll_over_"></span><span id="HOW_OFTEN_DOES_QPC_ROLL_OVER_"></span>**QPC 變換的頻率為何？**
</dt> <dd>

從最近的系統開機不到100年，而且可能會根據使用的基礎硬體計時器而更久。 在大部分的應用程式中，變換並不重要。

</dd> <dt>

<span id="What_is_the_computational_cost_of_calling_QPC_"></span><span id="what_is_the_computational_cost_of_calling_qpc_"></span><span id="WHAT_IS_THE_COMPUTATIONAL_COST_OF_CALLING_QPC_"></span>**呼叫 QPC 的計算成本為何？**
</dt> <dd>

[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)的計算呼叫成本主要是由基礎硬體平臺所決定。 如果使用 TSC 註冊作為 QPC 的基礎，則計算成本主要取決於處理器處理 **RDTSC** 指令所需的時間長度。 這段時間的範圍是從 CPU 迴圈10s 到數百個 CPU 迴圈，視所使用的處理器而定。 如果無法使用 TSC，系統將會選取不同的硬體時間。 因為這些時間基底位於主機板上 (例如，在 PCI 南橋接器或 PCH) 上，個別呼叫計算成本高於 TSC，而且通常會在 0.8-1.0 毫秒的鄰近範圍中，視處理器速度和其他硬體因素而定。 這項成本的依據是存取主機板上的硬體裝置所需的時間。

</dd> <dt>

<span id="Does_QPC_require_a_kernel_transition__system_call__"></span><span id="does_qpc_require_a_kernel_transition__system_call__"></span><span id="DOES_QPC_REQUIRE_A_KERNEL_TRANSITION__SYSTEM_CALL__"></span>**QPC 是否需要 (系統呼叫) 的核心轉換？**
</dt> <dd>

如果系統可以使用 TSC 註冊作為 [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)的基礎，則不需要進行核心轉換。 如果系統必須使用不同的時間基底（例如 HPET 或 PM 計時器），則需要系統呼叫。

</dd> <dt>

<span id="Is_the_performance_counter_monotonic__non-decreasing__"></span><span id="is_the_performance_counter_monotonic__non-decreasing__"></span><span id="IS_THE_PERFORMANCE_COUNTER_MONOTONIC__NON-DECREASING__"></span>**效能計數器單純 (非遞減) ？**
</dt> <dd>

Yes

</dd> <dt>

<span id="Can_the_performance_counter_be_used_to_order_events_in_time_"></span><span id="can_the_performance_counter_be_used_to_order_events_in_time_"></span><span id="CAN_THE_PERFORMANCE_COUNTER_BE_USED_TO_ORDER_EVENTS_IN_TIME_"></span>**效能計數器可以用來排序時間內的事件嗎？**
</dt> <dd>

是。 不過，在比較從不同執行緒取得的效能計數器結果時，依±1刻度差異的值會有不明確的順序，如同它們具有相同的時間戳記一樣。

</dd> <dt>

<span id="How_accurate_is_the_performance_counter_"></span><span id="how_accurate_is_the_performance_counter_"></span><span id="HOW_ACCURATE_IS_THE_PERFORMANCE_COUNTER_"></span>**效能計數器的精確度為何？**
</dt> <dd>

答案取決於各種不同的因素。 如需詳細資訊，請參閱 [低層級硬體時鐘特性](#low-level-hardware-clock-characteristics)。

</dd> </dl>

## <a name="faq-about-programming-with-qpc-and-tsc"></a>使用 QPC 和 TSC 進行程式設計的常見問題

以下是使用 [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) 和 TSCs 進行程式設計的常見問題的解答。

<dl> <dt>

<span id="I_need_to_convert_the_QPC_output_to_milliseconds._How_can_I_avoid_loss_of_________precision_with_converting_to_double_or_float_"></span><span id="i_need_to_convert_the_qpc_output_to_milliseconds._how_can_i_avoid_loss_of_________precision_with_converting_to_double_or_float_"></span><span id="I_NEED_TO_CONVERT_THE_QPC_OUTPUT_TO_MILLISECONDS._HOW_CAN_I_AVOID_LOSS_OF_________PRECISION_WITH_CONVERTING_TO_DOUBLE_OR_FLOAT_"></span>**我需要將 QPC 輸出轉換成毫秒。如何避免因為轉換成 double 或 float 而失去精確度？**
</dt> <dd>

在整數效能計數器上執行計算時，有幾件事要牢記在心：

-   整數除法將會遺失餘數。 這可能會導致在某些情況下遺失精確度。
-   64位整數和浮點數之間的轉換 (double) 可能會導致精確度遺失，因為浮點數尾數無法表示所有可能的整數值。
-   64位整數的乘法會導致整數溢位。

一般來說，請盡可能延遲這些計算和轉換，以避免複合所引進的錯誤。

</dd> <dt>

<span id="How_can_I_convert_QPC_to_100_nanosecond_ticks_so_I_can_add_it_to_a_________FILETIME_"></span><span id="how_can_i_convert_qpc_to_100_nanosecond_ticks_so_i_can_add_it_to_a_________filetime_"></span><span id="HOW_CAN_I_CONVERT_QPC_TO_100_NANOSECOND_TICKS_SO_I_CAN_ADD_IT_TO_A_________FILETIME_"></span>**如何將 QPC 轉換為100毫微秒的刻度，以便將它新增至 FILETIME？**
</dt> <dd>

檔案時間是64位的值，代表自上午12:00 以來經過的 100-毫微秒間隔數。 1601年1月1日國際標準時間 (UTC) 。 傳回當日時間的 WIN32 API 呼叫（例如 [**GetSystemTimeAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimeasfiletime) 和 [**GetSystemTimePreciseAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime)）會使用檔案時間。 相反地， [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) 會傳回代表時間的值，單位為 1/ (從 [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency)) 取得之效能計數器的頻率。 兩者之間的轉換需要計算 **QPC** 間隔和 100-毫微秒間隔的比率。 請小心避免遺失精確度，因為這些值可能很小 (0.0000001/0.000000340) 。

</dd> <dt>

<span id="Why_is_the_time_stamp_that_is_returned_from_QPC_a_signed_integer_"></span><span id="why_is_the_time_stamp_that_is_returned_from_qpc_a_signed_integer_"></span><span id="WHY_IS_THE_TIME_STAMP_THAT_IS_RETURNED_FROM_QPC_A_SIGNED_INTEGER_"></span>**為什麼從 QPC 帶正負號的整數傳回的時間戳記？**
</dt> <dd>

涉及 [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) 時間戳記的計算可能牽涉到減法。 藉由使用帶正負號的值，您可以處理可能產生負數值的計算。

</dd> <dt>

<span id="How_can_I_obtain_high_resolution_time_stamps_from_managed_code_"></span><span id="how_can_i_obtain_high_resolution_time_stamps_from_managed_code_"></span><span id="HOW_CAN_I_OBTAIN_HIGH_RESOLUTION_TIME_STAMPS_FROM_MANAGED_CODE_"></span>**如何從受控碼取得高解析度的時間戳記？**
</dt> <dd>

從 [**GetTimeStamp**](/previous-versions/windows/) 方法中，呼叫 [**system.object**](/previous-versions/windows/) 。 如需如何使用 **GetTimeStamp** 的範例，請參閱 [從 managed 程式碼取得高解析度的時間戳記](#acquiring-high-resolution-time-stamps-from-managed-code)。

</dd> <dt>

<span id="Under_what_circumstances_does_QueryPerformanceFrequency_return_FALSE__or_________QueryPerformanceCounter_return_zero_"></span><span id="under_what_circumstances_does_queryperformancefrequency_return_false__or_________queryperformancecounter_return_zero_"></span><span id="UNDER_WHAT_CIRCUMSTANCES_DOES_QUERYPERFORMANCEFREQUENCY_RETURN_FALSE__OR_________QUERYPERFORMANCECOUNTER_RETURN_ZERO_"></span>**在何種情況下，QueryPerformanceFrequency 會傳回 FALSE，或 QueryPerformanceCounter 會傳回零？**
</dt> <dd>

這不會發生在 Windows XP 或更新版本執行的任何系統上。

</dd> <dt>

<span id="Do_I_need_to_set_the_thread_affinity_to_a_single_core_to_use_QPC_"></span><span id="do_i_need_to_set_the_thread_affinity_to_a_single_core_to_use_qpc_"></span><span id="DO_I_NEED_TO_SET_THE_THREAD_AFFINITY_TO_A_SINGLE_CORE_TO_USE_QPC_"></span>**我是否需要將執行緒親和性設定為單一核心，才能使用 QPC？**
</dt> <dd>

不會。 如需詳細資訊，請參閱 [取得時間戳記的指引](#guidance-for-acquiring-time-stamps)。 這不是必要的，也不是理想的情況。 如果有多個執行緒在呼叫 [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)時將其親和性設定為相同的核心，執行此案例可能會將處理限制為一個核心，或在單一核心上建立瓶頸，進而對您的應用程式效能造成負面影響。

</dd> </dl>

## <a name="low-level-hardware-clock-characteristics"></a>低層級硬體時鐘特性

這些區段會顯示低層級的硬體時鐘特性。

### <a name="absolute-clocks-and-difference-clocks"></a>絕對時鐘和差異時鐘

絕對時鐘可提供正確的每日讀取時間。 它們通常是以國際標準時間 (UTC) 為基礎，因此其精確度取決於它們同步至外部時間參考的程度。 差異時鐘測量時間間隔，通常不是以外部時間 epoch 為基礎。 [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) 是不同的時鐘，而且未同步處理至外部時間 epoch 或參考。 當您使用 **QPC** 進行時間間隔測量時，您通常會得到比使用衍生自絕對時鐘的時間戳記更好的精確度。 這是因為同步處理絕對時鐘時間的程式可能會導致階段和頻率移位，從而提高短期時間間隔測量的不確定性。

### <a name="resolution-precision-accuracy-and-stability"></a>解析度、有效位數、精確度和穩定性

[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) 會使用硬體計數器作為基礎。 硬體計時器包含三個部分：滴答產生器、計算刻度的計數器，以及用來抓取計數器值的方法。 這三個元件的特性會決定 **QPC** 的解析度、有效位數、精確度和穩定性。

如果硬體產生器以固定速率提供刻度，只要計算這些刻度，即可測量時間間隔。 產生滴答的速率稱為「頻率」，並以赫茲 (Hz) 表示。 相較之下，頻率稱為「期間」或「滴答間隔」，並以適當的國際系統單位來表示 (SI) 時間單位 (例如，第二、毫秒、微秒或毫微秒) 。

![時間間隔](images/tick-interval.png)

計時器的解析度等於句號。 解決方式會決定區別任何兩個時間戳記的能力，並在可以測量的最小時間間隔下放置較低的界限。 這有時稱為「滴答解析」。

數位測量時間引進了±1刻度的測量不確定性，因為數位計數器會在離散步驟中前進，而時間會持續前進。 這種不確定性稱為「量化錯誤」。 針對一般時間間隔測量，通常會忽略此效果，因為量化錯誤比測量的時間間隔小很多。

![數位時間度量](images/digital-time-measure.png)

但是，如果要測量的期間很小，並接近計時器的解析度，您就必須考慮此量化錯誤。 所引進的錯誤大小是一個時鐘期間的大小。

下列兩個圖表說明使用具有1個時間單位之解析度的計時器，對±1滴答不確定性的影響。

![滴答不確定性](images/tick-uncertainty.png)

[**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) 會傳回 [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)的頻率，且句點和解析度等於此值的倒數。 **QueryPerformanceFrequency** 傳回的效能計數器頻率是在系統初始化期間決定，而且在系統執行時不會變更。

> [!Note]  
> 案例可能存在，而 [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) 不會傳回硬體滴答產生器的實際頻率。 例如，在許多情況下， **QueryPerformanceFrequency** 會傳回依1024的 TSC 頻率除以;而在 Hyper-v 上，當來賓虛擬機器在執行程式管理 [版本1.0 介面](https://msdn.microsoft.com/library/Ff541458(v=VS.85).aspx)的 [虛擬](https://msdn.microsoft.com/library/Ff542584(v=VS.85).aspx)程式下執行時，效能計數器的頻率一律為 10 MHz。 因此，請不要假設 **QueryPerformanceFrequency** 會傳回精確的 TSC 頻率。

 

[**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)會讀取效能計數器，並傳回啟動 Windows 作業系統之後發生的總滴答數，包括電腦處於睡眠狀態的時間，例如待命、休眠或連線待命。

這些範例示範如何計算滴答間隔和解決方式，以及如何將滴答計數轉換成時間值。

<dl> <dt>

<span id="Example_1"></span><span id="example_1"></span><span id="EXAMPLE_1"></span>**範例1**
</dt> <dd>

[**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) 會在特定電腦上傳回值3125000。 這台電腦上的 [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) 度量的滴答間隔和解析度為何？ 滴答間隔（或期間）是3125000的倒數，也就是 0.000000320 (320 毫微秒) 。 因此，每個刻度都代表傳遞320毫微秒。 無法在這部電腦上測量小於320毫微秒的時間間隔。

滴答間隔 = 1/ (效能頻率) 

滴答間隔 = 1/3125000 = 320 ns

</dd> <dt>

<span id="Example_2"></span><span id="example_2"></span><span id="EXAMPLE_2"></span>**範例2**
</dt> <dd>

在與上述範例相同的電腦上，從兩次連續呼叫 [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) 傳回的值的差異為5。 兩次呼叫之間經過了多少時間？ 5個刻度乘以320毫微秒會產生1.6 微秒。

經過時間 = 滴答 \* 滴答間隔

經過時間 = 5 \* 320 ns = 1.6 μs

</dd> </dl>

從軟體存取 (讀取) 滴答計數器需要一些時間，而且此存取時間可以減少時間測量的精確度。 這是因為最小間隔時間 (可測量的最小時間間隔) 是解析度的較大和存取時間。

Precision = MAX \[ 解析，AccessTime\]

例如，假設有一個假設性的硬體計時器，其解析度為100的毫微秒，以及800納秒的存取時間。 如果使用平臺計時器而非使用 TSC 登錄作為 [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)基礎，則可能會發生這種情況。 因此，精確度會是800毫微秒，不是100毫微秒，如這項計算所示。

Precision = MAX \[ 800 ns，100 ns \] = 800 ns

這兩個圖表描述此效果。

![qpc 存取時間](images/qpc-access-time.png)

如果存取時間大於解決方式，請不要嘗試透過猜測來改善精確度。 換句話說，假設時間戳記是在中間，或是在呼叫的開頭或結尾時，就會發生錯誤。

相反地，請考慮下列範例，其中 [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) 存取時間只有20個納秒，而硬體時鐘解析度為100毫微秒。 如果使用 TSC 登錄作為 **QPC** 的基礎，則可能會發生這種情況。 在這裡，精確度會受限於時鐘解析。

![qpc 精確度](images/qpc-precision.png)

在實務上，您可以找到讀取計數器所需時間大於或小於解析度的時間來源。 無論是哪一種情況，精確度都會是兩者中較大的一個。

下表提供各種時鐘的大約解析、存取時間和精確度的相關資訊。 請注意，有些值會隨著不同的處理器、硬體平臺和處理器速度而有所不同。



| 時鐘來源                                                      | 名義時鐘頻率 | 時鐘解析    | 存取時間 (一般)  | 精確度       |
|-------------------------------------------------------------------|-------------------------|---------------------|-----------------------|-----------------|
| 電腦 RTC                                                            | 64 Hz                   | 15.625 毫秒 | N/A                   | N/A             |
| 使用具有 3 GHz 處理器時鐘的 TSC 的查詢效能計數器  | 3 MHz                   | 333毫微秒     | 30毫微秒        | 333毫微秒 |
| 在具有 3 GHz 週期時間的系統上 **RDTSC** 機器指令 | 3 GHz                   | 333 picoseconds     | 30毫微秒        | 30毫微秒  |



 

由於 [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) 會使用硬體計數器，因此當您瞭解硬體計數器的一些基本特性時，您會瞭解 **QPC** 的功能和限制。

最常使用的硬體滴答產生器是 crystal oscillator。 Crystal 是一小部分的 quartz 或其他 ceramic 材質，展示 piezoelectric 的特性，可提供價格實惠的頻率參考，並具備絕佳的穩定性和精確度。 此頻率可用來產生時鐘所計算的刻度。

計時器的精確度是指符合 true 或標準值的一致性程度。 這主要取決於 crystal oscillator 能以指定的頻率提供刻度。 如果震盪的頻率過高，時鐘將會「快速執行」，且測量的間隔將會比實際時間更長;而且，如果頻率過低，時鐘將會「執行緩慢」，且測量的間隔會比實際的時間短。

針對短暫期間的一般時間間隔度量 (例如，回應時間測量、網路延遲測量等等) ，硬體 oscillator 的精確度通常就已足夠。 不過，對於某些測量，oscillator 頻率的精確度會變得很重要，特別是在長時間間隔內，或當您想要比較在不同電腦上所做的度量時。 本節的其餘部分將探索 oscillator 精確度的影響。

Crystals 的震盪頻率是在製造過程中設定的，製造商會以指定的頻率加上或減去製造容忍度（以「每百萬個部分」表示的製造容忍度為單位） (ppm) ，稱為最大頻率位移。 如果其實際頻率介於 999990 Hz 和 1000010 Hz 之間，則指定頻率為 1000000 Hz 且最大頻率位移為± 10 ppm 的 crystal 會在規格限制內。

藉由以每秒每秒的毫秒數來取代片語部分，我們可以將此頻率位移誤差套用至時間間隔測量。 具有 + 10 ppm 位移的 oscillator 會有每秒10毫秒的錯誤。 因此，當測量1秒的間隔時，它會快速執行，並將1秒的間隔測量為0.999990 秒。

很方便的參考是，100 ppm 的頻率錯誤會在24小時後導致8.64 秒的錯誤。 由於累積的錯誤較長的時間間隔，此資料表會顯示測量不確定性。



| 時間間隔持續時間 | 因具有 +/-10 PPM 頻率容錯之累積錯誤的測量不確定性 |
|------------------------|--------------------------------------------------------------------------------------|
| 1微秒          | ± 10 picoseconds (10-12)                                                              |
| 1毫秒          | ±10毫微秒 (10-9)                                                               |
| 1 秒               | ±10毫秒                                                                    |
| 1 小時                 | ±60微秒                                                                    |
| 1 日                  | ±0.86 秒                                                                       |
| 1 週                 | ±6.08 秒                                                                       |



 

上表顯示針對較短的時間間隔，頻率位移誤差通常可以忽略。 不過，在長時間間隔內，即使是較小的頻率位移，也可能造成大量的測量不確定性。

在個人電腦和伺服器中使用的 Crystal 聲音振盪器通常會以±30到50個部分的頻率承受度製造，而且很少 crystals 可以離 500 ppm。 雖然 crystals 具有更緊密的頻率位移容限，但它們較昂貴，因此不會在大部分的電腦中使用。

若要降低此頻率位移錯誤的負面影響，最新版本的 Windows，特別是 Windows 8，請使用多個硬體計時器來偵測頻率位移，並將其補償到可能的程度。 當 Windows 啟動時，就會執行此校正程式。

如下列範例所示，硬體時鐘的頻率位移錯誤會影響可達成的精確度，而且時鐘的解析度可能較不重要。

![頻率位移錯誤會影響可達成的精確度](images/freq-offset-error.png)

<dl> <dt>

<span id="Example_1"></span><span id="example_1"></span><span id="EXAMPLE_1"></span>**範例1**
</dt> <dd>

假設您使用 1 MHz oscillator （具有1微秒的解析度，以及± 50 ppm 的最大頻率位移誤差）來執行時間間隔測量。 現在，讓我們假設位移正好是 + 50 ppm。 這表示實際的頻率會是 1000050 Hz。 如果我們測量的是24小時的時間間隔，我們的測量會是4.3 秒太短 (23：59：55.700000 測量與24：00：00.000000 實際) 。

一天中的秒數 = 86400

頻率位移錯誤 = 50 ppm = 0.00005

86400秒 \* 0.00005 = 4.3 秒

</dd> <dt>

<span id="Example_2"></span><span id="example_2"></span><span id="EXAMPLE_2"></span>**範例2**
</dt> <dd>

假設處理器 TSC 時鐘由 crystal oscillator 控制，並指定頻率為 3 GHz。 這表示解析度會是 1/3000000000 或約 333 picoseconds。 假設用來控制處理器時鐘的 crystal 具有± 50 ppm 的頻率容錯，其實是 + 50 ppm。 儘管有令人印象深刻的解決方式，但24小時的時間間隔量值仍會是4.3 秒太短。  (23：59：55.7000000000 測量與24：00：00.0000000000 實際) 。

一天中的秒數 = 86400

頻率位移錯誤 = 50 ppm = 0.00005

86400秒 \* 0.00005 = 4.3 秒

這會顯示高解析度的 TSC 時鐘不一定能提供比較低解析度時鐘更精確的度量。

</dd> <dt>

<span id="Example_3"></span><span id="example_3"></span><span id="EXAMPLE_3"></span>**範例3**
</dt> <dd>

請考慮使用兩部不同的電腦來測量相同的24小時時間間隔。 這兩部電腦都有一個 oscillator，最大頻率位移為± 50 ppm。 這兩個系統上的相同時間間隔可以有多遠？ 如同先前的範例，± 50 ppm 會在24小時後產生最多±4.3 秒的錯誤。 如果有一個系統快速執行4.3 秒，而另一個4.3 秒的速度變慢，24小時之後的最大錯誤可能會是8.6 秒。

一天中的秒數 = 86400

頻率位移錯誤 = ± 50 ppm = ±0.00005

± (86400 秒 \* 0.00005) = ±4.3 秒

兩個系統之間的最大位移 = 8.6 秒

總而言之，測量長時間間隔以及比較不同系統之間的度量時，頻率位移誤差會變得越來越重要。

計時器的穩定性描述滴答頻率是否會隨著時間而改變，例如溫度變更的結果。 使用 Quartz crystals 做為電腦上的滴答產生器，會以頻率的函式來呈現較小的頻率變更。 相較于一般溫度範圍的頻率位移錯誤，散熱漂移所造成的錯誤通常很小。 不過，受限於大型溫度波動的可攜式裝置或設備的軟體設計人員可能需要考慮此效果。

</dd> </dl>

## <a name="hardware-timer-info"></a>硬體計時器資訊

<dl> <dt>

<span id="TSC_Register"></span><span id="tsc_register"></span><span id="TSC_REGISTER"></span>**TSC 註冊**
</dt> <dd>

某些 Intel 和 AMD 處理器包含的 TSC 暫存器是64位暫存器，它會以較高的速率增加，通常等於處理器時鐘。 您可以透過 **RDTSC** 或 **RDTSCP** 機器指示讀取此計數器的值，以數十或數百部機器週期的順序提供非常低的存取時間和計算成本，視處理器而定。

雖然 TSC 登錄看起來像是理想的時間戳記機制，但在此情況下，它無法針對 timekeeping 用途可靠地運作：

-   並非所有處理器都有 TSC 登錄，因此使用軟體中的 TSC 註冊可直接建立可攜性問題。 在此情況下， (Windows 會為 [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)選取替代的時間來源，以避免可攜性問題。 ) 
-   有些處理器可能會改變 TSC 時鐘的頻率，或停止 TSC 登錄的進展，讓 TSC 不適合這些處理器上的時間用途。 這些處理器稱為具有非不變的 TSC 登錄。  (Windows 會自動偵測到此情況，並為 [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)) 選取替代的時間來源。
-   在多處理器或多核心系統上，有些處理器和系統無法將每個核心上的時鐘同步處理為相同的值。  (Windows 會自動偵測到此情況，並為 [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)) 選取替代的時間來源。
-   在某些大型的多處理器系統上，即使處理器具有不變的 TSC，您可能還是無法將處理器時鐘同步處理為相同的值。  (Windows 會自動偵測到此情況，並為 [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)) 選取替代的時間來源。
-   有些處理器會依序執行指令。 當使用 **RDTSC** 來時間指令序列時，這可能會導致不正確的迴圈計數，因為 **RDTSC** 指令可能會在您的程式中指定的時間以外執行。 已在某些處理器上引進 **RDTSCP** 指令，以回應此問題。

與其他計時器一樣，TSC 是以 crystal oscillator 為基礎，其確切的頻率不事先知道，而且有頻率位移錯誤。 因此，在使用之前，必須使用另一個時間參考來校正。

在系統初始化期間，Windows 會檢查 TSC 是否適用于時間用途，並執行必要的頻率校正和核心同步處理。

</dd> <dt>

<span id="PM_Clock"></span><span id="pm_clock"></span><span id="PM_CLOCK"></span>**PM 時鐘**
</dt> <dd>

ACPI 計時器（也稱為 PM 時鐘）已新增至系統架構，以提供可靠的時間戳記，而不受處理器速度影響。 因為這是此計時器的單一目標，所以它會在單一時鐘週期中提供時間戳記，但不會提供任何其他功能。

</dd> <dt>

<span id="HPET_Timer"></span><span id="hpet_timer"></span><span id="HPET_TIMER"></span>**HPET 計時器**
</dt> <dd>

高精確度事件計時器 (HPET) 是由 Intel 和 Microsoft 共同開發，以符合多媒體和其他時效性應用程式的時間需求。 HPET 支援自 Windows Vista 起 Windows，Windows 7 和 Windows 8 硬體標誌認證需要硬體平臺的 HPET 支援。

</dd> </dl>

 

 
