---
title: 'gluGetNurbsProperty 函式 (X.glu 隊) '
description: GluGetNurbsProperty 函式會取得非統一的有理 B 曲線 (NURBS) 屬性。
ms.assetid: 7dbc75a0-d04e-4794-b3dd-a602addf9dfa
keywords:
- gluGetNurbsProperty 函式 OpenGL
topic_type:
- apiref
api_name:
- gluGetNurbsProperty
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 583da688e3495ebc2eb9d6f71972658c6426469c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094375"
---
# <a name="glugetnurbsproperty-function"></a><span data-ttu-id="0e9a9-104">gluGetNurbsProperty 函式</span><span class="sxs-lookup"><span data-stu-id="0e9a9-104">gluGetNurbsProperty function</span></span>

<span data-ttu-id="0e9a9-105">**GluGetNurbsProperty** 函式會取得非統一的有理 B 曲線 ([NURBS](using-nurbs-curves-and-surfaces.md)) 屬性。</span><span class="sxs-lookup"><span data-stu-id="0e9a9-105">The **gluGetNurbsProperty** function gets a Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e9a9-106">語法</span><span class="sxs-lookup"><span data-stu-id="0e9a9-106">Syntax</span></span>


```C++
void WINAPI gluGetNurbsProperty(
   GLUnurbs *nobj,
   GLenum   property,
   GLfloat  *value
);
```



## <a name="parameters"></a><span data-ttu-id="0e9a9-107">參數</span><span class="sxs-lookup"><span data-stu-id="0e9a9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e9a9-108">*nobj*</span><span class="sxs-lookup"><span data-stu-id="0e9a9-108">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="0e9a9-109">使用 [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)) 建立的 NURBS 物件 (。</span><span class="sxs-lookup"><span data-stu-id="0e9a9-109">The NURBS object (created with [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span></span>

</dd> <dt>

<span data-ttu-id="0e9a9-110">*property*</span><span class="sxs-lookup"><span data-stu-id="0e9a9-110">*property*</span></span> 
</dt> <dd>

<span data-ttu-id="0e9a9-111">要取出其值的屬性。</span><span class="sxs-lookup"><span data-stu-id="0e9a9-111">The property whose value is to be retrieved.</span></span> <span data-ttu-id="0e9a9-112">下列值有效： X.GLU 隊 \_ 取樣 \_ 容錯、X.glu 隊 \_ 顯示 \_ 模式、X.glu 隊 \_ 剔除、X.GLU 隊 \_ 自動 \_ 載入 \_ 矩陣、X.GLU 隊 \_ 參數 \_ 容錯、X.glu 隊 \_ 取樣 \_ 方法、x.glu 隊 \_ U \_ 步驟和 x.glu 隊 \_ V \_ 步驟。</span><span class="sxs-lookup"><span data-stu-id="0e9a9-112">The following values are valid: GLU\_SAMPLING\_TOLERANCE, GLU\_DISPLAY\_MODE, GLU\_CULLING, GLU\_AUTO\_LOAD\_MATRIX, GLU\_PARAMETRIC\_TOLERANCE, GLU\_SAMPLING\_METHOD, GLU\_U\_STEP, and GLU\_V\_STEP.</span></span>

</dd> <dt>

<span data-ttu-id="0e9a9-113">*value*</span><span class="sxs-lookup"><span data-stu-id="0e9a9-113">*value*</span></span> 
</dt> <dd>

<span data-ttu-id="0e9a9-114">要在其中寫入已命名屬性值之位置的指標。</span><span class="sxs-lookup"><span data-stu-id="0e9a9-114">A pointer to the location into which the value of the named property is written.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e9a9-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="0e9a9-115">Return value</span></span>

<span data-ttu-id="0e9a9-116">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="0e9a9-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e9a9-117">備註</span><span class="sxs-lookup"><span data-stu-id="0e9a9-117">Remarks</span></span>

<span data-ttu-id="0e9a9-118">使用 **gluGetNurbsProperty** 來取出儲存在 NURBS 物件中的屬性。</span><span class="sxs-lookup"><span data-stu-id="0e9a9-118">Use **gluGetNurbsProperty** to retrieve properties stored in a NURBS object.</span></span> <span data-ttu-id="0e9a9-119">這些屬性會影響 NURBS 曲線和表面的呈現方式。</span><span class="sxs-lookup"><span data-stu-id="0e9a9-119">These properties affect the way NURBS curves and surfaces are rendered.</span></span> <span data-ttu-id="0e9a9-120">如需 NURBS 屬性的詳細資訊，請參閱 [**gluNurbsProperty**](glunurbsproperty.md)。</span><span class="sxs-lookup"><span data-stu-id="0e9a9-120">For information about NURBS properties, see [**gluNurbsProperty**](glunurbsproperty.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0e9a9-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="0e9a9-121">Requirements</span></span>



| <span data-ttu-id="0e9a9-122">需求</span><span class="sxs-lookup"><span data-stu-id="0e9a9-122">Requirement</span></span> | <span data-ttu-id="0e9a9-123">值</span><span class="sxs-lookup"><span data-stu-id="0e9a9-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0e9a9-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0e9a9-124">Minimum supported client</span></span><br/> | <span data-ttu-id="0e9a9-125">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0e9a9-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="0e9a9-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0e9a9-126">Minimum supported server</span></span><br/> | <span data-ttu-id="0e9a9-127">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0e9a9-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="0e9a9-128">標頭</span><span class="sxs-lookup"><span data-stu-id="0e9a9-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e9a9-129"><dt>X.glu 隊。h</dt></span><span class="sxs-lookup"><span data-stu-id="0e9a9-129"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="0e9a9-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="0e9a9-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="0e9a9-131"><dt>Glu32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="0e9a9-131"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="0e9a9-132">DLL</span><span class="sxs-lookup"><span data-stu-id="0e9a9-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e9a9-133"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e9a9-133"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e9a9-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0e9a9-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e9a9-135">**gluNewNurbsRenderer**</span><span class="sxs-lookup"><span data-stu-id="0e9a9-135">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> <dt>

[<span data-ttu-id="0e9a9-136">**gluNurbsProperty**</span><span class="sxs-lookup"><span data-stu-id="0e9a9-136">**gluNurbsProperty**</span></span>](glunurbsproperty.md)
</dt> </dl>

 

 





