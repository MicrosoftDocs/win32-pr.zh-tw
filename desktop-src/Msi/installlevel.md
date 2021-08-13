---
description: INSTALLLEVEL 屬性是選取功能的初始層級 &\# 0034;&\# 0034; 預設為安裝。
ms.assetid: 5051cc46-837a-4446-a54c-4bd4081a424c
title: INSTALLLEVEL 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e349e8d92a2c480866b04a1ca57885ffa1cdb230d8346b357318fa239ead72a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118629957"
---
# <a name="installlevel-property"></a>INSTALLLEVEL 屬性

**INSTALLLEVEL** 屬性是在預設情況下，選取 [開啟] 來安裝特徵的初始層級。 只有當 [功能資料表](feature-table.md) 的 [層級] 欄位中的值小於或等於目前的 INSTALLLEVEL 值時，才會安裝功能。 任何安裝的安裝層級都是由 **INSTALLLEVEL** 屬性指定，而且可以是從1到32767的整數。 如需安裝層級的進一步討論，請參閱 [功能表](feature-table.md)。

## <a name="default-value"></a>預設值

如果未指定任何值，則安裝層級預設為1。

## <a name="remarks"></a>備註

**INSTALLLEVEL** 屬性指定的安裝層級可以由下列屬性覆寫：

-   [**ADDLOCAL**](addlocal.md)
-   [**ADDSOURCE**](addsource.md)
-   [**ADDDEFAULT**](adddefault.md)
-   [**COMPADDLOCAL**](compaddlocal.md)
-   [**COMPADDSOURCE**](compaddsource.md)
-   [**FILEADDLOCAL**](fileaddlocal.md)
-   [**FILEADDSOURCE**](fileaddsource.md)
-   [**刪除**](remove.md)
-   [**REINSTALL**](reinstall.md)
-   [**做廣告**](advertise.md)

例如，不論 **INSTALLLEVEL** 屬性的值為何，設定 ADDLOCAL = all 都會在本機安裝所有功能。 如果 [功能資料表](feature-table.md) 中層級資料行的值為0，則不會安裝該功能，也不會顯示在 UI 中。

系統管理員可以藉由套用自訂轉換，在該功能的層級資料行中設定0，以永久停用功能。 自訂轉換的應用會防止安裝和顯示功能，即使使用者使用 UI 選取完整安裝，或在命令列上將 ADDLOCAL 設定為 [全部]。 請參閱 [自訂轉換範例](a-customization-transform-example.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式。 如需 Windows Installer 版本所需的最低 Windows service pack 相關資訊，請參閱[Windows Installer Run-Time 需求](windows-installer-portal.md)。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 




