---
title: Win32_RDMSDeploymentSettings 類別的 GetDiffVHDPath 方法
description: 抓取為虛擬桌面集合部署差異磁片的目錄路徑。
ms.assetid: 4340c817-2276-48a1-a856-b4c9e91ea981
ms.tgt_platform: multiple
keywords:
- GetDiffVHDPath 方法遠端桌面服務
- GetDiffVHDPath 方法遠端桌面服務，Win32_RDMSDeploymentSettings 類別
- Win32_RDMSDeploymentSettings 類別遠端桌面服務，GetDiffVHDPath 方法
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetDiffVHDPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7391315013cf8487d93b32f645933d14f06db2d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384054"
---
# <a name="getdiffvhdpath-method-of-the-win32_rdmsdeploymentsettings-class"></a>Win32 RDMSDeploymentSettings 類別的 GetDiffVHDPath 方法 \_

抓取為虛擬桌面集合部署差異磁片的目錄路徑。

## <a name="syntax"></a>語法


```mof
uint32 GetDiffVHDPath(
  [out] string DirectoryPath
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*DirectoryPath* \[擴展\]
</dt> <dd>

接收新的差異磁片路徑。

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

 

 





