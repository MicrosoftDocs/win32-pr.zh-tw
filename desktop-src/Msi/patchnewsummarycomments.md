---
description: PATCHNEWSUMMARYCOMMENTS 屬性會在修補期間更新系統管理安裝的留言摘要屬性。
ms.assetid: 555813d8-6cb2-4b93-aa01-32d30b75b3d5
title: PATCHNEWSUMMARYCOMMENTS 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eef7a67b960b41e55caf5251a33ac6d3198147b92bcab895a2ca711af330acd9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074778"
---
# <a name="patchnewsummarycomments-property"></a>PATCHNEWSUMMARYCOMMENTS 屬性

**PATCHNEWSUMMARYCOMMENTS** 屬性會在修補期間更新系統管理安裝的 [**留言摘要**](comments-summary.md)屬性。 只有 .msp 檔中的轉換會設定這個屬性。 .Msp 檔必須包含將這個屬性加入至 [屬性工作表](property-table.md) 的轉換，並設定其值。 然後，安裝程式會將 **PATCHNEWSUMMARYCOMMENTS** 的值寫入 [ [**修訂編號摘要**](revision-number-summary.md) ] 屬性。

## <a name="remarks"></a>備註

[**PATCHNEWPACKAGECODE**](patchnewpackagecode.md)、 **PATCHNEWSUMMARYCOMMENTS** 和 [**PATCHNEWSUMMARYSUBJECT**](patchnewsummarysubject.md)屬性是用來在修補程式安裝至系統管理映射時，更新摘要資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式。 如需 Windows Installer 版本所需的最低 Windows service pack 相關資訊，請參閱[Windows Installer Run-Time 需求](windows-installer-portal.md)。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 




