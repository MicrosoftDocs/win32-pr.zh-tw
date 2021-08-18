---
title: 使用者自訂類型
description: 使用下列語法來宣告使用者定義型別。
ms.assetid: 8ef18864-f456-4b52-af83-f9b1050a0bba
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ee73cd5afcda15bcc821d7fea5b648924829d483a33b9c67c140eed0b100e861
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119789308"
---
# <a name="user-defined-type"></a>使用者自訂類型

使用下列語法來宣告使用者定義型別。



|                                           |
|-------------------------------------------|
| typedef **\[ const \] 型別 \[ 名稱 \] 索引**; |



 

## <a name="parameters"></a>參數



| 項目                                                                                         | 描述                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="_const_"></span><span id="_CONST_"></span>**\[常量\]**<br/>                 | 選擇性。 此關鍵字會將類型明確標示為常數。<br/>             |
| <span id="Type"></span><span id="type"></span><span id="TYPE"></span>**類型**<br/>     | 識別資料類型;必須是其中一個 HLSL 內建資料類型。<br/>     |
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**名字**<br/>     | 可唯一識別變數名稱的 ASCII 字串。<br/>                 |
| <span id="Index"></span><span id="index"></span><span id="INDEX"></span>**指數**<br/> | 選擇性陣列大小。 必須是介於1到4（含）之間的不帶正負號的整數。<br/> |



 

除了內建的內建資料類型，HLSL 還支援遵循下列語法的使用者定義或自訂類型：

## <a name="remarks"></a>備註

使用者定義類型不區分大小寫。 為了方便起見，下列類型會自動定義在超級全域範圍中。


```
typedef vector <bool, #> bool#;
typedef vector <int, #> int#;
typedef vector <uint, #> uint#;
typedef vector <half, #> half#;
typedef vector <float, #> float#;
typedef vector <double, #> double#;

typedef matrix <bool, #, #> bool#x#;
typedef matrix <int, #, #> int#x#;
typedef matrix <uint, #, #> uint#x#;
typedef matrix <half, #, #> half#x#;
typedef matrix <float, #, #> float#x#;
typedef matrix <double, #, #> double#x#;
```



井字型大小 (\#) 代表介於1到4之間的整數數位。

為了與 DirectX 8 效果相容，下列類型會自動定義在超級全域範圍內：


```
typedef int DWORD;
typedef float FLOAT; 
typedef vector <float, 4> VECTOR;
typedef matrix <float, 4, 4> MATRIX;
typedef string STRING;
typedef texture TEXTURE;
typedef pixelshader PIXELSHADER;
typedef vertexshader VERTEXSHADER;
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[ (DirectX HLSL) 的資料類型 ](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 





