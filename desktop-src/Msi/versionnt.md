---
description: 如果作業系統不是 Windows NT、Windows 2000、Windows XP、Windows Vista、Windows Server 2008 或 Windows 7，安裝程式會將 VersionNT 屬性設定為作業系統的版本號碼。
ms.assetid: 49005783-0bcb-458e-8266-56e6ea6afb43
title: VersionNT 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61ce8d7d5c738be3b2fd51f2ca3054b8800d4c40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995328"
---
# <a name="versionnt-property"></a>VersionNT 屬性

如果作業系統不是 Windows NT、Windows 2000、Windows XP、Windows Vista、Windows Server 2008 或 Windows 7，安裝程式會將 **VersionNT** 屬性設定為作業系統的版本號碼。 此值為整數： MajorVersion \* 100 + MinorVersion。

相依于作業系統的條件陳述式可以使用此屬性。

另請參閱 [作業系統屬性值](operating-system-property-values.md)。

## <a name="remarks"></a>備註

條件運算式可以使用屬性名稱來測試 Windows NT、Windows 2000 或 Windows XP，或可使用比較運算子來驗證版本。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Installer 在 Windows Server 2003 或 Windows XP 上，請參閱 Windows Installer Run-Time Windows Installer 版本所需的最低 Windows service pack 相關資訊的 [需求](windows-installer-portal.md) 。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 




