---
description: 您可以設定 MSIDEPLOYMENTCOMPLIANT 屬性，向安裝程式指出封裝已撰寫並測試，以符合 Windows Vista 中 (UAC) 的使用者帳戶控制。
ms.assetid: 7ee0dc56-bb9d-4a6e-aa3e-ae4c83f583d7
title: MSIDEPLOYMENTCOMPLIANT 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cd1cea551c68858b4286e168862488e6d3361bfc501001b491ec9e655537185
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077948"
---
# <a name="msideploymentcompliant-property"></a>MSIDEPLOYMENTCOMPLIANT 屬性

您可以設定 **MSIDEPLOYMENTCOMPLIANT** 屬性，向安裝程式指出封裝已撰寫並測試，以符合 Windows Vista 中 (UAC) 的 [*使用者帳戶控制*](u-gly.md)。 如果未設定這個屬性，安裝程式會判斷套件是否符合 Windows Vista 上的 UAC。

如需 uac 和 Windows Installer 的詳細資訊，請參閱[使用 Windows Installer 搭配 uac](using-windows-installer-with-uac.md)和[套件的指導方針](guidelines-for-packages.md)。

**Windows Installer 3.1、Windows Installer 3.0 和 Windows Installer 2.0：** 忽略這個屬性。 只有 Windows Vista 中的 Windows Installer 4.0 才會使用這個屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 如需 Windows Installer 版本所需的最低 service pack 資訊，請參閱[Windows Installer Run-Time 需求](windows-installer-portal.md)。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> <dt>

[Windows Installer 3.1 及更早版本不支援](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




