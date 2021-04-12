---
title: 'glIndexPointer 函式 (Gl) '
description: GlIndexPointer 函式會定義色彩索引的陣列。
ms.assetid: b435d950-1f87-4041-93e4-f1f8786cabdb
keywords:
- glIndexPointer 函式 OpenGL
topic_type:
- apiref
api_name:
- glIndexPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cca6858d7d1e3f13e4155bd40307a53b22e80a56
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464337"
---
# <a name="glindexpointer-function"></a><span data-ttu-id="05cdd-104">glIndexPointer 函式</span><span class="sxs-lookup"><span data-stu-id="05cdd-104">glIndexPointer function</span></span>

<span data-ttu-id="05cdd-105">**GlIndexPointer** 函式會定義色彩索引的陣列。</span><span class="sxs-lookup"><span data-stu-id="05cdd-105">The **glIndexPointer** function defines an array of color indexes.</span></span>

## <a name="syntax"></a><span data-ttu-id="05cdd-106">語法</span><span class="sxs-lookup"><span data-stu-id="05cdd-106">Syntax</span></span>


```C++
void WINAPI glIndexPointer(
         GLenum  type,
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a><span data-ttu-id="05cdd-107">參數</span><span class="sxs-lookup"><span data-stu-id="05cdd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05cdd-108">*type*</span><span class="sxs-lookup"><span data-stu-id="05cdd-108">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="05cdd-109">陣列中每個色彩索引的資料類型，使用下列符號常數： GL \_ SHORT、gl \_ INT、GL \_ FLOAT、gl \_ DOUBLE。</span><span class="sxs-lookup"><span data-stu-id="05cdd-109">The data type of each color index in the array using the following symbolic constants: GL\_SHORT, GL\_INT, GL\_FLOAT, GL\_DOUBLE.</span></span>

</dd> <dt>

<span data-ttu-id="05cdd-110">*大步*</span><span class="sxs-lookup"><span data-stu-id="05cdd-110">*stride*</span></span> 
</dt> <dd>

<span data-ttu-id="05cdd-111">連續色彩索引之間的位元組位移。</span><span class="sxs-lookup"><span data-stu-id="05cdd-111">The byte offset between consecutive color indexes.</span></span> <span data-ttu-id="05cdd-112">當 *stride* 為零時，色彩索引會緊密地封裝在陣列中。</span><span class="sxs-lookup"><span data-stu-id="05cdd-112">When *stride* is zero, the color indexes are tightly packed in the array.</span></span>

</dd> <dt>

<span data-ttu-id="05cdd-113">*指標*</span><span class="sxs-lookup"><span data-stu-id="05cdd-113">*pointer*</span></span> 
</dt> <dd>

<span data-ttu-id="05cdd-114">陣列中第一個色彩索引的指標。</span><span class="sxs-lookup"><span data-stu-id="05cdd-114">A pointer to the first color index in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05cdd-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="05cdd-115">Return value</span></span>

<span data-ttu-id="05cdd-116">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="05cdd-116">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="05cdd-117">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="05cdd-117">Error codes</span></span>

<span data-ttu-id="05cdd-118">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="05cdd-118">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="05cdd-119">Name</span><span class="sxs-lookup"><span data-stu-id="05cdd-119">Name</span></span>                                                                                              | <span data-ttu-id="05cdd-120">意義</span><span class="sxs-lookup"><span data-stu-id="05cdd-120">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="05cdd-121"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="05cdd-121"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>  | <span data-ttu-id="05cdd-122">*類型* 不是可接受的值。</span><span class="sxs-lookup"><span data-stu-id="05cdd-122">*type* was not an accepted value.</span></span><br/> |
| <dl> <span data-ttu-id="05cdd-123"><dt>**GL \_ 無效 \_ 值**</dt></span><span class="sxs-lookup"><span data-stu-id="05cdd-123"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="05cdd-124">*stride* 或 *計數* 為負數。</span><span class="sxs-lookup"><span data-stu-id="05cdd-124">*stride* or *count* was negative.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="05cdd-125">備註</span><span class="sxs-lookup"><span data-stu-id="05cdd-125">Remarks</span></span>

<span data-ttu-id="05cdd-126">**GlIndexPointer** 函式會指定轉譯時要使用之色彩索引陣列的位置和資料。</span><span class="sxs-lookup"><span data-stu-id="05cdd-126">The **glIndexPointer** function specifies the location and data of an array of color indexes to use when rendering.</span></span> <span data-ttu-id="05cdd-127">*Type* 參數指定每個色彩索引的資料類型 *，並決定* 從某個色彩索引到下一個色彩索引的位元組位移，以在單一陣列或不同陣列中的儲存區中封裝頂點和屬性。</span><span class="sxs-lookup"><span data-stu-id="05cdd-127">The *type* parameter specifies the data type of each color index and *stride* determines the byte offset from one color index to the next, enabling the packing of vertices and attributes in a single array or storage in separate arrays.</span></span> <span data-ttu-id="05cdd-128">在某些情況下，將頂點和屬性儲存在單一陣列中的效率可能比使用個別陣列更有效率。</span><span class="sxs-lookup"><span data-stu-id="05cdd-128">In some implementations, storing the vertices and attributes in a single array can be more efficient than using separate arrays.</span></span> <span data-ttu-id="05cdd-129">如需詳細資訊，請參閱 [**glInterleavedArrays**](glinterleavedarrays.md)。</span><span class="sxs-lookup"><span data-stu-id="05cdd-129">For more information, see [**glInterleavedArrays**](glinterleavedarrays.md).</span></span>

<span data-ttu-id="05cdd-130">當您 \_ \_ 使用 [**glEnableClientState**](glenableclientstate.md)指定 GL 索引陣列常數時，會啟用色彩索引陣列。</span><span class="sxs-lookup"><span data-stu-id="05cdd-130">A color-index array is enabled when you specify the GL\_INDEX\_ARRAY constant with [**glEnableClientState**](glenableclientstate.md).</span></span> <span data-ttu-id="05cdd-131">啟用時， [**glDrawArrays**](gldrawarrays.md) 和 [**glArrayElement**](glarrayelement.md) 會使用色彩索引陣列。</span><span class="sxs-lookup"><span data-stu-id="05cdd-131">When enabled, [**glDrawArrays**](gldrawarrays.md) and [**glArrayElement**](glarrayelement.md) use the color-index array.</span></span> <span data-ttu-id="05cdd-132">預設會停用色彩索引陣列。</span><span class="sxs-lookup"><span data-stu-id="05cdd-132">By default the color-index array is disabled.</span></span>

<span data-ttu-id="05cdd-133">您無法在顯示清單中包含 **glIndexPointer** 。</span><span class="sxs-lookup"><span data-stu-id="05cdd-133">You cannot include **glIndexPointer** in display lists.</span></span>

<span data-ttu-id="05cdd-134">當您使用 **glIndexPointer** 指定色彩索引陣列時，所有函式的色彩索引陣列參數值都會儲存在用戶端狀態，而且可以快取靜態陣列元素。</span><span class="sxs-lookup"><span data-stu-id="05cdd-134">When you specify a color-index array using **glIndexPointer**, the values of all the function's color-index array parameters are saved in a client-side state and static array elements can be cached.</span></span> <span data-ttu-id="05cdd-135">由於色彩索引陣列參數是用戶端狀態，因此 [**glPushAttrib**](glpushattrib.md) 和 **glPopAttrib** 不會儲存或還原它們的值。</span><span class="sxs-lookup"><span data-stu-id="05cdd-135">Because the color-index array parameters are client-side state, their values are not saved or restored by [**glPushAttrib**](glpushattrib.md) and **glPopAttrib**.</span></span>

<span data-ttu-id="05cdd-136">雖然在 [**glBegin**](glbegin.md)和 **glEnd** 配對內呼叫 **glIndexPointer** 時不會產生任何錯誤，但結果未定義。</span><span class="sxs-lookup"><span data-stu-id="05cdd-136">Although no error is generated when you call **glIndexPointer** within [**glBegin**](glbegin.md) and **glEnd** pairs, the results are undefined.</span></span>

<span data-ttu-id="05cdd-137">下列函式會取出與 **glIndexPointer** 相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="05cdd-137">The following functions retrieve information related to **glIndexPointer**:</span></span>

<span data-ttu-id="05cdd-138">[](glisenabled.md)具有引數 GL \_ 索引 \_ 陣列的 glIsEnabled</span><span class="sxs-lookup"><span data-stu-id="05cdd-138">[**glIsEnabled**](glisenabled.md) with argument GL\_INDEX\_ARRAY</span></span>

<span data-ttu-id="05cdd-139">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 索引 \_ 陣列 \_ STRIDE 的 glGet</span><span class="sxs-lookup"><span data-stu-id="05cdd-139">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_INDEX\_ARRAY\_STRIDE</span></span>

<span data-ttu-id="05cdd-140">具有引數 GL \_ 索引 \_ 陣列 \_ 計數的 glGet</span><span class="sxs-lookup"><span data-stu-id="05cdd-140">**glGet** with argument GL\_INDEX\_ARRAY\_COUNT</span></span>

<span data-ttu-id="05cdd-141">具有引數 GL \_ 索引 \_ 陣列 \_ 類型的 glGet</span><span class="sxs-lookup"><span data-stu-id="05cdd-141">**glGet** with argument GL\_INDEX\_ARRAY\_TYPE</span></span>

<span data-ttu-id="05cdd-142">具有引數 GL \_ 索引 \_ 陣列 \_ 大小的 glGet</span><span class="sxs-lookup"><span data-stu-id="05cdd-142">**glGet** with argument GL\_INDEX\_ARRAY\_SIZE</span></span>

<span data-ttu-id="05cdd-143">[](glgetpointerv.md)具有引數 GL \_ 索引 \_ 陣列 \_ 指標的 glGetPointerv</span><span class="sxs-lookup"><span data-stu-id="05cdd-143">[**glGetPointerv**](glgetpointerv.md) with argument GL\_INDEX\_ARRAY\_POINTER</span></span>

## <a name="requirements"></a><span data-ttu-id="05cdd-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="05cdd-144">Requirements</span></span>



| <span data-ttu-id="05cdd-145">需求</span><span class="sxs-lookup"><span data-stu-id="05cdd-145">Requirement</span></span> | <span data-ttu-id="05cdd-146">值</span><span class="sxs-lookup"><span data-stu-id="05cdd-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="05cdd-147">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="05cdd-147">Minimum supported client</span></span><br/> | <span data-ttu-id="05cdd-148">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="05cdd-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="05cdd-149">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="05cdd-149">Minimum supported server</span></span><br/> | <span data-ttu-id="05cdd-150">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="05cdd-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="05cdd-151">標頭</span><span class="sxs-lookup"><span data-stu-id="05cdd-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="05cdd-152"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="05cdd-152"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="05cdd-153">程式庫</span><span class="sxs-lookup"><span data-stu-id="05cdd-153">Library</span></span><br/>                  | <dl> <span data-ttu-id="05cdd-154"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="05cdd-154"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="05cdd-155">DLL</span><span class="sxs-lookup"><span data-stu-id="05cdd-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="05cdd-156"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05cdd-156"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05cdd-157">另請參閱</span><span class="sxs-lookup"><span data-stu-id="05cdd-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05cdd-158">**glArrayElement**</span><span class="sxs-lookup"><span data-stu-id="05cdd-158">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="05cdd-159">**glColorPointer**</span><span class="sxs-lookup"><span data-stu-id="05cdd-159">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="05cdd-160">**glDrawArrays**</span><span class="sxs-lookup"><span data-stu-id="05cdd-160">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="05cdd-161">**glEdgeFlagPointer**</span><span class="sxs-lookup"><span data-stu-id="05cdd-161">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="05cdd-162">**glGetPointerv**</span><span class="sxs-lookup"><span data-stu-id="05cdd-162">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="05cdd-163">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="05cdd-163">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="05cdd-164">**glNormalPointer**</span><span class="sxs-lookup"><span data-stu-id="05cdd-164">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="05cdd-165">**glPushAttrib**</span><span class="sxs-lookup"><span data-stu-id="05cdd-165">**glPushAttrib**</span></span>](glpushattrib.md)
</dt> <dt>

[<span data-ttu-id="05cdd-166">**glTexCoordPointer**</span><span class="sxs-lookup"><span data-stu-id="05cdd-166">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="05cdd-167">**glVertexPointer**</span><span class="sxs-lookup"><span data-stu-id="05cdd-167">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





