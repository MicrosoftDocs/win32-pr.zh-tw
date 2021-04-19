---
title: ID2D1Factory CreateWicBitmapRenderTarget 方法
description: 建立呈現至 Microsoft Windows 影像處理元件 (WIC) 點陣圖的轉譯目標。
ms.assetid: 93141743-c11d-40b4-83c5-07c9066836c7
keywords:
- CreateWicBitmapRenderTarget 方法 Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 4025028582c254e7a5724a575ef0d7f1c7d91570
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992835"
---
# <a name="id2d1factorycreatewicbitmaprendertarget-methods"></a><span data-ttu-id="6ffe9-104">ID2D1Factory：： CreateWicBitmapRenderTarget 方法</span><span class="sxs-lookup"><span data-stu-id="6ffe9-104">ID2D1Factory::CreateWicBitmapRenderTarget methods</span></span>

<span data-ttu-id="6ffe9-105">建立呈現至 Microsoft Windows 影像處理元件 (WIC) 點陣圖的轉譯目標。</span><span class="sxs-lookup"><span data-stu-id="6ffe9-105">Creates a render target that renders to a Microsoft Windows Imaging Component (WIC) bitmap.</span></span>

### <a name="overload-list"></a><span data-ttu-id="6ffe9-106">多載清單</span><span class="sxs-lookup"><span data-stu-id="6ffe9-106">Overload list</span></span>



| <span data-ttu-id="6ffe9-107">方法</span><span class="sxs-lookup"><span data-stu-id="6ffe9-107">Method</span></span>                                                                                                                                                                                                                            | <span data-ttu-id="6ffe9-108">描述</span><span class="sxs-lookup"><span data-stu-id="6ffe9-108">Description</span></span>                                                                                            |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ffe9-109">[**CreateWicBitmapRenderTarget (IWICBitmap \* 、D2D1 \_ 轉譯 \_ 目標 \_ 屬性 \* 、ID2D1RenderTarget \* \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createwicbitmaprendertarget(iwicbitmap_constd2d1_render_target_properties_id2d1rendertarget))</span><span class="sxs-lookup"><span data-stu-id="6ffe9-109">[**CreateWicBitmapRenderTarget(IWICBitmap\*,D2D1\_RENDER\_TARGET\_PROPERTIES\*,ID2D1RenderTarget\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createwicbitmaprendertarget(iwicbitmap_constd2d1_render_target_properties_id2d1rendertarget))</span></span> | <span data-ttu-id="6ffe9-110">建立呈現至 Microsoft Windows 影像處理元件 (WIC) 點陣圖的轉譯目標。</span><span class="sxs-lookup"><span data-stu-id="6ffe9-110">Creates a render target that renders to a Microsoft Windows Imaging Component (WIC) bitmap.</span></span><br/> |
| <span data-ttu-id="6ffe9-111">[**CreateWicBitmapRenderTarget (IWICBitmap \* 、D2D1 \_ 轉譯 \_ 目標 \_ 屬性&、ID2D1RenderTarget \* \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createwicbitmaprendertarget(iwicbitmap_constd2d1_render_target_properties__id2d1rendertarget))</span><span class="sxs-lookup"><span data-stu-id="6ffe9-111">[**CreateWicBitmapRenderTarget(IWICBitmap\*,D2D1\_RENDER\_TARGET\_PROPERTIES&,ID2D1RenderTarget\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createwicbitmaprendertarget(iwicbitmap_constd2d1_render_target_properties__id2d1rendertarget))</span></span>  | <span data-ttu-id="6ffe9-112">建立呈現至 Microsoft Windows 影像處理元件 (WIC) 點陣圖的轉譯目標。</span><span class="sxs-lookup"><span data-stu-id="6ffe9-112">Creates a render target that renders to a Microsoft Windows Imaging Component (WIC) bitmap.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="6ffe9-113">備註</span><span class="sxs-lookup"><span data-stu-id="6ffe9-113">Remarks</span></span>

<span data-ttu-id="6ffe9-114">您的應用程式應該建立轉譯目標一次，並在應用程式的存留期內保存它們，或在收到 [**D2DERR \_ 重新建立 \_ 目標**](direct2d-error-codes.md) 錯誤之前保留。</span><span class="sxs-lookup"><span data-stu-id="6ffe9-114">Your application should create render targets once and hold onto them for the life of the application or until the [**D2DERR\_RECREATE\_TARGET**](direct2d-error-codes.md) error is received.</span></span> <span data-ttu-id="6ffe9-115">當您收到此錯誤時，您必須重新建立轉譯目標 (以及它所建立) 的任何資源。</span><span class="sxs-lookup"><span data-stu-id="6ffe9-115">When you receive this error, you need to recreate the render target (and any resources it created).</span></span>

<span data-ttu-id="6ffe9-116">**注意**   Windows Phone 上不支援此方法，而且在裝置上呼叫時將會失敗，並出現錯誤碼 0x8899000b ( 此作業 ) 沒有硬體轉譯裝置可用。</span><span class="sxs-lookup"><span data-stu-id="6ffe9-116">**Note**   This method isn't supported on Windows Phone and will fail when called on a device with error code 0x8899000b ( There is no hardware rendering device available for this operation ).</span></span> <span data-ttu-id="6ffe9-117">因為 Windows Phone 模擬器支援變形轉譯，所以在模擬器上使用不同的錯誤碼（0x88982f80 (wincodec \_ err unsupporteDPIxelformat) ）呼叫時，這個方法將會失敗 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6ffe9-117">Because the Windows Phone Emulator supports WARP rendering, this method will fail when called on the emulator with a different error code, 0x88982f80 (wincodec\_err\_unsupportedpixelformat).</span></span>

## <a name="requirements"></a><span data-ttu-id="6ffe9-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="6ffe9-118">Requirements</span></span>



| <span data-ttu-id="6ffe9-119">需求</span><span class="sxs-lookup"><span data-stu-id="6ffe9-119">Requirement</span></span> | <span data-ttu-id="6ffe9-120">值</span><span class="sxs-lookup"><span data-stu-id="6ffe9-120">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6ffe9-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="6ffe9-121">Library</span></span><br/> | <dl> <span data-ttu-id="6ffe9-122"><dt>D2d1 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="6ffe9-122"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="6ffe9-123">DLL</span><span class="sxs-lookup"><span data-stu-id="6ffe9-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="6ffe9-124"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ffe9-124"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ffe9-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6ffe9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ffe9-126">**ID2D1Factory**</span><span class="sxs-lookup"><span data-stu-id="6ffe9-126">**ID2D1Factory**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)
</dt> </dl>

 

