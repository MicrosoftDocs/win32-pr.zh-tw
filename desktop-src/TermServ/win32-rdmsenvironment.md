---
title: Win32_RDMSEnvironment 類別
description: 管理 (RDMS) 環境的遠端桌面管理服務。
ms.assetid: 8a3b10c1-d01d-4e52-8915-29159cc406cc
ms.tgt_platform: multiple
keywords:
- Win32_RDMSEnvironment 類別遠端桌面服務
- Win32_RDMSEnvironment 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_RDMSEnvironment
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a78acb964471844be74481d1ddfa2d4cf56a173
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967331"
---
# <a name="win32_rdmsenvironment-class"></a>Win32 \_ RDMSEnvironment 類別

管理 (RDMS) 環境的遠端桌面管理服務。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSEnvironment
{
};
```

## <a name="members"></a>成員

**Win32 \_ RDMSEnvironment** 類別具有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**Win32 \_ RDMSEnvironment** 類別具有這些方法。



| 方法                                                                   | 描述                                                                                          |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [**GetActiveServer**](getactiveserver-win32-rdmsenvironment.md)         | 捕獲 RDMS 環境 (FQDN) 的完整功能變數名稱。<br/>                 |
| [**GetClientAccessName**](getclientaccessname-win32-rdmsenvironment.md) | 抓取 (DNS) 資源記錄 (RR) RDMS 環境名稱的網域名稱系統。<br/> |
| [**SetActiveServer**](setactiveserver-win32-rdmsenvironment.md)         | 將 RDMS 環境的 FQDN 設定為目前的節點。<br/>                                |
| [**SetClientAccessName**](setclientaccessname-win32-rdmsenvironment.md) | 更新 RDM 環境的 DNS RR 名稱。<br/>                                          |



 

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

 

 





