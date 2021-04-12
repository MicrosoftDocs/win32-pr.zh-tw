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
ms.openlocfilehash: 1649d52c2e9098513c115daaf295c4005e890b8e
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/12/2021
ms.locfileid: "104195699"
---
# <a name="inkd2drenderer-class"></a><span data-ttu-id="e94c2-103">InkD2DRenderer 類別</span><span class="sxs-lookup"><span data-stu-id="e94c2-103">InkD2DRenderer class</span></span>

<span data-ttu-id="e94c2-104">實行 [**IInkD2DRenderer**](/windows/win32/api/inkrenderer/nn-inkrenderer-iinkd2drenderer) 介面。</span><span class="sxs-lookup"><span data-stu-id="e94c2-104">Implements the [**IInkD2DRenderer**](/windows/win32/api/inkrenderer/nn-inkrenderer-iinkd2drenderer) interface.</span></span>

<span data-ttu-id="e94c2-105">[**IInkD2DRenderer**](/windows/win32/api/inkrenderer/nn-inkrenderer-iinkd2drenderer)物件可將筆墨筆劃轉譯至通用 Windows 應用程式的指定 Direct2D 裝置內容，而不是預設的 [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas)控制項。</span><span class="sxs-lookup"><span data-stu-id="e94c2-105">An [**IInkD2DRenderer**](/windows/win32/api/inkrenderer/nn-inkrenderer-iinkd2drenderer) object enables the rendering of ink strokes onto the designated Direct2D device context of a Universal Windows app, instead of the default [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas) control.</span></span>

## <a name="members"></a><span data-ttu-id="e94c2-106">成員</span><span class="sxs-lookup"><span data-stu-id="e94c2-106">Members</span></span>

<span data-ttu-id="e94c2-107">**InkD2DRenderer** 類別繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="e94c2-107">The **InkD2DRenderer** class inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="e94c2-108">**InkD2DRenderer** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e94c2-108">**InkD2DRenderer** also has these types of members:</span></span>

- [<span data-ttu-id="e94c2-109">方法</span><span class="sxs-lookup"><span data-stu-id="e94c2-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e94c2-110">方法</span><span class="sxs-lookup"><span data-stu-id="e94c2-110">Methods</span></span>

<span data-ttu-id="e94c2-111">**InkD2DRenderer** 類別有這些方法。</span><span class="sxs-lookup"><span data-stu-id="e94c2-111">The **InkD2DRenderer** class has these methods.</span></span>

| <span data-ttu-id="e94c2-112">方法</span><span class="sxs-lookup"><span data-stu-id="e94c2-112">Method</span></span>                              | <span data-ttu-id="e94c2-113">描述</span><span class="sxs-lookup"><span data-stu-id="e94c2-113">Description</span></span>                                                                             |
|:------------------------------------|:----------------------------------------------------------------------------------------|
| [<span data-ttu-id="e94c2-114">**Draw**</span><span class="sxs-lookup"><span data-stu-id="e94c2-114">**Draw**</span></span>](/windows/win32/api/inkrenderer/nf-inkrenderer-iinkd2drenderer-draw) | <span data-ttu-id="e94c2-115">將筆墨筆劃轉譯為應用程式的指定 Direct2D 裝置內容。</span><span class="sxs-lookup"><span data-stu-id="e94c2-115">Renders the ink stroke to the designated Direct2D device context of the app.</span></span><br/> |

## <a name="creationaccess-functions"></a><span data-ttu-id="e94c2-116">建立 \\ 存取函數</span><span class="sxs-lookup"><span data-stu-id="e94c2-116">Creation\\Access Functions</span></span>

<span data-ttu-id="e94c2-117">使用類別識別碼<strong>InkD2DRenderer</strong>呼叫[<strong>CoCreateInstance</strong>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) ，以取得物件的參考。</span><span class="sxs-lookup"><span data-stu-id="e94c2-117">Call [<strong>CoCreateInstance</strong>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) with the class identifier <strong>InkD2DRenderer</strong> to retrieve a reference to the object.</span></span>

``` C++
CoCreateInstance(__uuidof(InkD2DRenderer),
  nullptr,
  CLSCTX_INPROC_SERVER,
  IID_PPV_ARGS(&_spInkD2DRenderer));
```

## <a name="examples"></a><span data-ttu-id="e94c2-118">範例</span><span class="sxs-lookup"><span data-stu-id="e94c2-118">Examples</span></span>

<span data-ttu-id="e94c2-119">[複雜筆墨範例](/samples/microsoft/windows-universal-samples/complexink/)"SceneComposer" 檔案中的這個程式碼片段會示範如何將筆墨筆劃集合轉譯為 Direct2D 裝置內容。</span><span class="sxs-lookup"><span data-stu-id="e94c2-119">This snippet from the "SceneComposer.cpp" file of the [Complex inking sample](/samples/microsoft/windows-universal-samples/complexink/) demonstrates the rendering of a collection of ink strokes to a Direct2D device context.</span></span>

```C++
_inkRenderer->Render(strokes, _deviceResources->GetD2DDeviceContext());
strokes->Clear();
```

<span data-ttu-id="e94c2-120">[複雜筆墨範例](/samples/microsoft/windows-universal-samples/complexink/)"InkRenderer" 檔案中的這個程式碼片段會示範在先前的程式碼片段中呼叫的轉譯方法 (，) 呼叫 [**Draw**](/windows/win32/api/inkrenderer/nf-inkrenderer-iinkd2drenderer-draw)方法來呈現筆劃。</span><span class="sxs-lookup"><span data-stu-id="e94c2-120">This snippet from the "InkRenderer.cpp" file of the [Complex inking sample](/samples/microsoft/windows-universal-samples/complexink/) shows the Render method (called in the previous snippet) that calls the [**Draw**](/windows/win32/api/inkrenderer/nf-inkrenderer-iinkd2drenderer-draw) method for rendering the strokes.</span></span>

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

## <a name="requirements"></a><span data-ttu-id="e94c2-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="e94c2-121">Requirements</span></span>

| <span data-ttu-id="e94c2-122">需求</span><span class="sxs-lookup"><span data-stu-id="e94c2-122">Requirement</span></span> | <span data-ttu-id="e94c2-123">值</span><span class="sxs-lookup"><span data-stu-id="e94c2-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="e94c2-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e94c2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e94c2-125">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e94c2-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e94c2-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e94c2-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e94c2-127">都不支援</span><span class="sxs-lookup"><span data-stu-id="e94c2-127">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="e94c2-128">標頭</span><span class="sxs-lookup"><span data-stu-id="e94c2-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="e94c2-129"><dt>Inkrenderer。h</dt></span><span class="sxs-lookup"><span data-stu-id="e94c2-129"><dt>Inkrenderer.h</dt></span></span> </dl>   |
| <span data-ttu-id="e94c2-130">Idl</span><span class="sxs-lookup"><span data-stu-id="e94c2-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e94c2-131"><dt>Inkrenderer .idl</dt></span><span class="sxs-lookup"><span data-stu-id="e94c2-131"><dt>Inkrenderer.idl</dt></span></span> </dl> |
| <span data-ttu-id="e94c2-132">IID</span><span class="sxs-lookup"><span data-stu-id="e94c2-132">IID</span></span><br/>                      | <span data-ttu-id="e94c2-133">IID \_ IInkD2DRenderer 定義為4044e60c-7b01-4671-a97c-04e0210a07a5</span><span class="sxs-lookup"><span data-stu-id="e94c2-133">IID\_IInkD2DRenderer is defined as 4044e60c-7b01-4671-a97c-04e0210a07a5</span></span><br/>         |

## <a name="related-topics"></a><span data-ttu-id="e94c2-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="e94c2-134">Related topics</span></span>

<span data-ttu-id="e94c2-135">[筆墨](ink-renderer.md)轉譯器、[畫筆和手寫筆互動](/windows/uwp/design/input/pen-and-stylus-interactions)、[筆墨分析範例](/samples/microsoft/windows-universal-samples/inkanalysis/)、[簡單筆墨範例](/samples/microsoft/windows-universal-samples/simpleink/)、[複雜](/samples/microsoft/windows-universal-samples/complexink/)的筆墨範例</span><span class="sxs-lookup"><span data-stu-id="e94c2-135">[Ink renderer](ink-renderer.md), [Pen and stylus interactions](/windows/uwp/design/input/pen-and-stylus-interactions), [Ink Analysis sample](/samples/microsoft/windows-universal-samples/inkanalysis/), [Simple inking sample](/samples/microsoft/windows-universal-samples/simpleink/), [Complex inking sample](/samples/microsoft/windows-universal-samples/complexink/)</span></span>
