---
description: 如果已安裝所有目前選取的功能，則安裝程式會將 PrimaryVolumeSpaceRemaining 屬性的值設為字串，代表 PrimaryVolumePath 屬性所參考的磁片區上剩餘的位元組總數。
ms.assetid: 8a59d22f-b8a1-47bf-90f3-f8cadfae8ecd
title: PrimaryVolumeSpaceRemaining 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdae4e0895c18ca32ab65f68daa13cd6c702f62c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976280"
---
# <a name="primaryvolumespaceremaining-property"></a>PrimaryVolumeSpaceRemaining 屬性

如果已安裝所有目前選取的功能，則安裝程式會將 **PrimaryVolumeSpaceRemaining** 屬性的值設為字串，代表 [**PrimaryVolumePath**](primaryvolumepath.md) 屬性所參考的磁片區上剩餘的位元組總數。 如同 [**PrimaryVolumeSpaceAvailable**](primaryvolumespaceavailable.md) 屬性，此數位會以512個位元組的單位表示。

## <a name="remarks"></a>備註

注意：如果此值要顯示在靜態 [文字控制項](text-control.md)內，則可以使用 [FormatSize](formatsize-control-attribute.md) 位自動格式化，並以適當的單位（kb 或 mb）標記此數位。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 




