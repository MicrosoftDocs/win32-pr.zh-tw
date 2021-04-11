---
title: 'gluQuadricDrawStyle 函式 (X.glu 隊) '
description: GluQuadricDrawStyle 函式會指定 quadrics 所需的繪製樣式。
ms.assetid: 30f6da40-9306-46bb-a815-f51722e57e18
keywords:
- gluQuadricDrawStyle 函式 OpenGL
topic_type:
- apiref
api_name:
- gluQuadricDrawStyle
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8a1b44b7894ea9762b450c5a5d6c2b022c5e02f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934757"
---
# <a name="gluquadricdrawstyle-function"></a><span data-ttu-id="cc294-104">gluQuadricDrawStyle 函式</span><span class="sxs-lookup"><span data-stu-id="cc294-104">gluQuadricDrawStyle function</span></span>

<span data-ttu-id="cc294-105">**GluQuadricDrawStyle** 函式會指定 quadrics 所需的繪製樣式。</span><span class="sxs-lookup"><span data-stu-id="cc294-105">The **gluQuadricDrawStyle** function specifies the draw style desired for quadrics.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc294-106">語法</span><span class="sxs-lookup"><span data-stu-id="cc294-106">Syntax</span></span>


```C++
void WINAPI gluQuadricDrawStyle(
   GLUquadric *quadObject,
   GLenum     drawStyle
);
```



## <a name="parameters"></a><span data-ttu-id="cc294-107">參數</span><span class="sxs-lookup"><span data-stu-id="cc294-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc294-108">*quadObject*</span><span class="sxs-lookup"><span data-stu-id="cc294-108">*quadObject*</span></span> 
</dt> <dd>

<span data-ttu-id="cc294-109">Quadric 物件 (使用 [**gluNewQuadric**](glunewquadric.md)) 建立。</span><span class="sxs-lookup"><span data-stu-id="cc294-109">The quadric object (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> <dt>

<span data-ttu-id="cc294-110">*drawStyle*</span><span class="sxs-lookup"><span data-stu-id="cc294-110">*drawStyle*</span></span> 
</dt> <dd>

<span data-ttu-id="cc294-111">所需的繪製樣式。</span><span class="sxs-lookup"><span data-stu-id="cc294-111">The desired draw style.</span></span> <span data-ttu-id="cc294-112">下列是有效的值。</span><span class="sxs-lookup"><span data-stu-id="cc294-112">The following values are valid.</span></span>



| <span data-ttu-id="cc294-113">值</span><span class="sxs-lookup"><span data-stu-id="cc294-113">Value</span></span>                                                                                                                                                            | <span data-ttu-id="cc294-114">意義</span><span class="sxs-lookup"><span data-stu-id="cc294-114">Meaning</span></span>                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_FILL"></span><span id="glu_fill"></span><dl> <span data-ttu-id="cc294-115"><dt>**X.GLU 隊 \_ 填滿**</dt></span><span class="sxs-lookup"><span data-stu-id="cc294-115"><dt>**GLU\_FILL**</dt></span></span> </dl>                   | <span data-ttu-id="cc294-116">Quadrics 是以多邊形基本專案轉譯。</span><span class="sxs-lookup"><span data-stu-id="cc294-116">Quadrics are rendered with polygon primitives.</span></span> <span data-ttu-id="cc294-117">多邊形是以逆時針方式繪製，與 [**gluQuadricOrientation**](gluquadricorientation.md)) 所定義的法線 (有關。</span><span class="sxs-lookup"><span data-stu-id="cc294-117">The polygons are drawn in a counterclockwise fashion with respect to their normals (as defined with [**gluQuadricOrientation**](gluquadricorientation.md)).</span></span><br/> |
| <span id="GLU_LINE"></span><span id="glu_line"></span><dl> <span data-ttu-id="cc294-118"><dt>**X.GLU 隊 \_ 行**</dt></span><span class="sxs-lookup"><span data-stu-id="cc294-118"><dt>**GLU\_LINE**</dt></span></span> </dl>                   | <span data-ttu-id="cc294-119">Quadrics 會轉譯為一組線。</span><span class="sxs-lookup"><span data-stu-id="cc294-119">Quadrics are rendered as a set of lines.</span></span><br/>                                                                                                                                                                    |
| <span id="GLU_SILHOUETTE"></span><span id="glu_silhouette"></span><dl> <span data-ttu-id="cc294-120"><dt>**X.GLU 隊 \_ 側面**</dt></span><span class="sxs-lookup"><span data-stu-id="cc294-120"><dt>**GLU\_SILHOUETTE**</dt></span></span> </dl> | <span data-ttu-id="cc294-121">Quadrics 會轉譯為一組線，不同之處在于不會繪製分隔共面的臉部的邊緣。</span><span class="sxs-lookup"><span data-stu-id="cc294-121">Quadrics are rendered as a set of lines, except that edges separating coplanar faces will not be drawn.</span></span><br/>                                                                                                     |
| <span id="GLU_POINT"></span><span id="glu_point"></span><dl> <span data-ttu-id="cc294-122"><dt>**X.GLU 隊 \_ 點**</dt></span><span class="sxs-lookup"><span data-stu-id="cc294-122"><dt>**GLU\_POINT**</dt></span></span> </dl>                | <span data-ttu-id="cc294-123">Quadrics 會轉譯為一組點。</span><span class="sxs-lookup"><span data-stu-id="cc294-123">Quadrics are rendered as a set of points.</span></span><br/>                                                                                                                                                                   |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc294-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="cc294-124">Return value</span></span>

<span data-ttu-id="cc294-125">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="cc294-125">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc294-126">備註</span><span class="sxs-lookup"><span data-stu-id="cc294-126">Remarks</span></span>

<span data-ttu-id="cc294-127">**GluQuadricDrawStyle** 函式會指定使用 **quadObject** 轉譯之 quadrics 的繪製樣式。</span><span class="sxs-lookup"><span data-stu-id="cc294-127">The **gluQuadricDrawStyle** function specifies the draw style for quadrics rendered with **quadObject**.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc294-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="cc294-128">Requirements</span></span>



| <span data-ttu-id="cc294-129">需求</span><span class="sxs-lookup"><span data-stu-id="cc294-129">Requirement</span></span> | <span data-ttu-id="cc294-130">值</span><span class="sxs-lookup"><span data-stu-id="cc294-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cc294-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cc294-131">Minimum supported client</span></span><br/> | <span data-ttu-id="cc294-132">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cc294-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="cc294-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cc294-133">Minimum supported server</span></span><br/> | <span data-ttu-id="cc294-134">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cc294-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="cc294-135">標頭</span><span class="sxs-lookup"><span data-stu-id="cc294-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc294-136"><dt>X.glu 隊。h</dt></span><span class="sxs-lookup"><span data-stu-id="cc294-136"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="cc294-137">程式庫</span><span class="sxs-lookup"><span data-stu-id="cc294-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="cc294-138"><dt>Glu32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="cc294-138"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="cc294-139">DLL</span><span class="sxs-lookup"><span data-stu-id="cc294-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cc294-140"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc294-140"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc294-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cc294-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc294-142">**gluNewQuadric**</span><span class="sxs-lookup"><span data-stu-id="cc294-142">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> <dt>

[<span data-ttu-id="cc294-143">**gluQuadricNormals**</span><span class="sxs-lookup"><span data-stu-id="cc294-143">**gluQuadricNormals**</span></span>](gluquadricnormals.md)
</dt> <dt>

[<span data-ttu-id="cc294-144">**gluQuadricOrientation**</span><span class="sxs-lookup"><span data-stu-id="cc294-144">**gluQuadricOrientation**</span></span>](gluquadricorientation.md)
</dt> <dt>

[<span data-ttu-id="cc294-145">**gluQuadricTexture**</span><span class="sxs-lookup"><span data-stu-id="cc294-145">**gluQuadricTexture**</span></span>](gluquadrictexture.md)
</dt> </dl>

 

 





