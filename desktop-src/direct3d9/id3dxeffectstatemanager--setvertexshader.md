---
description: 必須由使用者執行以設定頂點著色器的回呼函數。
ms.assetid: 8f3d3be3-c073-441d-a318-6d2cd5e7aca5
title: 'ID3DXEffectStateManager：： SetVertexShader 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetVertexShader
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5f52daf5174608985b18140d2e6efde849f0bd6292c00584ece3453cca33ebf0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118520920"
---
# <a name="id3dxeffectstatemanagersetvertexshader-method"></a>ID3DXEffectStateManager：： SetVertexShader 方法

必須由使用者執行以設定頂點著色器的回呼函數。

## <a name="syntax"></a>語法


```C++
HRESULT SetVertexShader(
  [in] LPDIRECT3DVERTEXSHADER9 pShader
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pShader* \[在\]
</dt> <dd>

類型： **[ **LPDIRECT3DVERTEXSHADER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexshader9)**

頂點著色器物件的指標。 請參閱 [**IDirect3DVertexShader9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexshader9)。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

使用者執行的方法應該會傳回 S \_ OK。 如果回呼在設定裝置狀態時失敗，將會發生下列其中一種情況：

-   [**ID3DXEffect：： BeginPass**](id3dxeffect--beginpass.md)期間的效果將會失敗。
-   動態效果狀態呼叫 (例如 [**IDirect3DDevice9：： SetVertexShader**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader)) 將會失敗。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Effect。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
