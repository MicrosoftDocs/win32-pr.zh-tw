---
description: 將 MSIUSEREALADMINDETECTION 屬性設定為1，以要求安裝程式在設定 AdminUser 屬性時，使用實際的使用者資訊。
ms.assetid: eb0ed6e3-377b-40f4-afee-346a83e310cf
title: MSIUSEREALADMINDETECTION 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0989174f41bc4b58f89e440dd9852dfde6249a5c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995995"
---
# <a name="msiuserealadmindetection-property"></a>MSIUSEREALADMINDETECTION 屬性

將 **MSIUSEREALADMINDETECTION** 屬性設定為1，以要求安裝程式在設定 [**AdminUser**](adminuser.md) 屬性時，使用實際的使用者資訊。 在 Windows Vista 上執行時，特殊 [**許可權**](privileged.md) 和 **AdminUser** 相同。 作者應該在新的封裝中使用具有特殊 **許可權** 的屬性。 需要特殊 **許可權** 和 **AdminUser** 屬性的舊版封裝，可以藉由設定 **MSIUSEREALADMINDETECTION** 屬性來還原差異。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> <dt>

[Windows Installer 3.1 及更早版本不支援](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




