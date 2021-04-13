---
title: 利用 High-Definition 滑鼠移動
description: 本文著重于將遊戲中的高定義滑鼠輸入效能優化的最佳方式，例如第一個人的射擊。
ms.assetid: 0138a248-e8e0-a392-564e-7a9229b94b56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ebe2abd9487d95b8fe12aa3c6938e21d72d8e2f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104376080"
---
# <a name="taking-advantage-of-high-definition-mouse-movement"></a>利用 High-Definition 滑鼠移動

標準電腦滑鼠以每英寸400點傳回資料 (DPI) ，而高定義的滑鼠會在 800 DPI 或更高的時間產生資料。 如此一來，來自高定義滑鼠的輸入會比標準滑鼠更精確。 但是，無法透過標準的 WM MOUSEMOVE 訊息取得高定義資料 \_ 。 一般情況下，遊戲將會從高定義的滑鼠裝置獲益，但只使用 WM MOUSEMOVE 取得滑鼠資料的遊戲將無法 \_ 存取完整、未篩選的滑鼠解析度。

許多公司都是製造高定義的滑鼠裝置，例如 Microsoft 和 Logitech。 隨著高解析度的滑鼠裝置越來越普及，開發人員必須瞭解如何以最佳方式使用這些裝置所產生的資訊。 本文著重于將遊戲中的高定義滑鼠輸入效能優化的最佳方式，例如第一個人的射擊。

## <a name="retrieving-mouse-movement-data"></a>正在抓取滑鼠移動資料

以下是用來取出滑鼠資料的三種主要方法：

-   [WM \_ MOUSEMOVE](/windows)
-   [WM \_ 輸入](/windows)
-   [DirectInput](#directinput)

每種方法都有其優點和缺點，視資料的使用方式而定。

### <a name="wm_mousemove"></a>WM \_ MOUSEMOVE

讀取滑鼠移動資料最簡單的方法是透過 WM \_ MOUSEMOVE 訊息。 以下是如何從 WM MOUSEMOVE 訊息讀取滑鼠移動資料的範例 \_ ：

```cpp
case WM_MOUSEMOVE:
{
    int xPosAbsolute = GET_X_PARAM(lParam); 
    int yPosAbsolute = GET_Y_PARAM(lParam);
    // ...
    break;
}
```

從 WM MOUSEMOVE 資料的主要缺點 \_ 是限制為螢幕解析度。 這表示，如果您稍微移動滑鼠，而不是太大而導致指標移至下一個圖元，則不 \_ 會產生任何 WM MOUSEMOVE 訊息。 因此，使用這個方法來讀取滑鼠移動會使高定義輸入的優點更不一樣。

不過，有了 WM MOUSEMOVE 的優點， \_ 就是 Windows 會將指標加速 (也稱為 ballistics) 至原始滑鼠資料，讓滑鼠指標的行為如同客戶預期般運作。 如此可讓 \_ 多部 wm 的 (透過 wm \_ 輸入或 DirectInput) 的指標控制選項，因為它會導致使用者更自然的行為。 雖然 WM \_ MOUSEMOVE 很適合用來移動滑鼠指標，但不太適合用來移動第一張相機，因為高度定義的精確度將會遺失。

如需有關 WM mousemove 的詳細資訊 \_ ，請參閱 [**wm \_ mousemove**](/windows/desktop/inputdev/wm-mousemove)。

### <a name="wm_input"></a>WM \_ 輸入

取得滑鼠資料的第二種方法是讀取 WM \_ 輸入訊息。 處理 WM \_ 輸入訊息比處理 wm \_ MOUSEMOVE 訊息更複雜，但 \_ 會直接從人類介面裝置讀取 wm 輸入訊息 (隱藏) 堆疊，並反映高定義結果。

若要讀取來自 WM 輸入訊息的滑鼠移動資料 \_ ，必須先註冊裝置; 下列程式碼提供這項操作的範例：

```cpp
// you can #include <hidusage.h> for these defines
#ifndef HID_USAGE_PAGE_GENERIC
#define HID_USAGE_PAGE_GENERIC         ((USHORT) 0x01)
#endif
#ifndef HID_USAGE_GENERIC_MOUSE
#define HID_USAGE_GENERIC_MOUSE        ((USHORT) 0x02)
#endif

RAWINPUTDEVICE Rid[1];
Rid[0].usUsagePage = HID_USAGE_PAGE_GENERIC; 
Rid[0].usUsage = HID_USAGE_GENERIC_MOUSE; 
Rid[0].dwFlags = RIDEV_INPUTSINK;   
Rid[0].hwndTarget = hWnd;
RegisterRawInputDevices(Rid, 1, sizeof(Rid[0]));
```

下列程式碼會 \_ 在應用程式的 WinProc 處理常式中處理 WM 輸入訊息：

```cpp
case WM_INPUT: 
{
    UINT dwSize = sizeof(RAWINPUT);
    static BYTE lpb[sizeof(RAWINPUT)];

    GetRawInputData((HRAWINPUT)lParam, RID_INPUT, lpb, &dwSize, sizeof(RAWINPUTHEADER));

    RAWINPUT* raw = (RAWINPUT*)lpb;

    if (raw->header.dwType == RIM_TYPEMOUSE) 
    {
        int xPosRelative = raw->data.mouse.lLastX;
        int yPosRelative = raw->data.mouse.lLastY;
    } 
    break;
}
```

使用 WM 輸入的好處 \_ 是，您的遊戲可能會以最低層級從滑鼠接收原始資料。

缺點是，WM \_ 輸入沒有套用至其資料的 ballistics，因此如果您想要利用這項資料來驅動資料指標，將需要額外的投入時間，讓資料指標的行為就像在 Windows 中一樣。 如需套用指標 ballistics 的詳細資訊，請參閱 [WINDOWS XP 的指標 ballistics](https://www.microsoft.com/whdc/archive/pointer-bal.mspx)。

如需有關 WM 輸入的詳細資訊 \_ ，請參閱 [關於 Raw 輸入](/windows/desktop/inputdev/about-raw-input)。

### <a name="directinput"></a>DirectInput

[DirectInput](/windows-hardware/drivers/hid/directinput) 是一組 API 呼叫，可將系統上的輸入裝置抽象化。 就內部而言，DirectInput 會建立第二個執行緒來讀取 WM \_ 輸入資料，而使用 DirectInput api 會增加額外負荷，而不只是直接讀取 wm \_ 輸入。 DirectInput 僅適用于從 DirectInput 操縱杆讀取資料;但是，如果您只需要支援適用于 Windows 的 Xbox 360 控制器，請改用 [XInput](/windows/desktop/xinput/xinput-game-controller-apis-portal) 。 整體來說，使用 DirectInput 從滑鼠或鍵盤裝置讀取資料時，不會提供任何優點，而且不建議在這些案例中使用 DirectInput。

將使用 [DirectInput](/windows-hardware/drivers/hid/directinput)（如下列程式碼所示）的複雜性與先前所述的方法進行比較。 建立 DirectInput 滑鼠需要下列一組呼叫：

```cpp
LPDIRECTINPUT8 pDI;
LPDIRECTINPUTDEVICE8 pMouse;

hr = DirectInput8Create(GetModuleHandle(NULL), DIRECTINPUT_VERSION, IID_IDirectInput8, (VOID**)&pDI, NULL);
if(FAILED(hr))
    return hr;

hr = pDI->CreateDevice(GUID_SysMouse, &pMouse, NULL);
if(FAILED(hr))
    return hr;

hr = pMouse->SetDataFormat(&c_dfDIMouse2);
if(FAILED(hr))
    return hr;

hr = pMouse->SetCooperativeLevel(hWnd, DISCL_NONEXCLUSIVE | DISCL_FOREGROUND);
if(FAILED(hr))
    return hr;

if(!bImmediate)
{
    DIPROPDWORD dipdw;
    dipdw.diph.dwSize       = sizeof(DIPROPDWORD);
    dipdw.diph.dwHeaderSize = sizeof(DIPROPHEADER);
    dipdw.diph.dwObj        = 0;
    dipdw.diph.dwHow        = DIPH_DEVICE;
    dipdw.dwData            = 16; // Arbitrary buffer size

    if(FAILED(hr = pMouse->SetProperty(DIPROP_BUFFERSIZE, &dipdw.diph)))
        return hr;
}

pMouse->Acquire();
```

然後可以讀取每個畫面格的 DirectInput 滑鼠裝置：

```cpp
DIMOUSESTATE2 dims2; 
ZeroMemory(&dims2, sizeof(dims2));

hr = pMouse->GetDeviceState(sizeof(DIMOUSESTATE2), &dims2);
if(FAILED(hr)) 
{
    hr = pMouse->Acquire();
    while(hr == DIERR_INPUTLOST) 
        hr = pMouse->Acquire();

    return S_OK; 
}

int xPosRelative = dims2.lX;
int yPosRelative = dims2.lY;
```

## <a name="summary"></a>總結

整體來說，接收高定義滑鼠移動資料的最佳方法是輸入 WM \_ 。 如果您的使用者只是移動滑鼠指標，則請考慮使用 WM \_ MOUSEMOVE，以避免需要執行指標 ballistics。 這兩個視窗訊息都可以正常運作，即使滑鼠不是高定義的滑鼠也一樣。 藉由支援高定義，Windows 遊戲可為使用者提供更精確的控制。