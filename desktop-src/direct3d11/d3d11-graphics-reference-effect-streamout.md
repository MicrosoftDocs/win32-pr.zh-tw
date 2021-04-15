---
title: 資料流程輸出語法
description: 具有資料流程輸出的幾何著色器會使用特定語法來宣告。
ms.assetid: 58cf6503-0dde-4c88-837d-ae0e0eda17d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 535ea78d1b2109e343f01800b3a3d5e1bf6efaba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104990619"
---
# <a name="stream-out-syntax"></a><span data-ttu-id="9484a-103">資料流程輸出語法</span><span class="sxs-lookup"><span data-stu-id="9484a-103">Stream Out Syntax</span></span>

<span data-ttu-id="9484a-104">具有資料流程輸出的幾何著色器會使用特定語法來宣告。</span><span class="sxs-lookup"><span data-stu-id="9484a-104">A geometry shader with stream out is declared with a particular syntax.</span></span> <span data-ttu-id="9484a-105">本主題說明語法。</span><span class="sxs-lookup"><span data-stu-id="9484a-105">This topic describes the syntax.</span></span> <span data-ttu-id="9484a-106">在效果執行時間中，會將此語法轉換成 [**ID3D11Device：： CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput)的呼叫。</span><span class="sxs-lookup"><span data-stu-id="9484a-106">In the effect runtime, this syntax will be converted to a call to [**ID3D11Device::CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput).</span></span>

## <a name="construct-syntax"></a><span data-ttu-id="9484a-107">結構語法</span><span class="sxs-lookup"><span data-stu-id="9484a-107">Construct Syntax</span></span>


```
[ StreamingShaderVar = ] ConstructGSWithSO( ShaderVar, "OutputDecl0" )
```





| <span data-ttu-id="9484a-108">名稱</span><span class="sxs-lookup"><span data-stu-id="9484a-108">Name</span></span>                   | <span data-ttu-id="9484a-109">描述</span><span class="sxs-lookup"><span data-stu-id="9484a-109">Description</span></span>                                                                                                                                                                                                                |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9484a-110">**StreamingShaderVar**</span><span class="sxs-lookup"><span data-stu-id="9484a-110">**StreamingShaderVar**</span></span> | <span data-ttu-id="9484a-111">選擇性。</span><span class="sxs-lookup"><span data-stu-id="9484a-111">Optional.</span></span> <span data-ttu-id="9484a-112">使用資料流程來唯一識別幾何著色器變數名稱的 ASCI 字串。這是選擇性的，因為 ConstructGSWithSO 可以直接放在 SetGeometryShader 或 BindInterfaces 呼叫中。</span><span class="sxs-lookup"><span data-stu-id="9484a-112">An ASCI string that uniquely identifies the name of a geometry shader variable with stream out. This is optional because ConstructGSWithSO can be placed directly in a SetGeometryShader or BindInterfaces call.</span></span> |
| <span data-ttu-id="9484a-113">**ShaderVar**</span><span class="sxs-lookup"><span data-stu-id="9484a-113">**ShaderVar**</span></span>          | <span data-ttu-id="9484a-114">幾何著色器或頂點著色器變數。</span><span class="sxs-lookup"><span data-stu-id="9484a-114">A geometry shader or vertex shader variable.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="9484a-115">**OutputDecl0**</span><span class="sxs-lookup"><span data-stu-id="9484a-115">**OutputDecl0**</span></span>        | <span data-ttu-id="9484a-116">字串，定義資料流程0中的著色器輸出資料流程處理。請參閱下面的語法。</span><span class="sxs-lookup"><span data-stu-id="9484a-116">A string defining which shader outputs in stream 0 are streamed out. See below for syntax.</span></span>                                                                                                                                 |



 

<span data-ttu-id="9484a-117">這是在 fx 4 0 檔案中定義的語法 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="9484a-117">This is the syntax was defined in fx\_4\_0 files.</span></span> <span data-ttu-id="9484a-118">請注意，在 gs \_ 4 \_ 0 和 vs \_ x 著色器中，只有一個資料串流。</span><span class="sxs-lookup"><span data-stu-id="9484a-118">Note that in gs\_4\_0 and vs\_x shaders, there is only one stream of data.</span></span> <span data-ttu-id="9484a-119">產生的著色器會將一個資料流程輸出至串流輸出單元和轉譯器單位。</span><span class="sxs-lookup"><span data-stu-id="9484a-119">The resulting shader will output one stream to both the stream out unit and the rasterizer unit.</span></span>


```
[ StreamingShaderVar = ] ConstructGSWithSO( ShaderVar, "OutputDecl0", "OutputDecl1", "OutputDecl2", 
"OutputDecl3", RasterizedStream )
```





| <span data-ttu-id="9484a-120">名稱</span><span class="sxs-lookup"><span data-stu-id="9484a-120">Name</span></span>                   | <span data-ttu-id="9484a-121">描述</span><span class="sxs-lookup"><span data-stu-id="9484a-121">Description</span></span>                                                                                                                                                                                                                |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9484a-122">**StreamingShaderVar**</span><span class="sxs-lookup"><span data-stu-id="9484a-122">**StreamingShaderVar**</span></span> | <span data-ttu-id="9484a-123">選擇性。</span><span class="sxs-lookup"><span data-stu-id="9484a-123">Optional.</span></span> <span data-ttu-id="9484a-124">使用資料流程來唯一識別幾何著色器變數名稱的 ASCI 字串。這是選擇性的，因為 ConstructGSWithSO 可以直接放在 SetGeometryShader 或 BindInterfaces 呼叫中。</span><span class="sxs-lookup"><span data-stu-id="9484a-124">An ASCI string that uniquely identifies the name of a geometry shader variable with stream out. This is optional because ConstructGSWithSO can be placed directly in a SetGeometryShader or BindInterfaces call.</span></span> |
| <span data-ttu-id="9484a-125">**ShaderVar**</span><span class="sxs-lookup"><span data-stu-id="9484a-125">**ShaderVar**</span></span>          | <span data-ttu-id="9484a-126">幾何著色器或頂點著色器變數。</span><span class="sxs-lookup"><span data-stu-id="9484a-126">A geometry shader or vertex shader variable.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="9484a-127">**OutputDecl0**</span><span class="sxs-lookup"><span data-stu-id="9484a-127">**OutputDecl0**</span></span>        | <span data-ttu-id="9484a-128">字串，定義資料流程0中的著色器輸出資料流程處理。請參閱下面的語法。</span><span class="sxs-lookup"><span data-stu-id="9484a-128">A string defining which shader outputs in stream 0 are streamed out. See below for syntax.</span></span>                                                                                                                                 |
| <span data-ttu-id="9484a-129">**OutputDecl1**</span><span class="sxs-lookup"><span data-stu-id="9484a-129">**OutputDecl1**</span></span>        | <span data-ttu-id="9484a-130">字串，定義串流1中的著色器輸出資料流程處理。請參閱下面的語法。</span><span class="sxs-lookup"><span data-stu-id="9484a-130">A string defining which shader outputs in stream 1 are streamed out. See below for syntax.</span></span>                                                                                                                                 |
| <span data-ttu-id="9484a-131">**OutputDecl2**</span><span class="sxs-lookup"><span data-stu-id="9484a-131">**OutputDecl2**</span></span>        | <span data-ttu-id="9484a-132">字串，定義串流2中的著色器輸出資料流程處理。請參閱下面的語法。</span><span class="sxs-lookup"><span data-stu-id="9484a-132">A string defining which shader outputs in stream 2 are streamed out. See below for syntax.</span></span>                                                                                                                                 |
| <span data-ttu-id="9484a-133">**OutputDecl3**</span><span class="sxs-lookup"><span data-stu-id="9484a-133">**OutputDecl3**</span></span>        | <span data-ttu-id="9484a-134">字串，定義串流3中的著色器輸出資料流程處理。請參閱下面的語法。</span><span class="sxs-lookup"><span data-stu-id="9484a-134">A string defining which shader outputs in stream 3 are streamed out. See below for syntax.</span></span>                                                                                                                                 |
| <span data-ttu-id="9484a-135">**RasterizedStream**</span><span class="sxs-lookup"><span data-stu-id="9484a-135">**RasterizedStream**</span></span>   | <span data-ttu-id="9484a-136">整數，指定要將哪個資料流程傳送至轉譯器。</span><span class="sxs-lookup"><span data-stu-id="9484a-136">An integer specifying which stream will be sent to the rasterizer.</span></span>                                                                                                                                                         |



 

<span data-ttu-id="9484a-137">請注意，gs \_ 5 \_ 0 著色器最多可以定義四個數據流。</span><span class="sxs-lookup"><span data-stu-id="9484a-137">Note that gs\_5\_0 shaders can define up to four streams of data.</span></span> <span data-ttu-id="9484a-138">產生的著色器會針對每個非 **Null** 的輸出宣告，將一個資料流程輸出到資料流程輸出單位，並將一個資料流程輸出到轉譯器單位。</span><span class="sxs-lookup"><span data-stu-id="9484a-138">The resulting shader will output one stream to the stream out unit for each non-**NULL** output declaration and one stream the rasterizer unit.</span></span>

## <a name="stream-out-declaration-syntax"></a><span data-ttu-id="9484a-139">資料流程輸出宣告語法</span><span class="sxs-lookup"><span data-stu-id="9484a-139">Stream Out Declaration Syntax</span></span>


```
" [ Buffer: ] Semantic[ SemanticIndex ] [ .Mask ]; [ ... ; ] ... [ ... ;]"
```





| <span data-ttu-id="9484a-140">名稱</span><span class="sxs-lookup"><span data-stu-id="9484a-140">Name</span></span>              | <span data-ttu-id="9484a-141">描述</span><span class="sxs-lookup"><span data-stu-id="9484a-141">Description</span></span>                                                                                           |
|-------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9484a-142">**Buffer**</span><span class="sxs-lookup"><span data-stu-id="9484a-142">**Buffer**</span></span>        | <span data-ttu-id="9484a-143">選擇性。</span><span class="sxs-lookup"><span data-stu-id="9484a-143">Optional.</span></span> <span data-ttu-id="9484a-144">整數，0 <= 緩衝區 < 4，指定要將值移至哪個資料流程輸出緩衝區。</span><span class="sxs-lookup"><span data-stu-id="9484a-144">An integer, 0 <= Buffer < 4, specifying which stream out buffer the value will go to.</span></span> |
| <span data-ttu-id="9484a-145">**語義**</span><span class="sxs-lookup"><span data-stu-id="9484a-145">**Semantic**</span></span>      | <span data-ttu-id="9484a-146">字串，連同 SemanticIndex，指定要輸出的值。</span><span class="sxs-lookup"><span data-stu-id="9484a-146">A string, along with SemanticIndex, specifying which value to output.</span></span>                                 |
| <span data-ttu-id="9484a-147">**SemanticIndex**</span><span class="sxs-lookup"><span data-stu-id="9484a-147">**SemanticIndex**</span></span> | <span data-ttu-id="9484a-148">選擇性。</span><span class="sxs-lookup"><span data-stu-id="9484a-148">Optional.</span></span> <span data-ttu-id="9484a-149">與語義相關聯的索引。</span><span class="sxs-lookup"><span data-stu-id="9484a-149">The index associated with Semantic.</span></span>                                                         |
| <span data-ttu-id="9484a-150">**Mask**</span><span class="sxs-lookup"><span data-stu-id="9484a-150">**Mask**</span></span>          | <span data-ttu-id="9484a-151">選擇性。</span><span class="sxs-lookup"><span data-stu-id="9484a-151">Optional.</span></span> <span data-ttu-id="9484a-152">元件遮罩，指出要輸出值的哪些元件。</span><span class="sxs-lookup"><span data-stu-id="9484a-152">A component mask, indicating which components of the value to output.</span></span>                       |



 

<span data-ttu-id="9484a-153">有一個特殊的語義，標示為 "$SKIP"，表示空的語義，將對應的記憶體保留在串流輸出緩衝區中。</span><span class="sxs-lookup"><span data-stu-id="9484a-153">There is one special Semantic, labeled "$SKIP" which indicates an empty semantic, leaving the corresponding memory in the stream out buffer untouched.</span></span> <span data-ttu-id="9484a-154">$SKIP 語義不能有 SemanticIndex，但可以有遮罩。</span><span class="sxs-lookup"><span data-stu-id="9484a-154">The $SKIP semantic cannot have a SemanticIndex, but can have a Mask.</span></span>

<span data-ttu-id="9484a-155">整個資料流程輸出宣告可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="9484a-155">The entire stream out declaration can be **NULL**.</span></span>

## <a name="example"></a><span data-ttu-id="9484a-156">範例</span><span class="sxs-lookup"><span data-stu-id="9484a-156">Example</span></span>


```
struct GSOutput
{
int4 Pos : Position;
int4 Color : Color;
int4 Texcoord : Texcoord;
};

[maxvertexcount(1)]
void gsBase (inout PointStream<GSOutput> OutputStream, inout PointStream<GSOutput> OutputStream1)
{
GSOutput output;
output.Pos = int4(1,2,3,4);
output.Color = int4(5,6,7,8);
output.Texcoord = int4(9,10,11,12);
OutputStream.Append(output);

output.Pos = int4(1,2,3,4);
    output.Color = int4(5,6,7,8);
output.Texcoord = int4(9,10,11,12);
OutputStream1.Append(output);
};


GeometryShader pGSComp = CompileShader(gs_5_0, gsBase());
GeometryShader pGSwSO = ConstructGSWithSO(pGSComp, "0:Position.xy; 1:Position.zw; 2:Color.xy", 
                                                   "3:Texcoord.xyzw; 3:$SKIP.x;", NULL, NULL, 1);

// The following two passes perform the same operation
technique11 SOPoints
{
    pass 
    {
        SetGeometryShader(ConstructGSWithSO(pGSComp, "0:Position.xy; 1:Position.zw; 2:Color.xy", 
                                                     "3:Texcoord.xyzw; 3:$SKIP.x;", NULL, NULL, 1));
    }
    pass 
    {
        SetGeometryShader(pGSwSO);
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="9484a-157">相關主題</span><span class="sxs-lookup"><span data-stu-id="9484a-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9484a-158"> (Direct3D 11) 的效果 </span><span class="sxs-lookup"><span data-stu-id="9484a-158">Effects (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 




