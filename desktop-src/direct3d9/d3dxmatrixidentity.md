---
description: 建立識別矩陣。
ms.assetid: 0dd6d4fb-284c-4d01-9a85-63aa08e71723
title: 'D3DXMatrixIdentity 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixIdentity
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 10dffa12a379754006ca65d1239be96632a68b93
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946046"
---
# <a name="d3dxmatrixidentity-function"></a>D3DXMatrixIdentity 函式

建立識別矩陣。

## <a name="syntax"></a>語法


```C++
D3DXMATRIX* D3DXMatrixIdentity(
  _Inout_ D3DXMATRIX *pOut
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*不悅* \[in、out\]
</dt> <dd>

類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***

[**D3DXMATRIX**](d3dxmatrix.md)結構的指標，此結構是作業的結果。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***

[**D3DXMATRIX**](d3dxmatrix.md)結構的指標，該結構為識別矩陣。

## <a name="remarks"></a>備註

識別矩陣是一個矩陣，其中所有係數都是0，但 \[ 1、1 \] \[ 2、2 \] \[ 3、3 \] \[ 4、4個 \] 係數設定為1。 識別矩陣的特殊之處，就是當它套用至頂點時，不會變更。 身分識別矩陣可作為矩陣的起點，以修改頂點值以建立旋轉、轉譯，以及可由4個4個4個矩陣表示的任何其他轉換。

此函式的傳回值與 *不悅* 參數中所傳回的值相同。 如此一來， **D3DXMatrixIdentity** 函式就可以用來做為另一個函式的參數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9math。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixIsIdentity**](d3dxmatrixisidentity.md)
</dt> </dl>

 

 




