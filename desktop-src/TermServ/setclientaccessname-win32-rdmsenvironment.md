---
title: Win32_RDMSEnvironment 類別的 SetClientAccessName 方法
description: 將網域名稱系統 (DNS) 資源記錄 (RR) 遠端桌面管理服務 (的) 環境的名稱。
ms.assetid: bbce3fc1-d2c5-4874-bdd0-be27fb5981d1
ms.tgt_platform: multiple
keywords:
- SetClientAccessName 方法遠端桌面服務
- SetClientAccessName 方法遠端桌面服務，Win32_RDMSEnvironment 類別
- Win32_RDMSEnvironment 類別遠端桌面服務，SetClientAccessName 方法
topic_type:
- apiref
api_name:
- Win32_RDMSEnvironment.SetClientAccessName
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13f9087fe2c2139833baeb21bc62da508c6e5989
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966540"
---
# <a name="setclientaccessname-method-of-the-win32_rdmsenvironment-class"></a>Win32 RDMSEnvironment 類別的 SetClientAccessName 方法 \_

將網域名稱系統 (DNS) 資源記錄 (RR) 遠端桌面管理服務 (的) 環境的名稱。

## <a name="syntax"></a>語法


```mof
uint32 SetClientAccessName(
  [in] string ClientAccessName
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ClientAccessName* \[在\]
</dt> <dd>

新的 RR 名稱。

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

 

 





