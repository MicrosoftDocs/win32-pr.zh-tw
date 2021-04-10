---
title: 'glCallLists 函式 (Gl) '
description: GlCallLists 函式會執行顯示清單清單。
ms.assetid: 7c0a00df-91ee-44ad-9e02-97c1b078e87f
keywords:
- glCallLists 函式 OpenGL
topic_type:
- apiref
api_name:
- glCallLists
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a119f3a63b0f04140a72cc5ca818833ae9ea8b20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934514"
---
# <a name="glcalllists-function"></a><span data-ttu-id="50785-104">glCallLists 函式</span><span class="sxs-lookup"><span data-stu-id="50785-104">glCallLists function</span></span>

<span data-ttu-id="50785-105">**GlCallLists** 函式會執行顯示清單清單。</span><span class="sxs-lookup"><span data-stu-id="50785-105">The **glCallLists** function executes a list of display lists.</span></span>

## <a name="syntax"></a><span data-ttu-id="50785-106">語法</span><span class="sxs-lookup"><span data-stu-id="50785-106">Syntax</span></span>


```C++
void WINAPI glCallLists(
         GLsizei n,
         GLenum  type,
   const GLvoid  *lists
);
```



## <a name="parameters"></a><span data-ttu-id="50785-107">參數</span><span class="sxs-lookup"><span data-stu-id="50785-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50785-108">*n*</span><span class="sxs-lookup"><span data-stu-id="50785-108">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="50785-109">要執行的顯示清單數目。</span><span class="sxs-lookup"><span data-stu-id="50785-109">The number of display lists to be executed.</span></span>

</dd> <dt>

<span data-ttu-id="50785-110">*type*</span><span class="sxs-lookup"><span data-stu-id="50785-110">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="50785-111">*清單* 中的數值型別。</span><span class="sxs-lookup"><span data-stu-id="50785-111">The type of values in *lists*.</span></span> <span data-ttu-id="50785-112">接受下列符號常數。</span><span class="sxs-lookup"><span data-stu-id="50785-112">The following symbolic constants are accepted.</span></span>



| <span data-ttu-id="50785-113">值</span><span class="sxs-lookup"><span data-stu-id="50785-113">Value</span></span>                                                                                                                                                                      | <span data-ttu-id="50785-114">意義</span><span class="sxs-lookup"><span data-stu-id="50785-114">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_BYTE"></span><span id="gl_byte"></span><dl> <span data-ttu-id="50785-115"><dt>**GL \_ 位元組**</dt></span><span class="sxs-lookup"><span data-stu-id="50785-115"><dt>**GL\_BYTE**</dt></span></span> </dl>                                | <span data-ttu-id="50785-116">List *參數會* 被視為帶正負號之位元組的陣列，每個都在128到127的範圍中。</span><span class="sxs-lookup"><span data-stu-id="50785-116">The *lists* parameter is treated as an array of signed bytes, each in the range -128 through 127.</span></span><br/>                                                                                                                                                                                                                                                                                       |
| <span id="GL_UNSIGNED_BYTE"></span><span id="gl_unsigned_byte"></span><dl> <span data-ttu-id="50785-117"><dt>**GL 不 \_ 帶正負號的 \_ 位元組**</dt></span><span class="sxs-lookup"><span data-stu-id="50785-117"><dt>**GL\_UNSIGNED\_BYTE**</dt></span></span> </dl>    | <span data-ttu-id="50785-118">*Lists* 參數會被視為不帶正負號的位元組陣列，每個都在0到255的範圍內。</span><span class="sxs-lookup"><span data-stu-id="50785-118">The *lists* parameter is treated as an array of unsigned bytes, each in the range 0 through 255.</span></span><br/>                                                                                                                                                                                                                                                                                        |
| <span id="GL_SHORT"></span><span id="gl_short"></span><dl> <span data-ttu-id="50785-119"><dt>**GL \_ 短期**</dt></span><span class="sxs-lookup"><span data-stu-id="50785-119"><dt>**GL\_SHORT**</dt></span></span> </dl>                             | <span data-ttu-id="50785-120">*Lists* 參數會被視為帶正負號的2位元組整數陣列，每個都在範圍-32768 到32767之間。</span><span class="sxs-lookup"><span data-stu-id="50785-120">The *lists* parameter is treated as an array of signed 2-byte integers, each in the range -32768 through 32767.</span></span><br/>                                                                                                                                                                                                                                                                         |
| <span id="GL_UNSIGNED_SHORT"></span><span id="gl_unsigned_short"></span><dl> <span data-ttu-id="50785-121"><dt>**GL 不 \_ 帶正負號 \_ 簡短**</dt></span><span class="sxs-lookup"><span data-stu-id="50785-121"><dt>**GL\_UNSIGNED\_SHORT**</dt></span></span> </dl> | <span data-ttu-id="50785-122">*Lists* 參數會被視為不帶正負號的2位元組整數陣列，每個都在0到65535的範圍內。</span><span class="sxs-lookup"><span data-stu-id="50785-122">The *lists* parameter is treated as an array of unsigned 2-byte integers, each in the range 0 through 65535.</span></span><br/>                                                                                                                                                                                                                                                                            |
| <span id="GL_INT"></span><span id="gl_int"></span><dl> <span data-ttu-id="50785-123"><dt>**GL \_ INT**</dt></span><span class="sxs-lookup"><span data-stu-id="50785-123"><dt>**GL\_INT**</dt></span></span> </dl>                                   | <span data-ttu-id="50785-124">*Lists* 參數會被視為帶正負號之4位元組整數的陣列。</span><span class="sxs-lookup"><span data-stu-id="50785-124">The *lists* parameter is treated as an array of signed 4-byte integers.</span></span><br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="GL_UNSIGNED_INT"></span><span id="gl_unsigned_int"></span><dl> <span data-ttu-id="50785-125"><dt>**GL 不 \_ 帶正負號 \_ INT**</dt></span><span class="sxs-lookup"><span data-stu-id="50785-125"><dt>**GL\_UNSIGNED\_INT**</dt></span></span> </dl>       | <span data-ttu-id="50785-126">*Lists* 參數會被視為不帶正負號4位元組整數的陣列。</span><span class="sxs-lookup"><span data-stu-id="50785-126">The *lists* parameter is treated as an array of unsigned 4-byte integers.</span></span><br/>                                                                                                                                                                                                                                                                                                               |
| <span id="GL_FLOAT"></span><span id="gl_float"></span><dl> <span data-ttu-id="50785-127"><dt>**GL \_ FLOAT**</dt></span><span class="sxs-lookup"><span data-stu-id="50785-127"><dt>**GL\_FLOAT**</dt></span></span> </dl>                             | <span data-ttu-id="50785-128">*Lists* 參數會被視為4位元組、浮點值的陣列。</span><span class="sxs-lookup"><span data-stu-id="50785-128">The *lists* parameter is treated as an array of 4-byte, floating-point values.</span></span><br/>                                                                                                                                                                                                                                                                                                          |
| <span id="GL_2_BYTES"></span><span id="gl_2_bytes"></span><dl> <span data-ttu-id="50785-129"><dt>**GL \_ 2 \_ 個位元組**</dt></span><span class="sxs-lookup"><span data-stu-id="50785-129"><dt>**GL\_2\_BYTES**</dt></span></span> </dl>                      | <span data-ttu-id="50785-130">*Lists* 參數會被視為不帶正負號的位元組陣列。</span><span class="sxs-lookup"><span data-stu-id="50785-130">The *lists* parameter is treated as an array of unsigned bytes.</span></span> <span data-ttu-id="50785-131">每一對位元組都指定單一顯示清單名稱。</span><span class="sxs-lookup"><span data-stu-id="50785-131">Each pair of bytes specifies a single display-list name.</span></span> <span data-ttu-id="50785-132">配對的值會計算為第一個位元組不帶正負號值的256倍加上第二個位元組的不帶正負號值。</span><span class="sxs-lookup"><span data-stu-id="50785-132">The value of the pair is computed as 256 times the unsigned value of the first byte plus the unsigned value of the second byte.</span></span><br/>                                                                                                                                |
| <span id="GL_3_BYTES"></span><span id="gl_3_bytes"></span><dl> <span data-ttu-id="50785-133"><dt>**GL \_ 3 \_ 位元組**</dt></span><span class="sxs-lookup"><span data-stu-id="50785-133"><dt>**GL\_3\_BYTES**</dt></span></span> </dl>                      | <span data-ttu-id="50785-134">*Lists* 參數會被視為不帶正負號的位元組陣列。</span><span class="sxs-lookup"><span data-stu-id="50785-134">The *lists* parameter is treated as an array of unsigned bytes.</span></span> <span data-ttu-id="50785-135">每三個位元組都指定單一顯示清單名稱。</span><span class="sxs-lookup"><span data-stu-id="50785-135">Each triplet of bytes specifies a single display list name.</span></span> <span data-ttu-id="50785-136">三元的值會計算為第一個位元組不帶正負號值的65536倍，加上第二個位元組不帶正負號值的256倍，再加上第三個位元組的不帶正負號值。</span><span class="sxs-lookup"><span data-stu-id="50785-136">The value of the triplet is computed as 65536 times the unsigned value of the first byte, plus 256 times the unsigned value of the second byte, plus the unsigned value of the third byte.</span></span><br/>                                                                  |
| <span id="GL_4_BYTES"></span><span id="gl_4_bytes"></span><dl> <span data-ttu-id="50785-137"><dt>**GL \_ 4 \_ 位元組**</dt></span><span class="sxs-lookup"><span data-stu-id="50785-137"><dt>**GL\_4\_BYTES**</dt></span></span> </dl>                      | <span data-ttu-id="50785-138">*Lists* 參數會被視為不帶正負號的位元組陣列。</span><span class="sxs-lookup"><span data-stu-id="50785-138">The *lists* parameter is treated as an array of unsigned bytes.</span></span> <span data-ttu-id="50785-139">每個位元組 quadruplet 會指定單一顯示清單名稱。</span><span class="sxs-lookup"><span data-stu-id="50785-139">Each quadruplet of bytes specifies a single display list name.</span></span> <span data-ttu-id="50785-140">Quadruplet 的值會計算為第一個位元組不帶正負號值的16777216倍，加上第二個位元組不帶正負號值的65536倍，加上第三個位元組不帶正負號值的256倍，再加上第四個位元組的不帶正負號值。</span><span class="sxs-lookup"><span data-stu-id="50785-140">The value of the quadruplet is computed as 16777216 times the unsigned value of the first byte, plus 65536 times the unsigned value of the second byte, plus 256 times the unsigned value of the third byte, plus the unsigned value of the fourth byte.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="50785-141">*清單*</span><span class="sxs-lookup"><span data-stu-id="50785-141">*lists*</span></span> 
</dt> <dd>

<span data-ttu-id="50785-142">顯示清單中名稱位移陣列的位址。</span><span class="sxs-lookup"><span data-stu-id="50785-142">The address of an array of name offsets in the display list.</span></span> <span data-ttu-id="50785-143">指標類型為 void，因為位移可以是位元組、短、整數或浮點數，這取決於 *類型* 的值。</span><span class="sxs-lookup"><span data-stu-id="50785-143">The pointer type is void because the offsets can be bytes, shorts, ints, or floats, depending on the value of *type*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50785-144">傳回值</span><span class="sxs-lookup"><span data-stu-id="50785-144">Return value</span></span>

<span data-ttu-id="50785-145">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="50785-145">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="50785-146">備註</span><span class="sxs-lookup"><span data-stu-id="50785-146">Remarks</span></span>

<span data-ttu-id="50785-147">**GlCallLists** 函式會將名稱清單中的每個顯示清單視為 *要執行的清單。*</span><span class="sxs-lookup"><span data-stu-id="50785-147">The **glCallLists** function causes each display list in the list of names passed as *lists* to be executed.</span></span> <span data-ttu-id="50785-148">因此，儲存在每個顯示清單中的函式會依序執行，就像在不使用顯示清單的情況下呼叫一樣。</span><span class="sxs-lookup"><span data-stu-id="50785-148">As a result, the functions saved in each display list are executed in order, just as if they were called without using a display list.</span></span> <span data-ttu-id="50785-149">未定義的顯示清單名稱將會被忽略。</span><span class="sxs-lookup"><span data-stu-id="50785-149">Names of display lists that have not been defined are ignored.</span></span>

<span data-ttu-id="50785-150">**GlCallLists** 函式提供一種有效率的方式來執行顯示清單。</span><span class="sxs-lookup"><span data-stu-id="50785-150">The **glCallLists** function provides an efficient means for executing display lists.</span></span> <span data-ttu-id="50785-151">*N* 參數會指定) **glCallLists** 執行的 *類型* 參數所指定的不同名稱格式 (清單數目。</span><span class="sxs-lookup"><span data-stu-id="50785-151">The *n* parameter specifies the number of lists with various name formats (specified by the *type* parameter) **glCallLists** executes.</span></span>

<span data-ttu-id="50785-152">顯示清單名稱的清單不是以 null 結束。</span><span class="sxs-lookup"><span data-stu-id="50785-152">The list of display list names is not null-terminated.</span></span> <span data-ttu-id="50785-153">相反地， *n* 指定要從 *清單* 中取得多少名稱。</span><span class="sxs-lookup"><span data-stu-id="50785-153">Rather, *n* specifies how many names are to be taken from *lists*.</span></span>

<span data-ttu-id="50785-154">[**GlListBase**](gllistbase.md)函式可提供額外的間接取值層級。</span><span class="sxs-lookup"><span data-stu-id="50785-154">The [**glListBase**](gllistbase.md) function makes an additional level of indirection available.</span></span> <span data-ttu-id="50785-155">**GlListBase** 函式會指定不帶正負號的位移，該位移會新增至 *清單* 中指定的每個顯示清單名稱，再執行該顯示清單。</span><span class="sxs-lookup"><span data-stu-id="50785-155">The **glListBase** function specifies an unsigned offset that is added to each display list name specified in *lists* before that display list is executed.</span></span>

<span data-ttu-id="50785-156">**GlCallLists** 函數可以出現在顯示清單中。</span><span class="sxs-lookup"><span data-stu-id="50785-156">The **glCallLists** function can appear inside a display list.</span></span> <span data-ttu-id="50785-157">為了避免因為顯示清單彼此呼叫而產生無限遞迴的可能性，在顯示清單執行期間，會在顯示清單的嵌套層級上設定限制。</span><span class="sxs-lookup"><span data-stu-id="50785-157">To avoid the possibility of infinite recursion resulting from display lists calling one another, a limit is placed on the nesting level of display lists during display list execution.</span></span> <span data-ttu-id="50785-158">此限制必須至少為64，且取決於執行。</span><span class="sxs-lookup"><span data-stu-id="50785-158">This limit must be at least 64, and it depends on the implementation.</span></span>

<span data-ttu-id="50785-159">在呼叫 **glCallLists** 時，不會儲存並還原 OpenGL 狀態。</span><span class="sxs-lookup"><span data-stu-id="50785-159">The OpenGL state is not saved and restored across a call to **glCallLists**.</span></span> <span data-ttu-id="50785-160">因此，在執行完成之後，在顯示清單執行期間對 OpenGL 狀態所做的變更仍會保留。</span><span class="sxs-lookup"><span data-stu-id="50785-160">Thus, changes made to the OpenGL state during the execution of the display lists remain after execution is completed.</span></span> <span data-ttu-id="50785-161">使用 [**glPushAttrib**](glpushattrib.md)、 [**glPopAttrib**](glpopattrib.md)、 [**glPushMatrix**](glpushmatrix.md)和 [**glPopMatrix**](glpopmatrix.md) ，可在 **glCallLists** 呼叫之間保留 OpenGL 狀態。</span><span class="sxs-lookup"><span data-stu-id="50785-161">Use [**glPushAttrib**](glpushattrib.md), [**glPopAttrib**](glpopattrib.md), [**glPushMatrix**](glpushmatrix.md), and [**glPopMatrix**](glpopmatrix.md) to preserve the OpenGL state across **glCallLists** calls.</span></span>

<span data-ttu-id="50785-162">只要顯示清單只包含此間隔中允許的函式，您就可以在呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間執行顯示清單。</span><span class="sxs-lookup"><span data-stu-id="50785-162">You can execute display lists between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md), as long as the display list includes only functions that are allowed in this interval.</span></span>

<span data-ttu-id="50785-163">下列函式會取出與 **glCallLists** 函數相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="50785-163">The following functions retrieve information related to the **glCallLists** function:</span></span>

<span data-ttu-id="50785-164">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 清單 \_ 基底的 glGet</span><span class="sxs-lookup"><span data-stu-id="50785-164">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_LIST\_BASE</span></span>

<span data-ttu-id="50785-165">具有引數 GL \_ 最大 \_ 清單 \_ 嵌套的 glGet</span><span class="sxs-lookup"><span data-stu-id="50785-165">**glGet** with argument GL\_MAX\_LIST\_NESTING</span></span>

[<span data-ttu-id="50785-166">**glIsList**</span><span class="sxs-lookup"><span data-stu-id="50785-166">**glIsList**</span></span>](glislist.md)

## <a name="requirements"></a><span data-ttu-id="50785-167">規格需求</span><span class="sxs-lookup"><span data-stu-id="50785-167">Requirements</span></span>



| <span data-ttu-id="50785-168">需求</span><span class="sxs-lookup"><span data-stu-id="50785-168">Requirement</span></span> | <span data-ttu-id="50785-169">值</span><span class="sxs-lookup"><span data-stu-id="50785-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="50785-170">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="50785-170">Minimum supported client</span></span><br/> | <span data-ttu-id="50785-171">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="50785-171">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="50785-172">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="50785-172">Minimum supported server</span></span><br/> | <span data-ttu-id="50785-173">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="50785-173">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="50785-174">標頭</span><span class="sxs-lookup"><span data-stu-id="50785-174">Header</span></span><br/>                   | <dl> <span data-ttu-id="50785-175"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="50785-175"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="50785-176">程式庫</span><span class="sxs-lookup"><span data-stu-id="50785-176">Library</span></span><br/>                  | <dl> <span data-ttu-id="50785-177"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="50785-177"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="50785-178">DLL</span><span class="sxs-lookup"><span data-stu-id="50785-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50785-179"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50785-179"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50785-180">另請參閱</span><span class="sxs-lookup"><span data-stu-id="50785-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50785-181">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="50785-181">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="50785-182">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="50785-182">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="50785-183">**glDeleteLists**</span><span class="sxs-lookup"><span data-stu-id="50785-183">**glDeleteLists**</span></span>](gldeletelists.md)
</dt> <dt>

[<span data-ttu-id="50785-184">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="50785-184">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="50785-185">**glGenLists**</span><span class="sxs-lookup"><span data-stu-id="50785-185">**glGenLists**</span></span>](glgenlists.md)
</dt> <dt>

[<span data-ttu-id="50785-186">**glGet**</span><span class="sxs-lookup"><span data-stu-id="50785-186">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="50785-187">**glIsList**</span><span class="sxs-lookup"><span data-stu-id="50785-187">**glIsList**</span></span>](glislist.md)
</dt> <dt>

[<span data-ttu-id="50785-188">**glListBase**</span><span class="sxs-lookup"><span data-stu-id="50785-188">**glListBase**</span></span>](gllistbase.md)
</dt> <dt>

[<span data-ttu-id="50785-189">**glNewList**</span><span class="sxs-lookup"><span data-stu-id="50785-189">**glNewList**</span></span>](glnewlist.md)
</dt> <dt>

[<span data-ttu-id="50785-190">**glPopAttrib**</span><span class="sxs-lookup"><span data-stu-id="50785-190">**glPopAttrib**</span></span>](glpopattrib.md)
</dt> <dt>

[<span data-ttu-id="50785-191">**glPopMatrix**</span><span class="sxs-lookup"><span data-stu-id="50785-191">**glPopMatrix**</span></span>](glpopmatrix.md)
</dt> <dt>

[<span data-ttu-id="50785-192">**glPushAttrib**</span><span class="sxs-lookup"><span data-stu-id="50785-192">**glPushAttrib**</span></span>](glpushattrib.md)
</dt> <dt>

[<span data-ttu-id="50785-193">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="50785-193">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> </dl>

 

 





