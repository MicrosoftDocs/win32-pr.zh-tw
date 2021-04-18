---
title: Win32_SessionBrokerServiceProperties 類別
description: 定義 session broker 服務的查詢。
ms.assetid: fe7a0317-8b52-4685-9d0d-2f81058b4561
ms.tgt_platform: multiple
keywords:
- Win32_SessionBrokerServiceProperties 類別遠端桌面服務
- Win32_SessionBrokerServiceProperties 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties
- Win32_SessionBrokerServiceProperties.SBNetworkName
- Win32_SessionBrokerServiceProperties.SBDbConnectionString
- Win32_SessionBrokerServiceProperties.SBDbSecondaryConnectionString
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 507c4211b9506e0635966e9541167d24495735ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509376"
---
# <a name="win32_sessionbrokerserviceproperties-class"></a>Win32 \_ SessionBrokerServiceProperties 類別

定義 session broker 服務的查詢。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[dynamic, singleton, provider("Win32_WIN32_SESSIONBROKERSERVICEPROPERTIES_Prov"), AMENDMENT]
class Win32_SessionBrokerServiceProperties
{
  string SBNetworkName;
  string SBDbConnectionString;
  string SBDbSecondaryConnectionString;
};
```

## <a name="members"></a>成員

**Win32 \_ SessionBrokerServiceProperties** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](/windows)

### <a name="methods"></a>方法

**Win32 \_ SessionBrokerServiceProperties** 類別具有這些方法。



| 方法                                                                                                | 描述                                                                                                                                                                                                                          |
|:------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DeleteSBDbConnectionString**](win32-sessionbrokerserviceproperties-deletesbdbconnectionstring.md) | 從登錄中刪除主要和次要)  (的資料庫連接字串。<br/> **Windows server 2012 r2、Windows server 2012 和 Windows server 2008 R2：** 在 Windows Server 2016 之前無法使用此方法<br/> |
| [**InstallBrokerDatabase**](win32-sessionbrokerserviceproperties-installbrokerdatabase.md)           | 在中央 SQL Server 上安裝 RD 連線代理人 DB<br/>                                                                                                                                                                    |
| [**IsDbReachable**](win32-sessionbrokerserviceproperties-isdbreachable.md)                           | 檢查資料庫是否可連線<br/>                                                                                                                                                                                                 |
| [**SetBrokerHAMode**](win32-sessionbrokerserviceproperties-setbrokerhamode.md)                       | 將資料從本機 WID 資料庫移轉至新的 SQL Server 資料庫。 它也會將訊息代理程式伺服器設定為使用中央 SQL Server<br/>                                                                                        |
| [**SetBrokerNonHAMode**](win32-sessionbrokerserviceproperties-setbrokernonhamode.md)                 | 將資料從中央 SQL Server 遷移至本機 DB。 它也會將訊息代理程式伺服器設定為使用本機資料庫。<br/>                                                                                                              |
| [**SetSBDbConnectionStrings**](win32-sessionbrokerserviceproperties-setsbdbconnectionstrings.md)     | 將資料庫連接字串儲存 (主要和次要) 登錄中。<br/> **Windows server 2012 r2、Windows server 2012 和 Windows server 2008 R2：** 在 Windows Server 2016 之前無法使用此方法<br/>     |



 

### <a name="properties"></a>屬性

**Win32 \_ SessionBrokerServiceProperties** 類別具有這些屬性。

<dl> <dt>

**SBDbConnectionString**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

Session Broker 服務所使用的資料庫連接字串。

**Windows Server 2008 R2：** 此屬性在 Windows Server 2012 之前無法使用

</dd> <dt>

**SBDbSecondaryConnectionString**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

選擇性。 Session Broker 服務用來支援密碼到期的次要資料庫連接字串。

**Windows server 2012 r2、Windows server 2012 和 Windows server 2008 R2：** 此屬性在 Windows Server 2016 之前無法使用

</dd> <dt>

**SBNetworkName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

Session broker 服務所使用的網路名稱。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                              |
| 最低支援的伺服器<br/> | Windows Server 2008 R2<br/>                                                      |
| 命名空間<br/>                | 根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



 

