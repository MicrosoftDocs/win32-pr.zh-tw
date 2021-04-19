---
description: 在使用 ID3DX10Mesh：： CommitToDevice 認可至裝置之後，存取網格的索引緩衝區。 這與 ID3DX10Mesh：： GetIndexBuffer 不同，它會在認可至裝置之前，傳回索引緩衝區。
ms.assetid: 94d21f50-91b5-4f8d-ac73-7a851bba8685
title: 'ID3DX10Mesh：： GetDeviceIndexBuffer 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetDeviceIndexBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 3ec3e65cfc4acb5a903bcf18d2f707d39127e975
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976508"
---
# <a name="id3dx10meshgetdeviceindexbuffer-method"></a>ID3DX10Mesh：： GetDeviceIndexBuffer 方法

在使用 [**ID3DX10Mesh：： CommitToDevice**](id3dx10mesh-committodevice.md)認可至裝置之後，存取網格的索引緩衝區。 這與 [**ID3DX10Mesh：： GetIndexBuffer**](id3dx10mesh-getindexbuffer.md)不同，它會在認可至裝置之前，傳回索引緩衝區。

## <a name="syntax"></a>語法


```C++
HRESULT GetDeviceIndexBuffer(
  [out] ID3D10Buffer **ppIndexBuffer
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppIndexBuffer* \[擴展\]
</dt> <dd>

類型： **[ **ID3D10Buffer**](/windows/desktop/api/D3D10/nn-d3d10-id3d10buffer)\*\***

索引緩衝區認可至裝置之後。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。

## <a name="remarks"></a>備註

如果網格的索引緩衝區尚未認可至裝置，此 API 將會在傳回緩衝區的指標之前，自動認可索引緩衝區。

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

 

 




