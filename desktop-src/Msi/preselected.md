---
description: 預先選取的屬性工作表示已選取功能，且不需要顯示選取對話方塊。相依於是否已安裝功能的條件運算式會使用這個值。
ms.assetid: 2bbab8b9-084a-4515-904c-d556d183d06e
title: 預先選取的屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a85f5c3248002fec776e45e9d7ad37550d3e16d7a5d76b098948b571b8c9c546
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042318"
---
# <a name="preselected-property"></a>預先選取的屬性

**預先** 選取的屬性工作表示已選取功能，且不需要顯示選取對話方塊。

相依於是否已安裝功能的條件運算式會使用這個值。 例如，您可以使用屬性來隱藏在已暫停的安裝繼續進行時，牽涉到特徵選取的任何對話方塊。

安裝程式在停用的安裝期間，或在命令列上指定了下列任何屬性時，會將 **預先** 選取的屬性設定為 "1" 的值。 如果 **預先** 選取的屬性已設定為1，安裝程式就不會使用 [Condition 資料表](condition-table.md) 來評估選取的功能。 您可以根據下列屬性來安裝功能。 安裝程式一律會以下列順序評估這些屬性：

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
12. [**FILEADDDEFAULT**](fileadddefault.md)

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式。 如需 Windows Installer 版本所需的最低 Windows service pack 相關資訊，請參閱[Windows Installer Run-Time 需求](windows-installer-portal.md)。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 




