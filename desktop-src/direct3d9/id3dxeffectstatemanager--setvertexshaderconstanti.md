---
description: ID3DXEffectStateManager：： SetVertexShaderConstantI 方法-必須由使用者實作為的回呼函式，以設定頂點著色器整數常數的陣列。
ms.assetid: 0035c97a-1b17-4665-9032-7b3b9a9d2cff
title: 'ID3DXEffectStateManager：： SetVertexShaderConstantI 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetVertexShaderConstantI
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 949f2cb23e15e3cfb99fcb6880795cfbd6019a8c858198b23bb9db6508714d44
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119856688"
---
# <a name="id3dxeffectstatemanagersetvertexshaderconstanti-method"></a>ID3DXEffectStateManager：： SetVertexShaderConstantI 方法

必須由使用者所執行的回呼函式，以設定頂點著色器整數常數的陣列。

## <a name="syntax"></a>語法


```C++
HRESULT SetVertexShaderConstantI(
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
-   動態效果狀態呼叫 (例如 [**IDirect3DDevice9：： SetVertexShaderConstantI**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti)) 將會失敗。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Effect。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
