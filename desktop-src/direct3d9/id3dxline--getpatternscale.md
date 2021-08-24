---
description: 取得 stipple 模式比例值。
ms.assetid: cf80ae8c-493d-4f35-b4f9-5981e64cc842
title: 'ID3DXLine：： GetPatternScale 方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.GetPatternScale
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3799901d071da08ee1bb0de4994ed330fabe2d8fedf3b59ce556105f0a280e3f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119675139"
---
# <a name="id3dxlinegetpatternscale-method"></a>ID3DXLine：： GetPatternScale 方法

取得 stipple 模式比例值。

## <a name="syntax"></a>語法


```C++
FLOAT GetPatternScale();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

傳回用來調整 stipple 模式的值。 1.0 f 是預設值，不代表縮放比例。 小於 1.0 f 的值會壓縮模式，而大於1.0 的值會拉長模式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9core。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXLine](id3dxline.md)
</dt> <dt>

[**ID3DXLine::SetPatternScale**](id3dxline--setpatternscale.md)
</dt> </dl>

 

 
