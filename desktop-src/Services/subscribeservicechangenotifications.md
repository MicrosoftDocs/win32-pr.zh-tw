---
description: 使用回呼函式訂閱服務狀態變更通知。
ms.assetid: d67113eb-2141-444c-9f09-eaa772bcad8a
title: 'SubscribeServiceChangeNotifications 函式 (Winsvcp) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SubscribeServiceChangeNotifications
api_type:
- DllExport
api_location:
- SecHost.dll
- API-MS-Win-Service-Private-L1-1-0.dll
- API-MS-Win-Service-Private-L1-1-1.dll
- Advapi32.dll
- API-MS-Win-Service-Private-L1-1-2.dll
ms.openlocfilehash: e327a44d613b514123862b1ddcb1bf302fea63ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990372"
---
# <a name="subscribeservicechangenotifications-function"></a>SubscribeServiceChangeNotifications 函式

使用回呼函式訂閱服務狀態變更通知。

## <a name="syntax"></a>語法


```C++
DWORD WINAPI SubscribeServiceChangeNotifications(
  _In_     SC_HANDLE                     hService,
  _In_     SC_EVENT_TYPE                 eEventType,
  _In_     PSC_NOTIFICATION_CALLBACK     pCallback,
  _In_opt_ PVOID                         pCallbackContext,
  _Out_    PSC_NOTIFICATION_REGISTRATION *pSubscription
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hService* \[在\]
</dt> <dd>

服務的控制碼或服務控制管理員的控制碼 (SCM) 來監視變更。

[**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea)和 [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea)函式會傳回服務的控制碼，而且必須要有 **服務 \_ 查詢 \_ 狀態** 存取權限。 [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera)函式會傳回服務控制管理員的控制碼，而且必須具有 **SC \_ 管理員 \_ 列舉 \_ 服務** 存取權限。

</dd> <dt>

*eEventType* \[在\]
</dt> <dd>

指定應回報的狀態變更類型。 此參數會設定為 [**SC \_ 事件 \_ 類型**](sc-event-type.md)中指定的其中一個值。 根據事件種類而定，此函式的行為會有所不同，如下所示。



| 值                                                                                                                                                                                                                                                   | 意義                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span id="SC_EVENT_DATABASE_CHANGE"></span><span id="sc_event_database_change"></span><dl> <dt>**SC \_事件 \_ 資料庫 \_ 變更**</dt> <dt>0</dt> </dl> | 已新增或刪除服務。 *HService* 參數必須是 SCM 的控制碼。<br/>                  |
| <span id="SC_EVENT_PROPERTY_CHANGE"></span><span id="sc_event_property_change"></span><dl> <dt>**SC \_事件 \_ 屬性 \_ 變更**</dt> <dt>1</dt> </dl> | 已更新一或多個服務屬性。 *HService* 參數必須是服務的控制碼。<br/> |
| <span id="SC_EVENT_STATUS_CHANGE"></span><span id="sc_event_status_change"></span><dl> <dt>**SC \_事件 \_ 狀態 \_ 變更**</dt> <dt>2</dt> </dl>       | 服務的狀態已變更。 *HService* 參數必須是服務的控制碼。<br/>              |



 

</dd> <dt>

*pCallback* \[在\]
</dt> <dd>

指定回呼函數。 回呼必須定義為具有 **SC \_ 通知 \_ 回呼** 的類型。 如需詳細資訊，請參閱＜備註＞。

</dd> <dt>

*pCallbackCoNtext* \[在中，選擇性\]
</dt> <dd>

表示此通知回呼內容的指標。

</dd> <dt>

*pSubscription* \[擴展\]
</dt> <dd>

傳回通知回呼註冊所產生之訂用帳戶的指標。 呼叫端會負責呼叫 [**UnsubscribeServiceChangeNotifications**](unsubscribeservicechangenotifications.md) ，以停止接收通知。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為「 **錯誤 \_ 成功**」。

如果函式失敗，則傳回值是其中一個 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。

## <a name="remarks"></a>備註

回呼函數的宣告方式如下：


```C++
typedef VOID CALLBACK SC_NOTIFICATION_CALLBACK(
    _In_    DWORD                   dwNotify,
    _In_    PVOID                   pCallbackContext
);
typedef SC_NOTIFICATION_CALLBACK* PSC_NOTIFICATION_CALLBACK;
```



回呼函式會接收呼叫端所提供內容的指標。 由於服務狀態變更事件，會叫用回呼。 叫用回呼時，會提供 **服務 \_ 通知 \_ * XXX*** 值的位元遮罩，指出服務狀態變更的類型。 以零（而不是有效的 **服務 \_ 通知 \_ * XXX*** 值）提供回呼時，應用程式必須確認變更了哪些內容。

回呼函數不能封鎖執行。 如果您預期執行回呼函式需要一些時間，請將工作專案排入執行緒集區中的執行緒，以將回呼函式中執行的工作卸載至個別的執行緒。 某些可讓回呼函數執行的工作類型包括執行檔案 i/o、等候事件，以及進行外部遠端程序呼叫。

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

[**UnsubscribeServiceChangeNotifications**](unsubscribeservicechangenotifications.md)
</dt> <dt>

[**QueryServiceDynamicInformation**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicedynamicinformation)
</dt> </dl>

 

