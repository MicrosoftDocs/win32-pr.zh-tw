---
description: ADDLOCAL 屬性的值是以逗號分隔，且要在本機安裝的功能清單。
ms.assetid: d408986d-7889-4fd9-8202-1d2e59673a2f
title: ADDLOCAL 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9618389d6e409829dce1eb7bb3a38c1269a2e06d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996510"
---
# <a name="addlocal-property"></a>ADDLOCAL 屬性

**ADDLOCAL** 屬性的值是以逗號分隔，且要在本機安裝的功能清單。 功能必須出現在 [功能資料表](feature-table.md)的功能資料行中。 若要在本機安裝所有功能，請在命令列上使用 ADDLOCAL = ALL。 請勿將 ADDLOCAL = 全部輸入至 [屬性工作表](property-table.md)，因為這樣會產生無法正確移除的本機安裝套件。

## <a name="remarks"></a>備註

功能名稱會區分大小寫。 如果在清單中功能元件的 [元件資料表](component-table.md) 的 [屬性] 資料行中設定 SourceOnly 位旗標，該元件會安裝為 [從來源執行]。

安裝程式一律會依下列順序評估下列屬性：

1.  **ADDLOCAL**
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
12. [**FILEADDDEFAULT**](fileadddefault.md)

例如：

-   如果命令列指定： ADDLOCAL = ALL、ADDSOURCE = **MyFeature**，則所有功能都會先設定為執行本機，然後 **MyFeature** 設定為從來源執行。
-   如果命令列是： ADDSOURCE = ALL、ADDLOCAL =**MyFeature**、first **MyFeature** 設定為 run-LOCAL，則當 ADDSOURCE = ALL 進行評估時，包括 **MyFeature**) 在內的所有 (功能都會重設為從來源執行。

安裝程式在暫停的安裝期間，或在命令列上指定任何先前的屬性時，會將 [**預先**](preselected.md) 選取的屬性設定為 "1" 的值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer。 如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 




