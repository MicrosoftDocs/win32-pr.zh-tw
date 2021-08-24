---
description: 如果已安裝所有目前選取的功能，則安裝程式會將 PrimaryVolumeSpaceRemaining 屬性的值設為字串，代表 PrimaryVolumePath 屬性所參考的磁片區上剩餘的位元組總數。
ms.assetid: 8a59d22f-b8a1-47bf-90f3-f8cadfae8ecd
title: PrimaryVolumeSpaceRemaining 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16107af105de0684bd917177050017a3c14e40aff32c658881342a90e877c973
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580488"
---
# <a name="primaryvolumespaceremaining-property"></a>PrimaryVolumeSpaceRemaining 屬性

如果已安裝所有目前選取的功能，則安裝程式會將 **PrimaryVolumeSpaceRemaining** 屬性的值設為字串，代表 [**PrimaryVolumePath**](primaryvolumepath.md) 屬性所參考的磁片區上剩餘的位元組總數。 如同 [**PrimaryVolumeSpaceAvailable**](primaryvolumespaceavailable.md) 屬性，此數位會以512個位元組的單位表示。

## <a name="remarks"></a>備註

注意：如果此值要顯示在靜態 [文字控制項](text-control.md)內，則可以使用 [FormatSize](formatsize-control-attribute.md) 位自動格式化，並以適當的單位（kb 或 mb）標記此數位。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 




