---
description: 將緩衝區中的每個值乘以常數值。
ms.assetid: 3d7ef530-b83a-4123-a2ed-fff2b21378ee
title: 'ID3DXPRTBuffer：： ScaleBuffer 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.ScaleBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 05bdd066f4b7c33ad06f089551f16f0489608c83
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992136"
---
# <a name="id3dxprtbufferscalebuffer-method"></a>ID3DXPRTBuffer：： ScaleBuffer 方法

將緩衝區中的每個值乘以常數值。

## <a name="syntax"></a>語法


```C++
HRESULT ScaleBuffer(
  [in] FLOAT Scale
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*調整規模* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

用來調整緩衝區的常數值。 緩衝區中的每個值都是由這個值的乘積和原始的緩衝區值所取代。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則會傳回下列值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> </dl>

 

 
