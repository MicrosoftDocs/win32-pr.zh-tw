---
title: Win32_RDMSVirtualDesktopCollection 類別的 ProvisioningPrepJob 方法
description: 建立虛擬桌面布建作業。
ms.assetid: 240D4BE6-95BD-4858-8F8F-A00C92042AEF
ms.tgt_platform: multiple
keywords:
- ProvisioningPrepJob 方法遠端桌面服務
- ProvisioningPrepJob 方法遠端桌面服務，Win32_RDMSVirtualDesktopCollection 介面
- Win32_RDMSVirtualDesktopCollection 介面遠端桌面服務，ProvisioningPrepJob 方法
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.ProvisioningPrepJob
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2dab9dcbd606dd32857f0d2dc4b2de3d8516e2b2da10e804fa36254679c1d2b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119422838"
---
# <a name="provisioningprepjob-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>Win32 RDMSVirtualDesktopCollection 類別的 ProvisioningPrepJob 方法 \_

建立虛擬桌面布建作業。

## <a name="syntax"></a>語法


```mof
uint32 ProvisioningPrepJob(
  [in]  string  CollectionAlias,
  [in]  string  VMHostName,
  [in]  string  VMName,
  [in]  string  ExportToLocation,
  [in]  boolean bSysPrep,
  [in]  string  MachineName,
  [in]  string  UserName,
  [in]  string  Password,
  [out] string  JobGuid
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*CollectionAlias* \[在\]
</dt> <dd>

裝載虛擬桌面之集合的別名。

</dd> <dt>

*VMHostName* \[在\]
</dt> <dd>

虛擬機器主機名稱。

</dd> <dt>

*VMName* \[在\]
</dt> <dd>

虛擬機器的名稱。

</dd> <dt>

*ExportToLocation* \[在\]
</dt> <dd>

要匯出布建作業之位置的完整路徑。

</dd> <dt>

*bSysPrep* \[在\]
</dt> <dd>

指出布建作業是否代表 Sysprep 部署。

</dd> <dt>

*MachineName* \[在\]
</dt> <dd>

裝載虛擬機器之電腦的電腦名稱稱。

</dd> <dt>

使用者 *名稱* \[在\]
</dt> <dd>

虛擬機器的系統管理員使用者名稱。

</dd> <dt>

*密碼* \[在\]
</dt> <dd>

虛擬機器的系統管理員密碼。

</dd> <dt>

*JobGuid* \[擴展\]
</dt> <dd>

可唯一識別布建作業的 **GUID** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

成功時傳回0，否則會傳回 WMI 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                   |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                              |
| 命名空間<br/>                | 根 \\ cimv2 \\ rdm<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ RDMSVirtualDesktopCollection**](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





