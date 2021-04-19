---
description: FILEADDSOURCE 屬性的值代表以逗號分隔的檔案索引鍵清單，要從來源媒體執行安裝。
ms.assetid: 52e328e7-7a98-4762-86a1-48e52fd55882
title: FILEADDSOURCE 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24b99ea1d9f4d6e212b74d6c4ee54655dce98c60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976560"
---
# <a name="fileaddsource-property"></a>FILEADDSOURCE 屬性

**FILEADDSOURCE** 屬性的值代表以逗號分隔的檔案索引鍵清單，要從來源媒體執行安裝。 針對清單中的每個檔案機碼，安裝程式會決定控制該檔案的元件，然後檢查 [FeatureComponents](featurecomponents-table.md) 資料表連結至該元件的所有功能，並安裝需要最少量磁碟空間的功能。 清單中的檔案索引鍵必須存在於 [file](file-table.md) 資料表的 file 資料行中。

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
10. [**FILEADDLOCAL**](fileaddlocal.md)
11. **FILEADDSOURCE**
12. [**FILEADDDEFAULT**](fileadddefault.md)

例如，如果命令列指定： ADDLOCAL = ALL、ADDSOURCE = MyFeature，則所有功能都會先設定為執行本機，然後 MyFeature 設定為從來源執行。 如果命令列是： ADDSOURCE = ALL、ADDLOCAL = MyFeature、first MyFeature 設定為 run-local，則當 ADDSOURCE = ALL 進行評估時，包括 MyFeature) 在內的所有 (功能都會重設為從來源執行。

安裝程式在停用的安裝期間，或在命令列上指定了上述任何屬性時，會將 [**預先**](preselected.md) 選取的屬性設定為 "1" 的值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer。 如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 




