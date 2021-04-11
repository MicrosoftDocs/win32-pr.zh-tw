---
title: 'glTranslatef 函式 (Gl) '
description: GlTranslatef 函式會將目前的矩陣與轉譯矩陣相乘。
ms.assetid: 2354ad52-e80f-49fc-82e7-ac6c146aa59d
keywords:
- glTranslatef 函式 OpenGL
topic_type:
- apiref
api_name:
- glTranslatef
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d5b52c3890b70ecb931211af1788afe2b8e6ad4
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "103853272"
---
# <a name="gltranslatef-function"></a><span data-ttu-id="43bf1-104">glTranslatef 函式</span><span class="sxs-lookup"><span data-stu-id="43bf1-104">glTranslatef function</span></span>

<span data-ttu-id="43bf1-105">[**GlTranslatef**](gltranslate.md)函式會將目前的矩陣與轉譯矩陣相乘。</span><span class="sxs-lookup"><span data-stu-id="43bf1-105">The [**glTranslatef**](gltranslate.md) function multiplies the current matrix by a translation matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="43bf1-106">語法</span><span class="sxs-lookup"><span data-stu-id="43bf1-106">Syntax</span></span>


```C++
void WINAPI glTranslatef(
   GLfloat x,
   GLfloat y,
   GLfloat z
);
```



## <a name="parameters"></a><span data-ttu-id="43bf1-107">參數</span><span class="sxs-lookup"><span data-stu-id="43bf1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43bf1-108">*x*</span><span class="sxs-lookup"><span data-stu-id="43bf1-108">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="43bf1-109">平移向量的 *x* 座標。</span><span class="sxs-lookup"><span data-stu-id="43bf1-109">The *x* coordinate of a translation vector.</span></span>

</dd> <dt>

<span data-ttu-id="43bf1-110">*y*</span><span class="sxs-lookup"><span data-stu-id="43bf1-110">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="43bf1-111">平移向量的 *y* 座標。</span><span class="sxs-lookup"><span data-stu-id="43bf1-111">The *y* coordinate of a translation vector.</span></span>

</dd> <dt>

<span data-ttu-id="43bf1-112">*Z*</span><span class="sxs-lookup"><span data-stu-id="43bf1-112">*z*</span></span> 
</dt> <dd>

<span data-ttu-id="43bf1-113">平移向量的 *z* 座標。</span><span class="sxs-lookup"><span data-stu-id="43bf1-113">The *z* coordinate of a translation vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43bf1-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="43bf1-114">Return value</span></span>

<span data-ttu-id="43bf1-115">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="43bf1-115">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="43bf1-116">備註</span><span class="sxs-lookup"><span data-stu-id="43bf1-116">Remarks</span></span>

<span data-ttu-id="43bf1-117">**GlTranslatef** 函式會產生由 (*x*、 *y*、 *z*) 指定的平移。</span><span class="sxs-lookup"><span data-stu-id="43bf1-117">The **glTranslatef** function produces the translation specified by (*x*, *y*, *z*).</span></span> <span data-ttu-id="43bf1-118">轉譯向量用來計算4x4 平移矩陣：</span><span class="sxs-lookup"><span data-stu-id="43bf1-118">The translation vector is used to compute a 4x4 translation matrix:</span></span>

![顯示 x、y、z 所指定之4x4 平移矩陣的圖表。](images/trans01.png)

<span data-ttu-id="43bf1-120">目前的矩陣 (查看 [**glMatrixMode**](glmatrixmode.md)) 乘以此平移矩陣，並將產品取代為目前的矩陣。</span><span class="sxs-lookup"><span data-stu-id="43bf1-120">The current matrix (see [**glMatrixMode**](glmatrixmode.md)) is multiplied by this translation matrix, with the product replacing the current matrix.</span></span> <span data-ttu-id="43bf1-121">也就是說，如果 M 是目前的矩陣，而 T 是轉譯矩陣，則 M 會取代為 M T。</span><span class="sxs-lookup"><span data-stu-id="43bf1-121">That is, if M is the current matrix and T is the translation matrix, then M is replaced with M T.</span></span>

<span data-ttu-id="43bf1-122">如果矩陣模式是 GL \_ 模型或 gl \_ 投射，則會轉譯 **glTranslatef** 之後繪製的所有物件。</span><span class="sxs-lookup"><span data-stu-id="43bf1-122">If the matrix mode is either GL\_MODELVIEW or GL\_PROJECTION, all objects drawn after **glTranslatef** is called are translated.</span></span> <span data-ttu-id="43bf1-123">使用 [**glPushMatrix**](glpushmatrix.md) 和 **glPopMatrix** 來儲存及還原未轉譯的座標系統。</span><span class="sxs-lookup"><span data-stu-id="43bf1-123">Use [**glPushMatrix**](glpushmatrix.md) and **glPopMatrix** to save and restore the untranslated coordinate system.</span></span>

<span data-ttu-id="43bf1-124">下列函式會取出 [**glTranslated**](gltranslate.md) 和 **glTranslatef** 的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="43bf1-124">The following functions retrieve information related to [**glTranslated**](gltranslate.md) and **glTranslatef**:</span></span>

<span data-ttu-id="43bf1-125">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 矩陣 \_ 模式的 glGet</span><span class="sxs-lookup"><span data-stu-id="43bf1-125">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="43bf1-126">具有引數 GL \_ 模型 \_ 矩陣的 glGet</span><span class="sxs-lookup"><span data-stu-id="43bf1-126">**glGet** with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="43bf1-127">具有引數 GL \_ 投射 \_ 矩陣的 glGet</span><span class="sxs-lookup"><span data-stu-id="43bf1-127">**glGet** with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="43bf1-128">具有引數 GL \_ 材質 \_ 矩陣的 glGet</span><span class="sxs-lookup"><span data-stu-id="43bf1-128">**glGet** with argument GL\_TEXTURE\_MATRIX</span></span>

## <a name="requirements"></a><span data-ttu-id="43bf1-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="43bf1-129">Requirements</span></span>



| <span data-ttu-id="43bf1-130">需求</span><span class="sxs-lookup"><span data-stu-id="43bf1-130">Requirement</span></span> | <span data-ttu-id="43bf1-131">值</span><span class="sxs-lookup"><span data-stu-id="43bf1-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="43bf1-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="43bf1-132">Minimum supported client</span></span><br/> | <span data-ttu-id="43bf1-133">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="43bf1-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="43bf1-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="43bf1-134">Minimum supported server</span></span><br/> | <span data-ttu-id="43bf1-135">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="43bf1-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="43bf1-136">標頭</span><span class="sxs-lookup"><span data-stu-id="43bf1-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="43bf1-137"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="43bf1-137"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="43bf1-138">程式庫</span><span class="sxs-lookup"><span data-stu-id="43bf1-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="43bf1-139"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="43bf1-139"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="43bf1-140">DLL</span><span class="sxs-lookup"><span data-stu-id="43bf1-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43bf1-141"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43bf1-141"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43bf1-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="43bf1-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43bf1-143">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="43bf1-143">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="43bf1-144">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="43bf1-144">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="43bf1-145">**glMatrixMode**</span><span class="sxs-lookup"><span data-stu-id="43bf1-145">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="43bf1-146">**glMultMatrix**</span><span class="sxs-lookup"><span data-stu-id="43bf1-146">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="43bf1-147">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="43bf1-147">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> <dt>

[<span data-ttu-id="43bf1-148">**glRotate**</span><span class="sxs-lookup"><span data-stu-id="43bf1-148">**glRotate**</span></span>](glrotate.md)
</dt> <dt>

[<span data-ttu-id="43bf1-149">**glScale**</span><span class="sxs-lookup"><span data-stu-id="43bf1-149">**glScale**</span></span>](glscale.md)
</dt> </dl>

 

 





