---
title: Win32_RdvhManagement 類別的 RdvMigrateVmToDifferentHost 方法
description: 起始虛擬機器到指定主機的即時移轉。
ms.assetid: aa4b1e57-a97c-410b-9b9d-423a1c77de70
ms.tgt_platform: multiple
keywords:
- RdvMigrateVmToDifferentHost 方法遠端桌面服務
- RdvMigrateVmToDifferentHost 方法遠端桌面服務，Win32_RdvhManagement 類別
- Win32_RdvhManagement 類別遠端桌面服務，RdvMigrateVmToDifferentHost 方法
topic_type:
- apiref
api_name:
- Win32_RdvhManagement.RdvMigrateVmToDifferentHost
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a84171bc6db6a39cff5a2d55ca7e453bf9b963636ea765480fe87b16fd8da92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117756240"
---
# <a name="rdvmigratevmtodifferenthost-method-of-the-win32_rdvhmanagement-class"></a>Win32 RdvhManagement 類別的 RdvMigrateVmToDifferentHost 方法 \_

起始虛擬機器到指定主機的即時移轉。

## <a name="syntax"></a>語法


```mof
uint32 RdvMigrateVmToDifferentHost(
  [in] string VmName,
  [in] string DestinationHost
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*VmName* \[在\]
</dt> <dd>

要遷移的虛擬機器名稱。

</dd> <dt>

*DestinationHost* \[在\]
</dt> <dd>

目的地主機的名稱。

</dd> </dl>

## <a name="return-value"></a>傳回值

成功時傳回0，否則會傳回 WMI 錯誤碼。 如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                  |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                             |
| 命名空間<br/>                | 根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway<br/>                                                   |
| MOF<br/>                      | <dl> <dt>TSVmHost mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>TSVmHostWmi.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ RdvhManagement**](win32-rdvhmanagement.md)
</dt> </dl>

 

 





