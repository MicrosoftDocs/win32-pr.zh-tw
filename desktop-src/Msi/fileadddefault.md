---
description: FILEADDDEFAULT 屬性的值是以逗號分隔的檔案索引鍵清單，會安裝在其預設設定中。
ms.assetid: 089b8dd9-1841-4b6d-8da8-d5aa5de85a68
title: FILEADDDEFAULT 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bafa5692cbba5b00aff6c3cbdef66e33420b4b135d0c3dfa13d9ae6e2255e5d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828948"
---
# <a name="fileadddefault-property"></a>FILEADDDEFAULT 屬性

**FILEADDDEFAULT** 屬性的值是以逗號分隔的檔案索引鍵清單，會安裝在其預設設定中。 針對清單中的每個檔案機碼，安裝程式會決定控制該檔案的元件，並安裝需要最少磁碟空間的功能。 清單中的檔案索引鍵必須存在於 [file](file-table.md) 資料表的 file 資料行中。 某項功能的安裝狀態與使用者要求安裝時所需的功能相同。 狀態是由 [功能資料表](feature-table.md)的 [屬性] 資料行中的功能所設定的位，以及 [元件資料表](component-table.md)的 [屬性] 資料行中的功能元件所設定的位所決定。

## <a name="remarks"></a>備註

請注意，檔案索引鍵名稱會區分大小寫。 另請注意，如果在 [元件資料表的 [屬性](component-table.md) ] 資料行中設定 SourceOnly 位旗標，則元件會安裝成從來源執行。

安裝程式一律會依下列順序評估下列屬性。

1.  [**ADDLOCAL**](addlocal.md)
2.  [**刪除**](remove.md)
3.  [**ADDSOURCE**](addsource.md)
4.  [**ADDDEFAULT**](adddefault.md)
5.  [**REINSTALL**](reinstall.md)
6.  [**做廣告**](advertise.md)
7.  [**COMPADDLOCAL**](compaddlocal.md)
8.  [**COMPADDSOURCE**](compaddsource.md)
9.  [**COMPADDDEFAULT**](compadddefault.md)
10. [**FILEADDLOCAL**](fileaddlocal.md)
11. [**FILEADDSOURCE**](fileaddsource.md)
12. **FILEADDDEFAULT**

例如，如果命令列指定： ADDLOCAL = ALL、ADDSOURCE = MyFeature，則所有功能都會先設定為執行本機，然後 MyFeature 設定為從來源執行。 如果命令列是： ADDSOURCE = ALL、ADDLOCAL = MyFeature、first MyFeature 設定為 run-local，則當 ADDSOURCE = ALL 進行評估時，包括 MyFeature) 在內的所有 (功能都會重設為從來源執行。

安裝程式在停用的安裝期間，或在命令列上指定了上述任何屬性時，會將 [**預先**](preselected.md) 選取的屬性設定為 "1" 的值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式。 如需 Windows Installer 版本所需的最低 Windows service pack 相關資訊，請參閱[Windows Installer Run-Time 需求](windows-installer-portal.md)。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 




