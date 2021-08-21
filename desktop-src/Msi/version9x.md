---
description: Version9X 屬性會提供 Windows 作業系統之9x 版本的版本號碼。這個屬性的值是整數： MajorVersion \* 100 + MinorVersion。
ms.assetid: 0a22de88-4958-46be-82c3-6465aec86d33
title: Version9X 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efbf76faef4ead06043e4824b6b8f0989a64e261b7c48e260c9c25fa58381cf0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119498998"
---
# <a name="version9x-property"></a>Version9X 屬性

**Version9X** 屬性會提供 Windows 作業系統之9x 版本的版本號碼。

這個屬性的值是整數： MajorVersion \* 100 + MinorVersion。 如果作業系統不是9x 版本，屬性會保持未定義。 如需詳細資訊，請參閱 [作業系統屬性值](operating-system-property-values.md)。

## <a name="remarks"></a>備註

條件運算式可以使用屬性名稱測試版本，也可以使用比較運算子來驗證版本。

所有屬性名稱都會區分大小寫。 請注意，名稱 **Version9X** 中的 X 為大寫。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式。 如需 Windows Installer 版本所需的最低 Windows service pack 相關資訊，請參閱[Windows Installer Run-Time 需求](windows-installer-portal.md)。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 




