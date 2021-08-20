---
title: 使用 DR 診斷 GPU 錯誤
description: 裝置移除擴充資料 (DR) 是一組不斷演進的診斷功能，其設計目的是協助您找出未預期的裝置移除錯誤原因。
ms.custom: 19H1
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: ecb18b81107123564e265e49fad61c004b17938f732b373311743bf64bd92fab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118097642"
---
# <a name="use-dred-to-diagnose-gpu-faults"></a>使用 DR 診斷 GPU 錯誤
DR 代表裝置移除擴充的資料。 DR 是一組不斷演進的診斷功能，其設計目的是協助您找出非預期裝置移除錯誤的原因。 在支援所需功能 (如) 所定義的硬體上，DR 會提供自動階層連結以及 GPU 分頁錯誤報告。

## <a name="auto-breadcrumbs"></a>自動階層連結
若要設定自動階層連結的場景，讓我們先提及手動的多樣性。 若要可能性 [Timeout 偵測和復原 (TDR)](/windows-hardware/drivers/display/timeout-detection-and-recovery)，您可以使用 [ID3D12GraphicsCommandList2：： WriteBufferImmediate 方法](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist2-writebufferimmediate)*將階層連結置於 gpu* 命令資料流程中，以便追蹤 gpu 進度。

如果您想要建立自訂、低額外負荷的執行，這是合理的方法。 但是，它可能缺乏標準化解決方案的一些多樣性，例如偵錯工具擴充功能，或透過[Windows 錯誤報告 (WER) ](/windows/desktop/wer/windows-error-reporting)的報表 (也稱為 Watson) 。

因此，DR 的自動階層連結呼叫 **WriteBufferImmediate** ，將進度計數器放置於 GPU 命令資料流程中。 DR 會在每個轉譯作業之後插入階層 *連結，* &mdash; 這表示產生 GPU 的每個作業都會 (例如，**繪製**、**分派**、**複製**、**解析** 和其他) 。 如果裝置在 GPU 工作負載的中間移除，則 DR 階層連結值基本上是在錯誤之前完成的轉譯 ops 集合。

階層連結歷程記錄通道緩衝區會在指定的命令清單中保留最多64KiB 的作業。 如果命令清單中有65536以上的作業，則只會先儲存最後一個64KiB 作業來 &mdash; 覆寫最舊的作業。 不過，階層連結計數器值會繼續計算到最多 `UINT_MAX` 。 因此，LastOpIndex = (BreadcrumbCount-1) % 65536。

dr 1.0 是 Windows 10 版本 1809 (Windows 10 2018 年10月更新) 第一次提供，它會公開基本的自動階層連結。 但是，它並沒有 api，因此啟用 dr 1.0 的唯一方法就是使用 **意見反應中樞** 來捕捉 (TDR 重現) **應用程式 & 遊戲** 的 \> **效能和相容性**。 DR 1.0 的主要目的是協助根本原因-透過客戶意見反應來分析遊戲損毀。
### <a name="caveats"></a>警示
- 因為 GPU 會進行大量的管線，所以不保證階層連結計數器會指出失敗的確切作業。 事實上，在某些以磚為基礎的延遲轉譯裝置上，階層連結計數器可能是完整資源或未排序的存取權， (UAV) 在實際 GPU 進度背後的關卡。
- 顯示驅動程式可以重新排列命令、在執行命令前先從資源記憶體預先提取，或是在命令完成後清除快取的記憶體。 其中任何一項都可能產生 GPU 錯誤。 在這種情況下，自動階層連結計數器可能較不實用或誤導。
### <a name="performance"></a>效能
雖然自動階層連結設計為低額外負荷，但不是免費的。 經驗測量顯示一般 AAA Direct3D 12 圖形遊戲引擎的2-5% 效能損失。 基於這個理由，預設會關閉自動階層連結。
### <a name="hardware-requirements"></a>硬體需求
因為階層連結計數器值在裝置移除之後必須保留，所以包含階層連結的資源必須存在於系統記憶體中，而且必須在裝置移除時保存。 這表示顯示驅動程式必須支援 [**D3D12_FEATURE_EXISTING_HEAPS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature)。 幸運的是，在 Windows 10 1903 版上，大部分的 Direct3D 12 顯示驅動程式都是如此。
## <a name="gpu-page-fault-reporting"></a>GPU 分頁錯誤報告
DR 1.1 的新功能是 DR GPU 分頁錯誤報告。 GPU 分頁錯誤通常會在下列其中一種情況下發生。

1. 應用程式錯誤地在參考已刪除物件的 GPU 上執行工作。 這是意外移除裝置的主要原因之一。
2. 應用程式會在存取已收回資源或非常駐磚的 GPU 上，錯誤地執行工作。
3. 著色器參考未初始化或過時的描述項。
3. 根系結結尾以外的著色器索引。

DR 會藉由報告任何現有或最近釋出之 API 物件的名稱和類型，以符合 GPU 回報分頁錯誤的虛擬位址 (VA) ，來嘗試解決其中一些案例。

### <a name="caveat"></a>警告
雖然所有 Gpu 都不支援分頁錯誤 (但許多都) 。 某些 Gpu 會透過下列方式來回應記憶體錯誤：位值寫入;讀取模擬資料 (例如，零) ;或者只是掛斷。 可惜的是，在 GPU 不會立即停止回應的情況下， [TDR) 的超時偵測和復原 (](/windows-hardware/drivers/display/timeout-detection-and-recovery) 可能會在管道稍後發生，因此更難找到根本原因。

### <a name="performance"></a>效能
Direct3D 12 執行時間必須主動策展 (VA) 的虛擬位址可編制索引的現有和最近刪除 API 物件的集合。 這會增加系統記憶體的額外負荷，並對物件建立和終結帶來輕微的效能衝擊。 基於這個原因，預設會關閉此行為。

### <a name="hardware-requirements"></a>硬體需求
不支援分頁錯誤的 GPU 仍可受益于自動階層連結功能。

## <a name="setting-up-dred-in-code"></a>在程式碼中設定 DR
DR 設定對程式而言是全域的，您必須先設定這些設定，才能建立 Direct3D 12 裝置。 若要這樣做，請呼叫 [**D3D12GetDebugInterface**](/windows/desktop/api/d3d12/nf-d3d12-d3d12getdebuginterface) 函式來取得 [**ID3D12DeviceRemovedExtendedDataSettings**](/windows/desktop/api/d3d12/nn-d3d12-id3d12deviceremovedextendeddatasettings)。

```cpp
CComPtr<ID3D12DeviceRemovedExtendedDataSettings> pDredSettings;
VERIFY_SUCCEEDED(D3D12GetDebugInterface(IID_PPV_ARGS(&pDredSettings)));

// Turn on auto-breadcrumbs and page fault reporting.
pDredSettings->SetAutoBreadcrumbsEnablement(D3D12_DRED_ENABLEMENT_FORCED_ON);
pDredSettings->SetPageFaultEnablement(D3D12_DRED_ENABLEMENT_FORCED_ON);
```

> [!NOTE]
> DR 設定的修改不會影響已建立的裝置。 但後續的 [**D3D12CreateDevice**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice) 呼叫會使用最新的 dr 設定。

## <a name="accessing-dred-data-in-code"></a>存取程式碼中的 DR 資料
偵測到裝置移除之後 (例如， **現在** 會傳回 [**DXGI_ERROR_DEVICE_REMOVED**](/windows/desktop/com/com-error-codes-10)) ，請使用 [**ID3D12DeviceRemovedExtendedData**](/windows/desktop/api/d3d12/nn-d3d12-id3d12deviceremovedextendeddata) 介面的方法來存取已移除裝置的 dr 資料。

若要取出 **ID3D12DeviceRemovedExtendedData** 介面，請在 [ID3D12Device](/windows/win32/api/d3d12/nn-d3d12-id3d12device) (或衍生的) 介面上呼叫 [QueryInterface](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(refiid_void)) ，並將介面識別碼 (IID) 傳遞至 **ID3D12DeviceRemovedExtendedData**。

```cpp
void MyDeviceRemovedHandler(ID3D12Device * pDevice)
{
    CComPtr<ID3D12DeviceRemovedExtendedData> pDred;
    VERIFY_SUCCEEDED(pDevice->QueryInterface(IID_PPV_ARGS(&pDred)));
    D3D12_DRED_AUTO_BREADCRUMBS_OUTPUT DredAutoBreadcrumbsOutput;
    D3D12_DRED_PAGE_FAULT_OUTPUT DredPageFaultOutput;
    VERIFY_SUCCEEDED(pDred->GetAutoBreadcrumbsOutput(&DredAutoBreadcrumbsOutput));
    VERIFY_SUCCEEDED(pDred->GetPageFaultAllocationOutput(&DredPageFaultOutput));
    // Custom processing of DRED data can be done here.
    // Produce telemetry...
    // Log information to console...
    // break into a debugger...
}
```

## <a name="debugger-access-to-dred"></a>DR 的偵錯工具存取
偵錯工具可透過 d3d12 存取 DR 資料 **！D3D12DeviceRemovedExtendedData** 資料匯出。

## <a name="dred-telemetry"></a>DR 遙測
您的應用程式可以使用 DR Api 來控制 DR 功能，並收集遙測資料以協助分析問題。 這可提供您更廣泛的網路來攔截這些難以重現的 Tdr。

從 Windows 10 版本1903，所有使用者模式裝置移除的事件都會回報給[Windows 錯誤報告 (WER) ](/windows/desktop/wer/windows-error-reporting)，也稱為 Watson。 如果應用程式、GPU 和顯示驅動程式的特定組合產生足夠數目的裝置移除事件，則可能會暫時啟用 DR，讓客戶在類似的設定上啟動相同的應用程式。
