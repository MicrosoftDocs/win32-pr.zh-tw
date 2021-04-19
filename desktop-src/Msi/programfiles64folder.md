---
description: 安裝程式會將 ProgramFiles64Folder 屬性設定為預先定義之64位 Program Files 資料夾的完整路徑。 現有的 ProgramFilesFolder 屬性會設定為對應的32位資料夾。
ms.assetid: 9301628a-3d56-4d0a-aab5-88663742daa1
title: ProgramFiles64Folder 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdb8b85e0a433a3a4b51cfe23ef2de1f75dba09c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993522"
---
# <a name="programfiles64folder-property"></a>ProgramFiles64Folder 屬性

安裝程式會將 **ProgramFiles64Folder** 屬性設定為預先定義之64位 Program Files 資料夾的完整路徑。 現有的 [**ProgramFilesFolder**](programfilesfolder.md) 屬性會設定為對應的32位資料夾。

## <a name="remarks"></a>備註

安裝程式會設定這個屬性。 例如，在64位的 Windows 上，此值可能是 C： \\ Program Files。 這個屬性不會用於32位的 Windows 上。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer。 如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 




