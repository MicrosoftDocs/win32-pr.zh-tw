---
description: 如果設定此位，此控制項會顯示與目前安裝相關的所有磁片區，再加上所有 RAM 磁碟區。 如果未設定此位，控制項會列出目前安裝中的磁片區。
ms.assetid: 52526f39-26fb-4a67-a95f-77f7eb761372
title: RAMDiskVolume 控制項屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc4324af143bab619c6f881925586186be45b44a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980835"
---
# <a name="ramdiskvolume-control-attribute"></a>RAMDiskVolume 控制項屬性

如果設定此位，此控制項會顯示與目前安裝相關的所有磁片區，再加上所有 RAM 磁碟區。 如果未設定此位，控制項會列出目前安裝中的磁片區。

## <a name="valid-controls"></a>有效的控制項

[DirectoryCombo](directorycombo-control.md)

 

[VolumeCostList](volumecostlist-control.md)

 

[VolumeSelectCombo](volumeselectcombo-control.md)

## <a name="value"></a>值



| Decimal | 十六進位 | 常數                                |
|---------|-------------|-----------------------------------------|
| 1048567 | 0x00100000  | **msidbControlAttributesRAMDiskVolume** |



 

## <a name="remarks"></a>備註

若要在控制項上設定此屬性，請在控制項 [資料表](control-table.md)的 [屬性] 資料行中包含 RAMDiskVolume 位。

請參閱 [控制項屬性](control-attributes.md) 和 [控制項](controls.md)。

 

 



