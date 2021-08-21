---
title: 'InitializeNapAgentNotifier 函式 (NapUtil) '
description: 訂閱呼叫進程以 NapAgent 狀態變更通知和隔離狀態變更通知。
ms.assetid: 24180194-50d7-4f54-845d-25402af9cf9a
keywords:
- InitializeNapAgentNotifier 函數 NAP
topic_type:
- apiref
api_name:
- InitializeNapAgentNotifier
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ac2d874f6138bcc1fbc97952d4464e56e05b0a497c7b0ff98e9c05e8c8434e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118133453"
---
# <a name="initializenapagentnotifier-function"></a>InitializeNapAgentNotifier 函式

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**InitializeNapAgentNotifier** 函式會訂閱呼叫進程，以 NapAgent 狀態變更通知和隔離狀態變更通知。 這些通知是由 NapAgent 服務所提供。

## <a name="syntax"></a>語法


```C++
NAPAPI HRESULT WINAPI InitializeNapAgentNotifier(
  _In_ NapNotifyType type,
  _In_ HANDLE        hNotifyEvent
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*類型* \[在\]
</dt> <dd>

[**NapNotifyType**](/windows/win32/api/naptypes/ne-naptypes-napnotifytype)值，指定要接收的服務通知類型。

</dd> <dt>

*hNotifyEvent* \[在\]
</dt> <dd>

用於通知的事件控制碼。 呼叫端必須將開啟的控制碼傳遞給 *hNotifyEvent* 參數。 當不再需要時，呼叫端也必須關閉事件控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值



| 傳回碼                                                                                                | 描述                                                                                               |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                       | 初始化已順利完成。<br/>                                                         |
| <dl> <dt>**E \_ 失敗**</dt> </dl>                     | 初始化失敗。<br/>                                                                         |
| <dl> <dt>**錯誤 \_ 已 \_ 初始化**</dt> </dl> | 此處理程式已訂閱指定之 *類型* 的 NapAgent 服務通知。 <br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>               | 傳遞了無效的引數。 <br/>                                                               |



 

## <a name="remarks"></a>備註

此函式不是安全執行緒。

需要訂用帳戶才能 NapAgent 指定 *類型* 之服務通知的每個處理常式，都必須呼叫 **InitializeNapAgentNotifier** 來訂閱通知。 如果處理常式必須訂閱一種以上的通知類型，則必須針對每一種類型的通知呼叫 **InitializeNapAgentNotifier** 一次。

一旦進程不需要進一步的通知，處理常式就必須針對指定的 *型* 別呼叫 [**UninitializeNapAgentNotifier**](uninitializenapagentnotifier.md) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>NapUtil。h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**UninitializeNapAgentNotifier**](uninitializenapagentnotifier.md)
</dt> </dl>

 

 





