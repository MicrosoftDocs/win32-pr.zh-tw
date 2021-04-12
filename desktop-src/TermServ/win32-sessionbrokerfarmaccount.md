---
title: Win32_SessionBrokerFarmAccount 類別
description: Win32 \_ SessionBrokerFarmAccount 類別無法再供 Windows Server 2012 使用。 |Win32_SessionBrokerFarmAccount 類別
ms.assetid: a76ade0f-cd94-438c-bc07-30dc4b4ee6c8
ms.tgt_platform: multiple
keywords:
- Win32_SessionBrokerFarmAccount 類別遠端桌面服務
- Win32_SessionBrokerFarmAccount 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_SessionBrokerFarmAccount
- Win32_SessionBrokerFarmAccount.FarmName
- Win32_SessionBrokerFarmAccount.Manual
- Win32_SessionBrokerFarmAccount.AccountName
- Win32_SessionBrokerFarmAccount.AccountDomain
- Win32_SessionBrokerFarmAccount.AccountPassword
- Win32_SessionBrokerFarmAccount.AccountSPN1
- Win32_SessionBrokerFarmAccount.AccountSPN2
- Win32_SessionBrokerFarmAccount.ComputerDNSName
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a31f076ddc6f9361be12a57dc60ada24ed75e4bb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103696517"
---
# <a name="win32_sessionbrokerfarmaccount-class"></a>Win32 \_ SessionBrokerFarmAccount 類別

\[**Win32 \_ SessionBrokerFarmAccount** 類別無法再供 Windows Server 2012 使用。\]

定義 session broker 伺服器陣列帳戶。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONBROKERFARMACCOUNT_Prov"), AMENDMENT]
class Win32_SessionBrokerFarmAccount
{
  string  FarmName;
  boolean Manual;
  string  AccountName;
  string  AccountDomain;
  string  AccountPassword;
  string  AccountSPN1;
  string  AccountSPN2;
  string  ComputerDNSName;
};
```

## <a name="members"></a>成員

**Win32 \_ SessionBrokerFarmAccount** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Win32 \_ SessionBrokerFarmAccount** 類別具有這些方法。



| 方法                                                      | 描述                          |
|:------------------------------------------------------------|:-------------------------------------|
| [**DeleteEx**](deleteex-win32-sessionbrokerfarmaccount.md) | 刪除伺服器陣列帳戶。<br/> |



 

### <a name="properties"></a>屬性

**Win32 \_ SessionBrokerFarmAccount** 類別具有這些屬性。

<dl> <dt>

**AccountDomain**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

伺服器陣列帳戶所屬網域的名稱。

</dd> <dt>

**AccountName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

伺服器陣列帳戶的名稱。

</dd> <dt>

**AccountPassword**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

伺服器陣列帳戶的密碼。

</dd> <dt>

**AccountSPN1**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

第一個服務主體名稱 (SPN) 與伺服器陣列帳戶相關聯。

</dd> <dt>

**AccountSPN2**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

與伺服器陣列帳戶相關聯的第二個 SPN。

</dd> <dt>

**ComputerDNSName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

與伺服器陣列帳戶相關聯之電腦的 DNS 名稱。

</dd> <dt>

**FarmName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

會話代理程式伺服器陣列的名稱。

</dd> <dt>

**手動**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指出是否以手動方式更新帳戶的密碼。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                              |
| 最低支援的伺服器<br/> | Windows Server 2008 R2<br/>                                                      |
| 用戶端支援結束<br/>    | 都不支援<br/>                                                              |
| 伺服器支援結束<br/>    | Windows Server 2008 R2<br/>                                                      |
| 命名空間<br/>                | 根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



 

