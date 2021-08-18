---
description: 鎖定頂點緩衝區，並取得頂點緩衝區記憶體的指標。
ms.assetid: afcd479c-b268-4720-b26c-88b82f1aab08
title: 'ID3DXBaseMesh：： LockVertexBuffer 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.LockVertexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5bb0cd8539a996b66ccf9f413e57ebf1d213fe6372e56b50b35abc5e210595f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987608"
---
# <a name="id3dxbasemeshlockvertexbuffer-method"></a>ID3DXBaseMesh：： LockVertexBuffer 方法

鎖定頂點緩衝區，並取得頂點緩衝區記憶體的指標。

## <a name="syntax"></a>語法


```C++
HRESULT LockVertexBuffer(
  [in]          DWORD  Flags,
  [out, retval] LPVOID *ppData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*旗標* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

零或多個鎖定旗標的組合，這些旗標描述要執行的鎖定類型。 針對此方法，有效的旗標為：

-   D3DLOCK \_ 捨棄
-   D3DLOCK \_ 沒有 \_ 中途 \_ 更新
-   D3DLOCK \_ NOSYSLOCK
-   D3DLOCK \_ READONLY
-   D3DLOCK \_ NOOVERWRITE

如需旗標的描述，請參閱 [D3DLOCK](d3dlock.md)。

</dd> <dt>

*ppData* \[退出，retval\]
</dt> <dd>

類型： **[ **LPVOID**](../winprog/windows-data-types.md)\***

\*包含頂點資料之緩衝區的 VOID 指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。

## <a name="remarks"></a>備註

使用頂點緩衝區時，您可以進行多次鎖定呼叫;不過，您必須確定鎖定呼叫的數目符合解除鎖定呼叫的數目。 任何目前設定的頂點緩衝區上的任何未完成鎖定計數，DrawPrimitive 呼叫都不會成功。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> </dl>

 

 
