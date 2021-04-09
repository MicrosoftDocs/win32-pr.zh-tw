---
title: 'INapEnforcementClientCallback GetConnections 方法 (NapEnforcementClient .h) '
description: 由 NapAgent 呼叫並由強制用戶端所執行，以傳回一組連接。
ms.assetid: 8f697217-5799-48e4-9f0b-715f516e48d9
keywords:
- GetConnections 方法 NAP
- GetConnections 方法 NAP，INapEnforcementClientCallback 介面
- INapEnforcementClientCallback 介面 NAP，GetConnections 方法
topic_type:
- apiref
api_name:
- INapEnforcementClientCallback.GetConnections
api_location:
- NapEnforcementClient.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9acdc68dbc69cabe710414f3fa2501585f3e384e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844355"
---
# <a name="inapenforcementclientcallbackgetconnections-method"></a>INapEnforcementClientCallback：： GetConnections 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapEnforcementClientCallback：： GetConnections** 回呼方法是由 NapAgent 呼叫，並且由強制用戶端所執行，以傳回一組連接。

## <a name="syntax"></a>語法


```C++
HRESULT GetConnections(
  [out] Connections **connections
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*連接* \[擴展\]
</dt> <dd>

目前維護之 [**連接**](connections-struct.md)集的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

此回呼方法必須傳回下列其中一個錯誤碼。



| 傳回碼                                                                                                | Description                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                       | 如果作業成功，則傳回此值。<br/>                                                                                                                                                              |
| <dl> <dt>**RPC \_ S \_ 伺服器 \_ 無法使用**</dt> </dl> | 傳回這個值會導致從系結的-SHA 清單中移除 enforcer，以及要排清的對應 NapAgent 快取專案。 失敗的 SHA 接著可以使用 NapAgent 重新初始化。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                      |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                                |
| 標頭<br/>                   | <dl> <dt>NapEnforcementClient。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapEnforcementClient .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**INapEnforcementClientCallback**](inapenforcementclientcallback.md)
</dt> </dl>

 

 





