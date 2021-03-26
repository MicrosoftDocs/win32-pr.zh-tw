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
ms.openlocfilehash: 97ab88961b22529accb4402fc2bd095ede5275c1
ms.sourcegitcommit: 477b1efe7d9c2f91d5f2ac588a20edf348b1c734
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2019
ms.locfileid: "104313887"
---
# <a name="append-directx-hlsl-stream-output-object"></a>附加 (DirectX HLSL Stream-Output 物件) 

將幾何-著色器輸出資料附加至現有的資料流程。



|                            |
|----------------------------|
| 附加 ( *StreamDataType*) ; |



 

## <a name="parameters"></a>參數



| 項目                                                                                                                             | 描述                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="StreamDataType"></span><span id="streamdatatype"></span><span id="STREAMDATATYPE"></span>**StreamDataType**<br/> | 資料輸入描述。 此描述必須與名為 [DataType](dx-graphics-hlsl-so-type.md)的資料流程物件範本參數相符。<br/> |



 

## <a name="return-value"></a>傳回值

None

## <a name="example"></a>範例

這段來自 [CubeMapGS 範例](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx) (的程式碼片段，) 顯示將三角形區域基本專案附加至資料流程輸出物件的部分範例。


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



## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此函數。



| 著色器模型                                              | 支援 |
|-----------------------------------------------------------|-----------|
| [著色器模型4](dx-graphics-hlsl-sm4.md)                | 是       |
| [著色器模型 3 (DirectX HLSL) ](dx-graphics-hlsl-sm3.md) | 不可以        |
| [著色器模型 2 (DirectX HLSL) ](dx-graphics-hlsl-sm2.md) | 不可以        |
| [著色器模型 1 (DirectX HLSL) ](dx-graphics-hlsl-sm1.md) | 不可以        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[資料流程輸出物件](dx-graphics-hlsl-so-type.md)
</dt> </dl>

 

 





