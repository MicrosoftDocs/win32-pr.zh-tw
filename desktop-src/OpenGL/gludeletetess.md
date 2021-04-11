---
title: 'gluDeleteTess 函式 (X.glu 隊) '
description: GluDeleteTess 函式會終結鑲嵌式物件。
ms.assetid: 7e1540f7-5e7d-4a3b-8c94-5a6800b17411
keywords:
- gluDeleteTess 函式 OpenGL
topic_type:
- apiref
api_name:
- gluDeleteTess
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee4625f0a9c2f51e9d7147c9564fcd4fb1fa7117
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685690"
---
# <a name="gludeletetess-function"></a><span data-ttu-id="840f2-104">gluDeleteTess 函式</span><span class="sxs-lookup"><span data-stu-id="840f2-104">gluDeleteTess function</span></span>

<span data-ttu-id="840f2-105">**GluDeleteTess** 函式會終結鑲嵌式物件。</span><span class="sxs-lookup"><span data-stu-id="840f2-105">The **gluDeleteTess** function destroys a tessellation object.</span></span>

## <a name="syntax"></a><span data-ttu-id="840f2-106">語法</span><span class="sxs-lookup"><span data-stu-id="840f2-106">Syntax</span></span>


```C++
void WINAPI gluDeleteTess(
   GLUtesselator *tess
);
```



## <a name="parameters"></a><span data-ttu-id="840f2-107">參數</span><span class="sxs-lookup"><span data-stu-id="840f2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="840f2-108">*苔 絲*</span><span class="sxs-lookup"><span data-stu-id="840f2-108">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="840f2-109">要終結 (使用 [**gluNewTess**](glunewtess.md)) 所建立的鑲嵌式物件。</span><span class="sxs-lookup"><span data-stu-id="840f2-109">The tessellation object to destroy (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="840f2-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="840f2-110">Return value</span></span>

<span data-ttu-id="840f2-111">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="840f2-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="840f2-112">備註</span><span class="sxs-lookup"><span data-stu-id="840f2-112">Remarks</span></span>

<span data-ttu-id="840f2-113">**GluDeleteTess** 函式會終結指定的鑲嵌物件，並釋放其使用的任何記憶體。</span><span class="sxs-lookup"><span data-stu-id="840f2-113">The **gluDeleteTess** function destroys the indicated tessellation object and frees any memory that it used.</span></span>

## <a name="requirements"></a><span data-ttu-id="840f2-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="840f2-114">Requirements</span></span>



| <span data-ttu-id="840f2-115">需求</span><span class="sxs-lookup"><span data-stu-id="840f2-115">Requirement</span></span> | <span data-ttu-id="840f2-116">值</span><span class="sxs-lookup"><span data-stu-id="840f2-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="840f2-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="840f2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="840f2-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="840f2-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="840f2-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="840f2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="840f2-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="840f2-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="840f2-121">標頭</span><span class="sxs-lookup"><span data-stu-id="840f2-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="840f2-122"><dt>X.glu 隊。h</dt></span><span class="sxs-lookup"><span data-stu-id="840f2-122"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="840f2-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="840f2-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="840f2-124"><dt>Glu32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="840f2-124"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="840f2-125">DLL</span><span class="sxs-lookup"><span data-stu-id="840f2-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="840f2-126"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="840f2-126"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="840f2-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="840f2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="840f2-128">**gluNewTess**</span><span class="sxs-lookup"><span data-stu-id="840f2-128">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="840f2-129">**gluTessBeginPolygon**</span><span class="sxs-lookup"><span data-stu-id="840f2-129">**gluTessBeginPolygon**</span></span>](glubeginpolygon.md)
</dt> <dt>

[<span data-ttu-id="840f2-130">*gluTessCallback*</span><span class="sxs-lookup"><span data-stu-id="840f2-130">*gluTessCallback*</span></span>](glutess.md)
</dt> </dl>

 

 





