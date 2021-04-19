---
description: 使用記憶體複製來設定著色器常數的連續範圍。
ms.assetid: 8a3b5141-c67a-45b9-91c2-1877642164e3
title: 'ID3DXEffect：： SetRawValue 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.SetRawValue
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: cc3ce5eb547032ced5d0d79c533cefd1d2daab3a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982198"
---
# <a name="id3dxeffectsetrawvalue-method"></a>ID3DXEffect：： SetRawValue 方法

使用記憶體複製來設定著色器常數的連續範圍。

## <a name="syntax"></a>語法


```C++
HRESULT SetRawValue(
  [in] D3DXHANDLE Handle,
  [in] void       *pData,
  [in] DWORD      OffsetInBytes,
  [in] DWORD      Bytes
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*控制碼* \[在\]
</dt> <dd>

類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

要設定之值的控制碼，或傳入做為字串的值名稱。 傳遞控制碼更有效率。 請參閱 [處理 (Direct3D 9) ](handles.md)。

</dd> <dt>

*.pdata* \[在\]
</dt> <dd>

類型： **void \***

包含要設定之資料的緩衝區指標。 SetRawValue 會檢查是否有有效的記憶體，但不會檢查是否有有效的資料。

</dd> <dt>

*OffsetInBytes* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

效果資料開始與您要設定之效果常數開頭之間的位元組數目。

</dd> <dt>

*位元組* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

要設定的緩衝區大小（以位元組為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則傳回值可以是下列其中一項： E \_ INVALIDCALL。

## <a name="remarks"></a>備註

SetRawValue 是設定效果常數的最快速方式，因為它會執行記憶體複製而不執行驗證或任何資料轉換 (例如將資料列主要矩陣轉換成資料行主要矩陣) 。 使用 SetRawValue 來設定一連串連續的效果常數。 例如，您可以設定20個矩陣的陣列，其中包含20個對 [**ID3DXBaseEffect：： SetMatrix**](id3dxbaseeffect--setmatrix.md) 的呼叫，或使用單一 SetRawValue。

所有值都必須是 matrix4x4s 或 float4s，而且所有矩陣都必須是資料行主要順序。 Int 或 float 值會轉換成 float4;因此，強烈建議您只搭配 float4 或 matrix4x4 資料使用 SetRawValue。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Effect。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 
