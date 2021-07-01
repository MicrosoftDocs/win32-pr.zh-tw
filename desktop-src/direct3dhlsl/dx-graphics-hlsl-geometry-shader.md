---
title: Geometry-Shader 物件
description: 幾何著色器物件會處理整個基本專案。 使用下列語法來宣告幾何著色器物件。
ms.assetid: d5c1c22b-6fa6-40a8-900f-6d74f74468c1
keywords:
- 'maxvertexcount (DirectX HLSL) '
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e06bbc184a4b5f82d5edaaf7fdbfbd55f1906f12
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120613"
---
# <a name="geometry-shader-object"></a>Geometry-Shader 物件

幾何著色器物件會處理整個基本專案。 使用下列語法來宣告幾何著色器物件。

\[maxvertexcount (*NumVerts*) \] Void *ShaderName* ( *PrimitiveType DataType Name \[ NumElements \]*，inout *StreamOutputObject* ) ;



 

## <a name="parameters"></a>參數

<dl> <dt>

<span id="_maxvertexcount_NumVerts__"></span><span id="_maxvertexcount_numverts__"></span><span id="_MAXVERTEXCOUNT_NUMVERTS__"></span>\[maxvertexcount (*NumVerts*) \]
</dt> <dd>

\[\]表示要建立的最大頂點數目。

-   \[maxvertexcount () \] 必要關鍵字; 括弧和括弧是正確語法的必要字元。
-   *NumVerts* -代表頂點數目的整數數位。

</dd> <dt>

<span id="ShaderName"></span><span id="shadername"></span><span id="SHADERNAME"></span>*ShaderName*
</dt> <dd>

\[\]包含幾何著色器函式唯一名稱的 ASCII 字串。

</dd> <dt>

<span id="PrimitiveType_DataType_Name___NumElements__"></span><span id="primitivetype_datatype_name___numelements__"></span><span id="PRIMITIVETYPE_DATATYPE_NAME___NUMELEMENTS__"></span>*PrimitiveType DataType Name \[ NumElements \]*
</dt> <dd>

*PrimitiveType* -基本型別，決定基本資料的順序。



| 基本類型 | 描述                                                   |
|----------------|---------------------------------------------------------------|
| *點*        | 點清單                                                    |
| *line*         | 行清單或行帶                                       |
| *三角形*     | 三角形清單或三角形條紋                               |
| *lineadj*      | 連續的行清單或具有連續的行帶         |
| *triangleadj*  | 具有連續的相鄰或三角形條紋的三角形清單 |



 

  -  DataType \[在 \] 輸入資料類型中，可以是任何[HLSL 資料類型](dx-graphics-hlsl-data-types.md)。

*名稱* -引數名稱;這是 ASCII 字串。

*NumElements* -輸入的陣列大小，這取決於下表所示的 *PrimitiveType* 。

| 基本類型 | NumElements                                                                                                  |
|----------------|--------------------------------------------------------------------------------------------------------------|
| *點*        | \[1\]<br/> 您一次只能在一個點上操作。<br/>                                         |
| *line*         | \[2\]<br/> 一行需要兩個頂點。<br/>                                                    |
| *三角形*     | \[3\]<br/> 三角形需要三個頂點。<br/>                                              |
| *lineadj*      | \[4\]<br/> Lineadj 有兩個端點：因此，它需要四個頂點。<br/>                    |
| *triangleadj*  | \[6\]<br/> Triangleadj 框線三個三角形;因此，它需要六個頂點。<br/> |



 

</dd> <dt>

<span id="StreamOutputObject"></span><span id="streamoutputobject"></span><span id="STREAMOUTPUTOBJECT"></span>*StreamOutputObject*
</dt> <dd>

[資料流程輸出物件](dx-graphics-hlsl-so-type.md)的宣告。

</dd> </dl>

## <a name="return-value"></a>傳回值

無

## <a name="remarks"></a>備註

下圖顯示幾何著色器物件的各種基本類型。

![幾何著色器物件的各種基本類型圖例](images/d3d11-gsinputs1.png)

下圖顯示幾何著色器調用。

![幾何著色器調用的圖例](images/d3d11-gsinputs2.png)

## <a name="examples"></a>範例

此範例來自 [Direct3D 10 著色器模型4.0 研討會](https://msdn.microsoft.com/library/Ee416554(v=VS.85).aspx)的練習1。


```
[maxvertexcount(3)]
void GSScene( triangleadj GSSceneIn input[6], inout TriangleStream<PSSceneIn> OutputStream )
{   
    PSSceneIn output = (PSSceneIn)0;

    for( uint i=0; i<6; i+=2 )
    {
        output.Pos = input[i].Pos;
        output.Norm = input[i].Norm;
        output.Tex = input[i].Tex;
        
        OutputStream.Append( output );
    }
    
    OutputStream.RestartStrip();
}
```



## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此物件。



| 著色器模型                                                        | 支援 |
|---------------------------------------------------------------------|-----------|
| [著色器模型 4](dx-graphics-hlsl-sm4.md) 和更高的著色器模型 | 是       |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器模型4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 





