---
description: REMOVE 屬性的值是以逗號分隔的功能清單，要移除這些功能。
ms.assetid: 39f4609a-7bf8-42b3-b23e-0d6a40b69fd3
title: REMOVE 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8f46bcd5547abdefd67f98dff312bfdf1dff41e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999702"
---
# <a name="remove-property"></a>REMOVE 屬性

**REMOVE** 屬性的值是以逗號分隔的功能清單，要移除這些功能。 功能必須出現在 [功能資料表](feature-table.md)的功能資料行中。 請注意，如果您在命令列上使用 REMOVE = ALL，安裝程式會移除安裝層級大於0的所有功能。 在此情況下，安裝程式不會移除安裝層級為0的功能。 如需安裝層級功能的詳細資訊，請參閱 [功能表](feature-table.md)。

## <a name="remarks"></a>備註

若要判斷產品是否已設定為完全卸載，封裝作者可以使用條件運算式來檢查是否要移除 = 全部。 請注意，如果產品是藉由將其最上層功能設定為 [不存在] 來移除，則 [ **移除** ] 屬性在 [InstallValidate 動作](installvalidate-action.md)之後可能不會完全相同。 這表示任何相依于 REMOVE = ALL 的自訂動作都必須在 InstallValidate 之後排序。 如需詳細資訊，請參閱 [在移除期間要執行的調節動作](conditioning-actions-to-run-during-removal.md)。 請注意，功能名稱會區分大小寫。

安裝程式一律會依下列順序評估下列屬性：

1.  [**ADDLOCAL**](addlocal.md)
2.  **刪除**
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

例如，如果命令列指定 ADDLOCAL = ALL、ADDSOURCE = MyFeature，則所有功能都會先設定為執行本機，然後 MyFeature 設定為從來源執行。 如果命令列是 ADDSOURCE = ALL、ADDLOCAL = MyFeature、first MyFeature 設定為 local local，則當 ADDSOURCE = ALL 進行評估時，所有功能 (包括 MyFeature) 都會重設為從來源執行。

安裝程式在停用的安裝期間，或在命令列上指定了上述任何屬性時，會將 [**預先**](preselected.md) 選取的屬性設定為 "1" 的值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer。 如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 




