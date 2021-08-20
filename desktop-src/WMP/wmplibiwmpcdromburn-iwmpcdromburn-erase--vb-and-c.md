---
title: IWMPCdromBurn erase 方法
description: 清除方法會清除目前的 CD。
ms.assetid: ed0fbd7e-61a6-445a-bca5-ed2969d5cadc
keywords:
- erase 方法 Windows Media Player
- IWMPCdromBurn 介面 Windows Media Player 清除方法
- IWMPCdromBurn 介面 Windows Media Player、erase 方法
topic_type:
- apiref
api_name:
- IWMPCdromBurn.erase
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 356b7bcdd332198c40760860e69741e76e0e993b6b47b3c5a5ff207d3d55bc42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118116331"
---
# <a name="iwmpcdromburnerase-method"></a>IWMPCdromBurn：： erase 方法

**清除** 方法會清除目前的 CD。

## <a name="syntax"></a>語法


```CSharp
public void erase();
```


```VB

Public Sub erase()
Implements IWMPCdromBurn.erase
```





## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

如果磁片磁碟機中的光碟無法擦寫，則此方法將無法運作。 使用 [IWMPCdromBurn isAvailable](wmplibiwmpcdromburn-iwmpcdromburn-isavailable--vb-and-c.md) 來判斷是否可以清除 CD。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 11。<br/>                                                                                    |
| 命名空間<br/> | **WMPLib**<br/>                                                                                                  |
| 組件<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMPCdromBurn 介面 (VB 和 c # )**](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





