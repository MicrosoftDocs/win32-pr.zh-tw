---
title: 'glDrawArrays 函式 (Gl) '
description: GlDrawArrays 函數會指定多個要轉譯的基本專案。
ms.assetid: 6ebd467b-5a63-43e4-b3fd-242c704d7d13
keywords:
- glDrawArrays 函式 OpenGL
topic_type:
- apiref
api_name:
- glDrawArrays
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88b20cf3a3e3b2c96a8172f53f8126815efe16d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934508"
---
# <a name="gldrawarrays-function"></a><span data-ttu-id="0fed1-104">glDrawArrays 函式</span><span class="sxs-lookup"><span data-stu-id="0fed1-104">glDrawArrays function</span></span>

<span data-ttu-id="0fed1-105">**GlDrawArrays** 函數會指定多個要轉譯的基本專案。</span><span class="sxs-lookup"><span data-stu-id="0fed1-105">The **glDrawArrays** function specifies multiple primitives to render.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fed1-106">語法</span><span class="sxs-lookup"><span data-stu-id="0fed1-106">Syntax</span></span>


```C++
void WINAPI glDrawArrays(
   GLenum  mode,
   GLint   first,
   GLsizei count
);
```



## <a name="parameters"></a><span data-ttu-id="0fed1-107">參數</span><span class="sxs-lookup"><span data-stu-id="0fed1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fed1-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="0fed1-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="0fed1-109">要轉譯的基本類型。</span><span class="sxs-lookup"><span data-stu-id="0fed1-109">The kind of primitives to render.</span></span> <span data-ttu-id="0fed1-110">下列常數指定可接受的基本類型： GL \_ 點、gl \_ 行 \_ 帶、gl \_ 線 \_ 迴圈、gl \_ 線、gl \_ 三角形區域 \_ 、gl \_ 三角形 \_ 風扇、gl \_ 三角形、gl \_ 四個區域 \_ 、gl \_ 四邊形和 gl \_ 多邊形。</span><span class="sxs-lookup"><span data-stu-id="0fed1-110">The following constants specify acceptable types of primitives: GL\_POINTS, GL\_LINE\_STRIP, GL\_LINE\_LOOP, GL\_LINES, GL\_TRIANGLE\_STRIP, GL\_TRIANGLE\_FAN, GL\_TRIANGLES, GL\_QUAD\_STRIP, GL\_QUADS, and GL\_POLYGON.</span></span>

</dd> <dt>

<span data-ttu-id="0fed1-111">*first*</span><span class="sxs-lookup"><span data-stu-id="0fed1-111">*first*</span></span> 
</dt> <dd>

<span data-ttu-id="0fed1-112">啟用的陣列中的起始索引。</span><span class="sxs-lookup"><span data-stu-id="0fed1-112">The starting index in the enabled arrays.</span></span>

</dd> <dt>

<span data-ttu-id="0fed1-113">*計數*</span><span class="sxs-lookup"><span data-stu-id="0fed1-113">*count*</span></span> 
</dt> <dd>

<span data-ttu-id="0fed1-114">要呈現的索引數目。</span><span class="sxs-lookup"><span data-stu-id="0fed1-114">The number of indexes to render.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0fed1-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="0fed1-115">Return value</span></span>

<span data-ttu-id="0fed1-116">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="0fed1-116">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0fed1-117">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="0fed1-117">Error codes</span></span>

<span data-ttu-id="0fed1-118">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="0fed1-118">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="0fed1-119">Name</span><span class="sxs-lookup"><span data-stu-id="0fed1-119">Name</span></span>                                                                                                  | <span data-ttu-id="0fed1-120">意義</span><span class="sxs-lookup"><span data-stu-id="0fed1-120">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0fed1-121"><dt>**GL \_ 無效 \_ 值**</dt></span><span class="sxs-lookup"><span data-stu-id="0fed1-121"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="0fed1-122">*計數* 為負數。</span><span class="sxs-lookup"><span data-stu-id="0fed1-122">*count* was negative.</span></span><br/>                                                                                                      |
| <dl> <span data-ttu-id="0fed1-123"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="0fed1-123"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="0fed1-124">*模式* 不是可接受的值。</span><span class="sxs-lookup"><span data-stu-id="0fed1-124">*mode* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="0fed1-125"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="0fed1-125"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="0fed1-126">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="0fed1-126">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="0fed1-127">備註</span><span class="sxs-lookup"><span data-stu-id="0fed1-127">Remarks</span></span>

<span data-ttu-id="0fed1-128">使用 **glDrawArrays**，您可以指定多個幾何基本型別來呈現。</span><span class="sxs-lookup"><span data-stu-id="0fed1-128">With **glDrawArrays**, you can specify multiple geometric primitives to render.</span></span> <span data-ttu-id="0fed1-129">除了呼叫個別的 OpenGL 函式來傳遞每個個別頂點、一般或色彩之外，您還可以指定不同的頂點、法線和色彩陣列，以定義一系列的基本專案， (所有相同種類) 與 **glDrawArrays** 的單一呼叫。</span><span class="sxs-lookup"><span data-stu-id="0fed1-129">Instead of calling separate OpenGL functions to pass each individual vertex, normal, or color, you can specify separate arrays of vertices, normals, and colors to define a sequence of primitives (all the same kind) with a single call to **glDrawArrays**.</span></span>

<span data-ttu-id="0fed1-130">當您呼叫 **glDrawArrays** 時，會使用每個已啟用陣列的連續元素 *計數* ，從 *第一個* 元素開始，用來建立一系列幾何基本專案。</span><span class="sxs-lookup"><span data-stu-id="0fed1-130">When you call **glDrawArrays**, *count* sequential elements from each enabled array are used to construct a sequence of geometric primitives, beginning with the *first* element.</span></span> <span data-ttu-id="0fed1-131">*Mode* 參數指定要建立的基本類型，以及如何使用陣列元素來建立基本專案。</span><span class="sxs-lookup"><span data-stu-id="0fed1-131">The *mode* parameter specifies what kind of primitive to construct and how to use the array elements to construct the primitives.</span></span>

<span data-ttu-id="0fed1-132">**GlDrawArrays** 傳回之後，由 **glDrawArrays** 修改的頂點屬性值為未定義。</span><span class="sxs-lookup"><span data-stu-id="0fed1-132">After **glDrawArrays** returns, the values of vertex attributes that are modified by **glDrawArrays** are undefined.</span></span> <span data-ttu-id="0fed1-133">例如，如果 \_ \_ 已啟用 GL 色彩陣列，則在 **glDrawArrays** 傳回之後，目前色彩的值會是未定義的。</span><span class="sxs-lookup"><span data-stu-id="0fed1-133">For example, if GL\_COLOR\_ARRAY is enabled, the value of the current color is undefined after **glDrawArrays** returns.</span></span> <span data-ttu-id="0fed1-134">**GlDrawArrays** 未修改的屬性仍會定義。</span><span class="sxs-lookup"><span data-stu-id="0fed1-134">Attributes not modified by **glDrawArrays** remain defined.</span></span> <span data-ttu-id="0fed1-135">如果 \_ \_ 未啟用 GL 頂點陣列，則不會產生任何幾何基本專案，但是會修改對應至已啟用陣列的屬性。</span><span class="sxs-lookup"><span data-stu-id="0fed1-135">When GL\_VERTEX\_ARRAY is not enabled, no geometric primitives are generated but the attributes corresponding to enabled arrays are modified.</span></span>

<span data-ttu-id="0fed1-136">您可以在顯示清單中包含 **glDrawArrays** 。</span><span class="sxs-lookup"><span data-stu-id="0fed1-136">You can include **glDrawArrays** in display lists.</span></span> <span data-ttu-id="0fed1-137">當您在顯示清單中包含 **glDrawArrays** 時，會在顯示清單中產生並輸入必要的陣列資料（由陣列指標和啟用所決定）。</span><span class="sxs-lookup"><span data-stu-id="0fed1-137">When you include **glDrawArrays** in a display list, the necessary array data, determined by the array pointers and the enables, are generated and entered in the display list.</span></span> <span data-ttu-id="0fed1-138">陣列指標和啟用的值會在建立顯示清單期間決定。</span><span class="sxs-lookup"><span data-stu-id="0fed1-138">The values of array pointers and enables are determined during the creation of display lists.</span></span>

<span data-ttu-id="0fed1-139">您可以隨時讀取靜態陣列資料。</span><span class="sxs-lookup"><span data-stu-id="0fed1-139">You can read static array data at any time.</span></span> <span data-ttu-id="0fed1-140">如果已修改任何靜態陣列元素，且未再次指定陣列，則任何後續呼叫 **glDrawArrays** 的結果都是未定義的。</span><span class="sxs-lookup"><span data-stu-id="0fed1-140">If any static array elements are modified and the array is not specified again, the results of any subsequent calls to **glDrawArrays** are undefined.</span></span>

<span data-ttu-id="0fed1-141">雖然當您在 [**glBegin**](glbegin.md) 和 [**glend**](glend.md) 配對中多次指定陣列時，不會產生任何錯誤，但結果是未定義的。</span><span class="sxs-lookup"><span data-stu-id="0fed1-141">Although no error is generated when you specify an array more than once within [**glBegin**](glbegin.md) and [**glend**](glend.md) pairs, the results are undefined.</span></span>

## <a name="requirements"></a><span data-ttu-id="0fed1-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="0fed1-142">Requirements</span></span>



| <span data-ttu-id="0fed1-143">需求</span><span class="sxs-lookup"><span data-stu-id="0fed1-143">Requirement</span></span> | <span data-ttu-id="0fed1-144">值</span><span class="sxs-lookup"><span data-stu-id="0fed1-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0fed1-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0fed1-145">Minimum supported client</span></span><br/> | <span data-ttu-id="0fed1-146">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0fed1-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="0fed1-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0fed1-147">Minimum supported server</span></span><br/> | <span data-ttu-id="0fed1-148">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0fed1-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0fed1-149">標頭</span><span class="sxs-lookup"><span data-stu-id="0fed1-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="0fed1-150"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="0fed1-150"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="0fed1-151">程式庫</span><span class="sxs-lookup"><span data-stu-id="0fed1-151">Library</span></span><br/>                  | <dl> <span data-ttu-id="0fed1-152"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="0fed1-152"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="0fed1-153">DLL</span><span class="sxs-lookup"><span data-stu-id="0fed1-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0fed1-154"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0fed1-154"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0fed1-155">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0fed1-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fed1-156">**glArrayElement**</span><span class="sxs-lookup"><span data-stu-id="0fed1-156">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="0fed1-157">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="0fed1-157">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="0fed1-158">**glColorPointer**</span><span class="sxs-lookup"><span data-stu-id="0fed1-158">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="0fed1-159">**glEdgeFlagPointer**</span><span class="sxs-lookup"><span data-stu-id="0fed1-159">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="0fed1-160">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="0fed1-160">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="0fed1-161">**glGetPointerv**</span><span class="sxs-lookup"><span data-stu-id="0fed1-161">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="0fed1-162">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="0fed1-162">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="0fed1-163">**glIndexPointer**</span><span class="sxs-lookup"><span data-stu-id="0fed1-163">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="0fed1-164">**glNormalPointer**</span><span class="sxs-lookup"><span data-stu-id="0fed1-164">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="0fed1-165">**glTexCoordPointer**</span><span class="sxs-lookup"><span data-stu-id="0fed1-165">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="0fed1-166">**glVertexPointer**</span><span class="sxs-lookup"><span data-stu-id="0fed1-166">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





