---
title: 'gluQuadricTexture 函式 (X.glu 隊) '
description: GluQuadricTexture 函數會指定是否要將 quadrics 設為紋理。
ms.assetid: 11681497-f099-4856-a0ac-6a44abd3e1a1
keywords:
- gluQuadricTexture 函式 OpenGL
topic_type:
- apiref
api_name:
- gluQuadricTexture
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cc395564b6c6f30f38a8c5129c489d0bfca6b80
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104928"
---
# <a name="gluquadrictexture-function"></a><span data-ttu-id="64b54-104">gluQuadricTexture 函式</span><span class="sxs-lookup"><span data-stu-id="64b54-104">gluQuadricTexture function</span></span>

<span data-ttu-id="64b54-105">**GluQuadricTexture** 函數會指定是否要將 quadrics 設為紋理。</span><span class="sxs-lookup"><span data-stu-id="64b54-105">The **gluQuadricTexture** function specifies whether quadrics are to be textured.</span></span>

## <a name="syntax"></a><span data-ttu-id="64b54-106">語法</span><span class="sxs-lookup"><span data-stu-id="64b54-106">Syntax</span></span>


```C++
void WINAPI gluQuadricTexture(
   GLUquadric *quadObject,
   GLboolean  textureCoords
);
```



## <a name="parameters"></a><span data-ttu-id="64b54-107">參數</span><span class="sxs-lookup"><span data-stu-id="64b54-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64b54-108">*quadObject*</span><span class="sxs-lookup"><span data-stu-id="64b54-108">*quadObject*</span></span> 
</dt> <dd>

<span data-ttu-id="64b54-109">Quadric 物件 (使用 [**gluNewQuadric**](glunewquadric.md)) 建立。</span><span class="sxs-lookup"><span data-stu-id="64b54-109">The quadric object (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> <dt>

<span data-ttu-id="64b54-110">*textureCoords*</span><span class="sxs-lookup"><span data-stu-id="64b54-110">*textureCoords*</span></span> 
</dt> <dd>

<span data-ttu-id="64b54-111">指出是否要產生紋理座標的旗標。</span><span class="sxs-lookup"><span data-stu-id="64b54-111">A flag indicating whether texture coordinates are to be generated.</span></span> <span data-ttu-id="64b54-112">下列是有效的值。</span><span class="sxs-lookup"><span data-stu-id="64b54-112">The following values are valid.</span></span>



| <span data-ttu-id="64b54-113">值</span><span class="sxs-lookup"><span data-stu-id="64b54-113">Value</span></span>                                                                                                                                          | <span data-ttu-id="64b54-114">意義</span><span class="sxs-lookup"><span data-stu-id="64b54-114">Meaning</span></span>                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="GL_TRUE"></span><span id="gl_true"></span><dl> <span data-ttu-id="64b54-115"><dt>**GL \_ TRUE**</dt></span><span class="sxs-lookup"><span data-stu-id="64b54-115"><dt>**GL\_TRUE**</dt></span></span> </dl>    | <span data-ttu-id="64b54-116">產生材質座標。</span><span class="sxs-lookup"><span data-stu-id="64b54-116">Generate texture coordinates.</span></span><br/>                                   |
| <span id="GL_FALSE"></span><span id="gl_false"></span><dl> <span data-ttu-id="64b54-117"><dt>**GL \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="64b54-117"><dt>**GL\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="64b54-118">不要產生材質座標。</span><span class="sxs-lookup"><span data-stu-id="64b54-118">Do not generate texture coordinates.</span></span> <span data-ttu-id="64b54-119">這是預設值。</span><span class="sxs-lookup"><span data-stu-id="64b54-119">This is the default value.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64b54-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="64b54-120">Return value</span></span>

<span data-ttu-id="64b54-121">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="64b54-121">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="64b54-122">備註</span><span class="sxs-lookup"><span data-stu-id="64b54-122">Remarks</span></span>

<span data-ttu-id="64b54-123">**GluQuadricTexture** 函式會指定是否要針對以 **quadObject** 轉譯的 quadrics 產生材質座標。</span><span class="sxs-lookup"><span data-stu-id="64b54-123">The **gluQuadricTexture** function specifies whether texture coordinates are to be generated for quadrics rendered with **quadObject**.</span></span>

<span data-ttu-id="64b54-124">材質座標產生的方式取決於轉譯的特定 quadric。</span><span class="sxs-lookup"><span data-stu-id="64b54-124">The manner in which texture coordinates are generated depends upon the specific quadric rendered.</span></span>

## <a name="requirements"></a><span data-ttu-id="64b54-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="64b54-125">Requirements</span></span>



| <span data-ttu-id="64b54-126">需求</span><span class="sxs-lookup"><span data-stu-id="64b54-126">Requirement</span></span> | <span data-ttu-id="64b54-127">值</span><span class="sxs-lookup"><span data-stu-id="64b54-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="64b54-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="64b54-128">Minimum supported client</span></span><br/> | <span data-ttu-id="64b54-129">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="64b54-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="64b54-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="64b54-130">Minimum supported server</span></span><br/> | <span data-ttu-id="64b54-131">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="64b54-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="64b54-132">標頭</span><span class="sxs-lookup"><span data-stu-id="64b54-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="64b54-133"><dt>X.glu 隊。h</dt></span><span class="sxs-lookup"><span data-stu-id="64b54-133"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="64b54-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="64b54-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="64b54-135"><dt>Glu32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="64b54-135"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="64b54-136">DLL</span><span class="sxs-lookup"><span data-stu-id="64b54-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64b54-137"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="64b54-137"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64b54-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="64b54-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64b54-139">**gluNewQuadric**</span><span class="sxs-lookup"><span data-stu-id="64b54-139">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> <dt>

[<span data-ttu-id="64b54-140">**gluQuadricDrawStyle**</span><span class="sxs-lookup"><span data-stu-id="64b54-140">**gluQuadricDrawStyle**</span></span>](gluquadricdrawstyle.md)
</dt> <dt>

[<span data-ttu-id="64b54-141">**gluQuadricNormals**</span><span class="sxs-lookup"><span data-stu-id="64b54-141">**gluQuadricNormals**</span></span>](gluquadricnormals.md)
</dt> </dl>

 

 





