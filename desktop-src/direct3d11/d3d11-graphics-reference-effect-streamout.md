---
title: 資料流程輸出語法
description: 具有資料流程輸出的幾何著色器會使用特定語法來宣告。
ms.assetid: 58cf6503-0dde-4c88-837d-ae0e0eda17d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43980d79d9c338a965d7ab2f2ceb008411d9713dec935d953dd5a1854c40465b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096388"
---
# <a name="stream-out-syntax"></a>資料流程輸出語法

具有資料流程輸出的幾何著色器會使用特定語法來宣告。 本主題說明語法。 在效果執行時間中，會將此語法轉換成 [**ID3D11Device：： CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput)的呼叫。

## <a name="construct-syntax"></a>結構語法


```
[ StreamingShaderVar = ] ConstructGSWithSO( ShaderVar, "OutputDecl0" )
```





| 名稱                   | 描述                                                                                                                                                                                                                |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **StreamingShaderVar** | 選擇性。 使用資料流程來唯一識別幾何著色器變數名稱的 ASCI 字串。這是選擇性的，因為 ConstructGSWithSO 可以直接放在 SetGeometryShader 或 BindInterfaces 呼叫中。 |
| **ShaderVar**          | 幾何著色器或頂點著色器變數。                                                                                                                                                                               |
| **OutputDecl0**        | 字串，定義資料流程0中的著色器輸出資料流程處理。請參閱下面的語法。                                                                                                                                 |



 

這是在 fx 4 0 檔案中定義的語法 \_ \_ 。 請注意，在 gs \_ 4 \_ 0 和 vs \_ x 著色器中，只有一個資料串流。 產生的著色器會將一個資料流程輸出至串流輸出單元和轉譯器單位。


```
[ StreamingShaderVar = ] ConstructGSWithSO( ShaderVar, "OutputDecl0", "OutputDecl1", "OutputDecl2", 
"OutputDecl3", RasterizedStream )
```





| 名稱                   | 描述                                                                                                                                                                                                                |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **StreamingShaderVar** | 選擇性。 使用資料流程來唯一識別幾何著色器變數名稱的 ASCI 字串。這是選擇性的，因為 ConstructGSWithSO 可以直接放在 SetGeometryShader 或 BindInterfaces 呼叫中。 |
| **ShaderVar**          | 幾何著色器或頂點著色器變數。                                                                                                                                                                               |
| **OutputDecl0**        | 字串，定義資料流程0中的著色器輸出資料流程處理。請參閱下面的語法。                                                                                                                                 |
| **OutputDecl1**        | 字串，定義串流1中的著色器輸出資料流程處理。請參閱下面的語法。                                                                                                                                 |
| **OutputDecl2**        | 字串，定義串流2中的著色器輸出資料流程處理。請參閱下面的語法。                                                                                                                                 |
| **OutputDecl3**        | 字串，定義串流3中的著色器輸出資料流程處理。請參閱下面的語法。                                                                                                                                 |
| **RasterizedStream**   | 整數，指定要將哪個資料流程傳送至轉譯器。                                                                                                                                                         |



 

請注意，gs \_ 5 \_ 0 著色器最多可以定義四個數據流。 產生的著色器會針對每個非 **Null** 的輸出宣告，將一個資料流程輸出到資料流程輸出單位，並將一個資料流程輸出到轉譯器單位。

## <a name="stream-out-declaration-syntax"></a>資料流程輸出宣告語法


```
" [ Buffer: ] Semantic[ SemanticIndex ] [ .Mask ]; [ ... ; ] ... [ ... ;]"
```





| 名稱              | 描述                                                                                           |
|-------------------|-------------------------------------------------------------------------------------------------------|
| **Buffer**        | 選擇性。 整數，0 <= 緩衝區 < 4，指定要將值移至哪個資料流程輸出緩衝區。 |
| **語義**      | 字串，連同 SemanticIndex，指定要輸出的值。                                 |
| **SemanticIndex** | 選擇性。 與語義相關聯的索引。                                                         |
| **Mask**          | 選擇性。 元件遮罩，指出要輸出值的哪些元件。                       |



 

有一個特殊的語義，標示為 "$SKIP"，表示空的語義，將對應的記憶體保留在串流輸出緩衝區中。 $SKIP 語義不能有 SemanticIndex，但可以有遮罩。

整個資料流程輸出宣告可以是 **Null**。

## <a name="example"></a>範例


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[ (Direct3D 11) 的效果 ](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 




