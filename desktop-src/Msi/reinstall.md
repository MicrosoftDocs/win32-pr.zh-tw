---
description: 重新安裝屬性的值是以逗號分隔的功能清單，這些功能是以要重新安裝的逗號分隔。 列出的功能必須存在於功能資料表的 [功能] 資料行中。 若要重新安裝所有功能，請使用命令列上的 [重新安裝 = 全部]。
ms.assetid: 14346fef-7923-4f30-bca8-96a29c0f820d
title: 重新安裝屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5147b4120968991aa3cb6caf438b7565281fc6f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976093"
---
# <a name="reinstall-property"></a>重新安裝屬性

**重新安裝** 屬性的值是以逗號分隔的功能清單，這些功能是以要重新安裝的逗號分隔。 列出的功能必須存在於 [功能](feature-table.md) 資料表的 [功能] 資料行中。 若要重新安裝所有功能，請使用命令列上的 [重新安裝 = 全部]。

## <a name="remarks"></a>備註

請注意，功能名稱會區分大小寫。

如果已設定 [ **重新安裝** ] 屬性，則也應該設定 [**REINSTALLMODE**](reinstallmode.md) 屬性，以指出要執行的重新安裝類型。 如果未設定 **REINSTALLMODE** 屬性，則根據預設，如果目前安裝的檔案是較小的版本 (或不存在) ，則預設會重新安裝目前安裝的所有檔案。 依預設，不會重新寫入任何登錄專案。

請注意，即使 **重新安裝** 已設定為 [全部]，也只會重新安裝先前已安裝的功能。 因此，如果已針對尚未安裝的產品設定 **重新安裝** ，則完全不會進行任何安裝動作。

安裝程式一律會依下列順序評估下列屬性：

1.  [**ADDLOCAL**](addlocal.md)
2.  [**刪除**](remove.md)
3.  [**ADDSOURCE**](addsource.md)
4.  [**ADDDEFAULT**](adddefault.md)
5.  **REINSTALL**
6.  [**做廣告**](advertise.md)
7.  [**COMPADDLOCAL**](compaddlocal.md)
8.  [**COMPADDSOURCE**](compaddsource.md)
9.  [**FILEADDLOCAL**](fileaddlocal.md)
10. [**FILEADDSOURCE**](fileaddsource.md)
11. [**FILEADDDEFAULT**](fileadddefault.md)

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

 

 




