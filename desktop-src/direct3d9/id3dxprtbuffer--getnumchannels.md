---
description: ID3DXPRTBuffer：： GetNumChannels 方法-抓取記憶體中用來儲存範例的色彩通道數目。
ms.assetid: dd1e3590-78e1-41a2-9f15-79389d9a210a
title: 'ID3DXPRTBuffer：： GetNumChannels 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.GetNumChannels
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5dab8491128a242116c48a58e8edba1be9eb51b6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107336"
---
# <a name="id3dxprtbuffergetnumchannels-method"></a>ID3DXPRTBuffer：： GetNumChannels 方法

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

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> </dl>

 

 
