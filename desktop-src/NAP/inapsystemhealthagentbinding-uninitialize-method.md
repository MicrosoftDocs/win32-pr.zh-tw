---
title: 'INapSystemHealthAgentBinding 解除初始化方法 (NapSystemHealthAgent .h) '
description: 導致 NapAgent 釋出其所有對系統健康情況代理程式 COM 指標的參考。
ms.assetid: 8b9fabc9-7453-41fe-a1e7-2ec5fa275a3a
keywords:
- 解除初始化方法 NAP
- 解除初始化方法 NAP，INapSystemHealthAgentBinding 介面
- INapSystemHealthAgentBinding 介面 NAP，解除初始化方法
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding.Uninitialize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a863e9d742610ab764a3b7a00966e8e112278317
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106991776"
---
# <a name="inapsystemhealthagentbindinguninitialize-method"></a>INapSystemHealthAgentBinding：：解除初始化方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapSystemHealthAgentBinding：：解除初始化** 方法會使 NapAgent 釋放對系統健康情況代理程式 COM 指標的所有參考。

## <a name="syntax"></a>語法


```C++
HRESULT Uninitialize();
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

NapAgent 會封鎖此方法呼叫的執行，直到系結和回呼介面上所有現有的呼叫都完成為止。

SHA 必須在呼叫這個方法或 [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md)介面的任何其他方法之前呼叫 [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) 。

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

 

 





