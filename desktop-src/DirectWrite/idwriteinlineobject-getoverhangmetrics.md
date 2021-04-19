---
title: IDWriteInlineObject GetOverhangMetrics 方法
description: IDWriteTextLayout 會呼叫這個回呼函式，以取得内嵌物件的 Dip)  (可見的範圍。 如果是簡單點陣圖，沒有填補且沒有任何懸垂，則所有 overhangs 只會是零。
ms.assetid: b3b3e9f0-ee35-4117-9a62-a975c03b5ca9
keywords:
- GetOverhangMetrics 方法直接寫入
- GetOverhangMetrics 方法 Direct Write，IDWriteInlineObject 介面
- IDWriteInlineObject 介面 Direct Write，GetOverhangMetrics 方法
topic_type:
- apiref
api_name:
- IDWriteInlineObject.GetOverhangMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a0960f28394c5b55c3377136451a5c13748edc1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990697"
---
# <a name="idwriteinlineobjectgetoverhangmetrics-method"></a><span data-ttu-id="cf072-107">IDWriteInlineObject：： GetOverhangMetrics 方法</span><span class="sxs-lookup"><span data-stu-id="cf072-107">IDWriteInlineObject::GetOverhangMetrics method</span></span>

<span data-ttu-id="cf072-108">[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) 會呼叫這個回呼函式，以取得内嵌物件的 dip)  (可見的範圍。</span><span class="sxs-lookup"><span data-stu-id="cf072-108">[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) calls this callback function to get the visible extents (in DIPs) of the inline object.</span></span> <span data-ttu-id="cf072-109">如果是簡單點陣圖，沒有填補且沒有任何懸垂，則所有 overhangs 只會是零。</span><span class="sxs-lookup"><span data-stu-id="cf072-109">In the case of a simple bitmap, with no padding and no overhang, all the overhangs will simply be zeroes.</span></span>

<span data-ttu-id="cf072-110">Overhangs 應該會傳回相對於所報告的物件大小 (請參閱 [**DWRITE \_ 內嵌 \_ 物件 \_ 度量**](/windows/win32/api/dwrite/ns-dwrite-dwrite_inline_object_metrics)) ，而且不應該調整基準。</span><span class="sxs-lookup"><span data-stu-id="cf072-110">The overhangs should be returned relative to the reported size of the object (see [**DWRITE\_INLINE\_OBJECT\_METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_inline_object_metrics)), and should not be baseline adjusted.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf072-111">語法</span><span class="sxs-lookup"><span data-stu-id="cf072-111">Syntax</span></span>


```C++
virtual HRESULT GetOverhangMetrics(
  [out] DWRITE_OVERHANG_METRICS *overhangs
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="cf072-112">參數</span><span class="sxs-lookup"><span data-stu-id="cf072-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf072-113">*overhangs* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="cf072-113">*overhangs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cf072-114">類型： **[ **DWRITE \_ 懸垂 \_ 計量**](/windows/win32/api/dwrite/ns-dwrite-dwrite_overhang_metrics)\***</span><span class="sxs-lookup"><span data-stu-id="cf072-114">Type: **[**DWRITE\_OVERHANG\_METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_overhang_metrics)\***</span></span>

<span data-ttu-id="cf072-115">超過可見範圍 (在物件外部的 Dip) 中。</span><span class="sxs-lookup"><span data-stu-id="cf072-115">Overshoot of visible extents (in DIPs) outside the object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf072-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="cf072-116">Return value</span></span>

<span data-ttu-id="cf072-117">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="cf072-117">Type: **HRESULT**</span></span>

<span data-ttu-id="cf072-118">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="cf072-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cf072-119">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="cf072-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf072-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="cf072-120">Requirements</span></span>



| <span data-ttu-id="cf072-121">需求</span><span class="sxs-lookup"><span data-stu-id="cf072-121">Requirement</span></span> | <span data-ttu-id="cf072-122">值</span><span class="sxs-lookup"><span data-stu-id="cf072-122">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cf072-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="cf072-123">Library</span></span><br/> | <dl> <span data-ttu-id="cf072-124"><dt>Dwrite .lib</dt></span><span class="sxs-lookup"><span data-stu-id="cf072-124"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="cf072-125">DLL</span><span class="sxs-lookup"><span data-stu-id="cf072-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="cf072-126"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf072-126"><dt>Dwrite.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf072-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cf072-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf072-128">**IDWriteInlineObject**</span><span class="sxs-lookup"><span data-stu-id="cf072-128">**IDWriteInlineObject**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject)
</dt> <dt>

[<span data-ttu-id="cf072-129">**IDWriteInlineObject**</span><span class="sxs-lookup"><span data-stu-id="cf072-129">**IDWriteInlineObject**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject)
</dt> </dl>

 

