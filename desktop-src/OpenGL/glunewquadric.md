---
title: 'gluNewQuadric 函式 (X.glu 隊) '
description: GluNewQuadric 函式會建立 quadric 物件。
ms.assetid: 5a4289bf-b57a-4c74-b0e3-b7536671e4df
keywords:
- gluNewQuadric 函式 OpenGL
topic_type:
- apiref
api_name:
- gluNewQuadric
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: affedc7dcebd2b7925449e22cc1b902e88d936f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934604"
---
# <a name="glunewquadric-function"></a><span data-ttu-id="10388-104">gluNewQuadric 函式</span><span class="sxs-lookup"><span data-stu-id="10388-104">gluNewQuadric function</span></span>

<span data-ttu-id="10388-105">**GluNewQuadric** 函式會建立 quadric 物件。</span><span class="sxs-lookup"><span data-stu-id="10388-105">The **gluNewQuadric** function creates a quadric object.</span></span>

## <a name="syntax"></a><span data-ttu-id="10388-106">語法</span><span class="sxs-lookup"><span data-stu-id="10388-106">Syntax</span></span>


```C++
GLUquadric* WINAPI gluNewQuadric(void);
```



## <a name="parameters"></a><span data-ttu-id="10388-107">參數</span><span class="sxs-lookup"><span data-stu-id="10388-107">Parameters</span></span>

<span data-ttu-id="10388-108">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="10388-108">This function has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="10388-109">備註</span><span class="sxs-lookup"><span data-stu-id="10388-109">Remarks</span></span>

<span data-ttu-id="10388-110">**GluNewQuadric** 函式會建立並傳回新 quadric 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="10388-110">The **gluNewQuadric** function creates and returns a pointer to a new quadric object.</span></span> <span data-ttu-id="10388-111">呼叫 quadric 轉譯和控制函式時，請參考這個物件。</span><span class="sxs-lookup"><span data-stu-id="10388-111">Refer to this object when calling quadric rendering and control functions.</span></span> <span data-ttu-id="10388-112">傳回值為0表示沒有足夠的記憶體可配置給物件。</span><span class="sxs-lookup"><span data-stu-id="10388-112">A return value of zero means there is not enough memory to allocate to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="10388-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="10388-113">Requirements</span></span>



| <span data-ttu-id="10388-114">需求</span><span class="sxs-lookup"><span data-stu-id="10388-114">Requirement</span></span> | <span data-ttu-id="10388-115">值</span><span class="sxs-lookup"><span data-stu-id="10388-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="10388-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="10388-116">Minimum supported client</span></span><br/> | <span data-ttu-id="10388-117">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="10388-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="10388-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="10388-118">Minimum supported server</span></span><br/> | <span data-ttu-id="10388-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="10388-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="10388-120">標頭</span><span class="sxs-lookup"><span data-stu-id="10388-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="10388-121"><dt>X.glu 隊。h</dt></span><span class="sxs-lookup"><span data-stu-id="10388-121"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="10388-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="10388-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="10388-123"><dt>Glu32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="10388-123"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="10388-124">DLL</span><span class="sxs-lookup"><span data-stu-id="10388-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10388-125"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10388-125"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10388-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="10388-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10388-127">**gluCylinder**</span><span class="sxs-lookup"><span data-stu-id="10388-127">**gluCylinder**</span></span>](glucylinder.md)
</dt> <dt>

[<span data-ttu-id="10388-128">**gluDeleteQuadric**</span><span class="sxs-lookup"><span data-stu-id="10388-128">**gluDeleteQuadric**</span></span>](gludeletequadric.md)
</dt> <dt>

[<span data-ttu-id="10388-129">**gluDisk**</span><span class="sxs-lookup"><span data-stu-id="10388-129">**gluDisk**</span></span>](gludisk.md)
</dt> <dt>

[<span data-ttu-id="10388-130">**gluPartialDisk**</span><span class="sxs-lookup"><span data-stu-id="10388-130">**gluPartialDisk**</span></span>](glupartialdisk.md)
</dt> <dt>

[<span data-ttu-id="10388-131">*gluQuadricCallback*</span><span class="sxs-lookup"><span data-stu-id="10388-131">*gluQuadricCallback*</span></span>](gluquadric.md)
</dt> <dt>

[<span data-ttu-id="10388-132">**gluQuadricDrawStyle**</span><span class="sxs-lookup"><span data-stu-id="10388-132">**gluQuadricDrawStyle**</span></span>](gluquadricdrawstyle.md)
</dt> <dt>

[<span data-ttu-id="10388-133">**gluQuadricNormals**</span><span class="sxs-lookup"><span data-stu-id="10388-133">**gluQuadricNormals**</span></span>](gluquadricnormals.md)
</dt> <dt>

[<span data-ttu-id="10388-134">**gluQuadricOrientation**</span><span class="sxs-lookup"><span data-stu-id="10388-134">**gluQuadricOrientation**</span></span>](gluquadricorientation.md)
</dt> <dt>

[<span data-ttu-id="10388-135">**gluQuadricTexture**</span><span class="sxs-lookup"><span data-stu-id="10388-135">**gluQuadricTexture**</span></span>](gluquadrictexture.md)
</dt> <dt>

[<span data-ttu-id="10388-136">**gluSphere**</span><span class="sxs-lookup"><span data-stu-id="10388-136">**gluSphere**</span></span>](glusphere.md)
</dt> </dl>

 

 





