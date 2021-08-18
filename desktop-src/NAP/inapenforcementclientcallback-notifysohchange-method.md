---
title: 'INapEnforcementClientCallback NotifySoHChange 方法 (NapEnforcementClient .h) '
description: NapAgent 用來通知強制用戶端有 SoH 變更。
ms.assetid: da8b9238-6371-4a6a-a9e7-ab791391ffc2
keywords:
- NotifySoHChange 方法 NAP
- NotifySoHChange 方法 NAP，INapEnforcementClientCallback 介面
- INapEnforcementClientCallback 介面 NAP，NotifySoHChange 方法
topic_type:
- apiref
api_name:
- INapEnforcementClientCallback.NotifySoHChange
api_location:
- NapEnforcementClient.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9011db09b698f886bd10ad19298a104668d038cc2bb11136b6e4ac58035e3425
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940132"
---
# <a name="inapenforcementclientcallbacknotifysohchange-method"></a>INapEnforcementClientCallback：： NotifySoHChange 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapEnforcementClientCallback：： NotifySoHChange** 回呼方法是由 NapAgent 用來通知強制用戶端的 SoH 變更。

## <a name="syntax"></a>語法


```C++
HRESULT NotifySoHChange();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

此回呼方法必須傳回下列其中一個錯誤碼。



| 傳回碼                                                                                                | 描述                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                       | 如果作業成功，則傳回此值。<br/>                                                                                                                                                              |
| <dl> <dt>**RPC \_ S \_ 伺服器 \_ 無法使用**</dt> </dl> | 傳回這個值會導致從系結的-SHA 清單中移除 enforcer，以及要排清的對應 NapAgent 快取專案。 失敗的 SHA 接著可以使用 NapAgent 重新初始化。<br/> |



 

## <a name="remarks"></a>備註

完成系統修正是系統健康狀態變更事件。 這表示當 [**INapSystemHealthAgentCallback：： GetFixupInfo**](inapsystemhealthagentcallback-getfixupinfo-method.md)通知指出用戶端已修正時，您必須呼叫 **NotifySoHChange** 。 修正用戶端時， **GetFixupInfo** 所傳回之 [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo)結構的 **狀態** 成員具有 **fixupStateSuccess** 的值。

透過此回呼呼叫 NapAgent 之後，強制代理程式必須呼叫 [**INapEnforcementClientBinding：： GetSoHRequest**](inapenforcementclientbinding-getsohrequest-method.md) 以取得新的要求。 此呼叫可以在與 **INapEnforcementClientCallback：： NotifySoHChange** 相同的執行緒上進行。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                      |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                                |
| 標頭<br/>                   | <dl> <dt>NapEnforcementClient。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapEnforcementClient .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**INapEnforcementClientCallback**](inapenforcementclientcallback.md)
</dt> </dl>

 

 





