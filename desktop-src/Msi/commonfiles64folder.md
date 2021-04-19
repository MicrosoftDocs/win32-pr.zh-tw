---
description: 安裝程式會將 CommonFiles64Folder 屬性設定為預先定義的64位通用檔案資料夾的完整路徑。 現有的 CommonFilesFolder 屬性會設定為對應的32位資料夾。
ms.assetid: 6730170a-0f73-4a84-b3fb-bd15c72917c7
title: CommonFiles64Folder 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c44a6720e609cfa79cd0e4adbfd5136c7a92a5ce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993369"
---
# <a name="commonfiles64folder-property"></a>CommonFiles64Folder 屬性

安裝程式會將 **CommonFiles64Folder** 屬性設定為預先定義的64位通用檔案資料夾的完整路徑。 現有的 [**CommonFilesFolder**](commonfilesfolder.md) 屬性會設定為對應的32位資料夾。

## <a name="remarks"></a>備註

安裝程式會在64位 Windows 上設定這個屬性。 這個屬性不會用於32位的 Windows 上。 使用64位 Windows 時，此值可能是 "C： \\ Program files \\ Common Files"。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer。 如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 




