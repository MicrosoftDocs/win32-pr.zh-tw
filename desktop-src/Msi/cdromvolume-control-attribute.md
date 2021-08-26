---
description: 如果設定了 CDROMVolume 控制項位，此控制項就會顯示目前安裝中的所有磁片區，再加上所有的 CD-ROM 磁片區。
ms.assetid: 233df659-413d-416e-a3d7-d05a67e9bd73
title: CDROMVolume 控制項屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78abd961ddfd710defea9b464ea861f731fcf84a0989062f0607fda8ced5b381
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078038"
---
# <a name="cdromvolume-control-attribute"></a>CDROMVolume 控制項屬性

如果設定了 CDROMVolume 控制項位，此控制項就會顯示目前安裝中的所有磁片區，再加上所有的 CD-ROM 磁片區。

如果未設定此位，控制項會顯示目前安裝中的所有磁片區。

## <a name="valid-controls"></a>有效的控制項

[DirectoryCombo](directorycombo-control.md)

 

[VolumeCostList](volumecostlist-control.md)

 

[VolumeSelectCombo](volumeselectcombo-control.md)

## <a name="value"></a>值



| Decimal | 十六進位 | 常數                              |
|---------|-------------|---------------------------------------|
| 524288  | 0x00080000  | **msidbControlAttributesCDROMVolume** |



 

## <a name="remarks"></a>備註

若要在控制項上設定此屬性，請在控制項 [資料表](control-table.md)的 [屬性] 資料行中包含 CDROMVolume 位。

請參閱 [控制項屬性](control-attributes.md) 和您需要在 [控制項](controls.md)下建立的控制項。

 

 



