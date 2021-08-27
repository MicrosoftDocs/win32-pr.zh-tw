---
title: IRemoteDesktopClientEvents OnDisconnected 方法
description: 當用戶端控制項與遠端會話中斷連接時呼叫。
ms.assetid: EA26B530-0AA8-49D6-8E3C-E53179FC5104
ms.tgt_platform: multiple
keywords:
- OnDisconnected 方法遠端桌面服務
- OnDisconnected 方法遠端桌面服務，IRemoteDesktopClientEvents 介面
- IRemoteDesktopClientEvents 介面遠端桌面服務，OnDisconnected 方法
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnDisconnected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e93ebf7c85e4015539cbbcc15723cdfed9c7d181741925c1a97c93ccc4326eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124898"
---
# <a name="iremotedesktopclienteventsondisconnected-method"></a>IRemoteDesktopClientEvents：： OnDisconnected 方法

當用戶端控制項與遠端會話中斷連接時呼叫。

## <a name="syntax"></a>語法


```C++
void OnDisconnected(
  [in] long disconnectReason,
  [in] long ExtendedDisconnectReason,
  [in] BSTR disconnectErrorMessage
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*disconnectReason* \[在\]
</dt> <dd>

中斷線上活動的原因。

</dd> <dt>

*ExtendedDisconnectReason* \[在\]
</dt> <dd>

中斷線上活動的延伸資訊。

</dd> <dt>

*disconnectErrorMessage* \[在\]
</dt> <dd>

中斷線上活動的錯誤訊息。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                           |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                                 |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| IID<br/>                      | DIID \_ IRemoteDesktopClientEvents 定義為079863B7-6D47-4105-8BFE-0CDCB360E67D<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IRemoteDesktopClientEvents**](iremotedesktopclientevents.md)
</dt> </dl>

 

 





