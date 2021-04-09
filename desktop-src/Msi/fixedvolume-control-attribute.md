---
description: 如果設定了 FixedVolume 控制項位，此控制項就會顯示與目前安裝相關的所有磁片區，再加上所有固定的內部硬碟。
ms.assetid: e0917a8c-f43a-412d-9b91-9d5f80779f41
title: FixedVolume 控制項屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c524bd228d19dbef823df00eff83e34df503a438
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848507"
---
# <a name="fixedvolume-control-attribute"></a>FixedVolume 控制項屬性

如果設定了 FixedVolume 控制項位，此控制項就會顯示與目前安裝相關的所有磁片區，再加上所有固定的內部硬碟。

如果未設定此位，控制項會列出目前安裝中的磁片區。

## <a name="valid-controls"></a>有效的控制項

[DirectoryCombo](directorycombo-control.md)

 

[VolumeCostList](volumecostlist-control.md)

 

[VolumeSelectCombo](volumeselectcombo-control.md)



| Decimal | 十六進位 | 常數                              |
|---------|-------------|---------------------------------------|
| 131072  | 0x00020000  | **msidbControlAttributesFixedVolume** |



 

## <a name="remarks"></a>備註

若要在控制項上設定此屬性，請在控制項 [資料表](control-table.md)的 [屬性] 資料行中包含 FixedVolume 位。

請參閱 [控制項屬性](control-attributes.md) 和您需要在 [控制項](controls.md)下建立的控制項。

 

 



