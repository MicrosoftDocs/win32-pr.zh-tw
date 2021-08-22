---
title: DWM 模糊背後總覽
description: 其中一個桌面視窗管理員 (DWM) 效果的簽章是透明且模糊的非工作區。 DWM Api 可讓應用程式將這些效果套用到其最上層視窗的工作區。
ms.assetid: bdf0f8bd-e399-4244-ae39-460f09a16f3c
keywords:
- 桌面視窗管理員 (DWM) ，模糊後變效果
- DWM (桌面視窗管理員) ，模糊後變效果
- 模糊後變效果
- 透明效果
- 透明玻璃效果
- 桌面視窗管理員 (DWM) ，半透明效果
- DWM (桌面視窗管理員) ，半透明效果
- 桌面視窗管理員 (DWM) 、透明玻璃效果
- DWM (桌面視窗管理員) 、透明玻璃效果
- 桌面視窗管理員 (DWM) ，將視窗框架擴充到工作區
- DWM (桌面視窗管理員) ，將視窗框架擴充到工作區
- 將視窗框架擴充到工作區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfb7b357719ea3aa5a4853a933350ee2dda417842777354e2bbf1711e1cbeff1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119456074"
---
# <a name="dwm-blur-behind-overview"></a>DWM 模糊背後總覽

其中一個桌面視窗管理員 (DWM) 效果的簽章是透明且模糊的非工作區。 DWM Api 可讓應用程式將這些效果套用到其最上層視窗的工作區。

> [!Note]  
> WindowsVista Home Basic edition 不支援透明的半透明效果。 通常會在其他 Windows 版本上以透明半透明效果呈現的區域會轉譯為不透明。
> 從 Windows 8 開始，呼叫此函式並不會造成模糊效果，因為轉譯視窗的方式中的樣式變更。


 

本主題討論 DWM 啟用的下列用戶端模糊背後案例。

-   [將模糊新增至工作區的特定區域](#adding-blur-to-a-specific-region-of-the-client-area)
-   [將視窗框架擴充到工作區](#extending-the-window-frame-into-the-client-area)
-   [相關主題](#related-topics)

## <a name="adding-blur-to-a-specific-region-of-the-client-area"></a>將模糊新增至工作區的特定區域

應用程式可將模糊效果套用到視窗的整個用戶端區域後方，或套用至特定的子領域。 這可讓應用程式新增樣式的路徑和搜尋列，與應用程式的其餘部分以視覺化方式區分。

此案例中使用的 API 是 [**DwmEnableBlurBehindWindow**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenableblurbehindwindow)函式，它會利用常數和 [**Dwm \_ BLURBEHIND**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind)結構 [**背後的 dwm 模糊**](dwm-bb-constants.md)。

下列範例函式 `EnableBlurBehind` 說明如何將模糊後端效果套用至整個視窗。


```
HRESULT EnableBlurBehind(HWND hwnd)
{
    HRESULT hr = S_OK;

    // Create and populate the blur-behind structure.
    DWM_BLURBEHIND bb = {0};

    // Specify blur-behind and blur region.
    bb.dwFlags = DWM_BB_ENABLE;
    bb.fEnable = true;
    bb.hRgnBlur = NULL;

    // Enable blur-behind.
    hr = DwmEnableBlurBehindWindow(hwnd, &bb);
    if (SUCCEEDED(hr))
    {
        // ...
    }
    return hr;
}
```



請注意， **Null** 是在 *hRgnBlur* 參數中指定。 這會告知 DWM 將模糊套用到整個視窗後方。

下圖說明套用至整個視窗的模糊後端效果。

![套用至視窗的模糊後端效果](images/dwm-blurbehindwindow.png)

若要將模糊套用到子領域後方，請將有效的區域控制碼 (HRGN) 套用至 [**DWM \_ BLURBEHIND**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind)結構的 **hRgnBlur** 成員，然後將 **DWM \_ BB \_ BLURREGION** 旗標加入 **dwFlags** 成員中。

當您將模糊後端效果套用至視窗的子領域時，視窗的 Alpha 色板會用於 nonblurred 區域。 這可能會導致視窗的 nonblurred 區域出現非預期的透明度。 因此，當您將模糊效果套用至子領域時，請務必小心。

## <a name="extending-the-window-frame-into-the-client-area"></a>將視窗框架擴充到工作區

應用程式可以將視窗框架的模糊擴充到工作區。 當您使用停駐的工具列套用視窗背後的模糊效果，或以視覺化方式將控制項與應用程式的其餘部分分開時，這會很有用。 這項功能是由 [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) 函數所公開。

若要使用 [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea)來啟用模糊，請使用 [**邊界**](/windows/win32/api/uxtheme/ns-uxtheme-margins) 結構來指出要延伸至工作區的程度。 下列範例函式會將 `ExtendIntoClientBottom` 非用戶端框架底部的模糊擴充功能切換至工作區。


```
HRESULT ExtendIntoClientBottom(HWND hwnd)
{
    HRESULT hr = S_OK;

    // Set the margins, extending the bottom margin.
    MARGINS margins = {0,0,0,25};

    // Extend the frame on the bottom of the client area.
    hr = DwmExtendFrameIntoClientArea(hwnd,&margins);
    if (SUCCEEDED(hr))
    {
        // ...
    }
    return hr;
}
```



下圖說明延伸至用戶端區域底部的模糊後端效果。

![顯示延伸至用戶端區域底部之模糊後變效果的影像](images/dwm-extendedbottom.png)

也可透過 [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) 方法使用，這是「半透明工作表」的效果，其中模糊效果會套用至視窗的整個表面，而不會有可見的視窗框線。 下列範例示範在不使用視窗框線的情況下呈現用戶端區域的效果。


```
HRESULT ExtendIntoClientAll(HWND hwnd)
{
    HRESULT hr = S_OK;

    // Negative margins have special meaning to DwmExtendFrameIntoClientArea.
    // Negative margins create the "sheet of glass" effect, where the client 
    // area is rendered as a solid surface without a window border.
    MARGINS margins = {-1};

    // Extend the frame across the whole window.
    hr = DwmExtendFrameIntoClientArea(hwnd,&margins);
    if (SUCCEEDED(hr))
    {
        // ...
    }
    return hr;
}
```



下圖說明「半透明工作表」視窗樣式的模糊背後。

![說明「半透明工作表」視窗樣式中模糊背後效果的影像](images/dwm-sheetofglass.png)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[桌面視窗管理員概觀](dwm-overview.md)
</dt> <dt>

[Enable and Control DWM Composition (啟用並控制 DWM 組合)](composition-ovw.md)
</dt> <dt>

[效能考慮和最佳作法](bestpractices-ovw.md)
</dt> </dl>

 

 