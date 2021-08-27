---
description: MsiNetAssemblySupport 屬性指出電腦是否支援通用語言執行時間元件。
ms.assetid: 32f4f971-8e42-46b0-96e4-b3505abd2314
title: MsiNetAssemblySupport 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2d135fcc9eb301d3624586318fdc0d5dbbc534c5771ee89d4ae625af78b0782
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118944901"
---
# <a name="msinetassemblysupport-property"></a>MsiNetAssemblySupport 屬性

**MsiNetAssemblySupport** 屬性指出電腦是否支援通用語言執行時間元件。 在支援通用語言執行時間元件的系統上，安裝程式會將 **MsiNetAssemblySupport** 的值設定為 Fusion.dll 的檔案版本。 如果作業系統不支援通用語言執行時間元件，安裝程式就不會設定這個屬性。 當使用者電腦上並存安裝多個版本的 Fusion.dll 時，這個屬性會設定為最新版本的 Fusion.dll 檔案。 例如，如果 .NET Framework version v1.0.3705 (Fusion.dll version 1.0.3705.15) 和 .NET Framework version 1.1.4322 (Fusion.dll version 1.1.4322.314) 會並存安裝， **MsiNetAssemblySupport** 屬性會設定為1.1.4322.314。 如需詳細資訊，請參閱 [元件](assemblies.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式。 如需 Windows Installer 版本所需的最低 Windows service pack 相關資訊，請參閱[Windows Installer Run-Time 需求](windows-installer-portal.md)。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 




