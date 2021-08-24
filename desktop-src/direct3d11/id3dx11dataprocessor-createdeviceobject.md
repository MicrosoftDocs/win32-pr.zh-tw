---
title: 'ID3DX11DataProcessor CreateDeviceObject 方法 (D3DX11core .h) '
description: 請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 建立裝置物件。
ms.assetid: 797d216b-2f54-4d24-aa97-04be0c71f909
keywords:
- CreateDeviceObject 方法 Direct3D 11
- CreateDeviceObject 方法 Direct3D 11，ID3DX11DataProcessor 介面
- ID3DX11DataProcessor 介面 Direct3D 11，CreateDeviceObject 方法
topic_type:
- apiref
api_name:
- ID3DX11DataProcessor.CreateDeviceObject
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15627fc823de8a46a1299607f74694a0f93236082423910adf395b2b00ad57f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894928"
---
# <a name="id3dx11dataprocessorcreatedeviceobject-method"></a>ID3DX11DataProcessor：： CreateDeviceObject 方法

> [!Note]  
> D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，不支援 Windows Store 應用程式。

 

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

傳回值是 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)中列出的其中一個值。

## <a name="remarks"></a>備註

[**ID3DX11ThreadPump 介面**](id3dx11threadpump.md)會使用這個方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX11core。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3DX11 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DX11DataProcessor](id3dx11dataprocessor.md)
</dt> <dt>

[D3DX 介面](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





