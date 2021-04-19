---
title: 'glTexCoordPointer 函式 (Gl) '
description: GlTexCoordPointer 函式會定義材質座標的陣列。
ms.assetid: c3640a1b-ccc7-4f1a-94a5-a164f7377dbc
keywords:
- glTexCoordPointer 函式 OpenGL
topic_type:
- apiref
api_name:
- glTexCoordPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: febc9c79bdbc4a1ed1c14380af47f36309f12662
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106972701"
---
# <a name="gltexcoordpointer-function"></a><span data-ttu-id="290cf-104">glTexCoordPointer 函式</span><span class="sxs-lookup"><span data-stu-id="290cf-104">glTexCoordPointer function</span></span>

<span data-ttu-id="290cf-105">**GlTexCoordPointer** 函式會定義材質座標的陣列。</span><span class="sxs-lookup"><span data-stu-id="290cf-105">The **glTexCoordPointer** function defines an array of texture coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="290cf-106">語法</span><span class="sxs-lookup"><span data-stu-id="290cf-106">Syntax</span></span>


```C++
void WINAPI glTexCoordPointer(
         GLint   size,
         GLenum  type,
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a><span data-ttu-id="290cf-107">參數</span><span class="sxs-lookup"><span data-stu-id="290cf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="290cf-108">*size*</span><span class="sxs-lookup"><span data-stu-id="290cf-108">*size*</span></span> 
</dt> <dd>

<span data-ttu-id="290cf-109">每個陣列元素的座標數目。</span><span class="sxs-lookup"><span data-stu-id="290cf-109">The number of coordinates per array element.</span></span> <span data-ttu-id="290cf-110">*大小* 的值必須是1、2、3或4。</span><span class="sxs-lookup"><span data-stu-id="290cf-110">The value of *size* must be 1, 2, 3, or 4.</span></span>

</dd> <dt>

<span data-ttu-id="290cf-111">*type*</span><span class="sxs-lookup"><span data-stu-id="290cf-111">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="290cf-112">陣列中每個材質座標的資料類型，使用下列符號常數： **GL \_ SHORT**、 **gl \_ INT**、 **gl \_ FLOAT** 和 **gl \_ DOUBLE**。</span><span class="sxs-lookup"><span data-stu-id="290cf-112">The data type of each texture coordinate in the array using the following symbolic constants: **GL\_SHORT**, **GL\_INT**, **GL\_FLOAT**, and **GL\_DOUBLE**.</span></span>

</dd> <dt>

<span data-ttu-id="290cf-113">*大步*</span><span class="sxs-lookup"><span data-stu-id="290cf-113">*stride*</span></span> 
</dt> <dd>

<span data-ttu-id="290cf-114">連續陣列元素之間的位元組位移。</span><span class="sxs-lookup"><span data-stu-id="290cf-114">The byte offset between consecutive array elements.</span></span> <span data-ttu-id="290cf-115">當 *stride* 為零時，陣列元素會緊密地封裝在陣列中。</span><span class="sxs-lookup"><span data-stu-id="290cf-115">When *stride* is zero, the array elements are tightly packed in the array.</span></span>

</dd> <dt>

<span data-ttu-id="290cf-116">*指標*</span><span class="sxs-lookup"><span data-stu-id="290cf-116">*pointer*</span></span> 
</dt> <dd>

<span data-ttu-id="290cf-117">陣列中第一個元素的第一個座標指標。</span><span class="sxs-lookup"><span data-stu-id="290cf-117">A pointer to the first coordinate of the first element in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="290cf-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="290cf-118">Return value</span></span>

<span data-ttu-id="290cf-119">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="290cf-119">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="290cf-120">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="290cf-120">Error codes</span></span>

<span data-ttu-id="290cf-121">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="290cf-121">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="290cf-122">Name</span><span class="sxs-lookup"><span data-stu-id="290cf-122">Name</span></span>                                                                                              | <span data-ttu-id="290cf-123">意義</span><span class="sxs-lookup"><span data-stu-id="290cf-123">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="290cf-124"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="290cf-124"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>  | <span data-ttu-id="290cf-125">*類型* 不是可接受的值。</span><span class="sxs-lookup"><span data-stu-id="290cf-125">*type* was not an accepted value.</span></span><br/> |
| <dl> <span data-ttu-id="290cf-126"><dt>**GL \_ 無效 \_ 值**</dt></span><span class="sxs-lookup"><span data-stu-id="290cf-126"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="290cf-127">*大小* 不是1、2、3或4。</span><span class="sxs-lookup"><span data-stu-id="290cf-127">*size* was not 1, 2, 3, or 4.</span></span><br/>     |
| <dl> <span data-ttu-id="290cf-128"><dt>**GL \_ 無效 \_ 值**</dt></span><span class="sxs-lookup"><span data-stu-id="290cf-128"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="290cf-129">*stride* 為負數。</span><span class="sxs-lookup"><span data-stu-id="290cf-129">*stride* was negative.</span></span><br/>            |



## <a name="remarks"></a><span data-ttu-id="290cf-130">備註</span><span class="sxs-lookup"><span data-stu-id="290cf-130">Remarks</span></span>

<span data-ttu-id="290cf-131">**GlTexCoordPointer** 函式會指定轉譯時要使用之材質座標陣列的位置和資料。*Size* 參數會指定陣列中每個元素所使用的座標數目。*Type* 參數指定每個材質座標的資料類型。</span><span class="sxs-lookup"><span data-stu-id="290cf-131">The **glTexCoordPointer** function specifies the location and data of an array of texture coordinates to use when rendering.The *size* parameter specifies the number of coordinates used for each element of the array.The *type* parameter specifies the data type of each texture coordinate.</span></span> <span data-ttu-id="290cf-132">*Stride* 參數會決定從某個陣列元素到下一個陣列專案的位元組位移，以便將單一陣列或儲存區中的頂點和屬性封裝成不同的陣列。</span><span class="sxs-lookup"><span data-stu-id="290cf-132">The *stride* parameter determines the byte offset from one array element to the next, enabling the packing of vertices and attributes in a single array or storage in separate arrays.</span></span> <span data-ttu-id="290cf-133">在某些情況下，將頂點和屬性儲存在單一陣列中的效率可能比使用個別陣列更有效率。</span><span class="sxs-lookup"><span data-stu-id="290cf-133">In some implementations, storing the vertices and attributes in a single array can be more efficient than using separate arrays.</span></span> <span data-ttu-id="290cf-134">如需詳細資訊，請參閱 [**glInterleavedArrays**](glinterleavedarrays.md)。</span><span class="sxs-lookup"><span data-stu-id="290cf-134">For more information, see [**glInterleavedArrays**](glinterleavedarrays.md).</span></span> <span data-ttu-id="290cf-135">當指定紋理座標陣列時，大小、類型、跨距和指標都會儲存用戶端狀態。</span><span class="sxs-lookup"><span data-stu-id="290cf-135">When a texture coordinate array is specified, size, type, stride, and pointer are saved client-side state.</span></span>

<span data-ttu-id="290cf-136">當您使用 [**glEnableClientState**](glenableclientstate.md)指定 **GL \_ 紋理 \_ COORD \_ 陣列** 常數時，會啟用紋理座標陣列。</span><span class="sxs-lookup"><span data-stu-id="290cf-136">A texture coordinate array is enabled when you specify the **GL\_TEXTURE\_COORD\_ARRAY** constant with [**glEnableClientState**](glenableclientstate.md).</span></span> <span data-ttu-id="290cf-137">啟用時， [**glDrawArrays**](gldrawarrays.md)、 [**glDrawElements**](gldrawelements.md)和 [**glArrayElement**](glarrayelement.md) 會使用材質座標陣列。</span><span class="sxs-lookup"><span data-stu-id="290cf-137">When enabled, [**glDrawArrays**](gldrawarrays.md), [**glDrawElements**](gldrawelements.md), and [**glArrayElement**](glarrayelement.md) use the texture coordinate array.</span></span> <span data-ttu-id="290cf-138">紋理座標陣列預設為停用。</span><span class="sxs-lookup"><span data-stu-id="290cf-138">By default the texture coordinate array is disabled.</span></span>

<span data-ttu-id="290cf-139">您無法在顯示清單中包含 **glTexCoordPointer** 。</span><span class="sxs-lookup"><span data-stu-id="290cf-139">You cannot include **glTexCoordPointer** in display lists.</span></span>

<span data-ttu-id="290cf-140">當您使用 **glTexCoordPointer** 指定紋理座標陣列時，所有函式的材質座標陣列參數值都會儲存在用戶端狀態中，而且可以快取靜態陣列元素。</span><span class="sxs-lookup"><span data-stu-id="290cf-140">When you specify a texture coordinate array using **glTexCoordPointer**, the values of all the function's texture coordinate array parameters are saved in a client-side state, and static array elements can be cached.</span></span> <span data-ttu-id="290cf-141">因為材質座標陣列參數是用戶端狀態，所以它們的值不會由 [**glPushAttrib**](glpushattrib.md) 和 [**glPopAttrib**](glpopattrib.md)儲存或還原。</span><span class="sxs-lookup"><span data-stu-id="290cf-141">Because the texture coordinate array parameters are client-side state, their values are not saved or restored by [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md).</span></span>

<span data-ttu-id="290cf-142">雖然在 [**glBegin**](glbegin.md)和 [**glEnd**](glend.md)配對內呼叫 **glTexCoordPointer** 時不會產生任何錯誤，但結果未定義。</span><span class="sxs-lookup"><span data-stu-id="290cf-142">Although no error is generated when you call **glTexCoordPointer** within [**glBegin**](glbegin.md) and [**glEnd**](glend.md) pairs, the results are undefined.</span></span>

<span data-ttu-id="290cf-143">下列函式會取出與 **glTexCoordPointer** 相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="290cf-143">The following functions retrieve information related to **glTexCoordPointer**:</span></span>

<span data-ttu-id="290cf-144">具有引數 **GL \_ 紋理 \_ COORD \_ 陣列** 的 [**glIsEnabled**](glisenabled.md)</span><span class="sxs-lookup"><span data-stu-id="290cf-144">[**glIsEnabled**](glisenabled.md) with argument **GL\_TEXTURE\_COORD\_ARRAY**</span></span>

<span data-ttu-id="290cf-145">具有引數 **GL \_ 紋理 \_ COORD \_ 陣列 \_ 大小** 的 [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)</span><span class="sxs-lookup"><span data-stu-id="290cf-145">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument **GL\_TEXTURE\_COORD\_ARRAY\_SIZE**</span></span>

<span data-ttu-id="290cf-146">**glGet** 與引數 **GL \_ 紋理 \_ COORD \_ 陣列 \_ STRIDE**</span><span class="sxs-lookup"><span data-stu-id="290cf-146">**glGet** with argument **GL\_TEXTURE\_COORD\_ARRAY\_STRIDE**</span></span>

<span data-ttu-id="290cf-147">具有引數 **GL \_ 紋理 \_ COORD \_ 陣列 \_ 計數** 的 **glGet**</span><span class="sxs-lookup"><span data-stu-id="290cf-147">**glGet** with argument **GL\_TEXTURE\_COORD\_ARRAY\_COUNT**</span></span>

<span data-ttu-id="290cf-148">具有引數 **GL \_ 紋理 \_ COORD \_ 陣列 \_ 類型** 的 **glGet**</span><span class="sxs-lookup"><span data-stu-id="290cf-148">**glGet** with argument **GL\_TEXTURE\_COORD\_ARRAY\_TYPE**</span></span>

<span data-ttu-id="290cf-149">具有引數 **GL \_ 紋理 \_ COORD \_ 陣列 \_ 指標** 的 [**glGetPointerv**](glgetpointerv.md)</span><span class="sxs-lookup"><span data-stu-id="290cf-149">[**glGetPointerv**](glgetpointerv.md) with argument **GL\_TEXTURE\_COORD\_ARRAY\_POINTER**</span></span>

## <a name="requirements"></a><span data-ttu-id="290cf-150">規格需求</span><span class="sxs-lookup"><span data-stu-id="290cf-150">Requirements</span></span>



| <span data-ttu-id="290cf-151">需求</span><span class="sxs-lookup"><span data-stu-id="290cf-151">Requirement</span></span> | <span data-ttu-id="290cf-152">值</span><span class="sxs-lookup"><span data-stu-id="290cf-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="290cf-153">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="290cf-153">Minimum supported client</span></span><br/> | <span data-ttu-id="290cf-154">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="290cf-154">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="290cf-155">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="290cf-155">Minimum supported server</span></span><br/> | <span data-ttu-id="290cf-156">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="290cf-156">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="290cf-157">標頭</span><span class="sxs-lookup"><span data-stu-id="290cf-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="290cf-158"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="290cf-158"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="290cf-159">程式庫</span><span class="sxs-lookup"><span data-stu-id="290cf-159">Library</span></span><br/>                  | <dl> <span data-ttu-id="290cf-160"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="290cf-160"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="290cf-161">DLL</span><span class="sxs-lookup"><span data-stu-id="290cf-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="290cf-162"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="290cf-162"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="290cf-163">另請參閱</span><span class="sxs-lookup"><span data-stu-id="290cf-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="290cf-164">**glArrayElement**</span><span class="sxs-lookup"><span data-stu-id="290cf-164">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="290cf-165">**glColorPointer**</span><span class="sxs-lookup"><span data-stu-id="290cf-165">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="290cf-166">**glDrawArrays**</span><span class="sxs-lookup"><span data-stu-id="290cf-166">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="290cf-167">**glDrawElements**</span><span class="sxs-lookup"><span data-stu-id="290cf-167">**glDrawElements**</span></span>](gldrawelements.md)
</dt> <dt>

[<span data-ttu-id="290cf-168">**glEdgeFlagPointer**</span><span class="sxs-lookup"><span data-stu-id="290cf-168">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="290cf-169">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="290cf-169">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="290cf-170">**glGetPointerv**</span><span class="sxs-lookup"><span data-stu-id="290cf-170">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="290cf-171">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="290cf-171">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="290cf-172">**glIndexPointer**</span><span class="sxs-lookup"><span data-stu-id="290cf-172">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="290cf-173">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="290cf-173">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="290cf-174">**glNormalPointer**</span><span class="sxs-lookup"><span data-stu-id="290cf-174">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="290cf-175">**glPopClientAttrib**</span><span class="sxs-lookup"><span data-stu-id="290cf-175">**glPopClientAttrib**</span></span>](glpopclientattrib.md)
</dt> <dt>

[<span data-ttu-id="290cf-176">**glPushClientAttrib**</span><span class="sxs-lookup"><span data-stu-id="290cf-176">**glPushClientAttrib**</span></span>](glpushclientattrib.md)
</dt> <dt>

[<span data-ttu-id="290cf-177">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="290cf-177">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="290cf-178">**glVertexPointer**</span><span class="sxs-lookup"><span data-stu-id="290cf-178">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





