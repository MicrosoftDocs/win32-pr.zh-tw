---
title: 'glEdgeFlagPointer 函式 (Gl) '
description: GlEdgeFlagPointer 函式會定義邊緣旗標的陣列。
ms.assetid: e0e7e442-533d-4c41-addd-a215ce0b1c56
keywords:
- glEdgeFlagPointer 函式 OpenGL
topic_type:
- apiref
api_name:
- glEdgeFlagPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4390a9838fef418763aa4bcafbf815ab0cdf3466
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686084"
---
# <a name="gledgeflagpointer-function"></a><span data-ttu-id="ee746-104">glEdgeFlagPointer 函式</span><span class="sxs-lookup"><span data-stu-id="ee746-104">glEdgeFlagPointer function</span></span>

<span data-ttu-id="ee746-105">**GlEdgeFlagPointer** 函式會定義邊緣旗標的陣列。</span><span class="sxs-lookup"><span data-stu-id="ee746-105">The **glEdgeFlagPointer** function defines an array of edge flags.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee746-106">語法</span><span class="sxs-lookup"><span data-stu-id="ee746-106">Syntax</span></span>


```C++
void WINAPI glEdgeFlagPointer(
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a><span data-ttu-id="ee746-107">參數</span><span class="sxs-lookup"><span data-stu-id="ee746-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee746-108">*大步*</span><span class="sxs-lookup"><span data-stu-id="ee746-108">*stride*</span></span> 
</dt> <dd>

<span data-ttu-id="ee746-109">連續邊緣旗標之間的位元組位移。</span><span class="sxs-lookup"><span data-stu-id="ee746-109">The byte offset between consecutive edge flags.</span></span> <span data-ttu-id="ee746-110">當 *stride* 為零時，邊緣旗標會緊密地封裝在陣列中。</span><span class="sxs-lookup"><span data-stu-id="ee746-110">When *stride* is zero, the edge flags are tightly packed in the array.</span></span>

</dd> <dt>

<span data-ttu-id="ee746-111">*指標*</span><span class="sxs-lookup"><span data-stu-id="ee746-111">*pointer*</span></span> 
</dt> <dd>

<span data-ttu-id="ee746-112">陣列中第一個邊緣旗標的指標。</span><span class="sxs-lookup"><span data-stu-id="ee746-112">A pointer to the first edge flag in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee746-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="ee746-113">Return value</span></span>

<span data-ttu-id="ee746-114">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="ee746-114">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ee746-115">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="ee746-115">Error codes</span></span>

<span data-ttu-id="ee746-116">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="ee746-116">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="ee746-117">Name</span><span class="sxs-lookup"><span data-stu-id="ee746-117">Name</span></span>                                                                                             | <span data-ttu-id="ee746-118">意義</span><span class="sxs-lookup"><span data-stu-id="ee746-118">Meaning</span></span>                                      |
|--------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="ee746-119"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="ee746-119"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl> | <span data-ttu-id="ee746-120">*stride* 或 *計數* 為負數。</span><span class="sxs-lookup"><span data-stu-id="ee746-120">*stride* or *count* was negative.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="ee746-121">備註</span><span class="sxs-lookup"><span data-stu-id="ee746-121">Remarks</span></span>

<span data-ttu-id="ee746-122">**GlEdgeFlagPointer** 函式會指定轉譯時要使用的布林邊緣旗標陣列的位置和資料。</span><span class="sxs-lookup"><span data-stu-id="ee746-122">The **glEdgeFlagPointer** function specifies the location and data of an array of Boolean edge flags to use when rendering.</span></span> <span data-ttu-id="ee746-123">*Stride* 參數會決定從某個邊緣旗標到下一個邊緣旗標的位元組位移，這可將單一陣列或儲存區中的頂點和屬性封裝成不同的陣列。</span><span class="sxs-lookup"><span data-stu-id="ee746-123">The *stride* parameter determines the byte offset from one edge flag to the next, which enables the packing of vertices and attributes in a single array or storage in separate arrays.</span></span> <span data-ttu-id="ee746-124">在某些情況下，將頂點和屬性儲存在單一陣列中的效率可能比使用個別陣列更有效率。</span><span class="sxs-lookup"><span data-stu-id="ee746-124">In some implementations, storing the vertices and attributes in a single array can be more efficient than using separate arrays.</span></span>

<span data-ttu-id="ee746-125">當您 \_ 使用 glEnableClientState 指定 GL edge \_ 旗標 \_ 陣列常數[](glenableclientstate.md)時，會啟用邊緣旗標陣列。</span><span class="sxs-lookup"><span data-stu-id="ee746-125">An edge-flag array is enabled when you specify the GL\_EDGE\_FLAG\_ARRAY constant with [**glEnableClientState**](glenableclientstate.md).</span></span> <span data-ttu-id="ee746-126">啟用時， [**glDrawArrays**](gldrawarrays.md) 或 [**glArrayElement**](glarrayelement.md) 會使用邊緣旗標陣列。</span><span class="sxs-lookup"><span data-stu-id="ee746-126">When enabled, [**glDrawArrays**](gldrawarrays.md) or [**glArrayElement**](glarrayelement.md) uses the edge-flag array.</span></span> <span data-ttu-id="ee746-127">Edge 旗標陣列預設為停用。</span><span class="sxs-lookup"><span data-stu-id="ee746-127">By default the edge-flag array is disabled.</span></span>

<span data-ttu-id="ee746-128">您可以使用 **glDrawArrays** 來建立一系列的基本類型， (預先指定頂點和頂點屬性陣列中) 的所有相同型別。</span><span class="sxs-lookup"><span data-stu-id="ee746-128">Use **glDrawArrays** to construct a sequence of primitives (all of the same type) from prespecified vertex and vertex attribute arrays.</span></span> <span data-ttu-id="ee746-129">您可以使用 **glArrayElement** ，藉由為頂點和頂點屬性編制索引來指定基本專案，並透過編制頂點和頂點屬性的索引， [**glDrawElements**](gldrawelements.md) 來建立基本類型的序列。</span><span class="sxs-lookup"><span data-stu-id="ee746-129">Use **glArrayElement** to specify primitives by indexing vertices and vertex attributes, and [**glDrawElements**](gldrawelements.md) to construct a sequence of primitives by indexing vertices and vertex attributes.</span></span>

<span data-ttu-id="ee746-130">您無法在顯示清單中包含 **glEdgeFlagPointer** 。</span><span class="sxs-lookup"><span data-stu-id="ee746-130">You cannot include **glEdgeFlagPointer** in display lists.</span></span>

<span data-ttu-id="ee746-131">當您使用 **glEdgeFlagPointer** 指定邊緣旗標陣列時，所有函式的邊緣旗標陣列參數值都會儲存在用戶端狀態中，而且可以快取靜態陣列元素。</span><span class="sxs-lookup"><span data-stu-id="ee746-131">When you specify an edge-flag array using **glEdgeFlagPointer**, the values of all the function's edge-flag array parameters are saved in a client-side state and static array elements can be cached.</span></span> <span data-ttu-id="ee746-132">由於 edge 旗標陣列參數處於用戶端狀態， [**glPushAttrib**](glpushattrib.md) 和 [**glPopAttrib**](glpopattrib.md) 不會儲存或還原它們的值。</span><span class="sxs-lookup"><span data-stu-id="ee746-132">Because the edge-flag array parameters are in a client-side state, [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md) do not save or restore their values.</span></span>

<span data-ttu-id="ee746-133">雖然在 [**glBegin**](glbegin.md) / [**glend**](glend.md)配對內呼叫 glEdgeFlagPointer 並不會產生錯誤，但結果是未定義的。</span><span class="sxs-lookup"><span data-stu-id="ee746-133">Although calling **glEdgeFlagPointer** within a [**glBegin**](glbegin.md)/[**glend**](glend.md) pair does not generate an error, the results are undefined.</span></span>

<span data-ttu-id="ee746-134">下列函式會取出與 **glEdgeFlagPointer** 函數相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="ee746-134">The following functions retrieve information related to the **glEdgeFlagPointer** function:</span></span>

<span data-ttu-id="ee746-135">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 邊緣 \_ 旗標 \_ 陣列 \_ STRIDE 的 glGet</span><span class="sxs-lookup"><span data-stu-id="ee746-135">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_EDGE\_FLAG\_ARRAY\_STRIDE</span></span>

<span data-ttu-id="ee746-136">具有引數 GL \_ EDGE \_ 旗標 \_ 陣列 \_ 計數的 glGet</span><span class="sxs-lookup"><span data-stu-id="ee746-136">**glGet** with argument GL\_EDGE\_FLAG\_ARRAY\_COUNT</span></span>

<span data-ttu-id="ee746-137">[](glgetpointerv.md)具有引數 GL \_ EDGE \_ 旗標 \_ 陣列 \_ 指標的 glGetPointerv</span><span class="sxs-lookup"><span data-stu-id="ee746-137">[**glGetPointerv**](glgetpointerv.md) with argument GL\_EDGE\_FLAG\_ARRAY\_POINTER</span></span>

<span data-ttu-id="ee746-138">[](glisenabled.md)具有引數 GL \_ EDGE \_ 旗標 \_ 陣列的 glIsEnabled</span><span class="sxs-lookup"><span data-stu-id="ee746-138">[**glIsEnabled**](glisenabled.md) with argument GL\_EDGE\_FLAG\_ARRAY</span></span>

## <a name="requirements"></a><span data-ttu-id="ee746-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="ee746-139">Requirements</span></span>



| <span data-ttu-id="ee746-140">需求</span><span class="sxs-lookup"><span data-stu-id="ee746-140">Requirement</span></span> | <span data-ttu-id="ee746-141">值</span><span class="sxs-lookup"><span data-stu-id="ee746-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ee746-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ee746-142">Minimum supported client</span></span><br/> | <span data-ttu-id="ee746-143">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ee746-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ee746-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ee746-144">Minimum supported server</span></span><br/> | <span data-ttu-id="ee746-145">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ee746-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ee746-146">標頭</span><span class="sxs-lookup"><span data-stu-id="ee746-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee746-147"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="ee746-147"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="ee746-148">程式庫</span><span class="sxs-lookup"><span data-stu-id="ee746-148">Library</span></span><br/>                  | <dl> <span data-ttu-id="ee746-149"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ee746-149"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="ee746-150">DLL</span><span class="sxs-lookup"><span data-stu-id="ee746-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee746-151"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee746-151"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee746-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ee746-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee746-153">**glArrayElement**</span><span class="sxs-lookup"><span data-stu-id="ee746-153">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="ee746-154">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="ee746-154">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="ee746-155">**glColorPointer**</span><span class="sxs-lookup"><span data-stu-id="ee746-155">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="ee746-156">**glDrawArrays**</span><span class="sxs-lookup"><span data-stu-id="ee746-156">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="ee746-157">**glEnableClientState**</span><span class="sxs-lookup"><span data-stu-id="ee746-157">**glEnableClientState**</span></span>](glenableclientstate.md)
</dt> <dt>

[<span data-ttu-id="ee746-158">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="ee746-158">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="ee746-159">**glGet**</span><span class="sxs-lookup"><span data-stu-id="ee746-159">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="ee746-160">**glGetPointerv**</span><span class="sxs-lookup"><span data-stu-id="ee746-160">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="ee746-161">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="ee746-161">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="ee746-162">**glIndexPointer**</span><span class="sxs-lookup"><span data-stu-id="ee746-162">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="ee746-163">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="ee746-163">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="ee746-164">**glNormalPointer**</span><span class="sxs-lookup"><span data-stu-id="ee746-164">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="ee746-165">**glPopAttrib**</span><span class="sxs-lookup"><span data-stu-id="ee746-165">**glPopAttrib**</span></span>](glpopattrib.md)
</dt> <dt>

[<span data-ttu-id="ee746-166">**glPushAttrib**</span><span class="sxs-lookup"><span data-stu-id="ee746-166">**glPushAttrib**</span></span>](glpushattrib.md)
</dt> <dt>

[<span data-ttu-id="ee746-167">**glTexCoordPointer**</span><span class="sxs-lookup"><span data-stu-id="ee746-167">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="ee746-168">**glVertexPointer**</span><span class="sxs-lookup"><span data-stu-id="ee746-168">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





