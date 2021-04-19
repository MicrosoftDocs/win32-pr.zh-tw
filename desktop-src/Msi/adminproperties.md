---
description: AdminProperties 應該撰寫在屬性工作表中。
ms.assetid: 91dd58cf-6c8c-4d20-a829-c43301a30d7f
title: AdminProperties 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 739a0e29526ac7c6d9c094bc492cde1d04cdd0f8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000485"
---
# <a name="adminproperties-property"></a>AdminProperties 屬性

**AdminProperties** 應該撰寫在 [屬性工作表](property-table.md)中。 **AdminProperties** 的值是以分號分隔的屬性名稱清單。 安裝程式會在 [系統管理安裝](administrative-installation.md)時儲存這些列出屬性的值。 當使用者從系統管理映射安裝時，安裝會使用屬性的儲存值，而不是 .msi 檔案中的值。

## <a name="remarks"></a>備註

清單中的屬性名稱可以是大寫和小寫字母 (私用屬性) ，或) 全部大寫 (公用屬性。

這個屬性絕不能以分號結尾。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer。 如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 




