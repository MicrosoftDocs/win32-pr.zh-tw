---
description: 必須由使用者執行以設定材質的回呼函式。
ms.assetid: 971802f4-ea7a-4906-83b8-0cd83111716e
title: 'ID3DXEffectStateManager：： SetTexture 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetTexture
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b395c19b65bb39b8328da24f727292f7dbe2a0f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104514641"
---
# <a name="id3dxeffectstatemanagersettexture-method"></a>ID3DXEffectStateManager：： SetTexture 方法

必須由使用者執行以設定材質的回呼函式。

## <a name="syntax"></a>語法


```C++
HRESULT SetTexture(
  [in] DWORD                  Stage,
  [in] LPDIRECT3DBASETEXTURE9 pTexture
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*Stage* \[in\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

要指派紋理的階段。 這是 [**IDirect3DDevice9：： SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) 或 [**IDirect3DDevice9：： SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate)中的索引值。

</dd> <dt>

*pTexture* \[在\]
</dt> <dd>

類型： **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**

紋理物件的指標。 這可以是任何 Direct3D 材質類型 (cube、磁片區等 ) 。 請參閱 [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

使用者執行的方法應該會傳回 S \_ OK。 如果回呼在設定裝置狀態時失敗，將會發生下列其中一種情況：

-   [**ID3DXEffect：： BeginPass**](id3dxeffect--beginpass.md)期間的效果將會失敗。
-   動態效果狀態呼叫 (例如 [**IDirect3DDevice9：： SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)) 將會失敗。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Effect。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
