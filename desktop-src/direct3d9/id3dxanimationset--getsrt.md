---
description: 取得動畫集合的縮放、旋轉和轉譯值。
ms.assetid: 84fc56f3-15bf-4e27-ad06-57fab94f3a33
title: 'ID3DXAnimationSet：： GetSRT 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetSRT
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: baa1b882972a91626b19194f83655ea1839877943f7463be8991167eb72d17fa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119791068"
---
# <a name="id3dxanimationsetgetsrt-method"></a>ID3DXAnimationSet：： GetSRT 方法

取得動畫集合的縮放、旋轉和轉譯值。

## <a name="syntax"></a>語法


```C++
HRESULT GetSRT(
  [in]  DOUBLE         PeriodicPosition,
  [in]  UINT           Animation,
  [out] D3DXVECTOR3    *pScale,
  [out] D3DXQUATERNION *pRotation,
  [out] D3DXVECTOR3    *pTranslation
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*PeriodicPosition* \[在\]
</dt> <dd>

類型： **[ **DOUBLE**](../winprog/windows-data-types.md)**

動畫集合的位置。 您可以藉由呼叫 [**ID3DXAnimationSet：： GetPeriodicPosition**](id3dxanimationset--getperiodicposition.md)來取得位置。

</dd> <dt>

*動畫* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

動畫索引。

</dd> <dt>

*pScale* \[擴展\]
</dt> <dd>

類型： **[ **D3DXVECTOR3**](d3dxvector3.md)\***

描述動畫集合尺規的 [**D3DXVECTOR3**](d3dxvector3.md) 向量指標。

</dd> <dt>

*pRotation* \[擴展\]
</dt> <dd>

類型： **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

[**D3DXQUATERNION**](d3dxquaternion.md)四元數的指標，該四元數描述動畫集合的旋轉。

</dd> <dt>

*pTranslation* \[擴展\]
</dt> <dd>

類型： **[ **D3DXVECTOR3**](d3dxvector3.md)\***

描述動畫集合轉譯的 [**D3DXVECTOR3**](d3dxvector3.md) 向量指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

這個方法的傳回值是由應用程式設計人員所執行。 一般情況下，如果沒有發生錯誤，請將方法程式設計為傳回「D3D \_ 正常」。 否則，請將方法程式設計成從 [D3DERR](d3derr.md) 或 [**D3DXERR**](./d3dxerr.md)傳回適當的錯誤訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9anim。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXAnimationSet](id3dxanimationset.md)
</dt> </dl>

 

 
