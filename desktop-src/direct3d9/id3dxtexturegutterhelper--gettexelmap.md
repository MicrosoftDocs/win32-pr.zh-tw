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
ms.openlocfilehash: af401eaa98ac4255b15961477b1ba2316e29edf0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322976"
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

 

 




