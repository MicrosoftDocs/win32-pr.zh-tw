---
title: 'glArrayElement 函式 (Gl) '
description: GlArrayElement 函式會指定用來呈現頂點的陣列元素。
ms.assetid: 2c4d76bb-e4c9-4baa-a190-66298b8a4335
keywords:
- glArrayElement 函式 OpenGL
topic_type:
- apiref
api_name:
- glArrayElement
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a20aff9fcaa5bf922bc9447f7b7022a8cd1a9c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967340"
---
# <a name="glarrayelement-function"></a><span data-ttu-id="bc90b-104">glArrayElement 函式</span><span class="sxs-lookup"><span data-stu-id="bc90b-104">glArrayElement function</span></span>

<span data-ttu-id="bc90b-105">**GlArrayElement** 函式會指定用來呈現頂點的陣列元素。</span><span class="sxs-lookup"><span data-stu-id="bc90b-105">The **glArrayElement** function specifies the array elements used to render a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc90b-106">語法</span><span class="sxs-lookup"><span data-stu-id="bc90b-106">Syntax</span></span>


```C++
void WINAPI glArrayElement(
   GLint index
);
```



## <a name="parameters"></a><span data-ttu-id="bc90b-107">參數</span><span class="sxs-lookup"><span data-stu-id="bc90b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc90b-108">*index*</span><span class="sxs-lookup"><span data-stu-id="bc90b-108">*index*</span></span> 
</dt> <dd>

<span data-ttu-id="bc90b-109">啟用的陣列中的索引。</span><span class="sxs-lookup"><span data-stu-id="bc90b-109">An index in the enabled arrays.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc90b-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="bc90b-110">Return value</span></span>

<span data-ttu-id="bc90b-111">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="bc90b-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc90b-112">備註</span><span class="sxs-lookup"><span data-stu-id="bc90b-112">Remarks</span></span>

<span data-ttu-id="bc90b-113">使用 [**glBegin**](glbegin.md)和 [**glEnd**](glend.md)配對內的 **glArrayElement** 函式來指定點、線條和多邊形基本專案的頂點和屬性資料。</span><span class="sxs-lookup"><span data-stu-id="bc90b-113">Use the **glArrayElement** function within [**glBegin**](glbegin.md) and [**glEnd**](glend.md) pairs to specify vertex and attribute data for point, line, and polygon primitives.</span></span> <span data-ttu-id="bc90b-114">**GlArrayElement** 函式會使用位於已啟用頂點陣列 *索引* 的頂點和屬性資料，來指定單一頂點的資料。</span><span class="sxs-lookup"><span data-stu-id="bc90b-114">The **glArrayElement** function specifies the data for a single vertex using vertex and attribute data located at the *index* of the enabled vertex arrays.</span></span>

<span data-ttu-id="bc90b-115">您可以使用 **glArrayElement** 來建立基本資料，方法是編制頂點資料的索引，而不是在第一次到最後一個訂單的資料陣列之間進行串流處理。</span><span class="sxs-lookup"><span data-stu-id="bc90b-115">You can use **glArrayElement** to construct primitives by indexing vertex data, rather than by streaming through arrays of data in first-to-last order.</span></span> <span data-ttu-id="bc90b-116">因為 **glArrayElement** 只會指定單一頂點，所以您可以明確指定個別基本專案的屬性。</span><span class="sxs-lookup"><span data-stu-id="bc90b-116">Because **glArrayElement** specifies a single vertex only, you can explicitly specify attributes for individual primitives.</span></span> <span data-ttu-id="bc90b-117">例如，您可以針對每個個別的三角形設定單一一般。</span><span class="sxs-lookup"><span data-stu-id="bc90b-117">For example, you can set a single normal for each individual triangle.</span></span>

<span data-ttu-id="bc90b-118">當您在顯示清單中包含 **glArrayElement** 的呼叫時，顯示清單中也會輸入必要的陣列資料（由陣列指標和啟用值所決定）。</span><span class="sxs-lookup"><span data-stu-id="bc90b-118">When you include calls to **glArrayElement** in display lists, the necessary array data, determined by the array pointers and enable values, is entered in the display list also.</span></span> <span data-ttu-id="bc90b-119">陣列指標和啟用值是在顯示清單建立時決定，而不是在執行顯示清單時決定。</span><span class="sxs-lookup"><span data-stu-id="bc90b-119">Array pointer and enable values are determined when display lists are created, not when display lists are executed.</span></span>

<span data-ttu-id="bc90b-120">您可以隨時使用 **glArrayElement** 來讀取和快取靜態陣列資料。</span><span class="sxs-lookup"><span data-stu-id="bc90b-120">You can read and cache static array data at any time with **glArrayElement**.</span></span> <span data-ttu-id="bc90b-121">當您修改靜態陣列的元素而未再次指定陣列時，任何後續呼叫 **glArrayElement** 的結果都是未定義的。</span><span class="sxs-lookup"><span data-stu-id="bc90b-121">When you modify the elements of a static array without specifying the array again, the results of any subsequent calls to **glArrayElement** are undefined.</span></span>

<span data-ttu-id="bc90b-122">當您呼叫 **glArrayElement** 時，若未先呼叫 **glEnableClientState** (GL \_ 頂點 \_ 陣列) ，就不會進行任何繪製，但是會修改對應到已啟用陣列的屬性。</span><span class="sxs-lookup"><span data-stu-id="bc90b-122">When you call **glArrayElement** without first calling **glEnableClientState**(GL\_VERTEX\_ARRAY), no drawing occurs, but the attributes corresponding to enabled arrays are modified.</span></span> <span data-ttu-id="bc90b-123">雖然當您在 **glBegin** 和 **glEnd** 配對內指定陣列時，不會產生任何錯誤，但結果是未定義的。</span><span class="sxs-lookup"><span data-stu-id="bc90b-123">Although no error is generated when you specify an array within **glBegin** and **glEnd** pairs, the results are undefined.</span></span>

> [!Note]  
> <span data-ttu-id="bc90b-124">**GlArrayElement** 函數僅適用于 OpenGL 1.1 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="bc90b-124">The **glArrayElement** function is only available in OpenGL version 1.1 or later.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bc90b-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="bc90b-125">Requirements</span></span>



| <span data-ttu-id="bc90b-126">需求</span><span class="sxs-lookup"><span data-stu-id="bc90b-126">Requirement</span></span> | <span data-ttu-id="bc90b-127">值</span><span class="sxs-lookup"><span data-stu-id="bc90b-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bc90b-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bc90b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="bc90b-129">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bc90b-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="bc90b-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bc90b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="bc90b-131">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bc90b-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bc90b-132">標頭</span><span class="sxs-lookup"><span data-stu-id="bc90b-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc90b-133"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="bc90b-133"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="bc90b-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="bc90b-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="bc90b-135"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="bc90b-135"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="bc90b-136">DLL</span><span class="sxs-lookup"><span data-stu-id="bc90b-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc90b-137"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc90b-137"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc90b-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bc90b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc90b-139">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="bc90b-139">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="bc90b-140">**glColorPointer**</span><span class="sxs-lookup"><span data-stu-id="bc90b-140">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="bc90b-141">**glDrawArrays**</span><span class="sxs-lookup"><span data-stu-id="bc90b-141">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="bc90b-142">**glEdgeFlagPointer**</span><span class="sxs-lookup"><span data-stu-id="bc90b-142">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="bc90b-143">**glEnableClientState**</span><span class="sxs-lookup"><span data-stu-id="bc90b-143">**glEnableClientState**</span></span>](glenableclientstate.md)
</dt> <dt>

[<span data-ttu-id="bc90b-144">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="bc90b-144">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="bc90b-145">**glGetPointerv**</span><span class="sxs-lookup"><span data-stu-id="bc90b-145">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="bc90b-146">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="bc90b-146">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="bc90b-147">**glIndexPointer**</span><span class="sxs-lookup"><span data-stu-id="bc90b-147">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="bc90b-148">**glNormalPointer**</span><span class="sxs-lookup"><span data-stu-id="bc90b-148">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="bc90b-149">**glTexCoordPointer**</span><span class="sxs-lookup"><span data-stu-id="bc90b-149">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="bc90b-150">**glVertexPointer**</span><span class="sxs-lookup"><span data-stu-id="bc90b-150">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





