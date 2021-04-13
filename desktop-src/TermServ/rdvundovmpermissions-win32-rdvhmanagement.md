---
title: Win32_RdvhManagement 類別的 RdvUndoVMPermissions 方法
description: 在指定的虛擬機器上還原 RdvSetupVMPermissions 所設定的許可權。
ms.assetid: 3331430e-7427-42f7-ab09-27fece8dc3ca
ms.tgt_platform: multiple
keywords:
- RdvUndoVMPermissions 方法遠端桌面服務
- RdvUndoVMPermissions 方法遠端桌面服務，Win32_RdvhManagement 類別
- Win32_RdvhManagement 類別遠端桌面服務，RdvUndoVMPermissions 方法
topic_type:
- apiref
api_name:
- Win32_RdvhManagement.RdvUndoVMPermissions
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d1dc8892435522dcd2c7457fe4b74a0d9671740
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466741"
---
# <a name="rdvundovmpermissions-method-of-the-win32_rdvhmanagement-class"></a>Win32 RdvhManagement 類別的 RdvUndoVMPermissions 方法 \_

在指定的虛擬機器上還原 [**RdvSetupVMPermissions**](rdvsetupvmpermissions-win32-rdvhmanagement.md) 所設定的許可權。

## <a name="syntax"></a>語法


```mof
uint32 RdvUndoVMPermissions(
  [in] string VmName
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*VmName* \[在\]
</dt> <dd>

要復原許可權的虛擬機器名稱。

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

 

 





