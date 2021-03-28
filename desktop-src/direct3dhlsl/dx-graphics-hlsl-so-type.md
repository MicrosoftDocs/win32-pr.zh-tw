---
title: Stream-Output 物件
description: 資料流程輸出物件是樣板化物件，可將資料從幾何著色器階段流出。 使用下列語法來宣告資料流程輸出物件。
ms.assetid: 07a5489c-c238-4466-9282-5b168448aff7
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 98063ddb45633dda6c897abf0f82f29a394c3f95
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375620"
---
# <a name="stream-output-object"></a><span data-ttu-id="d2ef3-104">Stream-Output 物件</span><span class="sxs-lookup"><span data-stu-id="d2ef3-104">Stream-Output Object</span></span>

<span data-ttu-id="d2ef3-105">資料流程輸出物件是樣板化物件，可將資料從 [幾何著色器階段](/previous-versions//bb205146(v=vs.85))流出。</span><span class="sxs-lookup"><span data-stu-id="d2ef3-105">A stream-output object is a templated object that streams data out of the [geometry-shader stage](/previous-versions//bb205146(v=vs.85)).</span></span> <span data-ttu-id="d2ef3-106">使用下列語法來宣告資料流程輸出物件。</span><span class="sxs-lookup"><span data-stu-id="d2ef3-106">Use the following syntax to declare a stream-output object.</span></span>



| <span data-ttu-id="d2ef3-107">inout *StreamOutputObject* < *資料類型* >  *名稱;*</span><span class="sxs-lookup"><span data-stu-id="d2ef3-107">inout *StreamOutputObject*<*DataType*> *Name;*</span></span> |
|------------------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="d2ef3-108">參數</span><span class="sxs-lookup"><span data-stu-id="d2ef3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2ef3-109"><span id="StreamOutputObject___________________________DataType_________________________________________Name"></span><span id="streamoutputobject___________________________datatype_________________________________________name"></span><span id="STREAMOUTPUTOBJECT___________________________DATATYPE_________________________________________NAME"></span>*StreamOutputObject*  < *DataType*  >   *名稱*</span><span class="sxs-lookup"><span data-stu-id="d2ef3-109"><span id="StreamOutputObject___________________________DataType_________________________________________Name"></span><span id="streamoutputobject___________________________datatype_________________________________________name"></span><span id="STREAMOUTPUTOBJECT___________________________DATATYPE_________________________________________NAME"></span>*StreamOutputObject* < *DataType* >   *Name*</span></span>
</dt> <dd>

<span data-ttu-id="d2ef3-110">資料流程輸出物件 (因此) 宣告。</span><span class="sxs-lookup"><span data-stu-id="d2ef3-110">The stream-output object (SO) declaration.</span></span>



| <span data-ttu-id="d2ef3-111">Stream-Output 物件類型</span><span class="sxs-lookup"><span data-stu-id="d2ef3-111">Stream-Output Object Types</span></span> | <span data-ttu-id="d2ef3-112">Description</span><span class="sxs-lookup"><span data-stu-id="d2ef3-112">Description</span></span>                       |
|----------------------------|-----------------------------------|
| <span data-ttu-id="d2ef3-113">*PointStream*</span><span class="sxs-lookup"><span data-stu-id="d2ef3-113">*PointStream*</span></span>              | <span data-ttu-id="d2ef3-114">一系列的點基本</span><span class="sxs-lookup"><span data-stu-id="d2ef3-114">A sequence of point primitives</span></span>    |
| <span data-ttu-id="d2ef3-115">*LineStream*</span><span class="sxs-lookup"><span data-stu-id="d2ef3-115">*LineStream*</span></span>               | <span data-ttu-id="d2ef3-116">行基本類型的序列</span><span class="sxs-lookup"><span data-stu-id="d2ef3-116">A sequence of line primitives</span></span>     |
| <span data-ttu-id="d2ef3-117">*TriangleStream*</span><span class="sxs-lookup"><span data-stu-id="d2ef3-117">*TriangleStream*</span></span>           | <span data-ttu-id="d2ef3-118">三角形基本類型的序列</span><span class="sxs-lookup"><span data-stu-id="d2ef3-118">A sequence of triangle primitives</span></span> |



 

<span data-ttu-id="d2ef3-119">*DataType* -Output 資料類型;可以是任何 [HLSL 資料類型](dx-graphics-hlsl-data-types.md)。</span><span class="sxs-lookup"><span data-stu-id="d2ef3-119">*DataType* - Output data type; can be any [HLSL data type](dx-graphics-hlsl-data-types.md).</span></span> <span data-ttu-id="d2ef3-120">必須以角括弧括住。</span><span class="sxs-lookup"><span data-stu-id="d2ef3-120">Must be surrounded by the angle brackets.</span></span>

<span data-ttu-id="d2ef3-121">*名稱* -變數名稱;可唯一識別物件的 ASCII 字串。</span><span class="sxs-lookup"><span data-stu-id="d2ef3-121">*Name* - Variable name; an ASCII string that uniquely identifies the object.</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="d2ef3-122">範例</span><span class="sxs-lookup"><span data-stu-id="d2ef3-122">Example</span></span>

<span data-ttu-id="d2ef3-123">這是資料流程輸出物件宣告的範例，它會串流出其資料是由結構中的 PS 立方體貼圖所定義的三角形基本類型 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="d2ef3-123">This is an example of a stream-output object declaration that streams out triangle primitives whose data is defined by the PS\_CUBEMAP\_IN structure.</span></span> <span data-ttu-id="d2ef3-124">幾何著色器僅限產生18個頂點。</span><span class="sxs-lookup"><span data-stu-id="d2ef3-124">The geometry-shader is limited to generating 18 vertices.</span></span>


```
struct PS_CUBEMAP_IN
{
    float4 Pos : SV_POSITION;     // Projection coord
    float2 Tex : TEXCOORD0;       // Texture coord
    uint RTIndex : SV_RenderTargetArrayIndex;
};

[maxvertexcount(18)]
void main( inout TriangleStream<PS_CUBEMAP_IN> CubeMapStream, triangle PS_CUBEMAP_INT[3] )
{
    ...
}
```



<span data-ttu-id="d2ef3-125">這是來自 [CubeMapGS 範例](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)的程式碼片段。</span><span class="sxs-lookup"><span data-stu-id="d2ef3-125">This is a code snippet from the [CubeMapGS Sample](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx).</span></span>

## <a name="stream-output-object-methods"></a><span data-ttu-id="d2ef3-126">Stream-Output 物件方法</span><span class="sxs-lookup"><span data-stu-id="d2ef3-126">Stream-Output Object Methods</span></span>

<span data-ttu-id="d2ef3-127">使用下列語法來呼叫資料流程輸出物件方法。</span><span class="sxs-lookup"><span data-stu-id="d2ef3-127">Use the following syntax to call stream-output-object methods.</span></span>


```
Object.Method
```



<span data-ttu-id="d2ef3-128">會實作為下列方法。</span><span class="sxs-lookup"><span data-stu-id="d2ef3-128">The following methods are implemented.</span></span>



| <span data-ttu-id="d2ef3-129">方法</span><span class="sxs-lookup"><span data-stu-id="d2ef3-129">Methods</span></span>                                              | <span data-ttu-id="d2ef3-130">描述</span><span class="sxs-lookup"><span data-stu-id="d2ef3-130">Description</span></span>                                                      |
|------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="d2ef3-131">Append</span><span class="sxs-lookup"><span data-stu-id="d2ef3-131">Append</span></span>](dx-graphics-hlsl-so-append.md)             | <span data-ttu-id="d2ef3-132">將輸出資料附加至現有的資料流程。</span><span class="sxs-lookup"><span data-stu-id="d2ef3-132">Append output data to an existing stream.</span></span>                        |
| [<span data-ttu-id="d2ef3-133">RestartStrip</span><span class="sxs-lookup"><span data-stu-id="d2ef3-133">RestartStrip</span></span>](dx-graphics-hlsl-so-restartstrip.md) | <span data-ttu-id="d2ef3-134">結束目前的基本區域並啟動新的基本區域。</span><span class="sxs-lookup"><span data-stu-id="d2ef3-134">End the current primitive strip and start a new primitive strip.</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d2ef3-135">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="d2ef3-135">Minimum Shader Model</span></span>

<span data-ttu-id="d2ef3-136">下列著色器模型支援此物件。</span><span class="sxs-lookup"><span data-stu-id="d2ef3-136">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="d2ef3-137">著色器模型</span><span class="sxs-lookup"><span data-stu-id="d2ef3-137">Shader Model</span></span>                                                        | <span data-ttu-id="d2ef3-138">支援</span><span class="sxs-lookup"><span data-stu-id="d2ef3-138">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| <span data-ttu-id="d2ef3-139">[著色器模型 4](dx-graphics-hlsl-sm4.md) 和更高的著色器模型</span><span class="sxs-lookup"><span data-stu-id="d2ef3-139">[Shader Model 4](dx-graphics-hlsl-sm4.md) and higher shader models</span></span> | <span data-ttu-id="d2ef3-140">是</span><span class="sxs-lookup"><span data-stu-id="d2ef3-140">yes</span></span>       |



 

## <a name="related-topics"></a><span data-ttu-id="d2ef3-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="d2ef3-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2ef3-142">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="d2ef3-142">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 