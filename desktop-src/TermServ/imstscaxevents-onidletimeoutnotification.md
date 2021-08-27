---
title: IMsTscAxEvents OnIdleTimeoutNotification 方法
description: 當使用者在 IMsRdpClientAdvancedSettings put MinutesToIdleTimeout 方法所設定的一段時間內沒有滑鼠或鍵盤輸入時呼叫 \_ 。
ms.assetid: 303f23c9-3544-4e06-93f0-3aca35d29fb5
ms.tgt_platform: multiple
keywords:
- OnIdleTimeoutNotification 方法遠端桌面服務
- OnIdleTimeoutNotification 方法遠端桌面服務，IMsTscAxEvents 介面
- IMsTscAxEvents 介面遠端桌面服務，OnIdleTimeoutNotification 方法
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnIdleTimeoutNotification
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 356414d03a6b102f37f93205e0dbb8c3261cffbbb5b71a58cdb3f80acda09212
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125118"
---
# <a name="imstscaxeventsonidletimeoutnotification-method"></a>IMsTscAxEvents：： OnIdleTimeoutNotification 方法

當使用者在 [**IMsRdpClientAdvancedSettings：:p 長 \_ MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) 方法設定期間沒有滑鼠或鍵盤輸入時呼叫。

## <a name="syntax"></a>語法


```C++
void OnIdleTimeoutNotification();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

根據預設， [**MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) 屬性的值會設定為零，而且系統不會監視閒置時間。 只有當屬性設定為非零值時，才會發生此事件。

每次發生事件時，就會自動重設 [**MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) 的值。

應用程式在中斷使用者的連線時，可以使用 [**MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) ;例如，在 kiosk 或其他公用終端機案例中。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                               |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                         |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents 定義為336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





