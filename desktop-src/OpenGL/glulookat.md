---
title: 'gluLookAt 函式 (X.glu 隊) '
description: GluLookAt 函式會定義「查看」轉換。
ms.assetid: 1fd87701-19c2-49b9-99ac-10e70aaedbfd
keywords:
- gluLookAt 函式 OpenGL
topic_type:
- apiref
api_name:
- gluLookAt
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5866f3c06ef6969c95eeef4b23fff7a4e7852eb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844387"
---
# <a name="glulookat-function"></a><span data-ttu-id="1cd7b-104">gluLookAt 函式</span><span class="sxs-lookup"><span data-stu-id="1cd7b-104">gluLookAt function</span></span>

<span data-ttu-id="1cd7b-105">**GluLookAt** 函式會定義「查看」轉換。</span><span class="sxs-lookup"><span data-stu-id="1cd7b-105">The **gluLookAt** function defines a viewing transformation.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cd7b-106">語法</span><span class="sxs-lookup"><span data-stu-id="1cd7b-106">Syntax</span></span>


```C++
void WINAPI gluLookAt(
   GLdouble eyex,
   GLdouble eyey,
   GLdouble eyez,
   GLdouble centerx,
   GLdouble centery,
   GLdouble centerz,
   GLdouble upx,
   GLdouble upy,
   GLdouble upz
);
```



## <a name="parameters"></a><span data-ttu-id="1cd7b-107">參數</span><span class="sxs-lookup"><span data-stu-id="1cd7b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cd7b-108">*eyex*</span><span class="sxs-lookup"><span data-stu-id="1cd7b-108">*eyex*</span></span> 
</dt> <dd>

<span data-ttu-id="1cd7b-109">眼睛點的位置。</span><span class="sxs-lookup"><span data-stu-id="1cd7b-109">The position of the eye point.</span></span>

</dd> <dt>

<span data-ttu-id="1cd7b-110">*eyey*</span><span class="sxs-lookup"><span data-stu-id="1cd7b-110">*eyey*</span></span> 
</dt> <dd>

<span data-ttu-id="1cd7b-111">眼睛點的位置。</span><span class="sxs-lookup"><span data-stu-id="1cd7b-111">The position of the eye point.</span></span>

</dd> <dt>

<span data-ttu-id="1cd7b-112">*eyez*</span><span class="sxs-lookup"><span data-stu-id="1cd7b-112">*eyez*</span></span> 
</dt> <dd>

<span data-ttu-id="1cd7b-113">眼睛點的位置。</span><span class="sxs-lookup"><span data-stu-id="1cd7b-113">The position of the eye point.</span></span>

</dd> <dt>

<span data-ttu-id="1cd7b-114">*system.windows.media.rotatetransform.centerx*</span><span class="sxs-lookup"><span data-stu-id="1cd7b-114">*centerx*</span></span> 
</dt> <dd>

<span data-ttu-id="1cd7b-115">參考點的位置。</span><span class="sxs-lookup"><span data-stu-id="1cd7b-115">The position of the reference point.</span></span>

</dd> <dt>

<span data-ttu-id="1cd7b-116">*centery*</span><span class="sxs-lookup"><span data-stu-id="1cd7b-116">*centery*</span></span> 
</dt> <dd>

<span data-ttu-id="1cd7b-117">參考點的位置。</span><span class="sxs-lookup"><span data-stu-id="1cd7b-117">The position of the reference point.</span></span>

</dd> <dt>

<span data-ttu-id="1cd7b-118">*centerz*</span><span class="sxs-lookup"><span data-stu-id="1cd7b-118">*centerz*</span></span> 
</dt> <dd>

<span data-ttu-id="1cd7b-119">參考點的位置。</span><span class="sxs-lookup"><span data-stu-id="1cd7b-119">The position of the reference point.</span></span>

</dd> <dt>

<span data-ttu-id="1cd7b-120">*upx*</span><span class="sxs-lookup"><span data-stu-id="1cd7b-120">*upx*</span></span> 
</dt> <dd>

<span data-ttu-id="1cd7b-121">向上向量的方向。</span><span class="sxs-lookup"><span data-stu-id="1cd7b-121">The direction of the up vector.</span></span>

</dd> <dt>

<span data-ttu-id="1cd7b-122">*upy*</span><span class="sxs-lookup"><span data-stu-id="1cd7b-122">*upy*</span></span> 
</dt> <dd>

<span data-ttu-id="1cd7b-123">向上向量的方向。</span><span class="sxs-lookup"><span data-stu-id="1cd7b-123">The direction of the up vector.</span></span>

</dd> <dt>

<span data-ttu-id="1cd7b-124">*upz*</span><span class="sxs-lookup"><span data-stu-id="1cd7b-124">*upz*</span></span> 
</dt> <dd>

<span data-ttu-id="1cd7b-125">向上向量的方向。</span><span class="sxs-lookup"><span data-stu-id="1cd7b-125">The direction of the up vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cd7b-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="1cd7b-126">Return value</span></span>

<span data-ttu-id="1cd7b-127">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="1cd7b-127">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1cd7b-128">備註</span><span class="sxs-lookup"><span data-stu-id="1cd7b-128">Remarks</span></span>

<span data-ttu-id="1cd7b-129">**GluLookAt** 函式會建立衍生自眼睛點的視圖矩陣、指出場景中心的參考點，以及向上向量。</span><span class="sxs-lookup"><span data-stu-id="1cd7b-129">The **gluLookAt** function creates a viewing matrix derived from an eye point, a reference point indicating the center of the scene, and an up vector.</span></span> <span data-ttu-id="1cd7b-130">矩陣會將參考點對應至負 Z 軸，並將眼睛點對應至原點，如此當您使用一般投射矩陣時，場景的中心就會對應到此區的中心。</span><span class="sxs-lookup"><span data-stu-id="1cd7b-130">The matrix maps the reference point to the negative z-axis and the eye point to the origin, so that when you use a typical projection matrix, the center of the scene maps to the center of the viewport.</span></span> <span data-ttu-id="1cd7b-131">同樣地，上傳至「觀看」平面的向上向量所描述的方向，會對應至正 y 軸，使其在視口中向上指向。</span><span class="sxs-lookup"><span data-stu-id="1cd7b-131">Similarly, the direction described by the up vector projected onto the viewing plane is mapped to the positive y-axis so that it points upward in the viewport.</span></span> <span data-ttu-id="1cd7b-132">向上向量不能平行至從眼睛到參考點的可見線。</span><span class="sxs-lookup"><span data-stu-id="1cd7b-132">The up vector must not be parallel to the line of sight from the eye to the reference point.</span></span>

<span data-ttu-id="1cd7b-133">**GluLookAt** 所產生的矩陣會 postmultiplies 目前的矩陣。</span><span class="sxs-lookup"><span data-stu-id="1cd7b-133">The matrix generated by **gluLookAt** postmultiplies the current matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="1cd7b-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="1cd7b-134">Requirements</span></span>



| <span data-ttu-id="1cd7b-135">需求</span><span class="sxs-lookup"><span data-stu-id="1cd7b-135">Requirement</span></span> | <span data-ttu-id="1cd7b-136">值</span><span class="sxs-lookup"><span data-stu-id="1cd7b-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1cd7b-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1cd7b-137">Minimum supported client</span></span><br/> | <span data-ttu-id="1cd7b-138">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1cd7b-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="1cd7b-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1cd7b-139">Minimum supported server</span></span><br/> | <span data-ttu-id="1cd7b-140">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1cd7b-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="1cd7b-141">標頭</span><span class="sxs-lookup"><span data-stu-id="1cd7b-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="1cd7b-142"><dt>X.glu 隊。h</dt></span><span class="sxs-lookup"><span data-stu-id="1cd7b-142"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="1cd7b-143">程式庫</span><span class="sxs-lookup"><span data-stu-id="1cd7b-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="1cd7b-144"><dt>Glu32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="1cd7b-144"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="1cd7b-145">DLL</span><span class="sxs-lookup"><span data-stu-id="1cd7b-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1cd7b-146"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1cd7b-146"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1cd7b-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1cd7b-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cd7b-148">**glFrustum**</span><span class="sxs-lookup"><span data-stu-id="1cd7b-148">**glFrustum**</span></span>](glfrustum.md)
</dt> <dt>

[<span data-ttu-id="1cd7b-149">**gluPerspective**</span><span class="sxs-lookup"><span data-stu-id="1cd7b-149">**gluPerspective**</span></span>](gluperspective.md)
</dt> </dl>

 

 





