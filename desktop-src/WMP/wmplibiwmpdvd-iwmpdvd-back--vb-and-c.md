---
title: IWMPDVD back 方法
description: Back 方法會將顯示從子功能表變更為其父功能表。
ms.assetid: 81d033d4-f570-44a5-898a-e419101c04fa
keywords:
- back 方法 Windows Media Player
- back 方法 Windows Media Player，IWMPDVD 介面
- IWMPDVD 介面 Windows Media Player，back 方法
topic_type:
- apiref
api_name:
- IWMPDVD.back
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 483e8e36f8ac5e539925306a53c04d144fb6de1281878840fc598c96c814f002
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119414558"
---
# <a name="iwmpdvdback-method"></a>IWMPDVD：： back 方法

**Back** 方法會將顯示從子功能表變更為其父功能表。

## <a name="syntax"></a>語法


```CSharp
public void back();
```


```VB

Public Sub back()
Implements IWMPDVD.back
```





## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

每個 DVD 的撰寫方式不同。 某些 Dvd 的撰寫目的是讓 `back` 方法可從根功能表中取得，但叫用時，它不會執行任何動作。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 9 系列或更新版本<br/>                                                                      |
| 命名空間<br/> | **WMPLib**<br/>                                                                                                  |
| 組件<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMPDVD 介面 (VB 和 c # )**](iwmpdvd--vb-and-c.md)
</dt> </dl>

 

 





