---
description: 鎖定索引緩衝區，並取得索引緩衝區記憶體的指標。
ms.assetid: c8941164-1f2a-4aed-b0bd-8130aac61da4
title: 'ID3DXBaseMesh：： LockIndexBuffer 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.LockIndexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 388915d0d11ff910c19a2c70b305597a79cd04bb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104035328"
---
# <a name="id3dxbasemeshlockindexbuffer-method"></a>ID3DXBaseMesh：： LockIndexBuffer 方法

鎖定索引緩衝區，並取得索引緩衝區記憶體的指標。

## <a name="syntax"></a>語法


```C++
HRESULT LockIndexBuffer(
  [in]          DWORD  Flags,
  [out, retval] LPVOID *ppData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*Flags* \[in\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

零或多個鎖定旗標的組合，這些旗標描述要執行的鎖定類型。 針對此方法，有效的旗標為：

-   D3DLOCK \_ 捨棄
-   D3DLOCK \_ 沒有 \_ 中途 \_ 更新
-   D3DLOCK \_ NOSYSLOCK
-   D3DLOCK \_ READONLY

如需旗標的描述，請參閱 [D3DLOCK](d3dlock.md)。

</dd> <dt>

*ppData* \[退出，retval\]
</dt> <dd>

類型： **[ **LPVOID**](../winprog/windows-data-types.md)\***

\*包含索引資料之緩衝區的 VOID 指標。 此緩衝區中的索引計數會等於 [**ID3DXBaseMesh：： GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* 3。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。

## <a name="remarks"></a>備註

使用索引緩衝區時，您可以進行多個鎖定呼叫。 不過，您必須確定鎖定呼叫的數目符合解除鎖定呼叫的數目。 任何目前設定的索引緩衝區上的任何未完成鎖定計數，DrawPrimitive 呼叫都不會成功。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> </dl>

 

 
