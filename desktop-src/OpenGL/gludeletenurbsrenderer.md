---
title: 'gluDeleteNurbsRenderer 函式 (X.glu 隊) '
description: GluDeleteNurbsRenderer 函式會終結非統一的有理 B 曲線 (NURBS) 物件。
ms.assetid: 77063dcb-90b8-47e4-8b00-e1c46cf4f712
keywords:
- gluDeleteNurbsRenderer 函式 OpenGL
topic_type:
- apiref
api_name:
- gluDeleteNurbsRenderer
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fb6ecf0bbb7076d4d6292676d3d358586d0986c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685887"
---
# <a name="gludeletenurbsrenderer-function"></a><span data-ttu-id="d5488-104">gluDeleteNurbsRenderer 函式</span><span class="sxs-lookup"><span data-stu-id="d5488-104">gluDeleteNurbsRenderer function</span></span>

<span data-ttu-id="d5488-105">**GluDeleteNurbsRenderer** 函式會終結非統一的有理 B 曲線 ([NURBS](using-nurbs-curves-and-surfaces.md)) 物件。</span><span class="sxs-lookup"><span data-stu-id="d5488-105">The **gluDeleteNurbsRenderer** function destroys a Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5488-106">語法</span><span class="sxs-lookup"><span data-stu-id="d5488-106">Syntax</span></span>


```C++
void WINAPI gluDeleteNurbsRenderer(
   GLUnurbs *nobj
);
```



## <a name="parameters"></a><span data-ttu-id="d5488-107">參數</span><span class="sxs-lookup"><span data-stu-id="d5488-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5488-108">*nobj*</span><span class="sxs-lookup"><span data-stu-id="d5488-108">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="d5488-109">要終結 (使用 **gluNewNurbsRenderer**) 所建立的 NURBS 物件。</span><span class="sxs-lookup"><span data-stu-id="d5488-109">The NURBS object to be destroyed (created with **gluNewNurbsRenderer**).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5488-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="d5488-110">Return value</span></span>

<span data-ttu-id="d5488-111">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="d5488-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5488-112">備註</span><span class="sxs-lookup"><span data-stu-id="d5488-112">Remarks</span></span>

<span data-ttu-id="d5488-113">**GluDeleteNurbsRenderer** 函式會終結 NURBS 物件，並釋放其使用的任何記憶體。</span><span class="sxs-lookup"><span data-stu-id="d5488-113">The **gluDeleteNurbsRenderer** function destroys the NURBS object and frees any memory that it used.</span></span> <span data-ttu-id="d5488-114">當您呼叫 **gluDeleteNurbsRenderer** 之後，就無法再使用 *nobj* 。</span><span class="sxs-lookup"><span data-stu-id="d5488-114">After you have called **gluDeleteNurbsRenderer**, you cannot use *nobj* again.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5488-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="d5488-115">Requirements</span></span>



| <span data-ttu-id="d5488-116">需求</span><span class="sxs-lookup"><span data-stu-id="d5488-116">Requirement</span></span> | <span data-ttu-id="d5488-117">值</span><span class="sxs-lookup"><span data-stu-id="d5488-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d5488-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d5488-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d5488-119">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d5488-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="d5488-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d5488-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d5488-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d5488-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d5488-122">標頭</span><span class="sxs-lookup"><span data-stu-id="d5488-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5488-123"><dt>X.glu 隊。h</dt></span><span class="sxs-lookup"><span data-stu-id="d5488-123"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="d5488-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="d5488-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="d5488-125"><dt>Glu32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d5488-125"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="d5488-126">DLL</span><span class="sxs-lookup"><span data-stu-id="d5488-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d5488-127"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5488-127"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5488-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d5488-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5488-129">**gluNewNurbsRenderer**</span><span class="sxs-lookup"><span data-stu-id="d5488-129">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> </dl>

 

 





