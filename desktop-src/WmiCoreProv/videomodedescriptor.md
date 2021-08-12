---
description: 包含 WmiMonitorListedSupportedSourceModes 類別中 MonitorSourceModes 陣列的模式描述項元素。
ms.assetid: 6d6c846d-caec-41a8-8a88-1c1e14bc0473
title: VideoModeDescriptor 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- VideoModeDescriptor
- VideoModeDescriptor.CompositePolarityType
- VideoModeDescriptor.HorizontalActivePixels
- VideoModeDescriptor.HorizontalBlankingPixels
- VideoModeDescriptor.HorizontalBorder
- VideoModeDescriptor.HorizontalImageSize
- VideoModeDescriptor.HorizontalPolarityType
- VideoModeDescriptor.HorizontalRefreshRateDenominator
- VideoModeDescriptor.HorizontalRefreshRateNumerator
- VideoModeDescriptor.HorizontalSyncOffset
- VideoModeDescriptor.HorizontalSyncPulseWidth
- VideoModeDescriptor.IsInterlaced
- VideoModeDescriptor.IsSerrationRequired
- VideoModeDescriptor.IsSyncOnRGB
- VideoModeDescriptor.PixelClockRate
- VideoModeDescriptor.StereoModeType
- VideoModeDescriptor.SyncSignalType
- VideoModeDescriptor.VerticalActivePixels
- VideoModeDescriptor.VerticalBlankingPixels
- VideoModeDescriptor.VerticalBorder
- VideoModeDescriptor.VerticalImageSize
- VideoModeDescriptor.VerticalRefreshRateDenominator
- VideoModeDescriptor.VerticalRefreshRateNumerator
- VideoModeDescriptor.VerticalSyncOffset
- VideoModeDescriptor.VerticalPolarityType
- VideoModeDescriptor.VerticalSyncPulseWidth
- VideoModeDescriptor.VideoStandardType
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: a8f103bf5a23f6e157fc9ecca697c0d1ce7c47bd71be20458d816ca74819dc10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118558403"
---
# <a name="videomodedescriptor-class"></a>VideoModeDescriptor 類別

**VideoModeDescriptorVideo** WMI 類別包含 [**WmiMonitorListedSupportedSourceModes**](wmimonitorlistedsupportedsourcemodes.md)類別中 **MonitorSourceModes** 陣列的模式描述項元素。 這些元素包括監視功能，例如重新整理速率、圖元特性或影像大小。 **VideoModeDescriptorVideo** 類別包含的資訊，是已建立、標準和詳細計時區塊可用之資料的超集合。

## <a name="syntax"></a>語法

``` syntax
class VideoModeDescriptor : WmiMonitorSupportedVideoModes
{
  uint8   CompositePolarityType;
  uint16  HorizontalActivePixels;
  uint16  HorizontalBlankingPixels;
  uint16  HorizontalBorder;
  uint16  HorizontalImageSize;
  uint8   HorizontalPolarityType;
  uint16  HorizontalRefreshRateDenominator;
  uint16  HorizontalRefreshRateNumerator;
  uint16  HorizontalSyncOffset;
  uint16  HorizontalSyncPulseWidth;
  boolean IsInterlaced;
  uint8   IsSerrationRequired;
  uint8   IsSyncOnRGB;
  uint32  PixelClockRate;
  uint8   StereoModeType;
  uint8   SyncSignalType;
  uint16  VerticalActivePixels;
  uint16  VerticalBlankingPixels;
  uint16  VerticalBorder;
  uint16  VerticalImageSize;
  uint16  VerticalRefreshRateDenominator;
  uint16  VerticalRefreshRateNumerator;
  uint16  VerticalSyncOffset;
  uint8   VerticalPolarityType;
  uint16  VerticalSyncPulseWidth;
  uint8   VideoStandardType;
};
```

## <a name="members"></a>成員

**VideoModeDescriptor** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**VideoModeDescriptor** 類別具有這些屬性。

<dl> <dt>

**CompositePolarityType**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

複合極性類型。 這是在垂直同步之外的水準同步跳動的極性。



| 值                                                                              | 意義                                                                    |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>0 (0x0) </dt> </dl> | 複合極性是正面的。<br/>                                 |
| <dl> <dt>1 (0x1) </dt> </dl> | 複合極性為負數。<br/>                                 |
| <dl> <dt>2 (0x2) </dt> </dl> | 不適用。 信號同步類型必須是數位複合。<br/> |



 

</dd> <dt>

**HorizontalActivePixels**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

水準作用中圖元的數目。

</dd> <dt>

**HorizontalBlankingPixels**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

水準消隱圖元的數目

</dd> <dt>

**HorizontalBorder**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

水準框線。

</dd> <dt>

**HorizontalImageSize**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

水準影像大小，以毫米 (mm) 。

</dd> <dt>

**HorizontalPolarityType**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

水準極性類型。



| 值                                                                              | 意義                                                                   |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>0 (0x0) </dt> </dl> | 水準極性是正面的。<br/>                               |
| <dl> <dt>1 (0x1) </dt> </dl> | 水準極性為負數。<br/>                               |
| <dl> <dt>2 (0x2) </dt> </dl> | 不適用。 信號同步類型必須是數位分開的。<br/> |



 

</dd> <dt>

**HorizontalRefreshRateDenominator**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

水準重新整理率分母。

</dd> <dt>

**HorizontalRefreshRateNumerator**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

以赫茲為單位的水準重新整理速率分子 (Hz) 。

</dd> <dt>

**HorizontalSyncOffset**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

水準同步位移。

</dd> <dt>

**HorizontalSyncPulseWidth**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

水準同步脈衝寬度。

</dd> <dt>

**IsInterlaced**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出顯示模式是否為交錯式。

</dd> <dt>

**IsSerrationRequired**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出需要何種類型的 serration （如果有的話）。



| 值                                                                              | 意義                                                                                                  |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <dl> <dt>0 (0x0) </dt> </dl> | 控制器應該在垂直同步期間提供水準同步處理。<br/>                                 |
| <dl> <dt>1 (0x1) </dt> </dl> | 控制器不應該在垂直同步期間提供水準同步處理。<br/>                             |
| <dl> <dt>2 (0x2) </dt> </dl> | 不適用。 信號同步類型必須是極性、類比複合或數位複合。<br/> |



 

</dd> <dt>

**IsSyncOnRGB**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出應該同步處理的視訊訊號行（如果有的話）。



| 值                                                                              | 意義                                                                           |
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <dt>0 (0x0) </dt> </dl> | 同步脈衝應該會出現在所有3個視訊訊號線上。<br/>                  |
| <dl> <dt>1 (0x1) </dt> </dl> | 同步脈衝應只出現在綠色的視訊訊號線上。<br/>          |
| <dl> <dt>2 (0x2) </dt> </dl> | 不適用。 信號同步類型必須是極性類比複合。<br/> |



 

</dd> <dt>

**PixelClockRate**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

以赫茲為單位的圖元頻率速率 (Hz) 。

</dd> <dt>

**StereoModeType**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

身歷聲模式類型。 下表列出可能的值。



| 值                                                                              | 意義                                                             |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>0 (0x0) </dt> </dl> | 沒有身歷聲。<br/>                                               |
| <dl> <dt>1 (0x1) </dt> </dl> | 在身歷聲同步上具有右影像的欄位順序身歷聲。<br/> |
| <dl> <dt>2 (0x2) </dt> </dl> | 具有左邊影像的欄位連續身歷聲（身歷聲同步）。<br/>  |
| <dl> <dt>3 (0x3) </dt> </dl> | 雙向交錯身歷聲，在偶數線條上有右影像。<br/> |
| <dl> <dt>4 (0x4) </dt> </dl> | 雙向交錯的身歷聲，在偶數行上具有左邊的影像。<br/>  |
| <dl> <dt>5 (0x5) </dt> </dl> | 4向交錯式身歷聲。<br/>                                |
| <dl> <dt>6 (0x6) </dt> </dl> | 並列交錯身歷聲。<br/>                         |



 

</dd> <dt>

**SyncSignalType**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

信號同步處理類型。 下表列出可能的值。



| 值                                                                              | 意義                             |
|------------------------------------------------------------------------------------|-------------------------------------|
| <dl> <dt>0 (0x0) </dt> </dl> | 類比複合<br/>         |
| <dl> <dt>1 (0x1) </dt> </dl> | 極性類比複合<br/> |
| <dl> <dt>2 (0x2) </dt> </dl> | 數位複合<br/>        |
| <dl> <dt>3 (0x3) </dt> </dl> | 數位分開<br/>         |



 

</dd> <dt>

**VerticalActivePixels**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

垂直現用圖元的數目。

</dd> <dt>

**VerticalBlankingPixels**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

垂直消隱圖元的數目。

</dd> <dt>

**VerticalBorder**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

垂直框線。

</dd> <dt>

**VerticalImageSize**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

垂直影像大小，以毫米 (mm) 。

</dd> <dt>

**VerticalPolarityType**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

垂直極性類型。



| 值                                                                              | 意義                                                                   |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>0 (0x0) </dt> </dl> | 垂直極性是正面的。<br/>                                 |
| <dl> <dt>1 (0x1) </dt> </dl> | 垂直極性為負數<br/>                                  |
| <dl> <dt>2 (0x2) </dt> </dl> | 不適用。 信號同步類型必須是數位分開的。<br/> |



 

</dd> <dt>

**VerticalRefreshRateDenominator**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

垂直重新整理率分母。

</dd> <dt>

**VerticalRefreshRateNumerator**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

以赫茲為單位的垂直重新整理率分子 (Hz) 。

</dd> <dt>

**VerticalSyncOffset**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

垂直同步位移。

</dd> <dt>

**VerticalSyncPulseWidth**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

垂直同步脈衝寬度。

</dd> <dt>

VideoStandardType
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

影片標準類型。



| 值                                                                                | 意義                                                                                                        |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0 (0x0) </dt> </dl>   | 其他<br/>                                                                                               |
| <dl> <dt>1 (0x1) </dt> </dl>   | VESA DMT。 從視頻電子產品標準關聯 (VESA) 顯示監視時間規格。<br/> |
| <dl> <dt>2 (0x2) </dt> </dl>   | VESA GTF。 從 VESA 一般化計時公式標準。<br/>                                            |
| <dl> <dt>3 (0x3) </dt> </dl>   | VESA CVT/來自 VESA 協調的影片計時標準。<br/>                                             |
| <dl> <dt>4 (0x4) </dt> </dl>   | IBM<br/>                                                                                                 |
| <dl> <dt>5 (0x5) </dt> </dl>   | 蘋果<br/>                                                                                               |
| <dl> <dt>6 (0x6) </dt> </dl>   | NTSC M<br/>                                                                                              |
| <dl> <dt>7 (0x7) </dt> </dl>   | NTSC J<br/>                                                                                              |
| <dl> <dt>8 (0x8) </dt> </dl>   | NTSC 433<br/>                                                                                            |
| <dl> <dt>9 (0x9) </dt> </dl>   | PAL B<br/>                                                                                               |
| <dl> <dt>10 (0xA) </dt> </dl>  | PAL B1<br/>                                                                                              |
| <dl> <dt>11 (0xB) </dt> </dl>  | PAL G<br/>                                                                                               |
| <dl> <dt>12 (0xC) </dt> </dl>  | PAL H<br/>                                                                                               |
| <dl> <dt>13 (0xD) </dt> </dl>  | PAL I<br/>                                                                                               |
| <dl> <dt>14 (0xE) </dt> </dl>  | PAL D<br/>                                                                                               |
| <dl> <dt>15 (0xF) </dt> </dl>  | PAL N<br/>                                                                                               |
| <dl> <dt>16 (0x10) </dt> </dl> | PAL NC<br/>                                                                                              |
| <dl> <dt>17 (0x11) </dt> </dl> | SECAM B<br/>                                                                                             |
| <dl> <dt>18 (0x12) </dt> </dl> | SECAM D<br/>                                                                                             |
| <dl> <dt>19 (0x13) </dt> </dl> | SECAM G<br/>                                                                                             |
| <dl> <dt>20 (0x14) </dt> </dl> | SECAM H<br/>                                                                                             |
| <dl> <dt>21 (0x15) </dt> </dl> | SECAM K<br/>                                                                                             |
| <dl> <dt>22 (0x16) </dt> </dl> | SECAM 版 K1<br/>                                                                                            |
| <dl> <dt>23 (0x17) </dt> </dl> | SECAM L<br/>                                                                                             |
| <dl> <dt>24 (0x18) </dt> </dl> | SECAM L1<br/>                                                                                            |
| <dl> <dt>25 (0x19) </dt> </dl> | EIA861<br/>                                                                                              |
| <dl> <dt>26 (0x1A) </dt> </dl> | EIA861A<br/>                                                                                             |
| <dl> <dt>27 (0x1B) </dt> </dl> | EIA861B<br/>                                                                                             |



 

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

 

 




