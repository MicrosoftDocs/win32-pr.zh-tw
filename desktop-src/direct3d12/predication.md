---
title: 預測
description: Predication 是一項功能，可啟用 GPU 而非 CPU 來決定不繪製、複製或分派物件。
ms.assetid: 5c5138c7-f6e8-4646-961a-0e2312b5356b
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a18df35c94fbd6b2b6f449585dfdcd4028bf2e9
ms.sourcegitcommit: 9dadca1a0d77cb2a372e5a941ec707f9d77b354d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/20/2020
ms.locfileid: "104548437"
---
# <a name="predication"></a>預測

Predication 是一項功能，可啟用 GPU 而非 CPU 來決定不繪製、複製或分派物件。

-   [概觀](#overview)
-   [SetPredication](#setpredication)
-   [相關主題](#related-topics)

## <a name="overview"></a>概觀

Predication 的一般用途是使用遮蔽;如果有繪製周框方塊，且 pixels occluded，在繪製物件本身時顯然沒有任何點。 在這種情況下，物件的繪圖可以是 "前提"，以便從 GPU 的實際轉譯中移除它。

一開始，這看起來可能會備援超過標準深度測試，再加上深度通過。 但是 predication 可以移除 draw 命令狀態本身的額外負荷，加上點陣化。 雖然深度傳遞會移除不必要的圖元，但它仍然可以執行頂點、輪廓、網域和幾何著色器，並叫用固定函式的輸入組合語言、tesselator 和轉譯器。 藉由繪製簡單的周框方塊或類似的周框， &mdash; 比實際模型更容易處理和點陣化， &mdash; 您可以避免不必要的點陣化和處理。

與 Direct3D 11 不同的是，predication 會從查詢分離出來，並在 Direct3D 12 中擴充，以根據應用程式開發人員可能 (決定的任何推理來啟用述詞物件，而不只是遮蔽) 。

## <a name="setpredication"></a>SetPredication

Predication 可以根據緩衝區內64位的值來設定 (請參閱 [**D3D12 \_ Predication \_ OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_predication_op)) 。

當 GPU 執行 [**SetPredication**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication) 命令時，它會在緩衝區中貼上值。 未來對緩衝區中資料所做的變更不會追溯影響 predication 狀態。

如果輸入參數緩衝區為 Null，則會停用 predication。

Direct3D 12 API 中不會有 Predication 提示;直接、計算和複製命令清單可以使用和 predication。 來源緩衝區可以是任何堆積類型 (預設、上傳、readback、自訂) 。

核心執行時間會驗證下列各項：

-   *AlignedBufferOffset* 是8個位元組的倍數
-   資源是緩衝區
-   作業是列舉的有效成員
-   無法從組合內呼叫 [**SetPredication**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication)
-   命令清單類型支援 predication
-   位移不超過緩衝區大小

如果來源緩衝區不在與 [**D3D12_RESOURCE_STATE_INDIRECT_ARGUMENT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states)相同的 [**D3D12_RESOURCE_STATE_PREDICATION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) (，而且只是) 狀態的別名，debug 層將會發出錯誤。

可以前提的一組作業如下：

-   [**DrawInstanced**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced)
-   [**DrawIndexedInstanced**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawindexedinstanced)
-   [**分派**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)
-   [**CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
-   [**CopyBufferRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
-   [**CopyResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
-   [**CopyTiles**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles)
-   [**ResolveSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvesubresource)
-   [**ClearDepthStencilView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-cleardepthstencilview)
-   [**ClearRenderTargetView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearrendertargetview)
-   [**ClearUnorderedAccessViewUint**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewuint)
-   [**ClearUnorderedAccessViewFloat**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewfloat)
-   [**ExecuteIndirect**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect)

[**ExecuteBundle**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executebundle) 不是前提本身。 相反地，上述清單中包含在組合內的個別作業會前提。

ID3D12GraphicsCommandList 方法 [**ResolveQueryData**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata)、 [**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) 和 [**EndQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery) 不會前提。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[計數器和查詢](counters-and-queries.md)
</dt> <dt>

[效能測量](performance-measurement.md)
</dt> <dt>

[Predication 查詢逐步解說](predication-queries.md)
</dt> </dl>

 

 




