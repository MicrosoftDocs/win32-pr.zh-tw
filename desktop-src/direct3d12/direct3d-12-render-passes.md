---
title: Direct3D 12 轉譯階段
description: 轉譯傳遞功能可減少進出晶片記憶體的記憶體流量，協助您的轉譯器改善 GPU 效率;它的做法是讓您的應用程式更清楚地識別資源轉譯順序需求和資料相依性。
ms.localizationpriority: high
ms.topic: article
ms.date: 11/15/2018
ms.openlocfilehash: 96ed14cecd518a3e03672f2667306ee0a4b8d64999aab01aa72aae04975f0a83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069688"
---
# <a name="direct3d-12-render-passes"></a>Direct3D 12 轉譯階段

轉譯階段功能是 Windows 10 版本 1809 (10.0 的新功能;組建 17763) ，並介紹 Direct3D 12 轉譯傳遞的概念。 轉譯階段是由您記錄至命令清單中的命令子集所組成。

若要宣告每個轉譯傳遞的開始和結束位置，您可以將屬於該傳遞的命令，裝載至 [**ID3D12GraphicsCommandList4：： BeginRenderPass**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-beginrenderpass) 和 [**EndRenderPass**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-endrenderpass)的呼叫內。 因此，任何命令清單都會包含零個、一個或多個轉譯階段。

## <a name="scenarios"></a>案例

轉譯行程可以改善轉譯器的效能（如果它是根據 Tile-Based 延後轉譯 (TBDR) ），以及其他技巧。 更具體來說，此技巧可讓您的應用程式更清楚地識別資源轉譯順序需求和資料相依性，藉此協助轉譯器改善 GPU 效率。

明確撰寫以利用轉譯階段功能的顯示器驅動程式，可提供最佳結果。 但即使在預先存在的驅動程式上，轉譯傳遞 Api 仍可執行 (但不一定會) 效能改進。

這些是轉譯階段為了提供價值而設計的案例。

### <a name="allow-your-application-to-avoid-unnecessary-loadsstores-of-resources-fromto-main-memory-on-a-tile-based-deferred-rendering-tbdr-architecture"></a>允許您的應用程式在 Tile-Based 延後轉譯 (TBDR) 架構上，避免不必要的資源載入/儲存至主儲存體

轉譯行程的價值主張之一，是它會提供中央位置，指出應用程式對於一組轉譯作業的資料相依性。 這些資料相依性可讓顯示驅動程式在系結/關卡時間檢查這項資料，併發出指示將資源的載入/儲存從主儲存體降至最低。

### <a name="allow-your-tbdr-architecture-to-opportunistically-persistent-resources-in-on-chip-cache-across-render-passes-even-in-separate-command-lists"></a>即使在個別的命令清單中，您的 TBDR 架構也可讓轉譯行程在內部晶片快取中伺機持續性資源 () 

> [!NOTE]
> 具體而言，此案例僅限於您要在多個命令清單中) 寫入相同轉譯目標 (s 的情況。

常見的轉譯模式是讓您的應用程式以序列方式跨多個命令清單轉譯成相同的轉譯目標 (s) ，即使是以平行方式產生轉譯命令也是一樣。 在此案例中使用轉譯階段可讓這些傳遞以 (的方式結合，因為應用程式知道它將會在立即的命令清單中繼續轉譯，) 顯示驅動程式可避免在命令清單界限上清除主儲存體。

## <a name="your-applications-responsibilities"></a>您的應用程式責任

即使使用轉譯階段功能，Direct3D 12 執行時間和顯示驅動程式都不會負責重新排序/避免載入和儲存的推算出機會。 若要正確運用轉譯階段功能，您的應用程式具有這些責任。

- 適當地識別其作業的資料/順序相依性。
- 以最小化 (的方式來排序其提交，將 **_PRESERVE** 旗標) 的使用降至最低。
- 正確利用資源阻礙，並追蹤資源狀態。
- 避免不必要的複本/清除。 為了協助識別這些資訊，您可以從[Windows 工具上的 PIX](https://devblogs.microsoft.com/pix/)使用自動化效能警告。

## <a name="using-the-render-pass-feature"></a>使用轉譯傳遞功能

### <a name="what-is-a-render-pass"></a>什麼是轉譯 *階段*？

轉譯行程是由這些元素所定義。

- 一組在轉譯行程期間固定的輸出系結。 這些系結會指向一或多個轉譯目標視圖 (RTVs) 和/或深度樣板視圖 (DSV) 。
- 以該輸出系結集合為目標的 GPU 作業清單。
- 中繼資料，描述轉譯行程設為目標之所有輸出系結的載入/儲存相依性。

### <a name="declare-your-output-bindings"></a>宣告您的輸出系結

在轉譯階段開始時，您可以宣告轉譯目標 (s) 和/或深度/樣板緩衝區的系結。 您可以選擇性地系結以轉譯目標 (s) ，而且可以選擇性地系結至深度/樣板緩衝區。 但是，您至少必須系結至兩者的其中一個，並在下面的程式碼範例中系結至兩者。

您可以在 [**ID3D12GraphicsCommandList4：： BeginRenderPass**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-beginrenderpass)的呼叫中宣告這些系結。

```cppwinrt
void render_passes(::ID3D12GraphicsCommandList4 * pIGCL4,
    D3D12_CPU_DESCRIPTOR_HANDLE const& rtvCPUDescriptorHandle,
    D3D12_CPU_DESCRIPTOR_HANDLE const& dsvCPUDescriptorHandle)
{
    const float clearColor4[]{ 0.f, 0.f, 0.f, 0.f };
    CD3DX12_CLEAR_VALUE clearValue{ DXGI_FORMAT_R32G32B32_FLOAT, clearColor4 };

    D3D12_RENDER_PASS_BEGINNING_ACCESS renderPassBeginningAccessClear{ D3D12_RENDER_PASS_BEGINNING_ACCESS_TYPE_CLEAR, { clearValue } };
    D3D12_RENDER_PASS_ENDING_ACCESS renderPassEndingAccessPreserve{ D3D12_RENDER_PASS_ENDING_ACCESS_TYPE_PRESERVE, {} };
    D3D12_RENDER_PASS_RENDER_TARGET_DESC renderPassRenderTargetDesc{ rtvCPUDescriptorHandle, renderPassBeginningAccessClear, renderPassEndingAccessPreserve };

    D3D12_RENDER_PASS_BEGINNING_ACCESS renderPassBeginningAccessNoAccess{ D3D12_RENDER_PASS_BEGINNING_ACCESS_TYPE_NO_ACCESS, {} };
    D3D12_RENDER_PASS_ENDING_ACCESS renderPassEndingAccessNoAccess{ D3D12_RENDER_PASS_ENDING_ACCESS_TYPE_NO_ACCESS, {} };
    D3D12_RENDER_PASS_DEPTH_STENCIL_DESC renderPassDepthStencilDesc{ dsvCPUDescriptorHandle, renderPassBeginningAccessNoAccess, renderPassBeginningAccessNoAccess, renderPassEndingAccessNoAccess, renderPassEndingAccessNoAccess };

    pIGCL4->BeginRenderPass(1, &renderPassRenderTargetDesc, &renderPassDepthStencilDesc, D3D12_RENDER_PASS_FLAG_NONE);
    // Record command list.
    pIGCL4->EndRenderPass();
    // Begin/End further render passes and then execute the command list(s).
}
```

您可以將 [**D3D12_RENDER_PASS_RENDER_TARGET_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_render_target_desc) 結構的第一個欄位設定為 CPU 描述項控制碼，以對應至一個或多個轉譯目標視圖 (RTVs) 。 同樣地， [**D3D12_RENDER_PASS_DEPTH_STENCIL_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_depth_stencil_desc) 包含對應至深度樣板視圖 (DSV) 的 CPU 描述項控制碼。 這些 CPU 描述項控制碼與您要傳遞給 [**ID3D12GraphicsCommandList：： OMSetRenderTargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets)的是相同的。 而且就像使用 **OMSetRenderTargets** 一樣，在呼叫 **BEGINRENDERPASS** 時，cpu 描述 *項會從其各自的 (* cpu 描述元) 堆積。

RTVs 和 DSV 不會繼承到轉譯階段。 相反地，必須設定它們。 **BeginRenderPass** 中宣告的 RTVS 和 DSV 也會傳播至命令清單。 相反地，它們會在轉譯階段之後處於未定義狀態。

### <a name="render-passes-and-workloads"></a>轉譯階段和工作負載

您無法嵌套轉譯行程，也不能有轉譯行程跨一個以上的命令清單 (它們必須在錄製至單一命令清單) 時開始和結束。 以下的「轉譯 [ 傳遞旗標](#render-pass-flags)」一節中會討論設計來啟用有效率的轉譯行程產生功能的優化。

您從轉譯傳遞中所做的寫入，在後續轉譯行程 *之前無法讀取* 。 這會從轉譯行程中排除某些類型的阻礙 &mdash; ，例如，從 **RENDER_TARGET** barriering 至目前系結轉譯目標上 **SHADER_RESOURCE** 。 如需詳細資訊，請參閱下方的轉譯行程 [和資源阻礙](#render-passes-and-resource-barriers)一節。

剛才提及之寫入讀取條件約束的唯一例外，就是在深度測試和轉譯目標混合的過程中發生的隱含讀取。
因此，轉譯行程中不允許這些 Api (如果在錄製) 期間呼叫了這些 Api，則會移除該命令清單。

- [**ID3D12GraphicsCommandList1::AtomicCopyBufferUINT**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-atomiccopybufferuint)
- [**ID3D12GraphicsCommandList1::AtomicCopyBufferUINT64**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-atomiccopybufferuint64)
- [**ID3D12GraphicsCommandList4::BeginRenderPass**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-beginrenderpass)
- [**ID3D12GraphicsCommandList::ClearDepthStencilView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-cleardepthstencilview)
- [**ID3D12GraphicsCommandList::ClearRenderTargetView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearrendertargetview)
- [**ID3D12GraphicsCommandList::ClearState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearstate)
- [**ID3D12GraphicsCommandList::ClearUnorderedAccessViewFloat**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewfloat)
- [**ID3D12GraphicsCommandList::ClearUnorderedAccessViewUint**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewuint)
- [**ID3D12GraphicsCommandList::CopyBufferRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
- [**ID3D12GraphicsCommandList::CopyResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
- [**ID3D12GraphicsCommandList::CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
- [**ID3D12GraphicsCommandList::CopyTiles**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles)
- [**ID3D12GraphicsCommandList：:D iscardResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource)
- [**ID3D12GraphicsCommandList：:D ispatch**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)
- [**ID3D12GraphicsCommandList::OMSetRenderTargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets)
- [**ID3D12GraphicsCommandList::ResolveQueryData**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata)
- [**ID3D12GraphicsCommandList::ResolveSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvesubresource)
- [**ID3D12GraphicsCommandList1::ResolveSubresourceRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-resolvesubresourceregion)
- [**ID3D12GraphicsCommandList3::SetProtectedResourceSession**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist3-setprotectedresourcesession)

### <a name="render-passes-and-resource-barriers"></a>轉譯通過和資源阻礙

您不得讀取或取用在相同轉譯階段中發生的寫入。 某些阻礙不符合此條件約束，例如，從 **D3D12_RESOURCE_STATE_RENDER_TARGET** 到目前系結轉譯 (目標上 **\* _SHADER_RESOURCE** ，而且 debug 圖層會導致該效果) 發生錯誤。 但是，在目前轉譯階段 *以外* 撰寫之轉譯目標的相同屏障是一致的，因為寫入將會在目前的轉譯階段開始之前完成。
您可能會受益于瞭解顯示驅動程式所能進行的特定優化。 針對符合標準的工作負載，顯示器驅動程式可能會將轉譯行程中遇到的任何阻礙移至轉譯行程的開頭。 在那裡，它們可以結合 (，而不會干擾) 的任何平平平/分類收納作業。 這是有效的優化，前提是在目前的轉譯階段開始之前，所有寫入都已完成。

以下是更完整的驅動程式優化範例，假設您有一個轉譯引擎，其具有預先 Direct3D 12 樣式的資源系結設計，可根據 &mdash; 資源的系結方式來 *視需要* 進行阻礙。 當寫入未排序的存取權視圖時 (UAV) 接近框架的結尾 (要在下一個畫面格中使用) ，則引擎可能會在框架結束時將資源保持 **D3D12_RESOURCE_STATE_UNORDERED_ACCESS** 狀態。 在接下來的框架中，當引擎要將資源系結為著色器資源查看 (SRV) 時，它會發現該資源不是正確的狀態，而且會發出從 **D3D12_RESOURCE_STATE_UNORDERED_ACCESS** 到 **D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE** 的屏障。 如果該屏障發生在轉譯階段內，則顯示驅動程式會對齊，假設所有寫入都已在這個目前的轉譯階段 *之外* 發生，因此 (，且此處提供優化的位置) 顯示驅動程式可能會 *將關卡移* 至轉譯行程的開頭。 同樣地，這是有效的，只要您的程式碼符合本節所述的寫入讀取條件約束和最後一個。


這些是一致的阻礙範例。
- **D3D12_RESOURCE_STATE_UNORDERED_ACCESS** **D3D12_RESOURCE_STATE_INDIRECT_ARGUMENT**。
- **D3D12_RESOURCE_STATE_COPY_DEST** **\* _SHADER_RESOURCE**。

這些都是不一致阻礙的範例。

- **D3D12_RESOURCE_STATE_RENDER_TARGET** 目前系結 RTVs/dsv 上的任何讀取狀態。
- **D3D12_RESOURCE_STATE_DEPTH_WRITE** 目前系結 RTVs/dsv 上的任何讀取狀態。
- 任何別名屏障。
- 未排序的存取權視圖 (UAV) 的阻礙。 

### <a name="resource-access-declaration"></a>資源存取宣告

在 **BeginRenderPass** 階段，以及宣告在該階段中做為 RTVs 和/或 DSV 的所有資源，您也必須指定其開始和結束 *存取* 特性。 如您在上述「宣告 [您的輸出](#declare-your-output-bindings) 系結」一節的程式碼範例中所見，您可以使用 [**D3D12_RENDER_PASS_RENDER_TARGET_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_render_target_desc) 和 [**D3D12_RENDER_PASS_DEPTH_STENCIL_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_depth_stencil_desc) 結構來完成這項作業。

如需詳細資訊，請參閱 [**D3D12_RENDER_PASS_BEGINNING_ACCESS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_beginning_access) 和 [**D3D12_RENDER_PASS_ENDING_ACCESS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_ending_access) 結構，以及 [**D3D12_RENDER_PASS_BEGINNING_ACCESS_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_render_pass_beginning_access_type) 和 [**D3D12_RENDER_PASS_ENDING_ACCESS_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_render_pass_ending_access_type) 列舉。

### <a name="render-pass-flags"></a>轉譯傳遞旗標

傳遞至 **BeginRenderPass** 的最後一個參數是轉譯傳遞旗標， (來自 [**D3D12_RENDER_PASS_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_render_pass_flags) 列舉) 的值。

```cppwinrt
enum D3D12_RENDER_PASS_FLAGS
{
    D3D12_RENDER_PASS_FLAG_NONE = 0,
    D3D12_RENDER_PASS_FLAG_ALLOW_UAV_WRITES = 0x1,
    D3D12_RENDER_PASS_FLAG_SUSPENDING_PASS = 0x2,
    D3D12_RENDER_PASS_FLAG_RESUMING_PASS = 0x4
};
```

#### <a name="uav-writes-within-a-render-pass"></a>在轉譯階段內 UAV 寫入

在轉譯行程中允許未排序的存取權 (UAV) 寫入，但是您必須特別指出您將在轉譯行程中，藉由指定 **D3D12_RENDER_PASS_FLAG_ALLOW_UAV_WRITES** 來發出 UAV 寫入，如此一來，顯示驅動程式就可以視需要退出並排顯示。

UAV 存取必須遵循以上所述的寫入讀取條件約束 (轉譯行程中的寫入，在後續轉譯行程) 之前無效。 轉譯行程中不允許 UAV 障礙。

透過根資料表或根) 描述元 (的 UAV 系結會繼承到轉譯行程中，並傳播到轉譯階段。

#### <a name="suspending-passes-and-resuming-passes"></a>暫止和繼續傳遞

您可以將整個轉譯階段表示為暫停傳遞和/或繼續進行。 暫止的繼續配對必須在行程之間擁有相同的視圖/存取旗標，而且可能不會有任何中間的 GPU 作業 (例如，繪製、分派、捨棄、清除、複製、更新磚-對應、寫入緩衝區 immediates、查詢、查詢在暫停轉譯傳遞與繼續轉譯行程之間的) 。

預期的使用案例是多執行緒轉譯，其中假設有四個命令清單 (每個都有自己的轉譯行程) 可將目標設為相同的呈現目標。 當轉譯階段跨命令清單暫停/繼續時，命令清單必須在 [**ID3D12CommandQueue：： ExecuteCommandLists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists)的相同呼叫中執行。

轉譯階段可以是繼續和暫停。 在剛剛指定的多執行緒範例中，命令清單2和3會分別從1和2繼續。 而且，相同的時間2和3會分別暫停至3和4。

## <a name="query-for-render-passes-feature-support"></a>查詢轉譯傳遞功能支援

您可以呼叫 [**ID3D12Device：： CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) 來查詢設備磁碟機和/或硬體有效率地支援轉譯行程的範圍。

```cppwinrt
D3D12_RENDER_PASS_TIER get_render_passes_tier(::ID3D12Device * pIDevice)
{
    D3D12_FEATURE_DATA_D3D12_OPTIONS5 featureSupport{};
    winrt::check_hresult(
        pIDevice->CheckFeatureSupport(D3D12_FEATURE_D3D12_OPTIONS5, &featureSupport, sizeof(featureSupport))
    );
    return featureSupport.RenderPassesTier;
}
...
    D3D12_RENDER_PASS_TIER renderPassesTier{ get_render_passes_tier(pIDevice) };
```

由於執行時間的對應邏輯，轉譯傳遞一律會運作。 但是，根據功能支援，他們不一定會提供好處。 您可以使用類似上述程式碼範例的程式碼，來判斷是否需要您的時間來將命令發出為轉譯行程，以及當它絕對不是優點時 (也就是，當執行時間只對應至現有的 API 介面) 時。 如果您使用的是 [D3D11On12](/windows/desktop/direct3d12/direct3d-11-on-12)) ，執行這項檢查就特別重要。

如需三個支援層級的說明，請參閱 [**D3D12_RENDER_PASS_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_render_pass_tier) 列舉。
