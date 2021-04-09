---
title: Win32_RDMSDeploymentSettings 類別的 GetStringArrayDeploymentSetting 方法
description: 抓取虛擬桌面集合的部署設定。
ms.assetid: ab380618-560e-425b-9bf0-a7de6b30d01a
ms.tgt_platform: multiple
keywords:
- GetStringArrayDeploymentSetting 方法遠端桌面服務
- GetStringArrayDeploymentSetting 方法遠端桌面服務，Win32_RDMSDeploymentSettings 類別
- Win32_RDMSDeploymentSettings 類別遠端桌面服務，GetStringArrayDeploymentSetting 方法
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetStringArrayDeploymentSetting
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9ac0b82441abef8af1b4f6c8e3bd48b89a8cb6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094119"
---
# <a name="getstringarraydeploymentsetting-method-of-the-win32_rdmsdeploymentsettings-class"></a>Win32 RDMSDeploymentSettings 類別的 GetStringArrayDeploymentSetting 方法 \_

抓取虛擬桌面集合的部署設定。

## <a name="syntax"></a>語法


```mof
uint32 GetStringArrayDeploymentSetting(
  [in]  string Key,
  [out] string Value[]
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*金鑰* \[在\]
</dt> <dd>

虛擬桌面集合的別名。

</dd> <dt>

*值* \[擴展\]
</dt> <dd>

接收包含部署設定的字串陣列。

</dd> </dl>

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

 

 





