---
title: MDM_Policy_Result01_Power02 類別
description: MDM \_ Policy \_ Result01 \_ Power02 類別代表電源原則。
ms.assetid: 1458228f-f442-4fd4-b402-e0a4c06ecaa5
keywords:
- MDM_Policy_Result01_Power02 類別
- MDM_Policy_Result01_Power02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Power02
- MDM_Policy_Result01_Power02.InstanceID
- MDM_Policy_Result01_Power02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1e0fcebabd0d95ba4b120e02f3b871e5a2deae1a188e439b8bc396ed7add534
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084888"
---
# <a name="mdm_policy_result01_power02-class"></a>MDM \_ 原則 \_ Result01 \_ Power02 類別

\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。 Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]

MDM \_ Policy \_ Result01 \_ Power02 類別代表電源原則。

下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Power02
{
  string InstanceID;
  string ParentID;
  string AllowStandbyWhenSleepingPluggedIn;
  string HibernateTimeoutPluggedIn;
  string HibernateTimeoutOnBattery;
  string DisplayOffTimeoutPluggedIn;
  string DisplayOffTimeoutOnBattery;
  string RequirePasswordWhenComputerWakesOnBattery;
  string RequirePasswordWhenComputerWakesPluggedIn;
  string StandbyTimeoutPluggedIn;
  string StandbyTimeoutOnBattery;
};
```

## <a name="members"></a>成員

**MDM \_ Policy \_ Result01 \_ Power02** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**MDM \_ Policy \_ Result01 \_ Power02** 類別具有這些屬性。

<dl> <dt>

[AllowStandbyWhenSleepingPluggedIn](/windows/client-management/mdm/policy-csp-power#power-allowstandbywhensleepingpluggedin)
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[DisplayOffTimeoutOnBattery](/windows/client-management/mdm/policy-csp-power#power-displayofftimeoutonbattery)
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[DisplayOffTimeoutPluggedIn](/windows/client-management/mdm/policy-csp-power#power-displayofftimeoutpluggedin)
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[HibernateTimeoutOnBattery](/windows/client-management/mdm/policy-csp-power#power-hibernatetimeoutonbattery)
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[HibernateTimeoutPluggedIn](/windows/client-management/mdm/policy-csp-power#power-hibernatetimeoutpluggedin)
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

**ParentID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

</dd> <dt>

[RequirePasswordWhenComputerWakesOnBattery](/windows/client-management/mdm/policy-csp-power#power-requirepasswordwhencomputerwakesonbattery)
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[RequirePasswordWhenComputerWakesPluggedIn](/windows/client-management/mdm/policy-csp-power#power-requirepasswordwhencomputerwakespluggedin)
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[StandbyTimeoutOnBattery](/windows/client-management/mdm/policy-csp-power#power-standbytimeoutonbattery)
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[StandbyTimeoutPluggedIn](/windows/client-management/mdm/policy-csp-power#power-standbytimeoutpluggedin)
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



 

