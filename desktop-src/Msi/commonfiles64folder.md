---
description: 安裝程式會將 CommonFiles64Folder 屬性設定為預先定義的64位通用檔案資料夾的完整路徑。 現有的 CommonFilesFolder 屬性會設定為對應的32位資料夾。
ms.assetid: 6730170a-0f73-4a84-b3fb-bd15c72917c7
title: CommonFiles64Folder 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 025645f7e5ef4b841115c1bedcfa4b6fccf027913b2b1708895f7ab21bd5d9df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118145357"
---
# <a name="commonfiles64folder-property"></a>CommonFiles64Folder 屬性

安裝程式會將 **CommonFiles64Folder** 屬性設定為預先定義的64位通用檔案資料夾的完整路徑。 現有的 [**CommonFilesFolder**](commonfilesfolder.md) 屬性會設定為對應的32位資料夾。

## <a name="remarks"></a>備註

安裝程式會在64位 Windows 上設定這個屬性。 這個屬性不會用於32位 Windows。 使用64位 Windows 時，此值可能是 "C： \\ Program files \\ Common Files"。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式。 如需 Windows Installer 版本所需的最低 Windows service pack 相關資訊，請參閱[Windows Installer Run-Time 需求](windows-installer-portal.md)。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 




