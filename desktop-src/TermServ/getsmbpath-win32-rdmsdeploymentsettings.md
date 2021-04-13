---
title: Win32_RDMSDeploymentSettings 類別的 GetSMBPath 方法
description: 抓取虛擬桌面集合的虛擬機器部署所在 SMB 共用的 UNC 路徑。
ms.assetid: 0a5d3c11-6a77-48f7-a3ea-6f82725ff01f
ms.tgt_platform: multiple
keywords:
- GetSMBPath 方法遠端桌面服務
- GetSMBPath 方法遠端桌面服務，Win32_RDMSDeploymentSettings 類別
- Win32_RDMSDeploymentSettings 類別遠端桌面服務，GetSMBPath 方法
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetSMBPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa1738faf82a6405018495dd762ba9585daa3e1b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385290"
---
# <a name="getsmbpath-method-of-the-win32_rdmsdeploymentsettings-class"></a>Win32 RDMSDeploymentSettings 類別的 GetSMBPath 方法 \_

抓取虛擬桌面集合的虛擬機器部署所在 SMB 共用的 UNC 路徑。

## <a name="syntax"></a>語法


```mof
uint32 GetSMBPath(
  [out] string DirectoryPath
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*DirectoryPath* \[擴展\]
</dt> <dd>

接收 SMB 共用的 UNC 格式化路徑。

</dd> </dl>

## <a name="return-value"></a>傳回值

成功時傳回0，否則會傳回 WMI 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                   |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                              |
| 命名空間<br/>                | 根 \\ CIMv2 \\ rdm<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ RDMSDeploymentSettings**](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





