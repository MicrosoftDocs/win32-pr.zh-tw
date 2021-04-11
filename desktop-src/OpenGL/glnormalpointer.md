---
title: 'glNormalPointer 函式 (Gl) '
description: GlNormalPointer 函式定義了法線的陣列。
ms.assetid: 6ffb0522-87cc-4be1-a5b1-f6fd30e04b43
keywords:
- glNormalPointer 函式 OpenGL
topic_type:
- apiref
api_name:
- glNormalPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c2f3abbfbd989351af647557ec64f8ee3172dc5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935115"
---
# <a name="glnormalpointer-function"></a><span data-ttu-id="a9a93-104">glNormalPointer 函式</span><span class="sxs-lookup"><span data-stu-id="a9a93-104">glNormalPointer function</span></span>

<span data-ttu-id="a9a93-105">**GlNormalPointer** 函式定義了法線的陣列。</span><span class="sxs-lookup"><span data-stu-id="a9a93-105">The **glNormalPointer** function defines an array of normals.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9a93-106">語法</span><span class="sxs-lookup"><span data-stu-id="a9a93-106">Syntax</span></span>


```C++
void WINAPI glNormalPointer(
         GLenum  type,
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a><span data-ttu-id="a9a93-107">參數</span><span class="sxs-lookup"><span data-stu-id="a9a93-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9a93-108">*type*</span><span class="sxs-lookup"><span data-stu-id="a9a93-108">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="a9a93-109">陣列中每個座標的資料類型，使用下列符號常數： GL \_ BYTE、gl \_ SHORT、GL \_ INT、GL \_ FLOAT 和 gl \_ DOUBLE。</span><span class="sxs-lookup"><span data-stu-id="a9a93-109">The data type of each coordinate in the array using the following symbolic constants: GL\_BYTE, GL\_SHORT, GL\_INT, GL\_FLOAT, and GL\_DOUBLE.</span></span>

</dd> <dt>

<span data-ttu-id="a9a93-110">*大步*</span><span class="sxs-lookup"><span data-stu-id="a9a93-110">*stride*</span></span> 
</dt> <dd>

<span data-ttu-id="a9a93-111">連續法線之間的位元組位移。</span><span class="sxs-lookup"><span data-stu-id="a9a93-111">The byte offset between consecutive normals.</span></span> <span data-ttu-id="a9a93-112">當 *stride* 為零時，就會將法線緊密地封裝在陣列中。</span><span class="sxs-lookup"><span data-stu-id="a9a93-112">When *stride* is zero, the normals are tightly packed in the array.</span></span>

</dd> <dt>

<span data-ttu-id="a9a93-113">*指標*</span><span class="sxs-lookup"><span data-stu-id="a9a93-113">*pointer*</span></span> 
</dt> <dd>

<span data-ttu-id="a9a93-114">陣列中第一個法線的指標。</span><span class="sxs-lookup"><span data-stu-id="a9a93-114">A pointer to the first normal in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9a93-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="a9a93-115">Return value</span></span>

<span data-ttu-id="a9a93-116">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="a9a93-116">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a9a93-117">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="a9a93-117">Error codes</span></span>

<span data-ttu-id="a9a93-118">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="a9a93-118">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="a9a93-119">Name</span><span class="sxs-lookup"><span data-stu-id="a9a93-119">Name</span></span>                                                                                                  | <span data-ttu-id="a9a93-120">意義</span><span class="sxs-lookup"><span data-stu-id="a9a93-120">Meaning</span></span>                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="a9a93-121"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="a9a93-121"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="a9a93-122">*類型* 不是可接受的值。</span><span class="sxs-lookup"><span data-stu-id="a9a93-122">*type* was not an accepted value.</span></span><br/> |
| <dl> <span data-ttu-id="a9a93-123"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="a9a93-123"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="a9a93-124">*stride* 或 *計數* 為負數。</span><span class="sxs-lookup"><span data-stu-id="a9a93-124">*stride* or *count* was negative.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="a9a93-125">備註</span><span class="sxs-lookup"><span data-stu-id="a9a93-125">Remarks</span></span>

<span data-ttu-id="a9a93-126">**GlNormalPointer** 函式會指定轉譯時要使用之法線陣列的位置和資料。</span><span class="sxs-lookup"><span data-stu-id="a9a93-126">The **glNormalPointer** function specifies the location and data of an array of normals to use when rendering.</span></span> <span data-ttu-id="a9a93-127">*Type* 參數指定每個一般座標的資料類型。</span><span class="sxs-lookup"><span data-stu-id="a9a93-127">The *type* parameter specifies the data type of each normal coordinate.</span></span> <span data-ttu-id="a9a93-128">*Stride* 參數會決定從一個標準到下一個標準的位元組位移，以便將單一陣列或儲存區中的頂點和屬性封裝成不同的陣列。</span><span class="sxs-lookup"><span data-stu-id="a9a93-128">The *stride* parameter determines the byte offset from one normal to the next, enabling the packing of vertices and attributes in a single array or storage in separate arrays.</span></span> <span data-ttu-id="a9a93-129">在某些執行中，將頂點和屬性儲存在單一陣列中的效率可能比使用個別陣列更有效率;如需詳細資訊，請參閱 [**glInterleavedArrays**](glinterleavedarrays.md) 。</span><span class="sxs-lookup"><span data-stu-id="a9a93-129">In some implementations storing the vertices and attributes in a single array can be more efficient than using separate arrays; see [**glInterleavedArrays**](glinterleavedarrays.md) for details.</span></span>

<span data-ttu-id="a9a93-130">當您 \_ \_ 使用 [**glEnableClientState**](glenableclientstate.md)指定 GL 一般陣列常數時，會啟用一般陣列。</span><span class="sxs-lookup"><span data-stu-id="a9a93-130">A normal array is enabled when you specify the GL\_NORMAL\_ARRAY constant with [**glEnableClientState**](glenableclientstate.md).</span></span> <span data-ttu-id="a9a93-131">啟用時， [**glDrawArrays**](gldrawarrays.md)、 [**glDrawElements**](gldrawelements.md) 和 [**glArrayElement**](glarrayelement.md) 會使用一般陣列。</span><span class="sxs-lookup"><span data-stu-id="a9a93-131">When enabled, [**glDrawArrays**](gldrawarrays.md), [**glDrawElements**](gldrawelements.md) and [**glArrayElement**](glarrayelement.md) use the normal array.</span></span> <span data-ttu-id="a9a93-132">預設會停用一般陣列。</span><span class="sxs-lookup"><span data-stu-id="a9a93-132">By default the normal array is disabled.</span></span>

<span data-ttu-id="a9a93-133">您無法在顯示清單中包含 **glNormalPointer** 。</span><span class="sxs-lookup"><span data-stu-id="a9a93-133">You cannot include **glNormalPointer** in display lists.</span></span>

<span data-ttu-id="a9a93-134">當您使用 **glNormalPointer** 指定一般陣列時，所有函式的一般陣列參數值都會儲存在用戶端狀態。</span><span class="sxs-lookup"><span data-stu-id="a9a93-134">When you specify a normal array using **glNormalPointer**, the values of all the function's normal array parameters are saved in a client-side state.</span></span> <span data-ttu-id="a9a93-135">由於一般陣列參數會儲存在用戶端狀態中，因此 [**glPushAttrib**](glpushattrib.md) 和 [**glPopAttrib**](glpopattrib.md)不會儲存或還原它們的值。</span><span class="sxs-lookup"><span data-stu-id="a9a93-135">Because the normal array parameters are saved in a client-side state, their values are not saved or restored by [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md).</span></span>

<span data-ttu-id="a9a93-136">雖然在 [**glBegin**](glbegin.md)和 [**glEnd**](glend.md)配對內呼叫 **glNormalPointer** 時不會產生任何錯誤，但結果未定義。</span><span class="sxs-lookup"><span data-stu-id="a9a93-136">Although no error is generated when you call **glNormalPointer** within [**glBegin**](glbegin.md) and [**glEnd**](glend.md) pairs, the results are undefined.</span></span>

<span data-ttu-id="a9a93-137">下列是與 **glNormalPointer** 相關聯的函式：</span><span class="sxs-lookup"><span data-stu-id="a9a93-137">The following functions are associated with **glNormalPointer**:</span></span>

<span data-ttu-id="a9a93-138">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 標準 \_ 陣列 \_ STRIDE 的 glGet</span><span class="sxs-lookup"><span data-stu-id="a9a93-138">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_NORMAL\_ARRAY\_STRIDE</span></span>

<span data-ttu-id="a9a93-139">具有引數 GL \_ 標準 \_ 陣列 \_ 計數的 glGet</span><span class="sxs-lookup"><span data-stu-id="a9a93-139">**glGet** with argument GL\_NORMAL\_ARRAY\_COUNT</span></span>

<span data-ttu-id="a9a93-140">具有引數 GL \_ 一般 \_ 陣列 \_ 類型的 glGet</span><span class="sxs-lookup"><span data-stu-id="a9a93-140">**glGet** with argument GL\_NORMAL\_ARRAY\_TYPE</span></span>

<span data-ttu-id="a9a93-141">具有引數 GL \_ 一般 \_ 陣列 \_ 指標的 glGetPointerv</span><span class="sxs-lookup"><span data-stu-id="a9a93-141">**glGetPointerv** with argument GL\_NORMAL\_ARRAY\_POINTER</span></span>

<span data-ttu-id="a9a93-142">[](glisenabled.md)具有引數 GL \_ 一般 \_ 陣列的 glIsEnabled</span><span class="sxs-lookup"><span data-stu-id="a9a93-142">[**glIsEnabled**](glisenabled.md) with argument GL\_NORMAL\_ARRAY</span></span>

## <a name="requirements"></a><span data-ttu-id="a9a93-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="a9a93-143">Requirements</span></span>



| <span data-ttu-id="a9a93-144">需求</span><span class="sxs-lookup"><span data-stu-id="a9a93-144">Requirement</span></span> | <span data-ttu-id="a9a93-145">值</span><span class="sxs-lookup"><span data-stu-id="a9a93-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a9a93-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a9a93-146">Minimum supported client</span></span><br/> | <span data-ttu-id="a9a93-147">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a9a93-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a9a93-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a9a93-148">Minimum supported server</span></span><br/> | <span data-ttu-id="a9a93-149">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a9a93-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a9a93-150">標頭</span><span class="sxs-lookup"><span data-stu-id="a9a93-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9a93-151"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="a9a93-151"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="a9a93-152">程式庫</span><span class="sxs-lookup"><span data-stu-id="a9a93-152">Library</span></span><br/>                  | <dl> <span data-ttu-id="a9a93-153"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a9a93-153"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="a9a93-154">DLL</span><span class="sxs-lookup"><span data-stu-id="a9a93-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9a93-155"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a9a93-155"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9a93-156">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a9a93-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9a93-157">**glArrayElement**</span><span class="sxs-lookup"><span data-stu-id="a9a93-157">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="a9a93-158">**glColorPointer**</span><span class="sxs-lookup"><span data-stu-id="a9a93-158">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="a9a93-159">**glDrawElements**</span><span class="sxs-lookup"><span data-stu-id="a9a93-159">**glDrawElements**</span></span>](gldrawelements.md)
</dt> <dt>

[<span data-ttu-id="a9a93-160">**glDrawArrays**</span><span class="sxs-lookup"><span data-stu-id="a9a93-160">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="a9a93-161">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="a9a93-161">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="a9a93-162">**glEdgeFlagPointer**</span><span class="sxs-lookup"><span data-stu-id="a9a93-162">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="a9a93-163">**glGetPointerv**</span><span class="sxs-lookup"><span data-stu-id="a9a93-163">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="a9a93-164">**glIndexPointer**</span><span class="sxs-lookup"><span data-stu-id="a9a93-164">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="a9a93-165">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="a9a93-165">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="a9a93-166">**glInterleavedArrays**</span><span class="sxs-lookup"><span data-stu-id="a9a93-166">**glInterleavedArrays**</span></span>](glinterleavedarrays.md)
</dt> <dt>

[<span data-ttu-id="a9a93-167">**glTexCoordPointer**</span><span class="sxs-lookup"><span data-stu-id="a9a93-167">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="a9a93-168">**glVertexPointer**</span><span class="sxs-lookup"><span data-stu-id="a9a93-168">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> <dt>

[<span data-ttu-id="a9a93-169">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="a9a93-169">**glGetString**</span></span>](glgetstring.md)
</dt> </dl>

 

 





