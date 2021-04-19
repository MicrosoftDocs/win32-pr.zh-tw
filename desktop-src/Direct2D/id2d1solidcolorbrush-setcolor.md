---
title: ID2D1SolidColorBrush SetColor 方法
description: 指定此單色筆刷的色彩。
ms.assetid: 2900bf72-9641-419c-b0d7-334f14f8a474
keywords:
- SetColor 方法 Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 580778135e840a69342ff34ffd8e415883317517
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987888"
---
# <a name="id2d1solidcolorbrushsetcolor-methods"></a><span data-ttu-id="8c624-104">ID2D1SolidColorBrush：： SetColor 方法</span><span class="sxs-lookup"><span data-stu-id="8c624-104">ID2D1SolidColorBrush::SetColor methods</span></span>

<span data-ttu-id="8c624-105">指定此單色筆刷的色彩。</span><span class="sxs-lookup"><span data-stu-id="8c624-105">Specifies the color of this solid color brush.</span></span>

### <a name="overload-list"></a><span data-ttu-id="8c624-106">多載清單</span><span class="sxs-lookup"><span data-stu-id="8c624-106">Overload list</span></span>



| <span data-ttu-id="8c624-107">方法</span><span class="sxs-lookup"><span data-stu-id="8c624-107">Method</span></span>                                                                          | <span data-ttu-id="8c624-108">描述</span><span class="sxs-lookup"><span data-stu-id="8c624-108">Description</span></span>                                                |
|:--------------------------------------------------------------------------------|:-----------------------------------------------------------|
| <span data-ttu-id="8c624-109">[**SetColor (D2D1 \_ COLOR \_ F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1solidcolorbrush-setcolor(constd2d1_color_f_))</span><span class="sxs-lookup"><span data-stu-id="8c624-109">[**SetColor(D2D1\_COLOR\_F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1solidcolorbrush-setcolor(constd2d1_color_f_))</span></span>  | <span data-ttu-id="8c624-110">指定此單色筆刷的色彩。</span><span class="sxs-lookup"><span data-stu-id="8c624-110">Specifies the color of this solid-color brush.</span></span> <br/> |
| <span data-ttu-id="8c624-111">[**SetColor (D2D1 \_ COLOR \_ F \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1solidcolorbrush-setcolor(constd2d1_color_f))</span><span class="sxs-lookup"><span data-stu-id="8c624-111">[**SetColor(D2D1\_COLOR\_F\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1solidcolorbrush-setcolor(constd2d1_color_f))</span></span> | <span data-ttu-id="8c624-112">指定此單色筆刷的色彩。</span><span class="sxs-lookup"><span data-stu-id="8c624-112">Specifies the color of this solid color brush.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="8c624-113">備註</span><span class="sxs-lookup"><span data-stu-id="8c624-113">Remarks</span></span>

<span data-ttu-id="8c624-114">Direct2D 提供 [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) 類別，以協助建立色彩。</span><span class="sxs-lookup"><span data-stu-id="8c624-114">To help create colors, Direct2D provides the [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) class.</span></span> <span data-ttu-id="8c624-115">它提供數個 helper 方法來建立色彩，並提供一組或預先定義的色彩。</span><span class="sxs-lookup"><span data-stu-id="8c624-115">It offers several helper methods for creating colors and provides a set or predefined colors.</span></span>

## <a name="examples"></a><span data-ttu-id="8c624-116">範例</span><span class="sxs-lookup"><span data-stu-id="8c624-116">Examples</span></span>

<span data-ttu-id="8c624-117">下列程式碼示範如何使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="8c624-117">The following code shows how to use this method.</span></span>


```C++
        m_pSolidColorBrush->SetColor(
            D2D1::ColorF(
                0.0f,
                intensity,
                1.0f - intensity
                ));

        hr = m_pRealization->Fill(
                m_pRT,
                m_pSolidColorBrush,
                m_useRealizations ?
                    REALIZATION_RENDER_MODE_DEFAULT :
                    REALIZATION_RENDER_MODE_FORCE_UNREALIZED
                );
```



## <a name="requirements"></a><span data-ttu-id="8c624-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="8c624-118">Requirements</span></span>



| <span data-ttu-id="8c624-119">需求</span><span class="sxs-lookup"><span data-stu-id="8c624-119">Requirement</span></span> | <span data-ttu-id="8c624-120">值</span><span class="sxs-lookup"><span data-stu-id="8c624-120">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8c624-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="8c624-121">Library</span></span><br/> | <dl> <span data-ttu-id="8c624-122"><dt>D2d1 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="8c624-122"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="8c624-123">DLL</span><span class="sxs-lookup"><span data-stu-id="8c624-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="8c624-124"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c624-124"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c624-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8c624-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c624-126">**ID2D1SolidColorBrush**</span><span class="sxs-lookup"><span data-stu-id="8c624-126">**ID2D1SolidColorBrush**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)
</dt> </dl>

 

