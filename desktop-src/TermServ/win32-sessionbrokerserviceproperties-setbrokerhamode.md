---
title: Win32_SessionBrokerServiceProperties 類別的 SetBrokerHAMode 方法
description: 將資料從本機 WID 資料庫移轉至新的 SQL server 資料庫。 它也會將訊息代理程式伺服器設定為使用中央 SQL server。
ms.assetid: 8f14590d-3042-403c-a1cb-a3b257866284
ms.tgt_platform: multiple
keywords:
- SetBrokerHAMode 方法遠端桌面服務
- SetBrokerHAMode 方法遠端桌面服務，Win32_SessionBrokerServiceProperties 類別
- Win32_SessionBrokerServiceProperties 類別遠端桌面服務，SetBrokerHAMode 方法
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.SetBrokerHAMode
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4526f8ded96086ccf223b3c8e5aad72d9e0262cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103673"
---
# <a name="setbrokerhamode-method-of-the-win32_sessionbrokerserviceproperties-class"></a>Win32 SessionBrokerServiceProperties 類別的 SetBrokerHAMode 方法 \_

將資料從本機 WID 資料庫移轉至新的 SQL server 資料庫。 它也會將訊息代理程式伺服器設定為使用中央 SQL server。

## <a name="syntax"></a>語法


```mof
uint32 SetBrokerHAMode(
  [in] string connStringToCentralDBRdcms,
  [in] string secondaryConnStringToCentralDBRdcms,
  [in] string brokerDnsRRName,
  [in] string activeBrokerName
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*connStringToCentralDBRdcms* \[在\]
</dt> <dd>

中央資料庫的連接字串。

</dd> <dt>

*secondaryConnStringToCentralDBRdcms* \[在\]
</dt> <dd>

中央資料庫的次要連接字串。

**Windows server 2012 R2 和 Windows server 2012：** 此參數在 Windows Server 2016 之前無法使用。

</dd> <dt>

*brokerDnsRRName* \[在\]
</dt> <dd>

訊息代理程式 DNS 名稱。

</dd> <dt>

*activeBrokerName* \[在\]
</dt> <dd>

Active broker 名稱。

**Windows server 2012 R2 和 Windows server 2012：** 此參數在 Windows Server 2016 之前無法使用。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                              |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                         |
| 命名空間<br/>                | 根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ SessionBrokerServiceProperties**](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 





