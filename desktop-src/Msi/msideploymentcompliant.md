---
description: 您可以設定 MSIDEPLOYMENTCOMPLIANT 屬性，向安裝程式指出封裝已撰寫並測試，以符合 Windows Vista (UAC) 的使用者帳戶控制。
ms.assetid: 7ee0dc56-bb9d-4a6e-aa3e-ae4c83f583d7
title: MSIDEPLOYMENTCOMPLIANT 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a965b7dce941a3d651e2f9f32e3d8f4993ded33
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994343"
---
# <a name="msideploymentcompliant-property"></a>MSIDEPLOYMENTCOMPLIANT 屬性

您可以設定 **MSIDEPLOYMENTCOMPLIANT** 屬性，向安裝程式指出封裝已撰寫並測試，以符合 Windows VISTA (UAC) 的 [*使用者帳戶控制*](u-gly.md) 。 如果未設定此屬性，安裝程式會判斷套件是否符合 Windows Vista 上的 UAC。

如需 UAC 和 Windows Installer 的詳細資訊，請參閱 [使用 Windows Installer 搭配 uac](using-windows-installer-with-uac.md) 和 [套件的指導方針](guidelines-for-packages.md)。

**Windows Installer 3.1、Windows Installer 3.0 和 Windows Installer 2.0：** 忽略這個屬性。 只有 Windows Vista 中的 Windows Installer 4.0 才會使用這個屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 如需 Windows Installer 版本所需的最低 service pack 資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> <dt>

[Windows Installer 3.1 及更早版本不支援](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




