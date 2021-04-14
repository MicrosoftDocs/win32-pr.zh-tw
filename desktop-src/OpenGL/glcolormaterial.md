---
title: 'glColorMaterial 函式 (Gl) '
description: GlColorMaterial 函式會導致材質色彩追蹤目前的色彩。
ms.assetid: 6dbef2c2-f902-4f25-8a87-9e3d710dd807
keywords:
- glColorMaterial 函式 OpenGL
topic_type:
- apiref
api_name:
- glColorMaterial
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d32823eaa82e6a260790dd6fa23747f2b4228649
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384822"
---
# <a name="glcolormaterial-function"></a><span data-ttu-id="5e4c2-104">glColorMaterial 函式</span><span class="sxs-lookup"><span data-stu-id="5e4c2-104">glColorMaterial function</span></span>

<span data-ttu-id="5e4c2-105">**GlColorMaterial** 函式會導致材質色彩追蹤目前的色彩。</span><span class="sxs-lookup"><span data-stu-id="5e4c2-105">The **glColorMaterial** function causes a material color to track the current color.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e4c2-106">語法</span><span class="sxs-lookup"><span data-stu-id="5e4c2-106">Syntax</span></span>


```C++
void WINAPI glColorMaterial(
   GLenum face,
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="5e4c2-107">參數</span><span class="sxs-lookup"><span data-stu-id="5e4c2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e4c2-108">*臉*</span><span class="sxs-lookup"><span data-stu-id="5e4c2-108">*face*</span></span> 
</dt> <dd>

<span data-ttu-id="5e4c2-109">指定 front、back 或 front 和 back 材質參數是否都應該追蹤目前的色彩。</span><span class="sxs-lookup"><span data-stu-id="5e4c2-109">Specifies whether front, back, or both front and back material parameters should track the current color.</span></span> <span data-ttu-id="5e4c2-110">接受的值是 GL \_ 前端、gl \_ 回來，以及 gl \_ 前端 \_ 和 \_ 後端。</span><span class="sxs-lookup"><span data-stu-id="5e4c2-110">Accepted values are GL\_FRONT, GL\_BACK, and GL\_FRONT\_AND\_BACK.</span></span> <span data-ttu-id="5e4c2-111">預設值是 GL \_ FRONT \_ 和 \_ BACK。</span><span class="sxs-lookup"><span data-stu-id="5e4c2-111">The default value is GL\_FRONT\_AND\_BACK.</span></span>

</dd> <dt>

<span data-ttu-id="5e4c2-112">*mode*</span><span class="sxs-lookup"><span data-stu-id="5e4c2-112">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="5e4c2-113">指定要追蹤目前色彩的數個材質參數。</span><span class="sxs-lookup"><span data-stu-id="5e4c2-113">Specifies which of several material parameters track the current color.</span></span> <span data-ttu-id="5e4c2-114">接受的值為 GL 發出 \_ 、gl \_ 環境、gl \_ 擴散、gl \_ 反射，以及 gl \_ 環境 \_ 和 \_ 擴散。</span><span class="sxs-lookup"><span data-stu-id="5e4c2-114">Accepted values are GL\_EMISSION, GL\_AMBIENT, GL\_DIFFUSE, GL\_SPECULAR, and GL\_AMBIENT\_AND\_DIFFUSE.</span></span> <span data-ttu-id="5e4c2-115">預設值為 GL \_ 環境 \_ 和 \_ 擴散。</span><span class="sxs-lookup"><span data-stu-id="5e4c2-115">The default value is GL\_AMBIENT\_AND\_DIFFUSE.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e4c2-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="5e4c2-116">Return value</span></span>

<span data-ttu-id="5e4c2-117">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="5e4c2-117">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5e4c2-118">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="5e4c2-118">Error codes</span></span>

<span data-ttu-id="5e4c2-119">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="5e4c2-119">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="5e4c2-120">Name</span><span class="sxs-lookup"><span data-stu-id="5e4c2-120">Name</span></span>                                                                                                  | <span data-ttu-id="5e4c2-121">意義</span><span class="sxs-lookup"><span data-stu-id="5e4c2-121">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5e4c2-122"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="5e4c2-122"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="5e4c2-123">*臉部* 或 *模式* 不是可接受的值。</span><span class="sxs-lookup"><span data-stu-id="5e4c2-123">*face* or *mode* was not an accepted value.</span></span><br/>                                                                                |
| <dl> <span data-ttu-id="5e4c2-124"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="5e4c2-124"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="5e4c2-125">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="5e4c2-125">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="5e4c2-126">備註</span><span class="sxs-lookup"><span data-stu-id="5e4c2-126">Remarks</span></span>

<span data-ttu-id="5e4c2-127">**GlColorMaterial** 函數會指定追蹤目前色彩的材質參數。</span><span class="sxs-lookup"><span data-stu-id="5e4c2-127">The **glColorMaterial** function specifies which material parameters track the current color.</span></span> <span data-ttu-id="5e4c2-128">當您 \_ \_ 針對 *臉部* 所指定的每個材質或材質啟用 GL 色彩材質時，由 *模式* 指定的材質參數或參數會隨時追蹤目前的色彩。</span><span class="sxs-lookup"><span data-stu-id="5e4c2-128">When you enable GL\_COLOR\_MATERIAL, for each of the material or materials specified by *face*, the material parameter or parameters specified by *mode* track the current color at all times.</span></span> <span data-ttu-id="5e4c2-129">使用 GlEnable 和 GlDisable 函式來啟用和停 \_ 用 gl 色彩 \_ 材質，以 GL [](glenable.md) [](gldisable.md) \_ 色彩 \_ 材質作為其引數來呼叫。</span><span class="sxs-lookup"><span data-stu-id="5e4c2-129">Enable and disable GL\_COLOR\_MATERIAL with the functions [**glEnable**](glenable.md) and [**glDisable**](gldisable.md), which you call with GL\_COLOR\_MATERIAL as their argument.</span></span> <span data-ttu-id="5e4c2-130">預設 \_ \_ 會停用 GL 色彩材質。</span><span class="sxs-lookup"><span data-stu-id="5e4c2-130">By default, GL\_COLOR\_MATERIAL is disabled.</span></span>

<span data-ttu-id="5e4c2-131">使用 **glColorMaterial**，您可以只使用 [**glColor**](glcolor-functions.md) 函數來變更每個頂點的材質參數子集，而不需要呼叫 [**glMaterial**](glmaterial-functions.md)。</span><span class="sxs-lookup"><span data-stu-id="5e4c2-131">With **glColorMaterial**, you can change a subset of material parameters for each vertex using only the [**glColor**](glcolor-functions.md) function, without calling [**glMaterial**](glmaterial-functions.md).</span></span> <span data-ttu-id="5e4c2-132">如果您只是針對每個頂點指定這類參數子集，最好使用 **glColorMaterial** 而不是 **glMaterial**。</span><span class="sxs-lookup"><span data-stu-id="5e4c2-132">If you are going to specify only such a subset of parameters for each vertex, it is better to do so with **glColorMaterial** than with **glMaterial**.</span></span>

<span data-ttu-id="5e4c2-133">下列函式會取出與 **glColorMaterial** 相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="5e4c2-133">The following functions retrieve information related to **glColorMaterial**:</span></span>

<span data-ttu-id="5e4c2-134">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ COLOR \_ 材質 \_ 參數的 glGet</span><span class="sxs-lookup"><span data-stu-id="5e4c2-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_COLOR\_MATERIAL\_PARAMETER</span></span>

<span data-ttu-id="5e4c2-135">**glGet** 與引數 GL \_ 色彩 \_ 材質 \_ 臉部</span><span class="sxs-lookup"><span data-stu-id="5e4c2-135">**glGet** with argument GL\_COLOR\_MATERIAL\_FACE</span></span>

<span data-ttu-id="5e4c2-136">[](glisenabled.md)具有引數 GL \_ 色彩 \_ 材質的 glIsEnabled</span><span class="sxs-lookup"><span data-stu-id="5e4c2-136">[**glIsEnabled**](glisenabled.md) with argument GL\_COLOR\_MATERIAL</span></span>

## <a name="requirements"></a><span data-ttu-id="5e4c2-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="5e4c2-137">Requirements</span></span>



| <span data-ttu-id="5e4c2-138">需求</span><span class="sxs-lookup"><span data-stu-id="5e4c2-138">Requirement</span></span> | <span data-ttu-id="5e4c2-139">值</span><span class="sxs-lookup"><span data-stu-id="5e4c2-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5e4c2-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5e4c2-140">Minimum supported client</span></span><br/> | <span data-ttu-id="5e4c2-141">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5e4c2-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="5e4c2-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5e4c2-142">Minimum supported server</span></span><br/> | <span data-ttu-id="5e4c2-143">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5e4c2-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5e4c2-144">標頭</span><span class="sxs-lookup"><span data-stu-id="5e4c2-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e4c2-145"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="5e4c2-145"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="5e4c2-146">程式庫</span><span class="sxs-lookup"><span data-stu-id="5e4c2-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="5e4c2-147"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="5e4c2-147"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="5e4c2-148">DLL</span><span class="sxs-lookup"><span data-stu-id="5e4c2-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e4c2-149"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e4c2-149"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e4c2-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5e4c2-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e4c2-151">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="5e4c2-151">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="5e4c2-152">**glColor**</span><span class="sxs-lookup"><span data-stu-id="5e4c2-152">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="5e4c2-153">**glDisable**</span><span class="sxs-lookup"><span data-stu-id="5e4c2-153">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="5e4c2-154">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="5e4c2-154">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="5e4c2-155">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="5e4c2-155">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="5e4c2-156">**glGet**</span><span class="sxs-lookup"><span data-stu-id="5e4c2-156">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="5e4c2-157">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="5e4c2-157">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="5e4c2-158">**glLight**</span><span class="sxs-lookup"><span data-stu-id="5e4c2-158">**glLight**</span></span>](gllight-functions.md)
</dt> <dt>

[<span data-ttu-id="5e4c2-159">**glLightModel**</span><span class="sxs-lookup"><span data-stu-id="5e4c2-159">**glLightModel**</span></span>](gllightmodel-functions.md)
</dt> <dt>

[<span data-ttu-id="5e4c2-160">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="5e4c2-160">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> </dl>

 

 





