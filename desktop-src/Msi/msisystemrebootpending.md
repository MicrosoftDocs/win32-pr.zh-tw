---
description: 如果有暫止的作業要重新命名檔案，安裝程式會將 MsiSystemRebootPending 屬性的值設定為1。
ms.assetid: 8bbbf42e-fb55-4e5d-a574-2c3aaa87a73a
title: MsiSystemRebootPending 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec5db7550be3fa27b0ed272ff08d88a4cad915a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999631"
---
# <a name="msisystemrebootpending-property"></a>MsiSystemRebootPending 屬性

如果有暫止的作業要重新命名檔案，安裝程式會將 **MsiSystemRebootPending** 屬性的值設定為1。

封裝作者可以在這個屬性的 [LaunchCondition 資料表](launchcondition-table.md) 中建立條件，以防止在有作業暫止重新命名檔案的情況下安裝套件。 這可能是為了避免重新命名檔案所造成的作業系統重新開機。 安裝程式在所有需要重新開機系統的情況下，都不會設定 **MsiSystemRebootPending** 屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer 4.5。 如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> <dt>

[系統重新開機](system-reboots.md)
</dt> <dt>

[Windows Installer 3.1 及更早版本不支援](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




