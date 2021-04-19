---
description: 具有特殊許可權的屬性會指出是否在較高許可權的內容中執行安裝。
ms.assetid: 483ab73a-3ff7-4111-a6b5-eac990d85bd7
title: 具有特殊許可權的屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5d28a7079e7ab12b9832447172f1b3b2c8650a8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991224"
---
# <a name="privileged-property"></a>具有特殊許可權的屬性

具有 **特殊許可權的屬性會** 指出是否在較高許可權的內容中執行安裝。 如果使用者具有系統管理員許可權、系統管理員已指派應用程式，或使用者和電腦原則 AlwaysInstallElevated 都設定為 true，則安裝程式會設定此屬性。

## <a name="default-value"></a>預設值

如果不允許使用者以較高的許可權安裝，安裝程式就不會設定此屬性。

## <a name="remarks"></a>備註

安裝程式套件的開發人員可以使用 [特殊 **許可權** ] 屬性，根據系統原則、使用者是系統管理員或系統管理員指派來進行安裝。

在 Windows Vista 上執行時，特殊 **許可權** 和 [**AdminUser**](adminuser.md) 相同。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer。 如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 




