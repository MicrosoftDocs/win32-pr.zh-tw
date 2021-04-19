---
title: 'D2D1_COLOR_F (D2DBaseTypes) '
description: '描述色彩的紅色、綠色、藍色和 Alpha 元件。 |D2D1_COLOR_F (D2DBaseTypes) '
ms.assetid: 564d4f41-2da7-49ed-b85a-d1070d662b40
keywords:
- D2D1_COLOR_F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78f12c4c833d7f73946b2309673dff8f3dd11395
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106991956"
---
# <a name="d2d1_color_f"></a><span data-ttu-id="57048-105">D2D1 \_ 色彩 \_ F</span><span class="sxs-lookup"><span data-stu-id="57048-105">D2D1\_COLOR\_F</span></span>

<span data-ttu-id="57048-106">描述色彩的紅色、綠色、藍色和 Alpha 元件。</span><span class="sxs-lookup"><span data-stu-id="57048-106">Describes the red, green, blue, and alpha components of a color.</span></span>


```C++
typedef D2D_COLOR_F D2D1_COLOR_F;
```



## <a name="remarks"></a><span data-ttu-id="57048-107">備註</span><span class="sxs-lookup"><span data-stu-id="57048-107">Remarks</span></span>

<span data-ttu-id="57048-108">**D2D1 \_\_F** 色是 [**D2D \_ 色 \_ f**](d2d-color-f.md)的 typedef，它本身是 [D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md)的 typedef。</span><span class="sxs-lookup"><span data-stu-id="57048-108">**D2D1\_COLOR\_F** is a typedef for [**D2D\_COLOR\_F**](d2d-color-f.md), which is itself a typedef for [D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md).</span></span> <span data-ttu-id="57048-109">如需 **D2D1 \_ COLOR \_ F** 所提供成員的詳細資訊，請參閱 [D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md)。</span><span class="sxs-lookup"><span data-stu-id="57048-109">For information about the members provided by **D2D1\_COLOR\_F**, see [D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md).</span></span>

<span data-ttu-id="57048-110">[**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf)類別會提供一組預先定義的色彩，以及用來定義色彩的 helper 函數。</span><span class="sxs-lookup"><span data-stu-id="57048-110">The [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) class provides a set of predefined colors and helper functions for defining colors.</span></span> <span data-ttu-id="57048-111">如需詳細資訊，請參閱 [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) 參考。</span><span class="sxs-lookup"><span data-stu-id="57048-111">For more information, see the [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) reference.</span></span>

## <a name="examples"></a><span data-ttu-id="57048-112">範例</span><span class="sxs-lookup"><span data-stu-id="57048-112">Examples</span></span>

<span data-ttu-id="57048-113">下列範例會使用 [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) 類別，在建立 [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)時，指定 (黑色) 預先定義的色彩。</span><span class="sxs-lookup"><span data-stu-id="57048-113">The following example uses the [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) class to specify a predefined color (black) when creating an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush).</span></span>


```C++
hr = m_pRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF::Black, 1.0f),
    &m_pBlackBrush
    );
```



<span data-ttu-id="57048-114">下列範例會使用 [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) 類別來指定使用紅色、綠色、藍色和 Alpha 值的色彩。</span><span class="sxs-lookup"><span data-stu-id="57048-114">The following example uses the [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) class to specify a color using red, green, blue, and alpha values.</span></span>


```C++
ID2D1SolidColorBrush *pGridBrush = NULL;
hr = pCompatibleRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF(0.93f, 0.94f, 0.96f, 1.0f)),
    &pGridBrush
    );
```



## <a name="requirements"></a><span data-ttu-id="57048-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="57048-115">Requirements</span></span>



| <span data-ttu-id="57048-116">需求</span><span class="sxs-lookup"><span data-stu-id="57048-116">Requirement</span></span> | <span data-ttu-id="57048-117">值</span><span class="sxs-lookup"><span data-stu-id="57048-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57048-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="57048-118">Minimum supported client</span></span><br/> | <span data-ttu-id="57048-119">Windows 7、windows Vista （含 SP2）和平臺更新（適用于 Windows Vista \[ 桌面應用程式 \| UWP 應用程式）\]</span><span class="sxs-lookup"><span data-stu-id="57048-119">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="57048-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="57048-120">Minimum supported server</span></span><br/> | <span data-ttu-id="57048-121">Windows server 2008 R2、Windows Server 2008 SP2 和 Windows Server 的平臺更新 2008 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="57048-121">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="57048-122">支援的最小電話</span><span class="sxs-lookup"><span data-stu-id="57048-122">Minimum supported phone</span></span><br/>  | <span data-ttu-id="57048-123">Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 和 Windows 執行階段應用程式\]</span><span class="sxs-lookup"><span data-stu-id="57048-123">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="57048-124">標頭</span><span class="sxs-lookup"><span data-stu-id="57048-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="57048-125"><dt>D2DBaseTypes (包含 D2d1) </dt></span><span class="sxs-lookup"><span data-stu-id="57048-125"><dt>D2DBaseTypes.h (include D2d1.h)</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="57048-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="57048-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57048-127">D3DCOLORVALUE</span><span class="sxs-lookup"><span data-stu-id="57048-127">D3DCOLORVALUE</span></span>](../direct3d9/d3dcolorvalue.md)
</dt> <dt>

[<span data-ttu-id="57048-128">**ColorF**</span><span class="sxs-lookup"><span data-stu-id="57048-128">**ColorF**</span></span>](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf)
</dt> </dl>

 

