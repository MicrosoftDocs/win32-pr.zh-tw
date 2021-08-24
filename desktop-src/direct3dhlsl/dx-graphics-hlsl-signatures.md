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
ms.openlocfilehash: 5631dbe473b2e3eea0abb525e58621faf9c5137dd5dc3d743bde53b0ae258f25
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119789578"
---
# <a name="signatures"></a>簽章

著色器簽章是參數的清單，這些參數是從著色器函式輸入或輸出。 在 Direct3D 10 中，連續的階段會有效地共用暫存器陣列，其中輸出著色器 (或管線階段) 將資料寫入暫存器陣列中的特定位置，而輸入著色器必須從相同的位置讀取。 API 會使用著色器簽章來系結具有輸入的著色器輸出，而不會造成語義解析的負擔。

在 Direct3D 10 中，輸入簽章是從著色器輸入宣告產生的，而且輸出簽章是從著色器輸出宣告產生的。 當輸出簽章是輸入簽章 (引數型別和訂單相符) 的嚴格子集時，就可以使用輸入簽章與輸出簽章相容。 達成此目的的最直接方式是將對應的著色器輸入和輸出連結到相同的結構類型。

以下是相容簽章的範例。


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



以下是不相容的簽章範例：輸入簽章中的參數順序不符合輸出簽章中的順序。


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



PSInWorks 是 VSOut 的相容子集 (前兩個專案會將類型和順序與 VSOut) 中的前兩個專案相符。 但是，PSInFails 不相容，因為順序與 VSOut 不相符。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[函數](dx-graphics-hlsl-functions.md)
</dt> </dl>

 

 




