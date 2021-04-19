---
description: 安裝程式會將 PrimaryVolumeSpaceAvailable 屬性的值設定為字串，該字串代表 PrimaryVolumePath 屬性所參考之磁片區上可用的位元組總數（單位為512）。
ms.assetid: fff546d5-d26c-48cf-8d00-595a23c0a2af
title: PrimaryVolumeSpaceAvailable 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d464626b68f9d8ccb32ceb08c52af0cf7efa5920
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998806"
---
# <a name="primaryvolumespaceavailable-property"></a>PrimaryVolumeSpaceAvailable 屬性

安裝程式會將 **PrimaryVolumeSpaceAvailable** 屬性的值設定為字串，該字串代表 [**PrimaryVolumePath**](primaryvolumepath.md) 屬性所參考之磁片區上可用的位元組總數（單位為512）。

## <a name="remarks"></a>備註

例如，如果 [**PrimaryVolumePath**](primaryvolumepath.md) 設定為 "D："，且磁片區 D：有446134272個位元組可用，則 **PrimaryVolumeSpaceAvailable** 會設定為871356。

注意：如果此值要顯示在靜態 [文字控制項](text-control.md)內，則可以使用 [FormatSize](formatsize-control-attribute.md) 位自動格式化，並以適當的單位（kb 或 mb）標記此數位。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer。 如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 




