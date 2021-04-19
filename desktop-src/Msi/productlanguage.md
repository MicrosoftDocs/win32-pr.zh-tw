---
description: ProductLanguage 屬性會指定安裝程式應針對使用者介面中未撰寫至資料庫的任何字串使用的語言。
ms.assetid: 5d798825-c70b-4d5a-b88c-a9db40663f6a
title: ProductLanguage 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3199bd2fcef457b40ad98e52f50c595bc424f9a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993572"
---
# <a name="productlanguage-property"></a>ProductLanguage 屬性

**ProductLanguage** 屬性會指定安裝程式應針對使用者介面中未撰寫至資料庫的任何字串使用的語言。 這個屬性必須是數位語言識別項 (LANGID) 。 如果轉換變更了資料庫中使用者介面的語言，則也應該變更這個屬性的值，以反映新的語言。

此為必要屬性。

## <a name="remarks"></a>備註

**ProductLanguage** 屬性的值必須是 [[**範本摘要**](template-summary.md)] 屬性中所列的其中一種語言。

將封裝編寫為非語言相關時，請將 **ProductLanguage** 屬性設定為0，並使用 MS Shell Dlg 字型作為所有撰寫之對話方塊的文字樣式。 因為某些字型不支援所有字元集，所以您可以使用這個字型來確定文字已正確顯示在所有當地語系化版本的作業系統上。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer。 如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 




