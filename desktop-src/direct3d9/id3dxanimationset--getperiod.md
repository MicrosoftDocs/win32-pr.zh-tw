---
description: 取得動畫集合的期間。
ms.assetid: 0bb19ec1-c918-44b6-83b0-4fdbb4e1a485
title: 'ID3DXAnimationSet：： GetPeriod 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetPeriod
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d8e984d1593fbbd79561bbb15fb27b62a9961c1830c42465ed529f08c374e180
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118522327"
---
# <a name="id3dxanimationsetgetperiod-method"></a>ID3DXAnimationSet：： GetPeriod 方法

取得動畫集合的期間。

## <a name="syntax"></a>語法


```C++
DOUBLE GetPeriod();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

類型： **[ **DOUBLE**](../winprog/windows-data-types.md)**

動畫集合的期間。

## <a name="remarks"></a>備註

期間是動畫主要畫面格有效的時間範圍。 在迴圈的動畫中，這是迴圈的期間。 在 (中指定主要畫面格的時間單位（例如，秒) 是由應用程式所決定）。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9anim。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXAnimationSet](id3dxanimationset.md)
</dt> </dl>

 

 
