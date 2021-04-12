---
title: 'glColorPointer 函式 (Gl) '
description: GlColorPointer 函式會定義色彩的陣列。
ms.assetid: 4d9d05fb-691d-4b71-b079-c42dc7103055
keywords:
- glColorPointer 函式 OpenGL
topic_type:
- apiref
api_name:
- glColorPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9abced52f0d0664e998ad8380e33d43d4af36bcc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464728"
---
# <a name="glcolorpointer-function"></a><span data-ttu-id="44603-104">glColorPointer 函式</span><span class="sxs-lookup"><span data-stu-id="44603-104">glColorPointer function</span></span>

<span data-ttu-id="44603-105">**GlColorPointer** 函式會定義色彩的陣列。</span><span class="sxs-lookup"><span data-stu-id="44603-105">The **glColorPointer** function defines an array of colors.</span></span>

## <a name="syntax"></a><span data-ttu-id="44603-106">語法</span><span class="sxs-lookup"><span data-stu-id="44603-106">Syntax</span></span>


```C++
void WINAPI glColorPointer(
         GLint   size,
         GLenum  type,
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a><span data-ttu-id="44603-107">參數</span><span class="sxs-lookup"><span data-stu-id="44603-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44603-108">*size*</span><span class="sxs-lookup"><span data-stu-id="44603-108">*size*</span></span> 
</dt> <dd>

<span data-ttu-id="44603-109">每一色彩的元件數目。</span><span class="sxs-lookup"><span data-stu-id="44603-109">The number of components per color.</span></span> <span data-ttu-id="44603-110">值必須是3或4。</span><span class="sxs-lookup"><span data-stu-id="44603-110">The value must be either 3 or 4.</span></span>

</dd> <dt>

<span data-ttu-id="44603-111">*type*</span><span class="sxs-lookup"><span data-stu-id="44603-111">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="44603-112">色彩陣列中每個色彩元件的資料類型。</span><span class="sxs-lookup"><span data-stu-id="44603-112">The data type of each color component in a color array.</span></span> <span data-ttu-id="44603-113">您可以使用下列常數指定可接受的資料類型： GL \_ 位元組、gl \_ 無符號 \_ 位元組、GL \_ short、gl 不 \_ 帶正負號 \_ 簡短、gl \_ int、GL 不 \_ 帶正負號 \_ INT、gl \_ FLOAT 或 GL \_ DOUBLE。</span><span class="sxs-lookup"><span data-stu-id="44603-113">Acceptable data types are specified with the following constants: GL\_BYTE, GL\_UNSIGNED\_BYTE, GL\_SHORT, GL\_UNSIGNED\_SHORT, GL\_INT, GL\_UNSIGNED\_INT, GL\_FLOAT, or GL\_DOUBLE.</span></span>

</dd> <dt>

<span data-ttu-id="44603-114">*大步*</span><span class="sxs-lookup"><span data-stu-id="44603-114">*stride*</span></span> 
</dt> <dd>

<span data-ttu-id="44603-115">連續色彩之間的位元組位移。</span><span class="sxs-lookup"><span data-stu-id="44603-115">The byte offset between consecutive colors.</span></span> <span data-ttu-id="44603-116">當 *stride* 為零時，色彩會緊密地封裝在陣列中。</span><span class="sxs-lookup"><span data-stu-id="44603-116">When *stride* is zero, the colors are tightly packed in the array.</span></span>

</dd> <dt>

<span data-ttu-id="44603-117">*指標*</span><span class="sxs-lookup"><span data-stu-id="44603-117">*pointer*</span></span> 
</dt> <dd>

<span data-ttu-id="44603-118">色彩陣列中第一個 color 元素第一個元件的指標。</span><span class="sxs-lookup"><span data-stu-id="44603-118">A pointer to the first component of the first color element in a color array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44603-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="44603-119">Return value</span></span>

<span data-ttu-id="44603-120">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="44603-120">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="44603-121">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="44603-121">Error codes</span></span>

<span data-ttu-id="44603-122">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="44603-122">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="44603-123">Name</span><span class="sxs-lookup"><span data-stu-id="44603-123">Name</span></span>                                                                                              | <span data-ttu-id="44603-124">意義</span><span class="sxs-lookup"><span data-stu-id="44603-124">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="44603-125"><dt>**GL \_ 無效 \_ 值**</dt></span><span class="sxs-lookup"><span data-stu-id="44603-125"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="44603-126">*大小* 不是3或4。</span><span class="sxs-lookup"><span data-stu-id="44603-126">*size* was not 3 or 4.</span></span><br/>            |
| <dl> <span data-ttu-id="44603-127"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="44603-127"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>  | <span data-ttu-id="44603-128">*類型* 不是可接受的值。</span><span class="sxs-lookup"><span data-stu-id="44603-128">*type* was not an accepted value.</span></span><br/> |
| <dl> <span data-ttu-id="44603-129"><dt>**GL \_ 無效 \_ 值**</dt></span><span class="sxs-lookup"><span data-stu-id="44603-129"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="44603-130">*stride* 或 *計數* 為負數。</span><span class="sxs-lookup"><span data-stu-id="44603-130">*stride* or *count* was negative.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="44603-131">備註</span><span class="sxs-lookup"><span data-stu-id="44603-131">Remarks</span></span>

<span data-ttu-id="44603-132">**GlColorPointer** 函式會指定轉譯時要使用之色彩元件陣列的位置和資料格式。</span><span class="sxs-lookup"><span data-stu-id="44603-132">The **glColorPointer** function specifies the location and data format of an array of color components to use when rendering.</span></span> <span data-ttu-id="44603-133">*Stride* 參數會決定從某種色彩到下一個色彩的位元組位移，以便將單一陣列或儲存區中的頂點屬性封裝成不同的陣列。</span><span class="sxs-lookup"><span data-stu-id="44603-133">The *stride* parameter determines the byte offset from one color to the next, enabling the packing of vertex attributes in a single array or storage in separate arrays.</span></span> <span data-ttu-id="44603-134">在某些情況下，在單一陣列中儲存頂點屬性，會比使用個別陣列更有效率。</span><span class="sxs-lookup"><span data-stu-id="44603-134">In some implementations, storing vertex attributes in a single array can be more efficient than the use of separate arrays.</span></span>

<span data-ttu-id="44603-135">藉由 \_ \_ 使用 [**glEnableClientState**](glenableclientstate.md)指定 GL 色彩陣列常數來啟用色彩陣列。</span><span class="sxs-lookup"><span data-stu-id="44603-135">Enabled the color array by specifying the GL\_COLOR\_ARRAY constant with [**glEnableClientState**](glenableclientstate.md).</span></span> <span data-ttu-id="44603-136">呼叫 [**glArrayElement**](glarrayelement.md)、 [**glDrawElements**](gldrawelements.md)或 [**glDrawArrays**](gldrawarrays.md) 會使用因此啟用的色彩陣列。</span><span class="sxs-lookup"><span data-stu-id="44603-136">Calling [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md), or [**glDrawArrays**](gldrawarrays.md) uses the color array that is thus enabled.</span></span> <span data-ttu-id="44603-137">預設會停用色彩陣列。</span><span class="sxs-lookup"><span data-stu-id="44603-137">By default, the color array is disabled.</span></span> <span data-ttu-id="44603-138">**GlColorPointer** 呼叫不能藉由在顯示清單中輸入。</span><span class="sxs-lookup"><span data-stu-id="44603-138">The **glColorPointer** calls cannot by entered in display lists.</span></span>

<span data-ttu-id="44603-139">當您使用 **glColorPointer** 指定色彩陣列時，所有函式的色彩陣列參數值都會儲存在用戶端狀態，而且您可以快取靜態陣列元素。</span><span class="sxs-lookup"><span data-stu-id="44603-139">When you specify a color array using **glColorPointer**, the values of all the function's color array parameters are saved in a client-side state, and you can cache static array elements.</span></span> <span data-ttu-id="44603-140">因為色彩陣列參數處於用戶端狀態， [**glPushAttrib**](glpushattrib.md) 和 [**glPopAttrib**](glpopattrib.md) 不會儲存或還原參數的值。</span><span class="sxs-lookup"><span data-stu-id="44603-140">Because the color array parameters are in a client-side state, [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md) do not save or restore the parameters' values.</span></span>

<span data-ttu-id="44603-141">雖然在 [**glBegin**](glbegin.md) 和 [**glend**](glend.md) 配對內指定色彩陣列並不會產生錯誤，但結果卻是未定義的。</span><span class="sxs-lookup"><span data-stu-id="44603-141">Although specifying the color array within [**glBegin**](glbegin.md) and [**glend**](glend.md) pairs does not generate an error, the results are undefined.</span></span>

<span data-ttu-id="44603-142">下列函式會取出與 **glColorPointer** 函數相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="44603-142">The following functions retrieve information related to the **glColorPointer** function:</span></span>

<span data-ttu-id="44603-143">[](glisenabled.md)具有引數 GL \_ 色彩 \_ 陣列的 glIsEnabled</span><span class="sxs-lookup"><span data-stu-id="44603-143">[**glIsEnabled**](glisenabled.md) with argument GL\_COLOR\_ARRAY</span></span>

<span data-ttu-id="44603-144">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 色彩 \_ 陣列 \_ 大小的 glGet</span><span class="sxs-lookup"><span data-stu-id="44603-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_COLOR\_ARRAY\_SIZE</span></span>

<span data-ttu-id="44603-145">具有引數 GL \_ 色彩 \_ 陣列 \_ 類型的 glGet</span><span class="sxs-lookup"><span data-stu-id="44603-145">**glGet** with argument GL\_COLOR\_ARRAY\_TYPE</span></span>

<span data-ttu-id="44603-146">具有引數 GL \_ 色彩 \_ 陣列 \_ STRIDE 的 glGet</span><span class="sxs-lookup"><span data-stu-id="44603-146">**glGet** with argument GL\_COLOR\_ARRAY\_STRIDE</span></span>

<span data-ttu-id="44603-147">具有引數 GL \_ 色彩 \_ 陣列 \_ 計數的 glGet</span><span class="sxs-lookup"><span data-stu-id="44603-147">**glGet** with argument GL\_COLOR\_ARRAY\_COUNT</span></span>

<span data-ttu-id="44603-148">[](glgetpointerv.md)具有引數 GL \_ 色彩 \_ 陣列 \_ 指標的 glGetPointerv</span><span class="sxs-lookup"><span data-stu-id="44603-148">[**glGetPointerv**](glgetpointerv.md) with argument GL\_COLOR\_ARRAY\_POINTER</span></span>

## <a name="requirements"></a><span data-ttu-id="44603-149">規格需求</span><span class="sxs-lookup"><span data-stu-id="44603-149">Requirements</span></span>



| <span data-ttu-id="44603-150">需求</span><span class="sxs-lookup"><span data-stu-id="44603-150">Requirement</span></span> | <span data-ttu-id="44603-151">值</span><span class="sxs-lookup"><span data-stu-id="44603-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="44603-152">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="44603-152">Minimum supported client</span></span><br/> | <span data-ttu-id="44603-153">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="44603-153">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="44603-154">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="44603-154">Minimum supported server</span></span><br/> | <span data-ttu-id="44603-155">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="44603-155">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="44603-156">標頭</span><span class="sxs-lookup"><span data-stu-id="44603-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="44603-157"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="44603-157"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="44603-158">程式庫</span><span class="sxs-lookup"><span data-stu-id="44603-158">Library</span></span><br/>                  | <dl> <span data-ttu-id="44603-159"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="44603-159"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="44603-160">DLL</span><span class="sxs-lookup"><span data-stu-id="44603-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44603-161"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44603-161"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44603-162">另請參閱</span><span class="sxs-lookup"><span data-stu-id="44603-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44603-163">**glArrayElement**</span><span class="sxs-lookup"><span data-stu-id="44603-163">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="44603-164">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="44603-164">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="44603-165">**glDrawArrays**</span><span class="sxs-lookup"><span data-stu-id="44603-165">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="44603-166">**glEdgeFlagPointer**</span><span class="sxs-lookup"><span data-stu-id="44603-166">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="44603-167">**glEnableClientState**</span><span class="sxs-lookup"><span data-stu-id="44603-167">**glEnableClientState**</span></span>](glenableclientstate.md)
</dt> <dt>

[<span data-ttu-id="44603-168">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="44603-168">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="44603-169">**glGet**</span><span class="sxs-lookup"><span data-stu-id="44603-169">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="44603-170">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="44603-170">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="44603-171">**glGetPointerv**</span><span class="sxs-lookup"><span data-stu-id="44603-171">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="44603-172">**glIndexPointer**</span><span class="sxs-lookup"><span data-stu-id="44603-172">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="44603-173">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="44603-173">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="44603-174">**glNormalPointer**</span><span class="sxs-lookup"><span data-stu-id="44603-174">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="44603-175">**glPopAttrib**</span><span class="sxs-lookup"><span data-stu-id="44603-175">**glPopAttrib**</span></span>](glpopattrib.md)
</dt> <dt>

[<span data-ttu-id="44603-176">**glPushAttrib**</span><span class="sxs-lookup"><span data-stu-id="44603-176">**glPushAttrib**</span></span>](glpushattrib.md)
</dt> <dt>

[<span data-ttu-id="44603-177">**glTexCoordPointer**</span><span class="sxs-lookup"><span data-stu-id="44603-177">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="44603-178">**glVertexPointer**</span><span class="sxs-lookup"><span data-stu-id="44603-178">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





