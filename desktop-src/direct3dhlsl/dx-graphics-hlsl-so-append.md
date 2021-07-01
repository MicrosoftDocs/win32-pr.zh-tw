---
title: '附加 (DirectX HLSL Stream-Output 物件) '
description: 將幾何-著色器輸出資料附加至現有的資料流程。
ms.assetid: 7df51383-7fc7-4a6f-aaa2-6c929f0443a3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 19d767f3c501cc42e21bbc44a196ba08cd6f1883
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120183"
---
# <a name="append-directx-hlsl-stream-output-object"></a><span data-ttu-id="79d6b-103">附加 (DirectX HLSL Stream-Output 物件) </span><span class="sxs-lookup"><span data-stu-id="79d6b-103">Append (DirectX HLSL Stream-Output Object)</span></span>

<span data-ttu-id="79d6b-104">將幾何-著色器輸出資料附加至現有的資料流程。</span><span class="sxs-lookup"><span data-stu-id="79d6b-104">Append geometry-shader-output data to an existing stream.</span></span>

<span data-ttu-id="79d6b-105">附加 ( *StreamDataType*) ;</span><span class="sxs-lookup"><span data-stu-id="79d6b-105">Append( *StreamDataType*);</span></span>



 

## <a name="parameters"></a><span data-ttu-id="79d6b-106">參數</span><span class="sxs-lookup"><span data-stu-id="79d6b-106">Parameters</span></span>



| <span data-ttu-id="79d6b-107">項目</span><span class="sxs-lookup"><span data-stu-id="79d6b-107">Item</span></span>                                                                                                                             | <span data-ttu-id="79d6b-108">描述</span><span class="sxs-lookup"><span data-stu-id="79d6b-108">Description</span></span>                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79d6b-109"><span id="StreamDataType"></span><span id="streamdatatype"></span><span id="STREAMDATATYPE"></span>**StreamDataType**</span><span class="sxs-lookup"><span data-stu-id="79d6b-109"><span id="StreamDataType"></span><span id="streamdatatype"></span><span id="STREAMDATATYPE"></span>**StreamDataType**</span></span><br/> | <span data-ttu-id="79d6b-110">資料輸入描述。</span><span class="sxs-lookup"><span data-stu-id="79d6b-110">A data input description.</span></span> <span data-ttu-id="79d6b-111">此描述必須與名為 [DataType](dx-graphics-hlsl-so-type.md)的資料流程物件範本參數相符。</span><span class="sxs-lookup"><span data-stu-id="79d6b-111">This description must match the stream-object template parameter called [DataType](dx-graphics-hlsl-so-type.md).</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="79d6b-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="79d6b-112">Return Value</span></span>

<span data-ttu-id="79d6b-113">None</span><span class="sxs-lookup"><span data-stu-id="79d6b-113">None</span></span>

## <a name="example"></a><span data-ttu-id="79d6b-114">範例</span><span class="sxs-lookup"><span data-stu-id="79d6b-114">Example</span></span>

<span data-ttu-id="79d6b-115">這段來自 [CubeMapGS 範例](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx) (的程式碼片段，) 顯示將三角形區域基本專案附加至資料流程輸出物件的部分範例。</span><span class="sxs-lookup"><span data-stu-id="79d6b-115">This code snippet (from the [CubeMapGS Sample](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)) shows a partial example of appending triangle strip primitives to a stream-output object.</span></span>


```
[maxvertexcount(18)]
void GS_CubeMap( triangle GS_CUBEMAP_IN input[3], 
                 inout TriangleStream<PS_CUBEMAP_IN> CubeMapStream )
{
    for( int f = 0; f < 6; ++f )
    {
        // Compute screen coordinates
        PS_CUBEMAP_IN output;
        output.RTIndex = f;
        for( int v = 0; v < 3; v++ )
        {
            output.Pos = mul( input[v].Pos, g_mViewCM[f] );
            output.Pos = mul( output.Pos, mProj );
            output.Tex = input[v].Tex;
            CubeMapStream.Append( output );
        }
        CubeMapStream.RestartStrip();
    }
}
```



## <a name="minimum-shader-model"></a><span data-ttu-id="79d6b-116">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="79d6b-116">Minimum Shader Model</span></span>

<span data-ttu-id="79d6b-117">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="79d6b-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="79d6b-118">著色器模型</span><span class="sxs-lookup"><span data-stu-id="79d6b-118">Shader Model</span></span>                                              | <span data-ttu-id="79d6b-119">支援</span><span class="sxs-lookup"><span data-stu-id="79d6b-119">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="79d6b-120">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="79d6b-120">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="79d6b-121">是</span><span class="sxs-lookup"><span data-stu-id="79d6b-121">yes</span></span>       |
| [<span data-ttu-id="79d6b-122">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="79d6b-122">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="79d6b-123">否</span><span class="sxs-lookup"><span data-stu-id="79d6b-123">no</span></span>        |
| [<span data-ttu-id="79d6b-124">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="79d6b-124">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="79d6b-125">否</span><span class="sxs-lookup"><span data-stu-id="79d6b-125">no</span></span>        |
| [<span data-ttu-id="79d6b-126">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="79d6b-126">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="79d6b-127">否</span><span class="sxs-lookup"><span data-stu-id="79d6b-127">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="79d6b-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="79d6b-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79d6b-129">資料流程輸出物件</span><span class="sxs-lookup"><span data-stu-id="79d6b-129">Stream-Output Object</span></span>](dx-graphics-hlsl-so-type.md)
</dt> </dl>

 

 





