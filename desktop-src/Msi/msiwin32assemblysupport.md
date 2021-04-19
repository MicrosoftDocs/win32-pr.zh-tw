---
description: MsiWin32AssemblySupport 屬性指出電腦是否支援 Win32 元件。
ms.assetid: 037202b6-41e4-4631-abbe-11291a5e5000
title: MsiWin32AssemblySupport 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99ab0c0e11d9e8a4b98503268c3a2c7ef67341c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106980147"
---
# <a name="msiwin32assemblysupport-property"></a>MsiWin32AssemblySupport 屬性

**MsiWin32AssemblySupport** 屬性指出電腦是否支援 Win32 元件。 在支援 Win32 元件的系統上，安裝程式會將 **MsiWin32AssemblySupport** 的值設定為 sxs.dll 的檔案版本。 如果作業系統不支援 Win32 元件，安裝程式就不會設定這個屬性。 如需詳細資訊，請參閱 [元件](assemblies.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer。 如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 




