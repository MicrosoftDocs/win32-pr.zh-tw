---
description: Version9X 屬性可提供適用于9x 版本之 Windows 作業系統的版本號碼。這個屬性的值是整數： MajorVersion \* 100 + MinorVersion。
ms.assetid: 0a22de88-4958-46be-82c3-6465aec86d33
title: Version9X 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1df599629fdf978837a8f53df7d1faa4f476db1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991546"
---
# <a name="version9x-property"></a>Version9X 屬性

**Version9X** 屬性可提供適用于9x 版本之 Windows 作業系統的版本號碼。

這個屬性的值是整數： MajorVersion \* 100 + MinorVersion。 如果作業系統不是9x 版本，屬性會保持未定義。 如需詳細資訊，請參閱 [作業系統屬性值](operating-system-property-values.md)。

## <a name="remarks"></a>備註

條件運算式可以使用屬性名稱測試版本，也可以使用比較運算子來驗證版本。

所有屬性名稱都會區分大小寫。 請注意，名稱 **Version9X** 中的 X 為大寫。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer。 如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 




