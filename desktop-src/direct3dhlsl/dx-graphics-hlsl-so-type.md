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
# <a name="stream-output-object"></a>Stream-Output 物件

資料流程輸出物件是樣板化物件，可將資料從 [幾何著色器階段](/previous-versions//bb205146(v=vs.85))流出。 使用下列語法來宣告資料流程輸出物件。



| inout *StreamOutputObject* < *資料類型* >  *名稱;* |
|------------------------------------------------------|



 

## <a name="parameters"></a>參數

<dl> <dt>

<span id="StreamOutputObject___________________________DataType_________________________________________Name"></span><span id="streamoutputobject___________________________datatype_________________________________________name"></span><span id="STREAMOUTPUTOBJECT___________________________DATATYPE_________________________________________NAME"></span>*StreamOutputObject*  < *DataType*  >   *名稱*
</dt> <dd>

資料流程輸出物件 (因此) 宣告。



| Stream-Output 物件類型 | Description                       |
|----------------------------|-----------------------------------|
| *PointStream*              | 一系列的點基本    |
| *LineStream*               | 行基本類型的序列     |
| *TriangleStream*           | 三角形基本類型的序列 |



 

*DataType* -Output 資料類型;可以是任何 [HLSL 資料類型](dx-graphics-hlsl-data-types.md)。 必須以角括弧括住。

*名稱* -變數名稱;可唯一識別物件的 ASCII 字串。

</dd> </dl>

## <a name="example"></a>範例

這是資料流程輸出物件宣告的範例，它會串流出其資料是由結構中的 PS 立方體貼圖所定義的三角形基本類型 \_ \_ 。 幾何著色器僅限產生18個頂點。


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



這是來自 [CubeMapGS 範例](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)的程式碼片段。

## <a name="stream-output-object-methods"></a>Stream-Output 物件方法

使用下列語法來呼叫資料流程輸出物件方法。


```
Object.Method
```



會實作為下列方法。



| 方法                                              | 描述                                                      |
|------------------------------------------------------|------------------------------------------------------------------|
| [Append](dx-graphics-hlsl-so-append.md)             | 將輸出資料附加至現有的資料流程。                        |
| [RestartStrip](dx-graphics-hlsl-so-restartstrip.md) | 結束目前的基本區域並啟動新的基本區域。 |



 

## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此物件。



| 著色器模型                                                        | 支援 |
|---------------------------------------------------------------------|-----------|
| [著色器模型 4](dx-graphics-hlsl-sm4.md) 和更高的著色器模型 | 是       |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器模型4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 