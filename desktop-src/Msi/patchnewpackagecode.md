---
description: PATCHNEWPACKAGECODE 屬性會在修補期間更新系統管理映射的修訂編號摘要屬性。
ms.assetid: 5ca0058a-b4eb-48df-89eb-fbc7da7224e8
title: PATCHNEWPACKAGECODE 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb7c1c70c91ede5788258c67626cdf429df74e27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982081"
---
# <a name="patchnewpackagecode-property"></a>PATCHNEWPACKAGECODE 屬性

**PATCHNEWPACKAGECODE** 屬性會在修補期間更新系統管理映射的 [**修訂編號摘要**](revision-number-summary.md)屬性。 只有 .msp 檔中的轉換會設定這個屬性。 .Msp 檔必須包含將這個屬性加入至 [屬性工作表](property-table.md) 的轉換，並設定其值。 然後，安裝程式會將 **PATCHNEWPACKAGECODE** 的值寫入 [ **修訂編號摘要** ] 屬性。

## <a name="remarks"></a>備註

**PATCHNEWPACKAGECODE**、 [**PATCHNEWSUMMARYCOMMENTS**](patchnewsummarycomments.md)和 [**PATCHNEWSUMMARYSUBJECT**](patchnewsummarysubject.md)屬性是用來在修補程式安裝至系統管理映射時，更新摘要資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer。 如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 




