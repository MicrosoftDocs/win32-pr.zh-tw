---
description: 如果設定此位，此控制項會顯示與目前安裝相關的所有磁片區，再加上所有遠端磁片區。 如果未設定此位，控制項會列出目前安裝中的磁片區。
ms.assetid: be70cd86-6aaf-4307-a553-715d6185accd
title: RemoteVolume 控制項屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3154b8002eaaf0115b57ea6b09ab3d31b2b7763a4a5c72bc97bbf29efb974e83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117990806"
---
# <a name="remotevolume-control-attribute"></a>RemoteVolume 控制項屬性

如果設定此位，此控制項會顯示與目前安裝相關的所有磁片區，再加上所有遠端磁片區。 如果未設定此位，控制項會列出目前安裝中的磁片區。

## <a name="valid-controls"></a>有效的控制項

[DirectoryCombo](directorycombo-control.md)

[VolumeCostList](volumecostlist-control.md)

[VolumeSelectCombo](volumeselectcombo-control.md)

## <a name="value"></a>值



| Decimal | 十六進位 | 常數                               |
|---------|-------------|----------------------------------------|
| 262144  | 0x00040000  | **msidbControlAttributesRemoteVolume** |



 

## <a name="remarks"></a>備註

若要在控制項上設定此屬性，請在控制項 [資料表](control-table.md)的 [屬性] 資料行中包含 RemoteVolume 位。

請參閱 [控制項屬性](control-attributes.md) 和 [控制項](controls.md)。

 

 



