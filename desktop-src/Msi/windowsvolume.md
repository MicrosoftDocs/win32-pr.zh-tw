---
description: 安裝程式會將 WindowsVolume 屬性設定為 windows 資料夾的磁片區。
ms.assetid: 56b78c88-ef58-4474-92ad-b42fe49a2f30
title: WindowsVolume 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec3e0632fa981e9ea511be5017d02411bb6bb18355187c818ac3cd6c39e4f670
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117989932"
---
# <a name="windowsvolume-property"></a>WindowsVolume 屬性

安裝程式會將 **WindowsVolume** 屬性設定為 windows 資料夾的磁片區。 屬性一律以反斜線結尾。 這可用來設定 Windows 資料夾所在磁片區的預設位置，因為 [**ROOTDRIVE**](rootdrive.md)屬性不一定等於此磁片磁碟機。

## <a name="remarks"></a>備註

請勿在 [目錄](directory-table.md)資料表的目錄資料行中使用 **WindowsVolume** 屬性。 [**WindowsFolder**](windowsfolder.md)屬性包含 Windows 資料夾的路徑。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式，請參閱[Windows Installer Run-Time](windows-installer-portal.md) Windows 版本所需的最小 Windows Installer service pack 資訊的需求。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 




