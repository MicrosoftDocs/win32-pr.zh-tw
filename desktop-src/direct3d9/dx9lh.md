---
description: 本檔特別提到適用于 DirectX 圖形的 Windows Vista 擴充功能。
ms.assetid: 3cc0b08c-e126-4f1b-b5d1-0d6c1ebeb0c5
title: Windows Vista) 的功能摘要 (Direct3D 9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d5cf2447297b7f24edf7d0200e640d5aef90bff
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106970692"
---
# <a name="feature-summary-direct3d-9-for-windows-vista"></a>Windows Vista) 的功能摘要 (Direct3D 9

本檔特別提到適用于 DirectX 圖形的 Windows Vista 擴充功能。 若要開發 Windows Vista 的 DirectX 功能，您必須安裝 Windows Vista SDK 和 DirectX SDK。 使用適用于 Windows Vista 的 DirectX 的應用程式必須使用使用 WDDM 驅動程式 (Windows 設備磁碟機模型) 而非 (XP 驅動程式模型) ;未執行 WDDM 的驅動程式無法具現化 Windows Vista DirectX 圖形介面。

在下列其中一節中探索 Windows Vista 的新 DirectX 圖形功能：

-   [裝置行為變更](#device-behavior-changes)
-   [停用多執行緒軟體頂點處理](#disabling-multithreaded-software-vertex-processing)
-   [一個位表面](#one-bit-surfaces)
-   [讀取深度/樣板緩衝區](#reading-depthstencil-buffers)
-   [共用資源](#sharing-resources)
-   [混合之前的 sRGB 轉換](#srgb-conversion-before-blending)
-   [StretchRect 改進](#stretchrect-improvements)
-   [系統記憶體中的材質建立](#texture-creation-in-system-memory)

## <a name="device-behavior-changes"></a>裝置行為變更

裝置現在只會在兩個情況下遺失;當硬體因為停止運作而重設時，以及設備磁碟機停止時。 當硬體停止回應時，可以藉由呼叫 [**ResetEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-resetex)來重設裝置。 如果硬體停止回應，則會遺失紋理記憶體。

停止驅動程式之後，必須重新建立 IDirect9Ex 物件才能繼續轉譯。

當視窗模式中的另一個視窗隱藏表示區，或將全螢幕應用程式最小化時， [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) 會傳回 S \_ D3DPRESENTATIONOCCLUDED。 全螢幕應用程式可在收到 [**WM \_ ACTI加值稅EAPP**](../winmsg/wm-activateapp.md) 回呼訊息時繼續呈現。

在舊版 DirectX 中，當應用程式發生模式變更時，復原的唯一方法是重設裝置，並重新建立所有的視訊記憶體資源和交換鏈。 現在有了適用于 Windows Vista 的 DirectX，在模式變更之後呼叫 Reset，並不會造成材質記憶體表面、材質和狀態資訊遺失，也不需要重新建立這些資源。

## <a name="disabling-multithreaded-software-vertex-processing"></a>停用多執行緒軟體頂點處理

新的 cap 位 (D3DCREATE \_ 停用 \_ PSGP \_ 執行緒) 已加入，將會停用 (swvp) 之軟體頂點處理的多執行緒處理。 使用此宏來產生 IDirect3D9：： CreateDevice 的行為旗標。


```
#define D3DCREATE_DISABLE_PSGP_THREADING
```



## <a name="one-bit-surfaces"></a>一個位表面

有一個新的 bit 介面格式類型，特別適合用來處理文字字元。 新的格式稱為 D3DFMT \_ A1。 一個位介面是設計用來作為個別圖元材質，或是 ComposeRects 或 ColorFill 所產生的轉譯目標輸出。 表面寬度和高度沒有個別的帽;實作為必須支援2K 材質 x 8K 材質的單一大小介面。

每個材質都有一個位介面;因此，其中一個表示所有元件 (r、g、b、圖元的) 為1，而零則表示所有的元件都等於0。 您可以搭配下列 Api 使用一個位介面： ColorFill、UpdateSurface 和 UpdateTexture。

當某個位介面被讀取時，執行時間可以執行 point 樣本或卷積篩選。 您可以調整卷積篩選 (查看 [**SetConvolutionMonoKernel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-setconvolutionmonokernel)) 。

一個位介面有一些限制：

-   Mip-不支援對應
-   sRGB 資料無法讀取或寫入至單一位介面。
-   一個位介面不能當做頂點材質或用於交叉取樣。

## <a name="reading-depthstencil-buffers"></a>讀取深度/樣板緩衝區

使用 IDirect3DDevice9：： UpdateSurface 來讀取或寫入從 IDirect3DDevice9：： CreateDepthStencilSurface 或 IDirect3DDevice9：： GetDepthStencilSurface 取得之表面的深度/樣板資料。

首先，使用 IDirect3DDevice9：： CreateOffscreenPlainSurface 建立僅限「鎖定」、「僅深度」或「僅樣板」介面。 請使用下列其中一個格式：

-   D3DFMT \_ D16 的 \_ 鎖定
-   D3DFMT \_ D32F 的 \_ 鎖定
-   D3DFMT \_ D32 的 \_ 鎖定
-   D3DFMT \_ S8 的 \_ 鎖定

其次，在深度/樣板緩衝區和新建立的「鎖定深度」或「樣板介面」之間傳輸資料。 此傳輸會使用 IDirect3DDevice9：： UpdateSurface 來執行。

當兩個介面都是可鎖定的格式，或兩者都不是可鎖定時，UpdateSurface 將會失敗。

傳送不存在的資料會導致錯誤 (例如，從非可鎖定深度介面傳送到 D3DFMT \_ S8 可 \_ 鎖定的介面) 。

IDirect3DDevice9：： UpdateSurface 的其餘限制仍然適用。

## <a name="sharing-resources"></a>共用資源

Direct3D 資源現在可以在裝置或進程之間共用。 這適用于任何 Direct3D 資源，包括紋理、頂點緩衝區、索引緩衝區或介面 (例如轉譯目標、深度樣板緩衝區或螢幕一般表面) 。 若要共用，您必須在建立時指定要共用的資源，並在預設集區中找出資源 (D3DPOOL \_ 預設) 。 建立資源以供共用之後，就可以在程式內的所有裝置間共用，或在進程間共用。

若要啟用共用資源，資源建立 Api 會有額外的控制碼參數。 這是指向共用資源的控制碼。 在先前的 DirectX 版本中，此引數已是 API 簽章的一部分，但是未使用且必須設定為 **Null**。 從 Windows Vista 開始，請以下列方式使用 pSharedHandle：

-   將指標 (pSharedHandle) 設定為 **Null** ，就不會共用資源。 這就像是 Windows Vista 之前的 DirectX 行為。
-   若要建立共用資源，請呼叫任何資源建立 API (查看下列) 使用未初始化的控制碼 (指標本身不是 **null** (pSharedHandle！ = **null**) ，但指標指向 **null** 值 (\* pSharedHandle = = **null**) ) 。 API 將會產生共用資源，並傳回有效的控制碼。
-   若要使用非 Null 共用資源控制碼來開啟和存取先前建立的共用資源，請將 pSharedHandle 設定為該控制碼的位址。 以這種方式開啟先前建立的共用資源之後，您可以在 Direct3D 9 或 Direct3D 9Ex API 中使用傳回的介面，如同介面是該類型的一般資源。

資源建立 Api 包括- [**CreateTexture**](/windows/desktop/api)、 [**CreateVolumeTexture**](/windows/desktop/api)、 [**CreateCubeTexture**](/windows/desktop/api)、 [**CreateRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget)、 [**CreateVertexBuffer**](/windows/desktop/api)、 [**CreateIndexBuffer**](/windows/desktop/api)、 [**CreateDepthStencilSurface**](/windows/desktop/api)、 [**CreateOffscreenPlainSurface**](/windows/desktop/api)、 [**CreateDepthStencilSurfaceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-createdepthstencilsurfaceex)、 [**CreateOffscreenPlainSurfaceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-createoffscreenplainsurfaceex)和 [**CreateRenderTargetEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-createrendertargetex)。

使用共用資源有一些限制。 這些包括：

-   您用來開啟共用資源的 API 必須符合您用來建立共用資源的 API。 例如，如果您使用 [**CreateTexture**](/windows/desktop/api) 來建立共用資源，就必須使用 **CreateTexture** 來開啟該共用資源;如果您使用 [**CreateRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget) 來建立共用資源，就必須使用 **CreateRenderTarget** 來開啟該共用資源; 依此類推。
-   當您開啟共用資源時，您必須指定 D3DPOOL \_ 預設值。
-   使用 D3DUSAGE \_ 動態、頂點緩衝區和索引緩衝區的可鎖定資源 (紋理，例如) 可能會在共用時遇到效能不佳的情況。 某些硬體上無法共用可鎖定的 rendertargets。
-   跨進程共用資源的參考必須與原始資源具有相同的維度。 當跨進程傳遞控制碼時，請包含維度資訊，如此就能以相同的方式建立參考。
-   共用的跨進程表面不提供同步處理機制。 對共用介面的讀取/寫入變更可能不會在預期的情況反映參考進程的外觀。 若要提供同步處理，請使用事件查詢或鎖定紋理。
-   只有一開始建立共用資源的進程才能將其鎖定 (任何開啟該共用資源參考的進程都無法將其鎖定) 。
-   如果共用資源已鎖定，其他進程就不會進行驗證，以得知資源是否可用。

## <a name="srgb-conversion-before-blending"></a>混合之前的 sRGB 轉換

您現在可以檢查裝置是否可以在框架緩衝區混合之前，將管線資料轉換成 sRGB。 這表示裝置會從 sRGB 轉換轉譯目標值。 若要查看硬體是否支援轉換，請檢查此上限：


```
D3DPMISCCAPS_POSTBLENDSRGBCONVERT
```



此端點會識別在混合之前支援轉換為 sRGB 的硬體。 這項功能對於從桌面視窗管理員 fp16 框架緩衝區的高品質轉譯而言很重要， (DWM) 。

## <a name="stretchrect-improvements"></a>StretchRect 改進

在舊版的 DirectX 中，StretchRect 有許多限制來容納不同的驅動程式 (請參閱 IDirect3DDevice9：： StretchRect) 。 Windows Vista 建基於 Windows 設備磁碟機模型 (WDDM) 。 這個新的驅動程式模型更為穩固，而且可讓驅動程式處理硬體中的特殊情況。

一般而言，唯一的限制是必須以轉譯目標使用方式建立轉譯目標 (D3DUSAGE \_ RENDERTARGET) 。 如果您要執行簡單的複製 (，其中來源和目的地的格式相同，而且沒有子矩形) ，則會提高此限制。

## <a name="texture-creation-in-system-memory"></a>系統記憶體中的材質建立

在使用、配置和刪除系統記憶體時需要更多彈性的應用程式，現在可以從系統記憶體指標建立紋理。 例如，應用程式可以從 GDI 系統記憶體點陣圖指標建立 Direct3D 材質。

您需要做兩件事來建立這類紋理：

-   配置足夠的系統記憶體來保存材質介面。 最小的位元組數目是每圖元的寬度 x 高度 x 位元組。
-   將控制碼參數的指標位址傳遞至 \* IDirect3DDevice9：： CreateTexture 的系統記憶體介面。

以下是 IDirect3DDevice9：： CreateTexture 的函式原型：


```
STDMETHOD(CreateTexture)(THIS_ UINT Width, UINT Height, UINT Levels, 
    DWORD Usage, D3DFORMAT Format, D3DPOOL Pool, IDirect3DTexture9** ppTexture, 
    HANDLE* pSharedHandle)
```



系統記憶體材質有下列限制：

-   材質間距必須等於材質寬度乘以每圖元的位元組數目。
-   使用壓縮格式 (DXT 格式) 時，應用程式會負責配置正確的大小。
-   僅支援具有單一 mipmap 層級的材質。
-   針對集區引數傳遞給 CreateTexture 的值必須是 D3DPOOL \_ SYSTEMMEM。
-   此 API 會將提供的記憶體包裝在材質中。 請勿將此記憶體解除配置，直到完成為止。

 

 
