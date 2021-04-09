---
title: Windows 圖形 API 之間共用的介面
description: 本主題提供在 Windows 圖形 Api （包括 Direct3D 11、Direct2D、DirectWrite、Direct3D 10 和 Direct3D 9Ex）之間使用介面共用的互通性技術總覽。
ms.assetid: 65abf33e-3d15-42ff-99bd-674f24da773e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d889797902c964e603adefc51b25039afca7d46
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/01/2020
ms.locfileid: "103683223"
---
# <a name="surface-sharing-between-windows-graphics-apis"></a>Windows 圖形 API 之間共用的介面

本主題提供在 Windows 圖形 Api （包括 Direct3D 11、Direct2D、DirectWrite、Direct3D 10 和 Direct3D 9Ex）之間使用介面共用的互通性技術總覽。 如果您已經瞭解這些 Api，這份檔可協助您在針對 Windows 7 或 Windows Vista 作業系統設計的應用程式中，使用多個 Api 轉譯成相同的介面。 本主題也提供最佳做法指導方針和其他資源的指標。

> [!Note]  
> 針對 DirectX 11.1 執行時間上的 Direct2D 和 DirectWrite 互通性，您可以使用 [Direct2D 裝置和裝置](/windows/desktop/Direct2D/devices-and-device-contexts) 內容直接轉譯至 Direct3D 11 裝置。

 

本主題包含下列各節。

-   [簡介](#introduction)
-   [API 互通性總覽](#api-interoperability-overview)
-   [互通性案例](#interoperability-scenarios)
    -   [使用 Direct2D 共用 Direct3D 10.1 裝置](#direct3d-101-device-sharing-with-direct2d)
    -   [DXGI 1.1 同步共用的表面](#dxgi-11-synchronized-shared-surfaces)
    -   [Direct3D 9Ex 和 DXGI 型 Api 之間的互通性](#interoperability-between-direct3d-9ex-and-dxgi-based-apis)
-   [結論](#conclusion)

## <a name="introduction"></a>簡介

在本檔中，Windows 圖形 API 互通性是指由不同的 Api 共用相同的呈現介面。 這種互通性可讓應用程式利用多個 Windows 圖形 Api 來建立吸引人的顯示器，並藉由維持與現有 Api 的相容性，讓您輕鬆地遷移至新的技術。

在 Windows 7 (和 Windows Vista SP2 （含 Windows 7 Interop 套件）中，使用 Vista 7IP) ，圖形轉譯 Api 是 Direct3D 11、Direct2D、Direct3D 10.1、Direct3D 10.0、Direct3D 9Ex、Direct3D 9c 及舊版 Direct3D Api，以及 GDI 和 GDI +。 Windows 影像處理元件 (WIC) 和 DirectWrite 是影像處理的相關技術，而 Direct2D 會執行文字轉譯。 以 Direct3D 9c 和 Direct3D 9Ex 為基礎的 DirectX Video 加速 API (DXVA) 用於影片處理。

隨著 Windows 圖形 Api 的發展，Microsoft 致力於確保 Api 之間的互通性。 根據 Direct3D Api 的新開發 Direct3D Api 和較高層級 Api 也會提供支援，讓您在需要時將相容性與舊版 Api 銜接。 為了說明，Direct2D 應用程式可以藉由共用 Direct3D 10.1 裝置，來使用 Direct3D 10.1。 此外，Direct3D 11、Direct2D 和 Direct3D 10.1 Api 都能充分利用 DirectX Graphic Infrastructure (DXGI) 1.1，這會啟用完整支援這些 Api 之間互通性的同步共用表面。 透過從 DXGI 1.1 介面取得 GDI 裝置內容，以透過關聯性來與 GDI 互動的 DXGI 1.1 型 Api。 如需詳細資訊，請參閱 MSDN 上提供的 DXGI 和 GDI 互通性檔。

Direct3D 9Ex 執行時間支援未同步的介面共用。 以 DXVA 為基礎的影片應用程式，可以使用 direct3d 9Ex 和 DXGI 互通性協助程式進行 direct3d 9Ex 型 DXVA 與 Direct3D 11 for compute 著色器的互通性，或者可以與 Direct2D 互動以進行2D 控制項或文字轉譯。 WIC 和 DirectWrite 也會與 GDI、Direct2D 以及其他 Direct3D Api 相互關聯。

Direct3D 10.0、Direct3D 9c 和舊版 Direct3D 執行時間不支援共用的表面。 系統記憶體複本將繼續用於與 GDI 或 DXGI 型 Api 的互通性。

請注意，本檔中的互通性案例指的是轉譯成共用轉譯介面的多個圖形 Api，而不是相同的應用程式視窗。 針對不同的介面，以不同表面為目標的個別 Api 進行同步處理時，會在本檔的討論範圍之外。

## <a name="api-interoperability-overview"></a>API 互通性總覽

您可以根據 API 對 API 案例和對應的互通性功能，來描述 Windows 圖形 Api 的介面共用互通性。 從 Windows 7 開始，開始使用7IP 的 Windows Vista SP2，新的 Api 和相關聯的執行時間包括 Direct2D 和相關技術： Direct3D 11 和 DXGI 1.1。 Windows 7 也改善了 GDI 效能。 Windows Vista SP1 引進了 Direct3D 10.1。 下圖顯示 Api 之間的互通性支援。

![windows 圖形 api 之間的互通性支援圖表](images/surface-sharing-interoperability.png)

在此圖中，箭號會顯示連線 Api 可以存取相同介面的互通性案例。 藍色箭號表示 Windows Vista 中引進的互通性機制。 綠色箭號表示支援新 Api 或增強功能的互通性支援，可協助舊版 Api 與較新的 Api 交互操作。 例如，綠色箭號代表裝置共用、同步處理的共用介面支援、Direct3D 9Ex/DXGI 同步處理協助程式，以及從相容的介面取得 GDI 裝置內容。

## <a name="interoperability-scenarios"></a>互通性案例

從 Windows 7 和 Windows Vista 7IP 開始，Windows 圖形 Api 的主流供應專案支援多個 Api 轉譯成相同的 DXGI 1.1 介面。

**Direct3D 11、Direct3D 10.1、Direct2D-互通性**

Direct3d 11、Direct3D 10.1 和 Direct2D Api (與其相關的 Api （例如 DirectWrite 和 WIC）) 可以使用 Direct3D 10.1 裝置共用或同步處理的共用介面彼此交互操作。

### <a name="direct3d-101-device-sharing-with-direct2d"></a>使用 Direct2D 共用 Direct3D 10.1 裝置

在 Direct2D 與 Direct3D 10.1 之間共用裝置，可讓應用程式使用相同的基礎 Direct3D 裝置物件，以順暢且有效率的方式將這兩個 Api 轉譯至相同的 DXGI 1.1 介面。 Direct2D 可讓您使用現有的 Direct3D 10.1 裝置來呼叫 Direct2D Api，並運用 Direct2D 建置於 Direct3D 10.1 和 DXGI 1.1 執行時間的事實。 下列程式碼片段說明 Direct2D 如何從與裝置相關聯的 DXGI 1.1 介面取得 Direct3D 10.1 裝置呈現目標。 Direct3D 10.1 裝置轉譯目標可在 BeginDraw 和 EndDraw Api 之間執行 Direct2D 繪圖呼叫。


```C++
// Direct3D 10.1 Device and Swapchain creation
HRESULT hr = D3D10CreateDeviceandSwapChain1(
                pAdapter,
                DriverType,
                Software,
                D3D10_CREATE_DEVICE_BGRA_SUPPORT,
                featureLevel,
                D3D10_1_SDK_VERSION,
                pSwapChainDesc,
                &pSwapChain,
                &pDevice
                );

hr = pSwapChain->GetBuffer(
        0,
        __uuidof(IDXGISurface),
        (void **)&pDXGIBackBuffer
        ));

// Direct3D 10.1 API rendering calls
...

hr = D2D1CreateFactory(
        D2D1_FACTORY_TYPE_SINGLE_THREADED,
        &m_spD2DFactory
        ));

pD2DFactory->CreateDxgiSurfaceRenderTarget(
        pDXGIBackBuffer,
        &renderTargetProperties,
        &pD2DBackBufferRenderTarget
        ));
...

pD2DBackBufferRenderTarget->BeginDraw();
//Direct2D API rendering calls
...

pD2DBackBufferRenderTarget->EndDraw();

pSwapChain->Present(0, 0);
```



**備註**

-   相關聯的 Direct3D 10.1 裝置必須支援 BGRA 格式。 該裝置是藉由使用參數 D3D10 \_ 建立 \_ 裝置 \_ BGRA 支援來呼叫 D3D10CreateDevice1 所建立 \_ 。 從 Direct3D 10 功能等級9.1 開始支援 BGRA 格式。
-   應用程式不應建立多個與相同 Direct3D 10.1 裝置相關聯的 ID2D1RenderTargets。
-   為了達到最佳效能，請隨時保留至少一個資源，例如與裝置相關聯的材質或表面。

裝置共用適用于同進程的單一執行緒使用，這兩種轉譯裝置都是由 Direct3D 10.1 和 Direct2D 轉譯 Api 所共用。 已同步處理的共用介面可讓 Direct3D 10.1、Direct2D 和 Direct3D 11 Api 使用多個轉譯裝置的多執行緒、同進程和跨進程使用。

Direct3D 10.1 和 Direct2D 互通性的另一種方法是使用 ID3D1RenderTarget：： CreateSharedBitmap，它會從 IDXGISurface 建立 ID2D1Bitmap 物件。 您可以將 Direct3D 10.1 場景寫入點陣圖，並使用 Direct2D 加以呈現。 如需詳細資訊，請參閱 [ID2D1RenderTarget：： CreateSharedBitmap 方法](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap)。

### <a name="direct2d-software-rasterization"></a>Direct2D 軟體點陣化

使用 Direct2D software 轉譯器時，不支援使用 Direct3D 10.1 進行裝置共用，例如，藉由指定 D2D1 轉譯 \_ \_ 目標使用方式， \_ \_ \_ \_ 在 \_ \_ \_ 建立 Direct2D 轉譯目標時，于 D2D1 轉譯目標使用方式中強制軟體轉譯。

Direct2D 可以使用 WARP10 軟體轉譯器與 Direct3D 10 或 Direct3D 11 共用裝置，但效能會大幅降低。

### <a name="dxgi-11-synchronized-shared-surfaces"></a>DXGI 1.1 同步共用的表面

Direct3D 11、Direct3D 10.1 和 Direct2D Api 全都使用 DXGI 1.1，其提供的功能可將讀取和寫入相同的視訊記憶體介面， (DXGISurface1 由兩個或更多 Direct3D 裝置進行) 。 使用同步共用表面的轉譯裝置可以是 Direct3D 10.1 或 Direct3D 11 裝置，每個裝置都在相同的進程或跨進程中執行。

應用程式可以使用已同步處理的共用介面，從 Direct2D 轉譯目標物件取得 Direct3D 10.1 裝置，以便在任何 DXGI 1.1 型裝置（例如 Direct3D 11 和 Direct3D 10.1）或 Direct3D 11 和 Direct2D 之間互通。

在 Direct3D 10.1 和更新版本的 Api 中，若要使用 DXGI 1.1，請確定已使用 dxgi 1.1 factory 物件列舉的 DXGI 1.1 介面卡物件來建立 Direct3D 裝置。 呼叫 CreateDXGIFactory1 來建立 IDXGIFactory1 物件，並呼叫 EnumAdapters1 來列舉 IDXGIAdapter1 物件。 IDXGIAdapter1 物件必須傳入作為 D3D10CreateDevice 或 D3D10CreateDeviceAndSwapChain 呼叫的一部分。 如需有關 DXGI 1.1 Api 的詳細資訊，請參閱 [dxgi 的程式設計指南](https://msdn.microsoft.com/library/ee418147(VS.85).aspx)。

### <a name="apis"></a>API

**D3D10 \_ 資源的 \_ 其他 \_ 共用 \_ KEYEDMUTEX**  
建立已同步處理的共用資源時， \_ 請 \_ \_ \_ 在 D3D10 \_ 資源的 \_ 其他旗標中設定 D3D10 資源的其他共用 KEYEDMUTEX \_ 。  


```C++
typedef enum D3D10_RESOURCE_MISC_FLAG {
    D3D10_RESOURCE_MISC_GENERATE_MIPS      = 0x1L,
    D3D10_RESOURCE_MISC_SHARED             = 0x2L,
    D3D10_RESOURCE_MISC_TEXTURECUBE        = 0x4L,
    D3D10_RESOURCE_MISC_SHARED_KEYEDMUTEX  = 0x10L,
    D3D10_RESOURCE_MISC_GDI_COMPATIBLE     = 0x20L,
}   D3D10_RESOURCE_MISC_FLAG;
```



**D3D10 \_ 資源的 \_ 其他 \_ 共用 \_ KEYEDMUTEX**  
啟用使用 IDXGIKeyedMutex：： AcquireSync 和 ReleaseSync Api 來同步處理所建立的資源。 下列資源建立 Direct3D 10.1 Api 全都採用 D3D10 \_ 資源 \_ 其他 \_ 旗標參數，以支援新的旗標。  

-   ID3D10Device1::CreateTexture1D
-   ID3D10Device1::CreateTexture2D
-   ID3D10Device1::CreateTexture3D
-   ID3D10Device1::CreateBuffer

  
如果使用 D3D10 資源的「其他共用 KEYEDMUTEX 旗標集合來呼叫任何列出的函 \_ \_ \_ \_ 式，則可以針對 IDXGIKeyedMutex 介面查詢傳回的介面，該介面會執行 AcquireSync 和 ReleaseSync api 來同步處理介面的存取。 建立介面的裝置，以及使用 OpenSharedResource) 開啟介面 (的任何其他裝置，都必須在介面的任何轉譯命令之前呼叫 IDXGIKeyedMutex：： AcquireSync，並在完成轉譯時呼叫 IDXGIKeyedMutex：： ReleaseSync。  
變形和 REF 裝置不支援共用資源。 嘗試在彎曲或 REF 裝置上使用此旗標建立資源，會導致 create 方法傳回 E \_ OUTOFMEMORY 錯誤碼。  
**IDXGIKEYEDMUTEX 介面**  
在 DXGI 1.1 （IDXGIKeyedMutex）中的新介面代表索引 mutex，可讓您獨佔存取多個裝置使用的共用資源。 如需有關此介面和其兩種方法（AcquireSync 和 ReleaseSync）的參考檔，請參閱 [IDXGIKeyedMutex](https://msdn.microsoft.com/library/ee421920(VS.85).aspx)。  
</dl>

### <a name="sample-synchronized-surface-sharing-between-two-direct3d-101-devices"></a>範例：兩個 Direct3D 10.1 裝置之間的同步表面共用

下列範例說明如何在兩個 Direct3D 10.1 裝置之間共用一個表面。 同步處理的共用介面是由 Direct3D 10.1 裝置所建立。


```C++
// Create Sync Shared Surface using Direct3D10.1 Device 1.
D3D10_TEXTURE2D_DESC desc;
ZeroMemory( &desc, sizeof(desc) );
desc.Width = width;
desc.Height = height;
desc.MipLevels = 1;
desc.ArraySize = 1;
// must match swapchain format in order to CopySubresourceRegion.
desc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
desc.SampleDesc.Count = 1;
desc.Usage = D3D10_USAGE_DEFAULT;
// creates 2D texture as a Synchronized Shared Surface.
desc.MiscFlags = D3D10_RESOURCE_MISC_SHARED_KEYEDMUTEX;
desc.BindFlags = D3D10_BIND_RENDER_TARGET | D3D10_BIND_SHADER_RESOURCE;
ID3D10Texture2D* g_pShared = NULL;
g_pd3dDevice1->CreateTexture2D( &desc, NULL, &g_pShared );

// QI IDXGIResource interface to synchronized shared surface.
IDXGIResource* pDXGIResource = NULL;
g_pShared->QueryInterface(__uuidof(IDXGIResource), (LPVOID*) &pDXGIResource);

// obtain handle to IDXGIResource object.
pDXGIResource->GetSharedHandle(&g_hsharedHandle);
pDXGIResource->Release();
if ( !g_hsharedHandle )
    return E_FAIL;

// QI IDXGIKeyedMutex interface of synchronized shared surface's resource handle.
hr = g_pShared->QueryInterface( __uuidof(IDXGIKeyedMutex),
    (LPVOID*)&g_pDXGIKeyedMutex_dev1 );
If ( FAILED( hr ) || ( g_pDXGIKeyedMutex_dev1 == NULL ) )
    return E_FAIL;
```



相同的 Direct3D 10.1 裝置可以藉由呼叫 AcquireSync 來取得已同步處理的共用介面，然後藉由呼叫 ReleaseSync 來釋出其他裝置呈現的介面。 當您未與任何其他 Direct3D 裝置共用同步處理的共用介面時，建立者可以取得和釋放已同步處理的共用介面 (，藉由使用相同的索引鍵值取得和釋放) 開始和結束轉譯。


```C++
// Obtain handle to Sync Shared Surface created by Direct3D10.1 Device 1.
hr = g_pd3dDevice2->OpenSharedResource( g_hsharedHandle,__uuidof(ID3D10Texture2D),
                                        (LPVOID*) &g_pdev2Shared);
if (FAILED (hr))
    return hr;
hr = g_pdev2Shared->QueryInterface( __uuidof(IDXGIKeyedMutex),
                                    (LPVOID*) &g_pDXGIKeyedMutex_dev2);
if( FAILED( hr ) || ( g_pDXGIKeyedMutex_dev2 == NULL ) )
    return E_FAIL;

// Rendering onto Sync Shared Surface from D3D10.1 Device 1 using D3D10.1 Device 2.
UINT acqKey = 1;
UINT relKey = 0;
DWORD timeOut = 5;
DWORD result = g_pDXGIKeyedMutex_dev2->AcquireSync(acqKey, timeOut);
if ( result == WAIT_OBJECT_0 )
    // Rendering calls using Device 2.
else
    // Handle unable to acquire shared surface error.
result = g_pDXGIKeyedMutex_dev2->ReleaseSync(relKey));
if (result == WAIT_OBJECT_0)
    return S_OK;
```



第二個 Direct3D 10.1 裝置可以藉由呼叫 AcquireSync 來取得已同步處理的共用介面，然後藉由呼叫 ReleaseSync 來釋放第一個裝置轉譯的介面。 請注意，裝置2可以使用與裝置 1 ReleaseSync 呼叫中所指定的相同金鑰值，來取得已同步處理的共用介面。


```C++
// Rendering onto Sync Shared Surface from D3D10.1 Device 1 using D3D10.1 Device 1.
UINT acqKey = 0;
UINT relKey = 1;
DWORD timeOut = 5;
DWORD result = g_pDXGIKeyedMutex_dev1->AcquireSync(acqKey, timeOut);
if (result == WAIT_OBJECT_0)
    // Rendering calls using Device 1.
else
    // Handle unable to acquire shared surface error.
result = g_pDXGIKeyedMutex_dev1->ReleaseSync(relKey));
if ( result == WAIT_OBJECT_0 )
    return S_OK;
```



共用相同介面的其他裝置可以使用額外的按鍵來取得和釋放介面，如下列呼叫所示。


```C++
// Within Device 1's process/thread:
// Rendering onto Sync Shared Surface from D3D10.1 Device 1 using D3D10.1 Device 1
result = g_pDXGIKeyedMutex_dev1->AcquireSync(0, timeOut);
// Rendering calls using Device 1
...
result = g_pDXGIKeyedMutex_dev1->ReleaseSync(1);
...
////////////////////////////////////////////////////////////////////////////
// Within Device 2's process/thread:
// Rendering onto Sync Shared Surface from D3D10.1 Device 1 using D3D10.1 Device 2
result = g_pDXGIKeyedMutex_dev2->AcquireSync(1, timeOut);
// Rendering calls using Device 2
...
result = g_pDXGIKeyedMutex_dev1->ReleaseSync(2);

////////////////////////////////////////////////////////////////////////////
// Within Device 3's process/thread:
// Rendering onto Sync Shared Surface from D3D10.1 Device 1 using D3D10.1 Device 3
result = g_pDXGIKeyedMutex_dev1->AcquireSync(2, timeOut);
// Rendering calls using Device 3
...
result = g_pDXGIKeyedMutex_dev1->ReleaseSync(0);
...
```



請注意，真實世界的應用程式可能一律會轉譯成中繼表面，然後將它複製到共用表面，以防止在另一部共用介面的裝置上等候任何一個裝置。

### <a name="using-synchronized-shared-surfaces-with-direct2d-and-direct3d-11"></a>搭配 Direct2D 和 Direct3D 11 使用同步共用的表面

同樣地，針對 Direct3D 11 和 Direct3D 10.1 Api 之間的共用，您可以從 API 裝置建立已同步處理的共用介面，並與其他 API 裝置共用 (s) 、進出進程。

使用 Direct2D 的應用程式可以共用 Direct3D 10.1 裝置，並使用同步處理的共用介面與 Direct3D 11 或其他 Direct3D 10.1 裝置交互操作，不論它們屬於相同的進程或不同的進程。 不過，對於單一進程、單一線程應用程式，裝置共用是 Direct2D 與 Direct3D 10 或 Direct3D 11 之間最高效能且有效率的互通性方法。

### <a name="software-rasterizer"></a>軟體轉譯器

當應用程式使用 Direct3D 或 Direct2D software rasterizers （包括參考轉譯器和變形）（而不是使用圖形硬體加速）時，不支援同步共用的表面。

### <a name="interoperability-between-direct3d-9ex-and-dxgi-based-apis"></a>Direct3D 9Ex 和 DXGI 型 Api 之間的互通性

Direct3D 9Ex Api 包含介面共用的概念，可讓其他 Api 從共用介面讀取。 為了共用對 Direct3D 9Ex 共用介面的讀取和寫入，您必須將手動同步處理新增至應用程式本身。

### <a name="direct3d-9ex-shared-surfaces-plus-manual-synchronization-helper"></a>Direct3D 9Ex 共用的表面加上手動同步處理協助程式

Direct3D 9Ex 和 Direct3D 10 或11互通性中最基本的工作，是將第一個裝置的單一介面從第一個裝置 (裝置 A) 傳送至第二個 (裝置 B) 如此一來，當裝置 B 取得介面上的控制碼時，即保證裝置 A 的轉譯已完成。 因此，裝置 B 可以使用此介面，而不需要擔心。 這非常類似于傳統生產者-取用者的問題，而此討論會以這種方式為問題建模。 第一個使用介面的裝置，然後會讓出它是生產者 (裝置 A) ，而最初等待的裝置是取用者 (裝置 B) 。 任何真實世界的應用程式都比這個更複雜，而且會將多個生產者-取用者建立區塊串連在一起，以建立所需的功能。

生產者-取用者組建區塊會使用表面的佇列在協助程式中實作為。 介面會由取用者排入佇列，並由取用者清除佇列。 此協助程式引進三個 COM 介面： ISurfaceQueue、ISurfaceProducer 和 ISurfaceConsumer。

### <a name="high-level-overview-of-helper"></a>Helper 的 High-Level 總覽

ISurfaceQueue 物件是使用共用表面的建立區塊。 它是以初始化的 Direct3D 裝置所建立，並提供描述來建立固定的共用表面數目。 佇列物件會管理資源的建立和開啟程式碼。 曲面的數目和類型是固定的;一旦建立介面之後，應用程式就無法新增或移除這些表面。

ISurfaceQueue 物件的每個實例都會提供一種單向街道，可用來從產生的裝置傳送表面到取用的裝置。 您可以使用多個這種單向街道，在特定應用程式的裝置之間啟用 surface 共用案例。

**建立/物件存留期**  
有兩種方式可以建立佇列物件：透過 CreateSurfaceQueue，或透過 ISurfaceQueue 的複製方法。 因為介面是 COM 物件，所以會套用標準 COM 存留期管理。  
**生產者/取用者模型**  
排入佇列 () ：生產者會呼叫此函式來表示它是使用介面完成，現在可供其他裝置使用。 從這個函式傳回時，生產者裝置不再有介面的許可權，而且不安全地繼續使用。  
清除佇列 () ：取用裝置會呼叫此函式以取得共用的介面。 API 可保證任何已清除佇列的表面都可供使用。  
**中繼資料**  
API 支援將中繼資料與共享的表面產生關聯。  
排入佇列 () 可選擇指定將傳遞給取用裝置的其他中繼資料。 中繼資料必須小於建立時已知的最大值。  
清除佇列 () 可以選擇性地傳遞緩衝區和緩衝區大小的指標。 佇列會以對應的排入佇列呼叫的中繼資料填入緩衝區。  
**複製**  
每個 ISurfaceQueue 物件都會解決單向同步處理。 我們假設大部分的應用程式使用此 API 都將使用封閉式系統。 有兩個裝置來回傳送表面的最簡單關閉系統需要兩個佇列。 ISurfaceQueue 物件具有複製 () 方法，可讓您建立多個屬於相同較大管線的佇列。  
複製會從現有的 ISurfaceQueue 物件建立新的物件，並共用它們之間所有已開啟的資源。 產生的物件與來源佇列有完全相同的表面。 複製的佇列可以有不同的中繼資料大小。  
**表面**  
ISurfaceQueue 會負責建立及管理其表面。 將任意表面排入佇列是不正確。 此外，介面應該只有一個使用中的「擁有者」。 它應該是在特定的佇列上，或是由特定裝置使用。 在多個佇列上，或讓裝置在排入佇列之後仍繼續使用介面，是不正確。  
</dl>

### <a name="api-details"></a>API 詳細資料

### <a name="isurfacequeue"></a>IsurfaceQueue

佇列負責建立和維護共用資源。 它也提供使用 Clone 來連鎖多個佇列的功能。 佇列具有開啟產生裝置和取用裝置的方法。 每次只能開啟其中一個。

佇列會公開下列 Api：



|                             |                                                                                  |
|-----------------------------|----------------------------------------------------------------------------------|
| CreateSurfaceQueue          | 建立 ISurfaceQueue 物件 ("root" 佇列) 。                              |
| ISurfaceQueue::OpenConsumer | 傳回取用裝置清除佇列的介面。                        |
| ISurfaceQueue::OpenProducer | 傳回產生裝置排入佇列的介面。                        |
| ISurfaceQueue：： Clone        | 建立 ISurfaceQueue 物件，該物件會與根佇列物件共用表面。 |



 

**CreateSurfaceQueue**  


```C++
typedef struct SURFACE_QUEUE_DESC {
  UINT            Width;
  UINT            Height;
  DXGI_FORMAT     Format;
  UINT            NumSurfaces;
  UINT            MetaDataSize;
  DWORD           Flags;
} SURFACE_QUEUE_DESC;
```



**成員**  

**寬度**、 **高度**  ：共用表面的維度。 所有共用的表面都必須有相同的維度。  
**格式** 共用表面的格式。 所有共用的表面都必須具有相同的格式。 有效的格式取決於將使用的裝置，因為不同的裝置配對可以共用不同的格式類型。  
**NumSurfaces**  屬於佇列一部分的表面數目。 這是固定的數位。  
 **MetaDataSize**  元資料緩衝區的大小上限。  
**旗標**  用來控制佇列行為的旗標。 請參閱＜備註＞。  



```C++
HRESULT CreateSurfaceQueue(
  [in]   SURFACE_QUEUE_DESC *pDesc,
  [in]   IUnknown *pDevice,
  [out]  IDXGIXSurfaceQueue **ppQueue
);
```



**參數**

 *pDesc* \[在 \]  要建立之共用介面佇列的描述中。  

 *pDevice* \[\]應該用來建立共用表面的裝置。 這是 Windows Vista 中的一項功能，因此是明確的參數。 若為 Direct3D 9 與 Direct3D 10 之間共用的介面，則必須使用 Direct3D 9 來建立這些表面。  

 *ppQueue* \[傳回 \]  時，包含 ISurfaceQueue 物件的指標。  


**傳回值**

如果 *pDevice* 無法共用資源，此函式會傳回 DXGI \_ 錯誤 \_ 不正確 \_ 呼叫。 此函數會建立資源。 如果失敗，則會傳回錯誤。 如果成功，則會傳回 S \_ OK。

**備註**

建立佇列物件也會建立所有的表面。 所有表面都會假設為2D 轉譯目標，並會使用 D3D10 系結轉譯 \_ \_ \_ 目標和 D3D10 系結 \_ \_ 著色器 \_ 資源旗標設定 (或不同執行時間) 的相等旗標來建立。

開發人員可以指定旗標，以指出多個執行緒是否會存取佇列。 如果未將旗標設定 (**旗標** = = 0) ，則佇列將會由多個執行緒使用。 開發人員可以指定單一執行緒存取，以關閉同步處理常式代碼，並針對這些案例提供效能改進。 每個複製的佇列都有自己的旗標，因此系統中的不同佇列可能會有不同的同步控制。

 **開啟生產者**  


```C++
HRESULT OpenProducer(
  [in]   IUnknown *pDevice,
  [out]  IDXGIXSurfaceProducer **ppProducer
);
```



**參數**  

*pDevice* \[在\]  

將顯示在介面佇列上的生產者裝置。 

*ppProducer* \[out 會將 \] 物件傳回給生產者介面。  


**傳回值**

如果裝置無法共用介面，會傳回 DXGI \_ 錯誤 \_ 不正確 \_ 呼叫。

**開啟取用者**  


```C++
HRESULT OpenConsumer(
  [in]   IUnknown *pDevice,
  [out]  IDXGIXSurfaceConsumer **ppConsumer
);
```



**參數**  
 *pDevice* \[在\]  
 清除介面佇列表面的取用者裝置。 
 *ppConsumer* \[out 會將 \]  物件傳回到取用者介面。  


**傳回值**

如果裝置無法共用介面，會傳回 DXGI \_ 錯誤 \_ 不正確 \_ 呼叫。

**備註**

此函式會開啟輸入裝置之佇列中的所有表面，並加以快取。 後續的清除佇列呼叫會直接移至快取，而不需要每次重新開啟介面。



### <a name="cloning-an-idxgixsurfacequeue"></a>複製識別碼XGIXSurfaceQueue




```C++
typedef struct SHARED_SURFACE_QUEUE_CLONE_DESC {
  UINT         MetaDataSize;
  DWORD        Flags;
} SHARED_SURFACE_QUEUE_CLONE_DESC;
```



**成員** **MetaDataSize** 和 **旗標** 具有與 CreateSurfaceQueue 相同的行為。  



```C++
HRESULT Clone(
  [in]   SHARED_SURFACE_QUEUE_CLONE_DESC *pDesc,
  [out]  IDXGIXSurfaceQueue **ppQueue
);
```



**參數**

*pDesc* \[在 \] 提供要建立之複製物件描述的結構中。 此參數應初始化。  
*ppQueue* \[out 會傳回 \] 初始化的物件。  
</dl>

**備註**

您可以從任何現有的佇列物件進行複製（即使它不是根目錄）。  
</dl>

### <a name="idxgixsurfaceconsumer"></a>IDXGIXSurfaceConsumer

<dl>


```C++
HRESULT Dequeue(
  [in]      REFIID    id,
  [out]     void      **ppSurface,
  [in,out]  void      *pBuffer,
  [in,out]  UINT      *pBufferSize,
  [in]      DWORD     dwTimeout
);
```



**參數**  
 \[ 中的識別碼\]  
使用中裝置之2D 介面的 REFIID。  

-   若為 IDirect3DDevice9，REFIID 應該是 \_ \_ Uuidof (IDirect3DTexture9) 。
-   若為 ID3D10Device，REFIID 應該是 \_ \_ Uuidof (ID3D10Texture2D) 。
-   若為 ID3D11Device，REFIID 應該是 \_ \_ Uuidof (ID3D11Texture2D) 。

*ppSurface* \[out 會將 \] 指標傳回至介面。  
*pBuffer* \[在中，out \] 選擇性的參數，如果不是 **Null**，則在傳回時，會包含在對應的佇列呼叫上傳入的中繼資料。  
*pBufferSize* \[在中， \] *pBuffer* 的大小（以位元組為單位）。 傳回 *pBuffer* 中傳回的位元組數目。 如果排入佇列的呼叫未提供中繼資料，則 *pBuffer* 會設定為0。  
*dwTimeout* \[中的 \] 指定超時值。 如需詳細資訊，請參閱備註。  
</dl>

**傳回值**

\_如果指定了超時值，且函式未在超時值之前傳回，此函式可能會傳回等候時間。 請參閱＜備註＞。 如果沒有可用的介面，則函式會傳回，並將 *ppSurface* 設定為 **Null**， *pBufferSize* 設定為0，且傳回值為 0X80070120 (WIN32 \_ 到 \_ HRESULT (等候 \_ 超時) ) 。  
</dl>

**備註**

如果佇列是空的，此 API 就會封鎖。 *DwTimeout* 參數的運作方式與 Windows 同步處理 api 相同，例如 WaitForSingleObject。 若為非封鎖的行為，請使用 timeout 0。  
</dl>

### <a name="isurfaceproducer"></a>ISurfaceProducer

此介面提供兩種可讓應用程式排入佇列的方法。 將介面排入佇列之後，介面指標就不再有效，而且不安全地使用。 應用程式應該以指標執行的唯一動作是釋放它。



|                           |                                                                                                                                                       |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| ISurfaceProducer：：排入佇列 | 將至佇列物件的介面。 此呼叫完成之後，就會使用介面來完成產生者，並為其他裝置準備好表面。 |
| ISurfaceProducer：： Flush   | 如果應用程式應該有非封鎖的行為，則會使用。 如需詳細資訊，請參閱備註。                                                                  |



 

**排入佇列**  


```C++
HRESULT Enqueue(
  [in]  IUnknown *pSurface,
  [in]  void *pBuffer,
  [in]  UINT BufferSize,
  [in]  DWORD Flags
);
```



**參數**  
*pSurface* \[在\]  
產生裝置的表面，需要排入佇列。 此介面必須是來自相同佇列網路的佇列表面。 *pBuffer* \[\]用於傳入中繼資料的選擇性參數。 它應該指向將會傳遞至清除佇列呼叫的資料。  
*BufferSize* \[以 \] 位元組為單位的 *pBuffer* 大小。  
*旗標* \[在 \] 控制此函數行為的選擇性參數中。 唯一的旗標是介面佇列旗標不會 \_ \_ \_ \_ \_ 等候。 請參閱 Flush 的備註。 如果未傳遞旗標 (*旗標* = = 0) ，則會使用預設的封鎖行為。  
</dl>

**傳回值**

\_ \_ \_ \_ 如果 \_ 使用介面佇列 \_ 旗標 \_ \_ 不等候旗標 \_ ，則此函式會傳回 DXGI 錯誤仍在繪圖中。  
</dl>

**備註**

-   此函式會將介面放在佇列上。 如果應用程式未指定 SURFACE \_ QUEUE \_ 旗標 \_ ，則此函 \_ 式會 \_ 封鎖並進行 GPU CPU 同步處理，以確保已排入佇列之介面上的所有轉譯都已完成。 如果此函式成功，則會有介面可供清除佇列使用。 如果您想要非封鎖的行為，請使用「請勿 \_ \_ 等候」旗標。 如需詳細資訊，請參閱 Flush () 。
-   根據 COM 參考計數規則，清除佇列所傳回的介面會 AddRef () 因此應用程式不需要這麼做。 呼叫排入佇列之後，應用程式必須釋放介面，因為它們不再使用它。

**清除**  


```C++
HRESULT Flush(
  [in]  DWORD Flags,
  [out] UINT *nSurfaces
);
```



**參數**  
*Flags* \[in\]  
唯一的旗標是介面佇列旗標不會 \_ \_ \_ \_ \_ 等候。 請參閱＜備註＞。 *nSurfaces* \[out \] 會傳回仍在暫止且未排清的表面數目。  
</dl>

**傳回值**

\_ \_ \_ \_ 如果 \_ 使用介面佇列 \_ 旗標 \_ \_ 不等候 \_ 旗標，則此函式會傳回 DXGI 錯誤仍在繪圖中。 如果成功排清任何介面，則此函式會傳回 S \_ OK。 只有未排清任何介面時，此函式才會傳回 DXGI \_ 錯誤 \_ \_ \_ 。 然後，傳回值和 *nSurfaces* 會向應用程式指出已完成的工作，以及是否有任何工作需要進行。  
</dl>

**備註**

只有在先前對排入佇列的呼叫使用「請勿等候」旗標，否則排清才有意義 \_ \_ ; 否則，它將不會有任何作用。 如果使用「請勿等候」旗標來呼叫排入佇列，則會立即傳回加入 \_ \_ 佇列，且不保證 GPU CPU 同步處理。 介面仍會被視為已排入佇列、產生的裝置無法繼續使用，但無法供清除佇列使用。 為了嘗試認可要清除佇列的介面，必須呼叫 Flush。 排清會嘗試認可目前排入佇列的所有表面。 如果未將旗標傳遞至 Flush，它會封鎖並清除整個佇列，使其中的所有表面都能清除佇列。 如果使用「 \_ 不 \_ 等候」旗標，則佇列會檢查介面，查看是否有任何這些介面就緒; 此步驟未封鎖。 已完成 GPU CPU 同步處理的表面，將可供取用者裝置使用。 仍在擱置中的表面不會受到影響。 函數會傳回仍需要排清的表面數目。

> [!Note]  
> Flush 不會中斷佇列的語法。 API 可保證先排入佇列的介面會在稍後排入佇列的介面之前認可，而不論何時發生 GPU CPU 同步處理。

 

  
</dl>

### <a name="direct3d-9ex-and-dxgi-interop-helper-how-to-use"></a>Direct3D 9Ex 和 DXGI Interop Helper：如何使用

我們預期大部分的使用案例都牽涉到兩個裝置共用許多表面。 因為這也是最簡單的案例，這份檔會詳細說明如何使用 Api 來達成此目標、討論非封鎖的變化，並以有關為三部裝置初始化的簡短章節結尾。

### <a name="two-devices"></a>兩部裝置

使用此 helper 的範例應用程式可以搭配使用 Direct3D 9Ex 和 Direct3D 11。 應用程式可以處理這兩個裝置的內容，並使用 Direct3D 9 呈現內容。 處理可能表示轉譯內容、解碼影片、執行計算著色器等等。 在每個框架中，應用程式會先使用 Direct3D 11 處理，然後使用 Direct3D 9 處理，最後再以 Direct3D 9 呈現。 此外，使用 Direct3D 11 的處理會產生一些中繼資料，而 Direct3D 9 所存在的中繼資料將需要使用。 本節涵蓋三個對應至此順序的元件中的協助程式使用方式：初始化、主要迴圈和清除。

**初始 化**  
初始化牽涉到下列步驟：  

1.  初始化這兩個裝置。
2.  建立根佇列： m \_ 11to9Queue。
3.  從根佇列複製： m \_ 9to11Queue。
4.  在兩個佇列上呼叫 OpenProducer/OpenConsumer。

佇列名稱會使用數位9和11來指出哪個 API 是生產者，而後者是取用者： **m \_ ***生產者*** 至取用 ***者*** 佇列**。 因此，m \_ 11to9Queue 會指出 direct3d 11 裝置會產生 direct3d 9 裝置所用的表面所使用的佇列。 同樣地，m \_ 9to11Queue 表示一種佇列，而 direct3d 9 會產生 direct3d 11 所耗用的表面。  
根佇列一開始是完整的，且所有複製的佇列一開始都是空的。 這應該不會造成應用程式的問題，但將和清除的第一個週期和中繼資料的可用性除外。 如果清除佇列要求中繼資料，但未設定任何 (可能是因為一開始沒有任何專案，或排入佇列未設定任何) ，所以清除佇列看到未收到任何中繼資料。  

1.  **初始化這兩個裝置。**  
    ```C++
    m_pD3D9Device = InitializeD3D9ExDevice();
    m_pD3D11Device = InitializeD3D11Device();
    ```

    

2.  **建立根佇列。**  
    此步驟也會建立表面。 大小和格式限制等同于建立任何共用資源。 元資料緩衝區的大小是在建立時固定的，在此情況下，我們只會傳遞 UINT。  
    您必須使用固定的介面數目來建立佇列。 效能將視案例而異。 擁有多個表面可增加裝置忙碌的機會。 例如，如果只有一個介面，則這兩個裝置之間將不會有平行處理。 另一方面，增加介面數量會增加記憶體使用量，這可能會降低效能。 此範例使用兩個表面。  
    ```C++
    SURFACE_QUEUE_DESC Desc;
    Desc.Width        = 640;
    Desc.Height       = 480;
    Desc.Format       = DXGI_FORMAT_R16G16B16A16_FLOAT;
    Desc.NumSurfaces  = 2;
    Desc.MetaDataSize = sizeof(UINT);
    Desc.Flags        = 0;

    CreateSurfaceQueue(&Desc, m_pD3D9Device, &m_11to9Queue);
    ```

    

3.  **複製根佇列。**  
    每個複製的佇列都必須使用相同的表面，但可以有不同的元資料緩衝區大小和不同的旗標。 在此情況下，沒有從 Direct3D 9 到 Direct3D 11 的中繼資料。  
    ```C++
    SURFACE_QUEUE_CLONE_DESC Desc;
    Desc.MetaDataSize = 0;
    Desc.Flags        = 0;

    m_11to9Queue->Clone(&Desc, &m_9to11Queue);
    ```

    

4.  **開啟生產者和取用者裝置。**  
    應用程式必須在呼叫排入佇列和清除佇列之前執行此步驟。 開啟生產者和取用者會傳回包含排入佇列/清除佇列 Api 的介面。  
    ```C++
    // Open for m_p9to11Queue.
    m_p9to11Queue->OpenProducer(m_pD3D9Device, &m_pD3D9Producer);
    m_p9to11Queue->OpenConsumer(m_pD3D11Device, &m_pD3D11Consumer);

    // Open for m_p11to9Queue.
    m_p11to9Queue->OpenProducer(m_pD3D11Device, &m_pD3D11Producer);
    m_p11to9Queue->OpenConsumer(m_pD3D9Device, &m_pD3D9Consumer);
    ```

    

**Main 迴圈**  
佇列的使用方式是在傳統生產者/取用者問題之後進行模型化。 請從每個裝置的觀點來思考這一點。 每個裝置都必須執行下列步驟：清除佇列以從其取用佇列中取得介面、在介面上處理，然後將其加入至其產生佇列。 針對 Direct3D 11 裝置，Direct3D 9 的使用方式幾乎完全相同。  


```C++
// Direct3D 9 Device.
IDirect3DTexture9* pTexture9 = NULL;
REFIID             surfaceID9 = _uuidof(IDirect3DTexture9);
UINT               metaData;
UINT               metaDataSize;
while (!done)
{
    // Dequeue surface.
    m_pD3D9Consumer->Dequeue(surfaceID9, (void**)&pSurface9,
                             &metaData, &metaDataSize, INFINITE);

    // Process the surface.
    ProcessD3D9(pSurface9);

    // Present the surface using the meta data.
    PresentD3D9(pSurface9, metaData, metaDataSize);

    // Enqueue surface.
    m_pD3D9Producer->Enqueue(pSurface9, NULL, 0, 0);
}
```



**清除**  
此步驟非常簡單。 除了清除 Direct3D Api 的一般步驟之外，應用程式也必須釋放傳回的 COM 介面。  


```C++
m_pD3D9Producer->Release();
m_pD3D9Consumer->Release();
m_pD3D11Producer->Release();
m_pD3D11Consumer->Release();
m_p9to11Queue->Release();
m_p11to9Queue->Release();
```



</dl>

### <a name="non-blocking-use"></a>非封鎖使用

上述範例適用于多執行緒使用案例，其中每個裝置都有自己的執行緒。 此範例會使用 Api 的封鎖版本：無限的超時時間，而且沒有任何要排入佇列的旗標。 如果您想要以非封鎖方式使用協助程式，則只需要進行一些變更。 本節顯示在一個執行緒上，對這兩個裝置的非封鎖使用。

**初始 化**  
除了旗標以外，初始化也相同。 因為應用程式是單一執行緒，所以請使用該旗標來建立。 這會關閉部分同步處理常式代碼，這可能會改善效能。  


```C++
SURFACE_QUEUE_DESC Desc;
Desc.Width        = 640;
Desc.Height       = 480;
Desc.Format       = DXGI_FORMAT_R16G16B16A16_FLOAT;
Desc.NumSurfaces  = 2;
Desc.MetaDataSize = sizeof(UINT);
Desc.Flags        = SURFACE_QUEUE_FLAG_SINGLE_THREADED;

CreateSurfaceQueue(&Desc, m_pD3D9Device, &m_11to9Queue);
```




```C++
SURFACE_QUEUE_CLONE_DESC Desc;
Desc.MetaDataSize = 0;
Desc.Flags        = SURFACE_QUEUE_FLAG_SINGLE_THREADED;

m_11to9Queue->Clone(&Desc, &m_9to11Queue);
```



開啟生產者和取用者裝置與封鎖範例中的相同。  
**使用佇列**  
有許多方式可以非封鎖的方式使用佇列的各種效能特性。 下列範例很簡單，但由於過度旋轉和輪詢而效能不佳。 儘管有這些問題，此範例也會示範如何使用 helper。 方法是不斷地坐在迴圈和清除佇列、處理、排入佇列和排清。 如果有任何步驟因為無法使用資源而失敗，應用程式只會再次嘗試下一個迴圈。  


```C++
// Direct3D 11 Device.
ID3D11Texture2D* pSurface11 = NULL;
REFIID           surfaceID11 = __uuidof(ID3D11Texture2D);
UINT             metaData;
while (!done)
{
    //
    // D3D11 Portion.
    //

    // Dequeue surface.
    hr = m_pD3D11Consumer->Dequeue(surfaceID11,
                                   (void**)&pSurface11,
                                   NULL, 0, 0);
    // Only continue if we got a surface.
    if (SUCCEEDED(hr))
    {
        // Process the surface and return some meta data.
        ProcessD3D11(pSurface11, &metaData);

        // Enqueue surface.
        m_pD3D11Producer->Enqueue(pSurface11, &metaData,
                                  sizeof(UINT),
                                  SURFACE_QUEUE_FLAG_DO_NOT_WAIT);
    }
    // Flush the queue to check if any surfaces completed.
    m_pD3D11Producer->Flush(NULL,SURFACE_QUEUE_FLAG_DO_NOT_WAIT);

    //
    // Do the same with the Direct3D 9 Device.
    //

    // Dequeue surface.
    hr = m_pD3D9Consumer->Dequeue(surfaceID9,
                                  (void**)&pSurface9,
                                  &metaData,
                                  &metaDataSize, 0);
    // Only continue if we got a surface.
    if (SUCCEEDED(hr)))
    {
        // Process the surface.
        ProcessD3D9(pSurface9);

        // Present the surface using the meta data.
        PresentD3D9(pSurface9, metaData, metaDataSize);

        // Enqueue surface.
        m_pD3D9Producer->Enqueue(pSurface9, NULL, 0,
                                 SURFACE_QUEUE_FLAG_DO_NOT_WAIT);
    }
    // Flush the queue to check if any surfaces completed.
    m_pD3D9Producer->Flush(NULL,SURFACE_QUEUE_FLAG_DO_NOT_WAIT);
}
```



比較複雜的解決方案可以從排入佇列和排清檢查傳回值，以判斷是否需要進行清除。  
</dl>

### <a name="three-devices"></a>三個裝置

擴充先前的範例以涵蓋多個裝置很簡單。 下列程式碼會執行初始化。 建立生產者/取用者物件之後，使用它們的程式碼就會相同。 此範例有三個裝置，因此有三個佇列。 介面從 Direct3D 9 流至 Direct3D 10 到 Direct3D 11。


```C++
SURFACE_QUEUE_DESC Desc;
Desc.Width        = 640;
Desc.Height       = 480;
Desc.Format       = DXGI_FORMAT_R16G16B16A16_FLOAT;
Desc.NumSurfaces  = 2;
Desc.MetaDataSize = sizeof(UINT);
Desc.Flags        = 0;

SURFACE_QUEUE_CLONE_DESC Desc;
Desc.MetaDataSize = 0;
Desc.Flags        = 0;

CreateSurfaceQueue(&Desc, m_pD3D9Device, &m_11to9Queue);
m_11to9Queue->Clone(&Desc, &m_9to10Queue);
m_11to9Queue->Clone(&Desc, &m_10to11Queue);
```



如先前所述，無論複製何種佇列，複製的運作方式都相同。 例如，第二個複製呼叫可能已關閉 m \_ 9to10Queue 物件。


```C++
// Open for m_p9to10Queue.
m_p9to10Queue->OpenProducer(m_pD3D9Device, &m_pD3D9Producer);
m_p9to10Queue->OpenConsumer(m_pD3D10Device, &m_pD3D10Consumer);

// Open for m_p10to11Queue.
m_p10to11Queue->OpenProducer(m_pD3D10Device, &m_pD3D10Producer);
m_p10to11Queue->OpenConsumer(m_pD3D11Device, &m_pD3D11Consumer);

// Open for m_p11to9Queue.
m_p11to9Queue->OpenProducer(m_pD3D11Device, &m_pD3D11Producer);
m_p11to9Queue->OpenConsumer(m_pD3D9Device, &m_pD3D9Consumer);
```



## <a name="conclusion"></a>結論

您可以建立使用互通性的解決方案，運用多個 DirectX Api 的強大功能。 Windows 圖形 API 互通性現在提供通用的 surface management runtime DXGI 1.1。 此執行時間可在新開發的 Api （例如 Direct3D 11、Direct3D 10.1 和 Direct2D）內啟用同步表面共用支援。 新 Api 與現有 Api 之間的互通性改善有助於應用程式遷移和回溯相容性。 Direct3D 9Ex 和 DXGI 1.1 取用者 Api 可以交互操作，如透過 MSDN 程式碼庫中的範例 helper 程式碼提供的同步處理機制所示。

 

 