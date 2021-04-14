---
title: 'glDrawElements 函式 (Gl) '
description: GlDrawElements 函式會從陣列資料呈現基本專案。
ms.assetid: fb433294-106e-48d5-ad49-4434934fe072
keywords:
- glDrawElements 函式 OpenGL
topic_type:
- apiref
api_name:
- glDrawElements
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 976e779235dc330467d610406156534b5e72841d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508791"
---
# <a name="gldrawelements-function"></a><span data-ttu-id="d6a33-104">glDrawElements 函式</span><span class="sxs-lookup"><span data-stu-id="d6a33-104">glDrawElements function</span></span>

<span data-ttu-id="d6a33-105">**GlDrawElements** 函式會從陣列資料呈現基本專案。</span><span class="sxs-lookup"><span data-stu-id="d6a33-105">The **glDrawElements** function renders primitives from array data.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6a33-106">語法</span><span class="sxs-lookup"><span data-stu-id="d6a33-106">Syntax</span></span>


```C++
void WINAPI glDrawElements(
         GLenum  mode,
         GLsizei count,
         GLenum  type,
   const GLvoid  *indices
);
```



## <a name="parameters"></a><span data-ttu-id="d6a33-107">參數</span><span class="sxs-lookup"><span data-stu-id="d6a33-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6a33-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="d6a33-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="d6a33-109">要轉譯的基本類型。</span><span class="sxs-lookup"><span data-stu-id="d6a33-109">The kind of primitives to render.</span></span> <span data-ttu-id="d6a33-110">它可以採用下列其中一個符號值： GL \_ 點、gl \_ 線區域 \_ 、gl \_ 線 \_ 迴圈、gl \_ 線、gl 三角形區域 \_ \_ 、gl \_ 三角形 \_ 風扇、gl \_ 三角形、gl \_ QUAD \_ 、gl \_ 四邊形和 gl \_ 多邊形。</span><span class="sxs-lookup"><span data-stu-id="d6a33-110">It can assume one of the following symbolic values: GL\_POINTS, GL\_LINE\_STRIP, GL\_LINE\_LOOP, GL\_LINES, GL\_TRIANGLE\_STRIP, GL\_TRIANGLE\_FAN, GL\_TRIANGLES, GL\_QUAD\_STRIP, GL\_QUADS, and GL\_POLYGON.</span></span>

</dd> <dt>

<span data-ttu-id="d6a33-111">*計數*</span><span class="sxs-lookup"><span data-stu-id="d6a33-111">*count*</span></span> 
</dt> <dd>

<span data-ttu-id="d6a33-112">要呈現的元素數目。</span><span class="sxs-lookup"><span data-stu-id="d6a33-112">The number of elements to be rendered.</span></span>

</dd> <dt>

<span data-ttu-id="d6a33-113">*type*</span><span class="sxs-lookup"><span data-stu-id="d6a33-113">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="d6a33-114">索引中值的型別。</span><span class="sxs-lookup"><span data-stu-id="d6a33-114">The type of the values in indices.</span></span> <span data-ttu-id="d6a33-115">必須是 GL 不 \_ 帶正負號的 \_ 位元組、gl 不 \_ 帶正負號的 \_ 整數或 gl 不 \_ 帶正負號整數之一 \_ 。</span><span class="sxs-lookup"><span data-stu-id="d6a33-115">Must be one of GL\_UNSIGNED\_BYTE, GL\_UNSIGNED\_SHORT, or GL\_UNSIGNED\_INT.</span></span>

</dd> <dt>

<span data-ttu-id="d6a33-116">*指標*</span><span class="sxs-lookup"><span data-stu-id="d6a33-116">*indices*</span></span> 
</dt> <dd>

<span data-ttu-id="d6a33-117">儲存索引之位置的指標。</span><span class="sxs-lookup"><span data-stu-id="d6a33-117">A pointer to the location where the indices are stored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6a33-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="d6a33-118">Return value</span></span>

<span data-ttu-id="d6a33-119">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="d6a33-119">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d6a33-120">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="d6a33-120">Error codes</span></span>

<span data-ttu-id="d6a33-121">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d6a33-121">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="d6a33-122">Name</span><span class="sxs-lookup"><span data-stu-id="d6a33-122">Name</span></span>                                                                                                  | <span data-ttu-id="d6a33-123">意義</span><span class="sxs-lookup"><span data-stu-id="d6a33-123">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d6a33-124"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="d6a33-124"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="d6a33-125">*模式* 不是可接受的值。</span><span class="sxs-lookup"><span data-stu-id="d6a33-125">*mode* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="d6a33-126"><dt>**GL \_ 無效 \_ 值**</dt></span><span class="sxs-lookup"><span data-stu-id="d6a33-126"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="d6a33-127">*計數* 為負數值。</span><span class="sxs-lookup"><span data-stu-id="d6a33-127">*count* was a negative value.</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="d6a33-128"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="d6a33-128"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="d6a33-129">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="d6a33-129">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="d6a33-130">備註</span><span class="sxs-lookup"><span data-stu-id="d6a33-130">Remarks</span></span>

<span data-ttu-id="d6a33-131">**GlDrawElements** 函式可讓您使用極少數的函式呼叫來指定多個幾何基本類型。</span><span class="sxs-lookup"><span data-stu-id="d6a33-131">The **glDrawElements** function enables you to specify multiple geometric primitives with very few function calls.</span></span> <span data-ttu-id="d6a33-132">您可以事先指定個別的頂點、法線和色彩陣列，並使用它們來定義一系列的基本類型 (所有相同類型) 與 **glDrawElements** 的單一呼叫，而不是呼叫 OpenGL 函式來傳遞每個頂點、法線或色彩。</span><span class="sxs-lookup"><span data-stu-id="d6a33-132">Instead of calling an OpenGL function to pass each individual vertex, normal, or color, you can specify separate arrays of vertices, normals, and colors beforehand and use them to define a sequence of primitives (all of the same type) with a single call to **glDrawElements**.</span></span>

<span data-ttu-id="d6a33-133">當您呼叫 **glDrawElements** 函式時，它會使用來自 *索引* 的 *計數* 順序元素，來建立一系列幾何基本專案。</span><span class="sxs-lookup"><span data-stu-id="d6a33-133">When you call the **glDrawElements** function, it uses *count* sequential elements from *indices* to construct a sequence of geometric primitives.</span></span> <span data-ttu-id="d6a33-134">*Mode* 參數指定要建立的基本類型，以及陣列元素如何用來建立這些基本專案。</span><span class="sxs-lookup"><span data-stu-id="d6a33-134">The *mode* parameter specifies what kind of primitives are constructed, and how the array elements are used to construct these primitives.</span></span> <span data-ttu-id="d6a33-135">如果 \_ \_ 未啟用 GL 頂點陣列，則不會產生任何幾何基本專案。</span><span class="sxs-lookup"><span data-stu-id="d6a33-135">If GL\_VERTEX\_ARRAY is not enabled, no geometric primitives are generated.</span></span>

<span data-ttu-id="d6a33-136">**GlDrawElements** 修改的頂點屬性在 **glDrawElements** 傳回之後具有未指定的值。</span><span class="sxs-lookup"><span data-stu-id="d6a33-136">Vertex attributes that are modified by **glDrawElements** have an unspecified value after **glDrawElements** returns.</span></span> <span data-ttu-id="d6a33-137">例如，如果 \_ \_ 已啟用 GL 色彩陣列，則在 **glDrawElements** 執行之後，目前色彩的值會是未定義的。</span><span class="sxs-lookup"><span data-stu-id="d6a33-137">For example, if GL\_COLOR\_ARRAY is enabled, the value of the current color is undefined after **glDrawElements** executes.</span></span> <span data-ttu-id="d6a33-138">未修改的屬性會維持不變。</span><span class="sxs-lookup"><span data-stu-id="d6a33-138">Attributes that aren't modified remain unchanged.</span></span>

<span data-ttu-id="d6a33-139">您可以在顯示清單中包含 **glDrawElements** 函數。</span><span class="sxs-lookup"><span data-stu-id="d6a33-139">You can include the **glDrawElements** function in display lists.</span></span> <span data-ttu-id="d6a33-140">當 **glDrawElements** 包含在顯示清單中時，必要的陣列資料 (由陣列指標決定，而且也可以在顯示清單中輸入) 。</span><span class="sxs-lookup"><span data-stu-id="d6a33-140">When **glDrawElements** is included in a display list, the necessary array data (determined by the array pointers and enables) is also entered into the display list.</span></span> <span data-ttu-id="d6a33-141">因為陣列指標和可啟用的是用戶端狀態變數，所以它們的值會在建立清單時影響顯示清單，而不是在執行清單時影響。</span><span class="sxs-lookup"><span data-stu-id="d6a33-141">Because the array pointers and enables are client-side state variables, their values affect display lists when the lists are created, not when the lists are executed.</span></span>

> [!Note]  
> <span data-ttu-id="d6a33-142">**GlDrawElements** 函數僅適用于 OpenGL 1.1 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="d6a33-142">The **glDrawElements** function is only available in OpenGL version 1.1 or later.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d6a33-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="d6a33-143">Requirements</span></span>



| <span data-ttu-id="d6a33-144">需求</span><span class="sxs-lookup"><span data-stu-id="d6a33-144">Requirement</span></span> | <span data-ttu-id="d6a33-145">值</span><span class="sxs-lookup"><span data-stu-id="d6a33-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d6a33-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d6a33-146">Minimum supported client</span></span><br/> | <span data-ttu-id="d6a33-147">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d6a33-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="d6a33-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d6a33-148">Minimum supported server</span></span><br/> | <span data-ttu-id="d6a33-149">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d6a33-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d6a33-150">標頭</span><span class="sxs-lookup"><span data-stu-id="d6a33-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6a33-151"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="d6a33-151"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="d6a33-152">程式庫</span><span class="sxs-lookup"><span data-stu-id="d6a33-152">Library</span></span><br/>                  | <dl> <span data-ttu-id="d6a33-153"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d6a33-153"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="d6a33-154">DLL</span><span class="sxs-lookup"><span data-stu-id="d6a33-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6a33-155"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6a33-155"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6a33-156">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d6a33-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6a33-157">**glArrayElement**</span><span class="sxs-lookup"><span data-stu-id="d6a33-157">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="d6a33-158">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="d6a33-158">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="d6a33-159">**glColorPointer**</span><span class="sxs-lookup"><span data-stu-id="d6a33-159">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="d6a33-160">**glDrawArrays**</span><span class="sxs-lookup"><span data-stu-id="d6a33-160">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="d6a33-161">**glEdgeFlagPointer**</span><span class="sxs-lookup"><span data-stu-id="d6a33-161">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="d6a33-162">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="d6a33-162">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="d6a33-163">**glGetPointerv**</span><span class="sxs-lookup"><span data-stu-id="d6a33-163">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="d6a33-164">**glIndexPointer**</span><span class="sxs-lookup"><span data-stu-id="d6a33-164">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="d6a33-165">**glNormalPointer**</span><span class="sxs-lookup"><span data-stu-id="d6a33-165">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="d6a33-166">**glTexCoordPointer**</span><span class="sxs-lookup"><span data-stu-id="d6a33-166">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="d6a33-167">**glVertexPointer**</span><span class="sxs-lookup"><span data-stu-id="d6a33-167">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





