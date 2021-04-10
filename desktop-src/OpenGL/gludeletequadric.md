---
title: 'gluDeleteQuadric 函式 (X.glu 隊) '
description: GluDeleteQuadric 函式會終結 quadric 物件。
ms.assetid: 09efd887-0fe8-4a56-bc6f-2177a4930035
keywords:
- gluDeleteQuadric 函式 OpenGL
topic_type:
- apiref
api_name:
- gluDeleteQuadric
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b5ee85e943cd958e394efb191932393d228d948
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686090"
---
# <a name="gludeletequadric-function"></a><span data-ttu-id="bb914-104">gluDeleteQuadric 函式</span><span class="sxs-lookup"><span data-stu-id="bb914-104">gluDeleteQuadric function</span></span>

<span data-ttu-id="bb914-105">**GluDeleteQuadric** 函式會終結 quadric 物件。</span><span class="sxs-lookup"><span data-stu-id="bb914-105">The **gluDeleteQuadric** function destroys a quadric object.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb914-106">語法</span><span class="sxs-lookup"><span data-stu-id="bb914-106">Syntax</span></span>


```C++
void WINAPI gluDeleteQuadric(
   GLUquadricObj *state
);
```



## <a name="parameters"></a><span data-ttu-id="bb914-107">參數</span><span class="sxs-lookup"><span data-stu-id="bb914-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb914-108">*state*</span><span class="sxs-lookup"><span data-stu-id="bb914-108">*state*</span></span> 
</dt> <dd>

<span data-ttu-id="bb914-109">要終結 (使用 [**gluNewQuadric**](glunewquadric.md)) 所建立的 quadric 物件。</span><span class="sxs-lookup"><span data-stu-id="bb914-109">The quadric object to be destroyed (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb914-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="bb914-110">Return value</span></span>

<span data-ttu-id="bb914-111">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="bb914-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb914-112">備註</span><span class="sxs-lookup"><span data-stu-id="bb914-112">Remarks</span></span>

<span data-ttu-id="bb914-113">**GluDeleteQuadric** 函式會終結 quadric 物件，並釋放其使用的任何記憶體。</span><span class="sxs-lookup"><span data-stu-id="bb914-113">The **gluDeleteQuadric** function destroys the quadric object and frees any memory that it used.</span></span> <span data-ttu-id="bb914-114">在您呼叫 **gluDeleteQuadric** 之後，就無法再使用 *狀態* 。</span><span class="sxs-lookup"><span data-stu-id="bb914-114">After you have called **gluDeleteQuadric**, you cannot use *state* again.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb914-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="bb914-115">Requirements</span></span>



| <span data-ttu-id="bb914-116">需求</span><span class="sxs-lookup"><span data-stu-id="bb914-116">Requirement</span></span> | <span data-ttu-id="bb914-117">值</span><span class="sxs-lookup"><span data-stu-id="bb914-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="bb914-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bb914-118">Minimum supported client</span></span><br/> | <span data-ttu-id="bb914-119">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bb914-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="bb914-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bb914-120">Minimum supported server</span></span><br/> | <span data-ttu-id="bb914-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bb914-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="bb914-122">標頭</span><span class="sxs-lookup"><span data-stu-id="bb914-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb914-123"><dt>X.glu 隊。h</dt></span><span class="sxs-lookup"><span data-stu-id="bb914-123"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="bb914-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="bb914-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="bb914-125"><dt>Glu32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="bb914-125"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="bb914-126">DLL</span><span class="sxs-lookup"><span data-stu-id="bb914-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb914-127"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb914-127"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb914-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bb914-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb914-129">**gluNewQuadric**</span><span class="sxs-lookup"><span data-stu-id="bb914-129">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> </dl>

 

 





