---
description: FILEADDLOCAL 屬性的值代表要安裝以從本機來源媒體執行的逗號分隔檔案索引鍵清單。
ms.assetid: 89ae876e-53f0-4c1d-ba16-7513af79ee5e
title: FILEADDLOCAL 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2c764fa89480cf4f37e19a4f6a10ee354a07bfe18f9fbc203ea0db4410f7bdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946988"
---
# <a name="fileaddlocal-property"></a>FILEADDLOCAL 屬性

**FILEADDLOCAL** 屬性的值代表要安裝以從本機來源媒體執行的逗號分隔檔案索引鍵清單。 針對清單中的每個檔案機碼，安裝程式會決定控制該檔案的元件，然後檢查 [FeatureComponents](featurecomponents-table.md) 資料表連結至該元件的所有功能，並安裝需要最少量磁碟空間的功能。 清單中的檔案索引鍵必須存在於 [file](file-table.md) 資料表的 file 資料行中。

## <a name="remarks"></a>備註

請注意，檔案索引鍵名稱會區分大小寫。 另請注意，如果在 [元件資料表的 [屬性](component-table.md) ] 資料行中設定 LocalOnly 位旗標，則會將元件安裝在本機執行。

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
10. **FILEADDLOCAL**
11. [**FILEADDSOURCE**](fileaddsource.md)
12. [**FILEADDDEFAULT**](fileadddefault.md)

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

 

 




