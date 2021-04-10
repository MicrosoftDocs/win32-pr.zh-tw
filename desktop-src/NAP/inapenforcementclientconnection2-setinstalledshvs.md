---
title: 'INapEnforcementClientConnection2 SetInstalledShvs 方法 (NapEnforcementClient .h) '
description: NAP 代理程式用來將已安裝的系統健康狀態驗證 (Shv) 安裝在用戶端上。
ms.assetid: 38aa99b9-a15a-414d-91fc-128de8f5a654
keywords:
- SetInstalledShvs 方法 NAP
- SetInstalledShvs 方法 NAP，INapEnforcementClientConnection2 介面
- INapEnforcementClientConnection2 介面 NAP，SetInstalledShvs 方法
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection2.SetInstalledShvs
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6651cd5248094f82d9faa1862492f82648e94125
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106512"
---
# <a name="inapenforcementclientconnection2setinstalledshvs-method"></a>INapEnforcementClientConnection2：： SetInstalledShvs 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

NAP 代理程式會使用 **SetInstalledShvs** 方法，將已安裝的系統健康狀態驗證 (shv) 安裝在用戶端上。

## <a name="syntax"></a>語法


```C++
HRESULT SetInstalledShvs(
  [in] SystemHealthEntityCount count,
  [in] SystemHealthEntityId    *ids
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*計數* \[在\]
</dt> <dd>

[SystemHealthEntityCount](nap-datatypes.md)值，指定要在 *識別碼* 中安裝的 shv 數目。

</dd> <dt>

*識別碼* \[在\]
</dt> <dd>

[SystemHealthEntityId](nap-datatypes.md)值的指標，其中包含要安裝的 SHV 識別碼清單。

</dd> </dl>

## <a name="return-value"></a>傳回值

也可能傳回其他 COM 特定的錯誤碼。



| 傳回碼                                                                                  | Description                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> </dl>        | 此方法成功。<br/>          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | *Count* 參數為 0 (零) 。<br/> |



 

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

[**INapEnforcementClientConnection2**](inapenforcementclientconnection2.md)
</dt> </dl>

 

 





