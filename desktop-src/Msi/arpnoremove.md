---
description: 設定 ARPNOREMOVE 屬性會在移除產品的主控台中停用 [新增或移除程式] 功能。
ms.assetid: f86c1af8-c984-4075-9c6b-0a71000b01a1
title: ARPNOREMOVE 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d69e066aeb96861be220a40334d44bf55fe0569e855029d2a19399b56a1c205
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105428"
---
# <a name="arpnoremove-property"></a>ARPNOREMOVE 屬性

設定 **ARPNOREMOVE** 屬性會在移除產品的 **主控台** 中停用 [**新增或移除程式**] 功能。 針對 Windows 2000，這會從 **主控台** 中的 [**新增或移除程式**] 停用產品的 [**移除**] 按鈕。 針對較舊的作業系統，這會影響在 **主控台** 的 [**新增或移除程式**] 上，將產品從已安裝的產品清單中移除。

如果已設定 **ARPNOREMOVE** 屬性， [RegisterProduct 動作](registerproduct-action.md) 會在登錄機碼下寫入 "NoRemove" 值：

**HKLM** \\**軟體** \\**Microsoft** \\**Windows** \\**CurrentVersion** \\**卸載** \\ **{*產品金鑰*}**

設定 **ARPNOREMOVE** 屬性可防止在此機碼下寫入 UninstallString 值。 UnistallString 值是用來移除產品的命令列，而不是重新設定產品。

## <a name="remarks"></a>備註

例如，您可以在自訂轉換期間設定這個屬性，以防止使用者移除系統管理員自訂。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Vista 上的安裝程式4.0 或 Windows Installer 4.5 或更新版本。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式。 如需 Windows Installer 版本所需的最低 Windows service pack 相關資訊，請參閱[Windows Installer Run-Time 需求](windows-installer-portal.md)。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 




