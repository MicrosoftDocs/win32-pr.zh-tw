---
description: PATCHNEWSUMMARYSUBJECT 屬性會在修補期間更新系統管理映射的 [主體摘要] 屬性。
ms.assetid: 8aee1905-59a4-4818-b073-4bc401a6963d
title: PATCHNEWSUMMARYSUBJECT 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 912fe9ea21605625135b385a400fd5136c993c1d0dd0e3bfadd6a2b6699d21e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926163"
---
# <a name="patchnewsummarysubject-property"></a>PATCHNEWSUMMARYSUBJECT 屬性

**PATCHNEWSUMMARYSUBJECT** 屬性會在修補期間更新系統管理映射的 [[**主體摘要**](subject-summary.md)] 屬性。 只有 .msp 檔中的轉換會設定這個屬性。 .Msp 檔必須包含將這個屬性加入至 [屬性工作表](property-table.md) 的轉換，並設定其值。 然後，安裝程式會將 **PATCHNEWSUMMARYSUBJECT** 的值寫入 [ [**修訂編號摘要**](revision-number-summary.md) ] 屬性。

## <a name="remarks"></a>備註

[**PATCHNEWPACKAGECODE**](patchnewpackagecode.md)、 [**PATCHNEWSUMMARYCOMMENTS**](patchnewsummarycomments.md)和 **PATCHNEWSUMMARYSUBJECT** 屬性是用來在修補程式安裝至系統管理映射時，更新摘要資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式。 如需 Windows Installer 版本所需的最低 Windows service pack 相關資訊，請參閱[Windows Installer Run-Time 需求](windows-installer-portal.md)。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 




