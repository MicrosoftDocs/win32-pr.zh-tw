---
title: MDM_DeviceStatus_Battery01 類別
description: '\_ \_ 企業使用 MDM DeviceStatus Battery01 類別，以其企業原則查詢裝置的電池合規性狀態。'
ms.assetid: f4e92e2a-e267-467a-9905-2539dcaf8d8c
keywords:
- MDM_DeviceStatus_Battery01 類別
- MDM_DeviceStatus_Battery01 類別，描述
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_Battery01
- MDM_DeviceStatus_Battery01.InstanceID
- MDM_DeviceStatus_Battery01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51c637ce68aba89de1d43cf967fbfff3a80d07842dbb268c3f93df641a924f9b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119216398"
---
# <a name="mdm_devicestatus_battery01-class"></a>MDM \_ DeviceStatus \_ Battery01 類別

\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。 Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]

企業使用 **MDM \_ DeviceStatus \_ Battery01** 類別，以其企業原則查詢裝置的電池合規性狀態。

下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_Battery01
{
  string InstanceID;
  string ParentID;
  sint32 Status;
  sint32 EstimatedChargeRemaining;
  sint32 EstimatedRuntime;
};
```

## <a name="members"></a>成員

**MDM \_ DeviceStatus \_ Battery01** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**MDM \_ DeviceStatus \_ Battery01** 類別具有這些屬性。

<dl> <dt>

[EstimatedChargeRemaining](/windows/client-management/mdm/devicestatus-csp#devicestatus-battery-estimatedchargeremaining)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[EstimatedRuntime](/windows/client-management/mdm/devicestatus-csp#devicestatus-battery-estimatedruntime)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
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

電池查詢的節點。

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

描述父節點的完整路徑。 此類別的字串為 "./Vendor/MSFT/DeviceStatus"

</dd> <dt>

[狀態](/windows/client-management/mdm/devicestatus-csp#devicestatus-battery-status)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
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



 

