---
title: MDM_ActiveSync_User_Accounts01_01 類別
description: MDM \_ ActiveSync \_ 使用者 \_ Accounts01 \_ 01 類別會定義所有可用的 ActiveSync 帳戶。
ms.assetid: bcd1fdcb-675a-4833-9d3c-0509e68f7b00
keywords:
- MDM_ActiveSync_User_Accounts01_01 類別
- MDM_ActiveSync_User_Accounts01_01 類別，描述
topic_type:
- apiref
api_name:
- MDM_ActiveSync_User_Accounts01_01
- MDM_ActiveSync_User_Accounts01_01.InstanceID
- MDM_ActiveSync_User_Accounts01_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59532fed7b8ff5a866a438040a3d7f78d75f262d6ef5ffb20dd632a7adfd7dc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077404"
---
# <a name="mdm_activesync_user_accounts01_01-class"></a>MDM \_ ActiveSync \_ 使用者 \_ Accounts01 \_ 01 類別

\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。 Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]

**MDM \_ ActiveSync \_ 使用者 \_ Accounts01 \_ 01** 類別會定義所有可用的 ActiveSync 帳戶。

下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_ActiveSync_User_Accounts01_01
{
  string InstanceID;
  string ParentID;
  string EmailAddress;
  string Domain;
  string AccountIcon;
  string AccountType;
  string AccountName;
  string Password;
  string ServerName;
  string UserName;
};
```

## <a name="members"></a>成員

**MDM \_ ActiveSync \_ 使用者 \_ Accounts01 \_ 01** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**MDM \_ ActiveSync \_ 使用者 \_ Accounts01 \_ 01** 類別具有這些屬性。

<dl> <dt>

[AccountIcon](/windows/client-management/mdm/activesync-csp#account-guid-accounticon)
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[AccountName](/windows/client-management/mdm/activesync-csp#account-guid-accountname)
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[AccountType](/windows/client-management/mdm/activesync-csp#account-guid-accounttype)
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[網域](/windows/client-management/mdm/activesync-csp#account-guid-domain)
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[EmailAddress](/windows/client-management/mdm/activesync-csp#account-guid-emailaddress)
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

識別父節點的名稱。

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

描述父節點的完整路徑。 此類別的字串為 "./Vendor/MSFT/ActiveSync/"

</dd> <dt>

[密碼](/windows/client-management/mdm/activesync-csp#account-guid-password)
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[ServerName](/windows/client-management/mdm/activesync-csp#account-guid-servername)
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[使用者名稱](/windows/client-management/mdm/activesync-csp#account-guid-username)
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 \[僅限桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                      |
| 命名空間<br/>                | 根 \\ cimv2 \\ mdm \\ dmmap<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[使用 PowerShell 指令碼搭配 WMI 橋接器提供者](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

