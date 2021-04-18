---
title: 'glVertexPointer 函式 (Gl) '
description: GlVertexPointer 函式會定義頂點資料的陣列。
ms.assetid: e5f97fdc-9448-4389-8533-3855a3213feb
keywords:
- glVertexPointer 函式 OpenGL
topic_type:
- apiref
api_name:
- glVertexPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 422dd1a7938cc5adb183ff7e17c59a8f52eb4909
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466316"
---
# <a name="glvertexpointer-function"></a><span data-ttu-id="0a90f-104">glVertexPointer 函式</span><span class="sxs-lookup"><span data-stu-id="0a90f-104">glVertexPointer function</span></span>

<span data-ttu-id="0a90f-105">**GlVertexPointer** 函式會定義頂點資料的陣列。</span><span class="sxs-lookup"><span data-stu-id="0a90f-105">The **glVertexPointer** function defines an array of vertex data.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a90f-106">語法</span><span class="sxs-lookup"><span data-stu-id="0a90f-106">Syntax</span></span>


```C++
void WINAPI glVertexPointer(
         GLint   size,
         GLenum  type,
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a><span data-ttu-id="0a90f-107">參數</span><span class="sxs-lookup"><span data-stu-id="0a90f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a90f-108">*size*</span><span class="sxs-lookup"><span data-stu-id="0a90f-108">*size*</span></span> 
</dt> <dd>

<span data-ttu-id="0a90f-109">每個頂點的座標數目。</span><span class="sxs-lookup"><span data-stu-id="0a90f-109">The number of coordinates per vertex.</span></span> <span data-ttu-id="0a90f-110">*大小* 的值必須是2、3或4。</span><span class="sxs-lookup"><span data-stu-id="0a90f-110">The value of *size* must be 2, 3, or 4.</span></span>

</dd> <dt>

<span data-ttu-id="0a90f-111">*type*</span><span class="sxs-lookup"><span data-stu-id="0a90f-111">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="0a90f-112">陣列中每個座標的資料類型，使用下列符號常數： GL \_ SHORT、gl \_ INT、gl \_ FLOAT 和 gl \_ DOUBLE。</span><span class="sxs-lookup"><span data-stu-id="0a90f-112">The data type of each coordinate in the array using the following symbolic constants: GL\_SHORT, GL\_INT, GL\_FLOAT, and GL\_DOUBLE.</span></span>

</dd> <dt>

<span data-ttu-id="0a90f-113">*大步*</span><span class="sxs-lookup"><span data-stu-id="0a90f-113">*stride*</span></span> 
</dt> <dd>

<span data-ttu-id="0a90f-114">連續頂點之間的位元組位移。</span><span class="sxs-lookup"><span data-stu-id="0a90f-114">The byte offset between consecutive vertices.</span></span> <span data-ttu-id="0a90f-115">當 *stride* 為零時，就會將頂點緊密地封裝在陣列中。</span><span class="sxs-lookup"><span data-stu-id="0a90f-115">When *stride* is zero, the vertices are tightly packed in the array.</span></span>

</dd> <dt>

<span data-ttu-id="0a90f-116">*指標*</span><span class="sxs-lookup"><span data-stu-id="0a90f-116">*pointer*</span></span> 
</dt> <dd>

<span data-ttu-id="0a90f-117">陣列中第一個頂點的第一個座標指標。</span><span class="sxs-lookup"><span data-stu-id="0a90f-117">A pointer to the first coordinate of the first vertex in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a90f-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="0a90f-118">Return value</span></span>

<span data-ttu-id="0a90f-119">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="0a90f-119">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0a90f-120">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="0a90f-120">Error codes</span></span>

<span data-ttu-id="0a90f-121">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="0a90f-121">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="0a90f-122">Name</span><span class="sxs-lookup"><span data-stu-id="0a90f-122">Name</span></span>                                                                                              | <span data-ttu-id="0a90f-123">意義</span><span class="sxs-lookup"><span data-stu-id="0a90f-123">Meaning</span></span>                                       |
|---------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="0a90f-124"><dt>**GL \_ 無效 \_ 值**</dt></span><span class="sxs-lookup"><span data-stu-id="0a90f-124"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="0a90f-125">*大小* 不是2、3或4。</span><span class="sxs-lookup"><span data-stu-id="0a90f-125">*size* was not 2, 3, or 4.</span></span> <br/>        |
| <dl> <span data-ttu-id="0a90f-126"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="0a90f-126"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>  | <span data-ttu-id="0a90f-127">*類型* 不是可接受的值。</span><span class="sxs-lookup"><span data-stu-id="0a90f-127">*type* was not an accepted value.</span></span><br/>  |
| <dl> <span data-ttu-id="0a90f-128"><dt>**GL \_ 無效 \_ 值**</dt></span><span class="sxs-lookup"><span data-stu-id="0a90f-128"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="0a90f-129">*stride* 或 *計數* 為負數。</span><span class="sxs-lookup"><span data-stu-id="0a90f-129">*stride* or *count* was negative.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="0a90f-130">備註</span><span class="sxs-lookup"><span data-stu-id="0a90f-130">Remarks</span></span>

<span data-ttu-id="0a90f-131">**GlVertexPointer** 函式會指定要在轉譯時使用之頂點座標陣列的位置和資料。</span><span class="sxs-lookup"><span data-stu-id="0a90f-131">The **glVertexPointer** function specifies the location and data of an array of vertex coordinates to use when rendering.</span></span> <span data-ttu-id="0a90f-132">*Size* 參數指定每個頂點的座標數目。</span><span class="sxs-lookup"><span data-stu-id="0a90f-132">The *size* parameter specifies the number of coordinates per vertex.</span></span> <span data-ttu-id="0a90f-133">*Type* 參數指定每個頂點座標的資料類型。</span><span class="sxs-lookup"><span data-stu-id="0a90f-133">The *type* parameter specifies the data type of each vertex coordinate.</span></span> <span data-ttu-id="0a90f-134">*Stride* 參數會決定從某個頂點到下一個頂點的位元組位移，以便將單一陣列或儲存區中的頂點和屬性封裝成不同的陣列。</span><span class="sxs-lookup"><span data-stu-id="0a90f-134">The *stride* parameter determines the byte offset from one vertex to the next, enabling the packing of vertices and attributes in a single array or storage in separate arrays.</span></span> <span data-ttu-id="0a90f-135">在某些情況下，在單一陣列中儲存頂點和屬性，會比使用不同的陣列更有效率 (請參閱 [**glInterleavedArrays**](glinterleavedarrays.md)) 。</span><span class="sxs-lookup"><span data-stu-id="0a90f-135">In some implementations, storing the vertices and attributes in a single array can be more efficient than using separate arrays (see [**glInterleavedArrays**](glinterleavedarrays.md)).</span></span>

<span data-ttu-id="0a90f-136">當您 \_ \_ 使用 [**glEnableClientState**](glenableclientstate.md)指定 GL 頂點陣列常數時，會啟用頂點陣列。</span><span class="sxs-lookup"><span data-stu-id="0a90f-136">A vertex array is enabled when you specify the GL\_VERTEX\_ARRAY constant with [**glEnableClientState**](glenableclientstate.md).</span></span> <span data-ttu-id="0a90f-137">啟用時， [**glDrawArrays**](gldrawarrays.md)、 [**glDrawElements**](gldrawelements.md)和 [**glArrayElement**](glarrayelement.md) 會使用頂點陣列。</span><span class="sxs-lookup"><span data-stu-id="0a90f-137">When enabled, [**glDrawArrays**](gldrawarrays.md), [**glDrawElements**](gldrawelements.md), and [**glArrayElement**](glarrayelement.md) use the vertex array.</span></span> <span data-ttu-id="0a90f-138">預設會停用頂點陣列。</span><span class="sxs-lookup"><span data-stu-id="0a90f-138">By default, the vertex array is disabled.</span></span>

<span data-ttu-id="0a90f-139">您無法在顯示清單中包含 **glVertexPointer** 。</span><span class="sxs-lookup"><span data-stu-id="0a90f-139">You cannot include **glVertexPointer** in display lists.</span></span>

<span data-ttu-id="0a90f-140">當您使用 **glVertexPointer** 指定頂點陣列時，所有函式之頂點陣列參數的值都會儲存在用戶端狀態中，而且可以快取靜態陣列元素。</span><span class="sxs-lookup"><span data-stu-id="0a90f-140">When you specify a vertex array using **glVertexPointer**, the values of all the function's vertex array parameters are saved in a client-side state, and static array elements can be cached.</span></span> <span data-ttu-id="0a90f-141">因為頂點陣列參數是用戶端狀態，所以它們的值不會由 [**glPushAttrib**](glpushattrib.md) 和 **glPopAttrib** 儲存或還原。</span><span class="sxs-lookup"><span data-stu-id="0a90f-141">Because the vertex array parameters are client-side state, their values are not saved or restored by [**glPushAttrib**](glpushattrib.md) and **glPopAttrib**.</span></span>

<span data-ttu-id="0a90f-142">雖然在 [**glBegin**](glbegin.md)和 [**glEnd**](glend.md)配對內呼叫 **glVertexPointer** 時不會產生任何錯誤，但結果未定義。</span><span class="sxs-lookup"><span data-stu-id="0a90f-142">Although no error is generated if you call **glVertexPointer** within [**glBegin**](glbegin.md) and [**glEnd**](glend.md) pairs, the results are undefined.</span></span>

<span data-ttu-id="0a90f-143">下列函式會取出與 **glVertexPointer** 相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="0a90f-143">The following functions retrieve information related to **glVertexPointer**:</span></span>

<span data-ttu-id="0a90f-144">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 頂點 \_ 陣列 \_ 大小的 glGet</span><span class="sxs-lookup"><span data-stu-id="0a90f-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_VERTEX\_ARRAY\_SIZE</span></span>

<span data-ttu-id="0a90f-145">具有引數 GL \_ 頂點 \_ 陣列 \_ STRIDE 的 glGet</span><span class="sxs-lookup"><span data-stu-id="0a90f-145">**glGet** with argument GL\_VERTEX\_ARRAY\_STRIDE</span></span>

<span data-ttu-id="0a90f-146">具有引數 GL \_ 頂點 \_ 陣列 \_ 計數的 glGet</span><span class="sxs-lookup"><span data-stu-id="0a90f-146">**glGet** with argument GL\_VERTEX\_ARRAY\_COUNT</span></span>

<span data-ttu-id="0a90f-147">具有引數 GL \_ 頂點 \_ 陣列 \_ 類型的 glGet</span><span class="sxs-lookup"><span data-stu-id="0a90f-147">**glGet** with argument GL\_VERTEX\_ARRAY\_TYPE</span></span>

<span data-ttu-id="0a90f-148">[](glgetpointerv.md)具有引數 GL \_ 頂點 \_ 陣列 \_ 指標的 glGetPointerv</span><span class="sxs-lookup"><span data-stu-id="0a90f-148">[**glGetPointerv**](glgetpointerv.md) with argument GL\_VERTEX\_ARRAY\_POINTER</span></span>

<span data-ttu-id="0a90f-149">[](glisenabled.md)具有引數 GL \_ 頂點 \_ 陣列的 glIsEnabled</span><span class="sxs-lookup"><span data-stu-id="0a90f-149">[**glIsEnabled**](glisenabled.md) with argument GL\_VERTEX\_ARRAY</span></span>

## <a name="requirements"></a><span data-ttu-id="0a90f-150">規格需求</span><span class="sxs-lookup"><span data-stu-id="0a90f-150">Requirements</span></span>



| <span data-ttu-id="0a90f-151">需求</span><span class="sxs-lookup"><span data-stu-id="0a90f-151">Requirement</span></span> | <span data-ttu-id="0a90f-152">值</span><span class="sxs-lookup"><span data-stu-id="0a90f-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0a90f-153">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0a90f-153">Minimum supported client</span></span><br/> | <span data-ttu-id="0a90f-154">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0a90f-154">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="0a90f-155">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0a90f-155">Minimum supported server</span></span><br/> | <span data-ttu-id="0a90f-156">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0a90f-156">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0a90f-157">標頭</span><span class="sxs-lookup"><span data-stu-id="0a90f-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a90f-158"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="0a90f-158"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="0a90f-159">程式庫</span><span class="sxs-lookup"><span data-stu-id="0a90f-159">Library</span></span><br/>                  | <dl> <span data-ttu-id="0a90f-160"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="0a90f-160"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="0a90f-161">DLL</span><span class="sxs-lookup"><span data-stu-id="0a90f-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a90f-162"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a90f-162"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a90f-163">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0a90f-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a90f-164">**glArrayElement**</span><span class="sxs-lookup"><span data-stu-id="0a90f-164">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="0a90f-165">**glColorPointer**</span><span class="sxs-lookup"><span data-stu-id="0a90f-165">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="0a90f-166">**glDrawArrays**</span><span class="sxs-lookup"><span data-stu-id="0a90f-166">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="0a90f-167">**glEdgeFlagPointer**</span><span class="sxs-lookup"><span data-stu-id="0a90f-167">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="0a90f-168">**glEnableClientState**</span><span class="sxs-lookup"><span data-stu-id="0a90f-168">**glEnableClientState**</span></span>](glenableclientstate.md)
</dt> <dt>

[<span data-ttu-id="0a90f-169">**glGetPointerv**</span><span class="sxs-lookup"><span data-stu-id="0a90f-169">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="0a90f-170">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="0a90f-170">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="0a90f-171">**glIndexPointer**</span><span class="sxs-lookup"><span data-stu-id="0a90f-171">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="0a90f-172">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="0a90f-172">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="0a90f-173">**glNormalPointer**</span><span class="sxs-lookup"><span data-stu-id="0a90f-173">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="0a90f-174">**glTexCoordPointer**</span><span class="sxs-lookup"><span data-stu-id="0a90f-174">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> </dl>

 

 





