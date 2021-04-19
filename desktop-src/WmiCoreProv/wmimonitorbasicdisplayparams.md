---
description: 代表電腦監視器的基本顯示功能。
ms.assetid: 08405e7f-7824-4e44-9f37-da9bb5619cd6
title: WmiMonitorBasicDisplayParams 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBasicDisplayParams
- WmiMonitorBasicDisplayParams.Active
- WmiMonitorBasicDisplayParams.DisplayTransferCharacteristic
- WmiMonitorBasicDisplayParams.InstanceName
- WmiMonitorBasicDisplayParams.MaxHorizontalImageSize
- WmiMonitorBasicDisplayParams.MaxVerticalImageSize
- WmiMonitorBasicDisplayParams.SupportedDisplayFeatures
- WmiMonitorBasicDisplayParams.VideoInputType
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: e457757a3542bbfc8ded7536396458ef3e592714
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984638"
---
# <a name="wmimonitorbasicdisplayparams-class"></a>WmiMonitorBasicDisplayParams 類別

**WmiMonitorBasicDisplayParams** WMI 類別代表電腦監視器的基本顯示功能。 **VideoInputType** 屬性的值會指出監視器是否為類比或數位。 此類別中的資料會對應到視頻電子產品標準關聯之基本顯示參數/功能區塊中的資料 () 增強的擴充顯示器識別資料 (E-EDID) 標準。

## <a name="syntax"></a>語法

``` syntax
class WmiMonitorBasicDisplayParams : MSMonitorClass
{
  boolean                            Active;
  uint8                              DisplayTransferCharacteristic;
  string                             InstanceName;
  uint8                              MaxHorizontalImageSize;
  uint8                              MaxVerticalImageSize;
  SupportedDisplayFeaturesDescriptor SupportedDisplayFeatures;
  uint8                              VideoInputType;
};
```

## <a name="members"></a>成員

**WmiMonitorBasicDisplayParams** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**WmiMonitorBasicDisplayParams** 類別具有這些屬性。

<dl> <dt>

**使用中**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

表示使用中的監視器。

</dd> <dt>

**DisplayTransferCharacteristic**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

顯示傳輸特性 (100 \* Gamma-100) 。

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

**MaxHorizontalImageSize**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

水準影像大小的最大值（以公分為單位）。 如需詳細資訊，請參閱＜備註＞。

</dd> <dt>

**MaxVerticalImageSize**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

垂直影像大小的最大值（以公分為單位）。 如需詳細資訊，請參閱＜備註＞。

</dd> <dt>

**SupportedDisplayFeatures**
</dt> <dd> <dl> <dt>

資料類型： **[ **SupportedDisplayFeaturesDescriptor**](supporteddisplayfeaturesdescriptor.md)**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

顯示監視器支援的功能。

</dd> <dt>

**VideoInputType**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

影片輸入類型。



| 值                                                                              | 意義            |
|------------------------------------------------------------------------------------|--------------------|
| <dl> <dt>0 (0x0) </dt> </dl> | 類比<br/>  |
| <dl> <dt>1 (0x1) </dt> </dl> | Digital<br/> |



 

</dd> </dl>

## <a name="remarks"></a>備註

**MaxHorizontalImageSize** 和 **MaxVerticalImageSize** 代表監視器可針對整組支援的計時和格式組合正確顯示的影像維度大小上限。 最大影像維度是由 VESA 影片影像區域定義所定義 (VIAD) 標準，並四捨五入至最接近的釐米。 主機電腦系統可以使用此資料來選取影像大小和外觀比例，以允許適當調整的文字。 請注意，如果其中一或兩個欄位都是零，則系統不會對顯示大小做出任何假設。 例如，投影顯示器的大小可能不確定。

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

 

 




