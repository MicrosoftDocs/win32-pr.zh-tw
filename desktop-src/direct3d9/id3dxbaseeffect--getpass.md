---
description: 取得傳遞的控制碼。
ms.assetid: 71332f6a-18fe-4702-8620-6d16b835ba8f
title: 'ID3DXBaseEffect：： GetPass 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetPass
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 4602970ffd67492c8f98317488686b454a2698b7e94048da2894982c7ce78bae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987768"
---
# <a name="id3dxbaseeffectgetpass-method"></a>ID3DXBaseEffect：： GetPass 方法

取得傳遞的控制碼。

## <a name="syntax"></a>語法


```C++
D3DXHANDLE GetPass(
  [in] D3DXHANDLE hTechnique,
  [in] UINT       Index
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hTechnique* \[在\]
</dt> <dd>

類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

父技術的控制碼。 請參閱 [處理 (Direct3D 9) ](handles.md)。

</dd> <dt>

*索引* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

傳遞的索引。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

傳回指定之技術內所指定傳遞的控制碼，如果索引無效，則傳回 **Null** 。 請參閱 [處理 (Direct3D 9) ](handles.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Effect。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 
