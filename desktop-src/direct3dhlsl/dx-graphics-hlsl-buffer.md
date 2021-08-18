---
title: 緩衝區類型
description: 使用下列語法來宣告緩衝區變數。
ms.assetid: f21f0de5-58e3-466b-97bb-e4e7efa9cc1c
keywords:
- 緩衝區類型 HLSL
topic_type:
- apiref
api_name:
- Buffer Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 78d0b452a387ed1d4bf750062963996d0248fa249954a99be581118560866123
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120342"
---
# <a name="buffer-type"></a>緩衝區類型

使用下列語法來宣告緩衝區變數。



| 緩衝區<*類型* >  *名稱*; |
|------------------------------|



 

## <a name="parameters"></a>參數

<dl> <dt>

<span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>**緩衝區**
</dt> <dd>

必要關鍵字。

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>*類型*
</dt> <dd>

其中一個純 [量](dx-graphics-hlsl-scalar.md)、 [向量](dx-graphics-hlsl-vector.md)和某些 [矩陣](dx-graphics-hlsl-matrix.md) HLSL 類型。 您可以宣告具有矩陣的緩衝區變數，只要它符合 4 32 位數量即可。 因此，您可以撰寫 `Buffer<float2x2>` 。 但 `Buffer<float4x4>` 太大，編譯器將會產生錯誤。

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>*名字*
</dt> <dd>

可唯一識別變數名稱的 ASCII 字串。

</dd> </dl>

## <a name="example"></a>範例

以下是 [PipesGS 範例](https://msdn.microsoft.com/library/Ee416423(v=VS.85).aspx)中 PipesGS 檔案的緩衝區宣告範例。


```
Buffer<float4> g_Buffer;
```



使用 Load HLSL 內建函式的多 [**載**](dx-graphics-hlsl-to-load.md) 版本，從緩衝區讀取資料，此函式會採用一個輸入參數 (整數索引) 。 緩衝區的存取方式就像是元素陣列;因此，此範例會讀取第二個元素。


```
float4 bufferData = g_Buffer.Load( 1 );
```



使用 [資料流程輸出階段](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-stream-stage) 將資料輸出到緩衝區。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[ (DirectX HLSL) 的資料類型 ](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 