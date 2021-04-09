---
title: MDM_Policy_Config01_Kerberos02 類別
description: MDM \_ Policy \_ Config01 Kerberos02 類別會設定 \_ Kerberos 原則。
ms.assetid: d34ccc8a-0c0c-4b7a-88c2-35360ebd0b8e
keywords:
- MDM_Policy_Config01_Kerberos02 類別
- MDM_Policy_Config01_Kerberos02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Kerberos02
- MDM_Policy_Config01_Kerberos02.InstanceID
- MDM_Policy_Config01_Kerberos02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c173c892985487ed1ac061ea720e3485ecb355ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843555"
---
# <a name="mdm_policy_config01_kerberos02-class"></a>MDM \_ 原則 \_ Config01 \_ Kerberos02 類別

\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。 Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]

MDM \_ Policy \_ Config01 Kerberos02 類別會設定 \_ Kerberos 原則。

下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Kerberos02
{
  string InstanceID;
  string ParentID;
  string AllowForestSearchOrder;
  string KerberosClientSupportsClaimsCompoundArmor;
  string RequireKerberosArmoring;
  string RequireStrictKDCValidation;
  string SetMaximumContextTokenSize;
};
```

## <a name="members"></a>成員

**MDM \_ Policy \_ Config01 \_ Kerberos02** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**MDM \_ Policy \_ Config01 \_ Kerberos02** 類別具有這些屬性。

<dl> <dt>

[AllowForestSearchOrder](/windows/client-management/mdm/policy-csp-kerberos#kerberos-allowforestsearchorder)
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

</dd> <dt>

[KerberosClientSupportsClaimsCompoundArmor](/windows/client-management/mdm/policy-csp-kerberos#kerberos-kerberosclientsupportsclaimscompoundarmor)
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

</dd> <dt>

[RequireKerberosArmoring](/windows/client-management/mdm/policy-csp-kerberos#kerberos-requirekerberosarmoring)
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[RequireStrictKDCValidation](/windows/client-management/mdm/policy-csp-kerberos#kerberos-requirestrictkdcvalidation)
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[SetMaximumCoNtextTokenSize](/windows/client-management/mdm/policy-csp-kerberos#kerberos-setmaximumcontexttokensize)
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 10 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                      |
| 命名空間<br/>                | 根 \\ cimv2 \\ mdm \\ dmmap<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



 

