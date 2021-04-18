---
title: Win32_RDMSDeploymentSettings 類別
description: 管理虛擬桌面集合的部署設定。
ms.assetid: c33563d5-a388-46d3-b23a-797aab9d472a
ms.tgt_platform: multiple
keywords:
- Win32_RDMSDeploymentSettings 類別遠端桌面服務
- Win32_RDMSDeploymentSettings 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6be75f74a71a82800bc6fdd7ba0c4bae5a85021
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508472"
---
# <a name="win32_rdmsdeploymentsettings-class"></a>Win32 \_ RDMSDeploymentSettings 類別

管理虛擬桌面集合的部署設定。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSDeploymentSettings
{
};
```

## <a name="members"></a>成員

**Win32 \_ RDMSDeploymentSettings** 類別具有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**Win32 \_ RDMSDeploymentSettings** 類別具有這些方法。



| 方法                                                                                                  | 描述                                                                                                                       |
|:--------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [**GetBaseVHDPath**](getbasevhdpath-win32-rdmsdeploymentsettings.md)                                   | 抓取虛擬桌面集合 Vhd 部署所在目錄的基底路徑。<br/>                 |
| [**GetConnectionString**](win32-rdmsdeploymentsettings-getconnectionstring.md)                         | 抓取部署層級的資料庫連接字串。<br/>                                                             |
| [**GetDiffVHDPath**](getdiffvhdpath-win32-rdmsdeploymentsettings.md)                                   | 抓取為虛擬桌面集合部署差異磁片的目錄路徑。<br/>            |
| [**GetExportPath**](getexportpath-win32-rdmsdeploymentsettings.md)                                     | 抓取虛擬機器集合的虛擬機器部署所在的目錄路徑。<br/>                  |
| [**GetInt32Property**](getint32property-win32-rdmsdeploymentsettings.md)                               | 抓取虛擬桌面集合部署設定的整數屬性。<br/>                             |
| [**GetSecondaryConnectionString**](win32-rdmsdeploymentsettings-getsecondaryconnectionstring.md)       | 抓取部署層級資料庫的次要連接字串，可用來支援密碼到期。<br/> |
| [**GetSMBPath**](getsmbpath-win32-rdmsdeploymentsettings.md)                                           | 抓取虛擬桌面集合的虛擬機器部署所在 SMB 共用的 UNC 路徑。<br/>      |
| [**GetStringArrayDeploymentSetting**](getstringarraydeploymentsetting-win32-rdmsdeploymentsettings.md) | 抓取虛擬桌面集合的部署設定。<br/>                                                    |
| [**GetStringProperty**](getstringproperty-win32-rdmsdeploymentsettings.md)                             | 抓取虛擬桌面集合之部署設定的字串屬性。<br/>                               |
| [**RemoveDeploymentSetting**](removedeploymentsetting-win32-rdmsdeploymentsettings.md)                 | 刪除虛擬桌面集合的部署設定。<br/>                                                      |
| [**SetBaseVHDPath**](setbasevhdpath-win32-rdmsdeploymentsettings.md)                                   | 抓取虛擬桌面集合 Vhd 部署所在目錄的基底路徑。<br/>                 |
| [**SetConnectionString**](win32-rdmsdeploymentsettings-setconnectionstring.md)                         | 設定部署層級的資料庫連接字串。<br/>                                                                  |
| [**SetDiffVHDPath**](setdiffvhdpath-win32-rdmsdeploymentsettings.md)                                   | 更新為虛擬桌面集合部署差異磁片的目錄路徑。<br/>              |
| [**SetExportPath**](setexportpath-win32-rdmsdeploymentsettings.md)                                     | 更新虛擬機器集合的虛擬機器部署所在的目錄路徑。<br/>                    |
| [**SetInt32Property**](setint32property-win32-rdmsdeploymentsettings.md)                               | 針對虛擬桌面集合的部署設定，更新整數屬性。<br/>                               |
| [**SetSecondaryConnectionString**](win32-rdmsdeploymentsettings-setsecondaryconnectionstring.md)       | 設定部署層級資料庫次要連接字串。<br/>                                                        |
| [**SetSMBPath**](setsmbpath-win32-rdmsdeploymentsettings.md)                                           | 將 UNC 路徑更新為虛擬桌面集合的虛擬機器部署所在的 SMB 共用。<br/>        |
| [**SetStringArrayDeploymentSetting**](setstringarraydeploymentsetting-win32-rdmsdeploymentsettings.md) | 更新虛擬桌面集合的部署設定。<br/>                                                      |
| [**SetStringProperty**](setstringproperty-win32-rdmsdeploymentsettings.md)                             | 更新虛擬桌面集合之部署設定的字串屬性。<br/>                                 |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                   |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                              |
| 命名空間<br/>                | 根 \\ cimv2 \\ rdm<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[遠端桌面管理服務提供者](rdms-api-reference.md)
</dt> </dl>

 

 





