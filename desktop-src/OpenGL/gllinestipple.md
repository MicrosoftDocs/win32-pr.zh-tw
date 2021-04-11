---
title: 'glLineStipple 函式 (Gl) '
description: GlLineStipple 函數會指定行 stipple 模式。
ms.assetid: 256d968c-9e72-4aec-9faf-afe70f1087a8
keywords:
- glLineStipple 函式 OpenGL
topic_type:
- apiref
api_name:
- glLineStipple
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b47202b25c0779a3daa0bd801900b1d29e0b37b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685482"
---
# <a name="gllinestipple-function"></a><span data-ttu-id="f2c8a-104">glLineStipple 函式</span><span class="sxs-lookup"><span data-stu-id="f2c8a-104">glLineStipple function</span></span>

<span data-ttu-id="f2c8a-105">**GlLineStipple** 函數會指定行 stipple 模式。</span><span class="sxs-lookup"><span data-stu-id="f2c8a-105">The **glLineStipple** function specifies the line stipple pattern.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2c8a-106">語法</span><span class="sxs-lookup"><span data-stu-id="f2c8a-106">Syntax</span></span>


```C++
void WINAPI glLineStipple(
   GLint    factor,
   GLushort pattern
);
```



## <a name="parameters"></a><span data-ttu-id="f2c8a-107">參數</span><span class="sxs-lookup"><span data-stu-id="f2c8a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2c8a-108">*因素*</span><span class="sxs-lookup"><span data-stu-id="f2c8a-108">*factor*</span></span> 
</dt> <dd>

<span data-ttu-id="f2c8a-109">行 stipple 模式中每個位的乘數。</span><span class="sxs-lookup"><span data-stu-id="f2c8a-109">A multiplier for each bit in the line stipple pattern.</span></span> <span data-ttu-id="f2c8a-110">例如，如果 *因數* 為3，則在使用模式中的下一個位之前，會使用模式中的每個位三次。</span><span class="sxs-lookup"><span data-stu-id="f2c8a-110">If *factor* is 3, for example, each bit in the pattern will be used three times before the next bit in the pattern is used.</span></span> <span data-ttu-id="f2c8a-111">*因數* 參數壓制至範圍 \[ 1，256， \] 預設值為一。</span><span class="sxs-lookup"><span data-stu-id="f2c8a-111">The *factor* parameter is clamped to the range \[1, 256\] and defaults to one.</span></span>

</dd> <dt>

<span data-ttu-id="f2c8a-112">*模式*</span><span class="sxs-lookup"><span data-stu-id="f2c8a-112">*pattern*</span></span> 
</dt> <dd>

<span data-ttu-id="f2c8a-113">16位整數，其位模式會決定何時要繪製線條的片段。</span><span class="sxs-lookup"><span data-stu-id="f2c8a-113">A 16-bit integer whose bit pattern determines which fragments of a line will be drawn when the line is rasterized.</span></span> <span data-ttu-id="f2c8a-114">第一個是使用位零，預設模式是所有的。</span><span class="sxs-lookup"><span data-stu-id="f2c8a-114">Bit zero is used first, and the default pattern is all ones.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2c8a-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="f2c8a-115">Return value</span></span>

<span data-ttu-id="f2c8a-116">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="f2c8a-116">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f2c8a-117">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="f2c8a-117">Error codes</span></span>

<span data-ttu-id="f2c8a-118">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f2c8a-118">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="f2c8a-119">Name</span><span class="sxs-lookup"><span data-stu-id="f2c8a-119">Name</span></span>                                                                                                  | <span data-ttu-id="f2c8a-120">意義</span><span class="sxs-lookup"><span data-stu-id="f2c8a-120">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f2c8a-121"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="f2c8a-121"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="f2c8a-122">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="f2c8a-122">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f2c8a-123">備註</span><span class="sxs-lookup"><span data-stu-id="f2c8a-123">Remarks</span></span>

<span data-ttu-id="f2c8a-124">**GlLineStipple** 函數會指定行 stipple 模式。</span><span class="sxs-lookup"><span data-stu-id="f2c8a-124">The **glLineStipple** function specifies the line stipple pattern.</span></span> <span data-ttu-id="f2c8a-125">Line stippling 會將點陣化所產生的特定片段遮罩;將不會繪製這些片段。</span><span class="sxs-lookup"><span data-stu-id="f2c8a-125">Line stippling masks out certain fragments produced by rasterization; those fragments will not be drawn.</span></span> <span data-ttu-id="f2c8a-126">遮罩的達成方式是使用三個參數：16位行 stipple 模式 *模式*、重複計數 *因數*，以及整數 stipple 計數器 *s*。</span><span class="sxs-lookup"><span data-stu-id="f2c8a-126">The masking is achieved by using three parameters: the 16-bit line stipple pattern *pattern*, the repeat count *factor*, and an integer stipple counter *s*.</span></span>

<span data-ttu-id="f2c8a-127">每當呼叫 [**glBegin**](glbegin.md)時，計數器 *s* 就會重設為零，而在 **glBegin** (GL 行的每個行區段之前，會 \_ 產生) /**glEnd** 序列。</span><span class="sxs-lookup"><span data-stu-id="f2c8a-127">Counter *s* is reset to zero whenever [**glBegin**](glbegin.md) is called, and before each line segment of a **glBegin**(GL\_LINES)/**glEnd** sequence is generated.</span></span> <span data-ttu-id="f2c8a-128">它會在產生單元寬度別名的每個片段之後，或在每次產生 *i* 寬線線段的每 *個片段之後* 遞增。</span><span class="sxs-lookup"><span data-stu-id="f2c8a-128">It is incremented after each fragment of a unit width aliased line segment is generated, or after each *i* fragments of an *i* width line segment are generated.</span></span> <span data-ttu-id="f2c8a-129">如果 *模式* 位 (*s*    /  *因數*) mod 16 為零，則與 count s 相關聯的 i 個片段會被遮罩。</span><span class="sxs-lookup"><span data-stu-id="f2c8a-129">The *i* fragments associated with count *s* are masked out if *pattern* bit (*s* / *factor*) mod 16 is zero.</span></span> <span data-ttu-id="f2c8a-130">否則會將這些片段傳送至畫面格緩衝區。</span><span class="sxs-lookup"><span data-stu-id="f2c8a-130">Otherwise these fragments are sent to the framebuffer.</span></span> <span data-ttu-id="f2c8a-131">*模式* 的位零是最不重要的位。</span><span class="sxs-lookup"><span data-stu-id="f2c8a-131">Bit zero of *pattern* is the least significant bit.</span></span>

<span data-ttu-id="f2c8a-132">基於 stippling 的目的，反鋸齒程式列會被視為一系列的 1x *寬度* 矩形。</span><span class="sxs-lookup"><span data-stu-id="f2c8a-132">Antialiased lines are treated as a sequence of 1x *width* rectangles for purposes of stippling.</span></span> <span data-ttu-id="f2c8a-133">矩形 *s* 會根據為別名行所描述的片段規則進行柵格化，它會計算矩形，而不是片段群組。</span><span class="sxs-lookup"><span data-stu-id="f2c8a-133">Rectangle *s* is rasterized or not based on the fragment rule described for aliased lines; it counts rectangles rather than groups of fragments.</span></span>

<span data-ttu-id="f2c8a-134">使用 [**glEnable**](glenable.md) 和 **glDisable** 搭配引數 GL 行 STIPPLE 來啟用或停用行 stippling \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="f2c8a-134">Line stippling is enabled or disabled using [**glEnable**](glenable.md) and **glDisable** with argument GL\_LINE\_STIPPLE.</span></span> <span data-ttu-id="f2c8a-135">啟用時，會如上面所述套用行 stipple 模式。</span><span class="sxs-lookup"><span data-stu-id="f2c8a-135">When enabled, the line stipple pattern is applied as described above.</span></span> <span data-ttu-id="f2c8a-136">停用時，就像模式是全部一樣。</span><span class="sxs-lookup"><span data-stu-id="f2c8a-136">When disabled, it is as if the pattern were all ones.</span></span> <span data-ttu-id="f2c8a-137">一開始，行 stippling 已停用。</span><span class="sxs-lookup"><span data-stu-id="f2c8a-137">Initially, line stippling is disabled.</span></span>

<span data-ttu-id="f2c8a-138">下列函式會取出與 **glLineStipple** 相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="f2c8a-138">The following functions retrieve information related to **glLineStipple**:</span></span>

<span data-ttu-id="f2c8a-139">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 行 \_ STIPPLE \_ 模式的 glGet</span><span class="sxs-lookup"><span data-stu-id="f2c8a-139">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_LINE\_STIPPLE\_PATTERN</span></span>

<span data-ttu-id="f2c8a-140">**glGet** 與引數 GL \_ 行 \_ STIPPLE \_ 重複</span><span class="sxs-lookup"><span data-stu-id="f2c8a-140">**glGet** with argument GL\_LINE\_STIPPLE\_REPEAT</span></span>

<span data-ttu-id="f2c8a-141">[](glisenabled.md)具有引數 GL \_ 行 \_ STIPPLE 的 glIsEnabled</span><span class="sxs-lookup"><span data-stu-id="f2c8a-141">[**glIsEnabled**](glisenabled.md) with argument GL\_LINE\_STIPPLE</span></span>

## <a name="requirements"></a><span data-ttu-id="f2c8a-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="f2c8a-142">Requirements</span></span>



| <span data-ttu-id="f2c8a-143">需求</span><span class="sxs-lookup"><span data-stu-id="f2c8a-143">Requirement</span></span> | <span data-ttu-id="f2c8a-144">值</span><span class="sxs-lookup"><span data-stu-id="f2c8a-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2c8a-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f2c8a-145">Minimum supported client</span></span><br/> | <span data-ttu-id="f2c8a-146">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f2c8a-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f2c8a-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f2c8a-147">Minimum supported server</span></span><br/> | <span data-ttu-id="f2c8a-148">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f2c8a-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f2c8a-149">標頭</span><span class="sxs-lookup"><span data-stu-id="f2c8a-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2c8a-150"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="f2c8a-150"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="f2c8a-151">程式庫</span><span class="sxs-lookup"><span data-stu-id="f2c8a-151">Library</span></span><br/>                  | <dl> <span data-ttu-id="f2c8a-152"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f2c8a-152"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="f2c8a-153">DLL</span><span class="sxs-lookup"><span data-stu-id="f2c8a-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2c8a-154"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2c8a-154"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2c8a-155">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f2c8a-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2c8a-156">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="f2c8a-156">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="f2c8a-157">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="f2c8a-157">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="f2c8a-158">**glLineWidth**</span><span class="sxs-lookup"><span data-stu-id="f2c8a-158">**glLineWidth**</span></span>](gllinewidth.md)
</dt> <dt>

[<span data-ttu-id="f2c8a-159">**glPolygonStipple**</span><span class="sxs-lookup"><span data-stu-id="f2c8a-159">**glPolygonStipple**</span></span>](glpolygonstipple.md)
</dt> </dl>

 

 





