---
title: MDM_Policy_Result01_Accounts02 類別
description: MDM \_ Policy \_ Result01 \_ Accounts02 類別代表與帳戶相關的原則。
ms.assetid: 581d63de-6ea8-4c4a-8b94-06228ed07371
keywords:
- MDM_Policy_Result01_Accounts02 類別
- MDM_Policy_Result01_Accounts02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Accounts02
- MDM_Policy_Result01_Accounts02.InstanceID
- MDM_Policy_Result01_Accounts02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a786251bbd2d95e57633e090e3226faaaa804e5a52b019011f7fc9c8b106382
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118164818"
---
# <a name="mdm_policy_result01_accounts02-class"></a>MDM \_ 原則 \_ Result01 \_ Accounts02 類別

\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。 Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]

**MDM \_ Policy \_ Result01 \_ Accounts02** 類別代表與帳戶相關的原則。

下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Accounts02
{
  string InstanceID;
  string ParentID;
  sint32 AllowMicrosoftAccountConnection;
  sint32 AllowMicrosoftAccountSignInAssistant;
  sint32 AllowAddingNonMicrosoftAccountsManually;
  string DomainNamesForEmailSync;
};
```

## <a name="members"></a>成員

**MDM \_ Policy \_ Result01 \_ Accounts02** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**MDM \_ Policy \_ Result01 \_ Accounts02** 類別具有這些屬性。

<dl> <dt>

[AllowAddingNonMicrosoftAccountsManually](/windows/client-management/mdm/policy-csp-accounts#accounts-allowaddingnonmicrosoftaccountsmanually)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[AllowMicrosoftAccountConnection](/windows/client-management/mdm/policy-csp-accounts#accounts-allowmicrosoftaccountconnection)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[AllowMicrosoftAccountSignInAssistant](/windows/client-management/mdm/policy-csp-accounts#accounts-allowmicrosoftaccountsigninassistant)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

DomainNamesForEmailSync
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

識別父節點的名稱。 此類別的字串為 "Accounts"。

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

描述父節點的完整路徑。 此類別的字串為 "./Vendor/MSFT/Policy/Result"

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 \[僅限桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                      |
| 命名空間<br/>                | 根 \\ CIMv2 \\ MDM \\ DMMap<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[使用 PowerShell 指令碼搭配 WMI 橋接器提供者](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

