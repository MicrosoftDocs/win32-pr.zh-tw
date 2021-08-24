---
description: 必須由使用者執行來設定轉譯狀態的回呼函式。
ms.assetid: a5a27e30-c141-44a4-b8d4-38c1d6076b2a
title: 'ID3DXEffectStateManager：： Graphicsdevice 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetRenderState
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: c7d34dae1d0789b80d896b72be7e35420daf587986ac2725e880b81597b15e88
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119459618"
---
# <a name="id3dxeffectstatemanagersetrenderstate-method"></a>ID3DXEffectStateManager：： Graphicsdevice 方法

必須由使用者執行來設定轉譯狀態的回呼函式。

## <a name="syntax"></a>語法


```C++
HRESULT SetRenderState(
  [in] D3DRENDERSTATETYPE State,
  [in] DWORD              Value
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*狀態* \[在\]
</dt> <dd>

類型： **[ **D3DRENDERSTATETYPE**](./d3drenderstatetype.md)**

要設定的呈現狀態。 [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)

</dd> <dt>

*值* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

呈現狀態值。 請參閱 [效果狀態 (Direct3D 9) ](effect-states.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

使用者執行的方法應該會傳回 S \_ OK。 如果回呼在設定裝置狀態時失敗，將會發生下列其中一種情況：

-   [**ID3DXEffect：： BeginPass**](id3dxeffect--beginpass.md)期間的效果將會失敗。
-   動態效果狀態呼叫 (例如 [**IDirect3DDevice9：： graphicsdevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)) 將會失敗。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Effect。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
