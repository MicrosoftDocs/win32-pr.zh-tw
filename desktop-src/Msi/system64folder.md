---
description: 安裝程式會將 System64Folder 屬性設定為預先定義之 System64 資料夾的完整路徑。 現有的 System64Folder 屬性會設定為對應的32位資料夾。
ms.assetid: ce25c95e-cff5-44ec-81cb-b3104fb9b987
title: System64Folder 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d586451ab596f5b480c74f382659596128a12c041596dec3c530b18307af2820
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119500428"
---
# <a name="system64folder-property"></a>System64Folder 屬性

安裝程式會將 **System64Folder** 屬性設定為預先定義之 System64 資料夾的完整路徑。 現有的 **System64Folder** 屬性會設定為對應的32位資料夾。

## <a name="remarks"></a>備註

安裝程式會在64位 Windows 上設定這個屬性。 例如，在64位 Windows 上，此值可能是 C： \\ Window \\ System32。 這個屬性不會用於32位 Windows。

此資料夾通常是 Windows 資料夾的子目錄。 不過，它會在設定共用 Windows 時位於伺服器上。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式。 如需 Windows Installer 版本所需的最低 Windows service pack 相關資訊，請參閱[Windows Installer Run-Time 需求](windows-installer-portal.md)。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 




