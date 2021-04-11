---
description: 取消訂閱服務狀態變更通知。
ms.assetid: 8c04ebf7-4d61-4617-b120-dbe26b2f9ad2
title: 'UnsubscribeServiceChangeNotifications 函式 (Winsvcp) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UnsubscribeServiceChangeNotifications
api_type:
- DllExport
api_location:
- SecHost.dll
- API-MS-Win-Service-Private-L1-1-0.dll
- API-MS-Win-Service-Private-L1-1-1.dll
- Advapi32.dll
- API-MS-Win-Service-Private-L1-1-2.dll
ms.openlocfilehash: ebecfb133172c9c7a56ed6d28f7ad6b395d8afce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850511"
---
# <a name="unsubscribeservicechangenotifications-function"></a>UnsubscribeServiceChangeNotifications 函式

取消訂閱服務狀態變更通知。 此函數會使用 [**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md)傳回的訂閱。

## <a name="syntax"></a>語法


```C++
 VOID WINAPI UnsubscribeServiceChangeNotifications(
  _In_ PSC_NOTIFICATION_REGISTRATION pSubscription
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pSubscription* \[在\]
</dt> <dd>

要取消訂閱之訂用帳戶的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

在完成的同進程回呼完成之前， **UnsubscribeServiceChangeNotifications** 不會傳回。 因此，您無法在回呼內呼叫 **UnsubscribeServiceChangeNotifications** ，而不會造成鎖死。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                   |
| 標頭<br/>                   | <dl> <dt>Winsvcp。h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>SecHost.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea)
</dt> <dt>

[**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea)
</dt> <dt>

[**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera)
</dt> <dt>

[**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md)
</dt> <dt>

[**QueryServiceDynamicInformation**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicedynamicinformation)
</dt> </dl>

 

 




