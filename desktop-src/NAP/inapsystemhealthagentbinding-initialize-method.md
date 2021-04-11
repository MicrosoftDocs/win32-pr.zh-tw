---
title: 'INapSystemHealthAgentBinding Initialize 方法 (NapSystemHealthAgent .h) '
description: 將系統健全狀況代理程式初始化 (SHA) ，並將 SHA 系結至 NapAgent 服務。
ms.assetid: abbc942b-0217-4b07-bf43-fab55ca9c411
keywords:
- Initialize 方法 NAP
- Initialize 方法 NAP，INapSystemHealthAgentBinding 介面
- INapSystemHealthAgentBinding 介面 NAP，Initialize 方法
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding.Initialize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ee4d4f602303ca1943e47c04ba30ab8f6e75e72
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317132"
---
# <a name="inapsystemhealthagentbindinginitialize-method"></a>INapSystemHealthAgentBinding：： Initialize 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapSystemHealthAgentBinding：： Initialize** 方法會將系統健全狀況代理程式初始化 (sha) ，並將 sha 系結至 NapAgent 服務。 在呼叫 [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) 介面上的任何其他方法之前，必須先呼叫這個方法。

## <a name="syntax"></a>語法


```C++
HRESULT Initialize(
  [in] SystemHealthEntityId          id,
  [in] INapSystemHealthAgentCallback *callback
);
```



## <a name="parameters"></a>參數

<dl> <dt>

 \[ 中的識別碼\]
</dt> <dd>

包含系結至 NapAgent 服務之 SHA 識別碼的唯一 [SystemHealthEntityId](nap-datatypes.md) 。

</dd> <dt>

*回呼* \[在\]
</dt> <dd>

[**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md)介面的 COM 指標，由 NapAgent 用來以通知/進程回呼健康情況代理程式。 NapAgent 會保存與這個介面相關聯之物件的參考，直到呼叫解除 [**初始化**](inapsystemhealthagentbinding-uninitialize-method.md) 為止。

</dd> </dl>

## <a name="return-value"></a>傳回值

也可能傳回其他 COM 特定的錯誤碼。



| 傳回碼                                                                                                | Description                                                                                                                    |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> </dl>                      | 作業成功。<br/>                                                                                                |
| <dl> <dt>**E \_ACCESSDENIED**</dt> </dl>            | 許可權錯誤，拒絕存取。<br/>                                                                                   |
| <dl> <dt>**E \_OUTOFMEMORY**</dt> </dl>             | 系統資源限制，無法執行操作。<br/>                                                             |
| <dl> <dt>**錯誤 \_ 已 \_ 初始化**</dt> </dl> | 如果 SHA 先前已初始化，則會傳回此錯誤。<br/>                                                      |
| <dl> <dt>**NAP \_ E \_ 未 \_ 註冊**</dt> </dl>     | 如果 SHA 尚未註冊，則會傳回此錯誤。<br/>                                                      |
| <dl> <dt>**RPC \_ E \_ 中斷連接**</dt> </dl>        | NapAgent 已停止。 這個物件會在重新開機後自動復原並重新系結至 NapAgent。<br/> |



 

## <a name="remarks"></a>備註

NapAgent 不會觸發 SoH 交換作為初始化的結果。 系統健康狀態代理程式必須呼叫 [**NotifySoHChange**](inapsystemhealthagentbinding-notifysohchange-method.md) ，以要求在使用 NapAgent 初始化之後交換 SoH 封包。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                      |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                                |
| 標頭<br/>                   | <dl> <dt>NapSystemHealthAgent。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthAgent .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md)
</dt> </dl>

 

 





