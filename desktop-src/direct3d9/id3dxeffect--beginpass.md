---
description: 在主動技術內開始進行。
ms.assetid: fbb2bf1c-e37a-4117-8c3c-5f5b6a267301
title: 'ID3DXEffect：： BeginPass 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.BeginPass
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 56a2648f65c3747f8a98fc0cdbd3ed06cea560b9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992720"
---
# <a name="id3dxeffectbeginpass-method"></a>ID3DXEffect：： BeginPass 方法

在主動技術內開始進行。

## <a name="syntax"></a>語法


```C++
HRESULT BeginPass(
  [in] UINT Pass
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*Pass* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

技術中以零為基底的整數索引。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。

## <a name="remarks"></a>備註

應用程式會藉由呼叫 **ID3DXEffect：： BeginPass**，在效果系統內的一個作用中的) 技巧內設定一個主動傳遞 (。 應用程式會藉由呼叫 [**ID3DXEffect：： EndPass**](id3dxeffect--endpass.md)來表示主動傳遞的結尾。 **ID3DXEffect：： BeginPass** 和 **ID3DXEffect：： EndPass** 必須在成對的 [**ID3DXEffect：： Begin**](id3dxeffect--begin.md) 和 [**ID3DXEffect：： End**](id3dxeffect--end.md) 呼叫內的配對配對中進行。

如果應用程式使用 **ID3DXEffect：： BeginPass** ID3DXEffect：： EndPass 比對配對內的任何 [**effect：： Setx**](id3dxeffect.md)方法來變更任何效果狀態 / [](id3dxeffect--endpass.md) ，則應用程式必須呼叫 [**ID3DXEffect：： CommitChanges**](id3dxeffect--commitchanges.md) ，以設定狀態變更的裝置更新。 如果 **ID3DXEffect：： BeginPass** 和 **ID3DXEffect：： EndPass** 比對配對中沒有發生狀態變更，則不需要呼叫 **ID3DXEffect：： CommitChanges**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Effect。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 
