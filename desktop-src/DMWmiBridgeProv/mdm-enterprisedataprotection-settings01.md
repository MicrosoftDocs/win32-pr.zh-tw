---
title: MDM_EnterpriseDataProtection_Settings01 類別
description: MDM \_ EnterpriseDataProtection \_ Settings01 類別可用來設定 Windows 資訊保護 (WIP)  (先前稱為 Enterprise 資料保護) 特定設定。
ms.assetid: 7537f548-85fb-46b4-ab94-c9dcf2bf1447
keywords:
- MDM_EnterpriseDataProtection_Settings01 類別
- MDM_EnterpriseDataProtection_Settings01 類別，描述
topic_type:
- apiref
api_name:
- MDM_EnterpriseDataProtection_Settings01
- MDM_EnterpriseDataProtection_Settings01.InstanceID
- MDM_EnterpriseDataProtection_Settings01.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e80502ff724a43f1034922b0734fe128124c193f0ef5319ee2976257d26fbe3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118165831"
---
# <a name="mdm_enterprisedataprotection_settings01-class"></a>MDM \_ EnterpriseDataProtection \_ Settings01 類別

\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。 Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]

**MDM \_ EnterpriseDataProtection \_ Settings01** 類別可用來設定 Windows 資訊保護 (WIP)  (先前稱為 Enterprise 資料保護) 特定設定。 如需有關 WIP 的詳細資訊，請參閱 [使用企業資料保護來保護您的企業資料 (EDP) ](/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip)。

下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_EnterpriseDataProtection_Settings01
{
  string InstanceID;
  string ParentID;
  sint32 EDPEnforcementLevel;
  string EnterpriseProtectedDomainNames;
  sint32 AllowUserDecryption;
  string DataRecoveryCertificate;
  sint32 RevokeOnUnenroll;
  string SMBAutoEncryptedFileExtensions;
  sint32 AllowAzureRMSForEDP;
  string RMSTemplateIDForEDP;
  sint32 EDPShowIcons;
};
```

## <a name="members"></a>成員

**MDM \_ EnterpriseDataProtection \_ Settings01** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**MDM \_ EnterpriseDataProtection \_ Settings01** 類別具有這些屬性。

<dl> <dt>

[AllowAzureRMSForEDP](/windows/client-management/mdm/enterprisedataprotection-csp#settings-allowazurermsforedp)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[AllowUserDecryption](/windows/client-management/mdm/enterprisedataprotection-csp#settings-allowuserdecryption)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[DataRecoveryCertificate](/windows/client-management/mdm/enterprisedataprotection-csp#settings-datarecoverycertificate)
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： **Octetstring**
</dt> </dl>

</dd> <dt>

[EDPEnforcementLevel](/windows/client-management/mdm/enterprisedataprotection-csp#settings-edpenforcementlevel)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[EDPShowIcons](/windows/client-management/mdm/enterprisedataprotection-csp#settings-edpshowicons)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[EnterpriseProtectedDomainNames](/windows/client-management/mdm/enterprisedataprotection-csp#settings-enterpriseprotecteddomainnames)
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

識別父節點的名稱。 此類別的字串為 "設定"。

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

描述父節點的完整路徑。 此類別的字串為 "./Vendor/MSFT/EnterpriseDataProtection"

</dd> <dt>

[RevokeOnUnenroll](/windows/client-management/mdm/enterprisedataprotection-csp#settings-revokeonunenroll)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[RMSTemplateIDForEDP](/windows/client-management/mdm/enterprisedataprotection-csp#settings-rmstemplateidforedp)
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[SMBAutoEncryptedFileExtensions](/windows/client-management/mdm/enterprisedataprotection-csp#settings-smbautoencryptedfileextensions)
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 \[僅限桌面應用程式\]<br/>                                                          |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                            |
| 命名空間<br/>                | 根 \\ cimv2 \\ mdm \\ dmmap<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv1 mof</dt> </dl>      |
| DLL<br/>                      | <dl> <dt>Mof \\DMWmiBridgeProv.dll</dt> </dl> |



 

