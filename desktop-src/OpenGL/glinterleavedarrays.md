---
title: 'glInterleavedArrays 函式 (Gl) '
description: GlInterleavedArrays 函式會同時指定並啟用大型匯總陣列中的數個交錯陣列。
ms.assetid: f1133949-d755-43e3-bf29-8e4c7fb17980
keywords:
- glInterleavedArrays 函式 OpenGL
topic_type:
- apiref
api_name:
- glInterleavedArrays
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41403210e78d1a65dd700561243846d6e45bad67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384118"
---
# <a name="glinterleavedarrays-function"></a><span data-ttu-id="63142-104">glInterleavedArrays 函式</span><span class="sxs-lookup"><span data-stu-id="63142-104">glInterleavedArrays function</span></span>

<span data-ttu-id="63142-105">**GlInterleavedArrays** 函式會同時指定並啟用大型匯總陣列中的數個交錯陣列。</span><span class="sxs-lookup"><span data-stu-id="63142-105">The **glInterleavedArrays** function simultaneously specifies and enables several interleaved arrays in a larger aggregate array.</span></span>

## <a name="syntax"></a><span data-ttu-id="63142-106">語法</span><span class="sxs-lookup"><span data-stu-id="63142-106">Syntax</span></span>


```C++
void WINAPI glInterleavedArrays(
         GLenum  format,
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a><span data-ttu-id="63142-107">參數</span><span class="sxs-lookup"><span data-stu-id="63142-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63142-108">*format*</span><span class="sxs-lookup"><span data-stu-id="63142-108">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="63142-109">要啟用的陣列類型。</span><span class="sxs-lookup"><span data-stu-id="63142-109">The type of array to enable.</span></span> <span data-ttu-id="63142-110">參數可以採用下列其中一個符號值： GL \_ V2F、gl \_ V3F、gl \_ C4UB \_ V2F、GL \_ C4UB \_ V3F、gl \_ C3F \_ V3F、gl \_ N3F V3F、gl C4F N3F V3F、 \_ \_ gl T2F \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ V3F、gl T4F V4F、gl T2F C4UB V3F、gl T2F C3F V3F、gl T2F N3F V3F、gl T2F C4F N3F V3F 或 gl T4F C4F N3F V4F。</span><span class="sxs-lookup"><span data-stu-id="63142-110">The parameter can assume one of the following symbolic values: GL\_V2F, GL\_V3F, GL\_C4UB\_V2F, GL\_C4UB\_V3F, GL\_C3F\_V3F, GL\_N3F\_V3F, GL\_C4F\_N3F\_V3F, GL\_T2F\_V3F, GL\_T4F\_V4F, GL\_T2F\_C4UB\_V3F, GL\_T2F\_C3F\_V3F, GL\_T2F\_N3F\_V3F, GL\_T2F\_C4F\_N3F\_V3F, or GL\_T4F\_C4F\_N3F\_V4F.</span></span>

</dd> <dt>

<span data-ttu-id="63142-111">*大步*</span><span class="sxs-lookup"><span data-stu-id="63142-111">*stride*</span></span> 
</dt> <dd>

<span data-ttu-id="63142-112">每個匯總陣列元素之間的位移（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="63142-112">The offset in bytes between each aggregate array element.</span></span>

</dd> <dt>

<span data-ttu-id="63142-113">*指標*</span><span class="sxs-lookup"><span data-stu-id="63142-113">*pointer*</span></span> 
</dt> <dd>

<span data-ttu-id="63142-114">匯總陣列中第一個元素的指標。</span><span class="sxs-lookup"><span data-stu-id="63142-114">A pointer to the first element of an aggregate array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63142-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="63142-115">Return value</span></span>

<span data-ttu-id="63142-116">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="63142-116">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="63142-117">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="63142-117">Error codes</span></span>

<span data-ttu-id="63142-118">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="63142-118">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="63142-119">Name</span><span class="sxs-lookup"><span data-stu-id="63142-119">Name</span></span>                                                                                                  | <span data-ttu-id="63142-120">意義</span><span class="sxs-lookup"><span data-stu-id="63142-120">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="63142-121"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="63142-121"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="63142-122">*格式* 不是可接受的值。</span><span class="sxs-lookup"><span data-stu-id="63142-122">*format* was not an accepted value.</span></span><br/>                                                                                        |
| <dl> <span data-ttu-id="63142-123"><dt>**GL \_ 無效 \_ 值**</dt></span><span class="sxs-lookup"><span data-stu-id="63142-123"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="63142-124">*stride* 為負數值。</span><span class="sxs-lookup"><span data-stu-id="63142-124">*stride* was a negative value.</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="63142-125"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="63142-125"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="63142-126">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="63142-126">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="63142-127">備註</span><span class="sxs-lookup"><span data-stu-id="63142-127">Remarks</span></span>

<span data-ttu-id="63142-128">使用 **glInterleavedArrays** 函式，您可以同時指定並啟用數個交錯色彩、標準、材質和頂點陣列，其專案是較大的匯總陣列元素的一部分。</span><span class="sxs-lookup"><span data-stu-id="63142-128">With the **glInterleavedArrays** function, you can simultaneously specify and enable several interleaved color, normal, texture, and vertex arrays whose elements are part of a larger aggregate array element.</span></span> <span data-ttu-id="63142-129">針對某些記憶體架構，這比個別指定陣列更有效率。</span><span class="sxs-lookup"><span data-stu-id="63142-129">For some memory architectures, this is more efficient than specifying the arrays separately.</span></span>

<span data-ttu-id="63142-130">如果 *stride* 參數為零，則會連續儲存匯總陣列元素;否則，在匯總陣列元素之間會發生 *跨距* 位元組。</span><span class="sxs-lookup"><span data-stu-id="63142-130">If the *stride* parameter is zero then the aggregate array elements are stored consecutively; otherwise *stride* bytes occur between aggregate array elements.</span></span>

<span data-ttu-id="63142-131">*Format* 參數可做為描述如何從匯總陣列解壓縮個別陣列的索引鍵：</span><span class="sxs-lookup"><span data-stu-id="63142-131">The *format* parameter serves as a key that describes how to extract individual arrays from the aggregate array:</span></span>

-   <span data-ttu-id="63142-132">如果 *格式* 包含 T，則會從交錯的陣列中解壓縮紋理座標。</span><span class="sxs-lookup"><span data-stu-id="63142-132">If *format* contains a T, then texture coordinates are extracted from the interleaved array.</span></span>
-   <span data-ttu-id="63142-133">如果有 C，則會將色彩值解壓縮。</span><span class="sxs-lookup"><span data-stu-id="63142-133">If C is present, color values are extracted.</span></span>
-   <span data-ttu-id="63142-134">如果有 N，則會將一般座標解壓縮。</span><span class="sxs-lookup"><span data-stu-id="63142-134">If N is present, normal coordinates are extracted.</span></span>
-   <span data-ttu-id="63142-135">一律會將頂點座標解壓縮。</span><span class="sxs-lookup"><span data-stu-id="63142-135">Vertex coordinates are always extracted.</span></span>
-   <span data-ttu-id="63142-136">數位2、3和4表示要解壓縮的值數目。</span><span class="sxs-lookup"><span data-stu-id="63142-136">The digits 2, 3, and 4 denote how many values are extracted.</span></span>
-   <span data-ttu-id="63142-137">F 表示將值解壓縮為浮點值。</span><span class="sxs-lookup"><span data-stu-id="63142-137">F indicates that values are extracted as floating point values.</span></span>
-   <span data-ttu-id="63142-138">如果4UB 遵循 C，則色彩也可以解壓縮為4個不帶正負號的位元組。</span><span class="sxs-lookup"><span data-stu-id="63142-138">If 4UB follows the C, colors may also be extracted as 4 unsigned bytes.</span></span> <span data-ttu-id="63142-139">如果將色彩解壓縮為4個不帶正負號的位元組，後面的頂點陣列元素會位於第一個可能的浮點對齊位址。</span><span class="sxs-lookup"><span data-stu-id="63142-139">If a color is extracted as 4 unsigned bytes, the vertex array element that follows is located at the first possible floating-point aligned address.</span></span>

<span data-ttu-id="63142-140">如果您在編譯顯示清單時呼叫 **glInterleavedArrays** ，它不會編譯成清單，而是會立即執行。</span><span class="sxs-lookup"><span data-stu-id="63142-140">If you call **glInterleavedArrays** while compiling a display list, it is not compiled into the list but is executed immediately.</span></span>

<span data-ttu-id="63142-141">在對 [**glBegin**](glbegin.md)的呼叫和 **glEnd** 的對應呼叫之間，不能包含 **glDisableClientState** 的 **glInterleavedArrays** 呼叫。</span><span class="sxs-lookup"><span data-stu-id="63142-141">You cannot include calls to **glInterleavedArrays** in **glDisableClientState** between calls to [**glBegin**](glbegin.md) and the corresponding call to **glEnd**.</span></span>

> [!Note]  
> <span data-ttu-id="63142-142">**GlInterleavedArrays** 函數僅適用于 OpenGL 1.1 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="63142-142">The **glInterleavedArrays** function is only available in OpenGL version 1.1 or later.</span></span>

 

<span data-ttu-id="63142-143">**GlInterleavedArrays** 函式是在不含通訊協定的用戶端上執行。</span><span class="sxs-lookup"><span data-stu-id="63142-143">The **glInterleavedArrays** function is implemented on the client side with no protocol.</span></span> <span data-ttu-id="63142-144">因為頂點陣列參數是用戶端狀態，所以它們不會由 [**glPushAttrib**](glpushattrib.md) 和 **glPopAttrib** 儲存或還原。</span><span class="sxs-lookup"><span data-stu-id="63142-144">Because the vertex array parameters are client-side state, they are not saved or restored by [**glPushAttrib**](glpushattrib.md) and **glPopAttrib**.</span></span> <span data-ttu-id="63142-145">請改用 [**glPushClientAttrib**](glpushclientattrib.md) 和 **glPopClientAttrib** 。</span><span class="sxs-lookup"><span data-stu-id="63142-145">Use [**glPushClientAttrib**](glpushclientattrib.md) and **glPopClientAttrib** instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="63142-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="63142-146">Requirements</span></span>



| <span data-ttu-id="63142-147">需求</span><span class="sxs-lookup"><span data-stu-id="63142-147">Requirement</span></span> | <span data-ttu-id="63142-148">值</span><span class="sxs-lookup"><span data-stu-id="63142-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="63142-149">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="63142-149">Minimum supported client</span></span><br/> | <span data-ttu-id="63142-150">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="63142-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="63142-151">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="63142-151">Minimum supported server</span></span><br/> | <span data-ttu-id="63142-152">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="63142-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="63142-153">標頭</span><span class="sxs-lookup"><span data-stu-id="63142-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="63142-154"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="63142-154"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="63142-155">程式庫</span><span class="sxs-lookup"><span data-stu-id="63142-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="63142-156"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="63142-156"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="63142-157">DLL</span><span class="sxs-lookup"><span data-stu-id="63142-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63142-158"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63142-158"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63142-159">另請參閱</span><span class="sxs-lookup"><span data-stu-id="63142-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63142-160">**glArrayElement**</span><span class="sxs-lookup"><span data-stu-id="63142-160">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="63142-161">**glColorPointer**</span><span class="sxs-lookup"><span data-stu-id="63142-161">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="63142-162">**glDrawArrays**</span><span class="sxs-lookup"><span data-stu-id="63142-162">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="63142-163">**glDrawElements**</span><span class="sxs-lookup"><span data-stu-id="63142-163">**glDrawElements**</span></span>](gldrawelements.md)
</dt> <dt>

[<span data-ttu-id="63142-164">**glEdgeFlagPointer**</span><span class="sxs-lookup"><span data-stu-id="63142-164">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="63142-165">**glEnableClientState**</span><span class="sxs-lookup"><span data-stu-id="63142-165">**glEnableClientState**</span></span>](glenableclientstate.md)
</dt> <dt>

[<span data-ttu-id="63142-166">**glGetPointerv**</span><span class="sxs-lookup"><span data-stu-id="63142-166">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="63142-167">**glIndexPointer**</span><span class="sxs-lookup"><span data-stu-id="63142-167">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="63142-168">**glNormalPointer**</span><span class="sxs-lookup"><span data-stu-id="63142-168">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="63142-169">**glPushAttrib**</span><span class="sxs-lookup"><span data-stu-id="63142-169">**glPushAttrib**</span></span>](glpushattrib.md)
</dt> <dt>

[<span data-ttu-id="63142-170">**glPushClientAttrib**</span><span class="sxs-lookup"><span data-stu-id="63142-170">**glPushClientAttrib**</span></span>](glpushclientattrib.md)
</dt> <dt>

[<span data-ttu-id="63142-171">**glTexCoordPointer**</span><span class="sxs-lookup"><span data-stu-id="63142-171">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="63142-172">**glVertexPointer**</span><span class="sxs-lookup"><span data-stu-id="63142-172">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





