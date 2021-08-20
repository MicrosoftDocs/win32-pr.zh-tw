---
description: 安裝程式會將 SystemFolder 屬性設定為系統資料夾的完整路徑。
ms.assetid: 23883638-8d3d-4c2a-8ebf-0c306cf01e05
title: SystemFolder 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1567942e981af161654d41988ef797b64116af5cdb25e07a3d4f1465fc4ce975
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118142006"
---
# <a name="systemfolder-property"></a>SystemFolder 屬性

安裝程式會將 **SystemFolder** 屬性設定為系統資料夾的完整路徑。

## <a name="remarks"></a>備註

安裝程式會設定這個屬性。 例如，在32位 Windows 值可能是 C： \\ Windows \\ System32。 在64位 Windows 上，此值可能是 C： \\ Windows \\ SysWow64。

此資料夾通常是 Windows 資料夾的子目錄。 不過，它會在設定共用 Windows 時位於伺服器上。

這是本機資料夾，即使是針對共用 Windows 進行設定亦同。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式。 如需 Windows Installer 版本所需的最低 Windows service pack 相關資訊，請參閱[Windows Installer Run-Time 需求](windows-installer-portal.md)。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 




