---
title: IDWriteTextLayout GetOverhangMetrics 方法
description: 傳回配置的 Dip) 中的 overhangs (，以及其中包含的所有物件，包括文字字元和内嵌物件。
ms.assetid: 4b23f6c5-cacc-41e2-8934-6f95208b999a
keywords:
- GetOverhangMetrics 方法直接寫入
- GetOverhangMetrics 方法 Direct Write，IDWriteTextLayout 介面
- IDWriteTextLayout 介面 Direct Write，GetOverhangMetrics 方法
topic_type:
- apiref
api_name:
- IDWriteTextLayout.GetOverhangMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d8a015998f0a673a310319f93d8f4892dd4b1c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977719"
---
# <a name="idwritetextlayoutgetoverhangmetrics-method"></a><span data-ttu-id="917bc-106">IDWriteTextLayout：： GetOverhangMetrics 方法</span><span class="sxs-lookup"><span data-stu-id="917bc-106">IDWriteTextLayout::GetOverhangMetrics method</span></span>

<span data-ttu-id="917bc-107">傳回配置的 Dip) 中的 overhangs (，以及其中包含的所有物件，包括文字字元和内嵌物件。</span><span class="sxs-lookup"><span data-stu-id="917bc-107">Returns the overhangs (in DIPs) of the layout and all objects contained in it, including text glyphs and inline objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="917bc-108">語法</span><span class="sxs-lookup"><span data-stu-id="917bc-108">Syntax</span></span>


```C++
virtual HRESULT GetOverhangMetrics(
  [out] DWRITE_OVERHANG_METRICS *overhangs
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="917bc-109">參數</span><span class="sxs-lookup"><span data-stu-id="917bc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="917bc-110">*overhangs* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="917bc-110">*overhangs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="917bc-111">類型： **[ **DWRITE \_ 懸垂 \_ 計量**](/windows/win32/api/dwrite/ns-dwrite-dwrite_overhang_metrics)\***</span><span class="sxs-lookup"><span data-stu-id="917bc-111">Type: **[**DWRITE\_OVERHANG\_METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_overhang_metrics)\***</span></span>

<span data-ttu-id="917bc-112">越過可見範圍 (在版面配置之外的 Dip) 中。</span><span class="sxs-lookup"><span data-stu-id="917bc-112">Overshoots of visible extents (in DIPs) outside the layout.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="917bc-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="917bc-113">Return value</span></span>

<span data-ttu-id="917bc-114">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="917bc-114">Type: **HRESULT**</span></span>

<span data-ttu-id="917bc-115">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="917bc-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="917bc-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="917bc-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="917bc-117">備註</span><span class="sxs-lookup"><span data-stu-id="917bc-117">Remarks</span></span>

<span data-ttu-id="917bc-118">底線和 strikethroughs 不會對黑色方塊的決定造成影響，因為轉譯器實際上會繪製這些轉譯器，而這些轉譯器實際上是以各種不同的樣式來繪製它們。</span><span class="sxs-lookup"><span data-stu-id="917bc-118">Underlines and strikethroughs do not contribute to the black box determination, since these are actually drawn by the renderer, which is allowed to draw them in any variety of styles.</span></span>

## <a name="requirements"></a><span data-ttu-id="917bc-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="917bc-119">Requirements</span></span>



| <span data-ttu-id="917bc-120">需求</span><span class="sxs-lookup"><span data-stu-id="917bc-120">Requirement</span></span> | <span data-ttu-id="917bc-121">值</span><span class="sxs-lookup"><span data-stu-id="917bc-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="917bc-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="917bc-122">Library</span></span><br/> | <dl> <span data-ttu-id="917bc-123"><dt>Dwrite .lib</dt></span><span class="sxs-lookup"><span data-stu-id="917bc-123"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="917bc-124">DLL</span><span class="sxs-lookup"><span data-stu-id="917bc-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="917bc-125"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="917bc-125"><dt>Dwrite.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="917bc-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="917bc-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="917bc-127">**IDWriteTextLayout**</span><span class="sxs-lookup"><span data-stu-id="917bc-127">**IDWriteTextLayout**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> <dt>

[<span data-ttu-id="917bc-128">**IDWriteTextLayout**</span><span class="sxs-lookup"><span data-stu-id="917bc-128">**IDWriteTextLayout**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> </dl>

 

