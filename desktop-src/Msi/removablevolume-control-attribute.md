---
description: 如果設定此位，此控制項會顯示與目前安裝相關的所有磁片區，再加上所有抽取式磁碟區。 如果未設定此位，控制項會列出目前安裝中的磁片區。
ms.assetid: fc16ca46-54a1-4b24-ba51-8b4d358268f4
title: RemovableVolume 控制項屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5a91a464eb55ee965f12eae9885849eb2080996
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690240"
---
# <a name="removablevolume-control-attribute"></a>RemovableVolume 控制項屬性

如果設定此位，此控制項會顯示與目前安裝相關的所有磁片區，再加上所有抽取式磁碟區。 如果未設定此位，控制項會列出目前安裝中的磁片區。

## <a name="valid-controls"></a>有效的控制項

[DirectoryCombo](directorycombo-control.md)

 

[VolumeCostList](volumecostlist-control.md)

 

[VolumeSelectCombo](volumeselectcombo-control.md)

## <a name="value"></a>值



| Decimal | 十六進位 | 常數                                  |
|---------|-------------|-------------------------------------------|
| 65536   | 0x00010000  | **msidbControlAttributesRemovableVolume** |



 

## <a name="remarks"></a>備註

若要在控制項上設定此屬性，請在控制項 [資料表](control-table.md)的 [屬性] 資料行中包含 RemovableVolume 位。

請參閱 [控制項屬性](control-attributes.md) 和 [控制項](controls.md)。

 

 



