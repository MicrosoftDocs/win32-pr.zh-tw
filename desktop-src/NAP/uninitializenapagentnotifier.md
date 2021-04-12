---
title: 'UninitializeNapAgentNotifier 函式 (NapUtil) '
description: 從 NapAgent 狀態變更通知和隔離狀態變更通知取消訂閱呼叫的進程。
ms.assetid: b676ee33-caf6-48f0-acf8-5be1b23c62fe
keywords:
- UninitializeNapAgentNotifier 函數 NAP
topic_type:
- apiref
api_name:
- UninitializeNapAgentNotifier
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5d68b43fba64be82908d73803113f871b08c93c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384382"
---
# <a name="uninitializenapagentnotifier-function"></a>UninitializeNapAgentNotifier 函式

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**UninitializeNapAgentNotifier** 函式會從 NapAgent 狀態變更通知和隔離狀態變更通知，取消訂閱呼叫的進程。 這些通知是由 NapAgent 服務所提供。

## <a name="syntax"></a>語法


```C++
NAPAPI VOID WINAPI UninitializeNapAgentNotifier(
  _In_ NapNotifyType type
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*類型* \[在\]
</dt> <dd>

[**NapNotifyType**](/windows/win32/api/naptypes/ne-naptypes-napnotifytype)值，指定要取消訂閱的服務通知類型。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函數沒有傳回值。

## <a name="remarks"></a>備註

此函式不是安全執行緒。

每個訂閱 NapAgent 指定 *型* 別之服務通知的進程都必須呼叫 **UninitializeNapAgentNotifier** ，才能取消訂閱通知。 如果有一或多個通知的處理常式，它必須針對每一種類型的通知呼叫 **UninitializeNapAgentNotifier** 一次。

如果進程先前未針對通知類型呼叫 [**InitializeNapAgentNotifier**](initializenapagentnotifier.md) ，此函式將會以無訊息模式失敗。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>NapUtil。h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**InitializeNapAgentNotifier**](initializenapagentnotifier.md)
</dt> </dl>

 

 





