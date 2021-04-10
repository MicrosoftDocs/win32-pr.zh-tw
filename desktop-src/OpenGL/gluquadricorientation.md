---
title: 'gluQuadricOrientation 函式 (X.glu 隊) '
description: GluQuadricOrientation 函式會針對 quadrics 指定內部或外部方向。
ms.assetid: 4e3fc6d3-5a39-455b-bd24-8eb497333096
keywords:
- gluQuadricOrientation 函式 OpenGL
topic_type:
- apiref
api_name:
- gluQuadricOrientation
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d05ffb1eeff199297943e678783731a26a38092a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685480"
---
# <a name="gluquadricorientation-function"></a><span data-ttu-id="44f8f-104">gluQuadricOrientation 函式</span><span class="sxs-lookup"><span data-stu-id="44f8f-104">gluQuadricOrientation function</span></span>

<span data-ttu-id="44f8f-105">**GluQuadricOrientation** 函式會針對 quadrics 指定內部或外部方向。</span><span class="sxs-lookup"><span data-stu-id="44f8f-105">The **gluQuadricOrientation** function specifies inside or outside orientation for quadrics.</span></span>

## <a name="syntax"></a><span data-ttu-id="44f8f-106">語法</span><span class="sxs-lookup"><span data-stu-id="44f8f-106">Syntax</span></span>


```C++
void WINAPI gluQuadricOrientation(
   GLUquadric *quadObject,
   GLenum     orientation
);
```



## <a name="parameters"></a><span data-ttu-id="44f8f-107">參數</span><span class="sxs-lookup"><span data-stu-id="44f8f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44f8f-108">*quadObject*</span><span class="sxs-lookup"><span data-stu-id="44f8f-108">*quadObject*</span></span> 
</dt> <dd>

<span data-ttu-id="44f8f-109">Quadric 物件 (使用 [**gluNewQuadric**](glunewquadric.md)) 建立。</span><span class="sxs-lookup"><span data-stu-id="44f8f-109">The quadric object (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> <dt>

<span data-ttu-id="44f8f-110">*取向*</span><span class="sxs-lookup"><span data-stu-id="44f8f-110">*orientation*</span></span> 
</dt> <dd>

<span data-ttu-id="44f8f-111">所需的方向。</span><span class="sxs-lookup"><span data-stu-id="44f8f-111">The desired orientation.</span></span> <span data-ttu-id="44f8f-112">下列是有效的值。</span><span class="sxs-lookup"><span data-stu-id="44f8f-112">The following values are valid.</span></span>



| <span data-ttu-id="44f8f-113">值</span><span class="sxs-lookup"><span data-stu-id="44f8f-113">Value</span></span>                                                                                                                                                   | <span data-ttu-id="44f8f-114">意義</span><span class="sxs-lookup"><span data-stu-id="44f8f-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="GLU_OUTSIDE"></span><span id="glu_outside"></span><dl> <span data-ttu-id="44f8f-115"><dt>**\_外部 X.GLU 隊**</dt></span><span class="sxs-lookup"><span data-stu-id="44f8f-115"><dt>**GLU\_OUTSIDE**</dt></span></span> </dl> | <span data-ttu-id="44f8f-116">以指向外的法線繪製 quadrics。</span><span class="sxs-lookup"><span data-stu-id="44f8f-116">Draw quadrics with normals pointing outward.</span></span> <span data-ttu-id="44f8f-117">這是預設值。</span><span class="sxs-lookup"><span data-stu-id="44f8f-117">This is the default value.</span></span><br/> |
| <span id="GLU_INSIDE"></span><span id="glu_inside"></span><dl> <span data-ttu-id="44f8f-118"><dt>**X.GLU 隊 \_ 內部**</dt></span><span class="sxs-lookup"><span data-stu-id="44f8f-118"><dt>**GLU\_INSIDE**</dt></span></span> </dl>    | <span data-ttu-id="44f8f-119">繪製具有朝內 quadrics 的法線。</span><span class="sxs-lookup"><span data-stu-id="44f8f-119">Draw quadrics with normals pointing inward.</span></span><br/>                             |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44f8f-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="44f8f-120">Return value</span></span>

<span data-ttu-id="44f8f-121">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="44f8f-121">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="44f8f-122">備註</span><span class="sxs-lookup"><span data-stu-id="44f8f-122">Remarks</span></span>

<span data-ttu-id="44f8f-123">**GluQuadricOrientation** 函式會指定以 **quadObject** 轉譯 quadrics 所需的方向類型。</span><span class="sxs-lookup"><span data-stu-id="44f8f-123">The **gluQuadricOrientation** function specifies what kind of orientation is desired for quadrics rendered with **quadObject**.</span></span> <span data-ttu-id="44f8f-124">向外和向內的解讀取決於所繪製的 quadric。</span><span class="sxs-lookup"><span data-stu-id="44f8f-124">The interpretation of outward and inward depends on the quadric being drawn.</span></span>

## <a name="requirements"></a><span data-ttu-id="44f8f-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="44f8f-125">Requirements</span></span>



| <span data-ttu-id="44f8f-126">需求</span><span class="sxs-lookup"><span data-stu-id="44f8f-126">Requirement</span></span> | <span data-ttu-id="44f8f-127">值</span><span class="sxs-lookup"><span data-stu-id="44f8f-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="44f8f-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="44f8f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="44f8f-129">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="44f8f-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="44f8f-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="44f8f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="44f8f-131">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="44f8f-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="44f8f-132">標頭</span><span class="sxs-lookup"><span data-stu-id="44f8f-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="44f8f-133"><dt>X.glu 隊。h</dt></span><span class="sxs-lookup"><span data-stu-id="44f8f-133"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="44f8f-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="44f8f-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="44f8f-135"><dt>Glu32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="44f8f-135"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="44f8f-136">DLL</span><span class="sxs-lookup"><span data-stu-id="44f8f-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44f8f-137"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44f8f-137"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44f8f-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="44f8f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44f8f-139">**gluNewQuadric**</span><span class="sxs-lookup"><span data-stu-id="44f8f-139">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> <dt>

[<span data-ttu-id="44f8f-140">**gluQuadricDrawStyle**</span><span class="sxs-lookup"><span data-stu-id="44f8f-140">**gluQuadricDrawStyle**</span></span>](gluquadricdrawstyle.md)
</dt> <dt>

[<span data-ttu-id="44f8f-141">**gluQuadricNormals**</span><span class="sxs-lookup"><span data-stu-id="44f8f-141">**gluQuadricNormals**</span></span>](gluquadricnormals.md)
</dt> <dt>

[<span data-ttu-id="44f8f-142">**gluQuadricTexture**</span><span class="sxs-lookup"><span data-stu-id="44f8f-142">**gluQuadricTexture**</span></span>](gluquadrictexture.md)
</dt> </dl>

 

 





