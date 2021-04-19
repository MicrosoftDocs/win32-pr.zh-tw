---
description: 如果使用者具有系統管理員許可權，則安裝程式會設定此屬性。
ms.assetid: 2e7fd269-bd5f-40b7-b123-36b9c783a917
title: AdminUser 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11651f0d7103edabbcf7b40087db91f999b1a5b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999741"
---
# <a name="adminuser-property"></a>AdminUser 屬性

如果使用者具有系統管理員許可權，則安裝程式會設定此屬性。

**Windows Server 2008 和 Windows Vista：****AdminUser** 屬性與具有特殊 [**許可權**](privileged.md)的屬性相同。 作者應該使用具特殊 **許可權** 的屬性。 如果使用者具有系統管理員許可權、系統管理員已指派應用程式，或使用者和電腦原則 AlwaysInstallElevated 都設定為 true，則安裝程式會設定這些屬性。

## <a name="remarks"></a>備註

這些屬性之間的差異可能已用於某些舊版封裝中。 例如， **AdminUser** 可能已在條件陳述式中使用，而不是特殊 [**許可權**](privileged.md) ，因為如果使用者是系統管理員，則安裝程式只會設定 **AdminUser** 屬性。 如果使用者是系統管理員，或原則可讓使用者以較高的許可權安裝，則安裝程式會設定具有 **特殊許可權的屬性。**

**Windows Server 2008 和 Windows Vista：** 不支援。 具有特殊 [**許可權**](privileged.md) 的和 **AdminUser** 相同。 需要特殊 **許可權** 和 **AdminUser** 屬性的封裝，可以藉由設定 [**MSIUSEREALADMINDETECTION**](msiuserealadmindetection.md) 屬性來還原差異。

如需詳細資訊，請參閱以 [較高的許可權針對非系統管理員](installing-a-package-with-elevated-privileges-for-a-non-admin.md)和具 [**特殊許可權**](privileged.md) 的屬性安裝套件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Vista 或 Windows Server 2008 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer。 如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 




