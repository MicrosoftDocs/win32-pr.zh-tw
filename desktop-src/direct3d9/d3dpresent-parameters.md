---
description: 描述呈現參數。
ms.assetid: d677aeb7-a188-4ddc-b8c9-48e13676e9c8
title: 'D3DPRESENT_PARAMETERS 結構 (D3D9Types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPRESENT_PARAMETERS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: f113b3df247765b958dfe47bb04fafb6c9a13bbe
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343103"
---
# <a name="d3dpresent_parameters-structure"></a><span data-ttu-id="1edc5-103">D3DPRESENT \_ 參數結構</span><span class="sxs-lookup"><span data-stu-id="1edc5-103">D3DPRESENT\_PARAMETERS structure</span></span>

<span data-ttu-id="1edc5-104">描述呈現參數。</span><span class="sxs-lookup"><span data-stu-id="1edc5-104">Describes the presentation parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="1edc5-105">語法</span><span class="sxs-lookup"><span data-stu-id="1edc5-105">Syntax</span></span>


```C++
typedef struct D3DPRESENT_PARAMETERS {
  UINT                BackBufferWidth;
  UINT                BackBufferHeight;
  D3DFORMAT           BackBufferFormat;
  UINT                BackBufferCount;
  D3DMULTISAMPLE_TYPE MultiSampleType;
  DWORD               MultiSampleQuality;
  D3DSWAPEFFECT       SwapEffect;
  HWND                hDeviceWindow;
  BOOL                Windowed;
  BOOL                EnableAutoDepthStencil;
  D3DFORMAT           AutoDepthStencilFormat;
  DWORD               Flags;
  UINT                FullScreen_RefreshRateInHz;
  UINT                PresentationInterval;
} D3DPRESENT_PARAMETERS, *LPD3DPRESENT_PARAMETERS;
```



## <a name="members"></a><span data-ttu-id="1edc5-106">成員</span><span class="sxs-lookup"><span data-stu-id="1edc5-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="1edc5-107">**BackBufferWidth**</span><span class="sxs-lookup"><span data-stu-id="1edc5-107">**BackBufferWidth**</span></span>
</dt> <dd>

<span data-ttu-id="1edc5-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1edc5-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1edc5-109">新交換鏈背景緩衝區的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="1edc5-109">Width of the new swap chain's back buffers, in pixels.</span></span> <span data-ttu-id="1edc5-110">如果 **視窗** 化是 **FALSE** (表示呈現全螢幕) ，此值必須等於透過 [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes)找到的其中一個列舉顯示模式的寬度。</span><span class="sxs-lookup"><span data-stu-id="1edc5-110">If **Windowed** is **FALSE** (the presentation is full-screen), this value must equal the width of one of the enumerated display modes found through [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes).</span></span> <span data-ttu-id="1edc5-111">如果 **視窗** 化為 **TRUE** ，且 **BackBufferWidth** 或 **BackBufferHeight** 為零，則會採用 **hDeviceWindow** (或焦點視窗之工作區的對應維度（如果 **hDeviceWindow** 為) **Null** ）。</span><span class="sxs-lookup"><span data-stu-id="1edc5-111">If **Windowed** is **TRUE** and either **BackBufferWidth** or **BackBufferHeight** is zero, the corresponding dimension of the client area of the **hDeviceWindow** (or the focus window, if **hDeviceWindow** is **NULL**) is taken.</span></span>

</dd> <dt>

<span data-ttu-id="1edc5-112">**BackBufferHeight**</span><span class="sxs-lookup"><span data-stu-id="1edc5-112">**BackBufferHeight**</span></span>
</dt> <dd>

<span data-ttu-id="1edc5-113">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1edc5-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1edc5-114">新交換鏈背景緩衝區的高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="1edc5-114">Height of the new swap chain's back buffers, in pixels.</span></span> <span data-ttu-id="1edc5-115">如果 **視窗** 化是 **FALSE** (表示呈現全螢幕) ，此值必須等於透過 [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes)找到的其中一個列舉顯示模式的高度。</span><span class="sxs-lookup"><span data-stu-id="1edc5-115">If **Windowed** is **FALSE** (the presentation is full-screen), this value must equal the height of one of the enumerated display modes found through [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes).</span></span> <span data-ttu-id="1edc5-116">如果 **視窗** 化為 **TRUE** ，且 **BackBufferWidth** 或 **BackBufferHeight** 為零，則會採用 **hDeviceWindow** (或焦點視窗之工作區的對應維度（如果 **hDeviceWindow** 為) **Null** ）。</span><span class="sxs-lookup"><span data-stu-id="1edc5-116">If **Windowed** is **TRUE** and either **BackBufferWidth** or **BackBufferHeight** is zero, the corresponding dimension of the client area of the **hDeviceWindow** (or the focus window, if **hDeviceWindow** is **NULL**) is taken.</span></span>

</dd> <dt>

<span data-ttu-id="1edc5-117">**BackBufferFormat**</span><span class="sxs-lookup"><span data-stu-id="1edc5-117">**BackBufferFormat**</span></span>
</dt> <dd>

<span data-ttu-id="1edc5-118">類型： **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="1edc5-118">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1edc5-119">背景緩衝區格式。</span><span class="sxs-lookup"><span data-stu-id="1edc5-119">The back buffer format.</span></span> <span data-ttu-id="1edc5-120">如需有關格式的詳細資訊，請參閱 [D3DFORMAT](d3dformat.md)。</span><span class="sxs-lookup"><span data-stu-id="1edc5-120">For more information about formats, see [D3DFORMAT](d3dformat.md).</span></span> <span data-ttu-id="1edc5-121">此值必須是 [**CheckDeviceType**](/windows/desktop/api)所驗證的轉譯目標格式之一。</span><span class="sxs-lookup"><span data-stu-id="1edc5-121">This value must be one of the render-target formats as validated by [**CheckDeviceType**](/windows/desktop/api).</span></span> <span data-ttu-id="1edc5-122">您可以使用 [**GetDisplayMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode) 來取得目前的格式。</span><span class="sxs-lookup"><span data-stu-id="1edc5-122">You can use [**GetDisplayMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode) to obtain the current format.</span></span>

<span data-ttu-id="1edc5-123">事實上， \_ 在視窗模式中，可以為 **BACKBUFFERFORMAT** 指定 D3DFMT UNKNOWN。</span><span class="sxs-lookup"><span data-stu-id="1edc5-123">In fact, D3DFMT\_UNKNOWN can be specified for the **BackBufferFormat** while in windowed mode.</span></span> <span data-ttu-id="1edc5-124">這會告知執行時間使用目前的顯示模式格式，並免除呼叫 [**GetDisplayMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode)的需求。</span><span class="sxs-lookup"><span data-stu-id="1edc5-124">This tells the runtime to use the current display-mode format and eliminates the need to call [**GetDisplayMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode).</span></span>

<span data-ttu-id="1edc5-125">針對視窗型應用程式，背景緩衝區格式不再需要符合顯示模式格式，因為硬體 (的色彩轉換現在可透過硬體支援) 的色彩轉換來完成。</span><span class="sxs-lookup"><span data-stu-id="1edc5-125">For windowed applications, the back buffer format no longer needs to match the display-mode format because color conversion can now be done by the hardware (if the hardware supports color conversion).</span></span> <span data-ttu-id="1edc5-126">可能會有一組可能的背景緩衝區格式受到限制，但執行時間允許將任何有效的背景緩衝區格式呈現給任何桌面格式。</span><span class="sxs-lookup"><span data-stu-id="1edc5-126">The set of possible back buffer formats is constrained, but the runtime will allow any valid back buffer format to be presented to any desktop format.</span></span> <span data-ttu-id="1edc5-127"> (裝置在桌面上可運作的額外需求;裝置通常不會以每圖元模式8位的方式運作。 ) </span><span class="sxs-lookup"><span data-stu-id="1edc5-127">(There is the additional requirement that the device be operable in the desktop; devices typically do not operate in 8 bits per pixel modes.)</span></span>

<span data-ttu-id="1edc5-128">全螢幕應用程式無法進行色彩轉換。</span><span class="sxs-lookup"><span data-stu-id="1edc5-128">Full-screen applications cannot do color conversion.</span></span>

</dd> <dt>

<span data-ttu-id="1edc5-129">**BackBufferCount**</span><span class="sxs-lookup"><span data-stu-id="1edc5-129">**BackBufferCount**</span></span>
</dt> <dd>

<span data-ttu-id="1edc5-130">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1edc5-130">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1edc5-131">此值可介於0和 [D3DPRESENT \_ 背景緩衝區 \_ 的 \_ 最大](d3dpresent-back-buffers.md) (或 [D3DPRESENT \_ 回 \_ 緩衝區 \_ 最大 \_ ](d3dpresent-back-buffers.md) 值（例如，使用 Direct3D 9Ex) ）。</span><span class="sxs-lookup"><span data-stu-id="1edc5-131">This value can be between 0 and [D3DPRESENT\_BACK\_BUFFERS\_MAX](d3dpresent-back-buffers.md) (or [D3DPRESENT\_BACK\_BUFFERS\_MAX\_EX](d3dpresent-back-buffers.md) when using Direct3D 9Ex).</span></span> <span data-ttu-id="1edc5-132">0的值會被視為1。</span><span class="sxs-lookup"><span data-stu-id="1edc5-132">Values of 0 are treated as 1.</span></span> <span data-ttu-id="1edc5-133">如果無法建立背景緩衝區的數目，則執行時間將會使方法呼叫失敗，並以可建立的背景緩衝區數目填入此值。</span><span class="sxs-lookup"><span data-stu-id="1edc5-133">If the number of back buffers cannot be created, the runtime will fail the method call and fill this value with the number of back buffers that could be created.</span></span> <span data-ttu-id="1edc5-134">因此，應用程式可以使用相同的 D3DPRESENT 參數結構來呼叫方法兩次， \_ 並預期它會在第二次運作。</span><span class="sxs-lookup"><span data-stu-id="1edc5-134">As a result, an application can call the method twice with the same D3DPRESENT\_PARAMETERS structure and expect it to work the second time.</span></span>

<span data-ttu-id="1edc5-135">如果無法建立一個背景緩衝區，方法會失敗。</span><span class="sxs-lookup"><span data-stu-id="1edc5-135">The method fails if one back buffer cannot be created.</span></span> <span data-ttu-id="1edc5-136">**BackBufferCount** 的值會影響允許的交換效果集。</span><span class="sxs-lookup"><span data-stu-id="1edc5-136">The value of **BackBufferCount** influences what set of swap effects are allowed.</span></span> <span data-ttu-id="1edc5-137">具體而言，任何 D3DSWAPEFFECT \_ 複製交換效果都需要只有一個背景緩衝區。</span><span class="sxs-lookup"><span data-stu-id="1edc5-137">Specifically, any D3DSWAPEFFECT\_COPY swap effect requires that there be exactly one back buffer.</span></span>

</dd> <dt>

<span data-ttu-id="1edc5-138">**MultiSampleType**</span><span class="sxs-lookup"><span data-stu-id="1edc5-138">**MultiSampleType**</span></span>
</dt> <dd>

<span data-ttu-id="1edc5-139">類型： **[ **D3DMULTISAMPLE \_ 類型**](./d3dmultisample-type.md)**</span><span class="sxs-lookup"><span data-stu-id="1edc5-139">Type: **[**D3DMULTISAMPLE\_TYPE**](./d3dmultisample-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1edc5-140">[**D3DMULTISAMPLE \_ 型**](./d3dmultisample-type.md)別列舉型別的成員。</span><span class="sxs-lookup"><span data-stu-id="1edc5-140">Member of the [**D3DMULTISAMPLE\_TYPE**](./d3dmultisample-type.md) enumerated type.</span></span> <span data-ttu-id="1edc5-141">\_除非 **SwapEffect** 已設定為 D3DSWAPEFFECT 捨棄，否則值必須是 D3DMULTISAMPLE NONE \_ 。</span><span class="sxs-lookup"><span data-stu-id="1edc5-141">The value must be D3DMULTISAMPLE\_NONE unless **SwapEffect** has been set to D3DSWAPEFFECT\_DISCARD.</span></span> <span data-ttu-id="1edc5-142">只有在交換效果為 D3DSWAPEFFECT 捨棄時，才支援取樣 \_ 。</span><span class="sxs-lookup"><span data-stu-id="1edc5-142">Multisampling is supported only if the swap effect is D3DSWAPEFFECT\_DISCARD.</span></span>

</dd> <dt>

<span data-ttu-id="1edc5-143">**MultiSampleQuality**</span><span class="sxs-lookup"><span data-stu-id="1edc5-143">**MultiSampleQuality**</span></span>
</dt> <dd>

<span data-ttu-id="1edc5-144">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1edc5-144">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1edc5-145">品質層級。</span><span class="sxs-lookup"><span data-stu-id="1edc5-145">Quality level.</span></span> <span data-ttu-id="1edc5-146">有效範圍介於零到1之間，且小於 [**CheckDeviceMultiSampleType**](/windows/desktop/api)所使用的 pQualityLevels 所傳回的層級。</span><span class="sxs-lookup"><span data-stu-id="1edc5-146">The valid range is between zero and one less than the level returned by pQualityLevels used by [**CheckDeviceMultiSampleType**](/windows/desktop/api).</span></span> <span data-ttu-id="1edc5-147">傳遞較大的值會傳回錯誤 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="1edc5-147">Passing a larger value returns the error D3DERR\_INVALIDCALL.</span></span> <span data-ttu-id="1edc5-148">轉譯目標或深度樣板表面和 [**D3DMULTISAMPLE \_ 類型**](./d3dmultisample-type.md) 的成對值必須相符。</span><span class="sxs-lookup"><span data-stu-id="1edc5-148">Paired values of render targets or of depth stencil surfaces and [**D3DMULTISAMPLE\_TYPE**](./d3dmultisample-type.md) must match.</span></span>

</dd> <dt>

<span data-ttu-id="1edc5-149">**SwapEffect**</span><span class="sxs-lookup"><span data-stu-id="1edc5-149">**SwapEffect**</span></span>
</dt> <dd>

<span data-ttu-id="1edc5-150">類型： **[ **D3DSWAPEFFECT**](./d3dswapeffect.md)**</span><span class="sxs-lookup"><span data-stu-id="1edc5-150">Type: **[**D3DSWAPEFFECT**](./d3dswapeffect.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1edc5-151">[**D3DSWAPEFFECT**](./d3dswapeffect.md)列舉型別的成員。</span><span class="sxs-lookup"><span data-stu-id="1edc5-151">Member of the [**D3DSWAPEFFECT**](./d3dswapeffect.md) enumerated type.</span></span> <span data-ttu-id="1edc5-152">執行時間會保證有關緩衝區交換行為的隱含語義;因此，如果 **視窗** 化為 **TRUE** ，且 **SwapEffect** 設定為 D3DSWAPEFFECT \_ FLIP，則執行時間會建立一個額外的背景緩衝區，並複製以何種方式在簡報時成為前端緩衝區。</span><span class="sxs-lookup"><span data-stu-id="1edc5-152">The runtime will guarantee the implied semantics concerning buffer swap behavior; therefore, if **Windowed** is **TRUE** and **SwapEffect** is set to D3DSWAPEFFECT\_FLIP, the runtime will create one extra back buffer and copy whichever becomes the front buffer at presentation time.</span></span>

<span data-ttu-id="1edc5-153">D3DSWAPEFFECT \_ COPY 需要將 **BackBufferCount** 設定為1。</span><span class="sxs-lookup"><span data-stu-id="1edc5-153">D3DSWAPEFFECT\_COPY requires that **BackBufferCount** be set to 1.</span></span>

<span data-ttu-id="1edc5-154">\_在偵錯工具執行時間中，將會在出現任何緩衝區時填入任何緩衝區來強制執行 D3DSWAPEFFECT 捨棄。</span><span class="sxs-lookup"><span data-stu-id="1edc5-154">D3DSWAPEFFECT\_DISCARD will be enforced in the debug runtime by filling any buffer with noise after it is presented.</span></span>

<span data-ttu-id="1edc5-155">Direct3D9 和 Direct3D9Ex 之間的差異：</span><span class="sxs-lookup"><span data-stu-id="1edc5-155">Differences between Direct3D9 and Direct3D9Ex:</span></span>

- <span data-ttu-id="1edc5-156">在 Direct3D9Ex 中， \_ 會加入 D3DSWAPEFFECT FLIPEX，以指定應用程式採用翻轉模式的時機。</span><span class="sxs-lookup"><span data-stu-id="1edc5-156">In Direct3D9Ex, D3DSWAPEFFECT\_FLIPEX is added to designate when an application is adopting flip mode.</span></span> <span data-ttu-id="1edc5-157">也就是說，whan 應用程式的框架會以視窗的模式傳遞 (而不是複製) 至桌面視窗管理員 (DWM) 以進行組合。</span><span class="sxs-lookup"><span data-stu-id="1edc5-157">That is, whan an application's frame is passed in window's mode (instead of copied) to the Desktop Window Manager(DWM) for composition.</span></span> <span data-ttu-id="1edc5-158">Flip 模式提供更有效率的記憶體頻寬，並可讓應用程式利用全螢幕顯示的統計資料。</span><span class="sxs-lookup"><span data-stu-id="1edc5-158">Flip mode provides more efficient memory bandwidth and enables an application to take advantage of full-screen-present statistics.</span></span> <span data-ttu-id="1edc5-159">它不會變更全螢幕行為。</span><span class="sxs-lookup"><span data-stu-id="1edc5-159">It does not change full screen behavior.</span></span> <span data-ttu-id="1edc5-160">從 Windows 7 開始提供翻轉模式行為。</span><span class="sxs-lookup"><span data-stu-id="1edc5-160">Flip mode behavior is available beginning with Windows 7.</span></span>



 

</dd> <dt>

<span data-ttu-id="1edc5-161">**hDeviceWindow**</span><span class="sxs-lookup"><span data-stu-id="1edc5-161">**hDeviceWindow**</span></span>
</dt> <dd>

<span data-ttu-id="1edc5-162">類型： **[ **HWND**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1edc5-162">Type: **[**HWND**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1edc5-163">裝置視窗會決定螢幕上的背景緩衝區位置和大小。</span><span class="sxs-lookup"><span data-stu-id="1edc5-163">The device window determines the location and size of the back buffer on screen.</span></span> <span data-ttu-id="1edc5-164">當背景緩衝區內容在 [**存在**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)時複製到前端緩衝區時，Direct3D 會使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="1edc5-164">This is used by Direct3D when the back buffer contents are copied to the front buffer during [**Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).</span></span>

-   <span data-ttu-id="1edc5-165">針對全螢幕應用程式，這是最上層視窗的控制碼 (也就是焦點視窗) 。</span><span class="sxs-lookup"><span data-stu-id="1edc5-165">For a full-screen application, this is a handle to the top window (which is the focus window).</span></span>

    <span data-ttu-id="1edc5-166">針對使用多部全螢幕裝置 (例如 multimonitor 系統) 的應用程式，只有一部裝置可以使用焦點視窗作為裝置視窗。</span><span class="sxs-lookup"><span data-stu-id="1edc5-166">For applications that use multiple full-screen devices (such as a multimonitor system), exactly one device can use the focus window as the device window.</span></span> <span data-ttu-id="1edc5-167">所有其他裝置都必須有唯一的裝置視窗。</span><span class="sxs-lookup"><span data-stu-id="1edc5-167">All other devices must have unique device windows.</span></span>

-   <span data-ttu-id="1edc5-168">如果是視窗模式的應用程式，這個控制碼將會是 [**目前**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)的預設目標視窗。</span><span class="sxs-lookup"><span data-stu-id="1edc5-168">For a windowed-mode application, this handle will be the default target window for [**Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).</span></span> <span data-ttu-id="1edc5-169">如果此控制碼為 **Null**，則會採用焦點視窗。</span><span class="sxs-lookup"><span data-stu-id="1edc5-169">If this handle is **NULL**, the focus window will be taken.</span></span>

<span data-ttu-id="1edc5-170">請注意，執行時間不會嘗試在視窗大小中反映使用者變更。</span><span class="sxs-lookup"><span data-stu-id="1edc5-170">Note that no attempt is made by the runtime to reflect user changes in window size.</span></span> <span data-ttu-id="1edc5-171">重設此視窗時，不會隱含地重設背景緩衝區。</span><span class="sxs-lookup"><span data-stu-id="1edc5-171">The back buffer is not implicitly reset when this window is reset.</span></span> <span data-ttu-id="1edc5-172">不過， [**目前**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) 的方法會自動追蹤視窗位置的變更。</span><span class="sxs-lookup"><span data-stu-id="1edc5-172">However, the [**Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) method does automatically track window position changes.</span></span>

</dd> <dt>

<span data-ttu-id="1edc5-173">**視窗**</span><span class="sxs-lookup"><span data-stu-id="1edc5-173">**Windowed**</span></span>
</dt> <dd>

<span data-ttu-id="1edc5-174">類型： **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1edc5-174">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1edc5-175">如果應用程式以視窗視窗執行，則 **為 TRUE** ;如果應用程式全螢幕執行，則 **為 FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="1edc5-175">**TRUE** if the application runs windowed; **FALSE** if the application runs full-screen.</span></span>

</dd> <dt>

<span data-ttu-id="1edc5-176">**EnableAutoDepthStencil**</span><span class="sxs-lookup"><span data-stu-id="1edc5-176">**EnableAutoDepthStencil**</span></span>
</dt> <dd>

<span data-ttu-id="1edc5-177">類型： **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1edc5-177">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1edc5-178">如果這個值為 **TRUE**，Direct3D 將會管理應用程式的深度緩衝區。</span><span class="sxs-lookup"><span data-stu-id="1edc5-178">If this value is **TRUE**, Direct3D will manage depth buffers for the application.</span></span> <span data-ttu-id="1edc5-179">裝置會在建立時建立深度樣板緩衝區。</span><span class="sxs-lookup"><span data-stu-id="1edc5-179">The device will create a depth-stencil buffer when it is created.</span></span> <span data-ttu-id="1edc5-180">深度樣板緩衝區將會自動設定為裝置的呈現目標。</span><span class="sxs-lookup"><span data-stu-id="1edc5-180">The depth-stencil buffer will be automatically set as the render target of the device.</span></span> <span data-ttu-id="1edc5-181">當裝置重設時，會自動終結深度樣板緩衝區，並在新的大小中重新建立。</span><span class="sxs-lookup"><span data-stu-id="1edc5-181">When the device is reset, the depth-stencil buffer will be automatically destroyed and recreated in the new size.</span></span>

<span data-ttu-id="1edc5-182">如果 EnableAutoDepthStencil 為 **TRUE**，則 AutoDepthStencilFormat 必須是有效的深度樣板格式。</span><span class="sxs-lookup"><span data-stu-id="1edc5-182">If EnableAutoDepthStencil is **TRUE**, then AutoDepthStencilFormat must be a valid depth-stencil format.</span></span>

</dd> <dt>

<span data-ttu-id="1edc5-183">**AutoDepthStencilFormat**</span><span class="sxs-lookup"><span data-stu-id="1edc5-183">**AutoDepthStencilFormat**</span></span>
</dt> <dd>

<span data-ttu-id="1edc5-184">類型： **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="1edc5-184">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1edc5-185">[D3DFORMAT](d3dformat.md)列舉型別的成員。</span><span class="sxs-lookup"><span data-stu-id="1edc5-185">Member of the [D3DFORMAT](d3dformat.md) enumerated type.</span></span> <span data-ttu-id="1edc5-186">裝置將建立之自動深度樣板表面的格式。</span><span class="sxs-lookup"><span data-stu-id="1edc5-186">The format of the automatic depth-stencil surface that the device will create.</span></span> <span data-ttu-id="1edc5-187">除非 **EnableAutoDepthStencil** 為 **TRUE**，否則會忽略這個成員。</span><span class="sxs-lookup"><span data-stu-id="1edc5-187">This member is ignored unless **EnableAutoDepthStencil** is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="1edc5-188">**旗標**</span><span class="sxs-lookup"><span data-stu-id="1edc5-188">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="1edc5-189">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1edc5-189">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1edc5-190">其中一個 [D3DPRESENTFLAG](d3dpresentflag.md) 常數。</span><span class="sxs-lookup"><span data-stu-id="1edc5-190">One of the [D3DPRESENTFLAG](d3dpresentflag.md) constants.</span></span>

</dd> <dt>

<span data-ttu-id="1edc5-191">**全螢幕 \_ RefreshRateInHz**</span><span class="sxs-lookup"><span data-stu-id="1edc5-191">**FullScreen\_RefreshRateInHz**</span></span>
</dt> <dd>

<span data-ttu-id="1edc5-192">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1edc5-192">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1edc5-193">顯示配接器重新整理畫面的速率。</span><span class="sxs-lookup"><span data-stu-id="1edc5-193">The rate at which the display adapter refreshes the screen.</span></span> <span data-ttu-id="1edc5-194">此值取決於應用程式執行的模式：</span><span class="sxs-lookup"><span data-stu-id="1edc5-194">The value depends on the mode in which the application is running:</span></span>

-   <span data-ttu-id="1edc5-195">若為視窗型模式，重新整理率必須為0。</span><span class="sxs-lookup"><span data-stu-id="1edc5-195">For windowed mode, the refresh rate must be 0.</span></span>
-   <span data-ttu-id="1edc5-196">在全螢幕模式中，重新整理頻率是 [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes)所傳回的其中一個重新整理速率。</span><span class="sxs-lookup"><span data-stu-id="1edc5-196">For full-screen mode, the refresh rate is one of the refresh rates returned by [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes).</span></span>

</dd> <dt>

<span data-ttu-id="1edc5-197">**PresentationInterval**</span><span class="sxs-lookup"><span data-stu-id="1edc5-197">**PresentationInterval**</span></span>
</dt> <dd>

<span data-ttu-id="1edc5-198">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1edc5-198">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1edc5-199">交換鏈的背景緩衝區可以呈現到前端緩衝區的最大速率。</span><span class="sxs-lookup"><span data-stu-id="1edc5-199">The maximum rate at which the swap chain's back buffers can be presented to the front buffer.</span></span> <span data-ttu-id="1edc5-200">如需模式和所支援間隔的詳細說明，請參閱 [D3DPRESENT](d3dpresent.md)。</span><span class="sxs-lookup"><span data-stu-id="1edc5-200">For a detailed explanation of the modes and the intervals that are supported, see [D3DPRESENT](d3dpresent.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1edc5-201">規格需求</span><span class="sxs-lookup"><span data-stu-id="1edc5-201">Requirements</span></span>



| <span data-ttu-id="1edc5-202">需求</span><span class="sxs-lookup"><span data-stu-id="1edc5-202">Requirement</span></span> | <span data-ttu-id="1edc5-203">值</span><span class="sxs-lookup"><span data-stu-id="1edc5-203">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1edc5-204">標頭</span><span class="sxs-lookup"><span data-stu-id="1edc5-204">Header</span></span><br/> | <dl> <span data-ttu-id="1edc5-205"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="1edc5-205"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1edc5-206">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1edc5-206">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1edc5-207">Direct3D 結構</span><span class="sxs-lookup"><span data-stu-id="1edc5-207">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="1edc5-208">**CreateDevice**</span><span class="sxs-lookup"><span data-stu-id="1edc5-208">**CreateDevice**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)
</dt> <dt>

[<span data-ttu-id="1edc5-209">**CreateAdditionalSwapChain**</span><span class="sxs-lookup"><span data-stu-id="1edc5-209">**CreateAdditionalSwapChain**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain)
</dt> <dt>

[<span data-ttu-id="1edc5-210">**目前**</span><span class="sxs-lookup"><span data-stu-id="1edc5-210">**Present**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)
</dt> <dt>

[<span data-ttu-id="1edc5-211">**重設**</span><span class="sxs-lookup"><span data-stu-id="1edc5-211">**Reset**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)
</dt> </dl>

 

 
