---
title: Win32_SessionBrokerFarmAccount 類別的 DeleteEx 方法
description: '\_Windows Server 2012 不能再使用 Win32 SessionBrokerFarmAccount 類別。 |Win32_SessionBrokerFarmAccount 類別的 DeleteEx 方法'
ms.assetid: d30c5d3e-f63c-4b21-85ae-a0b8d5868d64
ms.tgt_platform: multiple
keywords:
- DeleteEx 方法遠端桌面服務
- DeleteEx 方法遠端桌面服務，Win32_SessionBrokerFarmAccount 類別
- Win32_SessionBrokerFarmAccount 類別遠端桌面服務，DeleteEx 方法
topic_type:
- apiref
api_name:
- Win32_SessionBrokerFarmAccount.DeleteEx
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa891c874c9592ed11b2aa0840913e67daa7226a93f6f746cf74c45a0454a476
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080218"
---
# <a name="deleteex-method-of-the-win32_sessionbrokerfarmaccount-class"></a>Win32 SessionBrokerFarmAccount 類別的 DeleteEx 方法 \_

\[Windows Server 2012 不能再使用 [**Win32 \_ SessionBrokerFarmAccount**](win32-sessionbrokerfarmaccount.md)類別。\]

刪除伺服器陣列帳戶。

## <a name="syntax"></a>語法


```mof
uint32 DeleteEx(
  [in] boolean DeleteComputerObject
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*DeleteComputerObject* \[在\]
</dt> <dd>

指出是否要從 Active Directory 移除與伺服器陣列相關聯的電腦物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

成功時傳回0，否則會傳回 WMI 錯誤碼。 如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                              |
| 最低支援的伺服器<br/> | Windows Server 2008 R2<br/>                                                      |
| 用戶端支援結束<br/>    | 都不支援<br/>                                                              |
| 伺服器支援結束<br/>    | Windows Server 2008 R2<br/>                                                      |
| 命名空間<br/>                | 根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ SessionBrokerFarmAccount**](win32-sessionbrokerfarmaccount.md)
</dt> </dl>

 

 





