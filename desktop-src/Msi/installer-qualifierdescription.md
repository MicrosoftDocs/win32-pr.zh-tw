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
ms.openlocfilehash: c226f00d7f95b4585fa4a0713fb281011079cdc35c4e421254beec75db84d7db
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763578"
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
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa)
</dt> <dt>

[合格元件](qualified-components.md)
</dt> </dl>

 

 




