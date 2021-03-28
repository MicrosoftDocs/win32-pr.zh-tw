---
title: 簽章
description: 著色器簽章是參數的清單，這些參數是從著色器函式輸入或輸出。
ms.assetid: c73a4f3e-e6fa-4e49-9ee8-4e200269dba7
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 37906222ec674c2c1bb5e1cdfea1cb2de2e1df3d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104990651"
---
# <a name="signatures"></a><span data-ttu-id="b7a4a-103">簽章</span><span class="sxs-lookup"><span data-stu-id="b7a4a-103">Signatures</span></span>

<span data-ttu-id="b7a4a-104">著色器簽章是參數的清單，這些參數是從著色器函式輸入或輸出。</span><span class="sxs-lookup"><span data-stu-id="b7a4a-104">A shader signature is a list of the parameters that are either input to or output from a shader function.</span></span> <span data-ttu-id="b7a4a-105">在 Direct3D 10 中，連續的階段會有效地共用暫存器陣列，其中輸出著色器 (或管線階段) 將資料寫入暫存器陣列中的特定位置，而輸入著色器必須從相同的位置讀取。</span><span class="sxs-lookup"><span data-stu-id="b7a4a-105">In Direct3D 10, adjacent stages effectively share a register array, where the output shader (or pipeline stage) writes data to specific locations in the register array and the input shader must read from the same locations.</span></span> <span data-ttu-id="b7a4a-106">API 會使用著色器簽章來系結具有輸入的著色器輸出，而不會造成語義解析的負擔。</span><span class="sxs-lookup"><span data-stu-id="b7a4a-106">The API uses shader signatures to bind shader outputs with inputs without the overhead of semantic resolution.</span></span>

<span data-ttu-id="b7a4a-107">在 Direct3D 10 中，輸入簽章是從著色器輸入宣告產生的，而且輸出簽章是從著色器輸出宣告產生的。</span><span class="sxs-lookup"><span data-stu-id="b7a4a-107">In Direct3D 10, input signatures are generated from a shader-input declaration and the output signature is generated from a shader-output declaration.</span></span> <span data-ttu-id="b7a4a-108">當輸出簽章是輸入簽章 (引數型別和訂單相符) 的嚴格子集時，就可以使用輸入簽章與輸出簽章相容。</span><span class="sxs-lookup"><span data-stu-id="b7a4a-108">An input signature is said to be compatible with an output signature when the output signature is a strict subset (argument type and order match) of the input signature.</span></span> <span data-ttu-id="b7a4a-109">達成此目的的最直接方式是將對應的著色器輸入和輸出連結到相同的結構類型。</span><span class="sxs-lookup"><span data-stu-id="b7a4a-109">The most straightforward way to achieve this is to link corresponding shader inputs and outputs by the same structure type.</span></span>

<span data-ttu-id="b7a4a-110">以下是相容簽章的範例。</span><span class="sxs-lookup"><span data-stu-id="b7a4a-110">Here is an example of compatible signatures.</span></span>


```
// Vertex Shader Output Signature
Struct VSOut
{
  float4 Pos: SV_Position;
  float3 MyNormal: Normal;
  float2 MyTex : Texcoord0;
}

// Pixel Shader Input Signature
Struct PSInWorks
{
  float4 Pos: SV_Position;
  float3 MyNormal: Normal;
}
```



<span data-ttu-id="b7a4a-111">以下是不相容的簽章範例：輸入簽章中的參數順序不符合輸出簽章中的順序。</span><span class="sxs-lookup"><span data-stu-id="b7a4a-111">Here is an example of incompatible signatures; the order of parameters in the input signature does not match the order in the output signature.</span></span>


```
// Vertex Shader Output Signature
Struct VSOut
{
  float4 Pos: SV_Position;
  float3 MyNormal: Normal;
  float2 MyTex : Texcoord0;
}

// Pixel Shader Input Signature
Struct PSInFails
{
  float3 MyNormal: Normal;
  float4 Pos: SV_Position;
}
```



<span data-ttu-id="b7a4a-112">PSInWorks 是 VSOut 的相容子集 (前兩個專案會將類型和順序與 VSOut) 中的前兩個專案相符。</span><span class="sxs-lookup"><span data-stu-id="b7a4a-112">PSInWorks is a compatible subset of VSOut (the first two entries match both type and order with the first two entries in VSOut).</span></span> <span data-ttu-id="b7a4a-113">但是，PSInFails 不相容，因為順序與 VSOut 不相符。</span><span class="sxs-lookup"><span data-stu-id="b7a4a-113">However, PSInFails is incompatible because the ordering does not match with VSOut.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b7a4a-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="b7a4a-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7a4a-115">函數</span><span class="sxs-lookup"><span data-stu-id="b7a4a-115">Functions</span></span>](dx-graphics-hlsl-functions.md)
</dt> </dl>

 

 




