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
ms.openlocfilehash: f83ab03773356a01c8c6ac490bb099c6e7508be2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323000"
---
# <a name="d3dpresent_parameters-structure"></a>D3DPRESENT \_ 參數結構

描述呈現參數。

## <a name="syntax"></a>語法


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



## <a name="members"></a>成員

<dl> <dt>

**BackBufferWidth**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

新交換鏈背景緩衝區的寬度（以圖元為單位）。 如果 **視窗** 化是 **FALSE** (表示呈現全螢幕) ，此值必須等於透過 [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes)找到的其中一個列舉顯示模式的寬度。 如果 **視窗** 化為 **TRUE** ，且 **BackBufferWidth** 或 **BackBufferHeight** 為零，則會採用 **hDeviceWindow** (或焦點視窗之工作區的對應維度（如果 **hDeviceWindow** 為) **Null** ）。

</dd> <dt>

**BackBufferHeight**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

新交換鏈背景緩衝區的高度（以圖元為單位）。 如果 **視窗** 化是 **FALSE** (表示呈現全螢幕) ，此值必須等於透過 [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes)找到的其中一個列舉顯示模式的高度。 如果 **視窗** 化為 **TRUE** ，且 **BackBufferWidth** 或 **BackBufferHeight** 為零，則會採用 **hDeviceWindow** (或焦點視窗之工作區的對應維度（如果 **hDeviceWindow** 為) **Null** ）。

</dd> <dt>

**BackBufferFormat**
</dt> <dd>

類型： **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

背景緩衝區格式。 如需有關格式的詳細資訊，請參閱 [D3DFORMAT](d3dformat.md)。 此值必須是 [**CheckDeviceType**](/windows/desktop/api)所驗證的轉譯目標格式之一。 您可以使用 [**GetDisplayMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode) 來取得目前的格式。

事實上， \_ 在視窗模式中，可以為 **BACKBUFFERFORMAT** 指定 D3DFMT UNKNOWN。 這會告知執行時間使用目前的顯示模式格式，並免除呼叫 [**GetDisplayMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode)的需求。

針對視窗型應用程式，背景緩衝區格式不再需要符合顯示模式格式，因為硬體 (的色彩轉換現在可透過硬體支援) 的色彩轉換來完成。 可能會有一組可能的背景緩衝區格式受到限制，但執行時間允許將任何有效的背景緩衝區格式呈現給任何桌面格式。  (裝置在桌面上可運作的額外需求;裝置通常不會以每圖元模式8位的方式運作。 ) 

全螢幕應用程式無法進行色彩轉換。

</dd> <dt>

**BackBufferCount**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

此值可介於0和 [D3DPRESENT \_ 背景緩衝區 \_ 的 \_ 最大](d3dpresent-back-buffers.md) (或 [D3DPRESENT \_ 回 \_ 緩衝區 \_ 最大 \_ ](d3dpresent-back-buffers.md) 值（例如，使用 Direct3D 9Ex) ）。 0的值會被視為1。 如果無法建立背景緩衝區的數目，則執行時間將會使方法呼叫失敗，並以可建立的背景緩衝區數目填入此值。 因此，應用程式可以使用相同的 D3DPRESENT 參數結構來呼叫方法兩次， \_ 並預期它會在第二次運作。

如果無法建立一個背景緩衝區，方法會失敗。 **BackBufferCount** 的值會影響允許的交換效果集。 具體而言，任何 D3DSWAPEFFECT \_ 複製交換效果都需要只有一個背景緩衝區。

</dd> <dt>

**MultiSampleType**
</dt> <dd>

類型： **[ **D3DMULTISAMPLE \_ 類型**](./d3dmultisample-type.md)**

</dd> <dd>

[**D3DMULTISAMPLE \_ 型**](./d3dmultisample-type.md)別列舉型別的成員。 \_除非 **SwapEffect** 已設定為 D3DSWAPEFFECT 捨棄，否則值必須是 D3DMULTISAMPLE NONE \_ 。 只有在交換效果為 D3DSWAPEFFECT 捨棄時，才支援取樣 \_ 。

</dd> <dt>

**MultiSampleQuality**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

品質層級。 有效範圍介於零到1之間，且小於 [**CheckDeviceMultiSampleType**](/windows/desktop/api)所使用的 pQualityLevels 所傳回的層級。 傳遞較大的值會傳回錯誤 D3DERR \_ INVALIDCALL。 轉譯目標或深度樣板表面和 [**D3DMULTISAMPLE \_ 類型**](./d3dmultisample-type.md) 的成對值必須相符。

</dd> <dt>

**SwapEffect**
</dt> <dd>

類型： **[ **D3DSWAPEFFECT**](./d3dswapeffect.md)**

</dd> <dd>

[**D3DSWAPEFFECT**](./d3dswapeffect.md)列舉型別的成員。 執行時間會保證有關緩衝區交換行為的隱含語義;因此，如果 **視窗** 化為 **TRUE** ，且 **SwapEffect** 設定為 D3DSWAPEFFECT \_ FLIP，則執行時間會建立一個額外的背景緩衝區，並複製以何種方式在簡報時成為前端緩衝區。

D3DSWAPEFFECT \_ COPY 需要將 **BackBufferCount** 設定為1。

\_在偵錯工具執行時間中，將會在出現任何緩衝區時填入任何緩衝區來強制執行 D3DSWAPEFFECT 捨棄。



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Direct3D9 和 Direct3D9Ex 之間的差異<br/> 在 Direct3D9Ex 中， \_ 會加入 D3DSWAPEFFECT FLIPEX，以指定應用程式採用翻轉模式的時機。 也就是說，whan 應用程式的框架會以視窗的模式傳遞 (而不是複製) 至桌面視窗管理員 (DWM) 以進行組合。 Flip 模式提供更有效率的記憶體頻寬，並可讓應用程式利用全螢幕顯示的統計資料。 它不會變更全螢幕行為。 從 Windows 7 開始提供翻轉模式行為。<br/> |



 

</dd> <dt>

**hDeviceWindow**
</dt> <dd>

類型： **[ **HWND**](../winprog/windows-data-types.md)**

</dd> <dd>

裝置視窗會決定螢幕上的背景緩衝區位置和大小。 當背景緩衝區內容在 [**存在**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)時複製到前端緩衝區時，Direct3D 會使用這項功能。

-   針對全螢幕應用程式，這是最上層視窗的控制碼 (也就是焦點視窗) 。

    針對使用多部全螢幕裝置 (例如 multimonitor 系統) 的應用程式，只有一部裝置可以使用焦點視窗作為裝置視窗。 所有其他裝置都必須有唯一的裝置視窗。

-   如果是視窗模式的應用程式，這個控制碼將會是 [**目前**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)的預設目標視窗。 如果此控制碼為 **Null**，則會採用焦點視窗。

請注意，執行時間不會嘗試在視窗大小中反映使用者變更。 重設此視窗時，不會隱含地重設背景緩衝區。 不過， [**目前**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) 的方法會自動追蹤視窗位置的變更。

</dd> <dt>

**視窗**
</dt> <dd>

類型： **[ **BOOL**](../winprog/windows-data-types.md)**

</dd> <dd>

如果應用程式以視窗視窗執行，則 **為 TRUE** ;如果應用程式全螢幕執行，則 **為 FALSE** 。

</dd> <dt>

**EnableAutoDepthStencil**
</dt> <dd>

類型： **[ **BOOL**](../winprog/windows-data-types.md)**

</dd> <dd>

如果這個值為 **TRUE**，Direct3D 將會管理應用程式的深度緩衝區。 裝置會在建立時建立深度樣板緩衝區。 深度樣板緩衝區將會自動設定為裝置的呈現目標。 當裝置重設時，會自動終結深度樣板緩衝區，並在新的大小中重新建立。

如果 EnableAutoDepthStencil 為 **TRUE**，則 AutoDepthStencilFormat 必須是有效的深度樣板格式。

</dd> <dt>

**AutoDepthStencilFormat**
</dt> <dd>

類型： **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

[D3DFORMAT](d3dformat.md)列舉型別的成員。 裝置將建立之自動深度樣板表面的格式。 除非 **EnableAutoDepthStencil** 為 **TRUE**，否則會忽略這個成員。

</dd> <dt>

**旗標**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

其中一個 [D3DPRESENTFLAG](d3dpresentflag.md) 常數。

</dd> <dt>

**全螢幕 \_ RefreshRateInHz**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

顯示配接器重新整理畫面的速率。 此值取決於應用程式執行的模式：

-   若為視窗型模式，重新整理率必須為0。
-   在全螢幕模式中，重新整理頻率是 [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes)所傳回的其中一個重新整理速率。

</dd> <dt>

**PresentationInterval**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

交換鏈的背景緩衝區可以呈現到前端緩衝區的最大速率。 如需模式和所支援間隔的詳細說明，請參閱 [D3DPRESENT](d3dpresent.md)。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3D9Types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 結構](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)
</dt> <dt>

[**CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain)
</dt> <dt>

[**目前**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)
</dt> <dt>

[**重設**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)
</dt> </dl>

 

 
