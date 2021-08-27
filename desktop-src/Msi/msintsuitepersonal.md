---
description: 在 Windows xp 和更新版本的作業系統上，如果作業系統是 Windows XP Home Edition，安裝程式會將 MsiNTSuitePersonal 屬性設定為1。
ms.assetid: 324a4c45-bd64-4361-90ba-6a0554a9c5ef
title: MsiNTSuitePersonal 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c946b707e0d66a2c5bd3cd9cb6bf75828be9dd8f21e0e81080910a9fac73d353
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118944489"
---
# <a name="msintsuitepersonal-property"></a>MsiNTSuitePersonal 屬性

在 Windows xp 和更新版本的作業系統上，如果作業系統是 Windows XP Home Edition，安裝程式會將 **MsiNTSuitePersonal** 屬性設定為1。 只有在 \_ \_ [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) 結構中設定了 VER SUITE 個人旗標時，安裝程式才會將這個屬性設定為1。 否則，安裝程式不會設定這個屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式。 如需 Windows Installer 版本所需的最低 Windows service pack 相關資訊，請參閱[Windows Installer Run-Time 需求](windows-installer-portal.md)。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 
