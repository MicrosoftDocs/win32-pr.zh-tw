---
title: Win32_RDMSEnvironment 類別的 GetClientAccessName 方法
description: 抓取網域名稱系統 (DNS) 資源記錄 (RR) 遠端桌面管理服務 (的) 環境名稱。
ms.assetid: 16f9d00d-a398-4a73-a641-ac552ba6a9d3
ms.tgt_platform: multiple
keywords:
- GetClientAccessName 方法遠端桌面服務
- GetClientAccessName 方法遠端桌面服務，Win32_RDMSEnvironment 類別
- Win32_RDMSEnvironment 類別遠端桌面服務，GetClientAccessName 方法
topic_type:
- apiref
api_name:
- Win32_RDMSEnvironment.GetClientAccessName
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 206ef89765bd18a73559c98d70a614664d076099214bd20f7b97ca9c29e94bc3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139001"
---
# <a name="getclientaccessname-method-of-the-win32_rdmsenvironment-class"></a>Win32 RDMSEnvironment 類別的 GetClientAccessName 方法 \_

抓取網域名稱系統 (DNS) 資源記錄 (RR) 遠端桌面管理服務 (的) 環境名稱。

## <a name="syntax"></a>語法


```mof
uint32 GetClientAccessName(
  [out] string ClientAccessName
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ClientAccessName* \[擴展\]
</dt> <dd>

接收已抓取的 RR 名稱。

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

 

 





