---
description: 實行 IInkD2DRenderer 介面。
ms.assetid: d1bd910d-ce64-4424-a0e1-4f55110b0265
title: InkD2DRenderer 類別
ms.topic: language-reference
ms.date: 02/03/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- InkD2DRenderer
api_type:
- COM
api_location:
- Inkrenderer.idl
ms.openlocfilehash: 51383770b8eb0c5dca5efbb5f1756bee81ece506c0e92337e9df9a60eb0a8aee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726728"
---
# <a name="inkd2drenderer-class"></a>InkD2DRenderer 類別

實行 [**IInkD2DRenderer**](/windows/win32/api/inkrenderer/nn-inkrenderer-iinkd2drenderer) 介面。

[**IInkD2DRenderer**](/windows/win32/api/inkrenderer/nn-inkrenderer-iinkd2drenderer)物件可將筆墨筆劃轉譯到通用 Windows 應用程式的指定 Direct2D 裝置內容，而不是預設的 [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas)控制項。

## <a name="members"></a>成員

**InkD2DRenderer** 類別繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **InkD2DRenderer** 也有下列類型的成員：

- [方法](#methods)

### <a name="methods"></a>方法

**InkD2DRenderer** 類別有這些方法。

| 方法                              | 描述                                                                             |
|:------------------------------------|:----------------------------------------------------------------------------------------|
| [**Draw**](/windows/win32/api/inkrenderer/nf-inkrenderer-iinkd2drenderer-draw) | 將筆墨筆劃轉譯為應用程式的指定 Direct2D 裝置內容。<br/> |

## <a name="creationaccess-functions"></a>建立 \\ 存取函數

使用類別識別碼<strong>InkD2DRenderer</strong>呼叫[<strong>CoCreateInstance</strong>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) ，以取得物件的參考。

``` C++
CoCreateInstance(__uuidof(InkD2DRenderer),
  nullptr,
  CLSCTX_INPROC_SERVER,
  IID_PPV_ARGS(&_spInkD2DRenderer));
```

## <a name="examples"></a>範例

[複雜筆墨範例](/samples/microsoft/windows-universal-samples/complexink/)"SceneComposer" 檔案中的這個程式碼片段會示範如何將筆墨筆劃集合轉譯為 Direct2D 裝置內容。

```C++
_inkRenderer->Render(strokes, _deviceResources->GetD2DDeviceContext());
strokes->Clear();
```

[複雜筆墨範例](/samples/microsoft/windows-universal-samples/complexink/)"InkRenderer" 檔案中的這個程式碼片段會示範在先前的程式碼片段中呼叫的轉譯方法 (，) 呼叫 [**Draw**](/windows/win32/api/inkrenderer/nf-inkrenderer-iinkd2drenderer-draw)方法來呈現筆劃。

```C++
void InkRenderer::Render(
    Platform::Collections::Vector<
        Windows::UI::Input::Inking::InkStroke^>^ strokes,
        Microsoft::WRL::ComPtr<ID2D1DeviceContext> d2dContext)
{
    HRESULT hr = S_OK;
    if (_spInkD2DRenderer != nullptr)
    {
        if (strokes != nullptr && strokes->Size > 0)
        {
            // Cast the stroke collection into IUnknown to call Inkd2dRenderer
            ComPtr<IUnknown> spUnkStrokes = 
                reinterpret_cast<IUnknown*>(reinterpret_cast<__abi_IUnknown*>(strokes));
            hr = _spInkD2DRenderer->Draw(d2dContext.Get(), spUnkStrokes.Get(), false);
            if (FAILED(hr))
            {
                DX::ThrowIfFailed(hr);
            }
        }
    }
}
```

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 \[僅限桌面應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                  |
| 標頭<br/>                   | <dl> <dt>Inkrenderer。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Inkrenderer .idl</dt> </dl> |
| IID<br/>                      | IID \_ IInkD2DRenderer 定義為4044e60c-7b01-4671-a97c-04e0210a07a5<br/>         |

## <a name="related-topics"></a>相關主題

[筆墨](ink-renderer.md)轉譯器、[畫筆和手寫筆互動](/windows/uwp/design/input/pen-and-stylus-interactions)、[筆墨分析範例](/samples/microsoft/windows-universal-samples/inkanalysis/)、[簡單筆墨範例](/samples/microsoft/windows-universal-samples/simpleink/)、[複雜](/samples/microsoft/windows-universal-samples/complexink/)的筆墨範例
