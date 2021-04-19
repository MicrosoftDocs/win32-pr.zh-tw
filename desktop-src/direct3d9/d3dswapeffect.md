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
ms.openlocfilehash: 41327dc66f676c6f498ad0cefb23202bedc13112
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106991450"
---
# <a name="d3dswapeffect-enumeration"></a><span data-ttu-id="57e9f-103">D3DSWAPEFFECT 列舉</span><span class="sxs-lookup"><span data-stu-id="57e9f-103">D3DSWAPEFFECT enumeration</span></span>

<span data-ttu-id="57e9f-104">定義交換效果。</span><span class="sxs-lookup"><span data-stu-id="57e9f-104">Defines swap effects.</span></span>

## <a name="syntax"></a><span data-ttu-id="57e9f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="57e9f-105">Syntax</span></span>

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

## <a name="constants"></a><span data-ttu-id="57e9f-106">常數</span><span class="sxs-lookup"><span data-stu-id="57e9f-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="57e9f-107"><span id="D3DSWAPEFFECT_DISCARD"></span><span id="d3dswapeffect_discard"></span>**D3DSWAPEFFECT \_ 捨棄**</span><span class="sxs-lookup"><span data-stu-id="57e9f-107"><span id="D3DSWAPEFFECT_DISCARD"></span><span id="d3dswapeffect_discard"></span>**D3DSWAPEFFECT\_DISCARD**</span></span>
</dt> <dd>

<span data-ttu-id="57e9f-108">使用 D3DSWAPEFFECT FLIP 或 D3DSWAPEFFECT COPY 的交換效果來建立交換鏈時 \_ \_ ，執行時間會確保 [**IDirect3DDevice9：:P**](/windows/desktop/api) 重新傳送的作業不會影響任何背景緩衝區的內容。</span><span class="sxs-lookup"><span data-stu-id="57e9f-108">When a swap chain is created with a swap effect of D3DSWAPEFFECT\_FLIP or D3DSWAPEFFECT\_COPY, the runtime will guarantee that an [**IDirect3DDevice9::Present**](/windows/desktop/api) operation will not affect the content of any of the back buffers.</span></span> <span data-ttu-id="57e9f-109">可惜的是，符合這種保證可能涉及大量的視頻記憶體或處理負荷，尤其是針對全螢幕交換鏈的視窗型交換鏈或複製語義執行翻轉語義時。</span><span class="sxs-lookup"><span data-stu-id="57e9f-109">Unfortunately, meeting this guarantee can involve substantial video memory or processing overheads, especially when implementing flip semantics for a windowed swap chain or copy semantics for a full-screen swap chain.</span></span> <span data-ttu-id="57e9f-110">應用程式可能會使用 D3DSWAPEFFECT \_ 捨棄交換效果來避免這些負荷，並讓顯示器驅動程式為交換鏈選取最有效率的呈現技巧。</span><span class="sxs-lookup"><span data-stu-id="57e9f-110">An application may use the D3DSWAPEFFECT\_DISCARD swap effect to avoid these overheads and to enable the display driver to select the most efficient presentation technique for the swap chain.</span></span> <span data-ttu-id="57e9f-111">這也是在 \_ 針對 [**D3DPRESENT \_ 參數**](d3dpresent-parameters.md)的 MultiSampleType 成員指定 D3DMULTISAMPLE NONE 以外的值時，可以使用的唯一交換效果。</span><span class="sxs-lookup"><span data-stu-id="57e9f-111">This is also the only swap effect that may be used when specifying a value other than D3DMULTISAMPLE\_NONE for the MultiSampleType member of [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md).</span></span>

<span data-ttu-id="57e9f-112">如同使用 D3DSWAPEFFECT FLIP 的交換鏈 \_ ，使用 D3DSWAPEFFECT 捨棄的交換鏈 \_ 可能包含多個背景緩衝區，其中任何一個都可以使用 [**IDirect3DDevice9：： GetBackBuffer**](/windows/desktop/api) 或 [**IDirect3DSwapChain9：： GetBackBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dswapchain9-getbackbuffer)來存取。</span><span class="sxs-lookup"><span data-stu-id="57e9f-112">Like a swap chain that uses D3DSWAPEFFECT\_FLIP, a swap chain that uses D3DSWAPEFFECT\_DISCARD might include more than one back buffer, any of which may be accessed using [**IDirect3DDevice9::GetBackBuffer**](/windows/desktop/api) or [**IDirect3DSwapChain9::GetBackBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dswapchain9-getbackbuffer).</span></span> <span data-ttu-id="57e9f-113">交換鏈最適合設想為佇列，其中0一律會為下一個目前作業所顯示的後置緩衝區編制索引，而在顯示緩衝區時，就會捨棄緩衝區。</span><span class="sxs-lookup"><span data-stu-id="57e9f-113">The swap chain is best envisaged as a queue in which 0 always indexes the back buffer that will be displayed by the next Present operation and from which buffers are discarded when they have been displayed.</span></span>

<span data-ttu-id="57e9f-114">使用此交換效果的應用程式無法對捨棄的背景緩衝區內容進行任何假設，因此應該在叫用顯示它的目前作業之前，先更新整個背景緩衝區。</span><span class="sxs-lookup"><span data-stu-id="57e9f-114">An application that uses this swap effect cannot make any assumptions about the contents of a discarded back buffer and should therefore update an entire back buffer before invoking a Present operation that would display it.</span></span> <span data-ttu-id="57e9f-115">雖然這不會強制執行，但執行時間的偵錯工具將會覆寫捨棄的緩衝區內容，並提供亂數據，讓開發人員可以驗證其應用程式是否正確地更新整個背景緩衝區介面。</span><span class="sxs-lookup"><span data-stu-id="57e9f-115">Although this is not enforced, the debug version of the runtime will overwrite the contents of discarded back buffers with random data to enable developers to verify that their applications are updating the entire back buffer surfaces correctly.</span></span>

</dd> <dt>

<span data-ttu-id="57e9f-116"><span id="D3DSWAPEFFECT_FLIP"></span><span id="d3dswapeffect_flip"></span>**D3DSWAPEFFECT \_ FLIP**</span><span class="sxs-lookup"><span data-stu-id="57e9f-116"><span id="D3DSWAPEFFECT_FLIP"></span><span id="d3dswapeffect_flip"></span>**D3DSWAPEFFECT\_FLIP**</span></span>
</dt> <dd>

<span data-ttu-id="57e9f-117">交換鏈可能包含多個背景緩衝區，而且最好設想為包含前端緩衝區的迴圈佇列。</span><span class="sxs-lookup"><span data-stu-id="57e9f-117">The swap chain might include multiple back buffers and is best envisaged as a circular queue that includes the front buffer.</span></span> <span data-ttu-id="57e9f-118">在此佇列中，反向緩衝區一律會依序從0到 (n-1) ，其中 n 是後端緩衝區的數目，因此0代表最近顯示的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="57e9f-118">Within this queue, the back buffers are always numbered sequentially from 0 to (n - 1), where n is the number of back buffers, so that 0 denotes the least recently presented buffer.</span></span> <span data-ttu-id="57e9f-119">當叫用時，佇列會「旋轉」，讓前端緩衝區變成 (n-1) 的緩衝區，而背景緩衝區0則會變成新的前端緩衝區。</span><span class="sxs-lookup"><span data-stu-id="57e9f-119">When Present is invoked, the queue is "rotated" so that the front buffer becomes back buffer (n - 1), while the back buffer 0 becomes the new front buffer.</span></span>

</dd> <dt>

<span data-ttu-id="57e9f-120"><span id="D3DSWAPEFFECT_COPY"></span><span id="d3dswapeffect_copy"></span>**D3DSWAPEFFECT \_ 複製**</span><span class="sxs-lookup"><span data-stu-id="57e9f-120"><span id="D3DSWAPEFFECT_COPY"></span><span id="d3dswapeffect_copy"></span>**D3DSWAPEFFECT\_COPY**</span></span>
</dt> <dd>

<span data-ttu-id="57e9f-121">此交換效果只能針對包含單一背景緩衝區的交換鏈來指定。</span><span class="sxs-lookup"><span data-stu-id="57e9f-121">This swap effect may be specified only for a swap chain comprising a single back buffer.</span></span> <span data-ttu-id="57e9f-122">無論交換鏈是視窗化或全螢幕，執行時間都將保證複製為基礎之目前作業所隱含的語法，也就是作業會讓背景緩衝區的內容保持不變，而不是以向前緩衝區的內容取代，做為以翻轉為基礎的目前操作。</span><span class="sxs-lookup"><span data-stu-id="57e9f-122">Whether the swap chain is windowed or full-screen, the runtime will guarantee the semantics implied by a copy-based Present operation, namely that the operation leaves the content of the back buffer unchanged, instead of replacing it with the content of the front buffer as a flip-based Present operation would.</span></span>

<span data-ttu-id="57e9f-123">針對全螢幕交換鏈，執行時間會使用翻轉作業和複製作業的組合（如有需要，在隱藏的緩衝區執行時支援）來完成目前的操作。</span><span class="sxs-lookup"><span data-stu-id="57e9f-123">For a full-screen swap chain, the runtime uses a combination of flip operations and copy operations, supported if necessary by hidden back buffers, to accomplish the Present operation.</span></span> <span data-ttu-id="57e9f-124">因此，此簡報會與顯示配接器的垂直回溯同步，而且其速率會受到所選呈現間隔的限制。</span><span class="sxs-lookup"><span data-stu-id="57e9f-124">Accordingly, the presentation is synchronized with the display adapter's vertical retrace and its rate is constrained by the chosen presentation interval.</span></span> <span data-ttu-id="57e9f-125">使用 D3DPRESENT INTERVAL IMMEDIATE 旗標指定的交換鏈 \_ \_ 是唯一的例外狀況。</span><span class="sxs-lookup"><span data-stu-id="57e9f-125">A swap chain specified with the D3DPRESENT\_INTERVAL\_IMMEDIATE flag is the only exception.</span></span> <span data-ttu-id="57e9f-126"> (參考 [**D3DPRESENT \_ 參數**](d3dpresent-parameters.md)結構之 **PresentationIntervals** 成員的描述 ) 。在此情況下，目前的作業會將背景緩衝區內容直接複製到前端緩衝區，而不會等待垂直回溯。</span><span class="sxs-lookup"><span data-stu-id="57e9f-126">(Refer to the description of the **PresentationIntervals** member of the [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md) structure.) In this case, a Present operation copies the back buffer content directly to the front buffer without waiting for the vertical retrace.</span></span>

</dd> <dt>

<span data-ttu-id="57e9f-127"><span id="D3DSWAPEFFECT_OVERLAY"></span><span id="d3dswapeffect_overlay"></span>**D3DSWAPEFFECT \_ 重迭**</span><span class="sxs-lookup"><span data-stu-id="57e9f-127"><span id="D3DSWAPEFFECT_OVERLAY"></span><span id="d3dswapeffect_overlay"></span>**D3DSWAPEFFECT\_OVERLAY**</span></span>
</dt> <dd>

<span data-ttu-id="57e9f-128">使用可在主要介面上重迭的影片記憶體私人區域。</span><span class="sxs-lookup"><span data-stu-id="57e9f-128">Use a dedicated area of video memory that can be overlayed on the primary surface.</span></span> <span data-ttu-id="57e9f-129">當重迭顯示時，不會執行任何複製。</span><span class="sxs-lookup"><span data-stu-id="57e9f-129">No copy is performed when the overlay is displayed.</span></span> <span data-ttu-id="57e9f-130">覆迭作業是在硬體中執行，而不需要修改主要介面中的資料。</span><span class="sxs-lookup"><span data-stu-id="57e9f-130">The overlay operation is performed in hardware, without modifying the data in the primary surface.</span></span>

|                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57e9f-131">Direct3D 9 與 Direct3D 9Ex 之間的差異：</span><span class="sxs-lookup"><span data-stu-id="57e9f-131">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="57e9f-132">D3DSWAPEFFECT 重迭 \_ 僅適用于在 Windows 7 上執行的 Direct3D9Ex (或更多目前的作業系統) 。</span><span class="sxs-lookup"><span data-stu-id="57e9f-132">D3DSWAPEFFECT\_OVERLAY is only available in Direct3D9Ex running on Windows 7 (or more current operating system).</span></span><br/> |

</dd> <dt>

<span data-ttu-id="57e9f-133"><span id="D3DSWAPEFFECT_FLIPEX"></span><span id="d3dswapeffect_flipex"></span>**D3DSWAPEFFECT \_ FLIPEX**</span><span class="sxs-lookup"><span data-stu-id="57e9f-133"><span id="D3DSWAPEFFECT_FLIPEX"></span><span id="d3dswapeffect_flipex"></span>**D3DSWAPEFFECT\_FLIPEX**</span></span>
</dt> <dd>

<span data-ttu-id="57e9f-134">指定應用程式採用翻轉模式的時間，在這段期間，會在應用程式以視窗模式呈現時，不會將應用程式的框架傳遞至桌面視窗管理員 (DWM) 以進行撰寫。</span><span class="sxs-lookup"><span data-stu-id="57e9f-134">Designates when an application is adopting flip mode, during which time an application's frame is passed instead of copied to the Desktop Window Manager(DWM) for composition when the application is presenting in windowed mode.</span></span> <span data-ttu-id="57e9f-135">翻轉模式可讓應用程式更有效率地使用記憶體頻寬，以及啟用應用程式以利用全螢幕顯示的統計資料。</span><span class="sxs-lookup"><span data-stu-id="57e9f-135">Flip mode allows an application to more efficiently use memory bandwidth as well as enabling an application to take advantage of full-screen-present statistics.</span></span> <span data-ttu-id="57e9f-136">翻轉模式不會影響全螢幕的行為。</span><span class="sxs-lookup"><span data-stu-id="57e9f-136">Flip mode does not affect full-screen behavior.</span></span>

> [!Note]  
> <span data-ttu-id="57e9f-137">如果您使用 D3DSWAPEFFECT FLIPEX 建立交換鏈 \_ ，則當您呈現新的框架以供顯示時，無法覆寫 [**D3DPRESENT \_ 參數**](d3dpresent-parameters.md)結構的 **hDeviceWindow** 成員。</span><span class="sxs-lookup"><span data-stu-id="57e9f-137">If you create a swap chain with D3DSWAPEFFECT\_FLIPEX, you can't override the **hDeviceWindow** member of the [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md) structure when you present a new frame for display.</span></span> <span data-ttu-id="57e9f-138">也就是說，您必須將 **Null** 傳遞至 [**IDirect3DDevice9Ex：:P resentex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex)的 *hDestWindowOverride* 參數，以指示執行時間使用 **D3DPRESENT \_ 參數** 的 **hDeviceWindow** 成員進行簡報。</span><span class="sxs-lookup"><span data-stu-id="57e9f-138">That is, you must pass **NULL** to the *hDestWindowOverride* parameter of [**IDirect3DDevice9Ex::PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) to instruct the runtime to use the **hDeviceWindow** member of **D3DPRESENT\_PARAMETERS** for the presentation.</span></span>

|                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57e9f-139">Direct3D 9 與 Direct3D 9Ex 之間的差異：</span><span class="sxs-lookup"><span data-stu-id="57e9f-139">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="57e9f-140">D3DSWAPEFFECT \_ FLIPEX 僅適用于在 Windows 7 上執行的 Direct3D9Ex (或更多目前的作業系統) 。</span><span class="sxs-lookup"><span data-stu-id="57e9f-140">D3DSWAPEFFECT\_FLIPEX is only available in Direct3D9Ex running on Windows 7 (or more current operating system).</span></span><br/> |

</dd> <dt>

<span data-ttu-id="57e9f-141"><span id="D3DSWAPEFFECT_FORCE_DWORD"></span><span id="d3dswapeffect_force_dword"></span>**D3DSWAPEFFECT \_ 強制 \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="57e9f-141"><span id="D3DSWAPEFFECT_FORCE_DWORD"></span><span id="d3dswapeffect_force_dword"></span>**D3DSWAPEFFECT\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="57e9f-142">強制此列舉的大小編譯為32位。</span><span class="sxs-lookup"><span data-stu-id="57e9f-142">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="57e9f-143">如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。</span><span class="sxs-lookup"><span data-stu-id="57e9f-143">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="57e9f-144">不使用這個值。</span><span class="sxs-lookup"><span data-stu-id="57e9f-144">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="57e9f-145">備註</span><span class="sxs-lookup"><span data-stu-id="57e9f-145">Remarks</span></span>

<span data-ttu-id="57e9f-146">出現呼叫之後的背景緩衝區狀態是由這些交換效果妥善定義的，以及是否使用全螢幕交換鏈或視窗型交換鏈來建立 Direct3D 裝置，並不會影響此狀態。</span><span class="sxs-lookup"><span data-stu-id="57e9f-146">The state of the back buffer after a call to Present is well-defined by each of these swap effects, and whether the Direct3D device was created with a full-screen swap chain or a windowed swap chain has no effect on this state.</span></span> <span data-ttu-id="57e9f-147">尤其是，D3DSWAPEFFECT \_ 翻轉交換效果的運作方式與視窗化或全螢幕相同，且 Direct3D 執行時間會藉由建立額外的緩衝區來保證這一點。</span><span class="sxs-lookup"><span data-stu-id="57e9f-147">In particular, the D3DSWAPEFFECT\_FLIP swap effect operates the same whether windowed or full-screen, and the Direct3D runtime guarantees this by creating extra buffers.</span></span> <span data-ttu-id="57e9f-148">因此，建議應用程式盡可能使用 D3DSWAPEFFECT \_ 捨棄，以避免任何這類的損失。</span><span class="sxs-lookup"><span data-stu-id="57e9f-148">As a result, it is recommended that applications use D3DSWAPEFFECT\_DISCARD whenever possible to avoid any such penalties.</span></span> <span data-ttu-id="57e9f-149">這是因為此交換效果在記憶體耗用量和效能方面一律是最有效率的。</span><span class="sxs-lookup"><span data-stu-id="57e9f-149">This is because this swap effect will always be the most efficient in terms of memory consumption and performance.</span></span>

<span data-ttu-id="57e9f-150">使用 D3DSWAPEFFECT \_ FLIP 或 D3DSWAPEFFECT 捨棄的應用程式 \_ 應該不會預期全螢幕目的地 Alpha 的運作。</span><span class="sxs-lookup"><span data-stu-id="57e9f-150">Applications that use D3DSWAPEFFECT\_FLIP or D3DSWAPEFFECT\_DISCARD should not expect full-screen destination alpha to work.</span></span> <span data-ttu-id="57e9f-151">這表示 D3DRS DESTBLEND 轉譯 \_ 狀態將無法如預期般運作，因為具有這些交換效果的全螢幕交換鏈並沒有從驅動程式的觀點來看，有明確的像素格式。</span><span class="sxs-lookup"><span data-stu-id="57e9f-151">This means that the D3DRS\_DESTBLEND render state will not work as expected because full-screen swap chains with these swap effects do not have an explicit pixel format from the driver's point of view.</span></span> <span data-ttu-id="57e9f-152">驅動程式會推斷它們應該採用顯示格式，而不具有 Alpha 色板。</span><span class="sxs-lookup"><span data-stu-id="57e9f-152">The driver infers that they should take on the display format, which does not have an alpha channel.</span></span> <span data-ttu-id="57e9f-153">若要解決此問題，請採取下列步驟：</span><span class="sxs-lookup"><span data-stu-id="57e9f-153">To work around this, take the following steps:</span></span>

-   <span data-ttu-id="57e9f-154">使用 D3DSWAPEFFECT \_ 複製。</span><span class="sxs-lookup"><span data-stu-id="57e9f-154">Use D3DSWAPEFFECT\_COPY.</span></span>
-   <span data-ttu-id="57e9f-155">檢查 \_ \_ D3DCAPS9 結構的 Caps3 成員中的 D3DCAPS3 ALPHA 全螢幕 \_ 翻轉 \_ 或 \_ 捨棄[](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)旗標。</span><span class="sxs-lookup"><span data-stu-id="57e9f-155">Check the D3DCAPS3\_ALPHA\_FULLSCREEN\_FLIP\_OR\_DISCARD flag in the Caps3 member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure.</span></span> <span data-ttu-id="57e9f-156">此旗標指出 \_ 使用 D3DSWAPEFFECT FLIP 或 D3DSWAPEFFECT 捨棄時，驅動程式是否可以進行 Alpha 混色 \_ 。</span><span class="sxs-lookup"><span data-stu-id="57e9f-156">This flag indicates whether the driver can do alpha blending when D3DSWAPEFFECT\_FLIP or D3DSWAPEFFECT\_DISCARD is used.</span></span>
-   <span data-ttu-id="57e9f-157">使用翻轉模式交換效果的應用程式 (D3DSWAPEFFECT \_ FLIPEX) 應該在調整視窗大小或區域變更之後呼叫 [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) ，以確保顯示內容已更新。</span><span class="sxs-lookup"><span data-stu-id="57e9f-157">Applications using flip mode swap effect (D3DSWAPEFFECT\_FLIPEX) should call [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) after a window resize or region change to ensure that the display content is updated.</span></span>

<span data-ttu-id="57e9f-158">隱藏的視窗無法接收使用者模式事件;此外，隱藏的全螢幕視窗將干擾另一個應用程式視窗強制回應視窗的呈現。</span><span class="sxs-lookup"><span data-stu-id="57e9f-158">An invisible window cannot receive user-mode events; furthermore, an invisible-fullscreen window will interfere with the presentation of another applications' windowed-mode window.</span></span> <span data-ttu-id="57e9f-159">因此，每個應用程式都必須確保在以全螢幕模式顯示 swapchain 時，會顯示裝置視窗。</span><span class="sxs-lookup"><span data-stu-id="57e9f-159">Therefore, each application needs to ensure that a device window is visible when a swapchain is presented in fullscreen mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="57e9f-160">規格需求</span><span class="sxs-lookup"><span data-stu-id="57e9f-160">Requirements</span></span>

| <span data-ttu-id="57e9f-161">需求</span><span class="sxs-lookup"><span data-stu-id="57e9f-161">Requirement</span></span> | <span data-ttu-id="57e9f-162">值</span><span class="sxs-lookup"><span data-stu-id="57e9f-162">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="57e9f-163">標頭</span><span class="sxs-lookup"><span data-stu-id="57e9f-163">Header</span></span><br/> | <dl> <span data-ttu-id="57e9f-164"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="57e9f-164"><dt>D3D9Types.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="57e9f-165">另請參閱</span><span class="sxs-lookup"><span data-stu-id="57e9f-165">See also</span></span>

[<span data-ttu-id="57e9f-166">Direct3D 列舉</span><span class="sxs-lookup"><span data-stu-id="57e9f-166">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)

[<span data-ttu-id="57e9f-167">**IDirect3DDevice9::Reset**</span><span class="sxs-lookup"><span data-stu-id="57e9f-167">**IDirect3DDevice9::Reset**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)
