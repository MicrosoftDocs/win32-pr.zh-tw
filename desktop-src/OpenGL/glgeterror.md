---
title: 'glGetError 函式 (Gl) '
description: GlGetError 函數會傳回錯誤資訊。
ms.assetid: 18f0368f-054f-4b84-8397-3f9ee4aa07fa
keywords:
- glGetError 函式 OpenGL
topic_type:
- apiref
api_name:
- glGetError
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74c0abf6ec03ca0c29ede3b7d396db375fd06ac6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934931"
---
# <a name="glgeterror-function"></a><span data-ttu-id="47d1e-104">glGetError 函式</span><span class="sxs-lookup"><span data-stu-id="47d1e-104">glGetError function</span></span>

<span data-ttu-id="47d1e-105">**GlGetError** 函數會傳回錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="47d1e-105">The **glGetError** function returns error information.</span></span>

## <a name="syntax"></a><span data-ttu-id="47d1e-106">語法</span><span class="sxs-lookup"><span data-stu-id="47d1e-106">Syntax</span></span>


```C++
GLenum WINAPI glGetError(void);
```



## <a name="parameters"></a><span data-ttu-id="47d1e-107">參數</span><span class="sxs-lookup"><span data-stu-id="47d1e-107">Parameters</span></span>

<span data-ttu-id="47d1e-108">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="47d1e-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="47d1e-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="47d1e-109">Return value</span></span>

<span data-ttu-id="47d1e-110">**GlGetError** 函數會傳回下列其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="47d1e-110">The **glGetError** function returns one of the following error codes.</span></span>



| <span data-ttu-id="47d1e-111">傳回碼</span><span class="sxs-lookup"><span data-stu-id="47d1e-111">Return code</span></span>                                                                                           | <span data-ttu-id="47d1e-112">Description</span><span class="sxs-lookup"><span data-stu-id="47d1e-112">Description</span></span>                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="47d1e-113"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="47d1e-113"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="47d1e-114">針對列舉引數指定了無法接受的值。</span><span class="sxs-lookup"><span data-stu-id="47d1e-114">An unacceptable value is specified for an enumerated argument.</span></span> <span data-ttu-id="47d1e-115">若未設定錯誤旗標，則會忽略有問題的函式，而不會有任何副作用。</span><span class="sxs-lookup"><span data-stu-id="47d1e-115">The offending function is ignored, having no side effect other than to set the error flag.</span></span><br/>         |
| <dl> <span data-ttu-id="47d1e-116"><dt>**GL \_ 無效 \_ 值**</dt></span><span class="sxs-lookup"><span data-stu-id="47d1e-116"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="47d1e-117">數值引數超出範圍。</span><span class="sxs-lookup"><span data-stu-id="47d1e-117">A numeric argument is out of range.</span></span> <span data-ttu-id="47d1e-118">若未設定錯誤旗標，則會忽略有問題的函式，而不會有任何副作用。</span><span class="sxs-lookup"><span data-stu-id="47d1e-118">The offending function is ignored, having no side effect other than to set the error flag.</span></span><br/>                                    |
| <dl> <span data-ttu-id="47d1e-119"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="47d1e-119"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="47d1e-120">目前的狀態不允許指定的作業。</span><span class="sxs-lookup"><span data-stu-id="47d1e-120">The specified operation is not allowed in the current state.</span></span> <span data-ttu-id="47d1e-121">若未設定錯誤旗標，則會忽略有問題的函式，而不會有任何副作用。</span><span class="sxs-lookup"><span data-stu-id="47d1e-121">The offending function is ignored, having no side effect other than to set the error flag.</span></span><br/>           |
| <dl> <span data-ttu-id="47d1e-122"><dt>**GL \_ 沒有 \_ 錯誤**</dt></span><span class="sxs-lookup"><span data-stu-id="47d1e-122"><dt>**GL\_NO\_ERROR**</dt></span></span> </dl>          | <span data-ttu-id="47d1e-123">未記錄任何錯誤。</span><span class="sxs-lookup"><span data-stu-id="47d1e-123">No error has been recorded.</span></span> <span data-ttu-id="47d1e-124">此符號常數的值保證為零。</span><span class="sxs-lookup"><span data-stu-id="47d1e-124">The value of this symbolic constant is guaranteed to be zero.</span></span><br/>                                                                         |
| <dl> <span data-ttu-id="47d1e-125"><dt>**GL \_ 堆疊 \_ 溢位**</dt></span><span class="sxs-lookup"><span data-stu-id="47d1e-125"><dt>**GL\_STACK\_OVERFLOW**</dt></span></span> </dl>    | <span data-ttu-id="47d1e-126">此函數會導致堆疊溢位。</span><span class="sxs-lookup"><span data-stu-id="47d1e-126">This function would cause a stack overflow.</span></span> <span data-ttu-id="47d1e-127">若未設定錯誤旗標，則會忽略有問題的函式，而不會有任何副作用。</span><span class="sxs-lookup"><span data-stu-id="47d1e-127">The offending function is ignored, having no side effect other than to set the error flag.</span></span><br/>                            |
| <dl> <span data-ttu-id="47d1e-128"><dt>**GL \_ 堆疊 \_ 下溢**</dt></span><span class="sxs-lookup"><span data-stu-id="47d1e-128"><dt>**GL\_STACK\_UNDERFLOW**</dt></span></span> </dl>   | <span data-ttu-id="47d1e-129">此函數會導致堆疊下溢。</span><span class="sxs-lookup"><span data-stu-id="47d1e-129">This function would cause a stack underflow.</span></span> <span data-ttu-id="47d1e-130">若未設定錯誤旗標，則會忽略有問題的函式，而不會有任何副作用。</span><span class="sxs-lookup"><span data-stu-id="47d1e-130">The offending function is ignored, having no side effect other than to set the error flag.</span></span><br/>                           |
| <dl> <span data-ttu-id="47d1e-131"><dt>**GL \_ \_ 記憶體不足 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="47d1e-131"><dt>**GL\_OUT\_OF\_MEMORY**</dt></span></span> </dl>    | <span data-ttu-id="47d1e-132">沒有足夠的記憶體可執行函式。</span><span class="sxs-lookup"><span data-stu-id="47d1e-132">There is not enough memory left to execute the function.</span></span> <span data-ttu-id="47d1e-133">在記錄此錯誤之後，不會定義 OpenGL 的狀態，除了錯誤旗標的狀態。</span><span class="sxs-lookup"><span data-stu-id="47d1e-133">The state of OpenGL is undefined, except for the state of the error flags, after this error is recorded.</span></span><br/> |



 

<span data-ttu-id="47d1e-134">請注意 ， \_ \_ 如果呼叫 [**GlBegin**](glbegin.md)和其對應的 [**glEnd**](glend.md)呼叫之間呼叫 glGetError，則會傳回 GL 不正確作業。</span><span class="sxs-lookup"><span data-stu-id="47d1e-134">Note that **glGetError** returns GL\_INVALID\_OPERATION if it is called between a call to [**glBegin**](glbegin.md) and its corresponding call to [**glEnd**](glend.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="47d1e-135">備註</span><span class="sxs-lookup"><span data-stu-id="47d1e-135">Remarks</span></span>

<span data-ttu-id="47d1e-136">每個可偵測的錯誤都會被指派一個數位代碼和符號名稱。</span><span class="sxs-lookup"><span data-stu-id="47d1e-136">Each detectable error is assigned a numeric code and symbolic name.</span></span> <span data-ttu-id="47d1e-137">發生錯誤時，錯誤旗標會設定為適當的錯誤碼值。</span><span class="sxs-lookup"><span data-stu-id="47d1e-137">When an error occurs, the error flag is set to the appropriate error code value.</span></span> <span data-ttu-id="47d1e-138">在呼叫 **glGetError** 之前，不會記錄其他錯誤，會傳回錯誤碼，並將旗標重設為 GL \_ 無 \_ 錯誤。</span><span class="sxs-lookup"><span data-stu-id="47d1e-138">No other errors are recorded until **glGetError** is called, the error code is returned, and the flag is reset to GL\_NO\_ERROR.</span></span> <span data-ttu-id="47d1e-139">如果呼叫 **glGetError** 時 \_ 未 \_ 發生錯誤，則在上一次呼叫 **GlGetError** 之後，或由於 OpenGL 已初始化，即沒有可偵測的錯誤。</span><span class="sxs-lookup"><span data-stu-id="47d1e-139">If a call to **glGetError** returns GL\_NO\_ERROR, there has been no detectable error since the last call to **glGetError**, or since OpenGL was initialized.</span></span>

<span data-ttu-id="47d1e-140">若要允許分散式執行，可能會有數個錯誤旗標。</span><span class="sxs-lookup"><span data-stu-id="47d1e-140">To allow for distributed implementations, there may be several error flags.</span></span> <span data-ttu-id="47d1e-141">如果有任何單一錯誤旗標已記錄錯誤，則會傳回該旗標的值，並在呼叫 GlGetError 時，將旗標重設為 GL \_ 無 \_ 錯誤。 </span><span class="sxs-lookup"><span data-stu-id="47d1e-141">If any single error flag has recorded an error, the value of that flag is returned and that flag is reset to GL\_NO\_ERROR when **glGetError** is called.</span></span> <span data-ttu-id="47d1e-142">如果有一個以上的旗標已記錄錯誤， **glGetError** 會傳回並清除任意錯誤旗標值。</span><span class="sxs-lookup"><span data-stu-id="47d1e-142">If more than one flag has recorded an error, **glGetError** returns and clears an arbitrary error flag value.</span></span> <span data-ttu-id="47d1e-143">如果要重設所有錯誤旗標，您應該一律在迴圈中呼叫 **glGetError** ，直到它傳回 GL \_ 沒有錯誤為止 \_ 。</span><span class="sxs-lookup"><span data-stu-id="47d1e-143">If all error flags are to be reset, you should always call **glGetError** in a loop until it returns GL\_NO\_ERROR.</span></span>

<span data-ttu-id="47d1e-144">一開始，所有錯誤旗標都會設定為 GL \_ 無 \_ 錯誤。</span><span class="sxs-lookup"><span data-stu-id="47d1e-144">Initially, all error flags are set to GL\_NO\_ERROR.</span></span>

<span data-ttu-id="47d1e-145">設定錯誤旗標時，只有當 GL 記憶體不足時，才會定義 OpenGL 作業的結果 \_ \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="47d1e-145">When an error flag is set, results of an OpenGL operation are undefined only if GL\_OUT\_OF\_MEMORY has occurred.</span></span> <span data-ttu-id="47d1e-146">在所有其他情況下，會忽略產生錯誤的函式，且不會影響 OpenGL 狀態或畫面格緩衝區內容。</span><span class="sxs-lookup"><span data-stu-id="47d1e-146">In all other cases, the function generating the error is ignored and has no effect on the OpenGL state or framebuffer contents.</span></span>

## <a name="requirements"></a><span data-ttu-id="47d1e-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="47d1e-147">Requirements</span></span>



| <span data-ttu-id="47d1e-148">需求</span><span class="sxs-lookup"><span data-stu-id="47d1e-148">Requirement</span></span> | <span data-ttu-id="47d1e-149">值</span><span class="sxs-lookup"><span data-stu-id="47d1e-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="47d1e-150">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="47d1e-150">Minimum supported client</span></span><br/> | <span data-ttu-id="47d1e-151">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="47d1e-151">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="47d1e-152">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="47d1e-152">Minimum supported server</span></span><br/> | <span data-ttu-id="47d1e-153">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="47d1e-153">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="47d1e-154">標頭</span><span class="sxs-lookup"><span data-stu-id="47d1e-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="47d1e-155"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="47d1e-155"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="47d1e-156">程式庫</span><span class="sxs-lookup"><span data-stu-id="47d1e-156">Library</span></span><br/>                  | <dl> <span data-ttu-id="47d1e-157"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="47d1e-157"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="47d1e-158">DLL</span><span class="sxs-lookup"><span data-stu-id="47d1e-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="47d1e-159"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47d1e-159"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47d1e-160">另請參閱</span><span class="sxs-lookup"><span data-stu-id="47d1e-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47d1e-161">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="47d1e-161">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="47d1e-162">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="47d1e-162">**glEnd**</span></span>](glend.md)
</dt> </dl>

 

 





