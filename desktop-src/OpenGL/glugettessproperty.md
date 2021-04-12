---
title: 'gluGetTessProperty 函式 (X.glu 隊) '
description: GluGetTessProperty 函式會取得鑲嵌式物件屬性。
ms.assetid: 6aa565d8-2257-4259-a959-b7d806a7ed96
keywords:
- gluGetTessProperty 函式 OpenGL
topic_type:
- apiref
api_name:
- gluGetTessProperty
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 482f32b227dbcf0c2a62405e344aa719bb4b9e17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384458"
---
# <a name="glugettessproperty-function"></a><span data-ttu-id="1ce2a-104">gluGetTessProperty 函式</span><span class="sxs-lookup"><span data-stu-id="1ce2a-104">gluGetTessProperty function</span></span>

<span data-ttu-id="1ce2a-105">**GluGetTessProperty** 函式會取得鑲嵌式物件屬性。</span><span class="sxs-lookup"><span data-stu-id="1ce2a-105">The **gluGetTessProperty** function gets a tessellation object property.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ce2a-106">語法</span><span class="sxs-lookup"><span data-stu-id="1ce2a-106">Syntax</span></span>


```C++
void WINAPI gluGetTessProperty(
   GLUtesselator *tess,
   GLenum        which,
   GLdouble      *value
);
```



## <a name="parameters"></a><span data-ttu-id="1ce2a-107">參數</span><span class="sxs-lookup"><span data-stu-id="1ce2a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ce2a-108">*苔 絲*</span><span class="sxs-lookup"><span data-stu-id="1ce2a-108">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="1ce2a-109">使用 [**gluNewTess**](glunewtess.md)) 建立的鑲嵌式物件 (。</span><span class="sxs-lookup"><span data-stu-id="1ce2a-109">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> <dt>

<span data-ttu-id="1ce2a-110">*頻率*</span><span class="sxs-lookup"><span data-stu-id="1ce2a-110">*which*</span></span> 
</dt> <dd>

<span data-ttu-id="1ce2a-111">要取出其值的屬性。</span><span class="sxs-lookup"><span data-stu-id="1ce2a-111">The property whose value is to be retrieved.</span></span> <span data-ttu-id="1ce2a-112">下列值有效： X.GLU 隊 \_ TESS \_ 繞組 \_ RULE、x.glu 隊 \_ TESS \_ 界限 \_ ，以及 x.glu 隊 \_ TESS \_ 容錯。</span><span class="sxs-lookup"><span data-stu-id="1ce2a-112">The following values are valid: GLU\_TESS\_WINDING\_RULE, GLU\_TESS\_BOUNDARY\_ONLY, and GLU\_TESS\_TOLERANCE.</span></span>

</dd> <dt>

<span data-ttu-id="1ce2a-113">*value*</span><span class="sxs-lookup"><span data-stu-id="1ce2a-113">*value*</span></span> 
</dt> <dd>

<span data-ttu-id="1ce2a-114">要在其中寫入已命名屬性值之位置的指標。</span><span class="sxs-lookup"><span data-stu-id="1ce2a-114">A pointer to the location where the value of the named property is written.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ce2a-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="1ce2a-115">Return value</span></span>

<span data-ttu-id="1ce2a-116">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="1ce2a-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ce2a-117">備註</span><span class="sxs-lookup"><span data-stu-id="1ce2a-117">Remarks</span></span>

<span data-ttu-id="1ce2a-118">使用 **gluGetTessProperty** 來取出鑲嵌物件中儲存的屬性。</span><span class="sxs-lookup"><span data-stu-id="1ce2a-118">Use **gluGetTessProperty** to retrieve properties stored in a tessellation object.</span></span> <span data-ttu-id="1ce2a-119">這些屬性會影響鑲嵌式物件的解讀和轉譯方式。</span><span class="sxs-lookup"><span data-stu-id="1ce2a-119">These properties affect the way tessellation objects are interpreted and rendered.</span></span> <span data-ttu-id="1ce2a-120">如需屬性的內容和其用途的詳細資訊，請參閱 [**gluTessProperty**](glutessproperty.md)。</span><span class="sxs-lookup"><span data-stu-id="1ce2a-120">For information about what the properties are and what they do, see [**gluTessProperty**](glutessproperty.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1ce2a-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="1ce2a-121">Requirements</span></span>



| <span data-ttu-id="1ce2a-122">需求</span><span class="sxs-lookup"><span data-stu-id="1ce2a-122">Requirement</span></span> | <span data-ttu-id="1ce2a-123">值</span><span class="sxs-lookup"><span data-stu-id="1ce2a-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1ce2a-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1ce2a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1ce2a-125">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1ce2a-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="1ce2a-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1ce2a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1ce2a-127">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1ce2a-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="1ce2a-128">標頭</span><span class="sxs-lookup"><span data-stu-id="1ce2a-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ce2a-129"><dt>X.glu 隊。h</dt></span><span class="sxs-lookup"><span data-stu-id="1ce2a-129"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="1ce2a-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="1ce2a-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="1ce2a-131"><dt>Glu32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="1ce2a-131"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="1ce2a-132">DLL</span><span class="sxs-lookup"><span data-stu-id="1ce2a-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ce2a-133"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ce2a-133"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ce2a-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1ce2a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ce2a-135">**gluNewTess**</span><span class="sxs-lookup"><span data-stu-id="1ce2a-135">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="1ce2a-136">**gluTessProperty**</span><span class="sxs-lookup"><span data-stu-id="1ce2a-136">**gluTessProperty**</span></span>](glutessproperty.md)
</dt> </dl>

 

 





