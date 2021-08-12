---
title: Win32_RDMSDeploymentSettings 類別的 SetBaseVHDPath 方法
description: 抓取虛擬桌面集合 Vhd 部署所在目錄的基底路徑。 |Win32_RDMSDeploymentSettings 類別的 SetBaseVHDPath 方法
ms.assetid: 1ea4cd93-ef17-4ec9-82f9-382c549f189c
ms.tgt_platform: multiple
keywords:
- SetBaseVHDPath 方法遠端桌面服務
- SetBaseVHDPath 方法遠端桌面服務，Win32_RDMSDeploymentSettings 類別
- Win32_RDMSDeploymentSettings 類別遠端桌面服務，SetBaseVHDPath 方法
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetBaseVHDPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6179c87e6566a18f2c47046007a17c6073a51e0afcdce4925b50d327adf528f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118605115"
---
# <a name="setbasevhdpath-method-of-the-win32_rdmsdeploymentsettings-class"></a>Win32 RDMSDeploymentSettings 類別的 SetBaseVHDPath 方法 \_

抓取虛擬桌面集合 Vhd 部署所在目錄的基底路徑。

## <a name="syntax"></a>語法


```mof
uint32 SetBaseVHDPath(
  [in] string DirectoryPath
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*DirectoryPath* \[在\]
</dt> <dd>

新的 VHD 部署路徑。

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

 

 





