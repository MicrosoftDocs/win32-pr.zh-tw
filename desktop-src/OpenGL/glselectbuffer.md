---
title: 'glSelectBuffer 函式 (Gl) '
description: GlSelectBuffer 函數會建立選取模式值的緩衝區。
ms.assetid: b5c64364-1f47-4281-96b5-95c3f5c8e753
keywords:
- glSelectBuffer 函式 OpenGL
topic_type:
- apiref
api_name:
- glSelectBuffer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efa5b97abad6575de77a760c72e3eb05e90461c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685542"
---
# <a name="glselectbuffer-function"></a><span data-ttu-id="99b98-104">glSelectBuffer 函式</span><span class="sxs-lookup"><span data-stu-id="99b98-104">glSelectBuffer function</span></span>

<span data-ttu-id="99b98-105">**GlSelectBuffer** 函數會建立選取模式值的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="99b98-105">The **glSelectBuffer** function establishes a buffer for selection mode values.</span></span>

## <a name="syntax"></a><span data-ttu-id="99b98-106">語法</span><span class="sxs-lookup"><span data-stu-id="99b98-106">Syntax</span></span>


```C++
void WINAPI glSelectBuffer(
   GLsizei size,
   GLuint  *buffer
);
```



## <a name="parameters"></a><span data-ttu-id="99b98-107">參數</span><span class="sxs-lookup"><span data-stu-id="99b98-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99b98-108">*size*</span><span class="sxs-lookup"><span data-stu-id="99b98-108">*size*</span></span> 
</dt> <dd>

<span data-ttu-id="99b98-109">*緩衝區* 的大小。</span><span class="sxs-lookup"><span data-stu-id="99b98-109">The size of *buffer*.</span></span>

</dd> <dt>

<span data-ttu-id="99b98-110">*緩衝區*</span><span class="sxs-lookup"><span data-stu-id="99b98-110">*buffer*</span></span> 
</dt> <dd>

<span data-ttu-id="99b98-111">傳回選取資料。</span><span class="sxs-lookup"><span data-stu-id="99b98-111">Returns the selection data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99b98-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="99b98-112">Return value</span></span>

<span data-ttu-id="99b98-113">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="99b98-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="99b98-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="99b98-114">Error codes</span></span>

<span data-ttu-id="99b98-115">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="99b98-115">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="99b98-116">Name</span><span class="sxs-lookup"><span data-stu-id="99b98-116">Name</span></span>                                                                                                  | <span data-ttu-id="99b98-117">意義</span><span class="sxs-lookup"><span data-stu-id="99b98-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="99b98-118"><dt>**GL \_ 無效 \_ 值**</dt></span><span class="sxs-lookup"><span data-stu-id="99b98-118"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="99b98-119">*大小* 為負數。</span><span class="sxs-lookup"><span data-stu-id="99b98-119">*size* was negative.</span></span><br/>                                                                                                       |
| <dl> <span data-ttu-id="99b98-120"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="99b98-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="99b98-121">當轉譯模式為 GL SELECT 時，即會呼叫此函數 \_ 。</span><span class="sxs-lookup"><span data-stu-id="99b98-121">The function was called while the render mode was GL\_SELECT.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="99b98-122"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="99b98-122"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="99b98-123">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="99b98-123">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="99b98-124">備註</span><span class="sxs-lookup"><span data-stu-id="99b98-124">Remarks</span></span>

<span data-ttu-id="99b98-125">**GlSelectBuffer** 函式有兩個參數： *buffer* 是不帶正負號整數陣列的指標，而 *size* 表示陣列的大小。</span><span class="sxs-lookup"><span data-stu-id="99b98-125">The **glSelectBuffer** function has two parameters: *buffer* is a pointer to an array of unsigned integers, and *size* indicates the size of the array.</span></span> <span data-ttu-id="99b98-126">*Buffer* 參數會從名稱堆疊傳回值 (請參閱 [**glInitNames**](glinitnames.md)、 [**glLoadName**](glloadname.md)、 [**glPushName**](glpushname.md)) 當轉譯模式為 GL 時，請 \_ 選取 (查看 [**glRenderMode**](glrendermode.md)) 。</span><span class="sxs-lookup"><span data-stu-id="99b98-126">The *buffer* parameter returns values from the name stack (see [**glInitNames**](glinitnames.md), [**glLoadName**](glloadname.md), [**glPushName**](glpushname.md)) when the rendering mode is GL\_SELECT (see [**glRenderMode**](glrendermode.md)).</span></span> <span data-ttu-id="99b98-127">**GlSelectBuffer** 函式必須在啟用選取模式之前發出，而且當轉譯模式為 GL 選取時，不能發出此函數 \_ 。</span><span class="sxs-lookup"><span data-stu-id="99b98-127">The **glSelectBuffer** function must be issued before selection mode is enabled, and it must not be issued while the rendering mode is GL\_SELECT.</span></span>

<span data-ttu-id="99b98-128">程式設計師會使用選取範圍來決定要將哪些基本專案繪製到某個視窗的某個區域。</span><span class="sxs-lookup"><span data-stu-id="99b98-128">Selection is used by a programmer to determine which primitives are drawn into some region of a window.</span></span> <span data-ttu-id="99b98-129">區域是由目前的模型和透視圖矩陣所定義。</span><span class="sxs-lookup"><span data-stu-id="99b98-129">The region is defined by the current modelview and perspective matrices.</span></span>

<span data-ttu-id="99b98-130">在選取模式中，不會從柵格化產生任何圖元片段。</span><span class="sxs-lookup"><span data-stu-id="99b98-130">In selection mode, no pixel fragments are produced from rasterization.</span></span> <span data-ttu-id="99b98-131">相反地，如果基本型別與 [視圖] 的 [剪取] 和 [使用者定義裁剪] 平面所定義的剪輯磁片區相交，則此基本型別會造成選取的點擊。</span><span class="sxs-lookup"><span data-stu-id="99b98-131">Instead, if a primitive intersects the clip volume defined by the viewing frustum and the user-defined clipping planes, this primitive causes a selection hit.</span></span> <span data-ttu-id="99b98-132">使用多邊形 (時，如果多邊形挑選，就不會發生命中。 ) 變更名稱堆疊，或呼叫 [**glRenderMode**](glrendermode.md) 時，如果在上一次這類事件之後發生任何命中，則會將叫用記錄複製到 *緩衝區* ，因為這類事件 (名稱堆疊變更或 **glRenderMode** 呼叫) 。</span><span class="sxs-lookup"><span data-stu-id="99b98-132">(With polygons, no hit occurs if the polygon is culled.) When a change is made to the name stack, or when [**glRenderMode**](glrendermode.md) is called, a hit record is copied to *buffer* if any hits have occurred since the last such event (either a name stack change or a **glRenderMode** call).</span></span> <span data-ttu-id="99b98-133">點擊記錄是由事件時名稱堆疊中的名稱數目所組成;然後是自從上一個事件以來碰到的所有頂點的最小和最大深度值;後面接著名稱堆疊內容、下名。</span><span class="sxs-lookup"><span data-stu-id="99b98-133">The hit record consists of the number of names in the name stack at the time of the event; followed by the minimum and maximum depth values of all vertices that hit since the previous event; followed by the name stack contents, bottom name first.</span></span>

<span data-ttu-id="99b98-134">傳回的深度值會對應到最大的不帶正負號的整數值對應至視窗座標深度1.0，而零對應至視窗座標深度0.0。</span><span class="sxs-lookup"><span data-stu-id="99b98-134">Returned depth values are mapped such that the largest unsigned integer value corresponds to window coordinate depth 1.0, and zero corresponds to window coordinate depth 0.0.</span></span>

<span data-ttu-id="99b98-135">當輸入選取模式時， *緩衝區* 的內部索引會重設為零。</span><span class="sxs-lookup"><span data-stu-id="99b98-135">An internal index into *buffer* is reset to zero whenever selection mode is entered.</span></span> <span data-ttu-id="99b98-136">每次將點擊記錄複製到 *緩衝區* 時，索引就會遞增，以指向下一個可用儲存格剛好超過 namesthat 區塊結尾的資料格。</span><span class="sxs-lookup"><span data-stu-id="99b98-136">Each time a hit record is copied into *buffer*, the index is incremented to point to the cell just past the end of the block of namesthat is, to the next available cell.</span></span> <span data-ttu-id="99b98-137">如果點擊記錄大於 *緩衝區* 中剩餘的位置數目，就會複製符合可容納的資料量，並設定溢位旗標。</span><span class="sxs-lookup"><span data-stu-id="99b98-137">If the hit record is larger than the number of remaining locations in *buffer*, as much data as can fit is copied, and the overflow flag is set.</span></span> <span data-ttu-id="99b98-138">如果在複製點擊記錄時，名稱堆疊是空的，則該記錄是由零開始，後面接著最小和最大深度值。</span><span class="sxs-lookup"><span data-stu-id="99b98-138">If the name stack is empty when a hit record is copied, that record consists of zero followed by the minimum and maximum depth values.</span></span>

<span data-ttu-id="99b98-139">使用 GL SELECT 以外的引數呼叫 **glRenderMode** ，結束選取模式 \_ 。</span><span class="sxs-lookup"><span data-stu-id="99b98-139">Selection mode is exited by calling **glRenderMode** with an argument other than GL\_SELECT.</span></span> <span data-ttu-id="99b98-140">每當在轉譯模式為 GL 時呼叫 **glRenderMode** 時 \_ ，它會傳回復制到 *緩衝區* 的點擊記錄數目，重設溢位旗標和選取範圍緩衝區指標，並將名稱堆疊初始化為空白。</span><span class="sxs-lookup"><span data-stu-id="99b98-140">Whenever **glRenderMode** is called while the render mode is GL\_SELECT, it returns the number of hit records copied to *buffer*, resets the overflow flag and the selection buffer pointer, and initializes the name stack to be empty.</span></span> <span data-ttu-id="99b98-141">如果在呼叫 **glRenderMode** 時設定溢位，則會傳回負的命中記錄計數。</span><span class="sxs-lookup"><span data-stu-id="99b98-141">If the overflow bit was set when **glRenderMode** was called, a negative hit record count is returned.</span></span>

<span data-ttu-id="99b98-142">在使用 GL SELECT 以外的引數呼叫 [**glRenderMode**](glrendermode.md)之前，不會定義 *緩衝區* 的內容 \_ 。</span><span class="sxs-lookup"><span data-stu-id="99b98-142">The contents of *buffer* are undefined until [**glRenderMode**](glrendermode.md) is called with an argument other than GL\_SELECT.</span></span>

<span data-ttu-id="99b98-143">**GlBegin** / **glEnd** 基本專案和對 [**glRasterPos**](glrasterpos-functions.md)的呼叫可能會導致點擊。</span><span class="sxs-lookup"><span data-stu-id="99b98-143">The **glBegin**/**glEnd** primitives and calls to [**glRasterPos**](glrasterpos-functions.md) can result in hits.</span></span>

<span data-ttu-id="99b98-144">下列函式會抓取 **glSelectBuffer** 的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="99b98-144">The following function retrieves information related to **glSelectBuffer**:</span></span>

<span data-ttu-id="99b98-145">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 名稱 \_ STACK \_ 深度的 glGet</span><span class="sxs-lookup"><span data-stu-id="99b98-145">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_NAME\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="99b98-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="99b98-146">Requirements</span></span>



| <span data-ttu-id="99b98-147">需求</span><span class="sxs-lookup"><span data-stu-id="99b98-147">Requirement</span></span> | <span data-ttu-id="99b98-148">值</span><span class="sxs-lookup"><span data-stu-id="99b98-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="99b98-149">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="99b98-149">Minimum supported client</span></span><br/> | <span data-ttu-id="99b98-150">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="99b98-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="99b98-151">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="99b98-151">Minimum supported server</span></span><br/> | <span data-ttu-id="99b98-152">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="99b98-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="99b98-153">標頭</span><span class="sxs-lookup"><span data-stu-id="99b98-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="99b98-154"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="99b98-154"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="99b98-155">程式庫</span><span class="sxs-lookup"><span data-stu-id="99b98-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="99b98-156"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="99b98-156"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="99b98-157">DLL</span><span class="sxs-lookup"><span data-stu-id="99b98-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="99b98-158"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99b98-158"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99b98-159">另請參閱</span><span class="sxs-lookup"><span data-stu-id="99b98-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99b98-160">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="99b98-160">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="99b98-161">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="99b98-161">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="99b98-162">**glFeedbackBuffer**</span><span class="sxs-lookup"><span data-stu-id="99b98-162">**glFeedbackBuffer**</span></span>](glfeedbackbuffer.md)
</dt> <dt>

[<span data-ttu-id="99b98-163">**glInitNames**</span><span class="sxs-lookup"><span data-stu-id="99b98-163">**glInitNames**</span></span>](glinitnames.md)
</dt> <dt>

[<span data-ttu-id="99b98-164">**glLoadName**</span><span class="sxs-lookup"><span data-stu-id="99b98-164">**glLoadName**</span></span>](glloadname.md)
</dt> <dt>

[<span data-ttu-id="99b98-165">**glPushName**</span><span class="sxs-lookup"><span data-stu-id="99b98-165">**glPushName**</span></span>](glpushname.md)
</dt> <dt>

[<span data-ttu-id="99b98-166">**glRenderMode**</span><span class="sxs-lookup"><span data-stu-id="99b98-166">**glRenderMode**</span></span>](glrendermode.md)
</dt> </dl>

 

 





