---
title: 如何針對文字版面配置執行點擊測試
description: 提供簡短的教學課程，說明如何將點擊測試新增至 DirectWrite 應用程式，以使用 IDWriteTextLayout 介面來顯示文字。
ms.assetid: ef30c931-10f6-4317-b2ea-b446990778b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2ca80ac641920c4e63c08f4cbb0fd9e24eb7b2d
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "103945730"
---
# <a name="how-to-perform-hit-testing-on-a-text-layout"></a>如何針對文字版面配置執行點擊測試

提供簡短的教學課程，說明如何將點擊測試新增至 [DirectWrite](direct-write-portal.md) 應用程式，以使用 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) 介面來顯示文字。

本教學課程的結果是應用程式，會將滑鼠左鍵按下滑鼠左鍵的字元，如下列螢幕擷取畫面所示。

![[按一下此文字] 的螢幕擷取畫面](images/hittest.png)

此如何包含下列元件：

- [步驟1：建立文字版面配置。](#step-1-create-a-text-layout)
- [步驟2：加入 OnClick 方法。](#step-2-add-an-onclick-method)
- [步驟3：執行點擊測試。](#step-3-perform-hit-testing)
- [步驟4：將按一下的文字加上底線。](#step-4-underline-the-clicked-text)
- [步驟5：處理 WM \_ LBUTTONDOWN 訊息。](/windows)

## <a name="step-1-create-a-text-layout"></a>步驟1：建立文字版面配置。

若要開始，您將需要使用 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) 物件的應用程式。 如果您已經有一個顯示文字版面配置的應用程式，請移至步驟2。

若要加入文字版面配置，您必須執行下列動作：

1. 宣告 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) 介面的指標做為類別的成員。

    ```cpp
    IDWriteTextLayout* pTextLayout_;
    ```

2. 在 **CreateDeviceIndependentResources** 方法的結尾，藉由呼叫 [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout)方法來建立 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)介面物件。

    ```cpp
    // Create a text layout using the text format.
    if (SUCCEEDED(hr))
    {
        RECT rect;
        GetClientRect(hwnd_, &rect); 
        float width  = rect.right  / dpiScaleX_;
        float height = rect.bottom / dpiScaleY_;

        hr = pDWriteFactory_->CreateTextLayout(
            wszText_,      // The string to be laid out and formatted.
            cTextLength_,  // The length of the string.
            pTextFormat_,  // The text format to apply to the string (contains font information, etc).
            width,         // The width of the layout box.
            height,        // The height of the layout box.
            &pTextLayout_  // The IDWriteTextLayout interface pointer.
            );
    }
    ```

3. 然後，您必須將 [**ID2D1RenderTarget：:D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) 方法的呼叫變更為 [**ID2D1RenderTarget：:D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) ，如下列程式碼所示。

    ```cpp
    pRT_->DrawTextLayout(
        origin,
        pTextLayout_,
        pBlackBrush_
        );
    ```

## <a name="step-2-add-an-onclick-method"></a>步驟2：加入 OnClick 方法。

現在將方法加入至將使用文字版面配置之點擊測試功能的類別。

1. 在類別標頭檔中宣告 **OnClick** 方法。

    ```cpp
    void OnClick(
        UINT x,
        UINT y
        );
    ```

2. 在類別實檔案中定義 **OnClick** 方法。

   ```cpp
    void DemoApp::OnClick(UINT x, UINT y)
    {    
    }
    ```

## <a name="step-3-perform-hit-testing"></a>步驟3：執行點擊測試。

為了判斷使用者按一下文字版面配置的位置，我們將使用 [**IDWriteTextLayout：： HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) 方法。

將下列程式新增至您在步驟2中定義的 **OnClick** 方法。

1. 宣告將作為參數傳遞給方法的變數。

    ```cpp
    DWRITE_HIT_TEST_METRICS hitTestMetrics;
    BOOL isTrailingHit;
    BOOL isInside; 
    ```

    [**HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint)方法會輸出下列參數。

    | 變數         | 描述                                                                                                                             |
    |------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
    | *hitTestMetrics* | 完全封閉點擊測試位置的幾何。                                                                                     |
    | *isInside*       | 指出點擊測試位置是否在文字字串內。 若為 FALSE，則會傳回最接近文字邊緣的位置。 |
    | *isTrailingHit*  | 指出點擊測試位置是否在字元的開頭或尾端。                                        |

2. 呼叫 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)物件的 [**HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint)方法。

    ```cpp
    pTextLayout_->HitTestPoint(
                    (FLOAT)x, 
                    (FLOAT)y,
                    &isTrailingHit,
                    &isInside,
                    &hitTestMetrics
                    );
    ```

    此範例中的程式碼會傳遞位置的 *x* 和 *y* 變數，而不需要修改。 這可在此範例中完成，因為文字配置的大小與視窗的大小相同，而且源自視窗的左上角。 如果不是這種情況，您必須決定相對於文字版面配置來源的座標。

## <a name="step-4-underline-the-clicked-text"></a>步驟4：將按一下的文字加上底線。

在呼叫 [**HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint)方法之後，將下列步驟新增至您在步驟2中定義的 **OnClick** 。

```cpp
if (isInside == TRUE)
{
    BOOL underline;

    pTextLayout_->GetUnderline(hitTestMetrics.textPosition, &underline);

    DWRITE_TEXT_RANGE textRange = {hitTestMetrics.textPosition, 1};

    pTextLayout_->SetUnderline(!underline, textRange);
}
```

此程式碼會執行下列動作。

1. 使用 *isInside* 變數檢查點擊測試點是否在文字內。
2. *HitTestMetrics* 結構的 **textPosition** 成員包含所按下之字元的以零為起始的索引。

    藉由將此值傳遞給 [**IDWriteTextLayout：： GetUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-getunderline) 方法，取得此字元的底線。

3. 宣告 [**DWRITE \_ 文字 \_ 範圍**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) 變數，其起始位置設定為 **hitTestMetrics. textPosition** 且長度為1。
4. 使用 [**IDWriteTextLayout：： SetUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setunderline) 方法切換底線。

設定底線之後，請呼叫類別的 **DrawD2DContent** 方法來重繪文字。

```cpp
DrawD2DContent();
```

## <a name="step-5-handle-the-wm_lbuttondown-message"></a>步驟5：處理 WM \_ LBUTTONDOWN 訊息。

最後，將 **WM \_ LBUTTONDOWN** 訊息新增至您應用程式的訊息處理常式，並呼叫類別的 **OnClick** 方法。

```cpp
case WM_LBUTTONDOWN:
    {
        int x = GET_X_LPARAM(lParam); 
        int y = GET_Y_LPARAM(lParam);

        pDemoApp->OnClick(x, y);
    }
    break;
```

**取得 \_X \_ LPARAM** 和 **GET \_ x \_ LPARAM** 宏是在 windowsx .h 標頭檔中宣告的。 他們可以輕鬆地取出滑鼠點擊的 x 和 y 位置。
