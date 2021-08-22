---
title: IRemoteDesktopClientEvents OnAutoReconnecting 方法
description: 當用戶端控制項嘗試自動重新建立遠端會話的連接時呼叫。
ms.assetid: 299408A9-ED14-42F4-B324-AF4C86FEDABE
ms.tgt_platform: multiple
keywords:
- OnAutoReconnecting 方法遠端桌面服務
- OnAutoReconnecting 方法遠端桌面服務，IRemoteDesktopClientEvents 介面
- IRemoteDesktopClientEvents 介面遠端桌面服務，OnAutoReconnecting 方法
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnAutoReconnecting
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7246b8822b3d3abed5d483f52c64eee88d67f99694bda44c5d8f72318cb2c04a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119511728"
---
# <a name="iremotedesktopclienteventsonautoreconnecting-method"></a>IRemoteDesktopClientEvents：： OnAutoReconnecting 方法

當用戶端控制項嘗試自動重新建立遠端會話的連接時呼叫。

## <a name="syntax"></a>語法


```C++
void OnAutoReconnecting(
  [in] long         disconnectReason,
  [in] long         ExtendedDisconnectReason,
  [in] BSTR         disconnectErrorMessage,
  [in] VARIANT_BOOL networkAvailable,
  [in] long         attemptCount,
  [in] long         maxAttemptCount
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

</dd> <dt>

*networkAvailable* \[在\]
</dt> <dd>

網路是否可供使用。

</dd> <dt>

*了 attemptcount* \[在\]
</dt> <dd>

這會嘗試這麼做。

</dd> <dt>

*maxAttemptCount* \[在\]
</dt> <dd>

將會執行重新連線嘗試的次數上限。

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

 

 





