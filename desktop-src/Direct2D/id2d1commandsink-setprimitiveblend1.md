---
title: ID2D1CommandSink1 SetPrimitiveBlend1 方法
description: 設定新的基本 blend 模式。
ms.assetid: 3EA9EC07-1B2F-48A2-ABFB-2DA0E2EFFBF4
keywords:
- SetPrimitiveBlend1 方法 Direct2D
- SetPrimitiveBlend1 方法 Direct2D、ID2D1CommandSink1 介面
- ID2D1CommandSink1 介面 Direct2D，SetPrimitiveBlend1 方法
topic_type:
- apiref
api_name:
- ID2D1CommandSink1.SetPrimitiveBlend1
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b3aa961eec873cc84e5b34ce41279c09f580e63d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094495"
---
# <a name="id2d1commandsink1setprimitiveblend1-method"></a><span data-ttu-id="6445a-106">ID2D1CommandSink1：： SetPrimitiveBlend1 方法</span><span class="sxs-lookup"><span data-stu-id="6445a-106">ID2D1CommandSink1::SetPrimitiveBlend1 method</span></span>

<span data-ttu-id="6445a-107">設定新的基本 blend 模式。</span><span class="sxs-lookup"><span data-stu-id="6445a-107">Sets a new primitive blend mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="6445a-108">語法</span><span class="sxs-lookup"><span data-stu-id="6445a-108">Syntax</span></span>


```C++
HRESULT SetPrimitiveBlend1(
   D2D1_PRIMITIVE_BLEND primitiveBlend
);
```



## <a name="parameters"></a><span data-ttu-id="6445a-109">參數</span><span class="sxs-lookup"><span data-stu-id="6445a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6445a-110">*primitiveBlend*</span><span class="sxs-lookup"><span data-stu-id="6445a-110">*primitiveBlend*</span></span> 
</dt> <dd>

<span data-ttu-id="6445a-111">類型： **[ **D2D1 \_ 基本 \_ BLEND**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend)**</span><span class="sxs-lookup"><span data-stu-id="6445a-111">Type: **[**D2D1\_PRIMITIVE\_BLEND**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend)**</span></span>

<span data-ttu-id="6445a-112">將套用至後續基本專案的基本 blend。</span><span class="sxs-lookup"><span data-stu-id="6445a-112">The primitive blend that will apply to subsequent primitives.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6445a-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="6445a-113">Return value</span></span>

<span data-ttu-id="6445a-114">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6445a-114">Type: **HRESULT**</span></span>

<span data-ttu-id="6445a-115">如果方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="6445a-115">If the method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6445a-116">如果失敗，則會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="6445a-116">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6445a-117">備註</span><span class="sxs-lookup"><span data-stu-id="6445a-117">Remarks</span></span>

### <a name="blend-modes"></a><span data-ttu-id="6445a-118">Blend 模式</span><span class="sxs-lookup"><span data-stu-id="6445a-118">Blend modes</span></span>

<span data-ttu-id="6445a-119">針對別名轉譯 (除了 MIN 模式) 之外，輸出值 O 是以線性方式將值 *blend (S，D)* 與目的地圖元值（根據原始物件涵蓋目的圖元的數量）來計算。</span><span class="sxs-lookup"><span data-stu-id="6445a-119">For aliased rendering (except for MIN mode), the output value O is computed by linearly interpolating the value *blend(S, D)* with the destination pixel value, based on the amount that the primitive covers the destination pixel.</span></span>

<span data-ttu-id="6445a-120">下表顯示別名和反鋸齒混合的基本 blend 模式。</span><span class="sxs-lookup"><span data-stu-id="6445a-120">The table here shows the primitive blend modes for both aliased and antialiased blending.</span></span> <span data-ttu-id="6445a-121">表格中所列的方能使用下列元素：</span><span class="sxs-lookup"><span data-stu-id="6445a-121">The equations listed in the table use these elements:</span></span>

-   <span data-ttu-id="6445a-122">O = 輸出</span><span class="sxs-lookup"><span data-stu-id="6445a-122">O = Output</span></span>
-   <span data-ttu-id="6445a-123">S = 來源</span><span class="sxs-lookup"><span data-stu-id="6445a-123">S = Source</span></span>
-   <span data-ttu-id="6445a-124">SA = 來源 Alpha</span><span class="sxs-lookup"><span data-stu-id="6445a-124">SA = Source Alpha</span></span>
-   <span data-ttu-id="6445a-125">D = 目的地</span><span class="sxs-lookup"><span data-stu-id="6445a-125">D = Destination</span></span>
-   <span data-ttu-id="6445a-126">DA = 目的地 Alpha</span><span class="sxs-lookup"><span data-stu-id="6445a-126">DA = Destination Alpha</span></span>
-   <span data-ttu-id="6445a-127">C = 圖元涵蓋範圍</span><span class="sxs-lookup"><span data-stu-id="6445a-127">C = Pixel coverage</span></span>



| <span data-ttu-id="6445a-128">基本 blend 模式</span><span class="sxs-lookup"><span data-stu-id="6445a-128">Primitive blend mode</span></span>                 | <span data-ttu-id="6445a-129">鋸齒混合</span><span class="sxs-lookup"><span data-stu-id="6445a-129">Aliased blending</span></span>                            | <span data-ttu-id="6445a-130">反鋸齒混合</span><span class="sxs-lookup"><span data-stu-id="6445a-130">Antialiased blending</span></span>            | <span data-ttu-id="6445a-131">Description</span><span class="sxs-lookup"><span data-stu-id="6445a-131">Description</span></span>                                                                                                              |
|--------------------------------------|---------------------------------------------|---------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6445a-132">D2D1 \_ 基本 \_ BLEND \_ 來源 \_</span><span class="sxs-lookup"><span data-stu-id="6445a-132">D2D1\_PRIMITIVE\_BLEND\_SOURCE\_OVER</span></span> | <span data-ttu-id="6445a-133">O = (S + (1 SA) \* D) \* C + D \* (1 C) </span><span class="sxs-lookup"><span data-stu-id="6445a-133">O = (S + (1   SA) \* D) \* C + D \* (1   C)</span></span> | <span data-ttu-id="6445a-134">O = S \* C + D \* (1 SA \* C) </span><span class="sxs-lookup"><span data-stu-id="6445a-134">O = S \* C + D \*(1   SA \*C)</span></span>   | <span data-ttu-id="6445a-135">標準來源 over 目的地 blend 模式。</span><span class="sxs-lookup"><span data-stu-id="6445a-135">The standard source-over-destination blend mode.</span></span>                                                                         |
| <span data-ttu-id="6445a-136">D2D1 \_ 基本 \_ BLEND \_ 複製</span><span class="sxs-lookup"><span data-stu-id="6445a-136">D2D1\_PRIMITIVE\_BLEND\_COPY</span></span>         | <span data-ttu-id="6445a-137">O = S \* C + D \* (1 C) </span><span class="sxs-lookup"><span data-stu-id="6445a-137">O = S \* C + D \* (1   C)</span></span>                   | <span data-ttu-id="6445a-138">O = S \* C + D \* (1 C) </span><span class="sxs-lookup"><span data-stu-id="6445a-138">O = S \* C + D \* (1   C)</span></span>       | <span data-ttu-id="6445a-139">來源會複製到目的地;系統會忽略目的地圖元。</span><span class="sxs-lookup"><span data-stu-id="6445a-139">The source is copied to the destination; the destination pixels are ignored.</span></span>                                             |
| <span data-ttu-id="6445a-140">D2D1 \_ 基本 \_ BLEND \_ 分鐘</span><span class="sxs-lookup"><span data-stu-id="6445a-140">D2D1\_PRIMITIVE\_BLEND\_MIN</span></span>          | <span data-ttu-id="6445a-141">O = Min (S + 1-SA，D) </span><span class="sxs-lookup"><span data-stu-id="6445a-141">O = Min(S + 1-SA, D)</span></span>                        | <span data-ttu-id="6445a-142">O = Min (S \* c + 1 SA \* c，D) </span><span class="sxs-lookup"><span data-stu-id="6445a-142">O = Min(S \* C + 1   SA \*C, D)</span></span> | <span data-ttu-id="6445a-143">產生的圖元值會使用來源和目的地圖元值的最小值。</span><span class="sxs-lookup"><span data-stu-id="6445a-143">The resulting pixel values use the minimum of the source and destination pixel values.</span></span> <span data-ttu-id="6445a-144">在 Windows 8 和更新版本中提供。</span><span class="sxs-lookup"><span data-stu-id="6445a-144">Available in Windows 8 and later.</span></span> |
| <span data-ttu-id="6445a-145">D2D1 \_ 基本 \_ BLEND \_ 新增</span><span class="sxs-lookup"><span data-stu-id="6445a-145">D2D1\_PRIMITIVE\_BLEND\_ADD</span></span>          | <span data-ttu-id="6445a-146">O = (S + D) \* c + D \* (1 C) </span><span class="sxs-lookup"><span data-stu-id="6445a-146">O = (S + D) \* C + D \* (1   C)</span></span>             | <span data-ttu-id="6445a-147">O = S \* C + D</span><span class="sxs-lookup"><span data-stu-id="6445a-147">O = S \* C + D</span></span>                  | <span data-ttu-id="6445a-148">產生的圖元值是來源和目的地圖元值的總和。</span><span class="sxs-lookup"><span data-stu-id="6445a-148">The resulting pixel values are the sum of the source and destination pixel values.</span></span> <span data-ttu-id="6445a-149">在 Windows 8 和更新版本中提供。</span><span class="sxs-lookup"><span data-stu-id="6445a-149">Available in Windows 8 and later.</span></span>     |



 

![以不同的不透明度和背景 direct2d 基本 blend 模式的圖例。](images/primblenddemo.png)

<span data-ttu-id="6445a-151">具有不同透明度和背景的基本 blend 模式圖例。</span><span class="sxs-lookup"><span data-stu-id="6445a-151">An illustration of the primitive blend modes with varying opacity and backgrounds.</span></span>

<span data-ttu-id="6445a-152">除非使用 [**DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)) API 上的 *compositeMode* 參數來覆寫此基本 blend，否則基本 blend 會套用至內容上繪製的所有基本型別。</span><span class="sxs-lookup"><span data-stu-id="6445a-152">The primitive blend will apply to all of the primitive drawn on the context, unless this is overridden with the *compositeMode* parameter on the [**DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)) API.</span></span>

<span data-ttu-id="6445a-153">基本 blend 適用于在內容上繪製之任何基本專案的內部。</span><span class="sxs-lookup"><span data-stu-id="6445a-153">The primitive blend applies to the interior of any primitives drawn on the context.</span></span> <span data-ttu-id="6445a-154">在 [**DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode))的案例中，這將由影像矩形、位移和世界轉換來隱含。</span><span class="sxs-lookup"><span data-stu-id="6445a-154">In the case of [**DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)), this will be implied by the image rectangle, offset and world transform.</span></span>

<span data-ttu-id="6445a-155">如果基本 blend 是 **D2D1 \_ 基本 \_ blend \_** 以外的任何物件，則 ClearType 轉譯將會關閉。</span><span class="sxs-lookup"><span data-stu-id="6445a-155">If the primitive blend is anything other than **D2D1\_PRIMITIVE\_BLEND\_OVER** then ClearType rendering will be turned off.</span></span> <span data-ttu-id="6445a-156">如果應用程式在這些模式中明確強制執行 ClearType 轉譯，則繪製內容會處於錯誤狀態。</span><span class="sxs-lookup"><span data-stu-id="6445a-156">If the application explicitly forces ClearType rendering in these modes, the drawing context will be placed in an error state.</span></span> <span data-ttu-id="6445a-157">\_ \_ [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw)或 [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush)會傳回 D2DERR 錯誤的狀態。</span><span class="sxs-lookup"><span data-stu-id="6445a-157">D2DERR\_WRONG\_STATE will be returned from either [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) or [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush).</span></span>

## <a name="requirements"></a><span data-ttu-id="6445a-158">規格需求</span><span class="sxs-lookup"><span data-stu-id="6445a-158">Requirements</span></span>



| <span data-ttu-id="6445a-159">需求</span><span class="sxs-lookup"><span data-stu-id="6445a-159">Requirement</span></span> | <span data-ttu-id="6445a-160">值</span><span class="sxs-lookup"><span data-stu-id="6445a-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6445a-161">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6445a-161">Minimum supported client</span></span><br/> | <span data-ttu-id="6445a-162">Windows 8.1 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6445a-162">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="6445a-163">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6445a-163">Minimum supported server</span></span><br/> | <span data-ttu-id="6445a-164">Windows Server 2012 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6445a-164">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="6445a-165">支援的最小電話</span><span class="sxs-lookup"><span data-stu-id="6445a-165">Minimum supported phone</span></span><br/>  | <span data-ttu-id="6445a-166">Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 和 Windows 執行階段應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6445a-166">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6445a-167">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6445a-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6445a-168">**ID2D1CommandSink1**</span><span class="sxs-lookup"><span data-stu-id="6445a-168">**ID2D1CommandSink1**</span></span>](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1commandsink1)
</dt> </dl>

 

