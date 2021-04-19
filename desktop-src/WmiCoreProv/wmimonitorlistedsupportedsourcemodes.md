---
description: 列出監視器描述項中影片監視器支援的來源模式（如果有的話）。
ms.assetid: cca59d28-bd93-4df2-989e-0516dd8eae83
title: WmiMonitorListedSupportedSourceModes 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorListedSupportedSourceModes
- WmiMonitorListedSupportedSourceModes.Active
- WmiMonitorListedSupportedSourceModes.InstanceName
- WmiMonitorListedSupportedSourceModes.NumOfMonitorSourceModes
- WmiMonitorListedSupportedSourceModes.PreferredMonitorSourceModeIndex
- WmiMonitorListedSupportedSourceModes.MonitorSourceModes
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 35cb4b3548654c72686a8843cc697f109f661d87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988265"
---
# <a name="wmimonitorlistedsupportedsourcemodes-class"></a>WmiMonitorListedSupportedSourceModes 類別

**WmiMonitorListedSupportedSourceModes** 會在其監視描述項中列出影片監視器支援的來源模式（如果有的話）。 針對沒有描述的監視器，此模式清單會根據監視器匯流排驅動程式所指定的監視器類型來產生。

## <a name="syntax"></a>語法

``` syntax
class WmiMonitorListedSupportedSourceModes : MSMonitorClass
{
  boolean             Active;
  string              InstanceName;
  uint16              NumOfMonitorSourceModes;
  uint16              PreferredMonitorSourceModeIndex;
  VideoModeDescriptor MonitorSourceModes[];
};
```

## <a name="members"></a>成員

**WmiMonitorListedSupportedSourceModes** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**WmiMonitorListedSupportedSourceModes** 類別具有這些屬性。

<dl> <dt>

**使用中**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

表示使用中的監視器。

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 **鍵**
</dt> </dl>

特定監視實例的名稱。

</dd> <dt>

**MonitorSourceModes**
</dt> <dd> <dl> <dt>

資料類型： **VideoModeDescriptor** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

列出 [**VideoModeDescriptor**](videomodedescriptor.md) 類別的實例所代表的監視器來源模式。

</dd> <dt>

**NumOfMonitorSourceModes**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

所列支援的監視器來源模式數目。

</dd> <dt>

**PreferredMonitorSourceModeIndex**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

慣用的監視器來源模式索引。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                               |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                         |
| 命名空間<br/>                | 根 \\ wmi<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WmiCore mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> </dl>

 

 




