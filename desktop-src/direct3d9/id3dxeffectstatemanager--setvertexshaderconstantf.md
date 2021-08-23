---
description: ID3DXEffectStateManager：： SetVertexShaderConstantF 方法-必須由使用者所執行的回呼函式，以設定頂點著色器浮點數常數的陣列。
ms.assetid: 3a13040d-5d5a-4454-bf11-cda9653585c0
title: 'ID3DXEffectStateManager：： SetVertexShaderConstantF 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetVertexShaderConstantF
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: aecc510a01bbb461f9f8742f2125b39913335c2ff9b135083f0f59f3f6544b85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748558"
---
# <a name="id3dxeffectstatemanagersetvertexshaderconstantf-method"></a>ID3DXEffectStateManager：： SetVertexShaderConstantF 方法

必須由使用者所執行的回呼函式，以設定頂點著色器浮點數常數的陣列。

## <a name="syntax"></a>語法


```C++
HRESULT SetVertexShaderConstantF(
  [out]       UINT  StartRegister,
  [out] const FLOAT *pConstantData,
  [out]       UINT  RegisterCount
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

Type： **Const [**FLOAT**](../winprog/windows-data-types.md) \***

浮點數常數的陣列。

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
-   動態效果狀態呼叫 (例如 [**IDirect3DDevice9：： SetVertexShaderConstantF**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf)) 將會失敗。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Effect。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
