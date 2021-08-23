---
description: 安裝程式會將 PrimaryVolumeSpaceAvailable 屬性的值設定為字串，該字串代表 PrimaryVolumePath 屬性所參考之磁片區上可用的位元組總數（單位為512）。
ms.assetid: fff546d5-d26c-48cf-8d00-595a23c0a2af
title: PrimaryVolumeSpaceAvailable 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9336bfa32ebb3bf0c12b7e7fc54ddad2b26cd635c820ca6e8ea2caabe163ceb6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580668"
---
# <a name="primaryvolumespaceavailable-property"></a>PrimaryVolumeSpaceAvailable 屬性

安裝程式會將 **PrimaryVolumeSpaceAvailable** 屬性的值設定為字串，該字串代表 [**PrimaryVolumePath**](primaryvolumepath.md) 屬性所參考之磁片區上可用的位元組總數（單位為512）。

## <a name="remarks"></a>備註

例如，如果 [**PrimaryVolumePath**](primaryvolumepath.md) 設定為 "D："，且磁片區 D：有446134272個位元組可用，則 **PrimaryVolumeSpaceAvailable** 會設定為871356。

注意：如果此值要顯示在靜態 [文字控制項](text-control.md)內，則可以使用 [FormatSize](formatsize-control-attribute.md) 位自動格式化，並以適當的單位（kb 或 mb）標記此數位。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式。 如需 Windows Installer 版本所需的最低 Windows service pack 相關資訊，請參閱[Windows Installer Run-Time 需求](windows-installer-portal.md)。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 




