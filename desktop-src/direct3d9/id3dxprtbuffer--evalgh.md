---
description: 將儲存的材質裝訂邊資料套用至 ID3DXPRTBuffer 材質緩衝區。
ms.assetid: 05cc0709-543a-4df5-980a-8549451d396b
title: 'ID3DXPRTBuffer：： EvalGH 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.EvalGH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 23896ff2514db7b5e12b164ea0c0a763b5d1d3b1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982244"
---
# <a name="id3dxprtbufferevalgh-method"></a>ID3DXPRTBuffer：： EvalGH 方法

將儲存的材質裝訂邊資料套用至 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 材質緩衝區。

## <a name="syntax"></a>語法


```C++
HRESULT EvalGH();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則會傳回下列值。

## <a name="remarks"></a>備註

這個方法會對 [**ID3DXTextureGutterHelper：： ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md) 進行內部呼叫，以抓取並套用材質裝訂邊資料。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> </dl>

 

 




