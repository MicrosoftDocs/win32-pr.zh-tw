---
title: Win32_RDMSDeploymentSettings 類別的 GetBaseVHDPath 方法
description: 抓取虛擬桌面集合 Vhd 部署所在目錄的基底路徑。 |Win32_RDMSDeploymentSettings 類別的 GetBaseVHDPath 方法
ms.assetid: d3629a08-ef16-4aab-b74b-f837a8ba00d0
ms.tgt_platform: multiple
keywords:
- GetBaseVHDPath 方法遠端桌面服務
- GetBaseVHDPath 方法遠端桌面服務，Win32_RDMSDeploymentSettings 類別
- Win32_RDMSDeploymentSettings 類別遠端桌面服務，GetBaseVHDPath 方法
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetBaseVHDPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 595c6459148a0270bed2328c70e15ef74a69acf3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103945897"
---
# <a name="getbasevhdpath-method-of-the-win32_rdmsdeploymentsettings-class"></a>Win32 RDMSDeploymentSettings 類別的 GetBaseVHDPath 方法 \_

抓取虛擬桌面集合 Vhd 部署所在目錄的基底路徑。

## <a name="syntax"></a>語法


```mof
uint32 GetBaseVHDPath(
  [out] string DirectoryPath
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*DirectoryPath* \[擴展\]
</dt> <dd>

接收 VHD 部署路徑。

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

 

 





