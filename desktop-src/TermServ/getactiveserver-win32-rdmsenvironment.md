---
title: Win32_RDMSEnvironment 類別的 GetActiveServer 方法
description: 抓取遠端桌面管理服務 (RDMS) 環境 (FQDN) 的完整功能變數名稱。
ms.assetid: 87e25d11-de1d-41d1-974d-2871dde444b5
ms.tgt_platform: multiple
keywords:
- GetActiveServer 方法遠端桌面服務
- GetActiveServer 方法遠端桌面服務，Win32_RDMSEnvironment 類別
- Win32_RDMSEnvironment 類別遠端桌面服務，GetActiveServer 方法
topic_type:
- apiref
api_name:
- Win32_RDMSEnvironment.GetActiveServer
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4265315e3ed2de87e564adab87c023401bbd55e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465801"
---
# <a name="getactiveserver-method-of-the-win32_rdmsenvironment-class"></a>Win32 RDMSEnvironment 類別的 GetActiveServer 方法 \_

抓取遠端桌面管理服務 (RDMS) 環境 (FQDN) 的完整功能變數名稱。

## <a name="syntax"></a>語法


```mof
uint32 GetActiveServer(
  [out] string ServerName
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ServerName* \[擴展\]
</dt> <dd>

接收已抓取的 FQDN。

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

[**Win32 \_ RDMSEnvironment**](win32-rdmsenvironment.md)
</dt> </dl>

 

 





