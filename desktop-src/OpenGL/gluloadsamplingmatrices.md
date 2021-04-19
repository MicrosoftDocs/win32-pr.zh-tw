---
title: 'gluLoadSamplingMatrices 函式 (X.glu 隊) '
description: GluLoadSamplingMatrices 函式會載入非統一的有理 B 曲線 (NURBS) 取樣和剔除矩陣。
ms.assetid: 7fdbc4e2-a037-4f07-bb03-e51feea42775
keywords:
- gluLoadSamplingMatrices 函式 OpenGL
topic_type:
- apiref
api_name:
- gluLoadSamplingMatrices
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 293b8bace0dff7d89bfcffa2af33738e0e59de7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106999811"
---
# <a name="gluloadsamplingmatrices-function"></a><span data-ttu-id="89574-104">gluLoadSamplingMatrices 函式</span><span class="sxs-lookup"><span data-stu-id="89574-104">gluLoadSamplingMatrices function</span></span>

<span data-ttu-id="89574-105">**GluLoadSamplingMatrices** 函式會載入非統一的有理 B 曲線 ([NURBS](using-nurbs-curves-and-surfaces.md)) 取樣和剔除矩陣。</span><span class="sxs-lookup"><span data-stu-id="89574-105">The **gluLoadSamplingMatrices** function loads Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) sampling and culling matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="89574-106">語法</span><span class="sxs-lookup"><span data-stu-id="89574-106">Syntax</span></span>


```C++
void WINAPI gluLoadSamplingMatrices(
         GLUnurbs *nobj,
   const GLfloat  modelMatrix[16],
   const GLfloat  projMatrix[16],
   const GLint    viewport[4]
);
```



## <a name="parameters"></a><span data-ttu-id="89574-107">參數</span><span class="sxs-lookup"><span data-stu-id="89574-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89574-108">*nobj*</span><span class="sxs-lookup"><span data-stu-id="89574-108">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="89574-109">使用 [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)) 建立的 NURBS 物件 (。</span><span class="sxs-lookup"><span data-stu-id="89574-109">The NURBS object (created with [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span></span>

</dd> <dt>

<span data-ttu-id="89574-110">*modelMatrix*</span><span class="sxs-lookup"><span data-stu-id="89574-110">*modelMatrix*</span></span> 
</dt> <dd>

<span data-ttu-id="89574-111">模型矩陣 (為 [**glGetFloatv**](glgetfloatv.md) 呼叫) 。</span><span class="sxs-lookup"><span data-stu-id="89574-111">A modelview matrix (as from a [**glGetFloatv**](glgetfloatv.md) call).</span></span>

</dd> <dt>

<span data-ttu-id="89574-112">*projMatrix*</span><span class="sxs-lookup"><span data-stu-id="89574-112">*projMatrix*</span></span> 
</dt> <dd>

<span data-ttu-id="89574-113">投射矩陣 (從 **glGetFloatv** 呼叫) 。</span><span class="sxs-lookup"><span data-stu-id="89574-113">A projection matrix (as from a **glGetFloatv** call).</span></span>

</dd> <dt>

<span data-ttu-id="89574-114">*視窗*</span><span class="sxs-lookup"><span data-stu-id="89574-114">*viewport*</span></span> 
</dt> <dd>

<span data-ttu-id="89574-115">從 [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) 呼叫)  (的區。</span><span class="sxs-lookup"><span data-stu-id="89574-115">A viewport (as from a [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) call).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89574-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="89574-116">Return value</span></span>

<span data-ttu-id="89574-117">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="89574-117">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="89574-118">備註</span><span class="sxs-lookup"><span data-stu-id="89574-118">Remarks</span></span>

<span data-ttu-id="89574-119">**GluLoadSamplingMatrices** 函式會使用 *modelMatrix*、 *projMatrix* 和 *視口* 來重新計算儲存在 *nobj* 中的取樣和剔除矩陣。</span><span class="sxs-lookup"><span data-stu-id="89574-119">The **gluLoadSamplingMatrices** function uses *modelMatrix*, *projMatrix*, and *viewport* to recompute the sampling and culling matrices stored in *nobj*.</span></span> <span data-ttu-id="89574-120">取樣矩陣會決定必須鑲嵌的 NURBS 曲線或表面，以滿足 X.GLU 隊 \_ 取樣容錯屬性) 所決定的取樣 (容錯 \_ 。</span><span class="sxs-lookup"><span data-stu-id="89574-120">The sampling matrix determines how finely a NURBS curve or surface must be tessellated to satisfy the sampling tolerance (as determined by the GLU\_SAMPLING\_TOLERANCE property).</span></span> <span data-ttu-id="89574-121">您可以使用 [剔除] 矩陣來決定是否應該在轉譯 (，然後在) 開啟 [X.GLU 隊剔除] 屬性時，挑選 \_ 。</span><span class="sxs-lookup"><span data-stu-id="89574-121">The culling matrix is used in deciding if a NURBS curve or surface should be culled before rendering (when the GLU\_CULLING property is turned on).</span></span>

<span data-ttu-id="89574-122">只有當 [X.GLU 隊 AUTO LOAD MATRIX] 屬性關閉時，才需要 **gluLoadSamplingMatrices** 函式 \_ \_ \_ (請參閱 [**gluNurbsProperty**](glunurbsproperty.md)) 。</span><span class="sxs-lookup"><span data-stu-id="89574-122">The **gluLoadSamplingMatrices** function is necessary only if the GLU\_AUTO\_LOAD\_MATRIX property is turned off (see [**gluNurbsProperty**](glunurbsproperty.md)).</span></span> <span data-ttu-id="89574-123">雖然讓 X.GLU 隊 \_ AUTO \_ LOAD MATRIX 屬性保持開啟很方便 \_ ，但這麼做會需要往返于 OpenGL 伺服器，才能取得模型矩陣、投影矩陣和視口的目前值。 ) </span><span class="sxs-lookup"><span data-stu-id="89574-123">Although it can be convenient to leave the GLU\_AUTO\_LOAD\_MATRIX property turned on, doing so necessitates a round trip to the OpenGL server to get the current values of the modelview matrix, projection matrix, and viewport.)</span></span>

## <a name="requirements"></a><span data-ttu-id="89574-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="89574-124">Requirements</span></span>



| <span data-ttu-id="89574-125">需求</span><span class="sxs-lookup"><span data-stu-id="89574-125">Requirement</span></span> | <span data-ttu-id="89574-126">值</span><span class="sxs-lookup"><span data-stu-id="89574-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="89574-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="89574-127">Minimum supported client</span></span><br/> | <span data-ttu-id="89574-128">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="89574-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="89574-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="89574-129">Minimum supported server</span></span><br/> | <span data-ttu-id="89574-130">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="89574-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="89574-131">標頭</span><span class="sxs-lookup"><span data-stu-id="89574-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="89574-132"><dt>X.glu 隊。h</dt></span><span class="sxs-lookup"><span data-stu-id="89574-132"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="89574-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="89574-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="89574-134"><dt>Glu32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="89574-134"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="89574-135">DLL</span><span class="sxs-lookup"><span data-stu-id="89574-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89574-136"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89574-136"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89574-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="89574-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89574-138">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="89574-138">**glGetFloatv**</span></span>](glgetfloatv.md)
</dt> <dt>

[<span data-ttu-id="89574-139">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="89574-139">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="89574-140">**gluGetNurbsProperty**</span><span class="sxs-lookup"><span data-stu-id="89574-140">**gluGetNurbsProperty**</span></span>](glugetnurbsproperty.md)
</dt> <dt>

[<span data-ttu-id="89574-141">**gluNewNurbsRenderer**</span><span class="sxs-lookup"><span data-stu-id="89574-141">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> </dl>

 

 





