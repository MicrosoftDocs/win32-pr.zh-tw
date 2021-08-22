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
ms.openlocfilehash: 3e37f2b786d32ab9f42738e6a8522c6f4593aa6b21a490a6fdd969233b4a6dff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118888167"
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
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                   |
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

 

 




