---
title: 'gluNurbsCallback 函式 (X.glu 隊) '
description: GluNurbsCallback 函式會定義非統一有理數 B 曲線 (NURBS) 物件的回呼。
ms.assetid: 1e9afc00-57c6-459e-a9fc-463f45df2084
keywords:
- gluNurbsCallback 函式 OpenGL
topic_type:
- apiref
api_name:
- gluNurbsCallback
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40a716724546ef0df4300bedb9aba44f7a23f530
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106976354"
---
# <a name="glunurbscallback-function"></a><span data-ttu-id="dcce1-104">gluNurbsCallback 函式</span><span class="sxs-lookup"><span data-stu-id="dcce1-104">gluNurbsCallback function</span></span>

<span data-ttu-id="dcce1-105">**GluNurbsCallback** 函式會定義非統一有理數 B 曲線 ([NURBS](using-nurbs-curves-and-surfaces.md)) 物件的回呼。</span><span class="sxs-lookup"><span data-stu-id="dcce1-105">The **gluNurbsCallback** function defines a callback for a Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcce1-106">語法</span><span class="sxs-lookup"><span data-stu-id="dcce1-106">Syntax</span></span>


```C++
void WINAPI gluNurbsCallback(
   GLUnurbs *nobj,
   GLenum   which,
   void (CALLBACK *fn)()
);
```



## <a name="parameters"></a><span data-ttu-id="dcce1-107">參數</span><span class="sxs-lookup"><span data-stu-id="dcce1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dcce1-108">*nobj*</span><span class="sxs-lookup"><span data-stu-id="dcce1-108">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="dcce1-109">使用 [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)) 建立的 NURBS 物件 (。</span><span class="sxs-lookup"><span data-stu-id="dcce1-109">The NURBS object (created with [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span></span>

</dd> <dt>

<span data-ttu-id="dcce1-110">*頻率*</span><span class="sxs-lookup"><span data-stu-id="dcce1-110">*which*</span></span> 
</dt> <dd>

<span data-ttu-id="dcce1-111">要定義的回呼。</span><span class="sxs-lookup"><span data-stu-id="dcce1-111">The callback being defined.</span></span> <span data-ttu-id="dcce1-112">唯一有效的值為 X.GLU 隊 \_ 錯誤。</span><span class="sxs-lookup"><span data-stu-id="dcce1-112">The only valid value is GLU\_ERROR.</span></span> <span data-ttu-id="dcce1-113">X.GLU 隊錯誤的意義 \_ 表示當發生錯誤時，會呼叫錯誤函式。</span><span class="sxs-lookup"><span data-stu-id="dcce1-113">The meaning of GLU\_ERROR means that the error function is called when an error is encountered.</span></span> <span data-ttu-id="dcce1-114">其單一引數的類型為 **GLenum**，它會指出發生的特定錯誤。</span><span class="sxs-lookup"><span data-stu-id="dcce1-114">Its single argument is of type **GLenum**, and it indicates the specific error that occurred.</span></span> <span data-ttu-id="dcce1-115">X.GLU 隊 \_ nurbs \_ ERROR1 透過 X.glu 隊 \_ NURBS ERROR37，是唯一的37錯誤 \_ 。</span><span class="sxs-lookup"><span data-stu-id="dcce1-115">There are 37 errors unique to NURBS, named GLU\_NURBS\_ERROR1 through GLU\_NURBS\_ERROR37.</span></span> <span data-ttu-id="dcce1-116">描述這些錯誤的字元字串可使用 [**gluErrorString**](gluerrorstring.md)來加以取出。</span><span class="sxs-lookup"><span data-stu-id="dcce1-116">Character strings describing these errors can be retrieved with [**gluErrorString**](gluerrorstring.md).</span></span>

</dd> <dt>

<span data-ttu-id="dcce1-117">*Fn*</span><span class="sxs-lookup"><span data-stu-id="dcce1-117">*fn*</span></span> 
</dt> <dd>

<span data-ttu-id="dcce1-118">回呼函數的指標。</span><span class="sxs-lookup"><span data-stu-id="dcce1-118">A pointer to the callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dcce1-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="dcce1-119">Return value</span></span>

<span data-ttu-id="dcce1-120">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="dcce1-120">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dcce1-121">備註</span><span class="sxs-lookup"><span data-stu-id="dcce1-121">Remarks</span></span>

<span data-ttu-id="dcce1-122">使用 **gluNurbsCallback** 來定義由 NURBS 物件使用的回呼。</span><span class="sxs-lookup"><span data-stu-id="dcce1-122">Use **gluNurbsCallback** to define a callback to be used by a NURBS object.</span></span> <span data-ttu-id="dcce1-123">如果已定義指定的回呼，則會予以取代。</span><span class="sxs-lookup"><span data-stu-id="dcce1-123">If the specified callback is already defined, it is replaced.</span></span> <span data-ttu-id="dcce1-124">如果 *fn* 為 **Null**，則會清除任何現有的回呼。</span><span class="sxs-lookup"><span data-stu-id="dcce1-124">If *fn* is **NULL**, then any existing callback is erased.</span></span>

## <a name="requirements"></a><span data-ttu-id="dcce1-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="dcce1-125">Requirements</span></span>



| <span data-ttu-id="dcce1-126">需求</span><span class="sxs-lookup"><span data-stu-id="dcce1-126">Requirement</span></span> | <span data-ttu-id="dcce1-127">值</span><span class="sxs-lookup"><span data-stu-id="dcce1-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="dcce1-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dcce1-128">Minimum supported client</span></span><br/> | <span data-ttu-id="dcce1-129">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dcce1-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="dcce1-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dcce1-130">Minimum supported server</span></span><br/> | <span data-ttu-id="dcce1-131">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dcce1-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="dcce1-132">標頭</span><span class="sxs-lookup"><span data-stu-id="dcce1-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="dcce1-133"><dt>X.glu 隊。h</dt></span><span class="sxs-lookup"><span data-stu-id="dcce1-133"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="dcce1-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="dcce1-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="dcce1-135"><dt>Glu32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="dcce1-135"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="dcce1-136">DLL</span><span class="sxs-lookup"><span data-stu-id="dcce1-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dcce1-137"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dcce1-137"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dcce1-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dcce1-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcce1-139">**gluErrorString**</span><span class="sxs-lookup"><span data-stu-id="dcce1-139">**gluErrorString**</span></span>](gluerrorstring.md)
</dt> <dt>

[<span data-ttu-id="dcce1-140">**gluNewNurbsRenderer**</span><span class="sxs-lookup"><span data-stu-id="dcce1-140">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> </dl>

 

 





