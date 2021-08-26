---
description: 如果執行安裝的系統平臺支援隔離的元件，安裝程式會設定 RedirectedDLLSupport 屬性。
ms.assetid: 703489c4-cac4-442c-bd96-d3927491a864
title: RedirectedDLLSupport 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24da5990645d4c27120c3a010cc517475ba6e706c2fb41d69a024d15ca524549
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119979318"
---
# <a name="redirecteddllsupport-property"></a>RedirectedDLLSupport 屬性

如果執行安裝的系統平臺支援 [隔離的元件](isolated-components.md)，安裝程式會設定 **RedirectedDLLSupport** 屬性。

如果執行安裝的系統支援根據的 [隔離元件](isolated-components.md)，則安裝程式會將 **RedirectedDLLSupport** 屬性設定為1的值。本機檔案。 如果執行安裝的系統支援使用兩者進行隔離，則安裝程式會將 **RedirectedDLLSupport** 屬性設定為2的值。本機檔案或 Win32 並存元件。

**RedirectedDLLSupport** 屬性可以用來在 [InstallUISequence 資料表](installuisequence-table.md)或 [InstallExecuteSequence 資料表](installexecutesequence-table.md)中條件 [IsolateComponents 動作](isolatecomponents-action.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式。 如需 Windows Installer 版本所需的最低 Windows service pack 相關資訊，請參閱[Windows Installer Run-Time 需求](windows-installer-portal.md)。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 




