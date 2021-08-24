---
description: 安裝程式會將 PrimaryVolumeSpaceRequired 屬性的值設定為字串，此字串代表 PrimaryVolumePath 屬性所參考之磁片區上所有選定功能所需的總位元組數。
ms.assetid: 44c89bd8-774a-4b4f-9608-9a1926ef3b7d
title: PrimaryVolumeSpaceRequired 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08c644c53b5a36c8ba834a52c22ca3ba2b192499cbf351f122d8ed2b6a66a57f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042258"
---
# <a name="primaryvolumespacerequired-property"></a>PrimaryVolumeSpaceRequired 屬性

安裝程式會將 **PrimaryVolumeSpaceRequired** 屬性的值設定為字串，此字串代表 [**PrimaryVolumePath**](primaryvolumepath.md) 屬性所參考之磁片區上所有選定功能所需的總位元組數。 如同 [**PrimaryVolumeSpaceAvailable**](primaryvolumespaceavailable.md) 屬性，此數位會以512個位元組的單位表示。

## <a name="remarks"></a>備註

注意：如果此值要顯示在靜態 [文字控制項](text-control.md)內，則可以使用 [FormatSize](formatsize-control-attribute.md) 位自動格式化，並以適當的單位（kb 或 mb）標記此數位。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式。 如需 Windows Installer 版本所需的最低 Windows service pack 相關資訊，請參閱[Windows Installer Run-Time 需求](windows-installer-portal.md)。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 




