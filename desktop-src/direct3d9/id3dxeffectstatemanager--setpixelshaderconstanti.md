---
description: ID3DXEffectStateManager：： SetPixelShaderConstantI 方法-必須由使用者實作為的回呼函式，以設定頂點著色器整數常數的陣列。
ms.assetid: 55f5747d-b7f8-4d13-ac2c-df2dcb160091
title: 'ID3DXEffectStateManager：： SetPixelShaderConstantI 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetPixelShaderConstantI
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: a817ac4e092eb9d8be2e4e2da02af051ae957dc97655b45e4e48dbe85b115ca3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119121501"
---
# <a name="id3dxeffectstatemanagersetpixelshaderconstanti-method"></a>ID3DXEffectStateManager：： SetPixelShaderConstantI 方法

必須由使用者所執行的回呼函式，以設定頂點著色器整數常數的陣列。

## <a name="syntax"></a>語法


```C++
HRESULT SetPixelShaderConstantI(
  [out]       UINT StartRegister,
  [out] const INT  *pConstantData,
  [out]       UINT RegisterCount
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*StartRegister* \[擴展\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

第一個常數暫存器的以零為基底的索引。

</dd> <dt>

*pConstantData* \[擴展\]
</dt> <dd>

類型： **Const [**INT**](../winprog/windows-data-types.md) \***

整數常數的陣列。

</dd> <dt>

*RegisterCount* \[擴展\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

PConstantData 中的暫存器數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

使用者執行的方法應該會傳回 S \_ OK。 如果回呼在設定裝置狀態時失敗，將會發生下列其中一種情況：

-   [**ID3DXEffect：： BeginPass**](id3dxeffect--beginpass.md)期間的效果將會失敗。
-   動態效果狀態呼叫 (例如 [**IDirect3DDevice9：： SetPixelShaderConstantI**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti)) 將會失敗。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Effect。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
