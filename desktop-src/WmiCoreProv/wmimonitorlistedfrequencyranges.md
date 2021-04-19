---
description: 列出監視器所支援的頻率範圍。
ms.assetid: e4713650-5f8c-4808-8b4f-1d29c54ab4e3
title: WmiMonitorListedFrequencyRanges 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorListedFrequencyRanges
- WmiMonitorListedFrequencyRanges.Active
- WmiMonitorListedFrequencyRanges.InstanceName
- WmiMonitorListedFrequencyRanges.NumOfMonitorFreqRanges
- WmiMonitorListedFrequencyRanges.MonitorFreqRanges
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: e13828f6d5e844147fc0b041617c8452c503ceef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106976967"
---
# <a name="wmimonitorlistedfrequencyranges-class"></a>WmiMonitorListedFrequencyRanges 類別

**WmiMonitorListedFrequencyRanges** WMI 類別會列出監視器所支援的頻率範圍。 您可以在視頻電子郵件標準關聯的影片輸入定義中找到這些範圍 (VESA) 增強的擴充顯示器識別資料 (E EDID) 區塊，或包含設備磁碟機資料的 Windows INF 檔案中。

## <a name="syntax"></a>語法

``` syntax
class WmiMonitorListedFrequencyRanges : MSMonitorClass
{
  boolean                  Active;
  string                   InstanceName;
  uint16                   NumOfMonitorFreqRanges;
  FrequencyRangeDescriptor MonitorFreqRanges[];
};
```

## <a name="members"></a>成員

**WmiMonitorListedFrequencyRanges** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**WmiMonitorListedFrequencyRanges** 類別具有這些屬性。

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

**MonitorFreqRanges**
</dt> <dd> <dl> <dt>

資料類型： **FrequencyRangeDescriptor** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

由 [**FrequencyRangeDescriptor**](frequencyrangedescriptor.md) 類別的實例所表示的監視器頻率範圍清單。

</dd> <dt>

**NumOfMonitorFreqRanges**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

所列支援的監視器頻率範圍數目。

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

 

 




