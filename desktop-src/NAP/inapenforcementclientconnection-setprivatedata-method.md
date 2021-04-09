---
title: 'INapEnforcementClientConnection SetPrivateData 方法 (NapEnforcementClient .h) '
description: NapAgent 會使用來設定私用資料。
ms.assetid: 2559a612-8857-4e60-b5bc-dd8235ff69f9
keywords:
- SetPrivateData 方法 NAP
- SetPrivateData 方法 NAP，INapEnforcementClientConnection 介面
- INapEnforcementClientConnection 介面 NAP，SetPrivateData 方法
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetPrivateData
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3e73248e546b1f0e48438553877f0523bd30b56
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024888"
---
# <a name="inapenforcementclientconnectionsetprivatedata-method"></a>INapEnforcementClientConnection：： SetPrivateData 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

NapAgent 會使用 **INapEnforcementClientConnection：： SetPrivateData** 方法來設定私用資料。

## <a name="syntax"></a>語法


```C++
HRESULT SetPrivateData(
  [in] const PrivateData *privateData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*privateData* \[在\]
</dt> <dd>

只有 NapAgent 可以解讀的 [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) 資料 blob 指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

也可能傳回其他 COM 特定的錯誤碼。



| 傳回碼                                                                                     | Description                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> </dl>           | 作業成功。<br/>                                    |
| <dl> <dt>**E \_ACCESSDENIED**</dt> </dl> | 許可權錯誤，拒絕存取。<br/>                       |
| <dl> <dt>**E \_OUTOFMEMORY**</dt> </dl>  | 系統資源限制，無法執行操作。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                      |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                                |
| 標頭<br/>                   | <dl> <dt>NapEnforcementClient。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapEnforcementClient .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> </dl>

 

 





