---
title: MDM_WindowsAdvancedThreatProtection_HealthState01 類別
description: MDM \_ WindowsAdvancedThreatProtection \_ HealthState01 類別用來判斷 Windows Defender Advanced 威脅防護 (WDATP) 端點的健全狀況狀態。
ms.assetid: 8d630b95-9895-4cb8-99f2-8f869c4dfd18
keywords:
- MDM_WindowsAdvancedThreatProtection_HealthState01 類別
- MDM_WindowsAdvancedThreatProtection_HealthState01 類別，描述
topic_type:
- apiref
api_name:
- MDM_WindowsAdvancedThreatProtection_HealthState01
- MDM_WindowsAdvancedThreatProtection_HealthState01.InstanceID
- MDM_WindowsAdvancedThreatProtection_HealthState01.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5519b731cf54a633a659ec865e7a1f0e12deda75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934765"
---
# <a name="mdm_windowsadvancedthreatprotection_healthstate01-class"></a>MDM \_ WindowsAdvancedThreatProtection \_ HealthState01 類別

\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。 Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]

**MDM \_ WindowsAdvancedThreatProtection \_ HealthState01** 類別用來判斷 Windows Defender ADVANCED 威脅防護 (WDATP) 端點的健全狀況狀態。

下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_WindowsAdvancedThreatProtection_HealthState01
{
  string   InstanceID;
  string   ParentID;
  datetime LastConnected;
  boolean  SenseIsRunning;
  sint32   OnboardingState;
  string   OrgId;
};
```

## <a name="members"></a>成員

**MDM \_ WindowsAdvancedThreatProtection \_ HealthState01** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**MDM \_ WindowsAdvancedThreatProtection \_ HealthState01** 類別具有這些屬性。

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

識別父節點的名稱。 此類別的字串為 "HealthState"。

</dd> <dt>

[LastConnected](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#healthstate-lastconnected)
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[OnboardingState](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#healthstate-onboardingstate)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[OrgId](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#healthstate-orgid)
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

描述父節點的完整路徑。 此類別的字串為 "./Vendor/MSFT/WindowsAdvancedThreatProtection"

</dd> <dt>

[SenseIsRunning](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#healthstate-senseisrunning)
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 10 桌面應用程式\]<br/>                                                          |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                            |
| 命名空間<br/>                | 根 \\ cimv2 \\ mdm \\ dmmap<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv1 mof</dt> </dl>      |
| DLL<br/>                      | <dl> <dt>Mof \\DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[使用 PowerShell 指令碼搭配 WMI 橋接器提供者](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

