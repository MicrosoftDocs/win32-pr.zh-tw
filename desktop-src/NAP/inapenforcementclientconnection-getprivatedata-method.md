---
title: 'INapEnforcementClientConnection GetPrivateData 方法 (NapEnforcementClient .h) '
description: NapAgent 用來取得私用資料。
ms.assetid: d38ef523-b645-401f-b3a9-1315ef39931a
keywords:
- GetPrivateData 方法 NAP
- GetPrivateData 方法 NAP，INapEnforcementClientConnection 介面
- INapEnforcementClientConnection 介面 NAP，GetPrivateData 方法
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetPrivateData
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6618ff7b25ad57cbb943107e80f299d9b6a68bea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843331"
---
# <a name="inapenforcementclientconnectiongetprivatedata-method"></a>INapEnforcementClientConnection：： GetPrivateData 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

NapAgent 會使用 **INapEnforcementClientConnection：： GetPrivateData** 方法來取得私用資料。

## <a name="syntax"></a>語法


```C++
HRESULT GetPrivateData(
  [out] PrivateData **privateData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*privateData* \[擴展\]
</dt> <dd>

[**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata)不透明資料 blob 指標的指標，而這些指標只有 NapAgent 可以解讀。

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

 

 





