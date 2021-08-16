---
title: 'INapSystemHealthAgentBinding NotifySoHChange 方法 (NapSystemHealthAgent .h) '
description: Sha 會在其 SoH 變更時使用。
ms.assetid: 3a653282-03b0-49d5-833f-966497f46faa
keywords:
- NotifySoHChange 方法 NAP
- NotifySoHChange 方法 NAP，INapSystemHealthAgentBinding 介面
- INapSystemHealthAgentBinding 介面 NAP，NotifySoHChange 方法
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding.NotifySoHChange
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a418a78e0d21178f3dd1889816873afb1c7ec7212da48be5d75e44d40d0a61d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118367836"
---
# <a name="inapsystemhealthagentbindingnotifysohchange-method"></a>INapSystemHealthAgentBinding：： NotifySoHChange 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapSystemHealthAgentBinding：： NotifySoHChange** 方法是在其 SoH 變更時由 sha 使用。

## <a name="syntax"></a>語法


```C++
HRESULT NotifySoHChange();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

也可能傳回其他 COM 特定的錯誤碼。



| 傳回碼                                                                                             | Description                                                                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> </dl>                   | 作業成功。<br/>                                                                                                |
| <dl> <dt>**E \_ACCESSDENIED**</dt> </dl>         | 許可權錯誤，拒絕存取。<br/>                                                                                   |
| <dl> <dt>**E \_OUTOFMEMORY**</dt> </dl>          | 系統資源限制，無法執行操作。<br/>                                                             |
| <dl> <dt>**NAP \_ E \_ 未 \_ 初始化**</dt> </dl> | SHA 先前尚未初始化。<br/>                                                                        |
| <dl> <dt>**RPC \_ E \_ 中斷連接**</dt> </dl>     | NapAgent 已停止。 這個物件會在重新開機後自動復原並重新系結至 NapAgent。<br/> |



 

## <a name="remarks"></a>備註

Sha 不能呼叫此 API 推測式運算，因為它會在網路上產生 SoH 交換。 只有在必要時，才應該進行此 API 的呼叫。

NapAgent 不會保留這個執行緒來處理 SoH 變更。 相反地，它會立即返回，並以非同步方式處理變更。

SHA 必須在呼叫這個方法或 [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md)介面的任何其他方法之前呼叫 [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                      |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                                |
| 標頭<br/>                   | <dl> <dt>NapSystemHealthAgent。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapSystemHealthAgent .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md)
</dt> </dl>

 

 





