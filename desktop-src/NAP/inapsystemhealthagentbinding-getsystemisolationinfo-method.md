---
title: 'INapSystemHealthAgentBinding GetSystemIsolationInfo 方法 (NapSystemHealthAgent .h) '
description: 由 Sha 呼叫以判斷系統隔離狀態。
ms.assetid: 0401a846-0da2-4975-87bc-3e9fe8b5b67d
keywords:
- GetSystemIsolationInfo 方法 NAP
- GetSystemIsolationInfo 方法 NAP，INapSystemHealthAgentBinding 介面
- INapSystemHealthAgentBinding 介面 NAP，GetSystemIsolationInfo 方法
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding.GetSystemIsolationInfo
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9058b78bcff60b27bb27f25f11b785a8cd341f9addafe1829c1e8a7f3fb02a15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939555"
---
# <a name="inapsystemhealthagentbindinggetsystemisolationinfo-method"></a>INapSystemHealthAgentBinding：： GetSystemIsolationInfo 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapSystemHealthAgentBinding：： GetSystemIsolationInfo** 方法是由 sha 呼叫，以判斷系統隔離狀態。

> [!Note]  
> 使用 [**INapSystemHealthAgentBinding2：： GetSystemIsolationInfoEx**](inapsystemhealthagentbinding2-getsystemisolationinfoex.md) 來判斷系統的擴充隔離狀態。

 

## <a name="syntax"></a>語法


```C++
HRESULT GetSystemIsolationInfo(
  [out] IsolationInfo **isolationInfo,
  [out] BOOL          *unknownConnections
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*isolationInfo* \[擴展\]
</dt> <dd>

[**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo)結構指標的指標，其中包含已知連接之系統的隔離狀態。 如果系統處於限制存取、試用或無限制存取的狀態，則為 *isolationInfoindicates* 。

</dd> <dt>

*unknownConnections* \[擴展\]
</dt> <dd>

**布林** 值的指標，如果有任何連接處於未知狀態，則為 **TRUE** ，否則為 **FALSE** 。

</dd> </dl>

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

SHA 必須在呼叫這個方法或 [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md)介面的任何其他方法之前呼叫 [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                      |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                                |
| 標頭<br/>                   | <dl> <dt>NapSystemHealthAgent。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthAgent .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md)
</dt> </dl>

 

 





