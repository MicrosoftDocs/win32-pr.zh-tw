---
title: 'ID3DX11DataLoader 摧毀方法 (D3DX11core .h) '
description: 請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 在工作專案完成後終結載入器。
ms.assetid: 5d86c4ad-3eb6-421f-bb77-c88e8f5b42bb
keywords:
- 終結方法 Direct3D 11
- 終結方法 Direct3D 11，ID3DX11DataLoader 介面
- ID3DX11DataLoader 介面 Direct3D 11，摧毀方法
topic_type:
- apiref
api_name:
- ID3DX11DataLoader.Destroy
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12c3a1c6511a00d66704c104b3b69150a8509e41
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974723"
---
# <a name="id3dx11dataloaderdestroy-method"></a>ID3DX11DataLoader：:D estroy 方法

> [!Note]  
> D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。

 

在工作專案完成後終結載入器。

## <a name="syntax"></a>語法


```C++
HRESULT Destroy();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

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

[ID3DX11DataLoader](id3dx11dataloader.md)
</dt> <dt>

[D3DX 介面](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





