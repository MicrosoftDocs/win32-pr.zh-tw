---
title: 常數變數的封裝規則
description: 封裝規則會規定資料儲存時如何排列緊密的資料。
ms.assetid: 5c399342-06e1-47d2-8ecf-e093ed04be50
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d85566083dc9ead93a1a9e73fb06051b62178114
ms.sourcegitcommit: 004d7881dc9ff92ea394cd2331774e13b1e7f13c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/12/2020
ms.locfileid: "103681624"
---
# <a name="packing-rules-for-constant-variables"></a><span data-ttu-id="25899-103">常數變數的封裝規則</span><span class="sxs-lookup"><span data-stu-id="25899-103">Packing Rules for Constant Variables</span></span>

<span data-ttu-id="25899-104">封裝規則會規定資料儲存時如何排列緊密的資料。</span><span class="sxs-lookup"><span data-stu-id="25899-104">Packing rules dictate how tightly data can be arranged when it is stored.</span></span> <span data-ttu-id="25899-105">HLSL 會針對 VS 輸出資料、GS 輸入和輸出資料，以及 PS 輸入和輸出資料來實行封裝規則。</span><span class="sxs-lookup"><span data-stu-id="25899-105">HLSL implements packing rules for VS output data, GS input and output data, and PS input and output data.</span></span> <span data-ttu-id="25899-106">因為 IA 階段無法解除封裝資料，所以不會針對 VS 輸入封裝 (的資料。 ) </span><span class="sxs-lookup"><span data-stu-id="25899-106">(Data is not packed for VS inputs because the IA stage cannot unpack data.)</span></span>

<span data-ttu-id="25899-107">HLSL 封裝規則類似于使用 Visual Studio 執行 **\# pragma pack 4** ，將資料封裝成4位元組的界限。</span><span class="sxs-lookup"><span data-stu-id="25899-107">HLSL packing rules are similar to performing a **\#pragma pack 4** with Visual Studio, which packs data into 4-byte boundaries.</span></span> <span data-ttu-id="25899-108">此外，HLSL 會封裝資料，使其不會跨越16位元組的界限。</span><span class="sxs-lookup"><span data-stu-id="25899-108">Additionally, HLSL packs data so that it does not cross a 16-byte boundary.</span></span> <span data-ttu-id="25899-109">變數會封裝成指定的四個元件向量，直到變數跨4向量界限為止;接下來的變數將會被退回到下四個元件向量。</span><span class="sxs-lookup"><span data-stu-id="25899-109">Variables are packed into a given four-component vector until the variable will straddle a 4-vector boundary; the next variables will be bounced to the next four-component vector.</span></span>

<span data-ttu-id="25899-110">每個結構都會強制下一個變數在接下來的四個元件向量上啟動。</span><span class="sxs-lookup"><span data-stu-id="25899-110">Each structure forces the next variable to start on the next four-component vector.</span></span> <span data-ttu-id="25899-111">這有時會為結構陣列產生填補。</span><span class="sxs-lookup"><span data-stu-id="25899-111">This sometimes generates padding for arrays of structures.</span></span> <span data-ttu-id="25899-112">任何結構的結果大小一律會由 **sizeof** (*四個元件向量*) 平均整除。</span><span class="sxs-lookup"><span data-stu-id="25899-112">The resulting size of any structure will always be evenly divisible by **sizeof**(*four-component vector*).</span></span>

<span data-ttu-id="25899-113">依預設，不會將陣列封裝在 HLSL 中。</span><span class="sxs-lookup"><span data-stu-id="25899-113">Arrays are not packed in HLSL by default.</span></span> <span data-ttu-id="25899-114">為了避免強制著色器針對位移計算採用 ALU 額外負荷，陣列中的每個元素都會儲存在四個元件的向量中。</span><span class="sxs-lookup"><span data-stu-id="25899-114">To avoid forcing the shader to take on ALU overhead for offset computations, every element in an array is stored in a four-component vector.</span></span> <span data-ttu-id="25899-115">請注意，您可以 (的陣列進行封裝，並使用轉型來產生定址計算) 。</span><span class="sxs-lookup"><span data-stu-id="25899-115">Note that you can achieve packing for arrays (and incur the addressing calculations) by using casting.</span></span>

<span data-ttu-id="25899-116">以下是 (指定的結構和其對應的封裝大小範例： **float1** 佔用4個位元組) ：</span><span class="sxs-lookup"><span data-stu-id="25899-116">Following are examples of structures and their corresponding packed sizes (given: a **float1** occupies 4 bytes):</span></span>


```
//  2 x 16byte elements
cbuffer IE
{
    float4 Val1;
    float2 Val2;  // starts a new vector
    float2 Val3;
};

//  3 x 16byte elements
cbuffer IE
{
    float2 Val1;
    float4 Val2;  // starts a new vector
    float2 Val3;  // starts a new vector
};

//  1 x 16byte elements
cbuffer IE
{
    float1 Val1;
    float1 Val2;
    float2 Val3;
};

//  1 x 16byte elements
cbuffer IE
{
    float1 Val1;
    float2 Val2;
    float1 Val3;
};

//  2 x 16byte elements
cbuffer IE
{
    float1 Val1;
    float1 Val1;
    float1 Val1;
    float2 Val2;    // starts a new vector
};


//  1 x 16byte elements
cbuffer IE
{
    float3 Val1;
    float1 Val2;
};

//  1 x 16byte elements
cbuffer IE
{
    float1 Val1;
    float3 Val2;
};

//  2 x 16byte elements
cbuffer IE
{
    float1 Val1;
    float1 Val1;
    float3 Val2;        // starts a new vector
};


// 3 x 16byte elements
cbuffer IE
{
    float1 Val1;

    struct     {
        float4 SVal1;    // starts a new vector
        float1 SVal2;    // starts a new vector
    } Val2;
};

// 3 x 16byte elements
cbuffer IE
{
    float1 Val1;  
    struct     {
        float1 SVal1;     // starts a new vector
        float4 SVal2;     // starts a new vector
    } Val2;
};

// 3 x 16byte elements
cbuffer IE
{
    struct     {
        float4 SVal1;
        float1 SVal2;    // starts a new vector
    } Val1;

    float1 Val2; 
};
```



## <a name="more-aggressive-packing"></a><span data-ttu-id="25899-117">更積極的封裝</span><span class="sxs-lookup"><span data-stu-id="25899-117">More Aggressive Packing</span></span>

<span data-ttu-id="25899-118">您可以更積極地封裝陣列。</span><span class="sxs-lookup"><span data-stu-id="25899-118">You could pack an array more aggressively.</span></span> <span data-ttu-id="25899-119">例如，假設有一個 float 變數陣列：</span><span class="sxs-lookup"><span data-stu-id="25899-119">For instance, given an array of float variables:</span></span>


```
float4 array[16];
```



<span data-ttu-id="25899-120">您可以選擇將它封裝起來，而不需要陣列中的任何空格：</span><span class="sxs-lookup"><span data-stu-id="25899-120">You could choose to pack it like this, without any spaces in the array:</span></span>


```
static float2 aggressivePackArray[32] = (float2[32])array;  
```



<span data-ttu-id="25899-121">更緊密的封裝是一種取捨，也就是位址計算的其他著色器指示需求。</span><span class="sxs-lookup"><span data-stu-id="25899-121">The tighter packing is a trade off versus the need for additional shader instructions for address computation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="25899-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="25899-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="25899-123">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="25899-123">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




