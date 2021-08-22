---
description: 目的電腦轉送資料變更的最近歷程記錄。
ms.assetid: 621e2734-fc75-4e7a-9fae-de3d1b0272ae
ms.tgt_platform: multiple
title: TargetForwardingHistory 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TargetForwardingHistory
- TargetForwardingHistory.TargetEndpoint
- TargetForwardingHistory.TargetMac
- TargetForwardingHistory.TargetGuid
- TargetForwardingHistory.CollectorEndpoint
- TargetForwardingHistory.Computer
- TargetForwardingHistory.ForwarderType
- TargetForwardingHistory.Destination
- TargetForwardingHistory.DestinationPattern
- TargetForwardingHistory.Error
- TargetForwardingHistory.ConnectedSince
- TargetForwardingHistory.DisconnectedSince
- TargetForwardingHistory.WmiDateTime
api_type:
- DllExport
api_location:
- BEvtCol.exe
ms.openlocfilehash: a58168995adf81f01d20486bcb7ceeef85b9424b2034da98ef628e098a674f39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529638"
---
# <a name="targetforwardinghistory-class"></a>TargetForwardingHistory 類別

目的電腦轉送資料變更的最近歷程記錄。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Provider("BootEventCollectorWmiProvider"), Dynamic, AMENDMENT]
class TargetForwardingHistory
{
  string   TargetEndpoint;
  string   TargetMac;
  string   TargetGuid;
  string   CollectorEndpoint;
  string   Computer;
  string   ForwarderType;
  string   Destination;
  string   DestinationPattern;
  string   Error;
  DATETIME ConnectedSince;
  DATETIME DisconnectedSince;
  DATETIME WmiDateTime;
};
```

## <a name="members"></a>成員

**TargetForwardingHistory** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**TargetForwardingHistory** 類別具有這些屬性。

<dl> <dt>

**CollectorEndpoint**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**修正**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

收集器伺服器的端點資訊。 這個屬性會格式化為 *主機*：*埠* 字串。

</dd> <dt>

**電腦**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**修正**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

目的電腦的電腦名稱稱。

</dd> <dt>

**ConnectedSince**
</dt> <dd> <dl> <dt>

資料類型： **DATETIME**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**修正**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

時間戳記，指出為轉送資料建立連接的時間。

</dd> <dt>

**目的地**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**修正**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

轉送資料的目的地，例如檔案名。

</dd> <dt>

**DestinationPattern**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**修正**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

用來產生轉送資料目的地的格式。

</dd> <dt>

**DisconnectedSince**
</dt> <dd> <dl> <dt>

資料類型： **DATETIME**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**修正**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

指出連接中斷連接的時間戳記。

</dd> <dt>

**錯誤**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**修正**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

描述發生錯誤的錯誤訊息。 如果未發生任何錯誤，此屬性是空的。

</dd> <dt>

**ForwarderType**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**修正**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

包含轉送資料（例如 ETL）的檔案類型。

</dd> <dt>

**TargetEndpoint**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)， [**固定**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

目的電腦的端點資訊，以人類看得懂的格式。 這個屬性會格式化為 *主機*：*埠* 字串。 例如，"127.0.0.1： 50000"。

</dd> <dt>

**TargetGuid**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)， [**固定**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

目的電腦的 SMBIOS **GUID** 。

</dd> <dt>

**TargetMac**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)， [**固定**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

目的電腦的 MAC 位址。

</dd> <dt>

**WmiDateTime**
</dt> <dd> <dl> <dt>

資料類型： **DATETIME**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**修正**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

記錄此狀態變更的時間戳記。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                            |
| 最低支援的伺服器<br/> | Windows Server 2016<br/>                                                                       |
| 命名空間<br/>                | 根 \\ Microsoft \\ Windows \\ BootEventCollector<br/>                                              |
| MOF<br/>                      | <dl> <dt>BootEventCollectorWMI mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[開機事件收集器 WMI 提供者](boot-event-collector-wmi-provider-portal.md)
</dt> </dl>

 

