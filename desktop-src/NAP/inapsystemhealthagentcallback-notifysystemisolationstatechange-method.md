---
title: 'INapSystemHealthAgentCallback NotifySystemIsolationStateChange 方法 (NapSystemHealthAgent .h) '
description: 由 NapAgent 呼叫，表示系統隔離狀態或試用結束時間已變更。
ms.assetid: 0837eea4-6d92-44dc-b8b8-eca6be5f63e6
keywords:
- NotifySystemIsolationStateChange 方法 NAP
- NotifySystemIsolationStateChange 方法 NAP，INapSystemHealthAgentCallback 介面
- INapSystemHealthAgentCallback 介面 NAP，NotifySystemIsolationStateChange 方法
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.NotifySystemIsolationStateChange
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fc75686801148e0866f8996dabdb31af66eac9b55c60473782a794ea59f7463
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118621149"
---
# <a name="inapsystemhealthagentcallbacknotifysystemisolationstatechange-method"></a>INapSystemHealthAgentCallback：： NotifySystemIsolationStateChange 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

NapAgent 會呼叫 **INapSystemHealthAgentCallback：： NotifySystemIsolationStateChange** 方法，表示系統隔離狀態或試用結束時間已變更。

## <a name="syntax"></a>語法


```C++
HRESULT NotifySystemIsolationStateChange();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                          | 描述                   |
|--------------------------------------------------------------------------------------|-------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 表示成功。<br/> |



 

## <a name="remarks"></a>備註

此回呼方法是由 NAP 系統所宣告，而且是由 SHA 寫入器所執行。

健康情況代理程式可以使用 [**INapSystemHealthAgentBinding：： GetSystemIsolationInfo**](inapsystemhealthagentbinding-getsystemisolationinfo-method.md)來查詢系統 NAP 狀態。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                      |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                                |
| 標頭<br/>                   | <dl> <dt>NapSystemHealthAgent。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthAgent .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 





