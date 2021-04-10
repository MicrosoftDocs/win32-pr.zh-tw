---
title: 'glCallList 函式 (Gl) '
description: GlCallList 函式會執行顯示清單。
ms.assetid: 9373d32e-b11e-4a80-8713-da2c1d8d9368
keywords:
- glCallList 函式 OpenGL
topic_type:
- apiref
api_name:
- glCallList
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0d356adc5d16ceb0ea10e3834d8dbb98abed2b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104130"
---
# <a name="glcalllist-function"></a><span data-ttu-id="04daa-104">glCallList 函式</span><span class="sxs-lookup"><span data-stu-id="04daa-104">glCallList function</span></span>

<span data-ttu-id="04daa-105">**GlCallList** 函式會執行顯示清單。</span><span class="sxs-lookup"><span data-stu-id="04daa-105">The **glCallList** function executes a display list.</span></span>

## <a name="syntax"></a><span data-ttu-id="04daa-106">語法</span><span class="sxs-lookup"><span data-stu-id="04daa-106">Syntax</span></span>


```C++
void WINAPI glCallList(
   GLuint list
);
```



## <a name="parameters"></a><span data-ttu-id="04daa-107">參數</span><span class="sxs-lookup"><span data-stu-id="04daa-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04daa-108">*list*</span><span class="sxs-lookup"><span data-stu-id="04daa-108">*list*</span></span> 
</dt> <dd>

<span data-ttu-id="04daa-109">要執行之顯示清單的整數名稱。</span><span class="sxs-lookup"><span data-stu-id="04daa-109">The integer name of the display list to be executed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04daa-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="04daa-110">Return value</span></span>

<span data-ttu-id="04daa-111">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="04daa-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="04daa-112">備註</span><span class="sxs-lookup"><span data-stu-id="04daa-112">Remarks</span></span>

<span data-ttu-id="04daa-113">叫用 **glCallList** 函式會開始執行命名的顯示清單。</span><span class="sxs-lookup"><span data-stu-id="04daa-113">Invoking the **glCallList** function begins execution of the named display list.</span></span> <span data-ttu-id="04daa-114">儲存在顯示清單中的函式會依序執行，就如同您在未使用顯示清單的情況下呼叫它們一樣。</span><span class="sxs-lookup"><span data-stu-id="04daa-114">The functions saved in the display list are executed in order, just as if you called them without using a display list.</span></span> <span data-ttu-id="04daa-115">如果 *清單* 尚未定義為顯示清單，則會忽略 **glCallList** 。</span><span class="sxs-lookup"><span data-stu-id="04daa-115">If *list* has not been defined as a display list, **glCallList** is ignored.</span></span>

<span data-ttu-id="04daa-116">**GlCallList** 函數可以出現在顯示清單中。</span><span class="sxs-lookup"><span data-stu-id="04daa-116">The **glCallList** function can appear inside a display list.</span></span> <span data-ttu-id="04daa-117">為了避免因為顯示清單彼此呼叫而產生無限遞迴的可能性，在顯示清單執行期間，會將限制放在顯示清單的嵌套層級上。</span><span class="sxs-lookup"><span data-stu-id="04daa-117">To avoid the possibility of infinite recursion resulting from display lists calling one another, a limit is placed on the nesting level of display lists during display-list execution.</span></span> <span data-ttu-id="04daa-118">這項限制至少為64，但相依于執行。</span><span class="sxs-lookup"><span data-stu-id="04daa-118">This limit is at least 64, however, it depends on the implementation.</span></span>

<span data-ttu-id="04daa-119">在呼叫 **glCallList** 時，不會儲存並還原 OpenGL 狀態。</span><span class="sxs-lookup"><span data-stu-id="04daa-119">The OpenGL state is not saved and restored across a call to **glCallList**.</span></span> <span data-ttu-id="04daa-120">因此，在顯示清單執行期間，在顯示清單執行期間所做的變更會保留下來。</span><span class="sxs-lookup"><span data-stu-id="04daa-120">Thus, changes made to the OpenGL state during the execution of a display list remain after execution of the display list is completed.</span></span> <span data-ttu-id="04daa-121">若要保留跨 **glCallList** 呼叫的 OpenGL 狀態，請使用 [**glPushAttrib**](glpushattrib.md)、 [**glPopAttrib**](glpopattrib.md)、 [**glPushMatrix**](glpushmatrix.md)和 [**glPopMatrix**](glpopmatrix.md)。</span><span class="sxs-lookup"><span data-stu-id="04daa-121">To preserve the OpenGL state across **glCallList** calls, use [**glPushAttrib**](glpushattrib.md), [**glPopAttrib**](glpopattrib.md), [**glPushMatrix**](glpushmatrix.md), and [**glPopMatrix**](glpopmatrix.md).</span></span>

<span data-ttu-id="04daa-122">只要顯示清單只包含此間隔中允許的函式，您就可以在呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間執行顯示清單。</span><span class="sxs-lookup"><span data-stu-id="04daa-122">You can execute display lists between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md), as long as the display list includes only functions that are allowed in this interval.</span></span>

<span data-ttu-id="04daa-123">下列函式會取出與 **glCallList** 相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="04daa-123">The following functions retrieve information related to **glCallList**:</span></span>

<span data-ttu-id="04daa-124">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 最大 \_ 清單 \_ 嵌套的 glGet</span><span class="sxs-lookup"><span data-stu-id="04daa-124">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAX\_LIST\_NESTING</span></span>

[<span data-ttu-id="04daa-125">**glIsList**</span><span class="sxs-lookup"><span data-stu-id="04daa-125">**glIsList**</span></span>](glislist.md)

## <a name="requirements"></a><span data-ttu-id="04daa-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="04daa-126">Requirements</span></span>



| <span data-ttu-id="04daa-127">需求</span><span class="sxs-lookup"><span data-stu-id="04daa-127">Requirement</span></span> | <span data-ttu-id="04daa-128">值</span><span class="sxs-lookup"><span data-stu-id="04daa-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="04daa-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="04daa-129">Minimum supported client</span></span><br/> | <span data-ttu-id="04daa-130">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="04daa-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="04daa-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="04daa-131">Minimum supported server</span></span><br/> | <span data-ttu-id="04daa-132">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="04daa-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="04daa-133">標頭</span><span class="sxs-lookup"><span data-stu-id="04daa-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="04daa-134"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="04daa-134"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="04daa-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="04daa-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="04daa-136"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="04daa-136"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="04daa-137">DLL</span><span class="sxs-lookup"><span data-stu-id="04daa-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04daa-138"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04daa-138"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04daa-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="04daa-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04daa-140">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="04daa-140">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="04daa-141">**glCallLists**</span><span class="sxs-lookup"><span data-stu-id="04daa-141">**glCallLists**</span></span>](glcalllists.md)
</dt> <dt>

[<span data-ttu-id="04daa-142">**glDeleteLists**</span><span class="sxs-lookup"><span data-stu-id="04daa-142">**glDeleteLists**</span></span>](gldeletelists.md)
</dt> <dt>

[<span data-ttu-id="04daa-143">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="04daa-143">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="04daa-144">**glGenLists**</span><span class="sxs-lookup"><span data-stu-id="04daa-144">**glGenLists**</span></span>](glgenlists.md)
</dt> <dt>

[<span data-ttu-id="04daa-145">**glGet**</span><span class="sxs-lookup"><span data-stu-id="04daa-145">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="04daa-146">**glIsList**</span><span class="sxs-lookup"><span data-stu-id="04daa-146">**glIsList**</span></span>](glislist.md)
</dt> <dt>

[<span data-ttu-id="04daa-147">**glNewList**</span><span class="sxs-lookup"><span data-stu-id="04daa-147">**glNewList**</span></span>](glnewlist.md)
</dt> <dt>

[<span data-ttu-id="04daa-148">**glPopAttrib**</span><span class="sxs-lookup"><span data-stu-id="04daa-148">**glPopAttrib**</span></span>](glpopattrib.md)
</dt> <dt>

[<span data-ttu-id="04daa-149">**glPopMatrix**</span><span class="sxs-lookup"><span data-stu-id="04daa-149">**glPopMatrix**</span></span>](glpopmatrix.md)
</dt> <dt>

[<span data-ttu-id="04daa-150">**glPushAttrib**</span><span class="sxs-lookup"><span data-stu-id="04daa-150">**glPushAttrib**</span></span>](glpushattrib.md)
</dt> <dt>

[<span data-ttu-id="04daa-151">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="04daa-151">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> </dl>

 

 





