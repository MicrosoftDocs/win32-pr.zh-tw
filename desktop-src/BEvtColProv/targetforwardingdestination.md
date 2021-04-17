---
description: 包含所收集資料的已知目的地。 只有在收集器在啟用狀態記錄檔的情況下才可使用。
ms.assetid: ab0d2949-9808-49c3-8a0c-f2ce9c300a2a
ms.tgt_platform: multiple
title: TargetForwardingDestination 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TargetForwardingDestination
- TargetForwardingDestination.TargetEndpoint
- TargetForwardingDestination.TargetMac
- TargetForwardingDestination.TargetGuid
- TargetForwardingDestination.CollectorEndpoint
- TargetForwardingDestination.Computer
- TargetForwardingDestination.ForwarderType
- TargetForwardingDestination.Destination
- TargetForwardingDestination.DestinationPattern
- TargetForwardingDestination.Error
- TargetForwardingDestination.ConnectedSince
- TargetForwardingDestination.DisconnectedSince
- TargetForwardingDestination.WmiDateTime
api_type:
- DllExport
api_location:
- BEvtCol.exe
ms.openlocfilehash: 735b6179fe9d72b5faf0cad976410aeace427f63
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104467984"
---
# <a name="targetforwardingdestination-class"></a>TargetForwardingDestination 類別

包含所收集資料的已知目的地。 只有在收集器在啟用狀態記錄檔的情況下才可使用。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Provider("BootEventCollectorWmiProvider"), Dynamic, AMENDMENT]
class TargetForwardingDestination
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

**TargetForwardingDestination** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**TargetForwardingDestination** 類別具有這些屬性。

<dl> <dt>

**CollectorEndpoint**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**修正**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

主機：收集端上端點的埠資訊。

</dd> <dt>

**電腦**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**修正**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

依收集器根據其設定決定的目標電腦名稱稱。

</dd> <dt>

**ConnectedSince**
</dt> <dd> <dl> <dt>

資料類型： **DATETIME**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**修正**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

建立連接的時間戳記。

</dd> <dt>

**目的地**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)， [**固定**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

資料的目的地。 意義取決於轉寄站類型。 可以是檔案名或其他識別碼。

</dd> <dt>

**DestinationPattern**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**修正**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

用來產生資料目的地的模式。 意義取決於轉寄站類型和設定。 若為固定目的地，就會與目的地本身相同。 如果目的地的檔案有旋轉，則會包含將取代為目的地中實際索引的模式字元。

</dd> <dt>

**DisconnectedSince**
</dt> <dd> <dl> <dt>

資料類型： **DATETIME**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**修正**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

中斷連接時的時間戳記。

</dd> <dt>

**錯誤**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**修正**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

如果發生錯誤，則為錯誤訊息。 否則將會是空的。

</dd> <dt>

**ForwarderType**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)， [**固定**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

轉寄站的類型 (例如 ' etl ' ) 。

</dd> <dt>

**TargetEndpoint**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**修正**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

目的電腦的端點資訊，以人類看得懂的格式。 這個屬性會格式化為 *主機*：*埠* 字串。 例如，"127.0.0.1： 50000"。

</dd> <dt>

**TargetGuid**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**修正**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

目的電腦的 SMBIOS GUID (已知的) 。

</dd> <dt>

**TargetMac**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**修正**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

目的電腦的 MAC 位址 (已知的) 。

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



 

