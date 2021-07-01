---
title: Geometry-Shader 物件
description: 幾何著色器物件會處理整個基本專案。 使用下列語法來宣告幾何著色器物件。
ms.assetid: d5c1c22b-6fa6-40a8-900f-6d74f74468c1
keywords:
- 'maxvertexcount (DirectX HLSL) '
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e06bbc184a4b5f82d5edaaf7fdbfbd55f1906f12
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120613"
---
# <a name="geometry-shader-object"></a><span data-ttu-id="e8fb8-105">Geometry-Shader 物件</span><span class="sxs-lookup"><span data-stu-id="e8fb8-105">Geometry-Shader Object</span></span>

<span data-ttu-id="e8fb8-106">幾何著色器物件會處理整個基本專案。</span><span class="sxs-lookup"><span data-stu-id="e8fb8-106">A geometry-shader object processes entire primitives.</span></span> <span data-ttu-id="e8fb8-107">使用下列語法來宣告幾何著色器物件。</span><span class="sxs-lookup"><span data-stu-id="e8fb8-107">Use the following syntax to declare a geometry-shader object.</span></span>

<span data-ttu-id="e8fb8-108">\[maxvertexcount (*NumVerts*) \] Void *ShaderName* ( *PrimitiveType DataType Name \[ NumElements \]*，inout *StreamOutputObject* ) ;</span><span class="sxs-lookup"><span data-stu-id="e8fb8-108">\[maxvertexcount(*NumVerts*)\] void *ShaderName* (   *PrimitiveType DataType Name \[ NumElements \]*,   inout *StreamOutputObject*  );</span></span>



 

## <a name="parameters"></a><span data-ttu-id="e8fb8-109">參數</span><span class="sxs-lookup"><span data-stu-id="e8fb8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8fb8-110"><span id="_maxvertexcount_NumVerts__"></span><span id="_maxvertexcount_numverts__"></span><span id="_MAXVERTEXCOUNT_NUMVERTS__"></span>\[maxvertexcount (*NumVerts*) \]</span><span class="sxs-lookup"><span data-stu-id="e8fb8-110"><span id="_maxvertexcount_NumVerts__"></span><span id="_maxvertexcount_numverts__"></span><span id="_MAXVERTEXCOUNT_NUMVERTS__"></span>\[maxvertexcount(*NumVerts*)\]</span></span>
</dt> <dd>

<span data-ttu-id="e8fb8-111">\[\]表示要建立的最大頂點數目。</span><span class="sxs-lookup"><span data-stu-id="e8fb8-111">\[in\] Declaration for the maximum number of vertices to create.</span></span>

-   <span data-ttu-id="e8fb8-112">\[maxvertexcount () \] 必要關鍵字; 括弧和括弧是正確語法的必要字元。</span><span class="sxs-lookup"><span data-stu-id="e8fb8-112">\[maxvertexcount()\] - required keyword; brackets and parenthesis are required characters for correct syntax.</span></span>
-   <span data-ttu-id="e8fb8-113">*NumVerts* -代表頂點數目的整數數位。</span><span class="sxs-lookup"><span data-stu-id="e8fb8-113">*NumVerts* - An integer number representing the number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="e8fb8-114"><span id="ShaderName"></span><span id="shadername"></span><span id="SHADERNAME"></span>*ShaderName*</span><span class="sxs-lookup"><span data-stu-id="e8fb8-114"><span id="ShaderName"></span><span id="shadername"></span><span id="SHADERNAME"></span>*ShaderName*</span></span>
</dt> <dd>

<span data-ttu-id="e8fb8-115">\[\]包含幾何著色器函式唯一名稱的 ASCII 字串。</span><span class="sxs-lookup"><span data-stu-id="e8fb8-115">\[in\] An ASCII string that contains a unique name for the geometry-shader function.</span></span>

</dd> <dt>

<span data-ttu-id="e8fb8-116"><span id="PrimitiveType_DataType_Name___NumElements__"></span><span id="primitivetype_datatype_name___numelements__"></span><span id="PRIMITIVETYPE_DATATYPE_NAME___NUMELEMENTS__"></span>*PrimitiveType DataType Name \[ NumElements \]*</span><span class="sxs-lookup"><span data-stu-id="e8fb8-116"><span id="PrimitiveType_DataType_Name___NumElements__"></span><span id="primitivetype_datatype_name___numelements__"></span><span id="PRIMITIVETYPE_DATATYPE_NAME___NUMELEMENTS__"></span>*PrimitiveType DataType Name \[ NumElements \]*</span></span>
</dt> <dd>

<span data-ttu-id="e8fb8-117">*PrimitiveType* -基本型別，決定基本資料的順序。</span><span class="sxs-lookup"><span data-stu-id="e8fb8-117">*PrimitiveType* - Primitive type, which determines the order of the primitive data.</span></span>



| <span data-ttu-id="e8fb8-118">基本類型</span><span class="sxs-lookup"><span data-stu-id="e8fb8-118">Primitive Type</span></span> | <span data-ttu-id="e8fb8-119">描述</span><span class="sxs-lookup"><span data-stu-id="e8fb8-119">Description</span></span>                                                   |
|----------------|---------------------------------------------------------------|
| <span data-ttu-id="e8fb8-120">*點*</span><span class="sxs-lookup"><span data-stu-id="e8fb8-120">*point*</span></span>        | <span data-ttu-id="e8fb8-121">點清單</span><span class="sxs-lookup"><span data-stu-id="e8fb8-121">Point list</span></span>                                                    |
| <span data-ttu-id="e8fb8-122">*line*</span><span class="sxs-lookup"><span data-stu-id="e8fb8-122">*line*</span></span>         | <span data-ttu-id="e8fb8-123">行清單或行帶</span><span class="sxs-lookup"><span data-stu-id="e8fb8-123">Line list or line strip</span></span>                                       |
| <span data-ttu-id="e8fb8-124">*三角形*</span><span class="sxs-lookup"><span data-stu-id="e8fb8-124">*triangle*</span></span>     | <span data-ttu-id="e8fb8-125">三角形清單或三角形條紋</span><span class="sxs-lookup"><span data-stu-id="e8fb8-125">Triangle list or triangle strip</span></span>                               |
| <span data-ttu-id="e8fb8-126">*lineadj*</span><span class="sxs-lookup"><span data-stu-id="e8fb8-126">*lineadj*</span></span>      | <span data-ttu-id="e8fb8-127">連續的行清單或具有連續的行帶</span><span class="sxs-lookup"><span data-stu-id="e8fb8-127">Line list with adjacency or line strip with adjacency</span></span>         |
| <span data-ttu-id="e8fb8-128">*triangleadj*</span><span class="sxs-lookup"><span data-stu-id="e8fb8-128">*triangleadj*</span></span>  | <span data-ttu-id="e8fb8-129">具有連續的相鄰或三角形條紋的三角形清單</span><span class="sxs-lookup"><span data-stu-id="e8fb8-129">Triangle list with adjacency or triangle strip with adjacency</span></span> |



 

<span data-ttu-id="e8fb8-130">  -  DataType \[在 \] 輸入資料類型中，可以是任何[HLSL 資料類型](dx-graphics-hlsl-data-types.md)。</span><span class="sxs-lookup"><span data-stu-id="e8fb8-130">*DataType* - \[in\] An input data type; can be any [HLSL data type](dx-graphics-hlsl-data-types.md).</span></span>

<span data-ttu-id="e8fb8-131">*名稱* -引數名稱;這是 ASCII 字串。</span><span class="sxs-lookup"><span data-stu-id="e8fb8-131">*Name* - Argument name; this is an ASCII string.</span></span>

<span data-ttu-id="e8fb8-132">*NumElements* -輸入的陣列大小，這取決於下表所示的 *PrimitiveType* 。</span><span class="sxs-lookup"><span data-stu-id="e8fb8-132">*NumElements* - Array size of the input, which depends on the *PrimitiveType* as shown in the following table.</span></span>

| <span data-ttu-id="e8fb8-133">基本類型</span><span class="sxs-lookup"><span data-stu-id="e8fb8-133">Primitive Type</span></span> | <span data-ttu-id="e8fb8-134">NumElements</span><span class="sxs-lookup"><span data-stu-id="e8fb8-134">NumElements</span></span>                                                                                                  |
|----------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8fb8-135">*點*</span><span class="sxs-lookup"><span data-stu-id="e8fb8-135">*point*</span></span>        | <span data-ttu-id="e8fb8-136">\[1\]</span><span class="sxs-lookup"><span data-stu-id="e8fb8-136">\[1\]</span></span><br/> <span data-ttu-id="e8fb8-137">您一次只能在一個點上操作。</span><span class="sxs-lookup"><span data-stu-id="e8fb8-137">You operate on only one point at a time.</span></span><br/>                                         |
| <span data-ttu-id="e8fb8-138">*line*</span><span class="sxs-lookup"><span data-stu-id="e8fb8-138">*line*</span></span>         | <span data-ttu-id="e8fb8-139">\[2\]</span><span class="sxs-lookup"><span data-stu-id="e8fb8-139">\[2\]</span></span><br/> <span data-ttu-id="e8fb8-140">一行需要兩個頂點。</span><span class="sxs-lookup"><span data-stu-id="e8fb8-140">A line requires two vertices.</span></span><br/>                                                    |
| <span data-ttu-id="e8fb8-141">*三角形*</span><span class="sxs-lookup"><span data-stu-id="e8fb8-141">*triangle*</span></span>     | <span data-ttu-id="e8fb8-142">\[3\]</span><span class="sxs-lookup"><span data-stu-id="e8fb8-142">\[3\]</span></span><br/> <span data-ttu-id="e8fb8-143">三角形需要三個頂點。</span><span class="sxs-lookup"><span data-stu-id="e8fb8-143">A triangle requires three vertices.</span></span><br/>                                              |
| <span data-ttu-id="e8fb8-144">*lineadj*</span><span class="sxs-lookup"><span data-stu-id="e8fb8-144">*lineadj*</span></span>      | <span data-ttu-id="e8fb8-145">\[4\]</span><span class="sxs-lookup"><span data-stu-id="e8fb8-145">\[4\]</span></span><br/> <span data-ttu-id="e8fb8-146">Lineadj 有兩個端點：因此，它需要四個頂點。</span><span class="sxs-lookup"><span data-stu-id="e8fb8-146">A lineadj has two ends; therefore, it requires four vertices.</span></span><br/>                    |
| <span data-ttu-id="e8fb8-147">*triangleadj*</span><span class="sxs-lookup"><span data-stu-id="e8fb8-147">*triangleadj*</span></span>  | <span data-ttu-id="e8fb8-148">\[6\]</span><span class="sxs-lookup"><span data-stu-id="e8fb8-148">\[6\]</span></span><br/> <span data-ttu-id="e8fb8-149">Triangleadj 框線三個三角形;因此，它需要六個頂點。</span><span class="sxs-lookup"><span data-stu-id="e8fb8-149">A triangleadj borders three more triangles; therefore, it requires six vertices.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e8fb8-150"><span id="StreamOutputObject"></span><span id="streamoutputobject"></span><span id="STREAMOUTPUTOBJECT"></span>*StreamOutputObject*</span><span class="sxs-lookup"><span data-stu-id="e8fb8-150"><span id="StreamOutputObject"></span><span id="streamoutputobject"></span><span id="STREAMOUTPUTOBJECT"></span>*StreamOutputObject*</span></span>
</dt> <dd>

<span data-ttu-id="e8fb8-151">[資料流程輸出物件](dx-graphics-hlsl-so-type.md)的宣告。</span><span class="sxs-lookup"><span data-stu-id="e8fb8-151">The declaration of the [stream-output object](dx-graphics-hlsl-so-type.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8fb8-152">傳回值</span><span class="sxs-lookup"><span data-stu-id="e8fb8-152">Return Value</span></span>

<span data-ttu-id="e8fb8-153">無</span><span class="sxs-lookup"><span data-stu-id="e8fb8-153">None</span></span>

## <a name="remarks"></a><span data-ttu-id="e8fb8-154">備註</span><span class="sxs-lookup"><span data-stu-id="e8fb8-154">Remarks</span></span>

<span data-ttu-id="e8fb8-155">下圖顯示幾何著色器物件的各種基本類型。</span><span class="sxs-lookup"><span data-stu-id="e8fb8-155">The following diagram shows the various primitive types for a geometry shader object.</span></span>

![幾何著色器物件的各種基本類型圖例](images/d3d11-gsinputs1.png)

<span data-ttu-id="e8fb8-157">下圖顯示幾何著色器調用。</span><span class="sxs-lookup"><span data-stu-id="e8fb8-157">The following diagram shows geometry shader invocations.</span></span>

![幾何著色器調用的圖例](images/d3d11-gsinputs2.png)

## <a name="examples"></a><span data-ttu-id="e8fb8-159">範例</span><span class="sxs-lookup"><span data-stu-id="e8fb8-159">Examples</span></span>

<span data-ttu-id="e8fb8-160">此範例來自 [Direct3D 10 著色器模型4.0 研討會](https://msdn.microsoft.com/library/Ee416554(v=VS.85).aspx)的練習1。</span><span class="sxs-lookup"><span data-stu-id="e8fb8-160">This example is from exercise 1 from the [Direct3D 10 Shader Model 4.0 Workshop](https://msdn.microsoft.com/library/Ee416554(v=VS.85).aspx).</span></span>


```
[maxvertexcount(3)]
void GSScene( triangleadj GSSceneIn input[6], inout TriangleStream<PSSceneIn> OutputStream )
{   
    PSSceneIn output = (PSSceneIn)0;

    for( uint i=0; i<6; i+=2 )
    {
        output.Pos = input[i].Pos;
        output.Norm = input[i].Norm;
        output.Tex = input[i].Tex;
        
        OutputStream.Append( output );
    }
    
    OutputStream.RestartStrip();
}
```



## <a name="minimum-shader-model"></a><span data-ttu-id="e8fb8-161">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="e8fb8-161">Minimum Shader Model</span></span>

<span data-ttu-id="e8fb8-162">下列著色器模型支援此物件。</span><span class="sxs-lookup"><span data-stu-id="e8fb8-162">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="e8fb8-163">著色器模型</span><span class="sxs-lookup"><span data-stu-id="e8fb8-163">Shader Model</span></span>                                                        | <span data-ttu-id="e8fb8-164">支援</span><span class="sxs-lookup"><span data-stu-id="e8fb8-164">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| <span data-ttu-id="e8fb8-165">[著色器模型 4](dx-graphics-hlsl-sm4.md) 和更高的著色器模型</span><span class="sxs-lookup"><span data-stu-id="e8fb8-165">[Shader Model 4](dx-graphics-hlsl-sm4.md) and higher shader models</span></span> | <span data-ttu-id="e8fb8-166">是</span><span class="sxs-lookup"><span data-stu-id="e8fb8-166">yes</span></span>       |



 

## <a name="related-topics"></a><span data-ttu-id="e8fb8-167">相關主題</span><span class="sxs-lookup"><span data-stu-id="e8fb8-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8fb8-168">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="e8fb8-168">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 





