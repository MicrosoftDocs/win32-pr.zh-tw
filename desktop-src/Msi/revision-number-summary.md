---
description: 若為安裝套件，[修訂編號摘要] 屬性會包含安裝程式套件的封裝程式碼。
ms.assetid: 79702b44-846a-4672-8e22-9b6e3f4b4678
title: 修訂編號摘要屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e97df1eafec2d543be0f975b9f5daca7728267b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984836"
---
# <a name="revision-number-summary-property"></a>修訂編號摘要屬性

若為安裝套件，[ **修訂編號摘要** ] 屬性會包含安裝程式套件的 [*封裝程式碼*](p-gly.md) 。 如需封裝程式碼的詳細資訊，請參閱 [封裝程式碼](package-codes.md)。

針對轉換，[ **修訂編號摘要** ] 屬性會列出產品程式碼 guid 和版本的新的和原始產品以及升級程式碼 GUID。 清單會以分號分隔，如下所示。

「原始產品-程式碼原始產品版本;New-Product 程式碼新產品版本;Upgrade-Code "

針對 patch 封裝，[ **修訂編號摘要** ] 屬性會指定修補程式的 GUID 修補程式碼。 這可以緊接著套用此修補程式時要移除之過時修補程式的修補程式程式碼 Guid 清單。 系統會串連修補程式碼，而不使用分隔符號分隔清單中的 Guid。

* * Windows Installer 3.0： * * 如果 [MsiPatchSequence 資料表](msipatchsequence-table.md)中有排序資訊，Windows Installer 3.0 會使用資料表中的排序資訊，並忽略 **修訂編號摘要** 屬性中包含的過時修補程式清單。 如果封裝未包含 MsiPatchSequence 資料表，則 Windows Installer 3.0 仍可使用 [ **修訂編號摘要** ] 屬性中的過時修補程式資訊。

* * Windows Installer 2.0： * * 不支援 [MsiPatchSequence 資料表](msipatchsequence-table.md) 。 如果封裝未包含 MsiPatchSequence 資料表，則 Windows Installer 2.0 仍可使用 [ **修訂編號摘要** ] 屬性中的過時修補程式資訊。

這是必要的摘要屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[摘要屬性描述](summary-property-descriptions.md)
</dt> </dl>

 

 




