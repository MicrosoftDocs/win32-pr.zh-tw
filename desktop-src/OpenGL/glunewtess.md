---
title: 'gluNewTess 函式 (X.glu 隊) '
description: GluNewTess 函式會建立鑲嵌式物件。
ms.assetid: dfc9fce8-ecab-493b-85ee-6d7487814186
keywords:
- gluNewTess 函式 OpenGL
topic_type:
- apiref
api_name:
- gluNewTess
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0573ead0cf9b81568c4bf2101e317bef7faf148
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968549"
---
# <a name="glunewtess-function"></a><span data-ttu-id="35e46-104">gluNewTess 函式</span><span class="sxs-lookup"><span data-stu-id="35e46-104">gluNewTess function</span></span>

<span data-ttu-id="35e46-105">**GluNewTess** 函式會建立鑲嵌式物件。</span><span class="sxs-lookup"><span data-stu-id="35e46-105">The **gluNewTess** function creates a tessellation object.</span></span>

## <a name="syntax"></a><span data-ttu-id="35e46-106">語法</span><span class="sxs-lookup"><span data-stu-id="35e46-106">Syntax</span></span>


```C++
GLUtesselator* WINAPI gluNewTess(void);
```



## <a name="parameters"></a><span data-ttu-id="35e46-107">參數</span><span class="sxs-lookup"><span data-stu-id="35e46-107">Parameters</span></span>

<span data-ttu-id="35e46-108">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="35e46-108">This function has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="35e46-109">備註</span><span class="sxs-lookup"><span data-stu-id="35e46-109">Remarks</span></span>

<span data-ttu-id="35e46-110">**GluNewTess** 函式會建立並傳回新鑲嵌物件的指標。</span><span class="sxs-lookup"><span data-stu-id="35e46-110">The **gluNewTess** function creates and returns a pointer to a new tessellation object.</span></span> <span data-ttu-id="35e46-111">呼叫鑲嵌函式時，請參考這個物件。</span><span class="sxs-lookup"><span data-stu-id="35e46-111">Refer to this object when calling tessellation functions.</span></span> <span data-ttu-id="35e46-112">傳回值為0表示沒有足夠的記憶體可配置給物件。</span><span class="sxs-lookup"><span data-stu-id="35e46-112">A return value of zero means there is not enough memory to allocate to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="35e46-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="35e46-113">Requirements</span></span>



| <span data-ttu-id="35e46-114">需求</span><span class="sxs-lookup"><span data-stu-id="35e46-114">Requirement</span></span> | <span data-ttu-id="35e46-115">值</span><span class="sxs-lookup"><span data-stu-id="35e46-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="35e46-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="35e46-116">Minimum supported client</span></span><br/> | <span data-ttu-id="35e46-117">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="35e46-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="35e46-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="35e46-118">Minimum supported server</span></span><br/> | <span data-ttu-id="35e46-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="35e46-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="35e46-120">標頭</span><span class="sxs-lookup"><span data-stu-id="35e46-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="35e46-121"><dt>X.glu 隊。h</dt></span><span class="sxs-lookup"><span data-stu-id="35e46-121"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="35e46-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="35e46-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="35e46-123"><dt>Glu32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="35e46-123"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="35e46-124">DLL</span><span class="sxs-lookup"><span data-stu-id="35e46-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35e46-125"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35e46-125"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35e46-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="35e46-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35e46-127">**gluDeleteTess**</span><span class="sxs-lookup"><span data-stu-id="35e46-127">**gluDeleteTess**</span></span>](gludeletetess.md)
</dt> <dt>

[<span data-ttu-id="35e46-128">**gluTessBeginPolygon**</span><span class="sxs-lookup"><span data-stu-id="35e46-128">**gluTessBeginPolygon**</span></span>](glubeginpolygon.md)
</dt> <dt>

[<span data-ttu-id="35e46-129">*gluTessCallback*</span><span class="sxs-lookup"><span data-stu-id="35e46-129">*gluTessCallback*</span></span>](glutess.md)
</dt> </dl>

 

 





