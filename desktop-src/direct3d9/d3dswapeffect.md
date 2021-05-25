---
description: 定義交換效果。
ms.assetid: 522a5f71-3ad9-4cfc-a899-e25b9b721b1b
title: D3DSWAPEFFECT 列舉 (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSWAPEFFECT
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 58354e35ca8456f6fde57d2f2567a6b6a202f6d7
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343033"
---
# <a name="d3dswapeffect-enumeration"></a>D3DSWAPEFFECT 列舉

定義交換效果。

## <a name="syntax"></a>Syntax

```cpp
typedef enum D3DSWAPEFFECT { 
  D3DSWAPEFFECT_DISCARD      = 1,
  D3DSWAPEFFECT_FLIP         = 2,
  D3DSWAPEFFECT_COPY         = 3,
  D3DSWAPEFFECT_OVERLAY      = 4,
  D3DSWAPEFFECT_FLIPEX       = 5,
  D3DSWAPEFFECT_FORCE_DWORD  = 0xFFFFFFFF
} D3DSWAPEFFECT, *LPD3DSWAPEFFECT;
```

## <a name="constants"></a>常數

<dl> <dt>

<span id="D3DSWAPEFFECT_DISCARD"></span><span id="d3dswapeffect_discard"></span>**D3DSWAPEFFECT \_ 捨棄**
</dt> <dd>

使用 D3DSWAPEFFECT FLIP 或 D3DSWAPEFFECT COPY 的交換效果來建立交換鏈時 \_ \_ ，執行時間會確保 [**IDirect3DDevice9：:P**](/windows/desktop/api) 重新傳送的作業不會影響任何背景緩衝區的內容。 可惜的是，符合這種保證可能涉及大量的視頻記憶體或處理負荷，尤其是針對全螢幕交換鏈的視窗型交換鏈或複製語義執行翻轉語義時。 應用程式可能會使用 D3DSWAPEFFECT \_ 捨棄交換效果來避免這些負荷，並讓顯示器驅動程式為交換鏈選取最有效率的呈現技巧。 這也是在 \_ 針對 [**D3DPRESENT \_ 參數**](d3dpresent-parameters.md)的 MultiSampleType 成員指定 D3DMULTISAMPLE NONE 以外的值時，可以使用的唯一交換效果。

如同使用 D3DSWAPEFFECT FLIP 的交換鏈 \_ ，使用 D3DSWAPEFFECT 捨棄的交換鏈 \_ 可能包含多個背景緩衝區，其中任何一個都可以使用 [**IDirect3DDevice9：： GetBackBuffer**](/windows/desktop/api) 或 [**IDirect3DSwapChain9：： GetBackBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dswapchain9-getbackbuffer)來存取。 交換鏈最適合設想為佇列，其中0一律會為下一個目前作業所顯示的後置緩衝區編制索引，而在顯示緩衝區時，就會捨棄緩衝區。

使用此交換效果的應用程式無法對捨棄的背景緩衝區內容進行任何假設，因此應該在叫用顯示它的目前作業之前，先更新整個背景緩衝區。 雖然這不會強制執行，但執行時間的偵錯工具將會覆寫捨棄的緩衝區內容，並提供亂數據，讓開發人員可以驗證其應用程式是否正確地更新整個背景緩衝區介面。

</dd> <dt>

<span id="D3DSWAPEFFECT_FLIP"></span><span id="d3dswapeffect_flip"></span>**D3DSWAPEFFECT \_ FLIP**
</dt> <dd>

交換鏈可能包含多個背景緩衝區，而且最好設想為包含前端緩衝區的迴圈佇列。 在此佇列中，反向緩衝區一律會依序從0到 (n-1) ，其中 n 是後端緩衝區的數目，因此0代表最近顯示的緩衝區。 當叫用時，佇列會「旋轉」，讓前端緩衝區變成 (n-1) 的緩衝區，而背景緩衝區0則會變成新的前端緩衝區。

</dd> <dt>

<span id="D3DSWAPEFFECT_COPY"></span><span id="d3dswapeffect_copy"></span>**D3DSWAPEFFECT \_ 複製**
</dt> <dd>

此交換效果只能針對包含單一背景緩衝區的交換鏈來指定。 無論交換鏈是視窗化或全螢幕，執行時間都將保證複製為基礎之目前作業所隱含的語法，也就是作業會讓背景緩衝區的內容保持不變，而不是以向前緩衝區的內容取代，做為以翻轉為基礎的目前操作。

針對全螢幕交換鏈，執行時間會使用翻轉作業和複製作業的組合（如有需要，在隱藏的緩衝區執行時支援）來完成目前的操作。 因此，此簡報會與顯示配接器的垂直回溯同步，而且其速率會受到所選呈現間隔的限制。 使用 D3DPRESENT INTERVAL IMMEDIATE 旗標指定的交換鏈 \_ \_ 是唯一的例外狀況。  (參考 [**D3DPRESENT \_ 參數**](d3dpresent-parameters.md)結構之 **PresentationIntervals** 成員的描述 ) 。在此情況下，目前的作業會將背景緩衝區內容直接複製到前端緩衝區，而不會等待垂直回溯。

</dd> <dt>

<span id="D3DSWAPEFFECT_OVERLAY"></span><span id="d3dswapeffect_overlay"></span>**D3DSWAPEFFECT \_ 重迭**
</dt> <dd>

使用可在主要介面上重迭的影片記憶體私人區域。 當重迭顯示時，不會執行任何複製。 覆迭作業是在硬體中執行，而不需要修改主要介面中的資料。

Direct3D 9 與 Direct3D 9Ex 之間的差異：

- D3DSWAPEFFECT 重迭 \_ 僅適用于在 Windows 7 上執行的 Direct3D9Ex (或更多目前的作業系統) 。

</dd> <dt>

<span id="D3DSWAPEFFECT_FLIPEX"></span><span id="d3dswapeffect_flipex"></span>**D3DSWAPEFFECT \_ FLIPEX**
</dt> <dd>

指定應用程式採用翻轉模式的時間，在這段期間，會在應用程式以視窗模式呈現時，不會將應用程式的框架傳遞至桌面視窗管理員 (DWM) 以進行撰寫。 翻轉模式可讓應用程式更有效率地使用記憶體頻寬，以及啟用應用程式以利用全螢幕顯示的統計資料。 翻轉模式不會影響全螢幕的行為。

> [!Note]  
> 如果您使用 D3DSWAPEFFECT FLIPEX 建立交換鏈 \_ ，則當您呈現新的框架以供顯示時，無法覆寫 [**D3DPRESENT \_ 參數**](d3dpresent-parameters.md)結構的 **hDeviceWindow** 成員。 也就是說，您必須將 **Null** 傳遞至 [**IDirect3DDevice9Ex：:P resentex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex)的 *hDestWindowOverride* 參數，以指示執行時間使用 **D3DPRESENT \_ 參數** 的 **hDeviceWindow** 成員進行簡報。

Direct3D 9 與 Direct3D 9Ex 之間的差異：

- D3DSWAPEFFECT \_ FLIPEX 僅適用于在 Windows 7 上執行的 Direct3D9Ex (或更多目前的作業系統) 。

</dd> <dt>

<span id="D3DSWAPEFFECT_FORCE_DWORD"></span><span id="d3dswapeffect_force_dword"></span>**D3DSWAPEFFECT \_ 強制 \_ DWORD**
</dt> <dd>

強制此列舉的大小編譯為32位。 如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。 不使用這個值。

</dd> </dl>

## <a name="remarks"></a>備註

出現呼叫之後的背景緩衝區狀態是由這些交換效果妥善定義的，以及是否使用全螢幕交換鏈或視窗型交換鏈來建立 Direct3D 裝置，並不會影響此狀態。 尤其是，D3DSWAPEFFECT \_ 翻轉交換效果的運作方式與視窗化或全螢幕相同，且 Direct3D 執行時間會藉由建立額外的緩衝區來保證這一點。 因此，建議應用程式盡可能使用 D3DSWAPEFFECT \_ 捨棄，以避免任何這類的損失。 這是因為此交換效果在記憶體耗用量和效能方面一律是最有效率的。

使用 D3DSWAPEFFECT \_ FLIP 或 D3DSWAPEFFECT 捨棄的應用程式 \_ 應該不會預期全螢幕目的地 Alpha 的運作。 這表示 D3DRS DESTBLEND 轉譯 \_ 狀態將無法如預期般運作，因為具有這些交換效果的全螢幕交換鏈並沒有從驅動程式的觀點來看，有明確的像素格式。 驅動程式會推斷它們應該採用顯示格式，而不具有 Alpha 色板。 若要解決此問題，請採取下列步驟：

-   使用 D3DSWAPEFFECT \_ 複製。
-   檢查 \_ \_ D3DCAPS9 結構的 Caps3 成員中的 D3DCAPS3 ALPHA 全螢幕 \_ 翻轉 \_ 或 \_ 捨棄[](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)旗標。 此旗標指出 \_ 使用 D3DSWAPEFFECT FLIP 或 D3DSWAPEFFECT 捨棄時，驅動程式是否可以進行 Alpha 混色 \_ 。
-   使用翻轉模式交換效果的應用程式 (D3DSWAPEFFECT \_ FLIPEX) 應該在調整視窗大小或區域變更之後呼叫 [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) ，以確保顯示內容已更新。

隱藏的視窗無法接收使用者模式事件;此外，隱藏的全螢幕視窗將干擾另一個應用程式視窗強制回應視窗的呈現。 因此，每個應用程式都必須確保在以全螢幕模式顯示 swapchain 時，會顯示裝置視窗。

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3D9Types。h</dt> </dl> |

## <a name="see-also"></a>另請參閱

[Direct3D 列舉](dx9-graphics-reference-d3d-enums.md)

[**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)
