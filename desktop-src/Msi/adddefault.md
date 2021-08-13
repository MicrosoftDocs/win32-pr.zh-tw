---
description: ADDDEFAULT 屬性的值是以逗號分隔的功能清單，這些功能會安裝在其預設設定中。
ms.assetid: 78cec3fc-c653-487a-b41c-a43c42e3a157
title: ADDDEFAULT 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e854df38b58a19f41f98cf1f96657dafdda0c4134c7085c50b4c9c4528b3164e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118639702"
---
# <a name="adddefault-property"></a>ADDDEFAULT 屬性

**ADDDEFAULT** 屬性的值是以逗號分隔的功能清單，這些功能會安裝在其預設設定中。 功能必須出現在[功能資料表](feature-table.md)的功能資料行中。 若要安裝預設設定中的所有功能，請在命令列上使用 ADDDEFAULT = ALL。

**ADDDEFAULT** 屬性中所列的功能會安裝在與使用者要求安裝功能時相同的安裝狀態。 狀態是由 [功能資料表](feature-table.md)的 [屬性] 資料行中針對功能所設定的位來決定，而在 [元件資料表](component-table.md)的 [屬性] 資料行中，為功能元件設定的位。

## <a name="remarks"></a>備註

功能名稱會區分大小寫。

安裝程式一律會依下列順序評估下列屬性：

1.  [**ADDLOCAL**](addlocal.md)
2.  [**刪除**](remove.md)
3.  [**ADDSOURCE**](addsource.md)
4.  **ADDDEFAULT**
5.  [**REINSTALL**](reinstall.md)
6.  [**做廣告**](advertise.md)
7.  [**COMPADDLOCAL**](compaddlocal.md)
8.  [**COMPADDSOURCE**](compaddsource.md)
9.  [**COMPADDDEFAULT**](compadddefault.md)
10. [**FILEADDLOCAL**](fileaddlocal.md)
11. [**FILEADDSOURCE**](fileaddsource.md)
12. [**FILEADDDEFAULT**](fileadddefault.md)

例如：

-   如果命令列指定： ADDLOCAL = ALL、ADDSOURCE = MyFeature，則所有功能都會先設定為執行本機，然後 **MyFeature** 設定為從來源執行。
-   如果命令列是： ADDSOURCE = ALL、ADDLOCAL = MyFeature、first **MyFeature** 設定為 run-local，則當 ADDSOURCE = ALL 進行評估時，包括 **MyFeature**) 在內的所有 (功能都會重設為從來源執行。

安裝程式在暫停的安裝期間，或在命令列上指定了上述任何屬性時，會將 [**預先**](preselected.md) 選取的屬性設定為 "1" 的值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式。 如需 Windows Installer 版本所需的最低 Windows service pack 相關資訊，請參閱[Windows Installer Run-Time 需求](windows-installer-portal.md)。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 




