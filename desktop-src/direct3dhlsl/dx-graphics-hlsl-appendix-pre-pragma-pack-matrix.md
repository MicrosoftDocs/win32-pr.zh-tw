---
title: pack_matrix pragma 指示詞
description: 指定矩陣之封裝對齊的 Pragma 指示詞。
ms.assetid: e77dc007-d915-4d78-9fff-d44d4999e4da
keywords:
- pack_matrix pragma 指示詞 HLSL
topic_type:
- apiref
api_name:
- pack_matrix pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4bb5474702a1caba3f772002c34677601715caff
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104022473"
---
# <a name="pack_matrix-pragma-directive"></a>pack \_ 矩陣 pragma 指示詞

指定矩陣之封裝對齊的 Pragma 指示詞。



| \#pragma pack \_ 矩陣 ( *對齊* )  |
|--------------------------------------|



 

## <a name="parameters"></a>參數



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>項目</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="alignment"></span><span id="ALIGNMENT"></span><em>對準</em><br/></td>
<td>矩陣的對齊設定。 此參數可以採用下表所列的其中一個值。 <br/> 
<table>
<thead>
<tr class="header">
<th>值</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>column_major</td>
<td>預設值。 將矩陣封裝對齊設定為數據行主要。</td>
</tr>
<tr class="even">
<td>row_major</td>
<td>將矩陣封裝對齊設定為 [資料列主要]。</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="examples"></a>範例

下列範例會將矩陣封裝對齊設定為 [資料列主要]。


```
#pragma pack_matrix( row_major )
```



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ (DirectX HLSL) 的預處理器指示詞 ](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[\# (DirectX HLSL) 的 pragma 指示詞 ](dx-graphics-hlsl-appendix-pre-pragma.md)
</dt> </dl>

 

 





