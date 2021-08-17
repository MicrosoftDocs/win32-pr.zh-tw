---
title: Windows 標題的主要問題
description: 本文將重點放在目前產生的電腦遊戲中，我們看到了許多常見的問題。
ms.assetid: 89b83473-1aa9-9a2d-8778-15cfb91cdea4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b89be8ad7a68c247d589f304ea77fa9b3e63e105739264e39f71794c705b66cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118396503"
---
# <a name="top-issues-for-windows-titles"></a>Windows 標題的主要問題

Microsoft Windows 遊戲和圖形技術開發人員關係群組會為每年的許多 Windows 遊戲執行效能分析。 在這些課程中，我們會取得實際操作體驗，以系結至每天收到的開發人員意見反應和查詢。 有時候我們會協助您追蹤標題中有神秘的損毀或其他問題，讓我們進一步瞭解開發人員遇到的問題。

本文將重點放在目前產生的電腦遊戲中，我們看到了許多常見的問題。

-   [CPU-有限效能](#cpu-limited-performance)
-   [不良的 Batch 管理](#poor-batch-management)
-   [記憶體複製過多](#excessive-memory-copying)
-   [過度使用動態繪圖提交](#excessive-use-of-dynamic-draw-submission)
-   [檔案處理的高度負擔](#high-overhead-in-file-processing)
-   [緩慢且挫折的安裝](#slow-and-frustrating-installation)
-   [缺乏實體記憶體的考慮](#lack-of-consideration-of-physical-memory)
-   [過度依賴 Real-Time 音訊取樣率轉換](#over-reliance-on-real-time-audio-sample-rate-conversion)
-   [虛擬記憶體的分散程度](#fragmention-of-virtual-memory)
-   [操作 Floating-Point 控制字組](#manipulation-of-the-floating-point-control-word)
-   [選用的 DirectX 執行時間安裝](#optional-installation-of-the-directx-runtime)
-   [過度使用執行緒同步處理](#excessive-use-of-thread-synchronization)
-   [使用 RDTSC](#use-of-rdtsc)

## <a name="cpu-limited-performance"></a>CPU-Limited 效能

大部分的遊戲在具有高效能圖形處理器 (Gpu) 的系統上受到 CPU 效能的限制。 這有時是因為對繪製提交使用批次處理不佳，但更常見的原因是其他遊戲系統耗用大量可用的 CPU 週期。 在我們已將 GPU 視為限制的幾種情況下，其原因是很高的填滿率或圖元著色器需求、高解析度設定，或視訊卡的低頂點著色器效能。

因為大部分的標題都有 CPU 限制，所以最大的效能獲勝來自于將需要大量 CPU 的遊戲系統優化。 一般而言，AI 或物理系統以及相關聯的衝突偵測邏輯，是在正常運作的 Microsoft Direct3D 應用程式中，CPU 週期的主要取用者。 改善這些系統的任何工作，都可以改善遊戲的整體效能。

## <a name="poor-batch-management"></a>不良的 Batch 管理

使用 GPU 達成良好的平行處理原則時，繪製批次必須包含足夠的幾何，而著色器有正確的複雜度，讓視訊卡保持忙碌，而不使用太多批次來處理命令緩衝區。 在目前世代的硬體上，我們建議每個畫面上大約300或更少的繪圖批次提交 (較低效能的 Cpu) ，以防止驅動程式處理命令緩衝區成為效能瓶頸。 有些其他的 API 狀態呼叫和驅動程式組合可能會產生昂貴的 CPU 處理 (驅動程式編譯著色器，例如) ，因此強烈建議進行例行的效能分析。

## <a name="excessive-memory-copying"></a>記憶體複製過多

在開發大部分的電腦標題期間，開發人員會使用方便的資料結構和字串進行內容管理。 字串比較、複製和其他操作所需的 CPU 工作量通常具有可測量的額外負荷，尤其是在考慮與快取和記憶體子系統相關聯的效能點擊時。 當產品進入主要測試和發行階段之後，在開發這些系統來移除或最小化依賴字串處理的情況時，應該進行規劃。

## <a name="excessive-use-of-dynamic-draw-submission"></a>過度使用動態繪圖提交

新式的影片硬體在處理靜態資料時執行得很順利。 高階介面卡通常會有非常大量的影片記憶體，但動態資料無法有效利用此記憶體。

雖然動態頂點緩衝區/索引緩衝區的有效使用模式可以針對動態內容來執行，但許多標題仍會使用這種方法來進行靜態內容的其他用途。 我們最常看到的是二進位空間分割 (BSP) 樹狀結構和以入口網站為基礎的系統，這些系統會將幾何儲存在未對應至硬體的資料結構中，且必須針對每個畫面格處理到緩衝區。 盡可能將最多的內容放入靜態資源，可大幅降低將資料傳送至視訊卡的頻寬負荷、更充分利用內部 VRAM，並減少處理此內容所涉及的 CPU/快取額外負荷。

## <a name="high-overhead-in-file-processing"></a>檔案處理的高度負擔

電腦遊戲已取得較長載入時間的信譽，特別是與具有嚴格載入時間需求的主控台標題相較之下。 我們對許多標題使用檔案子系統的方式進行分析，會顯示一些常見的問題。

開啟檔案的額外負荷通常比開發人員預期更高。 利用廣泛使用的隨選病毒掃描程式和 NTFS 的額外功能，開啟檔案是相當昂貴的作業。 一次開啟多個檔案或重複開啟和關閉相同的檔案，因此處理檔案管理的方法不佳。 有些遊戲試圖藉由在開啟檔案之前測試是否存在，來降低此效能成本。 實際的情況是，測試檔案在 NTFS 上是否存在，需要開啟檔案，因此在開啟結果之前先進行測試，再將成本支付兩次。

如果遊戲允許附加元件的修改或 mods >，或仍包含開發架構來檢查覆寫資料檔案，可能會因為檢查這些檔案而造成載入遊戲的延遲，即使這些檔案不存在也一樣。 建議遊戲在以特殊命令列參數或其他模式指標執行時，只檢查這些檔案，如此一來，只有使用這項功能的使用者才會實際支付這些 (的效能成本，通常會) 檢查。

您可以從檔案系統取得額外的效能，如下所示：

-   適當使用檔案系統提示檔案旗標 \_ \_ 隨機 \_ 存取和檔案旗 \_ 標 \_ 順序 \_ 掃描
-   調整緩衝區大小，以避免對作業系統的讀取/寫入 Api 進行大量呼叫
-   以非同步方式存取檔案
-   在背景載入執行緒

我們也強烈建議在組建或安裝期間將資料離線 (轉換) 而不是在第一次執行遊戲時依賴轉換，因為這樣做會為每位使用者帶來明顯的效能稅金。

## <a name="slow-and-frustrating-installation"></a>緩慢且挫折的安裝

我們看到的另一個常見問題是許多新式電腦遊戲所需的安裝時間很長。 安裝程式會提示使用者許多次，有時候只是告訴使用者，例如「您不需要安裝 DirectX」。 一般而言，這些違規的安裝程式需要使用者在安裝遊戲之前，先選取 **[下一步** **] 或 [確定]** ，然後才開始安裝遊戲。 開始之後，我們看過一些標題需要一小時或更長的時間，使用者才會獲得播放遊戲的機會。 我們強烈認為遊戲播放體驗的第一個小時不應該是安裝。

我們建議使用許多方法來處理安裝。 首先，讓提示保持簡單且最小。 其次，架構您的遊戲資料，讓部分或全部資料檔案可以在可能的情況下直接從散發磁片使用—新式 DVD 光碟機的頻寬非常高。 第三，請考慮在您的標題中執行隨選安裝，以減少或消除安裝程式，並讓使用者能夠儘快進入遊戲中。  (如需安裝隨選安裝的詳細資訊，請參閱 [適用于遊戲的隨選安裝](/windows/desktop/DxTechArts/install-on-demand-for-games)。 ) 

如需更多關於遊戲安裝的建議，請參閱 [簡化遊戲安裝](/windows/desktop/DxTechArts/simplifying-game-installation)。

## <a name="lack-of-consideration-of-physical-memory"></a>缺乏實體記憶體的考慮

由於市場上的電腦硬體有各式各樣的變化，因此標題通常會使用臨機操作設定測試來選取圖形詳細資料層級的預設設定。 我們看到的部分標題是在這些測試中使用影片記憶體大小，但無法使其與實體記憶體大小產生關聯。 為了處理遺失裝置的狀況，大部分的視訊記憶體 (卡上的本機 VRAM 和非本機的 AGP 記憶體光圈) 都必須透過使用受控資源或自訂資料結構，由實體記憶體支援。 某些高階視訊卡的 VRAM 大小 rivaling 低終端 CPU 記憶的大小。 相較于視訊卡，系統的實體記憶體有限，大部分的 VRAM 都無法有效使用，且應設定較低的詳細設定。

## <a name="over-reliance-on-real-time-audio-sample-rate-conversion"></a>Real-Time 音訊取樣率轉換 Over-Reliance

當音訊系統必須在混合到硬體緩衝區期間轉換播放速率時，就會看到另一個常見的 CPU 週期燒錄來源。 使用 Windows Driver Model (WDM) 驅動程式時，硬體緩衝區格式不受直接應用程式控制，因為它是核心層級的資源;相反地，會根據所有來源的最高品質格式以及硬體的功能，來選取格式。 根據預設，Windows XP 會針對此程式使用高品質的取樣率轉換，而且如果大部分的音訊範例都需要速率轉換，就會耗用 CPU 週期的重要部分。

建議您使用相同的取樣率來建立所有 DirectSound 緩衝區。 如果您使用 Microsoft Win32 **waveOut** 函式，您也應該使用一致的取樣率。 使用 WDM 驅動程式時，核心會將緩衝區全部混合，而如果您對某些緩衝區使用較高的取樣率，則所有其餘部分的取樣率將會轉換成相符的。 請注意，這表示所有音訊範例都使用相同的播放速率，包括任何串流音訊解壓縮緩衝區。 除非您的目標是 Windows 98 或 Windows Millennium Edition，否則設定主要緩衝區速率沒有任何作用。

> [!Note]  
> 在 Windows Vista 和更新版本的作業系統上，DirectSound 和 **waveOut** 會針對所有音訊輸出使用 [Windows 音訊會話 API (WASAPI)](/windows/desktop/CoreAudio/wasapi) 。

 

## <a name="fragmention-of-virtual-memory"></a>虛擬記憶體的分散程度

我們已在處理常式記憶體空間上看到許多與32位限制相關的最新問題。 雖然使用者模式進程的 2 GB 虛擬位址空間已超過一段時間，但增加了大型記憶體對應檔的使用、自訂記憶體配置器，以及增加 VRAM 大小 (必須對應到進程) 空間，才能導致虛擬記憶體空間配置失敗的情況。 某些非 Microsoft Dll 會在虛擬位址空間的中間使用固定的位置，這會導致產生失敗的分配。

當遊戲利用自訂記憶體配置配置來嘗試配置大型連續的虛擬記憶體空間時，最常出現這些問題。 我們的建議是撰寫配置器，讓它們視需要要求更合理大小的虛擬位址空間部分。 例如，一次要求64或 256 MB，但不是 1 GB。 不過，請務必小心，不要造成進一步的片段。 64位作業系統和硬體的問世將大幅説明這些問題，但必須特別注意目前的32位系統。

## <a name="manipulation-of-the-floating-point-control-word"></a>操作 Floating-Point 控制字組

在偵錯工具中，某些開發人員已透過浮點控制字組的操作，在浮點單位上啟用例外狀況 (FPU) 。 這麼做會造成極大的問題，而且可能會導致程式損毀。 就像呼叫慣例一樣，系統會要求保留 ebx 登錄，而大部分的系統都會假設 FPU 處於預設狀態，將會提供合理的結果，而不會產生例外狀況。 驅動程式和其他系統元件通常會根據假設在暫存器中出現不正確狀況的標準錯誤值來計算結果，但如果已啟用例外狀況，這些將會被未處理，並導致損毀。

除非使用 D3DCREATE FPU PRESERVE 旗標，否則 Direct3D 會將浮點單位設為單精確度浮點數，並將其四捨五入為最接近的初始設定，除非使用了 \_ FPU \_ PRESERVE 旗標，在這種情況下，浮點控制字組會維持不變。 因為控制字組是每個執行緒的設定，所以確保所有應用程式執行緒都設定為單精確度模式，可能會將效能優化。 請記住，呼叫 [**\_ control87**](https://msdn.microsoft.com/library/e9b52ceh(v=VS.71).aspx)對 x64 原生程式碼而言是不正確，它會改為使用 SSE，而且在 Xbox 360 CPU 的 PowerPC 架構架構上相當昂貴。

> [!Note]  
> 如果您修改了控制字組，請使用 [**\_ controlfp \_**](https://msdn.microsoft.com/library/c9676k6h(v=VS.80).aspx) ，請注意，對於 x64 平臺，您無法透過控制字組變更浮點精確度。

 

在需要不同舍入規則或其他行為的任何程式庫中（例如處理軟體頂點著色器或編譯），我們會儲存並還原控制字組。 如果遊戲需要使用非標準的舍入或 FPU 例外狀況，它應該儲存並還原浮點控制字組，您應該確定它不會呼叫未經過證實的任何外部程式碼，而不會受到這些問題的保護，包括系統 Api。

## <a name="optional-installation-of-the-directx-runtime"></a>選用的 DirectX 執行時間安裝

許多遊戲會詢問使用者是否要安裝 DirectX。 如果使用者假設系統已安裝最新的 DirectX 可轉散發套件並跳過安裝，則這可能會導致問題，並在後續安裝成功時繼續進行。 如果遊戲需要特定版本的 D3DX 或其他未安裝的更新功能，遊戲將無法運作，且使用者將會感到非常挫折。

強烈建議遊戲的安裝程式以無訊息模式安裝遊戲所建立的 DirectX 可轉散發套件。 DirectX 安裝程式的設計目的，是要驗證是否需要更新任何事項，並在不需要時快速傳回。 因此，不需要要求使用者安裝 DirectX。

您可以從安裝套件執行此命令來完成 DirectX 的無訊息安裝： **dxsetup.exe/silent**

此外，可轉散發資料夾的實際大小可設定為僅包含遊戲目標平臺和使用方式所需的封包檔 (.cab) 。

> [!Note]  
> 在使用 **dxsetup** 之前，請先閱讀 [ [不要直接設定](https://walbourn.github.io/)]。

 

## <a name="excessive-use-of-thread-synchronization"></a>過度使用執行緒同步處理

分析遊戲時，常見的熱點通常會與進入和離開重要區段有關。 隨著多核心 Cpu 的普及，在遊戲中使用多執行緒的方式大幅增加，而許多執行都依賴大量的執行緒同步處理。 即使沒有爭用的情況下，要採取重要區段的 CPU 時間很重要，而所有其他形式的執行緒同步處理也會更昂貴。 因此，必須小心將這些基本專案的使用降至最低。

遊戲中過度同步處理的常見來源，是使用 [D3DCREATE \_ 多執行緒](/windows/desktop/direct3d9/d3dcreate)。 此旗標雖然讓 Direct3D 執行緒安全可從多個執行緒進行轉譯，但卻是非常保守的方法，因此會產生高度的同步處理負荷。 遊戲應避免此旗標。 改為建立引擎的架構，讓所有與 Direct3D 的通訊都是來自單一線程，而執行緒之間的任何通訊都會直接處理。 如需設計多執行緒遊戲的詳細資訊，請參閱[Xbox 360 和 Microsoft Windows 上多核心的編碼](/windows/desktop/DxTechArts/coding-for-multiple-cores)文章。

## <a name="use-of-rdtsc"></a>使用 RDTSC

不建議使用 x86 指令 **RDTSC** 。 **RDTSC** 無法在某些電源管理配置上正確計算時間，以動態方式變更 CPU 頻率，並在許多多核心 cpu 上，不會在核心之間同步處理迴圈計數器。 遊戲應改為使用 [**QueryPerformanceCounter**](/windows/desktop/api/profileapi/nf-profileapi-queryperformancecounter) API。 如需有關 **RDTSC** 的問題，以及使用 **QueryPerformanceCounter** 來執行高解析度計時的詳細資訊，請參閱 [遊戲計時和多核心處理器](/windows/desktop/DxTechArts/game-timing-and-multicore-processors)一文。

 

 