---
description: 設定材質 barycentric 座標。
ms.assetid: 6c7c74aa-71a3-45aa-9b18-6409fbd63bda
title: 'ID3DXTextureGutterHelper：： SetBaryMap 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.SetBaryMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5e3de61913041a4e59e075ea42dacc308c1ce5f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196402"
---
# <a name="id3dxtexturegutterhelpersetbarymap-method"></a>ID3DXTextureGutterHelper：： SetBaryMap 方法

設定材質 barycentric 座標。

## <a name="syntax"></a>語法


```C++
HRESULT SetBaryMap(
  [in] D3DXVECTOR2 *pBaryData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pBaryData* \[在\]
</dt> <dd>

類型： **[ **D3DXVECTOR2**](d3dxvector2.md)\***

[**D3DXVECTOR2**](d3dxvector2.md)結構的指標，其中包含每個材質的前兩個 barycentric 座標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則會傳回下列值。D3DERR \_ INVALIDCALL

## <a name="remarks"></a>備註

第三個 barycentric 座標是由下列各項所提供：


```
1 - ( pBaryData.x + pBaryData.y )
```



Barycentric 會將輸入協調為此方法的輸入，僅適用于有效的 (非類別 0) 材質。 [**ID3DXTextureGutterHelper：： GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) 會針對有效的材質傳回非零值。

Barycentric 座標會根據三角形的頂點定義三角形內的點。 如需 barycentric 座標的更深入說明，請參閱 [Mathworld 的 Barycentric 座標描述](http://mathworld.wolfram.com/BarycentricCoordinates.html)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 




