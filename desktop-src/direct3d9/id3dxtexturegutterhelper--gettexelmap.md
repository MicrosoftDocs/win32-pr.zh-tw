---
description: 抓取每個材質的 (u，v) 材質座標。
ms.assetid: 7d8eecf8-6344-4a48-8338-b92ebb0ab2ef
title: 'ID3DXTextureGutterHelper：： GetTexelMap 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.GetTexelMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 321f5075bdfde3a5a3d707089867356b3f702230dd81d2a1c29b513a8cf8e1ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118800371"
---
# <a name="id3dxtexturegutterhelpergettexelmap-method"></a>ID3DXTextureGutterHelper：： GetTexelMap 方法

抓取每個材質的 (u，v) 材質座標。

## <a name="syntax"></a>語法


```C++
HRESULT GetTexelMap(
  [out] D3DXVECTOR2 *pTexelData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pTexelData* \[擴展\]
</dt> <dd>

類型： **[ **D3DXVECTOR2**](d3dxvector2.md)\***

以圖元為單位的位置指標 (u，v) 材質座標（每個材質所在位置）。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則會傳回下列值。D3DERR \_ INVALIDCALL

## <a name="remarks"></a>備註

針對 [**類別2和4材質**](id3dxtexturegutterhelper.md)，傳回的 (u，v) 材質座標會對應到最接近的三角形上最接近的點。

應用程式必須配置並管理 pTexelData。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 




