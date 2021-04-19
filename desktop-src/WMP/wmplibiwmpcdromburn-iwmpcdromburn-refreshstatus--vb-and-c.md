---
title: IWMPCdromBurn refreshStatus 方法
description: RefreshStatus 方法會更新目前燒錄播放清單的狀態資訊。
ms.assetid: 4dd90e76-92b5-4a00-b027-b54502e56804
keywords:
- refreshStatus 方法 Windows Media Player
- refreshStatus 方法 Windows Media Player，IWMPCdromBurn 介面
- IWMPCdromBurn 介面 Windows Media Player，refreshStatus 方法
topic_type:
- apiref
api_name:
- IWMPCdromBurn.refreshStatus
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55205e684d055d20c8e8f218ba58716de8472916
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993405"
---
# <a name="iwmpcdromburnrefreshstatus-method"></a>IWMPCdromBurn：： refreshStatus 方法

**RefreshStatus** 方法會更新目前燒錄播放清單的狀態資訊。

## <a name="syntax"></a>語法


```CSharp
public void refreshStatus();
```


```VB

Public Sub refreshStatus()
Implements IWMPCdromBurn.refreshStatus
```





## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

在您建立或變更燒錄播放清單之後，請先呼叫這個方法，然後再閱讀狀態資訊或燒錄 CD。 您可以藉由取得 **burnState** 和檢查 wmpbsRefreshStatusPending 的值，測試是否需要重新整理。

重新整理狀態是一項同步作業。 這表示，如果目前的燒錄播放清單是大型的，而且包含許多變更，則此方法會傳回較長的一段時間。

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

[**WMPBurnState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnstate)
</dt> </dl>

 

 





