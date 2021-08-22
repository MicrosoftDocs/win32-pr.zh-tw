---
description: 必須由使用者執行以設定材質狀態的回呼函式。
ms.assetid: 4c5e903f-551b-4346-a5eb-301a3a5b9b44
title: 'ID3DXEffectStateManager：： SetMaterial 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetMaterial
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 67e8b1ad498b5aacbae7aaad2d6b63fa406d54d6315a4e75b3028efe3107eaf8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118802872"
---
# <a name="id3dxeffectstatemanagersetmaterial-method"></a>ID3DXEffectStateManager：： SetMaterial 方法

必須由使用者執行以設定材質狀態的回呼函式。

## <a name="syntax"></a>語法


```C++
HRESULT SetMaterial(
  [in] const D3DMATERIAL9 *pMaterial
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pMaterial* \[在\]
</dt> <dd>

Type： **Const [**D3DMATERIAL9**](d3dmaterial9.md) \***

材質狀態的指標。 請參閱 [**D3DMATERIAL9**](d3dmaterial9.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

使用者執行的方法應該會傳回 S \_ OK。 如果回呼在設定裝置狀態時失敗，將會發生下列其中一種情況：

-   [**ID3DXEffect：： BeginPass**](id3dxeffect--beginpass.md)期間的效果將會失敗。
-   動態效果狀態呼叫 (例如 [**IDirect3DDevice9：： SetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial)) 將會失敗。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Effect。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
