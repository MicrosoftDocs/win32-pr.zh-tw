---
description: 如果設定了 FloppyVolume 控制項位，此控制項就會顯示與目前安裝相關的所有磁片區，再加上所有的磁片區。
ms.assetid: 65e17920-bb2c-4b98-a2dd-ebaee752ed0a
title: FloppyVolume 控制項屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4639960fee79336048082c91088e19c1b360f857216f2cf0ad9ed07c64b52b8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947009"
---
# <a name="floppyvolume-control-attribute"></a>FloppyVolume 控制項屬性

如果設定了 FloppyVolume 控制項位，此控制項就會顯示與目前安裝相關的所有磁片區，再加上所有的磁片區。

如果未設定此位，控制項會列出目前安裝中的磁片區。

## <a name="valid-controls"></a>有效的控制項

[DirectoryCombo](directorycombo-control.md)

[VolumeCostList](volumecostlist-control.md)

[VolumeSelectCombo](volumeselectcombo-control.md)

## <a name="value"></a>值



| Decimal | 十六進位 | 常數                               |
|---------|-------------|----------------------------------------|
| 2097152 | 0x00200000  | **msidbControlAttributesFloppyVolume** |



 

## <a name="remarks"></a>備註

若要在控制項上設定此屬性，請在控制項 [資料表](control-table.md)的 [屬性] 資料行中包含 FloppyVolume 位。

請參閱 [控制項屬性](control-attributes.md) 和您需要在 [控制項](controls.md)下建立的控制項。

 

 



