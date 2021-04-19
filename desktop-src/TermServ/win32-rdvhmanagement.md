---
title: Win32_RdvhManagement 類別
description: 描述 (RDVH) 管理服務的遠端桌面虛擬主機。
ms.assetid: 2a81786c-e772-4596-9846-a46828f9b48b
ms.tgt_platform: multiple
keywords:
- Win32_RdvhManagement 類別遠端桌面服務
- Win32_RdvhManagement 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_RdvhManagement
api_location:
- TSVmHostWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b01e2cde81173035d00587782dc45d9ddeb66fcf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967543"
---
# <a name="win32_rdvhmanagement-class"></a>Win32 \_ RdvhManagement 類別

描述 (RDVH) 管理服務的遠端桌面虛擬主機。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[dynamic, provider("Win32_TSVmHost_Prov"), AMENDMENT]
class Win32_RdvhManagement
{
};
```

## <a name="members"></a>成員

**Win32 \_ RdvhManagement** 類別具有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**Win32 \_ RdvhManagement** 類別具有這些方法。



| 方法                                                                                  | 描述                                                                                                                                                             |
|:----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RdvCreateUserDiskTemplate**](rdvcreateuserdisktemplate-win32-rdvhmanagement.md)     | 建立指定的大小上限和指定位置的使用者磁片範本。 所有建立的使用者磁片都會有符合範本大小上限的大小上限。<br/> |
| [**RdvMigrateVmToDifferentHost**](rdvmigratevmtodifferenthost-win32-rdvhmanagement.md) | 在 VDI 案例中起始虛擬機器的即時移轉<br/>                                                                                               |
| [**RdvCopyBaseVmLocally**](rdvcopybasevmlocally-win32-rdvhmanagement.md)               | 在本機將基底 VM 位置複製到 RDV 主機伺服器<br/>                                                                                                           |
| [**RdvCreateUserDiskTemplate**](rdvcreateuserdisktemplate-win32-rdvhmanagement.md)     | 建立指定的大小上限和指定位置的使用者磁片範本。 所有建立的使用者磁片都會有符合範本大小上限的大小上限。<br/> |
| [**RdvMigrateVmToDifferentHost**](rdvmigratevmtodifferenthost-win32-rdvhmanagement.md) | 在 VDI 案例中起始虛擬機器的即時移轉。<br/>                                                                                              |
| [**RdvSetupVMPermissions**](rdvsetupvmpermissions-win32-rdvhmanagement.md)             | 在 VM 中設定呼叫端的許可權<br/>                                                                                                                        |
| [**RdvUndoVMPermissions**](rdvundovmpermissions-win32-rdvhmanagement.md)               | 在 RdvSetupVMPermissions 中還原 VM 所設定的許可權<br/>                                                                                                       |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                  |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                             |
| 命名空間<br/>                | 根 \\ cimv2 \\ microsoft-windows-terminalservices-gateway<br/>                                                   |
| MOF<br/>                      | <dl> <dt>TSVmHost mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>TSVmHostWmi.dll</dt> </dl> |



 

 





