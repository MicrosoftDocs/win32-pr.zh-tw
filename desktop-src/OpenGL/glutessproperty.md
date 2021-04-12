---
title: 'gluTessProperty 函式 (X.glu 隊) '
description: GluTessProperty 函式會設定鑲嵌式物件的屬性。
ms.assetid: 1306b9ef-4f1e-4684-99ea-464bae1d0a61
keywords:
- gluTessProperty 函式 OpenGL
topic_type:
- apiref
api_name:
- gluTessProperty
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfe21f2961cd4cb1df31a1fdb3f407a71d6e6d68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105899"
---
# <a name="glutessproperty-function"></a><span data-ttu-id="e2fe1-104">gluTessProperty 函式</span><span class="sxs-lookup"><span data-stu-id="e2fe1-104">gluTessProperty function</span></span>

<span data-ttu-id="e2fe1-105">**GluTessProperty** 函式會設定鑲嵌式物件的屬性。</span><span class="sxs-lookup"><span data-stu-id="e2fe1-105">The **gluTessProperty** function sets the property of a tessellation object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2fe1-106">語法</span><span class="sxs-lookup"><span data-stu-id="e2fe1-106">Syntax</span></span>


```C++
void WINAPI gluTessProperty(
   GLUtesselator *tess,
   GLenum        which,
   GLdouble      value
);
```



## <a name="parameters"></a><span data-ttu-id="e2fe1-107">參數</span><span class="sxs-lookup"><span data-stu-id="e2fe1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2fe1-108">*苔 絲*</span><span class="sxs-lookup"><span data-stu-id="e2fe1-108">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="e2fe1-109">使用 [**gluNewTess**](glunewtess.md)) 建立的鑲嵌式物件 (。</span><span class="sxs-lookup"><span data-stu-id="e2fe1-109">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> <dt>

<span data-ttu-id="e2fe1-110">*頻率*</span><span class="sxs-lookup"><span data-stu-id="e2fe1-110">*which*</span></span> 
</dt> <dd>

<span data-ttu-id="e2fe1-111">要設定的屬性值。</span><span class="sxs-lookup"><span data-stu-id="e2fe1-111">The property value to set.</span></span> <span data-ttu-id="e2fe1-112">下列值有效： X.GLU 隊 \_ TESS \_ 繞組 \_ RULE、x.glu 隊 \_ TESS \_ 界限 \_ ，以及 x.glu 隊 \_ TESS \_ 容錯。</span><span class="sxs-lookup"><span data-stu-id="e2fe1-112">The following values are valid: GLU\_TESS\_WINDING\_RULE, GLU\_TESS\_BOUNDARY\_ONLY, and GLU\_TESS\_TOLERANCE.</span></span>



| <span data-ttu-id="e2fe1-113">值</span><span class="sxs-lookup"><span data-stu-id="e2fe1-113">Value</span></span>                                                                                                                                                                                      | <span data-ttu-id="e2fe1-114">意義</span><span class="sxs-lookup"><span data-stu-id="e2fe1-114">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_TESS_WINDING_RULE"></span><span id="glu_tess_winding_rule"></span><dl> <span data-ttu-id="e2fe1-115"><dt>**X.GLU 隊 \_ TESS \_ 繞組 \_ 規則**</dt></span><span class="sxs-lookup"><span data-stu-id="e2fe1-115"><dt>**GLU\_TESS\_WINDING\_RULE**</dt></span></span> </dl>    | <span data-ttu-id="e2fe1-116">判斷多邊形的哪些部分是在內部。</span><span class="sxs-lookup"><span data-stu-id="e2fe1-116">Determines which parts of the polygon are on the interior.</span></span> <span data-ttu-id="e2fe1-117">Value 參數可以設定為下列其中一項： X.GLU 隊 \_ TESS \_ 繞組 \_ 奇數、X.glu 隊 \_ TESS \_ 繞組 \_ 非零、X.glu 隊 \_ TESS \_ 繞組 \_ 正面、X.glu 隊 \_ TESS \_ 繞組 \_ 負值或 x.glu 隊 \_ TESS \_ 繞組 \_ ABS \_ GEQ \_ 二。</span><span class="sxs-lookup"><span data-stu-id="e2fe1-117">The value parameter may be set to one of the following: GLU\_TESS\_WINDING\_ODD, GLU\_TESS\_WINDING\_NONZERO, GLU\_TESS\_WINDING\_POSITIVE, GLU\_TESS\_WINDING\_NEGATIVE, or GLU\_TESS\_WINDING\_ABS\_GEQ\_TWO.</span></span> <br/> <span data-ttu-id="e2fe1-118">若要瞭解纏繞規則的運作方式，請先考慮輸入等高線會將平面分割成區域。</span><span class="sxs-lookup"><span data-stu-id="e2fe1-118">To understand how the winding rule works, first consider that the input contours partition the plane into regions.</span></span> <span data-ttu-id="e2fe1-119">纏繞規則會決定這些區域在多邊形內的哪些區域。</span><span class="sxs-lookup"><span data-stu-id="e2fe1-119">The winding rule determines which of these regions are inside the polygon.</span></span><br/> <span data-ttu-id="e2fe1-120">若為單一輪廓 C，則點 x 的纏繞數位只是我們在 x 左右移動一次，因為我們會在 C (，其中逆時針是正面) 。</span><span class="sxs-lookup"><span data-stu-id="e2fe1-120">For a single-contour C, the winding number of a point x is simply the signed number of revolutions we make around x as we travel once around C (where counterclockwise is positive).</span></span> <span data-ttu-id="e2fe1-121">當有數個輪廓時，個別的纏繞數位會加總。</span><span class="sxs-lookup"><span data-stu-id="e2fe1-121">When there are several contours, the individual winding numbers are summed.</span></span> <span data-ttu-id="e2fe1-122">此程式會將帶正負號的整數值與平面中的每個點 x 產生關聯。</span><span class="sxs-lookup"><span data-stu-id="e2fe1-122">This procedure associates a signed integer value with each point x in the plane.</span></span> <span data-ttu-id="e2fe1-123">請注意，對單一區域中的所有點而言，繞組數位都是相同的。</span><span class="sxs-lookup"><span data-stu-id="e2fe1-123">Note that the winding number is the same for all points in a single region.</span></span><br/> <span data-ttu-id="e2fe1-124">纏繞規則會將區域分類為「內部」，如果其繞組數位屬於所選類別 (奇數、非零、正面、負數或至少有兩個) 的絕對值。</span><span class="sxs-lookup"><span data-stu-id="e2fe1-124">The winding rule classifies a region as "inside" if its winding number belongs to the chosen category (odd, nonzero, positive, negative, or absolute value of at least two).</span></span> <span data-ttu-id="e2fe1-125">之前的 X.GLU 隊鑲嵌在 X.GLU 隊1.2 之前 () 使用「奇數」規則。</span><span class="sxs-lookup"><span data-stu-id="e2fe1-125">The previous GLU tessellator (prior to GLU 1.2) used the "odd" rule.</span></span> <span data-ttu-id="e2fe1-126">「非零」規則 (X.GLU 隊 \_ TESS \_ 繞組 \_ 非零) 是定義內部的另一種常見方式。</span><span class="sxs-lookup"><span data-stu-id="e2fe1-126">The "nonzero" rule (GLU\_TESS\_WINDING\_NONZERO) is another common way to define the interior.</span></span> <span data-ttu-id="e2fe1-127">其他三個規則 (X.GLU 隊 \_ TESS \_ 繞組 \_ 正面、X.glu 隊 \_ TESS \_ 繞組 \_ 負值、X.glu 隊 \_ TESS \_ 繞組 \_ ABS \_ GEQ \_ 兩個) 適用于多邊形 CSG 作業。</span><span class="sxs-lookup"><span data-stu-id="e2fe1-127">The other three rules (GLU\_TESS\_WINDING\_POSITIVE, GLU\_TESS\_WINDING\_NEGATIVE, GLU\_TESS\_WINDING\_ABS\_GEQ\_TWO) are useful for polygon CSG operations.</span></span><br/> |
| <span id="GLU_TESS_BOUNDARY_ONLY"></span><span id="glu_tess_boundary_only"></span><dl> <span data-ttu-id="e2fe1-128"><dt>**\_ \_ 僅限 X.GLU 隊 TESS 界限 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e2fe1-128"><dt>**GLU\_TESS\_BOUNDARY\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="e2fe1-129">指定布林值 (將值設定為 GL \_ TRUE 或 gl \_ FALSE) 。</span><span class="sxs-lookup"><span data-stu-id="e2fe1-129">Specifies a Boolean value (set value to GL\_TRUE or GL\_FALSE).</span></span> <span data-ttu-id="e2fe1-130">當您將值設定為 GL \_ TRUE 時，會傳回一組用來分隔多邊形內部和外部的封閉輪廓，而不是鑲嵌式。</span><span class="sxs-lookup"><span data-stu-id="e2fe1-130">When you set value to GL\_TRUE, a set of closed contours separating the polygon interior and exterior is returned instead of a tessellation.</span></span> <span data-ttu-id="e2fe1-131">對一般而言，外部輪廓是逆時針方向;內部輪廓會順時針方向。</span><span class="sxs-lookup"><span data-stu-id="e2fe1-131">Exterior contours are oriented counterclockwise with respect to the normal; interior contours are oriented clockwise.</span></span> <span data-ttu-id="e2fe1-132">X.GLU 隊 \_ TESS \_ BEGIN 和 X.glu 隊 \_ TESS \_ begin \_ DATA 回呼會 \_ \_ 針對每個輪廓使用類型 GL 行迴圈。</span><span class="sxs-lookup"><span data-stu-id="e2fe1-132">The GLU\_TESS\_BEGIN and GLU\_TESS\_BEGIN\_DATA callbacks use the type GL\_LINE\_LOOP for each contour.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="GLU_TESS_TOLERANCE"></span><span id="glu_tess_tolerance"></span><dl> <span data-ttu-id="e2fe1-133"><dt>**X.GLU 隊 \_ TESS \_ 容忍度**</dt></span><span class="sxs-lookup"><span data-stu-id="e2fe1-133"><dt>**GLU\_TESS\_TOLERANCE**</dt></span></span> </dl>              | <span data-ttu-id="e2fe1-134">指定合併功能以縮減輸出大小的容錯。</span><span class="sxs-lookup"><span data-stu-id="e2fe1-134">Specifies a tolerance for merging features to reduce the size of the output.</span></span> <span data-ttu-id="e2fe1-135">例如，兩個非常接近的頂點可能會由單一頂點取代。</span><span class="sxs-lookup"><span data-stu-id="e2fe1-135">For example, two vertexes that are very close to each other might be replaced by a single vertex.</span></span> <span data-ttu-id="e2fe1-136">容錯會乘以任何輸入頂點的最大座標量值;這會指定任何功能在單一合併作業的結果中，可以移動的最大距離。</span><span class="sxs-lookup"><span data-stu-id="e2fe1-136">The tolerance is multiplied by the largest coordinate magnitude of any input vertex; this specifies the maximum distance that any feature can move as the result of a single merge operation.</span></span> <span data-ttu-id="e2fe1-137">如果單一功能參與數個合併作業，移動的總距離可能會更大。</span><span class="sxs-lookup"><span data-stu-id="e2fe1-137">If a single feature takes part in several merge operations, the total distance moved can be larger.</span></span> <br/> <span data-ttu-id="e2fe1-138">功能合併完全是選擇性的;容錯是唯一的提示。</span><span class="sxs-lookup"><span data-stu-id="e2fe1-138">Feature merging is completely optional; the tolerance is only a hint.</span></span> <span data-ttu-id="e2fe1-139">在某些情況下，可以免費合併執行，或永遠不會合並功能。</span><span class="sxs-lookup"><span data-stu-id="e2fe1-139">The implementation is free to merge in some cases and not in others, or to never merge features at all.</span></span> <span data-ttu-id="e2fe1-140">預設容錯值為零。</span><span class="sxs-lookup"><span data-stu-id="e2fe1-140">The default tolerance is zero.</span></span><br/> <span data-ttu-id="e2fe1-141">目前的執行只會在完全一致的情況下合併頂點，而不考慮目前的容錯。</span><span class="sxs-lookup"><span data-stu-id="e2fe1-141">The current implementation merges vertexes only if they are exactly coincident, regardless of the current tolerance.</span></span> <span data-ttu-id="e2fe1-142">只有當實作為無法區分頂點所在邊緣的一端時，才會將頂點接合至邊緣。</span><span class="sxs-lookup"><span data-stu-id="e2fe1-142">A vertex is spliced into an edge only if the implementation is unable to distinguish which side of the edge the vertex lies on.</span></span> <span data-ttu-id="e2fe1-143">只有當兩個端點都相同時，才會合並兩個邊緣。</span><span class="sxs-lookup"><span data-stu-id="e2fe1-143">Two edges are merged only when both endpoints are identical.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                 |



 

</dd> <dt>

<span data-ttu-id="e2fe1-144">*value*</span><span class="sxs-lookup"><span data-stu-id="e2fe1-144">*value*</span></span> 
</dt> <dd>

<span data-ttu-id="e2fe1-145">指定之屬性的值。</span><span class="sxs-lookup"><span data-stu-id="e2fe1-145">The value of the indicated property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2fe1-146">傳回值</span><span class="sxs-lookup"><span data-stu-id="e2fe1-146">Return value</span></span>

<span data-ttu-id="e2fe1-147">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="e2fe1-147">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2fe1-148">備註</span><span class="sxs-lookup"><span data-stu-id="e2fe1-148">Remarks</span></span>

<span data-ttu-id="e2fe1-149">**GluTessProperty** 函式會控制儲存在鑲嵌式物件中的屬性。</span><span class="sxs-lookup"><span data-stu-id="e2fe1-149">The **gluTessProperty** function controls properties stored in a tessellation object.</span></span> <span data-ttu-id="e2fe1-150">這些屬性會影響多邊形的解讀和轉譯方式。</span><span class="sxs-lookup"><span data-stu-id="e2fe1-150">These properties affect the way the polygons are interpreted and rendered.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2fe1-151">規格需求</span><span class="sxs-lookup"><span data-stu-id="e2fe1-151">Requirements</span></span>



| <span data-ttu-id="e2fe1-152">需求</span><span class="sxs-lookup"><span data-stu-id="e2fe1-152">Requirement</span></span> | <span data-ttu-id="e2fe1-153">值</span><span class="sxs-lookup"><span data-stu-id="e2fe1-153">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e2fe1-154">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e2fe1-154">Minimum supported client</span></span><br/> | <span data-ttu-id="e2fe1-155">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e2fe1-155">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="e2fe1-156">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e2fe1-156">Minimum supported server</span></span><br/> | <span data-ttu-id="e2fe1-157">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e2fe1-157">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e2fe1-158">標頭</span><span class="sxs-lookup"><span data-stu-id="e2fe1-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2fe1-159"><dt>X.glu 隊。h</dt></span><span class="sxs-lookup"><span data-stu-id="e2fe1-159"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="e2fe1-160">程式庫</span><span class="sxs-lookup"><span data-stu-id="e2fe1-160">Library</span></span><br/>                  | <dl> <span data-ttu-id="e2fe1-161"><dt>Glu32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e2fe1-161"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="e2fe1-162">DLL</span><span class="sxs-lookup"><span data-stu-id="e2fe1-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2fe1-163"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2fe1-163"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2fe1-164">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e2fe1-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2fe1-165">**gluGetTessProperty**</span><span class="sxs-lookup"><span data-stu-id="e2fe1-165">**gluGetTessProperty**</span></span>](glugettessproperty.md)
</dt> <dt>

[<span data-ttu-id="e2fe1-166">**gluNewTess**</span><span class="sxs-lookup"><span data-stu-id="e2fe1-166">**gluNewTess**</span></span>](glunewtess.md)
</dt> </dl>

 

 





