---
title: 'ID2D1Factory CreateHwndRenderTarget 方法 (D2d1 .h) '
description: 建立呈現至視窗的 ID2D1HwndRenderTarget，轉譯目標。
ms.assetid: 3b55b1b0-a423-40dc-9581-c1fbe8134ca5
keywords:
- CreateHwndRenderTarget 方法 Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 984de8aea923c5b90d05fb79bc0c9edc319fb4bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984129"
---
# <a name="id2d1factorycreatehwndrendertarget-methods"></a><span data-ttu-id="af858-104">ID2D1Factory：： CreateHwndRenderTarget 方法</span><span class="sxs-lookup"><span data-stu-id="af858-104">ID2D1Factory::CreateHwndRenderTarget methods</span></span>

<span data-ttu-id="af858-105">建立呈現至視窗的 [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85))，轉譯目標。</span><span class="sxs-lookup"><span data-stu-id="af858-105">Creates an [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)), a render target that renders to a window.</span></span>

### <a name="overload-list"></a><span data-ttu-id="af858-106">多載清單</span><span class="sxs-lookup"><span data-stu-id="af858-106">Overload list</span></span>



| <span data-ttu-id="af858-107">方法</span><span class="sxs-lookup"><span data-stu-id="af858-107">Method</span></span>                                                                                                                                                                                                                                                                              | <span data-ttu-id="af858-108">描述</span><span class="sxs-lookup"><span data-stu-id="af858-108">Description</span></span>                                                                                                             |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af858-109">[**CreateHwndRenderTarget (D2D1 \_ 轉譯 \_ 目標 \_ 屬性 \* 、D2D1 \_ HWND \_ 轉譯 \_ 目標 \_ 屬性 \* 、ID2D1HwndRenderTarget \* \*)**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="af858-109">[**CreateHwndRenderTarget(D2D1\_RENDER\_TARGET\_PROPERTIES\*,D2D1\_HWND\_RENDER\_TARGET\_PROPERTIES\*,ID2D1HwndRenderTarget\*\*)**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85))</span></span> | <span data-ttu-id="af858-110">建立呈現至視窗的 [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85))，轉譯目標。</span><span class="sxs-lookup"><span data-stu-id="af858-110">Creates an [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)), a render target that renders to a window.</span></span><br/> |
| <span data-ttu-id="af858-111">[**CreateHwndRenderTarget (D2D1 \_ 轉譯 \_ 目標 \_ 屬性&、D2D1 \_ HWND \_ 轉譯 \_ 目標 \_ 屬性&、ID2D1HwndRenderTarget \* \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createhwndrendertarget(constd2d1_render_target_properties__constd2d1_hwnd_render_target_properties__id2d1hwndrendertarget))</span><span class="sxs-lookup"><span data-stu-id="af858-111">[**CreateHwndRenderTarget(D2D1\_RENDER\_TARGET\_PROPERTIES&,D2D1\_HWND\_RENDER\_TARGET\_PROPERTIES&,ID2D1HwndRenderTarget\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createhwndrendertarget(constd2d1_render_target_properties__constd2d1_hwnd_render_target_properties__id2d1hwndrendertarget))</span></span>   | <span data-ttu-id="af858-112">建立呈現至視窗的 [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85))，轉譯目標。</span><span class="sxs-lookup"><span data-stu-id="af858-112">Creates an [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)), a render target that renders to a window.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="af858-113">備註</span><span class="sxs-lookup"><span data-stu-id="af858-113">Remarks</span></span>

<span data-ttu-id="af858-114">當您建立轉譯目標並提供硬體加速時，您會在電腦的 GPU 上配置資源。</span><span class="sxs-lookup"><span data-stu-id="af858-114">When you create a render target and hardware acceleration is available, you allocate resources on the computer's GPU.</span></span> <span data-ttu-id="af858-115">藉由建立轉譯目標一次並保留最長的時間，您就能獲得效能優勢。</span><span class="sxs-lookup"><span data-stu-id="af858-115">By creating a render target once and retaining it as long as possible, you gain performance benefits.</span></span> <span data-ttu-id="af858-116">您的應用程式應該建立轉譯目標一次，並在應用程式的存留期內保存它們，或在收到 [**D2DERR \_ 重新建立 \_ 目標**](direct2d-error-codes.md) 錯誤之前保留。</span><span class="sxs-lookup"><span data-stu-id="af858-116">Your application should create render targets once and hold onto them for the life of the application or until the [**D2DERR\_RECREATE\_TARGET**](direct2d-error-codes.md) error is received.</span></span> <span data-ttu-id="af858-117">當您收到此錯誤時，您必須重新建立轉譯目標 (以及它所建立) 的任何資源。</span><span class="sxs-lookup"><span data-stu-id="af858-117">When you receive this error, you need to recreate the render target (and any resources it created).</span></span>

## <a name="examples"></a><span data-ttu-id="af858-118">範例</span><span class="sxs-lookup"><span data-stu-id="af858-118">Examples</span></span>

<span data-ttu-id="af858-119">下列範例會建立 [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="af858-119">The following example creates an [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)).</span></span>


```C++
RECT rc;
GetClientRect(m_hwnd, &rc);

D2D1_SIZE_U size = D2D1::SizeU(
    rc.right - rc.left,
    rc.bottom - rc.top
    );

// Create a Direct2D render target.
hr = m_pD2DFactory->CreateHwndRenderTarget(
    D2D1::RenderTargetProperties(),
    D2D1::HwndRenderTargetProperties(m_hwnd, size),
    &m_pRenderTarget
    );
```



## <a name="requirements"></a><span data-ttu-id="af858-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="af858-120">Requirements</span></span>



| <span data-ttu-id="af858-121">需求</span><span class="sxs-lookup"><span data-stu-id="af858-121">Requirement</span></span> | <span data-ttu-id="af858-122">值</span><span class="sxs-lookup"><span data-stu-id="af858-122">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="af858-123">標頭</span><span class="sxs-lookup"><span data-stu-id="af858-123">Header</span></span><br/>  | <dl> <span data-ttu-id="af858-124"><dt>D2d1。h</dt></span><span class="sxs-lookup"><span data-stu-id="af858-124"><dt>D2d1.h</dt></span></span> </dl>   |
| <span data-ttu-id="af858-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="af858-125">Library</span></span><br/> | <dl> <span data-ttu-id="af858-126"><dt>D2d1 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="af858-126"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="af858-127">DLL</span><span class="sxs-lookup"><span data-stu-id="af858-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="af858-128"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af858-128"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af858-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="af858-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af858-130">**ID2D1Factory**</span><span class="sxs-lookup"><span data-stu-id="af858-130">**ID2D1Factory**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)
</dt> </dl>
