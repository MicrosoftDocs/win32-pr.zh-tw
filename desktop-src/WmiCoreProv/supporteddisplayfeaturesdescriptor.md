---
description: 代表受支援的監視器顯示功能。
ms.assetid: 28eeead3-8fb9-4720-8d93-1c6757dfb31b
title: SupportedDisplayFeaturesDescriptor 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SupportedDisplayFeaturesDescriptor
- SupportedDisplayFeaturesDescriptor.ActiveOffSupported
- SupportedDisplayFeaturesDescriptor.DisplayType
- SupportedDisplayFeaturesDescriptor.GTFSupported
- SupportedDisplayFeaturesDescriptor.HasPreferredTimingMode
- SupportedDisplayFeaturesDescriptor.sRGBSupported
- SupportedDisplayFeaturesDescriptor.StandbySupported
- SupportedDisplayFeaturesDescriptor.SuspendSupported
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 30350d477533b7e51ba8b3130c5a24d81c12f10e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106978836"
---
# <a name="supporteddisplayfeaturesdescriptor-class"></a>SupportedDisplayFeaturesDescriptor 類別

**SupportedDisplayFeaturesDescriptor** 代表受支援的監視器顯示功能。 此類別中的資訊會對應至視頻電子產品標準關聯的影片輸入定義中的資料 (VESA) 增強的擴充顯示器識別資料 (E-EDID) 標準。

## <a name="syntax"></a>語法

``` syntax
class SupportedDisplayFeaturesDescriptor
{
  boolean ActiveOffSupported;
  uint8   DisplayType;
  boolean GTFSupported;
  boolean HasPreferredTimingMode;
  boolean sRGBSupported;
  boolean StandbySupported;
  boolean SuspendSupported;
};
```

## <a name="members"></a>成員

**SupportedDisplayFeaturesDescriptor** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**SupportedDisplayFeaturesDescriptor** 類別具有這些屬性。

<dl> <dt>

**ActiveOffSupported**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

支援主動式電源和非常低的耗電量。 當顯示器收到的計時信號超出宣告的作用中作業範圍時，就會耗用較少的電源。 如果計時信號回到正常的作業範圍，則顯示會還原為一般作業。 一般作業範圍外的計時信號範例不是任何同步信號，也不會有任何取消信號。

</dd> <dt>

**DisplayType**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

監視器的顯示類型。 下表列出可能的值。



| 值                                                                              | 意義                                 |
|------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>0 (0x0) </dt> </dl> | 單色/灰階顯示<br/> |
| <dl> <dt>1 (0x1) </dt> </dl> | RGB 色彩顯示<br/>            |
| <dl> <dt>2 (0x2) </dt> </dl> | 非 RGB 多色顯示<br/>   |



 

</dd> <dt>

**GTFSupported**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出顯示器是否具有 GTF 支援。 若 **為 True**，則顯示使用預設 GTF 參數值，以 GTF 標準為基礎來支援計時。

</dd> <dt>

**HasPreferredTimingMode**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出顯示器是否有慣用的時間模式。 若 **為 True**，則第一個詳細計時區塊包含監視的慣用計時模式。 使用慣用的時間模式是 EDID v1.0 和更新版本的必要項。

</dd> <dt>

**sRGBSupported**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

若 **為 True**，則顯示支援 sRGB。

</dd> <dt>

**StandbySupported**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出顯示器是否支援 VESA 顯示器電源管理信號 (DPMS) 待命。 若 **為 True**，則支援 DPMS 待命。

</dd> <dt>

**SuspendSupported**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出顯示器是否支援 VESA 顯示器電源管理信號 (DPMS) 暫停。 若 **為 True**，則支援 DPMS 暫止。

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

 

 




