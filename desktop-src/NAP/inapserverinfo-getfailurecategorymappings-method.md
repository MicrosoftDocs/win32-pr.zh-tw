---
title: 'INapServerInfo GetFailureCategoryMappings 方法 (NapServerManagement .h) '
description: 抓取指定 SHA 或 SHV 的失敗類別對應。
ms.assetid: 89b89003-40b3-4763-aec8-01cd0c307649
keywords:
- GetFailureCategoryMappings 方法 NAP
- GetFailureCategoryMappings 方法 NAP，INapServerInfo 介面
- INapServerInfo 介面 NAP，GetFailureCategoryMappings 方法
topic_type:
- apiref
api_name:
- INapServerInfo.GetFailureCategoryMappings
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7ba830dd8a35a2c60b14c4feec14846125223e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104467057"
---
# <a name="inapserverinfogetfailurecategorymappings-method"></a>INapServerInfo：： GetFailureCategoryMappings 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapServerInfo：： GetFailureCategoryMappings** 方法會抓取指定 SHA 或 SHV 的失敗類別對應。

## <a name="syntax"></a>語法


```C++
HRESULT GetFailureCategoryMappings(
  [in]  SystemHealthEntityId   id,
  [out] FailureCategoryMapping *mapping
);
```



## <a name="parameters"></a>參數

<dl> <dt>

 \[ 中的識別碼\]
</dt> <dd>

[**SystemHealthEntityId**](nap-type-constants.md) ，其中包含 SHA 或 SHV 的唯一識別碼。

</dd> <dt>

*對應* \[擴展\]
</dt> <dd>

[**FailureCategoryMapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping)的指標，其中包含對應資料。

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
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                               |
| 標頭<br/>                   | <dl> <dt>NapServerManagement。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapServerManagement .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qsvrmgmt.dll</dt> </dl>            |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**INapServerInfo**](inapserverinfo.md)
</dt> </dl>

 

 





