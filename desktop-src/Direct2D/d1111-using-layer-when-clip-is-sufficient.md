---
title: 當剪輯足夠時使用圖層 D1111
ms.assetid: 07fe3c66-15be-408b-a30b-a7f52919c058
description: 正在搭配 Null 不透明度遮罩、1.0 不透明度和軸對齊矩形幾何遮罩來使用圖層。 推送/Pop 剪輯 API 應該以更高的效能達成相同的結果。
keywords:
- 當剪輯足夠 Direct2D 時使用圖層 D1111
topic_type:
- apiref
api_name:
- D1111 Using Layer When Clip Is Sufficient
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: e8463cc3940b69e326f13df6be9602dd6073fec0
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549903"
---
# <a name="d1111-using-layer-when-clip-is-sufficient"></a><span data-ttu-id="b08be-105">D1111：當剪輯足夠時使用圖層</span><span class="sxs-lookup"><span data-stu-id="b08be-105">D1111: Using Layer When Clip Is Sufficient</span></span>

<span data-ttu-id="b08be-106">效能-正在搭配 **Null** 不透明度遮罩、1.0 不透明度和軸對齊矩形幾何遮罩使用層。</span><span class="sxs-lookup"><span data-stu-id="b08be-106">PERF - A layer is being used with a **NULL** opacity mask, 1.0 opacity, and an axis aligned rectangular geometric mask.</span></span> <span data-ttu-id="b08be-107">推送/Pop 剪輯 API 應該以更高的效能達成相同的結果。</span><span class="sxs-lookup"><span data-stu-id="b08be-107">The Push/Pop Clip API should achieve the same results with higher performance.</span></span>

## <a name="placeholders"></a><span data-ttu-id="b08be-108">預留位置</span><span class="sxs-lookup"><span data-stu-id="b08be-108">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="b08be-109"><span id="interface"></span><span id="INTERFACE"></span>*介面*</span><span class="sxs-lookup"><span data-stu-id="b08be-109"><span id="interface"></span><span id="INTERFACE"></span>*interface*</span></span>
</dt> <dd>

<span data-ttu-id="b08be-110">介面的位址。</span><span class="sxs-lookup"><span data-stu-id="b08be-110">The address of the interface.</span></span>

</dd> </dl> 

| &nbsp;      |    &nbsp;   |
|-------------|-------------|
| <span data-ttu-id="b08be-111">錯誤層級</span><span class="sxs-lookup"><span data-stu-id="b08be-111">Error Level</span></span> | <span data-ttu-id="b08be-112">資訊</span><span class="sxs-lookup"><span data-stu-id="b08be-112">Information</span></span> |



 

## <a name="examples"></a><span data-ttu-id="b08be-113">範例</span><span class="sxs-lookup"><span data-stu-id="b08be-113">Examples</span></span>

<span data-ttu-id="b08be-114">下列程式碼會在圖層僅包含一個基本 (矩形) ，而且 [**D2D1 \_ 圖層 \_ 參數**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters)結構的欄位設定為預設值時使用 [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer))和 [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) 。</span><span class="sxs-lookup"><span data-stu-id="b08be-114">The following code uses the [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) and [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) when the layer contains only one primitive (a rectangle) and the fields of the [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) structure are set to defaults.</span></span> <span data-ttu-id="b08be-115">如需 **D2D1 \_ 圖層 \_ 參數** 結構的預設值，請參閱 [**LayerParameter**](/windows/desktop/api/d2d1helper/nf-d2d1helper-layerparameters)。</span><span class="sxs-lookup"><span data-stu-id="b08be-115">For the default values of the **D2D1\_LAYER\_PARAMETERS** structure, see [**LayerParameter**](/windows/desktop/api/d2d1helper/nf-d2d1helper-layerparameters).</span></span>


```C++
        ID2D1Layer *m_pLayer;

        hr = m_pRenderTarget->CreateLayer(D2D1::SizeF(100, 100), &m_pLayer);
        m_pRenderTarget->PushLayer(D2D1::LayerParameters(), m_pLayer);
        m_pRenderTarget->FillRectangle(D2D1::RectF(100, 50, 400, 160), m_pBlackBrush);
        m_pRenderTarget->PopLayer();
```



<span data-ttu-id="b08be-116">此範例會產生下列 debug 訊息：</span><span class="sxs-lookup"><span data-stu-id="b08be-116">This example produces the following debug message:</span></span>

``` syntax
DEBUG INFO - PERF - A layer is being used with a NULL opacity mask, 1.0 opacity, 
            and an axis aligned rectangular geometric mask.  
            The Push/Pop Clip API should achieve the same results with higher performance.
```

## <a name="possible-causes"></a><span data-ttu-id="b08be-117">可能的原因</span><span class="sxs-lookup"><span data-stu-id="b08be-117">Possible Causes</span></span>

<span data-ttu-id="b08be-118">[**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode))和 [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip)方法有 sufficed 時，會使用一層。</span><span class="sxs-lookup"><span data-stu-id="b08be-118">A layer was used when the [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) and [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) methods would have sufficed.</span></span>

 

 