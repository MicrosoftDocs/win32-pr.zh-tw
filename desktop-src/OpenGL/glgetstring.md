---
title: 'glGetString 函式 (Gl) '
description: GlGetString 函式會傳回描述目前 OpenGL 連接的字串。
ms.assetid: 768e6ec2-3f00-44e6-b3cb-de0f06d6a73d
keywords:
- glGetString 函式 OpenGL
topic_type:
- apiref
api_name:
- glGetString
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e263e35802af752fa262c898d036fccaa37aff87
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934987"
---
# <a name="glgetstring-function"></a><span data-ttu-id="59f87-104">glGetString 函式</span><span class="sxs-lookup"><span data-stu-id="59f87-104">glGetString function</span></span>

<span data-ttu-id="59f87-105">**GlGetString** 函式會傳回描述目前 OpenGL 連接的字串。</span><span class="sxs-lookup"><span data-stu-id="59f87-105">The **glGetString** function returns a string describing the current OpenGL connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="59f87-106">語法</span><span class="sxs-lookup"><span data-stu-id="59f87-106">Syntax</span></span>


```C++
const GLubyte* WINAPI glGetString(
   GLenum name
);
```



## <a name="parameters"></a><span data-ttu-id="59f87-107">參數</span><span class="sxs-lookup"><span data-stu-id="59f87-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59f87-108">*name*</span><span class="sxs-lookup"><span data-stu-id="59f87-108">*name*</span></span> 
</dt> <dd>

<span data-ttu-id="59f87-109">下列其中一個符號常數。</span><span class="sxs-lookup"><span data-stu-id="59f87-109">One of the following symbolic constants.</span></span>



| <span data-ttu-id="59f87-110">值</span><span class="sxs-lookup"><span data-stu-id="59f87-110">Value</span></span>                                                                                                                                                         | <span data-ttu-id="59f87-111">意義</span><span class="sxs-lookup"><span data-stu-id="59f87-111">Meaning</span></span>                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_VENDOR"></span><span id="gl_vendor"></span><dl> <span data-ttu-id="59f87-112"><dt>**GL \_ 廠商**</dt></span><span class="sxs-lookup"><span data-stu-id="59f87-112"><dt>**GL\_VENDOR**</dt></span></span> </dl>             | <span data-ttu-id="59f87-113">傳回負責此 OpenGL 實的公司。</span><span class="sxs-lookup"><span data-stu-id="59f87-113">Returns the company responsible for this OpenGL implementation.</span></span> <span data-ttu-id="59f87-114">此名稱不會因為版本而變更。</span><span class="sxs-lookup"><span data-stu-id="59f87-114">This name does not change from release to release.</span></span><br/>                                                  |
| <span id="GL_RENDERER"></span><span id="gl_renderer"></span><dl> <span data-ttu-id="59f87-115"><dt>**GL \_ 轉譯器**</dt></span><span class="sxs-lookup"><span data-stu-id="59f87-115"><dt>**GL\_RENDERER**</dt></span></span> </dl>       | <span data-ttu-id="59f87-116">傳回轉譯器的名稱。</span><span class="sxs-lookup"><span data-stu-id="59f87-116">Returns the name of the renderer.</span></span> <span data-ttu-id="59f87-117">此名稱通常專屬於特定的硬體平臺設定。</span><span class="sxs-lookup"><span data-stu-id="59f87-117">This name is typically specific to a particular configuration of a hardware platform.</span></span> <span data-ttu-id="59f87-118">它不會因發行而變更。</span><span class="sxs-lookup"><span data-stu-id="59f87-118">It does not change from release to release.</span></span><br/> |
| <span id="GL_VERSION"></span><span id="gl_version"></span><dl> <span data-ttu-id="59f87-119"><dt>**GL \_ 版本**</dt></span><span class="sxs-lookup"><span data-stu-id="59f87-119"><dt>**GL\_VERSION**</dt></span></span> </dl>          | <span data-ttu-id="59f87-120">傳回版本或版本號碼。</span><span class="sxs-lookup"><span data-stu-id="59f87-120">Returns a version or release number.</span></span><br/>                                                                                                                                |
| <span id="GL_EXTENSIONS"></span><span id="gl_extensions"></span><dl> <span data-ttu-id="59f87-121"><dt>**GL \_ 延伸模組**</dt></span><span class="sxs-lookup"><span data-stu-id="59f87-121"><dt>**GL\_EXTENSIONS**</dt></span></span> </dl> | <span data-ttu-id="59f87-122">傳回 OpenGL 支援的延伸模組清單（以空格分隔）。</span><span class="sxs-lookup"><span data-stu-id="59f87-122">Returns a space-separated list of supported extensions to OpenGL.</span></span><br/>                                                                                                   |



 

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="59f87-123">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="59f87-123">Error codes</span></span>

<span data-ttu-id="59f87-124">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="59f87-124">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="59f87-125">Name</span><span class="sxs-lookup"><span data-stu-id="59f87-125">Name</span></span>                                                                                                  | <span data-ttu-id="59f87-126">意義</span><span class="sxs-lookup"><span data-stu-id="59f87-126">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="59f87-127"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="59f87-127"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="59f87-128">*名稱* 不是可接受的值。</span><span class="sxs-lookup"><span data-stu-id="59f87-128">*name* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="59f87-129"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="59f87-129"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="59f87-130">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="59f87-130">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="59f87-131">備註</span><span class="sxs-lookup"><span data-stu-id="59f87-131">Remarks</span></span>

<span data-ttu-id="59f87-132">**GlGetString** 函式會傳回靜態字串的指標，此字串描述目前 OpenGL 連接的某個方面。</span><span class="sxs-lookup"><span data-stu-id="59f87-132">The **glGetString** function returns a pointer to a static string describing some aspect of the current OpenGL connection.</span></span>

<span data-ttu-id="59f87-133">由於 OpenGL 不包含執行效能特性的查詢，因此某些應用程式應該會被撰寫以辨識已知的平臺，並根據這些平臺的已知效能特性修改其 OpenGL 使用量。</span><span class="sxs-lookup"><span data-stu-id="59f87-133">Because OpenGL does not include queries for the performance characteristics of an implementation, it is expected that some applications will be written to recognize known platforms and will modify their OpenGL usage based on known performance characteristics of these platforms.</span></span> <span data-ttu-id="59f87-134">字串 GL \_ 廠商和 GL 轉譯器 \_ 會以唯一的方式指定平臺，而不會從版本變更為版本。</span><span class="sxs-lookup"><span data-stu-id="59f87-134">The strings GL\_VENDOR and GL\_RENDERER together uniquely specify a platform, and will not change from release to release.</span></span> <span data-ttu-id="59f87-135">它們應該以平臺辨識演算法的形式來使用。</span><span class="sxs-lookup"><span data-stu-id="59f87-135">They should be used as such by platform recognition algorithms.</span></span>

<span data-ttu-id="59f87-136">**GlGetString** 所傳回之字串的格式和內容取決於執行，不同之處在于：</span><span class="sxs-lookup"><span data-stu-id="59f87-136">The format and contents of the string that **glGetString** returns depend on the implementation, except that:</span></span>

-   <span data-ttu-id="59f87-137">延伸模組名稱不會包含空白字元，而且會以 GL 擴充字串中的空白字元分隔 \_ 。</span><span class="sxs-lookup"><span data-stu-id="59f87-137">Extension names will not include space characters and will be separated by space characters in the GL\_EXTENSIONS string.</span></span>
-   <span data-ttu-id="59f87-138">GL \_ 版本字串的開頭為版本號碼。</span><span class="sxs-lookup"><span data-stu-id="59f87-138">The GL\_VERSION string begins with a version number.</span></span> <span data-ttu-id="59f87-139">版本號碼會使用下列其中一種形式：</span><span class="sxs-lookup"><span data-stu-id="59f87-139">The version number uses one of these forms:</span></span>

    <span data-ttu-id="59f87-140">*主要 \_ 號碼*。*次要 \_ 編號*</span><span class="sxs-lookup"><span data-stu-id="59f87-140">*major\_number*.*minor\_number*</span></span>

    <span data-ttu-id="59f87-141">*主要 \_ 號碼*。*次要 \_ 號碼*。*版本 \_ 號碼*</span><span class="sxs-lookup"><span data-stu-id="59f87-141">*major\_number*.*minor\_number*.*release\_number*</span></span>

-   <span data-ttu-id="59f87-142">廠商特定的資訊可能會遵循版本號碼。</span><span class="sxs-lookup"><span data-stu-id="59f87-142">Vendor-specific information may follow the version number.</span></span> <span data-ttu-id="59f87-143">其格式取決於執行，但空格一律會分隔版本號碼和廠商專屬的資訊。</span><span class="sxs-lookup"><span data-stu-id="59f87-143">Its format depends on the implementation, but a space always separates the version number and the vendor-specific information.</span></span>
-   <span data-ttu-id="59f87-144">所有字串都以 null 終止。</span><span class="sxs-lookup"><span data-stu-id="59f87-144">All strings are null-terminated.</span></span>

<span data-ttu-id="59f87-145">如果產生錯誤， **glGetString** 會傳回零。</span><span class="sxs-lookup"><span data-stu-id="59f87-145">If an error is generated, **glGetString** returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="59f87-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="59f87-146">Requirements</span></span>



| <span data-ttu-id="59f87-147">需求</span><span class="sxs-lookup"><span data-stu-id="59f87-147">Requirement</span></span> | <span data-ttu-id="59f87-148">值</span><span class="sxs-lookup"><span data-stu-id="59f87-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="59f87-149">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="59f87-149">Minimum supported client</span></span><br/> | <span data-ttu-id="59f87-150">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="59f87-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="59f87-151">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="59f87-151">Minimum supported server</span></span><br/> | <span data-ttu-id="59f87-152">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="59f87-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="59f87-153">標頭</span><span class="sxs-lookup"><span data-stu-id="59f87-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="59f87-154"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="59f87-154"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="59f87-155">程式庫</span><span class="sxs-lookup"><span data-stu-id="59f87-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="59f87-156"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="59f87-156"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="59f87-157">DLL</span><span class="sxs-lookup"><span data-stu-id="59f87-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59f87-158"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59f87-158"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59f87-159">另請參閱</span><span class="sxs-lookup"><span data-stu-id="59f87-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59f87-160">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="59f87-160">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="59f87-161">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="59f87-161">**glEnd**</span></span>](glend.md)
</dt> </dl>

 

 





