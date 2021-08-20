---
title: 'Win32_RDMSDeploymentSettings 類別的 GetInt32Property 方法 (appanalysis .h) '
description: 抓取虛擬桌面集合部署設定的整數屬性。
ms.assetid: 6b8174bb-ffb7-4699-a3fb-d32ab0b202fc
ms.tgt_platform: multiple
keywords:
- GetInt32Property 方法遠端桌面服務
- GetInt32Property 方法遠端桌面服務，Win32_RDMSDeploymentSettings 類別
- Win32_RDMSDeploymentSettings 類別遠端桌面服務，GetInt32Property 方法
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ac79fdacf6b8f64d354158f964be1019692933a10409a8bf085109d9f5a9a31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118130757"
---
# <a name="getint32property-method-of-the-win32_rdmsdeploymentsettings-class"></a>Win32 RDMSDeploymentSettings 類別的 GetInt32Property 方法 \_

抓取虛擬桌面集合部署設定的整數屬性。

## <a name="syntax"></a>語法


```mof
uint32 GetInt32Property(
  [in]  string Key,
  [out] sint32 Value
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

接收已抓取值的整數。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                                      |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                                                 |
| 命名空間<br/>                | 根 \\ CIMv2 \\ rdm<br/>                                                                                   |
| 標頭<br/>                   | <dl> <dt>Appanalysis。h</dt> </dl> |
| MOF<br/>                      | <dl> <dt>RDManagement mof</dt> </dl>                    |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>                            |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ RDMSDeploymentSettings**](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





