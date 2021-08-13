---
description: MSIFASTINSTALL 屬性可以用來減少安裝大型 Windows Installer 套件所需的時間。
ms.assetid: 011668da-da04-4b80-989e-192b0daa3060
title: MSIFASTINSTALL 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd28c731d34e769f0612acc12586349247231bce663036d3577f41df6a7256f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118628499"
---
# <a name="msifastinstall-property"></a>MSIFASTINSTALL 屬性

**MSIFASTINSTALL** 屬性可以用來減少安裝大型 Windows Installer 套件所需的時間。 您可以在命令列或 [屬性](property-table.md) 表中設定屬性，以設定使用者或開發人員所判斷的作業不是安裝的必要條件。

**MSIFASTINSTALL** 屬性的值可以是下列值的組合。



| 值 | 意義                                                                      |
|-------|------------------------------------------------------------------------------|
| 0     | 預設值                                                                |
| 1     | 此安裝不會儲存任何系統還原點。                      |
| 2     | 只執行檔案 [成本](file-costing.md) ，並略過檢查其他成本。 |
| 4     | 減少進度訊息的頻率。                                   |



 

**[Windows Installer 4.5 或更早版本](not-supported-in-windows-installer-4-5.md)：** 不支援。 從 Windows Installer 5.0 開始，可以使用這個屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 如需 Windows Installer 版本所需的最低 Windows service pack 相關資訊，請參閱[Windows Installer Run-Time 需求](windows-installer-portal.md)。<br/> |



 

 




