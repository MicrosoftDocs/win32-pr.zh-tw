---
title: 'glAddSwapHintRectWIN 函式 (Gl) '
description: GlAddSwapHintRectWIN 回呼函式會指定一組要由 SwapBuffers 複製的矩形。
ms.assetid: f242e755-8e8a-471a-9884-47efa22a3de6
keywords:
- glAddSwapHintRectWIN 函式 OpenGL
topic_type:
- apiref
api_name:
- glAddSwapHintRectWIN
api_location:
- Gl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ae3e10c2f51ff8d7c9763ff1dad7d09d800cd60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384833"
---
# <a name="gladdswaphintrectwin-function"></a><span data-ttu-id="d29de-104">glAddSwapHintRectWIN 函式</span><span class="sxs-lookup"><span data-stu-id="d29de-104">glAddSwapHintRectWIN function</span></span>

<span data-ttu-id="d29de-105">**GlAddSwapHintRectWIN** 回呼函式會指定一組要由 [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers)複製的矩形。</span><span class="sxs-lookup"><span data-stu-id="d29de-105">The **glAddSwapHintRectWIN** callback function specifies a set of rectangles that are to be copied by [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers).</span></span>

## <a name="syntax"></a><span data-ttu-id="d29de-106">語法</span><span class="sxs-lookup"><span data-stu-id="d29de-106">Syntax</span></span>


```C++
void WINAPI glAddSwapHintRectWIN(
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height
);
```



## <a name="parameters"></a><span data-ttu-id="d29de-107">參數</span><span class="sxs-lookup"><span data-stu-id="d29de-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d29de-108">*x*</span><span class="sxs-lookup"><span data-stu-id="d29de-108">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="d29de-109">視窗中的 *x* 座標 (會協調提示區域矩形左下角的) 。</span><span class="sxs-lookup"><span data-stu-id="d29de-109">The *x*-coordinate (in window coordinates) of the lower-left corner of the hint region rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="d29de-110">*y*</span><span class="sxs-lookup"><span data-stu-id="d29de-110">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="d29de-111">視窗中的 *y* 座標 (會協調提示區域矩形左下角的) 。</span><span class="sxs-lookup"><span data-stu-id="d29de-111">The *y*-coordinate (in window coordinates) of the lower-left corner of the hint region rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="d29de-112">*width* (寬度)</span><span class="sxs-lookup"><span data-stu-id="d29de-112">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="d29de-113">提示區域矩形的寬度。</span><span class="sxs-lookup"><span data-stu-id="d29de-113">The width of the hint region rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="d29de-114">*height* (高度)</span><span class="sxs-lookup"><span data-stu-id="d29de-114">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="d29de-115">提示區域矩形的高度。</span><span class="sxs-lookup"><span data-stu-id="d29de-115">The height of the hint region rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d29de-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="d29de-116">Return value</span></span>

<span data-ttu-id="d29de-117">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="d29de-117">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d29de-118">備註</span><span class="sxs-lookup"><span data-stu-id="d29de-118">Remarks</span></span>

<span data-ttu-id="d29de-119">**GlAddSwapHintRectWIN** 函式會藉由減少畫面格之間的重畫量來加快動畫的速度。</span><span class="sxs-lookup"><span data-stu-id="d29de-119">The **glAddSwapHintRectWIN** function speeds up animation by reducing the amount of repainting between frames.</span></span> <span data-ttu-id="d29de-120">使用 **glAddSwapHintRectWIN**，您可以指定一組要在呼叫 [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers)時複製的矩形區域。</span><span class="sxs-lookup"><span data-stu-id="d29de-120">With **glAddSwapHintRectWIN**, you specify a set of rectangular areas that you want copied when you call [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers).</span></span> <span data-ttu-id="d29de-121">當您在呼叫 **SwapBuffers** 之前未指定具有 **glAddSwapHintRectWIN** 的任何矩形時，會交換整個畫面格緩衝區。</span><span class="sxs-lookup"><span data-stu-id="d29de-121">When you do not specify any rectangles with **glAddSwapHintRectWIN** before calling **SwapBuffers**, the entire framebuffer is swapped.</span></span> <span data-ttu-id="d29de-122">使用 **glAddSwapHintRectWIN** 只複製已變更的緩衝區部分，可大幅提高 **SwapBuffers** 的效能，特別是在軟體中執行 **SwapBuffers** 時。</span><span class="sxs-lookup"><span data-stu-id="d29de-122">Using **glAddSwapHintRectWIN** to copy only changed parts of the buffer can significantly increase the performance of **SwapBuffers**, especially when **SwapBuffers** is implemented in software.</span></span>

<span data-ttu-id="d29de-123">**GlAddSwapHintRectWIN** 函式會將矩形新增至提示區域。</span><span class="sxs-lookup"><span data-stu-id="d29de-123">The **glAddSwapHintRectWIN** function adds a rectangle to the hint region.</span></span> <span data-ttu-id="d29de-124">當 \_ \_ 設定 [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) 像素格式結構的 PFD SWAP COPY 旗標時， **SwapBuffers** 會使用此區域來將背景緩衝區的複製工作裁剪至前端緩衝區。</span><span class="sxs-lookup"><span data-stu-id="d29de-124">When the PFD\_SWAP\_COPY flag of the [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) pixel format structure is set, **SwapBuffers** uses this region to clip the copying of the back buffer to the front buffer.</span></span> <span data-ttu-id="d29de-125">您不會指定 PFD \_ SWAP COPY，而 \_ 是由可用的硬體設定。</span><span class="sxs-lookup"><span data-stu-id="d29de-125">You don't specify PFD\_SWAP\_COPY; it is set by capable hardware.</span></span> <span data-ttu-id="d29de-126">每次呼叫 **SwapBuffers** 之後，就會清除提示區域。</span><span class="sxs-lookup"><span data-stu-id="d29de-126">The hint region is cleared after each call to **SwapBuffers**.</span></span> <span data-ttu-id="d29de-127">使用一些硬體設定時， **SwapBuffers** 可以忽略提示區域並交換整個緩衝區。</span><span class="sxs-lookup"><span data-stu-id="d29de-127">With some hardware configurations, **SwapBuffers** can ignore the hint region and exchange the entire buffer.</span></span> <span data-ttu-id="d29de-128">**SwapBuffers** 是由系統所執行，而不是由應用程式所執行。</span><span class="sxs-lookup"><span data-stu-id="d29de-128">**SwapBuffers** is implemented by the system, not by the application.</span></span>

<span data-ttu-id="d29de-129">OpenGL 會針對每個視窗維護個別的提示區域。</span><span class="sxs-lookup"><span data-stu-id="d29de-129">OpenGL maintains a separate hint region for each window.</span></span> <span data-ttu-id="d29de-130">當您在與視窗相關聯的任何轉譯內容上呼叫 **glAddSwapHintRectWIN** 時，提示矩形會合並到單一區域中。</span><span class="sxs-lookup"><span data-stu-id="d29de-130">When you call **glAddSwapHintRectWIN** on any rendering contexts associated with a window, the hint rectangles are combined into a single region.</span></span>

<span data-ttu-id="d29de-131">針對針對框架繪製的每個物件，使用周框矩形呼叫 **glAddSwapHintRectWIN** ，並清除每個矩形以清除先前的框架物件。</span><span class="sxs-lookup"><span data-stu-id="d29de-131">Call **glAddSwapHintRectWIN** with a bounding rectangle for each object drawn for a frame and for each rectangle cleared to erase previous frame objects.</span></span>

> [!Note]  
> <span data-ttu-id="d29de-132">**GlAddSwapHintRectWIN** 函式是延伸模組函式，不是標準 OpenGL 程式庫的一部分，而是 GL \_ WIN \_ 交換 \_ 提示擴充功能的一部分。</span><span class="sxs-lookup"><span data-stu-id="d29de-132">The **glAddSwapHintRectWIN** function is an extension function that is not part of the standard OpenGL library but is part of the GL\_WIN\_swap\_hint extension.</span></span> <span data-ttu-id="d29de-133">若要檢查您的 OpenGL 執行是否支援 **glAddSwapHintRectWIN**，請) 呼叫 **glGetString** (GL \_ 延伸模組。</span><span class="sxs-lookup"><span data-stu-id="d29de-133">To check whether your implementation of OpenGL supports **glAddSwapHintRectWIN**, call **glGetString**(GL\_EXTENSIONS).</span></span> <span data-ttu-id="d29de-134">如果它傳回 GL \_ WIN \_ 交換 \_ 提示，則會支援 **glAddSwapHintRectWIN** 。</span><span class="sxs-lookup"><span data-stu-id="d29de-134">If it returns GL\_WIN\_swap\_hint, **glAddSwapHintRectWIN** is supported.</span></span> <span data-ttu-id="d29de-135">若要取得擴充功能函式的位址，請呼叫 **wglGetProcAddress**。</span><span class="sxs-lookup"><span data-stu-id="d29de-135">To obtain the address of an extension function, call **wglGetProcAddress**.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d29de-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="d29de-136">Requirements</span></span>



| <span data-ttu-id="d29de-137">需求</span><span class="sxs-lookup"><span data-stu-id="d29de-137">Requirement</span></span> | <span data-ttu-id="d29de-138">值</span><span class="sxs-lookup"><span data-stu-id="d29de-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="d29de-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d29de-139">Minimum supported client</span></span><br/> | <span data-ttu-id="d29de-140">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d29de-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="d29de-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d29de-141">Minimum supported server</span></span><br/> | <span data-ttu-id="d29de-142">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d29de-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="d29de-143">標頭</span><span class="sxs-lookup"><span data-stu-id="d29de-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="d29de-144"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="d29de-144"><dt>Gl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d29de-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d29de-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d29de-146">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="d29de-146">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="d29de-147">**PIXELFORMATDESCRIPTOR**</span><span class="sxs-lookup"><span data-stu-id="d29de-147">**PIXELFORMATDESCRIPTOR**</span></span>](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor)
</dt> <dt>

[<span data-ttu-id="d29de-148">**SwapBuffers**</span><span class="sxs-lookup"><span data-stu-id="d29de-148">**SwapBuffers**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers)
</dt> <dt>

[<span data-ttu-id="d29de-149">**wglGetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="d29de-149">**wglGetProcAddress**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





