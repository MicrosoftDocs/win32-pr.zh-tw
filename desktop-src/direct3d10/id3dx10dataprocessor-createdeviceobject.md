---
description: 建立裝置物件。
ms.assetid: 5b9b00de-c744-43c7-b383-1d3358c80741
title: 'ID3DX10DataProcessor：： CreateDeviceObject 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10DataProcessor.CreateDeviceObject
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: ca20de85e867cc8c444f05ea187fb314a6b983ad8c72a5f8ae921c0747bd9ce8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118540416"
---
# <a name="id3dx10dataprocessorcreatedeviceobject-method"></a>ID3DX10DataProcessor：： CreateDeviceObject 方法

建立裝置物件。

## <a name="syntax"></a>語法


```C++
HRESULT CreateDeviceObject(
  [out] void **ppDataObject
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppDataObject* \[擴展\]
</dt> <dd>

類型： **void \* \***

所建立裝置物件的指標位址。

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

[ID3DX10DataProcessor](id3dx10dataprocessor.md)
</dt> <dt>

[D3DX 介面](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




