---
title: 使用 DirectX 裝置資源
description: 瞭解 Microsoft DirectX Graphic Infrastructure 在您的 Windows Store DirectX 遊戲中 (DXGI) 的角色。
ms.assetid: 24c0c81d-6b55-4116-868a-154addf0f04c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 600af9c5ca2d2ba8ce8a7b078c769e195c4a7898384d102a21be3aaaf2c936bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068658"
---
# <a name="work-with-directx-device-resources"></a>使用 DirectX 裝置資源

瞭解 Microsoft DirectX Graphic Infrastructure 在您的 Windows Store DirectX 遊戲中 (DXGI) 的角色。 DXGI 是一組用來設定及管理低層級圖形和圖形介面卡資源的 Api。 如果沒有，您就無法將遊戲的圖形繪製到視窗。

以這種方式來思考：若要直接存取 GPU 及管理其資源，您必須有方法可將其描述至您的應用程式。 您需要的 GPU 最重要資訊部分是繪製圖元的位置，因此可將這些圖元傳送至螢幕。 這通常稱為「背景緩衝區」（GPU 記憶體中的位置），您可以在其中繪製圖元，然後將它「翻轉」或「交換」，並在重新整理信號上傳送至螢幕。 DXGI 可讓您取得該位置，以及使用該緩衝區 (稱為 *交換鏈* 的方法，因為它是一種可插拔的緩衝區，因此可) 多個緩衝策略。

若要這樣做，您需要存取權來寫入交換鏈，以及視窗的控制碼，該視窗會顯示交換鏈目前的背景緩衝區。 您也需要連接這兩個，以確保作業系統會在您要求時，以背景緩衝區的內容重新整理視窗。

繪製到螢幕的整體程式如下：

-   為您的應用程式取得 [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow) 。
-   取得 Direct3D 裝置和內容的介面。
-   建立交換鏈，以在 [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow)中顯示呈現的影像。
-   建立繪圖的呈現目標，並以圖元填入。
-   展示交換鏈！

## <a name="create-a-window-for-your-app"></a>為您的應用程式建立視窗

我們要做的第一件事就是建立一個視窗。 首先，藉由填入 [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa)的實例來建立視窗類別，然後使用 [**RegisterClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa)進行註冊。 視窗類別包含視窗的基本屬性，包括它所使用的圖示、靜態訊息處理函式 (詳細說明此) ，以及視窗類別的唯一名稱。


```C++
if(m_hInstance == NULL) 
    m_hInstance = (HINSTANCE)GetModuleHandle(NULL);

HICON hIcon = NULL;
WCHAR szExePath[MAX_PATH];
    GetModuleFileName(NULL, szExePath, MAX_PATH);

// If the icon is NULL, then use the first one found in the exe
if(hIcon == NULL)
    hIcon = ExtractIcon(m_hInstance, szExePath, 0); 

// Register the windows class
WNDCLASS wndClass;
wndClass.style = CS_DBLCLKS;
wndClass.lpfnWndProc = MainClass::StaticWindowProc;
wndClass.cbClsExtra = 0;
wndClass.cbWndExtra = 0;
wndClass.hInstance = m_hInstance;
wndClass.hIcon = hIcon;
wndClass.hCursor = LoadCursor(NULL, IDC_ARROW);
wndClass.hbrBackground = (HBRUSH)GetStockObject(BLACK_BRUSH);
wndClass.lpszMenuName = NULL;
wndClass.lpszClassName = m_windowClassName.c_str();

if(!RegisterClass(&wndClass))
{
    DWORD dwError = GetLastError();
    if(dwError != ERROR_CLASS_ALREADY_EXISTS)
        return HRESULT_FROM_WIN32(dwError);
}
```



接下來，您要建立視窗。 我們也需要提供視窗的大小資訊，以及我們剛才建立的視窗類別名稱。 當您呼叫 [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa)時，會取回名為 HWND 的非透明指標，您將需要保留 HWND 指標，並在您需要參考視窗時使用它，包括終結或重新建立它，以及在建立用來在視窗中繪製的 DXGI 交換鏈時， (特別重要) 。


```C++
m_rc;
int x = CW_USEDEFAULT;
int y = CW_USEDEFAULT;

// No menu in this example.
m_hMenu = NULL;

// This example uses a non-resizable 640 by 480 viewport for simplicity.
int nDefaultWidth = 640;
int nDefaultHeight = 480;
SetRect(&m_rc, 0, 0, nDefaultWidth, nDefaultHeight);        
AdjustWindowRect(
    &m_rc,
    WS_OVERLAPPEDWINDOW,
    (m_hMenu != NULL) ? true : false
    );

// Create the window for our viewport.
m_hWnd = CreateWindow(
    m_windowClassName.c_str(),
    L"Cube11",
    WS_OVERLAPPEDWINDOW,
    x, y,
    (m_rc.right-m_rc.left), (m_rc.bottom-m_rc.top),
    0,
    m_hMenu,
    m_hInstance,
    0
    );

if(m_hWnd == NULL)
{
    DWORD dwError = GetLastError();
    return HRESULT_FROM_WIN32(dwError);
}
```



Windows 傳統型應用程式模型包含攔截 Windows 訊息迴圈。 您必須撰寫 "StaticWindowProc" 函式來處理視窗化事件，以將您的主要程式迴圈從這個攔截基礎。 這必須是靜態函式，因為 Windows 會在任何類別實例的內容之外呼叫。 以下是一個非常簡單的靜態訊息處理函數範例。


```C++
LRESULT CALLBACK MainClass::StaticWindowProc(
    HWND hWnd,
    UINT uMsg,
    WPARAM wParam,
    LPARAM lParam
    )
{
    switch(uMsg)
    {
        case WM_CLOSE:
        {
            HMENU hMenu;
            hMenu = GetMenu(hWnd);
            if (hMenu != NULL)
            {
                DestroyMenu(hMenu);
            }
            DestroyWindow(hWnd);
            UnregisterClass(
                m_windowClassName.c_str(),
                m_hInstance
                );
            return 0;
        }

        case WM_DESTROY:
            PostQuitMessage(0);
            break;
    }
    
    return DefWindowProc(hWnd, uMsg, wParam, lParam);
}
```



這個簡單的範例只會檢查程式的 [**\_ 結束**](/windows/desktop/winmsg/wm-close)條件：當要求關閉視窗時，會關閉並傳送 wm，而會在視窗實際從螢幕中移除之後傳送的 [**wm \_ 摧毀**](/windows/desktop/winmsg/wm-destroy)。 完整的生產環境應用程式也需要處理其他的視窗事件，如需視窗內事件的完整清單，請參閱 [視窗通知](/windows/desktop/winmsg/window-notifications)。

main 程式迴圈本身需要有機會執行靜態訊息程式，以確認 Windows Windows 的訊息。 藉由分叉行為來協助程式有效率地執行：每個反復專案都應該選擇處理新的 Windows 訊息（如果有的話），如果佇列中沒有任何訊息，則應該呈現新的框架。 以下是一個非常簡單的範例：


```C++
bool bGotMsg;
MSG  msg;
msg.message = WM_NULL;
PeekMessage(&msg, NULL, 0U, 0U, PM_NOREMOVE);

while (WM_QUIT != msg.message)
{
    // Process window events.
    // Use PeekMessage() so we can use idle time to render the scene. 
    bGotMsg = (PeekMessage(&msg, NULL, 0U, 0U, PM_REMOVE) != 0);

    if (bGotMsg)
    {
        // Translate and dispatch the message
        TranslateMessage(&msg);
        DispatchMessage(&msg);
    }
    else
    {
        // Update the scene.
        renderer->Update();

        // Render frames during idle time (when no messages are waiting).
        renderer->Render();

        // Present the frame to the screen.
        deviceResources->Present();
    }
}
```



## <a name="get-an-interface-for-the-direct3d-device-and-context"></a>取得 Direct3D 裝置和內容的介面

使用 Direct3D 的第一個步驟是取得 Direct3D 硬體的介面 (GPU) ，以 [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) 和 [**>id3d11devicecoNtext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2)的實例來表示。 前者是 GPU 資源的虛擬標記法，後者是轉譯管線和進程的裝置中立抽象概念。 以下是一個簡單的思考方式： **ID3D11Device** 包含您不常呼叫的圖形方法（通常會在任何轉譯之前），以取得並設定開始繪製圖元所需的資源集。 另一方面， **>id3d11devicecoNtext** 會包含您每個畫面格所呼叫的方法：在緩衝區和 views 和其他資源中載入、變更輸出合併和轉譯器狀態、管理著色器，以及繪製透過狀態和著色器傳遞這些資源的結果。

此程式有一個非常重要的部分：設定功能等級。 此功能層級會告知 DirectX 您應用程式支援的最低硬體層級，並以 D3D \_ 功能 \_ 層級 \_ 9 \_ 1 做為最小的功能集，並將 d3d \_ 功能 \_ 等級 \_ 11 \_ 1 設為最高。 \_如果您想要觸及最廣泛的物件，則應該支援 9 1。 請花一些時間閱讀 Direct3D [功能等級](/previous-versions/windows/apps/hh994923(v=win.10)) ，並評估您希望遊戲支援的最小和最大功能等級，並瞭解您所選擇的含意。

取得 (指標) 至 Direct3D 裝置和裝置內容的參考，並將它們儲存為 **DeviceResources** 實例上的類別層級變數， (為 **ComPtr** 智慧型指標) 。 每當您需要存取 Direct3D 裝置或裝置內容時，請使用這些參考。


```C++
D3D_FEATURE_LEVEL levels[] = {
    D3D_FEATURE_LEVEL_9_1,
    D3D_FEATURE_LEVEL_9_2,
    D3D_FEATURE_LEVEL_9_3,
    D3D_FEATURE_LEVEL_10_0,
    D3D_FEATURE_LEVEL_10_1,
    D3D_FEATURE_LEVEL_11_0,
    D3D_FEATURE_LEVEL_11_1
};

// This flag adds support for surfaces with a color-channel ordering different
// from the API default. It is required for compatibility with Direct2D.
UINT deviceFlags = D3D11_CREATE_DEVICE_BGRA_SUPPORT;

#if defined(DEBUG) || defined(_DEBUG)
deviceFlags |= D3D11_CREATE_DEVICE_DEBUG;
#endif

// Create the Direct3D 11 API device object and a corresponding context.
Microsoft::WRL::ComPtr<ID3D11Device>        device;
Microsoft::WRL::ComPtr<ID3D11DeviceContext> context;

hr = D3D11CreateDevice(
    nullptr,                    // Specify nullptr to use the default adapter.
    D3D_DRIVER_TYPE_HARDWARE,   // Create a device using the hardware graphics driver.
    0,                          // Should be 0 unless the driver is D3D_DRIVER_TYPE_SOFTWARE.
    deviceFlags,                // Set debug and Direct2D compatibility flags.
    levels,                     // List of feature levels this app can support.
    ARRAYSIZE(levels),          // Size of the list above.
    D3D11_SDK_VERSION,          // Always set this to D3D11_SDK_VERSION for Windows Store apps.
    &device,                    // Returns the Direct3D device created.
    &m_featureLevel,            // Returns feature level of device created.
    &context                    // Returns the device immediate context.
    );

if (FAILED(hr))
{
    // Handle device interface creation failure if it occurs.
    // For example, reduce the feature level requirement, or fail over 
    // to WARP rendering.
}

// Store pointers to the Direct3D 11.1 API device and immediate context.
device.As(&m_pd3dDevice);
context.As(&m_pd3dDeviceContext);
```



## <a name="create-the-swap-chain"></a>建立交換鏈

好：您有一個要在其中繪製的視窗，而且您有一個介面可傳送資料，並將命令提供給 GPU。 現在讓我們來看看如何將它們結合在一起。

首先，您會告訴 DXGI 要用於交換鏈屬性的值。 使用 [**DXGI \_ 交換 \_ 鏈 \_ DESC**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) 結構來進行此作業。 針對桌面應用程式，六個欄位特別重要：

-   **視窗型：指出** 交換鏈是否全螢幕或裁剪至視窗。 將此設為 TRUE，以將交換鏈放在您稍早建立的視窗中。
-   **BufferUsage**：將此設定為 DXGI \_ 使用量轉譯 \_ \_ 目標 \_ 輸出。 這表示交換鏈將會是一個繪圖介面，可讓您將它用作 Direct3D 轉譯目標。
-   **SwapEffect**：將此設定為 [DXGI \_ 交換 \_ 效果] \_ 反轉 \_ 順序。
-   **格式**： [DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM 格式] 會指定32位色彩：三個 RGB 色頻的每一個都是8位，Alpha 色板則為8位。
-   **BufferCount**：將此設定為2，以進行傳統的雙重緩衝行為，以避免發生撕裂。 如果您的圖形內容需要一個以上的監視器重新整理迴圈來轉譯單一畫面格 60 (（例如，閾值超過 16 ms) ，請將緩衝區計數設為3。
-   **SampleDesc**：此欄位會控制取樣。 針對翻轉模型交換鏈，將 **計數** 設定為1，並將 **品質** 設為0。  (若要使用具有翻轉模型交換鏈的交叉分析，請在個別的多重取樣轉譯目標上進行繪製，然後在呈現之前將該目標解析為交換鏈。 範例程式碼會在[Windows Store 應用程式的取樣](/previous-versions/windows/apps/dn458384(v=win.10))中提供。 ) 

指定交換鏈的設定之後，您必須使用建立 Direct3D 裝置 (和裝置內容) 的相同 DXGI factory，才能建立交換鏈。

* * 簡短形式： * *

取得您先前建立的 [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) 參考。 如果您尚未) ，請將它向上轉換成 [**IDXGIDevice3**](/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgidevice3) (，然後呼叫 [**IDXGIDevice：： GETADAPTER**](/windows/desktop/api/dxgi/nf-dxgi-idxgidevice-getadapter) 以取得 DXGI 介面卡。 藉由呼叫 [**IDXGIFactory2：： GetParent**](/windows/desktop/api/dxgi/nf-dxgi-idxgiobject-getparent) ([**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2) 繼承自 [**IDXGIObject**](/windows/desktop/api/dxgi/nn-dxgi-idxgiobject)) 來取得該介面卡的父 factory，現在您可以藉由呼叫 [**CreateSwapChainForHwnd**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd)來使用該 factory 來建立交換鏈，如下列程式碼範例所示。


```C++
DXGI_SWAP_CHAIN_DESC desc;
ZeroMemory(&desc, sizeof(DXGI_SWAP_CHAIN_DESC));
desc.Windowed = TRUE; // Sets the initial state of full-screen mode.
desc.BufferCount = 2;
desc.BufferDesc.Format = DXGI_FORMAT_B8G8R8A8_UNORM;
desc.BufferUsage = DXGI_USAGE_RENDER_TARGET_OUTPUT;
desc.SampleDesc.Count = 1;      //multisampling setting
desc.SampleDesc.Quality = 0;    //vendor-specific flag
desc.SwapEffect = DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL;
desc.OutputWindow = hWnd;

// Create the DXGI device object to use in other factories, such as Direct2D.
Microsoft::WRL::ComPtr<IDXGIDevice3> dxgiDevice;
m_pd3dDevice.As(&dxgiDevice);

// Create swap chain.
Microsoft::WRL::ComPtr<IDXGIAdapter> adapter;
Microsoft::WRL::ComPtr<IDXGIFactory> factory;

hr = dxgiDevice->GetAdapter(&adapter);

if (SUCCEEDED(hr))
{
    adapter->GetParent(IID_PPV_ARGS(&factory));

    hr = factory->CreateSwapChain(
        m_pd3dDevice.Get(),
        &desc,
        &m_pDXGISwapChain
        );
}
```



如果您剛開始使用，最好是使用此處所示的設定。 現在，如果您已經熟悉先前的 DirectX 版本，您可能會問：「為什麼我們不會同時建立裝置和交換鏈，而是不要回頭查看這些類別呢？」 答案是效率：交換鏈是 Direct3D 裝置資源，而裝置資源會系結至建立它們的特定 Direct3D 裝置。 如果您使用新的交換鏈來建立新的裝置，您必須使用新的 Direct3D 裝置重新建立所有裝置資源。 因此，藉由使用與上述相同的相同 factory (建立交換鏈) ，您可以重新建立交換鏈，然後繼續使用您已載入的 Direct3D 裝置資源！

現在您已從作業系統取得一個視窗、一種存取 GPU 和其資源的方式，以及顯示呈現結果的交換鏈。 剩下的就是把整體東西連在一起！

## <a name="create-a-render-target-for-drawing"></a>建立繪圖的呈現目標

著色器管線需要資源來繪製圖元。 建立此資源最簡單的方式，就是將 [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) 資源定義為要繪製之圖元著色器的後置緩衝區，然後將該材質讀入交換鏈中。

若要這樣做，請建立轉譯目標 *視圖*。 在 Direct3D 中，view 是存取特定資源的一種方式。 在此情況下，此視圖可讓圖元著色器在材質完成每個圖元的作業時寫入紋理。

讓我們看看此程式碼。 當您在 \_ 交換鏈上設定 DXGI 使用量轉譯 \_ \_ 目標輸出時 \_ ，會啟用基礎 Direct3D 資源做為繪圖介面使用。 為了取得轉譯目標視圖，我們只需要從交換鏈取得背面緩衝區，並建立系結至背景緩衝區資源的轉譯目標視圖。


```C++
hr = m_pDXGISwapChain->GetBuffer(
    0,
    __uuidof(ID3D11Texture2D),
    (void**) &m_pBackBuffer);

hr = m_pd3dDevice->CreateRenderTargetView(
    m_pBackBuffer.Get(),
    nullptr,
    m_pRenderTarget.GetAddressOf()
    );

m_pBackBuffer->GetDesc(&m_bbDesc);
```



也請建立 *深度樣板緩衝區*。 深度樣板緩衝區只是一種特殊形式的 [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) 資源，通常用來根據相機中物件的距離，根據相機中的物件距離來決定哪些圖元繪製優先權。 深度樣板緩衝區也可以用於樣板效果，其中特定圖元會在點陣化期間被捨棄或忽略。 這個緩衝區的大小必須與轉譯目標相同。 請注意，您無法讀取或轉譯至框架緩衝區深度樣板材質，因為它是由著色器管線在最終的點陣化之前和期間以獨佔方式使用。

此外，也請建立深度樣板緩衝區的視圖作為 [**ID3D11DepthStencilView**](/windows/desktop/api/d3d11/nn-d3d11-id3d11depthstencilview)。 此視圖會告知著色器管線如何解讀基礎 [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) 資源; 因此，如果您未提供此視圖，則不會執行每個圖元的深度測試，且場景中的物件可能會在最少的情況下顯示為一位


```C++
CD3D11_TEXTURE2D_DESC depthStencilDesc(
    DXGI_FORMAT_D24_UNORM_S8_UINT,
    static_cast<UINT> (m_bbDesc.Width),
    static_cast<UINT> (m_bbDesc.Height),
    1, // This depth stencil view has only one texture.
    1, // Use a single mipmap level.
    D3D11_BIND_DEPTH_STENCIL
    );

m_pd3dDevice->CreateTexture2D(
    &depthStencilDesc,
    nullptr,
    &m_pDepthStencil
    );

CD3D11_DEPTH_STENCIL_VIEW_DESC depthStencilViewDesc(D3D11_DSV_DIMENSION_TEXTURE2D);

m_pd3dDevice->CreateDepthStencilView(
    m_pDepthStencil.Get(),
    &depthStencilViewDesc,
    &m_pDepthStencilView
    );
```



最後一個步驟是建立一個視口。 這會定義顯示在畫面上的背景緩衝區可見的矩形;您可以藉由變更視口的參數，來變更螢幕上顯示的緩衝區部分。 這段程式碼會以整個視窗大小為目標，或螢幕解析度（如果是全螢幕交換鏈）。 有趣的是，變更提供的座標值並觀察結果。


```C++
ZeroMemory(&m_viewport, sizeof(D3D11_VIEWPORT));
m_viewport.Height = (float) m_bbDesc.Height;
m_viewport.Width = (float) m_bbDesc.Width;
m_viewport.MinDepth = 0;
m_viewport.MaxDepth = 1;

m_pd3dDeviceContext->RSSetViewports(
    1,
    &m_viewport
    );
```



這就是您在視窗中不需要繪製圖元的方式！ 當您開始時，最好先熟悉如何透過 DXGI 管理 DirectX，以管理開始繪製圖元所需的核心資源。

接下來，您將查看圖形管線的結構;請參閱 [瞭解 DirectX 應用程式範本的轉譯管線](understand-the-directx-11-2-graphics-pipeline.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**接下來**
</dt> <dt>

[使用著色器和著色器資源](work-with-shaders-and-shader-resources.md)
</dt> </dl>

 

 