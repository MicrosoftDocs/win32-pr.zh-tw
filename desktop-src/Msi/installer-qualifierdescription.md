---
description: 唯讀 QualifierDescription 屬性會傳回描述限定元件的文字字串。
ms.assetid: 43615bd9-824b-4b84-a8f2-eef30cc7619a
title: QualifierDescription 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.QualifierDescription
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8937e0a1fee89bb3ebe1b6402c94778bdd2a0915
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995460"
---
# <a name="installerqualifierdescription-property"></a>QualifierDescription 屬性

唯讀 **QualifierDescription** 屬性會傳回描述限定元件的文字字串。 這個可當地語系化的字串會編寫到 [PublishComponent 資料表](publishcomponent-table.md) 的 AppData 資料行中，而且可以向使用者顯示。 限定詞會區分相同元件的多個表單，例如以多種語言所執行的元件。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
propVal = Installer.QualifierDescription
```



## <a name="property-value"></a>屬性值

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa)
</dt> <dt>

[合格元件](qualified-components.md)
</dt> </dl>

 

 




