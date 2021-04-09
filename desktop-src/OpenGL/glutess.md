---
title: 'gluTessCallback 函式 (X.glu 隊) '
description: GluTessCallback 函式會定義鑲嵌式物件的回呼。
ms.assetid: a9709919-d34c-42c4-82b8-6a503f2b39b0
keywords:
- gluTessCallback 函式 OpenGL
topic_type:
- apiref
api_name:
- gluTessCallback
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17cdba8b9dd9a3e762a93923a3c353fbc9578377
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934984"
---
# <a name="glutesscallback-function"></a><span data-ttu-id="f3442-104">gluTessCallback 函式</span><span class="sxs-lookup"><span data-stu-id="f3442-104">gluTessCallback function</span></span>

<span data-ttu-id="f3442-105">**GluTessCallback** 函式會定義鑲嵌式物件的回呼。</span><span class="sxs-lookup"><span data-stu-id="f3442-105">The **gluTessCallback** function defines a callback for a tessellation object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3442-106">語法</span><span class="sxs-lookup"><span data-stu-id="f3442-106">Syntax</span></span>


```C++
void WINAPI gluTessCallback(
   GLUtesselator *tess,
   GLenum        which,
   void (CALLBACK *fn)()
);
```



## <a name="parameters"></a><span data-ttu-id="f3442-107">參數</span><span class="sxs-lookup"><span data-stu-id="f3442-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3442-108">*苔 絲*</span><span class="sxs-lookup"><span data-stu-id="f3442-108">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="f3442-109">使用 [**gluNewTess**](glunewtess.md)) 建立的鑲嵌式物件 (。</span><span class="sxs-lookup"><span data-stu-id="f3442-109">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> <dt>

<span data-ttu-id="f3442-110">*頻率*</span><span class="sxs-lookup"><span data-stu-id="f3442-110">*which*</span></span> 
</dt> <dd>

<span data-ttu-id="f3442-111">要定義的回呼。</span><span class="sxs-lookup"><span data-stu-id="f3442-111">The callback being defined.</span></span> <span data-ttu-id="f3442-112">下列值有效： X.GLU 隊 \_ TESS \_ BEGIN、X.glu 隊 \_ TESS \_ begin \_ DATA、x.glu 隊 \_ TESS \_ edge 旗標 \_ 、X.glu 隊 \_ TESS \_ edge 旗 \_ 標 \_ 資料、x.glu 隊 \_ TESS \_ 頂點、x.glu 隊 TESS 頂點資料、x.glu 隊 TESS END、x.glu 隊 TESS 端點 \_ 資料 \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ 、x.glu 隊 TESS、x.glu 隊 TESS、x.glu 隊 TESS、x.glu 隊 TESS、、data、error 和 error DATA。</span><span class="sxs-lookup"><span data-stu-id="f3442-112">The following values are valid: GLU\_TESS\_BEGIN, GLU\_TESS\_BEGIN\_DATA, GLU\_TESS\_EDGE\_FLAG, GLU\_TESS\_EDGE\_FLAG\_DATA, GLU\_TESS\_VERTEX, GLU\_TESS\_VERTEX\_DATA, GLU\_TESS\_END, GLU\_TESS\_END\_DATA, GLU\_TESS\_COMBINE, GLU\_TESS\_COMBINE\_DATA, GLU\_TESS\_ERROR, and GLU\_TESS\_ERROR\_DATA.</span></span>

<span data-ttu-id="f3442-113">如需這些回呼的詳細資訊，請參閱下列備註一節。</span><span class="sxs-lookup"><span data-stu-id="f3442-113">For more information on these callbacks, see the following Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="f3442-114">*Fn*</span><span class="sxs-lookup"><span data-stu-id="f3442-114">*fn*</span></span> 
</dt> <dd>

<span data-ttu-id="f3442-115">要呼叫的函式。</span><span class="sxs-lookup"><span data-stu-id="f3442-115">The function to be called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3442-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="f3442-116">Return value</span></span>

<span data-ttu-id="f3442-117">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="f3442-117">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3442-118">備註</span><span class="sxs-lookup"><span data-stu-id="f3442-118">Remarks</span></span>

<span data-ttu-id="f3442-119">使用 **gluTessCallback** 來指定鑲嵌式物件所要使用的回呼。</span><span class="sxs-lookup"><span data-stu-id="f3442-119">Use **gluTessCallback** to specify a callback to be used by a tessellation object.</span></span> <span data-ttu-id="f3442-120">如果已定義指定的回呼，則會予以取代。</span><span class="sxs-lookup"><span data-stu-id="f3442-120">If the specified callback is already defined, then it is replaced.</span></span> <span data-ttu-id="f3442-121">如果 *fn* 為 **Null**，則現有的回呼會變成未定義。</span><span class="sxs-lookup"><span data-stu-id="f3442-121">If *fn* is **NULL**, then the existing callback becomes undefined.</span></span>

<span data-ttu-id="f3442-122">鑲嵌式物件會使用這些回呼來描述您指定的多邊形如何細分為三角形。</span><span class="sxs-lookup"><span data-stu-id="f3442-122">The tessellation object uses these callbacks to describe how a polygon that you specify is broken into triangles.</span></span>

<span data-ttu-id="f3442-123">每個回呼都有兩個版本，一個具有可定義的多邊形資料，另一個則沒有。</span><span class="sxs-lookup"><span data-stu-id="f3442-123">There are two versions of each callback, one with polygon data that you can define and one without.</span></span> <span data-ttu-id="f3442-124">如果指定了這兩個版本的特定回呼，將會使用您指定的多邊形資料的回呼。</span><span class="sxs-lookup"><span data-stu-id="f3442-124">If both versions of a particular callback are specified, the callback with the polygon data you specify will be used.</span></span> <span data-ttu-id="f3442-125">[**GluTessBeginPolygon**](glutessbeginpolygon.md)的 *多邊形 \_ 資料* 參數是在呼叫 **gluTessBeginPolygon** 時所指定之指標的複本。</span><span class="sxs-lookup"><span data-stu-id="f3442-125">The *polygon\_data* parameter of [**gluTessBeginPolygon**](glutessbeginpolygon.md) is a copy of the pointer that was specified when **gluTessBeginPolygon** was called.</span></span>

<span data-ttu-id="f3442-126">以下是有效的回呼：</span><span class="sxs-lookup"><span data-stu-id="f3442-126">The following are valid callbacks:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f3442-127">回呼</span><span class="sxs-lookup"><span data-stu-id="f3442-127">Callback</span></span></th>
<th><span data-ttu-id="f3442-128">Description</span><span class="sxs-lookup"><span data-stu-id="f3442-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f3442-129">GLU_TESS_BEGIN</span><span class="sxs-lookup"><span data-stu-id="f3442-129">GLU_TESS_BEGIN</span></span></td>
<td><span data-ttu-id="f3442-130">GLU_TESS_BEGIN 回呼會以 <a href="glbegin.md"><strong>glBegin</strong></a> 的方式叫用，以指出 (三角形) 基本的開頭。</span><span class="sxs-lookup"><span data-stu-id="f3442-130">The GLU_TESS_BEGIN callback is invoked like <a href="glbegin.md"><strong>glBegin</strong></a> to indicate the start of a (triangle) primitive.</span></span> <span data-ttu-id="f3442-131">函數會採用 <strong>GLenum</strong>類型的單一引數。</span><span class="sxs-lookup"><span data-stu-id="f3442-131">The function takes a single argument of type <strong>GLenum</strong>.</span></span> <span data-ttu-id="f3442-132">如果您將 GLU_TESS_BOUNDARY_ONLY 屬性設定為 GL_FALSE，則引數會設定為 GL_TRIANGLE_FAN、GL_TRIANGLE_STRIP 或 GL_TRIANGLES。</span><span class="sxs-lookup"><span data-stu-id="f3442-132">If you set the GLU_TESS_BOUNDARY_ONLY property to GL_FALSE, the argument is set to either GL_TRIANGLE_FAN, GL_TRIANGLE_STRIP, or GL_TRIANGLES.</span></span> <span data-ttu-id="f3442-133">如果您將 GLU_TESS_BOUNDARY_ONLY 屬性設定為 GL_TRUE，則引數會設定為 GL_LINE_LOOP。</span><span class="sxs-lookup"><span data-stu-id="f3442-133">If you set the GLU_TESS_BOUNDARY_ONLY property to GL_TRUE, the argument is set to GL_LINE_LOOP.</span></span> <span data-ttu-id="f3442-134">此回呼的函式原型如下： <strong>void</strong> <strong>begin</strong> (<strong>GLenum</strong> <em>類型</em>) ;</span><span class="sxs-lookup"><span data-stu-id="f3442-134">The function prototype for this callback is as follows: <strong>void</strong> <strong>begin</strong> (<strong>GLenum</strong> <em>type</em>);</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f3442-135">GLU_TESS_BEGIN_DATA</span><span class="sxs-lookup"><span data-stu-id="f3442-135">GLU_TESS_BEGIN_DATA</span></span></td>
<td><span data-ttu-id="f3442-136">GLU_TESS_BEGIN_DATA 與 GLU_TESS_BEGIN 回呼相同，不同之處在于它會接受額外的指標引數。</span><span class="sxs-lookup"><span data-stu-id="f3442-136">GLU_TESS_BEGIN_DATA is the same as the GLU_TESS_BEGIN callback except that it takes an additional pointer argument.</span></span> <span data-ttu-id="f3442-137">這個指標等同于呼叫 <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>時所提供的不透明指標。</span><span class="sxs-lookup"><span data-stu-id="f3442-137">This pointer is identical to the opaque pointer provided when you call <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>.</span></span> <span data-ttu-id="f3442-138">此回呼的函式原型是： <strong>void</strong> <strong>beginData</strong> (<strong>GLenum</strong> <em>type</em>、 <strong>void</strong> \* <em>polygon_data</em>) ;</span><span class="sxs-lookup"><span data-stu-id="f3442-138">The function prototype for this callback is: <strong>void</strong> <strong>beginData</strong> (<strong>GLenum</strong> <em>type</em>, <strong>void</strong> \* <em>polygon_data</em>);</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f3442-139">GLU_TESS_EDGE_FLAG</span><span class="sxs-lookup"><span data-stu-id="f3442-139">GLU_TESS_EDGE_FLAG</span></span></td>
<td><span data-ttu-id="f3442-140">GLU_TESS_EDGE_FLAG 回呼類似于 <a href="gledgeflag-functions.md"><strong>glEdgeFlag</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="f3442-140">The GLU_TESS_EDGE_FLAG callback is similar to <a href="gledgeflag-functions.md"><strong>glEdgeFlag</strong></a>.</span></span> <span data-ttu-id="f3442-141">此函式會採用單一布林值旗標，指出哪些邊緣位於多邊形界限上。</span><span class="sxs-lookup"><span data-stu-id="f3442-141">The function takes a single Boolean flag that indicates which edges lie on the polygon boundary.</span></span> <span data-ttu-id="f3442-142">如果 GL_TRUE 旗標，則接下來的每個頂點會開始位於多邊形界限上的邊緣;也就是將內部區域與外部區域分隔開來的邊緣。</span><span class="sxs-lookup"><span data-stu-id="f3442-142">If the flag is GL_TRUE, then each vertex that follows begins an edge that lies on the polygon boundary; that is, an edge which separates an interior region from an exterior one.</span></span> <span data-ttu-id="f3442-143">如果 GL_FALSE 旗標，則接下來的每個頂點會開始位於多邊形內部的邊緣。</span><span class="sxs-lookup"><span data-stu-id="f3442-143">If the flag is GL_FALSE, then each vertex that follows begins an edge that lies in the polygon interior.</span></span> <span data-ttu-id="f3442-144">如果在執行第一個頂點回呼之前叫用了定義的) ，則會叫用 GLU_TESS_EDGE_FLAG 回呼 (。</span><span class="sxs-lookup"><span data-stu-id="f3442-144">The GLU_TESS_EDGE_FLAG callback (if defined) is invoked before the first vertex callback is made.</span></span> <span data-ttu-id="f3442-145">因為三角形風扇和三角形的條紋不支援邊緣旗標，所以不會使用 GL_TRIANGLE_FAN 來呼叫 begin 回呼，或在提供邊緣旗標回呼時 GL_TRIANGLE_STRIP。</span><span class="sxs-lookup"><span data-stu-id="f3442-145">Because triangle fans and triangle strips do not support edge flags, the begin callback is not called with GL_TRIANGLE_FAN or GL_TRIANGLE_STRIP if an edge flag callback is provided.</span></span> <span data-ttu-id="f3442-146">相反地，風扇和條紋會轉換成獨立的三角形。</span><span class="sxs-lookup"><span data-stu-id="f3442-146">Instead, the fans and strips are converted to independent triangles.</span></span> <span data-ttu-id="f3442-147">此回呼的函數原型為：</span><span class="sxs-lookup"><span data-stu-id="f3442-147">The function prototype for this callback is:</span></span><br/> <span data-ttu-id="f3442-148"><strong>void</strong> <strong>edgeFlag</strong> (<strong>GLboolean</strong> <em>旗</em> 標) ;</span><span class="sxs-lookup"><span data-stu-id="f3442-148"><strong>void</strong> <strong>edgeFlag</strong> (<strong>GLboolean</strong> <em>flag</em>);</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f3442-149">GLU_TESS_EDGE_FLAG_DATA</span><span class="sxs-lookup"><span data-stu-id="f3442-149">GLU_TESS_EDGE_FLAG_DATA</span></span></td>
<td><span data-ttu-id="f3442-150">GLU_TESS_EDGE_FLAG_DATA 回呼與 GLU_TESS_EDGE_FLAG 回呼相同，不同之處在于它會接受額外的指標引數。</span><span class="sxs-lookup"><span data-stu-id="f3442-150">The GLU_TESS_EDGE_FLAG_DATA callback is the same as the GLU_TESS_EDGE_FLAG callback except that it takes an additional pointer argument.</span></span> <span data-ttu-id="f3442-151">這個指標等同于呼叫 <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>時所提供的不透明指標。</span><span class="sxs-lookup"><span data-stu-id="f3442-151">This pointer is identical to the opaque pointer provided when you call <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>.</span></span> <span data-ttu-id="f3442-152">此回呼的函式原型是： <strong>void</strong> <strong>edgeFlagData</strong> (<strong>GLboolean</strong> <em>旗</em>標、 <strong>void</strong> \* <em>polygon_data</em>) ;</span><span class="sxs-lookup"><span data-stu-id="f3442-152">The function prototype for this callback is: <strong>void</strong> <strong>edgeFlagData</strong> (<strong>GLboolean</strong> <em>flag</em>, <strong>void</strong> \* <em>polygon_data</em>);</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f3442-153">GLU_TESS_VERTEX</span><span class="sxs-lookup"><span data-stu-id="f3442-153">GLU_TESS_VERTEX</span></span></td>
<td><span data-ttu-id="f3442-154">GLU_TESS_VERTEX 回呼是在 begin 和 end 回呼之間叫用。</span><span class="sxs-lookup"><span data-stu-id="f3442-154">The GLU_TESS_VERTEX callback is invoked between the begin and end callbacks.</span></span> <span data-ttu-id="f3442-155">它類似于 glVertex，它會定義鑲嵌式進程所建立之三角形的頂點。</span><span class="sxs-lookup"><span data-stu-id="f3442-155">It is similar to glVertex , and it defines the vertexes of the triangles created by the tessellation process.</span></span> <span data-ttu-id="f3442-156">函式會接受指標作為其唯一的引數。</span><span class="sxs-lookup"><span data-stu-id="f3442-156">The function takes a pointer as its only argument.</span></span> <span data-ttu-id="f3442-157">此指標與您定義頂點時所提供的不透明指標相同 (請參閱 <a href="glutessvertex.md"><strong>gluTessVertex</strong></a>) 。</span><span class="sxs-lookup"><span data-stu-id="f3442-157">This pointer is identical to the opaque pointer that you provided when you defined the vertex (see <a href="glutessvertex.md"><strong>gluTessVertex</strong></a>).</span></span> <span data-ttu-id="f3442-158">此回呼的函數原型是： <strong>void</strong> <strong>頂點</strong> (<strong>void</strong> \* <em>vertex_data</em>) ;</span><span class="sxs-lookup"><span data-stu-id="f3442-158">The function prototype for this callback is: <strong>void</strong> <strong>vertex</strong> (<strong>void</strong> \* <em>vertex_data</em>);</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f3442-159">GLU_TESS_VERTEX_DATA</span><span class="sxs-lookup"><span data-stu-id="f3442-159">GLU_TESS_VERTEX_DATA</span></span></td>
<td><span data-ttu-id="f3442-160">GLU_TESS_VERTEX_DATA 與 GLU_TESS_VERTEX 回呼相同，不同之處在于它會接受額外的指標引數。</span><span class="sxs-lookup"><span data-stu-id="f3442-160">The GLU_TESS_VERTEX_DATA is the same as the GLU_TESS_VERTEX callback except that it takes an additional pointer argument.</span></span> <span data-ttu-id="f3442-161">這個指標等同于呼叫 <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>時所提供的不透明指標。</span><span class="sxs-lookup"><span data-stu-id="f3442-161">This pointer is identical to the opaque pointer provided when you call <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>.</span></span> <span data-ttu-id="f3442-162">此回呼的函式原型是： <strong>void</strong>  <strong>vertexData</strong> (void \* <em>vertex_data</em>， <strong>void</strong> \* <em>polygon_data</em>) ;</span><span class="sxs-lookup"><span data-stu-id="f3442-162">The function prototype for this callback is: <strong>void</strong>  <strong>vertexData</strong> (void \* <em>vertex_data</em>, <strong>void</strong> \* <em>polygon_data</em>);</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f3442-163">GLU_TESS_END</span><span class="sxs-lookup"><span data-stu-id="f3442-163">GLU_TESS_END</span></span></td>
<td><span data-ttu-id="f3442-164">GLU_TESS_END 回呼的作用與 <a href="glend.md"><strong>glEnd</strong></a>相同。</span><span class="sxs-lookup"><span data-stu-id="f3442-164">The GLU_TESS_END callback serves the same purpose as <a href="glend.md"><strong>glEnd</strong></a>.</span></span> <span data-ttu-id="f3442-165">它會指出基本的結尾，且不會使用任何引數。</span><span class="sxs-lookup"><span data-stu-id="f3442-165">It indicates the end of a primitive, and it takes no arguments.</span></span> <span data-ttu-id="f3442-166">此回呼的函數原型是： <strong>void</strong> <strong>end</strong> (<strong>void</strong>) ;</span><span class="sxs-lookup"><span data-stu-id="f3442-166">The function prototype for this callback is: <strong>void</strong> <strong>end</strong> (<strong>void</strong>);</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f3442-167">GLU_TESS_END_DATA</span><span class="sxs-lookup"><span data-stu-id="f3442-167">GLU_TESS_END_DATA</span></span></td>
<td><span data-ttu-id="f3442-168">GLU_TESS_END_DATA 回呼與 GLU_TESS_END 回呼相同，不同之處在于它會接受額外的指標引數。</span><span class="sxs-lookup"><span data-stu-id="f3442-168">The GLU_TESS_END_DATA callback is the same as the GLU_TESS_END callback except that it takes an additional pointer argument.</span></span> <span data-ttu-id="f3442-169">這個指標等同于呼叫 <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>時所提供的不透明指標。</span><span class="sxs-lookup"><span data-stu-id="f3442-169">This pointer is identical to the opaque pointer provided when you call <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>.</span></span> <span data-ttu-id="f3442-170">此回呼的函數原型是： <strong>void</strong> <strong>endData</strong> (<strong>void</strong> \* <em>polygon_data</em>) ;</span><span class="sxs-lookup"><span data-stu-id="f3442-170">The function prototype for this callback is: <strong>void</strong> <strong>endData</strong> (<strong>void</strong> \* <em>polygon_data</em>);</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f3442-171">GLU_TESS_COMBINE</span><span class="sxs-lookup"><span data-stu-id="f3442-171">GLU_TESS_COMBINE</span></span></td>
<td><span data-ttu-id="f3442-172">呼叫 GLU_TESS_COMBINE 回呼，以在鑲嵌偵測到交集或合併功能時，建立新頂點。</span><span class="sxs-lookup"><span data-stu-id="f3442-172">Call the GLU_TESS_COMBINE callback to create a new vertex when the tessellation detects an intersection, or to merge features.</span></span> <span data-ttu-id="f3442-173">此函式會採用四個引數：三個元素的陣列，每個元素都是 Gldouble 類型。</span><span class="sxs-lookup"><span data-stu-id="f3442-173">The function takes four arguments: An array of three elements, each of type Gldouble.</span></span><br/> <span data-ttu-id="f3442-174">四個指標的陣列。</span><span class="sxs-lookup"><span data-stu-id="f3442-174">An array of four pointers.</span></span><br/> <span data-ttu-id="f3442-175">四個元素的陣列，每個專案都是 GLfloat 類型。</span><span class="sxs-lookup"><span data-stu-id="f3442-175">An array of four elements, each of type GLfloat.</span></span><br/> <span data-ttu-id="f3442-176">指標的指標。</span><span class="sxs-lookup"><span data-stu-id="f3442-176">A pointer to a pointer.</span></span><br/> <span data-ttu-id="f3442-177">此回呼的函數原型為：</span><span class="sxs-lookup"><span data-stu-id="f3442-177">The function prototype for this callback is:</span></span> <br/> <span data-ttu-id="f3442-178"><strong>void</strong> <strong>結合</strong> (<strong>GLdouble</strong> <em>coords</em>[3]、 <strong>void</strong> \* <em>vertex_data</em>[4]、 <strong>GLfloat</strong> <em>權數</em>[4]、 <strong>void</strong>  \*\* <em>outData</em>) ;</span><span class="sxs-lookup"><span data-stu-id="f3442-178"><strong>void</strong> <strong>combine</strong>(<strong>GLdouble</strong> <em>coords</em>[3], <strong>void</strong> \* <em>vertex_data</em>[4], <strong>GLfloat</strong> <em>weight</em>[4], <strong>void</strong> \*\*<em>outData</em>);</span></span><br/> <span data-ttu-id="f3442-179">頂點定義為最多四個現有頂點的線性組合，儲存在 vertex_data 中。</span><span class="sxs-lookup"><span data-stu-id="f3442-179">The vertex is defined as a linear combination of up to four existing vertexes, stored in vertex_data.</span></span> <span data-ttu-id="f3442-180">線性組合的係數是依權數提供;這些權數一律會加總為1.0。</span><span class="sxs-lookup"><span data-stu-id="f3442-180">The coefficients of the linear combination are given by weight; these weights always sum to 1.0.</span></span> <span data-ttu-id="f3442-181">即使部分權數為零，所有頂點指標都是有效的。</span><span class="sxs-lookup"><span data-stu-id="f3442-181">All vertex pointers are valid even when some of the weights are zero.</span></span> <span data-ttu-id="f3442-182">Coords 參數會提供新頂點的位置。</span><span class="sxs-lookup"><span data-stu-id="f3442-182">The coords parameter gives the location of the new vertex.</span></span><br/> <span data-ttu-id="f3442-183">配置另一個頂點、使用 vertex_data 和權數來插入參數，並傳回 outData 中的新頂點指標。</span><span class="sxs-lookup"><span data-stu-id="f3442-183">Allocate another vertex, interpolate parameters using vertex_data and weight, and return the new vertex pointer in outData.</span></span> <span data-ttu-id="f3442-184">這個控制碼是在轉譯回呼期間提供。</span><span class="sxs-lookup"><span data-stu-id="f3442-184">This handle is supplied during rendering callbacks.</span></span> <span data-ttu-id="f3442-185">在呼叫 <a href="glutessendpolygon.md"><strong>gluTessEndPolygon</strong></a>之後釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="f3442-185">Free the memory sometime after calling <a href="glutessendpolygon.md"><strong>gluTessEndPolygon</strong></a>.</span></span><br/> <span data-ttu-id="f3442-186">例如，如果多邊形位於立體空間的任意平面中，而您將色彩與每個頂點建立關聯，GLU_TESS_COMBINE 回呼看起來可能如下所示：</span><span class="sxs-lookup"><span data-stu-id="f3442-186">For example, if the polygon lies in an arbitrary plane in three-dimensional space, and you associate a color with each vertex, the GLU_TESS_COMBINE callback might look like the following:</span></span><br/>
<pre data-space="preserve"><code>void myCombine( GLdouble coords[3], VERTEX *d[4], 
                GLfloat w[4], VERTEX **dataOut ) 
{ 
    VERTEX *newVertex = new_vertex(); 
    newVertex->x = coords[0]; 
    newVertex->y = coords[1]; 
    newVertex->z = coords[2]; 
    newVertex->r = w[0]*d[0]->r + w[1]*d[1]->r + w[2]*d[2]->r + 
                   w[3]*d[3]->r; 
    newVertex->g = w[0]*d[0]->g + w[1]*d[1]->g + w[2]*d[2]->g + 
                   w[3]*d[3]->g; 
    newVertex->b = w[0]*d[0]->b + w[1]*d[1]->b + w[2]*d[2]->b + 
                   w[3]*d[3]->b; 
    newVertex->a = w[0]*d[0]->a + w[1]*d[1]->a + w[2]*d[2]->a + 
                   w[3]*d[3]->a; 
    *dataOut = newVertex; 
}</code></pre>
<span data-ttu-id="f3442-187">當鑲嵌偵測到交集時，GLU_TESS_COMBINE 或 GLU_TESS_COMBINE_DATA 回呼 (請參閱以下) 必須定義，而且必須將非<strong>Null</strong> 指標寫入 dataOut。</span><span class="sxs-lookup"><span data-stu-id="f3442-187">When the tessellation detects an intersection, the GLU_TESS_COMBINE or GLU_TESS_COMBINE_DATA callback (see below) must be defined, and must write a non-<strong>NULL</strong> pointer into dataOut.</span></span> <span data-ttu-id="f3442-188">否則會發生 GLU_TESS_NEED_COMBINE_CALLBACK 錯誤，而且不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="f3442-188">Otherwise the GLU_TESS_NEED_COMBINE_CALLBACK error occurs, and no output is generated.</span></span> <span data-ttu-id="f3442-189"> (這是鑲嵌和轉譯期間唯一可能發生的錯誤。 ) </span><span class="sxs-lookup"><span data-stu-id="f3442-189">(This is the only error that can occur during tessellation and rendering.)</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f3442-190">GLU_TESS_COMBINE_DATA</span><span class="sxs-lookup"><span data-stu-id="f3442-190">GLU_TESS_COMBINE_DATA</span></span></td>
<td><span data-ttu-id="f3442-191">GLU_TESS_COMBINE_DATA 回呼與 GLU_TESS_COMBINE 回呼相同，不同之處在于它會接受額外的指標引數。</span><span class="sxs-lookup"><span data-stu-id="f3442-191">The GLU_TESS_COMBINE_DATA callback is the same as the GLU_TESS_COMBINE callback except that it takes an additional pointer argument.</span></span> <span data-ttu-id="f3442-192">這個指標等同于呼叫 <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>時所提供的不透明指標。</span><span class="sxs-lookup"><span data-stu-id="f3442-192">This pointer is identical to the opaque pointer provided when you call <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>.</span></span> <span data-ttu-id="f3442-193">此回呼的函式原型為： <strong>void</strong> <strong>combineData</strong> (<strong>GLdouble</strong> <em>coords</em>[3]、 <strong>void</strong> \*<em>vertex_data</em>[4]、 <strong>GLfloat</strong> <em>權數</em>[4]、 <strong>void</strong>  \*\* <em>outData</em>、 <strong>void</strong> \* <em>polygon_data</em>) ;</span><span class="sxs-lookup"><span data-stu-id="f3442-193">The function prototype for this callback is: <strong>void</strong> <strong>combineData</strong> (<strong>GLdouble</strong> <em>coords</em>[3], <strong>void</strong> \*<em>vertex_data</em>[4], <strong>GLfloat</strong> <em>weight</em>[4], <strong>void</strong> \*\*<em>outData</em>, <strong>void</strong> \* <em>polygon_data</em>);</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f3442-194">GLU_TESS_ERROR</span><span class="sxs-lookup"><span data-stu-id="f3442-194">GLU_TESS_ERROR</span></span></td>
<td><span data-ttu-id="f3442-195">遇到錯誤時，會呼叫 GLU_TESS_ERROR 回呼。</span><span class="sxs-lookup"><span data-stu-id="f3442-195">The GLU_TESS_ERROR callback is called when an error is encountered.</span></span> <span data-ttu-id="f3442-196">其中一個引數的類型為 <strong>GLenum</strong>;它會指出發生的特定錯誤，並設定為下列其中一項： GLU_TESS_MISSING_BEGIN_POLYGON</span><span class="sxs-lookup"><span data-stu-id="f3442-196">The one argument is of type <strong>GLenum</strong>; it indicates the specific error that occurred and is set to one of the following: GLU_TESS_MISSING_BEGIN_POLYGON</span></span><br/> <span data-ttu-id="f3442-197">GLU_TESS_MISSING_END_POLYGON</span><span class="sxs-lookup"><span data-stu-id="f3442-197">GLU_TESS_MISSING_END_POLYGON</span></span><br/> <span data-ttu-id="f3442-198">GLU_TESS_MISSING_BEGIN_CONTOUR</span><span class="sxs-lookup"><span data-stu-id="f3442-198">GLU_TESS_MISSING_BEGIN_CONTOUR</span></span><br/> <span data-ttu-id="f3442-199">GLU_TESS_MISSING_END_CONTOUR</span><span class="sxs-lookup"><span data-stu-id="f3442-199">GLU_TESS_MISSING_END_CONTOUR</span></span><br/> <span data-ttu-id="f3442-200">GLU_TESS_COORD_TOO_LARGE</span><span class="sxs-lookup"><span data-stu-id="f3442-200">GLU_TESS_COORD_TOO_LARGE</span></span><br/> <span data-ttu-id="f3442-201">GLU_TESS_NEED_COMBINE_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="f3442-201">GLU_TESS_NEED_COMBINE_CALLBACK</span></span><br/> <span data-ttu-id="f3442-202">呼叫 gluErrorString 來取出描述這些錯誤的字元字串。</span><span class="sxs-lookup"><span data-stu-id="f3442-202">Call gluErrorString to retrieve character strings describing these errors.</span></span> <span data-ttu-id="f3442-203">此回呼的函數原型如下所示：</span><span class="sxs-lookup"><span data-stu-id="f3442-203">The function prototype for this callback is as follows:</span></span><br/> <span data-ttu-id="f3442-204"><strong>void</strong> <strong>錯誤</strong> (<strong>GLenum</strong> <em>errno</em>) ;</span><span class="sxs-lookup"><span data-stu-id="f3442-204"><strong>void</strong> <strong>error</strong> (<strong>GLenum</strong> <em>errno</em>);</span></span><br/> <span data-ttu-id="f3442-205">X.GLU 隊程式庫會藉由插入遺失的呼叫，從前四個錯誤中復原。</span><span class="sxs-lookup"><span data-stu-id="f3442-205">The GLU library recovers from the first four errors by inserting the missing call or calls.</span></span> <span data-ttu-id="f3442-206">GLU_TESS_COORD_TOO_LARGE 表示某些頂點座標超過預先定義的常數 GLU_TESS_MAX_COORD 絕對值，且已壓制該值。</span><span class="sxs-lookup"><span data-stu-id="f3442-206">GLU_TESS_COORD_TOO_LARGE indicates that some vertex coordinate exceeded the predefined constant GLU_TESS_MAX_COORD in absolute value, and that the value has been clamped.</span></span> <span data-ttu-id="f3442-207"> (座標值必須夠小，才能將兩個值相乘，而不會發生溢位。 ) GLU_TESS_NEED_COMBINE_CALLBACK 表示鑲嵌偵測到輸入資料中有兩個邊緣之間的交集，但未提供 GLU_TESS_COMBINE 或 GLU_TESS_COMBINE_DATA 回呼。</span><span class="sxs-lookup"><span data-stu-id="f3442-207">(Coordinate values must be small enough that two can be multiplied together without overflow.) GLU_TESS_NEED_COMBINE_CALLBACK indicates that the tessellation detected an intersection between two edges in the input data, and the GLU_TESS_COMBINE or GLU_TESS_COMBINE_DATA callback was not provided.</span></span> <span data-ttu-id="f3442-208">不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="f3442-208">No output will be generated.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f3442-209">GLU_TESS_ERROR_DATA</span><span class="sxs-lookup"><span data-stu-id="f3442-209">GLU_TESS_ERROR_DATA</span></span></td>
<td><span data-ttu-id="f3442-210">GLU_TESS_ERROR_DATA 回呼與 GLU_TESS_ERROR 回呼相同，不同之處在于它會接受額外的指標引數。</span><span class="sxs-lookup"><span data-stu-id="f3442-210">The GLU_TESS_ERROR_DATA callback is the same as the GLU_TESS_ERROR callback, except that it takes an additional pointer argument.</span></span> <span data-ttu-id="f3442-211">這個指標等同于呼叫 <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>時所提供的不透明指標。</span><span class="sxs-lookup"><span data-stu-id="f3442-211">This pointer is identical to the opaque pointer provided when you call <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>.</span></span> <span data-ttu-id="f3442-212">此回呼的函式原型是： <strong>void</strong> <strong>errorData</strong> (<strong>GLenum</strong> <em>errno</em>、 <strong>void</strong> \* <em>polygon_data</em>) ;</span><span class="sxs-lookup"><span data-stu-id="f3442-212">The function prototype for this callback is: <strong>void</strong> <strong>errorData</strong> (<strong>GLenum</strong> <em>errno</em>, <strong>void</strong> \* <em>polygon_data</em>);</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="f3442-213">規格需求</span><span class="sxs-lookup"><span data-stu-id="f3442-213">Requirements</span></span>



| <span data-ttu-id="f3442-214">需求</span><span class="sxs-lookup"><span data-stu-id="f3442-214">Requirement</span></span> | <span data-ttu-id="f3442-215">值</span><span class="sxs-lookup"><span data-stu-id="f3442-215">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f3442-216">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f3442-216">Minimum supported client</span></span><br/> | <span data-ttu-id="f3442-217">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f3442-217">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="f3442-218">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f3442-218">Minimum supported server</span></span><br/> | <span data-ttu-id="f3442-219">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f3442-219">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f3442-220">標頭</span><span class="sxs-lookup"><span data-stu-id="f3442-220">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3442-221"><dt>X.glu 隊。h</dt></span><span class="sxs-lookup"><span data-stu-id="f3442-221"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="f3442-222">程式庫</span><span class="sxs-lookup"><span data-stu-id="f3442-222">Library</span></span><br/>                  | <dl> <span data-ttu-id="f3442-223"><dt>Glu32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f3442-223"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="f3442-224">DLL</span><span class="sxs-lookup"><span data-stu-id="f3442-224">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3442-225"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3442-225"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3442-226">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f3442-226">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3442-227">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="f3442-227">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="f3442-228">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="f3442-228">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="f3442-229">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="f3442-229">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="f3442-230">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="f3442-230">**glVertex**</span></span>](glvertex-functions.md)
</dt> <dt>

[<span data-ttu-id="f3442-231">**gluDeleteTess**</span><span class="sxs-lookup"><span data-stu-id="f3442-231">**gluDeleteTess**</span></span>](gludeletetess.md)
</dt> <dt>

[<span data-ttu-id="f3442-232">**gluErrorString**</span><span class="sxs-lookup"><span data-stu-id="f3442-232">**gluErrorString**</span></span>](gluerrorstring.md)
</dt> <dt>

[<span data-ttu-id="f3442-233">**gluNewTess**</span><span class="sxs-lookup"><span data-stu-id="f3442-233">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="f3442-234">**gluTessBeginPolygon**</span><span class="sxs-lookup"><span data-stu-id="f3442-234">**gluTessBeginPolygon**</span></span>](glutessbeginpolygon.md)
</dt> <dt>

[<span data-ttu-id="f3442-235">**gluTessEndPolygon**</span><span class="sxs-lookup"><span data-stu-id="f3442-235">**gluTessEndPolygon**</span></span>](glutessendpolygon.md)
</dt> <dt>

[<span data-ttu-id="f3442-236">**gluTessVertex**</span><span class="sxs-lookup"><span data-stu-id="f3442-236">**gluTessVertex**</span></span>](glutessvertex.md)
</dt> </dl>

 

 





