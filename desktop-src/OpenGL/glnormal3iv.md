---
title: 'glNormal3iv 函式 (Gl) '
description: '設定目前的一般向量。 |glNormal3iv 函式 (Gl) '
ms.assetid: cf50e801-a34c-43bd-b7eb-facb84a6472d
keywords:
- glNormal3iv 函式 OpenGL
topic_type:
- apiref
api_name:
- glNormal3iv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5629a12d6c388da2aa133fbe72177646b4f95d63
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103946010"
---
# <a name="glnormal3iv-function"></a><span data-ttu-id="f5232-105">glNormal3iv 函式</span><span class="sxs-lookup"><span data-stu-id="f5232-105">glNormal3iv function</span></span>

<span data-ttu-id="f5232-106">設定目前的一般向量。</span><span class="sxs-lookup"><span data-stu-id="f5232-106">Sets the current normal vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5232-107">語法</span><span class="sxs-lookup"><span data-stu-id="f5232-107">Syntax</span></span>


```C++
void WINAPI glNormal3iv(
   const GLint *v
);
```



## <a name="parameters"></a><span data-ttu-id="f5232-108">參數</span><span class="sxs-lookup"><span data-stu-id="f5232-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5232-109">*V*</span><span class="sxs-lookup"><span data-stu-id="f5232-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="f5232-110">三個元素的陣列指標：新的目前一般標準的 x、y 和 z 座標。</span><span class="sxs-lookup"><span data-stu-id="f5232-110">A pointer to an array of three elements: the x, y, and z coordinates of the new current normal.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5232-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="f5232-111">Return value</span></span>

<span data-ttu-id="f5232-112">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="f5232-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5232-113">備註</span><span class="sxs-lookup"><span data-stu-id="f5232-113">Remarks</span></span>

<span data-ttu-id="f5232-114">當您呼叫 **glNormal3iv** 函式時，目前的一般會設定為指定的座標。</span><span class="sxs-lookup"><span data-stu-id="f5232-114">The current normal is set to the given coordinates whenever you call the **glNormal3iv** function.</span></span>

<span data-ttu-id="f5232-115">Byte、short 或 integer 引數會轉換成浮點數格式，其具有將最正面可表示的整數值對應至1.0 的線性對應，以及最大的負向-1.0 的可表示整數值。</span><span class="sxs-lookup"><span data-stu-id="f5232-115">Byte, short, or integer arguments are converted to floating-point format with a linear mapping that maps the most positive representable integer value to 1.0, and the most negative representable integer value to -1.0.</span></span>

<span data-ttu-id="f5232-116">使用 **glNormal3iv** 指定的法線不需要單位長度。</span><span class="sxs-lookup"><span data-stu-id="f5232-116">Normals specified by using **glNormal3iv** need not have unit length.</span></span> <span data-ttu-id="f5232-117">如果啟用正規化，則在轉換之後會正規化以 **glNormal3iv** 指定的法線。</span><span class="sxs-lookup"><span data-stu-id="f5232-117">If normalization is enabled, then normals specified with **glNormal3iv** are normalized after transformation.</span></span> <span data-ttu-id="f5232-118">您可以使用 [**glEnable**](glenable.md) 和 [**glDisable**](gldisable.md) 搭配引數 GL 標準化來控制正規化 \_ 。</span><span class="sxs-lookup"><span data-stu-id="f5232-118">You can control normalization by using [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) with the argument GL\_NORMALIZE.</span></span> <span data-ttu-id="f5232-119">預設會停用正規化。</span><span class="sxs-lookup"><span data-stu-id="f5232-119">By default, normalization is disabled.</span></span> <span data-ttu-id="f5232-120">您可以隨時更新目前的正常情況。</span><span class="sxs-lookup"><span data-stu-id="f5232-120">You can update the current normal at any time.</span></span> <span data-ttu-id="f5232-121">尤其是，您可以呼叫 [**glBegin**](glbegin.md)的呼叫與 [**glEnd**](glend.md)的對應呼叫之間的 **glNormal3iv**。</span><span class="sxs-lookup"><span data-stu-id="f5232-121">In particular, you can call **glNormal3iv** between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="f5232-122">下列函式會取出與 **glNormal3iv** 相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="f5232-122">The following functions retrieve information related to **glNormal3iv**:</span></span>

<span data-ttu-id="f5232-123">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 目前 \_ 標準的 glGet</span><span class="sxs-lookup"><span data-stu-id="f5232-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_NORMAL</span></span>

<span data-ttu-id="f5232-124">具有引數 GL 正規化的 [**glIsEnable**](glisenabled.md) \_</span><span class="sxs-lookup"><span data-stu-id="f5232-124">[**glIsEnable**](glisenabled.md) with argument GL\_NORMALIZE</span></span>

## <a name="requirements"></a><span data-ttu-id="f5232-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="f5232-125">Requirements</span></span>



| <span data-ttu-id="f5232-126">需求</span><span class="sxs-lookup"><span data-stu-id="f5232-126">Requirement</span></span> | <span data-ttu-id="f5232-127">值</span><span class="sxs-lookup"><span data-stu-id="f5232-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5232-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f5232-128">Minimum supported client</span></span><br/> | <span data-ttu-id="f5232-129">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f5232-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f5232-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f5232-130">Minimum supported server</span></span><br/> | <span data-ttu-id="f5232-131">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f5232-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f5232-132">標頭</span><span class="sxs-lookup"><span data-stu-id="f5232-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5232-133"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="f5232-133"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="f5232-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="f5232-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="f5232-135"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f5232-135"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="f5232-136">DLL</span><span class="sxs-lookup"><span data-stu-id="f5232-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5232-137"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5232-137"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5232-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f5232-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5232-139">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="f5232-139">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="f5232-140">**glColor**</span><span class="sxs-lookup"><span data-stu-id="f5232-140">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="f5232-141">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="f5232-141">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="f5232-142">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="f5232-142">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="f5232-143">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="f5232-143">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="f5232-144">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="f5232-144">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





