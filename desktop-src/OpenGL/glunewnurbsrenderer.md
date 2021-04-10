---
title: 'gluNewNurbsRenderer 函式 (X.glu 隊) '
description: GluNewNurbsRenderer 函式會建立非統一的有理 B 曲線 (NURBS) 物件。
ms.assetid: f47badb0-6b75-4bfd-9771-516668d9e255
keywords:
- gluNewNurbsRenderer 函式 OpenGL
topic_type:
- apiref
api_name:
- gluNewNurbsRenderer
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b6e35df5abd9fb9e7757dd79066fbbe7efe8680
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934605"
---
# <a name="glunewnurbsrenderer-function"></a><span data-ttu-id="74277-104">gluNewNurbsRenderer 函式</span><span class="sxs-lookup"><span data-stu-id="74277-104">gluNewNurbsRenderer function</span></span>

<span data-ttu-id="74277-105">**GluNewNurbsRenderer** 函式會建立非統一的有理 B 曲線 ([NURBS](using-nurbs-curves-and-surfaces.md)) 物件。</span><span class="sxs-lookup"><span data-stu-id="74277-105">The **gluNewNurbsRenderer** function creates a Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="74277-106">語法</span><span class="sxs-lookup"><span data-stu-id="74277-106">Syntax</span></span>


```C++
GLUnurbs* WINAPI gluNewNurbsRenderer(void);
```



## <a name="parameters"></a><span data-ttu-id="74277-107">參數</span><span class="sxs-lookup"><span data-stu-id="74277-107">Parameters</span></span>

<span data-ttu-id="74277-108">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="74277-108">This function has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="74277-109">備註</span><span class="sxs-lookup"><span data-stu-id="74277-109">Remarks</span></span>

<span data-ttu-id="74277-110">**GluNewNurbsRenderer** 函式會建立並傳回新的 NURBS 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="74277-110">The **gluNewNurbsRenderer** function creates and returns a pointer to a new NURBS object.</span></span> <span data-ttu-id="74277-111">呼叫 NURBS 轉譯和控制函式時，請參考這個物件。</span><span class="sxs-lookup"><span data-stu-id="74277-111">Refer to this object when calling NURBS rendering and control functions.</span></span> <span data-ttu-id="74277-112">傳回值為0表示沒有足夠的記憶體可配置給物件。</span><span class="sxs-lookup"><span data-stu-id="74277-112">A return value of zero means there is not enough memory to allocate to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="74277-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="74277-113">Requirements</span></span>



| <span data-ttu-id="74277-114">需求</span><span class="sxs-lookup"><span data-stu-id="74277-114">Requirement</span></span> | <span data-ttu-id="74277-115">值</span><span class="sxs-lookup"><span data-stu-id="74277-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="74277-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="74277-116">Minimum supported client</span></span><br/> | <span data-ttu-id="74277-117">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="74277-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="74277-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="74277-118">Minimum supported server</span></span><br/> | <span data-ttu-id="74277-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="74277-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="74277-120">標頭</span><span class="sxs-lookup"><span data-stu-id="74277-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="74277-121"><dt>X.glu 隊。h</dt></span><span class="sxs-lookup"><span data-stu-id="74277-121"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="74277-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="74277-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="74277-123"><dt>Glu32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="74277-123"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="74277-124">DLL</span><span class="sxs-lookup"><span data-stu-id="74277-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74277-125"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="74277-125"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74277-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="74277-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74277-127">**gluBeginCurve**</span><span class="sxs-lookup"><span data-stu-id="74277-127">**gluBeginCurve**</span></span>](glubegincurve.md)
</dt> <dt>

[<span data-ttu-id="74277-128">**gluBeginSurface**</span><span class="sxs-lookup"><span data-stu-id="74277-128">**gluBeginSurface**</span></span>](glubeginsurface.md)
</dt> <dt>

[<span data-ttu-id="74277-129">**gluBeginTrim**</span><span class="sxs-lookup"><span data-stu-id="74277-129">**gluBeginTrim**</span></span>](glubegintrim.md)
</dt> <dt>

[<span data-ttu-id="74277-130">**gluDeleteNurbsRenderer**</span><span class="sxs-lookup"><span data-stu-id="74277-130">**gluDeleteNurbsRenderer**</span></span>](gludeletenurbsrenderer.md)
</dt> <dt>

[<span data-ttu-id="74277-131">*gluNurbsCallback*</span><span class="sxs-lookup"><span data-stu-id="74277-131">*gluNurbsCallback*</span></span>](glunurbs.md)
</dt> <dt>

[<span data-ttu-id="74277-132">**gluNurbsProperty**</span><span class="sxs-lookup"><span data-stu-id="74277-132">**gluNurbsProperty**</span></span>](glunurbsproperty.md)
</dt> </dl>

 

 





