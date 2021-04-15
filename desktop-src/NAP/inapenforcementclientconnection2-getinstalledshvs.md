---
title: 'INapEnforcementClientConnection2 GetInstalledShvs 方法 (NapEnforcementClient .h) '
description: NAP 代理程式用來查詢用戶端上已安裝的系統健康狀態驗證 (Shv) 。
ms.assetid: b2e3ab29-90bf-4117-bc2e-2ff2827ee15c
keywords:
- GetInstalledShvs 方法 NAP
- GetInstalledShvs 方法 NAP，INapEnforcementClientConnection2 介面
- INapEnforcementClientConnection2 介面 NAP，GetInstalledShvs 方法
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection2.GetInstalledShvs
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa54d09a0c3d3c524262231982f662c497920a0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104467068"
---
# <a name="inapenforcementclientconnection2getinstalledshvs-method"></a>INapEnforcementClientConnection2：： GetInstalledShvs 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

NAP 代理程式會使用 **GetInstalledShvs** 方法來查詢用戶端上已安裝的系統健康狀態驗證 (shv) 。

## <a name="syntax"></a>語法


```C++
HRESULT GetInstalledShvs(
  [out] SystemHealthEntityCount *count,
  [out] SystemHealthEntityId    **ids
) const;
```



## <a name="parameters"></a>參數

<dl> <dt>

*計數* \[擴展\]
</dt> <dd>

[SystemHealthEntityCount](nap-datatypes.md)值的指標，指定 *識別碼* 中已安裝的 shv 數目。

</dd> <dt>

*識別碼* \[擴展\]
</dt> <dd>

[SystemHealthEntityId](nap-datatypes.md)值陣列的指標，其中包含已安裝的 SHV 識別碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

也可能傳回其他 COM 特定的錯誤碼。



| 傳回碼                                                                                   | Description                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> </dl>         | 作業成功。<br/>                          |
| <dl> <dt>**E \_INVALIDARG**</dt> </dl> | 傳遞給方法的引數無效。<br/> |



 

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

 

 





