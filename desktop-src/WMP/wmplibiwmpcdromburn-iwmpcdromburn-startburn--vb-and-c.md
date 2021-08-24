---
title: IWMPCdromBurn startBurn 方法
description: StartBurn 方法會燒錄 CD。
ms.assetid: e852c011-5f54-469f-aead-37fa711ef876
keywords:
- startBurn 方法 Windows Media Player
- startBurn 方法 Windows Media Player，IWMPCdromBurn 介面
- IWMPCdromBurn 介面 Windows Media Player，startBurn 方法
topic_type:
- apiref
api_name:
- IWMPCdromBurn.startBurn
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7806501a619d6172d9f1ce0715045c822b30326c2b59c268f432708ea13923ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119761068"
---
# <a name="iwmpcdromburnstartburn-method"></a>IWMPCdromBurn：： startBurn 方法

**StartBurn** 方法會燒錄 CD。

## <a name="syntax"></a>語法


```CSharp
public void startBurn();
```


```VB

Public Sub startBurn()
Implements IWMPCdromBurn.startBurn
```





## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

在呼叫這個方法之前， **burnstate** 的值應該是 WmpbsReady 或 wmpbsStopped。

如果 CD 光碟機不是燒錄機，或磁片磁碟機中的光碟無法寫入，此方法將無法運作。 使用 **isAvailable** 來判斷是否可以燒錄 CD。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 11。<br/>                                                                                    |
| 命名空間<br/> | **WMPLib**<br/>                                                                                                  |
| 組件<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMPCdromBurn 介面 (VB 和 c # )**](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[**IWMPCdromBurn. burnState (VB 和 c # )**](wmplibiwmpcdromburn-iwmpcdromburn-burnstate--vb-and-c.md)
</dt> <dt>

[**IWMPCdromBurn. isAvailable (VB 和 c # )**](wmplibiwmpcdromburn-iwmpcdromburn-isavailable--vb-and-c.md)
</dt> <dt>

[**IWMPCdromBurn. stopBurn (VB 和 c # )**](wmplibiwmpcdromburn-iwmpcdromburn-stopburn-iwmpcdromburn.md)
</dt> </dl>

 

 





