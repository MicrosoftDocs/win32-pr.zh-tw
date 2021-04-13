---
title: 'gluTessVertex 函式 (X.glu 隊) '
description: GluTessVertex 函數會指定多邊形上的頂點。
ms.assetid: 9c555b32-5257-4eeb-9323-ccad59591097
keywords:
- gluTessVertex 函式 OpenGL
topic_type:
- apiref
api_name:
- gluTessVertex
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 546bbad2be1205f62c7889fbb18f23d5b0e38b8a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509295"
---
# <a name="glutessvertex-function"></a><span data-ttu-id="50d83-104">gluTessVertex 函式</span><span class="sxs-lookup"><span data-stu-id="50d83-104">gluTessVertex function</span></span>

<span data-ttu-id="50d83-105">**GluTessVertex** 函數會指定多邊形上的頂點。</span><span class="sxs-lookup"><span data-stu-id="50d83-105">The **gluTessVertex** function specifies a vertex on a polygon.</span></span>

## <a name="syntax"></a><span data-ttu-id="50d83-106">語法</span><span class="sxs-lookup"><span data-stu-id="50d83-106">Syntax</span></span>


```C++
void WINAPI gluTessVertex(
   GLUtesselator *tess,
   GLdouble      coords[3],
   void          *data
);
```



## <a name="parameters"></a><span data-ttu-id="50d83-107">參數</span><span class="sxs-lookup"><span data-stu-id="50d83-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50d83-108">*苔 絲*</span><span class="sxs-lookup"><span data-stu-id="50d83-108">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="50d83-109">使用 [**gluNewTess**](glunewtess.md)) 建立的鑲嵌式物件 (。</span><span class="sxs-lookup"><span data-stu-id="50d83-109">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> <dt>

<span data-ttu-id="50d83-110">*coords*</span><span class="sxs-lookup"><span data-stu-id="50d83-110">*coords*</span></span> 
</dt> <dd>

<span data-ttu-id="50d83-111">頂點的位置。</span><span class="sxs-lookup"><span data-stu-id="50d83-111">The location of the vertex.</span></span>

</dd> <dt>

<span data-ttu-id="50d83-112">*data*</span><span class="sxs-lookup"><span data-stu-id="50d83-112">*data*</span></span> 
</dt> <dd>

<span data-ttu-id="50d83-113">使用頂點回呼傳回給程式的指標 (如 [*gluTessCallback*](glutess.md)) 所指定。</span><span class="sxs-lookup"><span data-stu-id="50d83-113">An pointer passed back to the program with the vertex callback (as specified by [*gluTessCallback*](glutess.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50d83-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="50d83-114">Return value</span></span>

<span data-ttu-id="50d83-115">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="50d83-115">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="50d83-116">備註</span><span class="sxs-lookup"><span data-stu-id="50d83-116">Remarks</span></span>

<span data-ttu-id="50d83-117">**GluTessVertex** 函式會在使用者所定義的多邊形上描述頂點。</span><span class="sxs-lookup"><span data-stu-id="50d83-117">The **gluTessVertex** function describes a vertex on a polygon that the user is defining.</span></span> <span data-ttu-id="50d83-118">後續的 **gluTessVertex** 呼叫會描述封閉的輪廓。</span><span class="sxs-lookup"><span data-stu-id="50d83-118">Successive **gluTessVertex** calls describe a closed contour.</span></span> <span data-ttu-id="50d83-119">例如，若要描述四邊形，請呼叫 **gluTessVertex** 四次。</span><span class="sxs-lookup"><span data-stu-id="50d83-119">For example, to describe a quadrilateral, call **gluTessVertex** four times.</span></span> <span data-ttu-id="50d83-120">您只能呼叫 [**gluTessBeginContour**](glutessbegincontour.md)和 [**GluTessEndContour**](glutessendcontour.md)之間的 **gluTessVertex** 。</span><span class="sxs-lookup"><span data-stu-id="50d83-120">You can only call **gluTessVertex** between [**gluTessBeginContour**](glutessbegincontour.md) and [**gluTessEndContour**](glutessendcontour.md).</span></span>

<span data-ttu-id="50d83-121">*資料* 參數通常會指向包含頂點位置的結構，以及其他每個頂點的屬性，例如色彩和一般。</span><span class="sxs-lookup"><span data-stu-id="50d83-121">The *data* parameter normally points to a structure containing the vertex location, as well as other per-vertex attributes such as color and normal.</span></span> <span data-ttu-id="50d83-122">在鑲嵌之後，會透過 X.GLU 隊頂點回呼將指標傳回給程式 \_ gluTessCallback (請參閱[](glutess.md)) 。</span><span class="sxs-lookup"><span data-stu-id="50d83-122">This pointer is passed back to the program through the GLU\_VERTEX callback after tessellation (see [*gluTessCallback*](glutess.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="50d83-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="50d83-123">Requirements</span></span>



| <span data-ttu-id="50d83-124">需求</span><span class="sxs-lookup"><span data-stu-id="50d83-124">Requirement</span></span> | <span data-ttu-id="50d83-125">值</span><span class="sxs-lookup"><span data-stu-id="50d83-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="50d83-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="50d83-126">Minimum supported client</span></span><br/> | <span data-ttu-id="50d83-127">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="50d83-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="50d83-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="50d83-128">Minimum supported server</span></span><br/> | <span data-ttu-id="50d83-129">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="50d83-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="50d83-130">標頭</span><span class="sxs-lookup"><span data-stu-id="50d83-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="50d83-131"><dt>X.glu 隊。h</dt></span><span class="sxs-lookup"><span data-stu-id="50d83-131"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="50d83-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="50d83-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="50d83-133"><dt>Glu32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="50d83-133"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="50d83-134">DLL</span><span class="sxs-lookup"><span data-stu-id="50d83-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50d83-135"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50d83-135"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50d83-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="50d83-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50d83-137">**gluNewTess**</span><span class="sxs-lookup"><span data-stu-id="50d83-137">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="50d83-138">**gluTessBeginContour**</span><span class="sxs-lookup"><span data-stu-id="50d83-138">**gluTessBeginContour**</span></span>](glutessbegincontour.md)
</dt> <dt>

[<span data-ttu-id="50d83-139">**gluTessBeginPolygon**</span><span class="sxs-lookup"><span data-stu-id="50d83-139">**gluTessBeginPolygon**</span></span>](glubeginpolygon.md)
</dt> <dt>

[<span data-ttu-id="50d83-140">*gluTessCallback*</span><span class="sxs-lookup"><span data-stu-id="50d83-140">*gluTessCallback*</span></span>](glutess.md)
</dt> <dt>

[<span data-ttu-id="50d83-141">**gluTessEndContour**</span><span class="sxs-lookup"><span data-stu-id="50d83-141">**gluTessEndContour**</span></span>](glutessendcontour.md)
</dt> <dt>

[<span data-ttu-id="50d83-142">**gluTessNormal**</span><span class="sxs-lookup"><span data-stu-id="50d83-142">**gluTessNormal**</span></span>](glutessnormal.md)
</dt> <dt>

[<span data-ttu-id="50d83-143">**gluTessProperty**</span><span class="sxs-lookup"><span data-stu-id="50d83-143">**gluTessProperty**</span></span>](glutessproperty.md)
</dt> </dl>

 

 





