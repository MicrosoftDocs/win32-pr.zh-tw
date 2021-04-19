---
description: 用來表示圖形管線階段的列舉。
MS-HAID: vspixengine.PIPELINESTAGES
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: PIPELINESTAGES 列舉
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: AF40441A-8027-4028-9A02-D53754FD2596
api_name:
- PIPELINESTAGES
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 11f52f62815228e459bed06d369fa6479d2b0e22
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106972944"
---
# <a name="span-idvspixenginepipelinestagesspanpipelinestages-enumeration"></a><span data-ttu-id="c2753-103"><span id="vspixengine.pipelinestages"></span>PIPELINESTAGES 列舉</span><span class="sxs-lookup"><span data-stu-id="c2753-103"><span id="vspixengine.pipelinestages"></span>PIPELINESTAGES enumeration</span></span>

<span data-ttu-id="c2753-104">用來表示圖形管線階段的列舉。</span><span class="sxs-lookup"><span data-stu-id="c2753-104">An enum used to indicate a stage of the graphics pipeline.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2753-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2753-105">Syntax</span></span>


```C++
};
```

## <a name="constants"></a><span data-ttu-id="c2753-106">常數</span><span class="sxs-lookup"><span data-stu-id="c2753-106">Constants</span></span>

<span data-ttu-id="c2753-107"><span id="PipeLineStages_InputAssembler"></span><span id="pipelinestages_inputassembler"></span><span id="PIPELINESTAGES_INPUTASSEMBLER"></span>**PipeLineStages \_ InputAssembler**</span><span class="sxs-lookup"><span data-stu-id="c2753-107"><span id="PipeLineStages_InputAssembler"></span><span id="pipelinestages_inputassembler"></span><span id="PIPELINESTAGES_INPUTASSEMBLER"></span>**PipeLineStages\_InputAssembler**</span></span>  
<span data-ttu-id="c2753-108">對應至輸入組合語言階段的值。</span><span class="sxs-lookup"><span data-stu-id="c2753-108">A value that corresponds to the Input Assembler stage.</span></span>

<span data-ttu-id="c2753-109"><span id="PipeLineStages_VertexShader"></span><span id="pipelinestages_vertexshader"></span><span id="PIPELINESTAGES_VERTEXSHADER"></span>**PipeLineStages \_ VertexShader**</span><span class="sxs-lookup"><span data-stu-id="c2753-109"><span id="PipeLineStages_VertexShader"></span><span id="pipelinestages_vertexshader"></span><span id="PIPELINESTAGES_VERTEXSHADER"></span>**PipeLineStages\_VertexShader**</span></span>  
<span data-ttu-id="c2753-110">對應至頂點著色器階段的值。</span><span class="sxs-lookup"><span data-stu-id="c2753-110">A value that corresponds to the Vertex Shader stage.</span></span>

<span data-ttu-id="c2753-111"><span id="PipeLineStages_HullShader"></span><span id="pipelinestages_hullshader"></span><span id="PIPELINESTAGES_HULLSHADER"></span>**PipeLineStages \_ HullShader**</span><span class="sxs-lookup"><span data-stu-id="c2753-111"><span id="PipeLineStages_HullShader"></span><span id="pipelinestages_hullshader"></span><span id="PIPELINESTAGES_HULLSHADER"></span>**PipeLineStages\_HullShader**</span></span>  
<span data-ttu-id="c2753-112">值，對應于輪廓著色器階段。</span><span class="sxs-lookup"><span data-stu-id="c2753-112">A value that corresponds to the Hull Shader stage.</span></span>

<span data-ttu-id="c2753-113"><span id="PipeLineStages_Tesselator"></span><span id="pipelinestages_tesselator"></span><span id="PIPELINESTAGES_TESSELATOR"></span>**PipeLineStages \_ Tesselator**</span><span class="sxs-lookup"><span data-stu-id="c2753-113"><span id="PipeLineStages_Tesselator"></span><span id="pipelinestages_tesselator"></span><span id="PIPELINESTAGES_TESSELATOR"></span>**PipeLineStages\_Tesselator**</span></span>  
<span data-ttu-id="c2753-114">值，這個值會對應至 Tesselator 階段。</span><span class="sxs-lookup"><span data-stu-id="c2753-114">A value that corresponds to the Tesselator stage.</span></span>

<span data-ttu-id="c2753-115"><span id="PipeLineStages_DomainShader"></span><span id="pipelinestages_domainshader"></span><span id="PIPELINESTAGES_DOMAINSHADER"></span>**PipeLineStages \_ DomainShader**</span><span class="sxs-lookup"><span data-stu-id="c2753-115"><span id="PipeLineStages_DomainShader"></span><span id="pipelinestages_domainshader"></span><span id="PIPELINESTAGES_DOMAINSHADER"></span>**PipeLineStages\_DomainShader**</span></span>  
<span data-ttu-id="c2753-116">對應到網域著色器階段的值。</span><span class="sxs-lookup"><span data-stu-id="c2753-116">A value that corresponds to the Domain Shader stage.</span></span>

<span data-ttu-id="c2753-117"><span id="PipeLineStages_GeometryShader"></span><span id="pipelinestages_geometryshader"></span><span id="PIPELINESTAGES_GEOMETRYSHADER"></span>**PipeLineStages \_ GeometryShader**</span><span class="sxs-lookup"><span data-stu-id="c2753-117"><span id="PipeLineStages_GeometryShader"></span><span id="pipelinestages_geometryshader"></span><span id="PIPELINESTAGES_GEOMETRYSHADER"></span>**PipeLineStages\_GeometryShader**</span></span>  
<span data-ttu-id="c2753-118">值，對應至幾何著色器階段。</span><span class="sxs-lookup"><span data-stu-id="c2753-118">A value that corresponds to the Geometry Shader stage.</span></span>

<span data-ttu-id="c2753-119"><span id="PipeLineStages_StreamOutput"></span><span id="pipelinestages_streamoutput"></span><span id="PIPELINESTAGES_STREAMOUTPUT"></span>**PipeLineStages \_ >streamoutput**</span><span class="sxs-lookup"><span data-stu-id="c2753-119"><span id="PipeLineStages_StreamOutput"></span><span id="pipelinestages_streamoutput"></span><span id="PIPELINESTAGES_STREAMOUTPUT"></span>**PipeLineStages\_StreamOutput**</span></span>  
<span data-ttu-id="c2753-120">對應至資料流程輸出階段的值。</span><span class="sxs-lookup"><span data-stu-id="c2753-120">A value that corresponds to the Stream Output stage.</span></span>

<span data-ttu-id="c2753-121"><span id="PipeLineStages_Rasterizer"></span><span id="pipelinestages_rasterizer"></span><span id="PIPELINESTAGES_RASTERIZER"></span>**PipeLineStages \_ 轉譯器**</span><span class="sxs-lookup"><span data-stu-id="c2753-121"><span id="PipeLineStages_Rasterizer"></span><span id="pipelinestages_rasterizer"></span><span id="PIPELINESTAGES_RASTERIZER"></span>**PipeLineStages\_Rasterizer**</span></span>  
<span data-ttu-id="c2753-122">對應至轉譯器階段的值。</span><span class="sxs-lookup"><span data-stu-id="c2753-122">A value that corresponds to the Rasterizer stage.</span></span>

<span data-ttu-id="c2753-123"><span id="PipeLineStages_PixelShader"></span><span id="pipelinestages_pixelshader"></span><span id="PIPELINESTAGES_PIXELSHADER"></span>**PipeLineStages \_ 無效**</span><span class="sxs-lookup"><span data-stu-id="c2753-123"><span id="PipeLineStages_PixelShader"></span><span id="pipelinestages_pixelshader"></span><span id="PIPELINESTAGES_PIXELSHADER"></span>**PipeLineStages\_PixelShader**</span></span>  
<span data-ttu-id="c2753-124">值，對應至圖元著色器階段。</span><span class="sxs-lookup"><span data-stu-id="c2753-124">A value that corresponds to the Pixel Shader stage.</span></span>

<span data-ttu-id="c2753-125"><span id="PipeLineStages_OutputMerger"></span><span id="pipelinestages_outputmerger"></span><span id="PIPELINESTAGES_OUTPUTMERGER"></span>**PipeLineStages \_ OutputMerger**</span><span class="sxs-lookup"><span data-stu-id="c2753-125"><span id="PipeLineStages_OutputMerger"></span><span id="pipelinestages_outputmerger"></span><span id="PIPELINESTAGES_OUTPUTMERGER"></span>**PipeLineStages\_OutputMerger**</span></span>  
<span data-ttu-id="c2753-126">值，對應至輸出合併階段。</span><span class="sxs-lookup"><span data-stu-id="c2753-126">A value that corresponds to the Output Merger stage.</span></span>

<span data-ttu-id="c2753-127"><span id="PipeLineStages_ComputeShader"></span><span id="pipelinestages_computeshader"></span><span id="PIPELINESTAGES_COMPUTESHADER"></span>**PipeLineStages \_ ComputeShader**</span><span class="sxs-lookup"><span data-stu-id="c2753-127"><span id="PipeLineStages_ComputeShader"></span><span id="pipelinestages_computeshader"></span><span id="PIPELINESTAGES_COMPUTESHADER"></span>**PipeLineStages\_ComputeShader**</span></span>  
<span data-ttu-id="c2753-128">對應到計算著色器階段的值。</span><span class="sxs-lookup"><span data-stu-id="c2753-128">A value that corresponds to the Compute Shader stage.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2753-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="c2753-129">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="c2753-130">標頭</span><span class="sxs-lookup"><span data-stu-id="c2753-130">Header</span></span></p></td><td><span data-ttu-id="c2753-131">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="c2753-131">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



