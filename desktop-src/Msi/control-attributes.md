---
description: 如需控制項屬性的詳細資訊，請參閱您需要在控制項中建立之特定控制項的連結，以及下列清單中特定控制項屬性的連結。
ms.assetid: 948ce3d3-e463-40de-8b5f-21ef18b1a0ce
title: 控制項屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb9d7412ce3893b785dccf067287c191f033bdf5a100628577260ff10f74ce1e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119500718"
---
# <a name="control-attributes"></a>控制項屬性

如需控制項屬性的詳細資訊，請參閱您需要在 [控制項](controls.md) 中建立之特定控制項的連結，以及下列清單中特定控制項屬性的連結。

下列方法可用來指定控制項的屬性：

-   您可以使用 [ControlCondition 資料表](controlcondition-table.md) ，根據屬性或條件陳述式的值來停用、啟用、隱藏或顯示控制項。 您也可以使用此資料表來覆寫在 [對話方塊資料表](dialog-table.md)中指定的預設控制項。
-   將控制項訂閱至 [EventMapping 資料表](eventmapping-table.md)中的 ControlEvent。 在 [屬性] 資料行中輸入屬性的識別碼，並在此資料表的 [事件] 資料行中輸入 ControlEvent 的識別碼。
-   在 [控制資料表](control-table.md)的 [屬性] 資料行中，設定控制項的控制項屬性位旗標。 這會在建立控制項時設定屬性。

某些屬性無法針對每個控制項設定，或由上述所有方法指定。 如需詳細資料，請參閱特定的控制項和屬性主題。

某些控制項屬性的初始值可以使用 [control 資料表](control-table.md)中的位來設定。



| 屬性                                          | Decimal | 十六進位 | 常數                               |
|----------------------------------------------------|---------|-------------|----------------------------------------|
| [BiDi](bidi-control-attribute.md)                 | 224     | 0x000000E0  | **msidbControlAttributesBiDi**         |
| [Enabled](enabled-control-attribute.md)           | 2       | 0x00000002  | **msidbControlAttributesEnabled**      |
| [間接](indirect-control-attribute.md)         | 8       | 0x00000008  | **msidbControlAttributesIndirect**     |
| [整數控制項](integer-control-attribute.md)   | 16      | 0x00000010  | **msidbControlAttributesInteger**      |
| [LeftScroll](leftscroll-control-attribute.md)     | 128     | 0x00000080  | **msidbControlAttributesLeftScroll**   |
| [RightAligned](rightaligned-control-attribute.md) | 64      | 0x00000040  | **msidbControlAttributesRightAligned** |
| [RTLRO](rtlro-control-attribute.md)               | 32      | 0x00000020  | **msidbControlAttributesRTLRO**        |
| [沉沒](sunken-control-attribute.md)             | 4       | 0x00000004  | **msidbControlAttributesSunken**       |
| [Visible](visible-control-attribute.md)           | 1       | 0x00000001  | **msidbControlAttributesVisible**      |



 

這些文字控制項的屬性是以位來設定。



| 屬性                                            | Decimal | 十六進位 | 常數                                |
|------------------------------------------------------|---------|-------------|-----------------------------------------|
| [FormatSize](formatsize-control-attribute.md)       | 524288  | 0x00080000  | **msidbControlAttributesFormatSize**    |
| [NoPrefix](noprefix-control-attribute.md)           | 131072  | 0x00020000  | **msidbControlAttributesNoPrefix**      |
| [NoWrap](nowrap-control-attribute.md)               | 262144  | 0x00040000  | **msidbControlAttributesNoWrap**        |
| [密碼](password-control-attribute.md)           | 2097152 | 0x00200000  | **msidbControlAttributesPasswordInput** |
| [透明](transparent-control-attribute.md)     | 65536   | 0x00010000  | **msidbControlAttributesTransparent**   |
| [UsersLanguage](userslanguage-control-attribute.md) | 1048576 | 0x00100000  | **msidbControlAttributesUsersLanguage** |



 

ProgressBar 控制項的這個屬性是以位來設定。



| 屬性                                      | Decimal | 十六進位 | 常數                             |
|------------------------------------------------|---------|-------------|--------------------------------------|
| [Progress95](progress95-control-attribute.md) | 65536   | 0x00010000  | **msidbControlAttributesProgress95** |



 

這些磁片區和目錄 SelectCombo 控制項的屬性是以位來設定。



| 屬性                                                | Decimal | 十六進位 | 常數                                  |
|----------------------------------------------------------|---------|-------------|-------------------------------------------|
| [CDROMVolume](cdromvolume-control-attribute.md)         | 524288  | 0x00080000  | **msidbControlAttributesCDROMVolume**     |
| [FixedVolume](fixedvolume-control-attribute.md)         | 131072  | 0x00020000  | **msidbControlAttributesFixedVolume**     |
| [FloppyVolume](floppyvolume-control-attribute.md)       | 2097152 | 0x00200000  | **msidbControlAttributesFloppyVolume**    |
| [RAMDiskVolume](ramdiskvolume-control-attribute.md)     | 1048576 | 0x00100000  | **msidbControlAttributesRAMDiskVolume**   |
| [RemoteVolume](remotevolume-control-attribute.md)       | 262144  | 0x00040000  | **msidbControlAttributesRemoteVolume**    |
| [RemovableVolume](removablevolume-control-attribute.md) | 65536   | 0x00010000  | **msidbControlAttributesRemovableVolume** |



 

ListBox 和 ComboBox 控制項的這些屬性是以位來設定。



| 屬性                                            | Decimal | 十六進位 | 常數                            |
|------------------------------------------------------|---------|-------------|-------------------------------------|
| [ComboList 控制項](combolist-control-attribute.md) | 131072  | 0x00020000  | **msidbControlAttributesComboList** |
| [排序的控制項](sorted-control-attribute.md)       | 65536   | 0x00010000  | **msidbControlAttributesSorted**    |



 

編輯控制項的這個屬性是以位來設定。



| 屬性                                    | Decimal | 十六進位 | 常數                            |
|----------------------------------------------|---------|-------------|-------------------------------------|
| [適用](multiline-control-attribute.md) | 65536   | 0x00010000  | **msidbControlAttributesMultiline** |



 

這些 PictureButton 控制項的屬性是以位來設定。



| 屬性                                          | Decimal | 十六進位 | 常數                             |
|----------------------------------------------------|---------|-------------|--------------------------------------|
| [點陣圖](bitmap-control-attribute.md)             | 262144  | 0x00040000  | **msidbControlAttributesBitmap**     |
| [FixedSize](fixedsize-control-attribute.md)       | 1048576 | 0x00100000  | **msidbControlAttributesFixedSize**  |
| [圖示](icon-control-attribute.md)                 | 524288  | 0x00080000  | **msidbControlAttributesIcon**       |
| [IconSize16](iconsize-control-attribute.md)       | 2097152 | 0x00200000  | **msidbControlAttributesIconSize16** |
| [IconSize32](iconsize-control-attribute.md)       | 4194304 | 0x00400000  | **msidbControlAttributesIconSize32** |
| [IconSize48](iconsize-control-attribute.md)       | 6291456 | 0x00600000  | **msidbControlAttributesIconSize48** |
| [PushLike 控制項](pushlike-control-attribute.md) | 131072  | 0x00020000  | **msidbControlAttributesPushLike**   |



 

選項按鈕控制項的這個屬性是以位來設定。



| 屬性                                    | Decimal  | 十六進位 | 常數                            |
|----------------------------------------------|----------|-------------|-------------------------------------|
| [HasBorder](hasborder-control-attribute.md) | 16777216 | 0x01000000  | **msidbControlAttributesHasBorder** |



 

此按鈕控制項的這個屬性是以位來設定。



| 屬性                                        | Decimal | 十六進位 | 常數                                  |
|--------------------------------------------------|---------|-------------|-------------------------------------------|
| [ElevationShield](elevationshield-attribute.md) | 8388608 | 0x00800000  | **msidbControlAttributesElevationShield** |



 

VolumeCostList 控制項的這個屬性是以位來設定。



| 屬性                                                                | Decimal | 十六進位 | 常數                         |
|--------------------------------------------------------------------------|---------|-------------|----------------------------------|
| [ControlShowRollbackCost](controlshowrollbackcost-control-attribute.md) | 4194304 | 0x00400000  | **msidbControlShowRollbackCost** |



 

下列控制項屬性不是以位設定。 這些屬性會編寫到使用者介面資料表中，或使用 [控制項事件](control-events.md)進行設定。

[BillboardName](billboardname-control-attribute.md)

 

[IndirectPropertyName](indirectpropertyname-control-attribute.md)

 

[位置](position-control-attribute.md)

 

[進度控制項](progress-control-attribute.md)

 

[PropertyName](propertyname-control-attribute.md)

 

[PropertyValue](propertyvalue-control-attribute.md)

 

[Text Control](text-control-attribute.md)

 

[TimeRemaining](timeremaining-control-attribute.md)

請參閱 [加入控制項和文字](adding-controls-and-text.md)。

 

 



