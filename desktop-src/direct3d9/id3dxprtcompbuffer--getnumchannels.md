---
description: ID3DXPRTCompBuffer：： GetNumChannels 方法-抓取記憶體中用來儲存範例的色彩通道數目。
ms.assetid: 8b033cda-feec-4e74-a4c4-ea44b5fb12c7
title: 'ID3DXPRTCompBuffer：： GetNumChannels 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.GetNumChannels
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ef36ef0d48dc3e6d94abe15c4b37e1843130a6d6da1b1e6e6c543c551c850422
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118801476"
---
# <a name="id3dxprtcompbuffergetnumchannels-method"></a>ID3DXPRTCompBuffer：： GetNumChannels 方法

抓取記憶體中用來儲存範例的色彩通道數目。

## <a name="syntax"></a>語法


```C++
UINT GetNumChannels();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

類型： **[ **UINT**](../winprog/windows-data-types.md)**

傳回記憶體中用來儲存範例的色彩通道數目。 此值通常會是1以表示亮度值，或3表示 RGB 值。

## <a name="remarks"></a>備註

## <a name="requirements"></a>需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXPRTCompBuffer](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
