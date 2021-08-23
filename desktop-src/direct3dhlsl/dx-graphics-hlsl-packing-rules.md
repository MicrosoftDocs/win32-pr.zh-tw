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
ms.openlocfilehash: 49b10f6383344821c7659ac40b367a77e0421d33be68a374c59920a62d37697c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120082"
---
# <a name="packing-rules-for-constant-variables"></a>常數變數的封裝規則

封裝規則會規定資料儲存時如何排列緊密的資料。 HLSL 會針對 VS 輸出資料、GS 輸入和輸出資料，以及 PS 輸入和輸出資料來實行封裝規則。 因為 IA 階段無法解除封裝資料，所以不會針對 VS 輸入封裝 (的資料。 ) 

HLSL 封裝規則類似于使用 Visual Studio 執行 **\# pragma pack 4** ，將資料封裝成4位元組的界限。 此外，HLSL 會封裝資料，使其不會跨越16位元組的界限。 變數會封裝成指定的四個元件向量，直到變數跨4向量界限為止;接下來的變數將會被退回到下四個元件向量。

每個結構都會強制下一個變數在接下來的四個元件向量上啟動。 這有時會為結構陣列產生填補。 任何結構的結果大小一律會由 **sizeof** (*四個元件向量*) 平均整除。

依預設，不會將陣列封裝在 HLSL 中。 為了避免強制著色器針對位移計算採用 ALU 額外負荷，陣列中的每個元素都會儲存在四個元件的向量中。 請注意，您可以 (的陣列進行封裝，並使用轉型來產生定址計算) 。

以下是 (指定的結構和其對應的封裝大小範例： **float1** 佔用4個位元組) ：


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



## <a name="more-aggressive-packing"></a>更積極的封裝

您可以更積極地封裝陣列。 例如，假設有一個 float 變數陣列：


```
float4 array[16];
```



您可以選擇將它封裝起來，而不需要陣列中的任何空格：


```
static float2 aggressivePackArray[32] = (float2[32])array;  
```



更緊密的封裝是一種取捨，也就是位址計算的其他著色器指示需求。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器模型4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




