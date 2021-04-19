---
title: 'glReadBuffer 函式 (Gl) '
description: GlReadBuffer 函式會選取圖元的色彩緩衝區來源。
ms.assetid: 734153fa-e809-4b70-867e-55e46ab95712
keywords:
- glReadBuffer 函式 OpenGL
topic_type:
- apiref
api_name:
- glReadBuffer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59f0e88cdcb2b1b3257b23606f8160e0986584db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966525"
---
# <a name="glreadbuffer-function"></a><span data-ttu-id="2cf92-104">glReadBuffer 函式</span><span class="sxs-lookup"><span data-stu-id="2cf92-104">glReadBuffer function</span></span>

<span data-ttu-id="2cf92-105">**GlReadBuffer** 函式會選取圖元的色彩緩衝區來源。</span><span class="sxs-lookup"><span data-stu-id="2cf92-105">The **glReadBuffer** function selects a color buffer source for pixels.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cf92-106">語法</span><span class="sxs-lookup"><span data-stu-id="2cf92-106">Syntax</span></span>


```C++
void WINAPI glReadBuffer(
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="2cf92-107">參數</span><span class="sxs-lookup"><span data-stu-id="2cf92-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2cf92-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="2cf92-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="2cf92-109">色彩緩衝區。</span><span class="sxs-lookup"><span data-stu-id="2cf92-109">A color buffer.</span></span> <span data-ttu-id="2cf92-110">接受的值為 GL \_ front \_ 、gl \_ FRONT \_ 右邊、gl 向 \_ 左、gl 向右、 \_ \_ \_ gl \_ front、gl \_ back、gl \_ LEFT、GL \_ RIGHT，以及 gl \_ aux *i*，在 0 和 gl \_ aux \_ 緩衝區1之間。</span><span class="sxs-lookup"><span data-stu-id="2cf92-110">Accepted values are GL\_FRONT\_LEFT, GL\_FRONT\_RIGHT, GL\_BACK\_LEFT, GL\_BACK\_RIGHT, GL\_FRONT, GL\_BACK, GL\_LEFT, GL\_RIGHT, and GL\_AUX *i*, where *i* is between 0 and GL\_AUX\_BUFFERS 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2cf92-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="2cf92-111">Return value</span></span>

<span data-ttu-id="2cf92-112">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="2cf92-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2cf92-113">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="2cf92-113">Error codes</span></span>

<span data-ttu-id="2cf92-114">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="2cf92-114">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="2cf92-115">Name</span><span class="sxs-lookup"><span data-stu-id="2cf92-115">Name</span></span>                                                                                                  | <span data-ttu-id="2cf92-116">意義</span><span class="sxs-lookup"><span data-stu-id="2cf92-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2cf92-117"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="2cf92-117"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="2cf92-118">*模式* 不是 12 (或更) 接受值的其中之一。</span><span class="sxs-lookup"><span data-stu-id="2cf92-118">*mode* was not an one of the twelve (or more) accepted values.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="2cf92-119"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="2cf92-119"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="2cf92-120">*模式* 指定了不存在的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="2cf92-120">*mode* specified a buffer that does not exist.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="2cf92-121"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="2cf92-121"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="2cf92-122">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="2cf92-122">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="2cf92-123">備註</span><span class="sxs-lookup"><span data-stu-id="2cf92-123">Remarks</span></span>

<span data-ttu-id="2cf92-124">**GlReadBuffer** 函式會將色彩緩衝區指定為後續 [**glReadPixels**](glreadpixels.md)和 [**glCopyPixels**](glcopypixels.md)命令的來源。</span><span class="sxs-lookup"><span data-stu-id="2cf92-124">The **glReadBuffer** function specifies a color buffer as the source for subsequent [**glReadPixels**](glreadpixels.md) and [**glCopyPixels**](glcopypixels.md) commands.</span></span> <span data-ttu-id="2cf92-125">*Mode* 參數接受十二個或更多預先定義的值之一。</span><span class="sxs-lookup"><span data-stu-id="2cf92-125">The *mode* parameter accepts one of twelve or more predefined values.</span></span> <span data-ttu-id="2cf92-126">\_一律會定義透過 gl AUX3 的 (gl AUX0 \_ ) 。在完整設定的系統、gl \_ front、GL 左方和 gl 前端中，都是以 \_ \_ \_ 所有名稱作為左上角緩衝區、gl \_ front \_ 右邊和 gl 右邊 \_ 的 \_ \_ \_ 名稱，並將右緩衝區命名為後置緩衝區。</span><span class="sxs-lookup"><span data-stu-id="2cf92-126">(GL\_AUX0 through GL\_AUX3 are always defined.) In a fully configured system, GL\_FRONT, GL\_LEFT, and GL\_FRONT\_LEFT all name the front-left buffer, GL\_FRONT\_RIGHT and GL\_RIGHT name the front-right buffer, and GL\_BACK\_LEFT and GL\_BACK name the back-left buffer.</span></span>

<span data-ttu-id="2cf92-127">Nonstereo 雙重緩衝設定只會有左上角的緩衝區和左邊的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="2cf92-127">Nonstereo double-buffered configurations have only a front-left and a back-left buffer.</span></span> <span data-ttu-id="2cf92-128">如果有身歷聲，單一緩衝的設定會有左上角和右中的緩衝區，而且只有在 nonstereo 時才會使用 front 左緩衝區。</span><span class="sxs-lookup"><span data-stu-id="2cf92-128">Single-buffered configurations have a front-left and a front-right buffer if stereo, and only a front-left buffer if nonstereo.</span></span> <span data-ttu-id="2cf92-129">將不存在的緩衝區指定給 **glReadBuffer** 是錯誤的。</span><span class="sxs-lookup"><span data-stu-id="2cf92-129">It is an error to specify a nonexistent buffer to **glReadBuffer**.</span></span>

<span data-ttu-id="2cf92-130">根據預設， *模式* 在單一緩衝設定中是 gl \_ 前端，而 \_ 在雙緩衝設定中則為 gl。</span><span class="sxs-lookup"><span data-stu-id="2cf92-130">By default, *mode* is GL\_FRONT in single-buffered configurations, and GL\_BACK in double-buffered configurations.</span></span>

<span data-ttu-id="2cf92-131">下列函式會抓取 **glReadBuffer** 的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="2cf92-131">The following function retrieves information related to **glReadBuffer**:</span></span>

<span data-ttu-id="2cf92-132">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 讀取 \_ 緩衝區的 glGet</span><span class="sxs-lookup"><span data-stu-id="2cf92-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_READ\_BUFFER</span></span>

## <a name="requirements"></a><span data-ttu-id="2cf92-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="2cf92-133">Requirements</span></span>



| <span data-ttu-id="2cf92-134">需求</span><span class="sxs-lookup"><span data-stu-id="2cf92-134">Requirement</span></span> | <span data-ttu-id="2cf92-135">值</span><span class="sxs-lookup"><span data-stu-id="2cf92-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2cf92-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2cf92-136">Minimum supported client</span></span><br/> | <span data-ttu-id="2cf92-137">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2cf92-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="2cf92-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2cf92-138">Minimum supported server</span></span><br/> | <span data-ttu-id="2cf92-139">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2cf92-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2cf92-140">標頭</span><span class="sxs-lookup"><span data-stu-id="2cf92-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="2cf92-141"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="2cf92-141"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="2cf92-142">程式庫</span><span class="sxs-lookup"><span data-stu-id="2cf92-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="2cf92-143"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2cf92-143"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="2cf92-144">DLL</span><span class="sxs-lookup"><span data-stu-id="2cf92-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2cf92-145"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2cf92-145"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2cf92-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2cf92-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cf92-147">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="2cf92-147">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="2cf92-148">**glCopyPixels**</span><span class="sxs-lookup"><span data-stu-id="2cf92-148">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="2cf92-149">**glDrawBuffer**</span><span class="sxs-lookup"><span data-stu-id="2cf92-149">**glDrawBuffer**</span></span>](gldrawbuffer.md)
</dt> <dt>

[<span data-ttu-id="2cf92-150">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="2cf92-150">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="2cf92-151">**glReadPixels**</span><span class="sxs-lookup"><span data-stu-id="2cf92-151">**glReadPixels**</span></span>](glreadpixels.md)
</dt> </dl>

 

 





