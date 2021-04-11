---
description: 代表電腦監視器的類比影片輸入參數。
ms.assetid: 87d4260d-06c7-4a76-a3a1-8f6e51e23d92
title: WmiMonitorAnalogVideoInputParams 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorAnalogVideoInputParams
- WmiMonitorAnalogVideoInputParams.Active
- WmiMonitorAnalogVideoInputParams.CompositeSyncSupported
- WmiMonitorAnalogVideoInputParams.InstanceName
- WmiMonitorAnalogVideoInputParams.SeparateSyncsSupported
- WmiMonitorAnalogVideoInputParams.SerrationOfVsyncRequired
- WmiMonitorAnalogVideoInputParams.SetupExpected
- WmiMonitorAnalogVideoInputParams.SignalLevelStandard
- WmiMonitorAnalogVideoInputParams.SyncOnGreenVideoSupported
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 900bf4353de0c81acb5aa2c69578256b0212a2c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944596"
---
# <a name="wmimonitoranalogvideoinputparams-class"></a>WmiMonitorAnalogVideoInputParams 類別

**WmiMonitorAnalogVideoInputParams** WMI 類別代表電腦監視器的類比影片輸入參數。 此類別中的資料會對應至視頻電子郵件標準關聯的影片輸入定義中的資料 (VESA) 增強的擴充顯示器識別資料 (E-EDID) 標準。 只有當 [**WmiMonitorBasicDisplayParams**](wmimonitorbasicdisplayparams.md)類別的 **VideoInputType** 屬性值為 "類比" 時，才能使用這個類別的實例。

## <a name="syntax"></a>語法

``` syntax
class WmiMonitorAnalogVideoInputParams : MSMonitorClass
{
  boolean Active;
  uint8   CompositeSyncSupported;
  string  InstanceName;
  uint8   SeparateSyncsSupported;
  uint8   SerrationOfVsyncRequired;
  uint8   SetupExpected;
  uint8   SignalLevelStandard;
  uint8   SyncOnGreenVideoSupported;
};
```

## <a name="members"></a>成員

**WmiMonitorAnalogVideoInputParams** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**WmiMonitorAnalogVideoInputParams** 類別具有這些屬性。

<dl> <dt>

**使用中**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

表示使用中的監視器。

</dd> <dt>

**CompositeSyncSupported**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出是否支援複合同步處理。



| 值                                                                              | 意義                                                             |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>0 (0x0) </dt> </dl> | 支援水準同步處理線上的複合同步處理。<br/>     |
| <dl> <dt>1 (0x1) </dt> </dl> | 不支援水準同步處理行上的複合同步處理。<br/> |



 

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

**SeparateSyncsSupported**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出是否支援個別同步處理。



| 值                                                                              | 意義                                      |
|------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>0 (0x0) </dt> </dl> | 支援不同的同步處理。<br/>     |
| <dl> <dt>1 (0x1) </dt> </dl> | 不支援個別的同步處理。<br/> |



 

</dd> <dt>

**SerrationOfVsyncRequired**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出是否需要垂直同步脈衝 serration。



| 值                                                                              | 意義                                                                                                             |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0 (0x0) </dt> </dl> | 使用複合同步處理或同步處理-綠色影片時，需要垂直同步脈衝的 Serration。<br/>     |
| <dl> <dt>1 (0x1) </dt> </dl> | 使用複合同步處理或「同步-開啟」影片時，不需要 Serration 垂直同步脈衝。<br/> |



 

</dd> <dt>

**SetupExpected**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出是否預期安裝程式。



| 值                                                                              | 意義                                                                                                                   |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0 (0x0) </dt> </dl> | 監視器預期每個適當的信號等級標準會有空白到空白的設定或基座。<br/>                      |
| <dl> <dt>1 (0x1) </dt> </dl> | 根據適當的信號等級標準，監視不會預期會有空白到空白的設定或基座。<br/> |



 

</dd> <dt>

**SignalLevelStandard**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

增強型視頻連接器的信號等級標準 (的 EVC) 連接。



| 值                                                                              | 意義                     |
|------------------------------------------------------------------------------------|-----------------------------|
| <dl> <dt>0 (0x0) </dt> </dl> | 0.7，0.3 \[ V\]<br/>     |
| <dl> <dt>1 (0x1) </dt> </dl> | 0.714，0.286 \[ V\]<br/> |
| <dl> <dt>2 (0x2) </dt> </dl> | 1.0、0.4 \[ V\]<br/>     |
| <dl> <dt>3 (0x3) </dt> </dl> | 0.7、0.0 \[ V\]<br/>     |



 

</dd> <dt>

**SyncOnGreenVideoSupported**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出是否支援在綠色上進行同步處理。



| 值                                                                              | 意義                                          |
|------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>0 (0x0) </dt> </dl> | 支援在綠色影片上進行同步處理。<br/>     |
| <dl> <dt>1 (0x1) </dt> </dl> | 不支援在綠色影片上進行同步處理。<br/> |



 

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

 

 




