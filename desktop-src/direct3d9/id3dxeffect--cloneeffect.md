---
description: 建立效果的複本。
ms.assetid: 6272bce0-b712-4a61-afe2-8f572993b03e
title: 'ID3DXEffect：： CloneEffect 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.CloneEffect
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: eba2f6248bd1373ebf0aae55cf94103e2c269be7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "107000601"
---
# <a name="id3dxeffectcloneeffect-method"></a>ID3DXEffect：： CloneEffect 方法

建立效果的複本。

## <a name="syntax"></a>語法


```C++
HRESULT CloneEffect(
  [in]  LPDIRECT3DDEVICE9 pDevice,
  [out] LPD3DXEFFECT      *ppEffect
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pDevice* \[在\]
</dt> <dd>

類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，代表與效果相關聯的裝置。

</dd> <dt>

*ppEffect* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXEFFECT**](id3dxeffect.md)\***

[**ID3DXEffect**](id3dxeffect.md)介面的指標，其中包含複製的效果。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。

## <a name="remarks"></a>備註

> [!Note]  
> 如果使用者在效果建立期間指定了 [D3DXFX \_ not \_ CLONEABLE](d3dxfx.md) ，此函式將不會複製效果。

 

若要以已複製效果的有效技術來更新共用和非共用參數，請參閱 [**ID3DXEffect：： CommitChanges**](id3dxeffect--commitchanges.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Effect。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 
