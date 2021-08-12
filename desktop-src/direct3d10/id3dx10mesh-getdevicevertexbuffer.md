---
description: 在使用 ID3DX10Mesh：： CommitToDevice 認可至裝置之後，存取網格的頂點緩衝區。 這與 ID3DX10Mesh：： GetVertexBuffer 不同，它會在認可至裝置之前傳回頂點緩衝區。
ms.assetid: 621d9105-e55d-47b8-8557-8adb7db19d66
title: 'ID3DX10Mesh：： GetDeviceVertexBuffer 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetDeviceVertexBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 11493392f710fe3fd3bebab5187b61522434b268bf099489d84ea1cc3ec99309
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118540261"
---
# <a name="id3dx10meshgetdevicevertexbuffer-method"></a>ID3DX10Mesh：： GetDeviceVertexBuffer 方法

在使用 [**ID3DX10Mesh：： CommitToDevice**](id3dx10mesh-committodevice.md)認可至裝置之後，存取網格的頂點緩衝區。 這與 [**ID3DX10Mesh：： GetVertexBuffer**](id3dx10mesh-getvertexbuffer.md)不同，它會在認可至裝置之前傳回頂點緩衝區。

## <a name="syntax"></a>語法


```C++
HRESULT GetDeviceVertexBuffer(
  [in]  UINT         iBuffer,
  [out] ID3D10Buffer **ppVertexBuffer
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*windows.storage.streams.ibuffer* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

識別要存取之頂點緩衝區的索引。

</dd> <dt>

*ppVertexBuffer* \[擴展\]
</dt> <dd>

類型： **[ **ID3D10Buffer**](/windows/desktop/api/D3D10/nn-d3d10-id3d10buffer)\*\***

將頂點緩衝區認可至裝置之後。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[D3DX 介面](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
