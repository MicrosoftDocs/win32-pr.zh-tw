---
description: 抓取記憶體中用來儲存範例的色彩通道數目。
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
ms.openlocfilehash: 99456c6386a822489eca6beef41f639008007778
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106975715"
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

 

 
