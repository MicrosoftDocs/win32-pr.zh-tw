---
description: Multihead 卡是具有通用框架緩衝區和加速器、獨立數位到類比轉換器 (Dac) 和監視輸出的卡片。
ms.assetid: f741cdb4-2eb6-42e9-81ea-a8c677e07582
title: 'Multihead (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04a74f51cea282618c9471eb9a63eedf8eef73c38b4d961209064261a93c4d46
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119563511"
---
# <a name="multihead-direct3d-9"></a>Multihead (Direct3D 9) 

Multihead 卡是具有通用框架緩衝區和加速器、獨立數位到類比轉換器 (Dac) 和監視輸出的卡片。 這類裝置可提供比相同數量的異類顯示器介面卡更容易使用的多監視器支援。

Multihead 卡在 API 中公開為單一 API 層級的裝置，可驅動數個全螢幕交換鏈。 因此，所有資源都會與所有的標頭共用，而且每個標頭都有完全相同的功能。 每個標頭都可以設定為獨立的顯示模式。 您可以使用不同的 [**IDirect3DSwapChain9 呼叫：:P**](/windows/desktop/api) 重新傳送以重新整理每個標頭。 您也可以使用一次呼叫 [**IDirect3DDevice9：:P**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) 重新傳送以依序重新整理每個標頭。

> [!Note]  
> 每個標頭的重新整理不會同時透過單一呼叫 [**IDirect3DDevice9：:P**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)重新傳送。 Direct3D 9Ex 中的 [顯示統計資料] 可以使用 [**D3DPRESENTSTATS**](d3dpresentstats.md) 結構，讓每個前端的重新整理保持彼此接近，以限制跨多張介面卡的撕裂效果。 如需有關同步處理 Direct3D 9Ex flip 模型應用程式之框架的詳細資訊，請參閱 [Direct3d 9Ex 增強功能](../direct3darticles/direct3d-9ex-improvements.md)。

 

Multihead 裝置的每個交換鏈都必須是全螢幕。 當裝置進入 multihead 模式時，它必須維持全螢幕。 轉換回視窗模式的模式需要終結裝置 (但一般 ALT + TAB 至最小化作業) 除外。

在 head 之間分割影片記憶體的舊方法，將每個標頭視為完全獨立的加速器，仍然是常見的使用案例。 除非應用程式已特別編碼為在 Direct3D 9 multihead 模式下運作，否則此建議程式不會取代該機制。

驅動程式會獲得足夠的知識，以便在這兩種作業模式之間切換。

其中一個標頭稱為主要 head，而同一張卡片上的所有其他標頭則稱為「次級」。 如果系統中有一個以上的 multihead 介面卡，則單一 multihead 介面卡上的主要和其從屬電腦稱為群組。 群組是由其主要 head 的介面卡序數表示。

[**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)結構已更新為公開下列新的硬體上限。


```
UINT NumberOfAdaptersInGroup; 
UINT MasterAdapterOrdinal; 
UINT AdapterOrdinalInGroup;
```



-   適用于傳統介面卡的 NumberOfAdaptersInGroup 是1，而 multihead 卡的主要介面卡則大於1。 Multihead 卡的從屬介面卡的值會是0。 每張卡片最多可以有一個主要主機，但可能有許多附屬。
-   MasterAdapterOrdinal 指出哪個裝置是此從屬的主要節點。
-   AdapterOrdinalInGroup 指出 API 參考標頭的順序。 主要介面卡一律會有 AdapterOrdinalInGroup 0。 這些值不會對應至傳遞給 IDirect3D9 方法的介面卡序數，而只會套用至群組內的標頭。

此定義可讓 multihead 卡片繼續以獨立卡形式來顯示多個介面卡，就像在 DirectX 8 中一樣。

若要建立 multihead 裝置，請 \_ \_ 在 [**IDirect3D9：： CreateDevice**](/windows/desktop/api)中指定行為旗標 D3DCREATE ADAPTERGROUP 裝置。 呈現參數 ([**D3DPRESENT \_ 參數**](d3dpresent-parameters.md) 的陣列) 應該包含 NumberOfAdaptersInGroup 元素。 執行時間會將每個元素指派給每個標頭，並以 AdapterOrdinalInGroup 的數值順序排列。 設定 D3DCREATE \_ ADAPTERGROUP \_ 裝置時，每個呈現參數都必須有：

-   設定為 **FALSE** 的視窗成員 (換言之，是全螢幕) 。
-   [**D3DPRESENT \_ 參數**](d3dpresent-parameters.md)之 EnableAutoDepthStencil 成員的相同值。

此外，如果 EnableAutoDepthStencil 為 **TRUE**，則下列每個欄位的每個 [**D3DPRESENT \_ 參數**](d3dpresent-parameters.md)都必須有相同的值：

-   AutoDepthStencilFormat
-   BackBufferWidth
-   BackBufferHeight
-   BackBufferFormat

如果設定 DAC， [**IDirect3DDevice9：： CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) 的其他呼叫不合法。

如果裝置是使用 DAC 建立的， [**IDirect3DDevice9：： Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) 將會預期 [**D3DPRESENT \_ 參數**](d3dpresent-parameters.md)的陣列。

傳遞至 [**IDirect3DDevice9：： Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)的每個 [**D3DPRESENT \_ 參數**](d3dpresent-parameters.md)結構都必須是全螢幕。 若要切換回視窗模式，應用程式必須終結裝置，並在視窗模式中重新建立非 multihead 裝置。

以下是基本使用案例：


```
1. Create multihead device 
2. For each swap chain of device:
   3. Call GetBackBuffer for the i-th swapchain
   4. Call SetRenderTarget 
   5. Call DrawPrimitive 
   6. Optionally call swapchain::Present (or wait until 
all swap chains are drawn and present outside of loop)
7. End the for loop
8. Optionally present all swap chains with device::Present
```



如需詳細資訊，請參閱 [**IDirect3D9：： CreateDevice**](/windows/desktop/api) 和 [**IDirect3DDevice9：： GetNumberOfSwapChains**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getnumberofswapchains)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[程式設計提示](programming-tips.md)
</dt> </dl>

 

 
