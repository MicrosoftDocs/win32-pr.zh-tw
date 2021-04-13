---
title: 'gluQuadricNormals 函式 (X.glu 隊) '
description: GluQuadricNormals 函式會指定要針對 quadrics 使用何種法線。
ms.assetid: 945759ec-ed4a-480f-8243-49fc785867c1
keywords:
- gluQuadricNormals 函式 OpenGL
topic_type:
- apiref
api_name:
- gluQuadricNormals
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f11f9d8cd1884d7a5d1bc4cd03797517ba484126
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466176"
---
# <a name="gluquadricnormals-function"></a><span data-ttu-id="10135-104">gluQuadricNormals 函式</span><span class="sxs-lookup"><span data-stu-id="10135-104">gluQuadricNormals function</span></span>

<span data-ttu-id="10135-105">**GluQuadricNormals** 函式會指定要針對 quadrics 使用何種法線。</span><span class="sxs-lookup"><span data-stu-id="10135-105">The **gluQuadricNormals** function specifies what kind of normals are to be used for quadrics.</span></span>

## <a name="syntax"></a><span data-ttu-id="10135-106">語法</span><span class="sxs-lookup"><span data-stu-id="10135-106">Syntax</span></span>


```C++
void WINAPI gluQuadricNormals(
   GLUquadric *quadObject,
   GLenum     normals
);
```



## <a name="parameters"></a><span data-ttu-id="10135-107">參數</span><span class="sxs-lookup"><span data-stu-id="10135-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10135-108">*quadObject*</span><span class="sxs-lookup"><span data-stu-id="10135-108">*quadObject*</span></span> 
</dt> <dd>

<span data-ttu-id="10135-109">Quadric 物件 (使用 [**gluNewQuadric**](glunewquadric.md)) 建立。</span><span class="sxs-lookup"><span data-stu-id="10135-109">The quadric object (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> <dt>

<span data-ttu-id="10135-110">*法線*</span><span class="sxs-lookup"><span data-stu-id="10135-110">*normals*</span></span> 
</dt> <dd>

<span data-ttu-id="10135-111">所需的法線類型。</span><span class="sxs-lookup"><span data-stu-id="10135-111">The desired type of normals.</span></span> <span data-ttu-id="10135-112">下列是有效的值。</span><span class="sxs-lookup"><span data-stu-id="10135-112">The following values are valid.</span></span>



| <span data-ttu-id="10135-113">值</span><span class="sxs-lookup"><span data-stu-id="10135-113">Value</span></span>                                                                                                                                                | <span data-ttu-id="10135-114">意義</span><span class="sxs-lookup"><span data-stu-id="10135-114">Meaning</span></span>                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="GLU_NONE"></span><span id="glu_none"></span><dl> <span data-ttu-id="10135-115"><dt>**X.GLU 隊 \_ 無**</dt></span><span class="sxs-lookup"><span data-stu-id="10135-115"><dt>**GLU\_NONE**</dt></span></span> </dl>       | <span data-ttu-id="10135-116">不會產生任何法線。</span><span class="sxs-lookup"><span data-stu-id="10135-116">No normals are generated.</span></span><br/>                                                         |
| <span id="GLU_FLAT"></span><span id="glu_flat"></span><dl> <span data-ttu-id="10135-117"><dt>**X.GLU 隊 \_ 平面**</dt></span><span class="sxs-lookup"><span data-stu-id="10135-117"><dt>**GLU\_FLAT**</dt></span></span> </dl>       | <span data-ttu-id="10135-118">Quadric 的每個 facet 都會產生一個正常情況。</span><span class="sxs-lookup"><span data-stu-id="10135-118">One normal is generated for every facet of a quadric.</span></span><br/>                             |
| <span id="GLU_SMOOTH"></span><span id="glu_smooth"></span><dl> <span data-ttu-id="10135-119"><dt>**X.GLU 隊 \_ 順暢**</dt></span><span class="sxs-lookup"><span data-stu-id="10135-119"><dt>**GLU\_SMOOTH**</dt></span></span> </dl> | <span data-ttu-id="10135-120">Quadric 的每個頂點都會產生一個正常情況。</span><span class="sxs-lookup"><span data-stu-id="10135-120">One normal is generated for every vertex of a quadric.</span></span> <span data-ttu-id="10135-121">這是預設值。</span><span class="sxs-lookup"><span data-stu-id="10135-121">This is the default value.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10135-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="10135-122">Return value</span></span>

<span data-ttu-id="10135-123">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="10135-123">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="10135-124">備註</span><span class="sxs-lookup"><span data-stu-id="10135-124">Remarks</span></span>

<span data-ttu-id="10135-125">**GluQuadricNormals** 函式會指定要針對以 **quadObject** 轉譯的 quadrics 使用何種法線。</span><span class="sxs-lookup"><span data-stu-id="10135-125">The **gluQuadricNormals** function specifies what kind of normals are to be used for quadrics rendered with **quadObject**.</span></span>

## <a name="requirements"></a><span data-ttu-id="10135-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="10135-126">Requirements</span></span>



| <span data-ttu-id="10135-127">需求</span><span class="sxs-lookup"><span data-stu-id="10135-127">Requirement</span></span> | <span data-ttu-id="10135-128">值</span><span class="sxs-lookup"><span data-stu-id="10135-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="10135-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="10135-129">Minimum supported client</span></span><br/> | <span data-ttu-id="10135-130">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="10135-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="10135-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="10135-131">Minimum supported server</span></span><br/> | <span data-ttu-id="10135-132">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="10135-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="10135-133">標頭</span><span class="sxs-lookup"><span data-stu-id="10135-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="10135-134"><dt>X.glu 隊。h</dt></span><span class="sxs-lookup"><span data-stu-id="10135-134"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="10135-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="10135-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="10135-136"><dt>Glu32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="10135-136"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="10135-137">DLL</span><span class="sxs-lookup"><span data-stu-id="10135-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10135-138"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10135-138"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10135-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="10135-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10135-140">**gluNewQuadric**</span><span class="sxs-lookup"><span data-stu-id="10135-140">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> <dt>

[<span data-ttu-id="10135-141">**gluQuadricDrawStyle**</span><span class="sxs-lookup"><span data-stu-id="10135-141">**gluQuadricDrawStyle**</span></span>](gluquadricdrawstyle.md)
</dt> <dt>

[<span data-ttu-id="10135-142">**gluQuadricOrientation**</span><span class="sxs-lookup"><span data-stu-id="10135-142">**gluQuadricOrientation**</span></span>](gluquadricorientation.md)
</dt> <dt>

[<span data-ttu-id="10135-143">**gluQuadricTexture**</span><span class="sxs-lookup"><span data-stu-id="10135-143">**gluQuadricTexture**</span></span>](gluquadrictexture.md)
</dt> </dl>

 

 





