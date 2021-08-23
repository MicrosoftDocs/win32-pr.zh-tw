---
description: ComponentQualifiers 屬性是唯讀屬性，它會傳回 StringList 物件，以列舉指定元件的已註冊限定詞集合。
ms.assetid: 49b16c9a-ce84-42ff-af1d-f4ecf7dbe23a
title: ComponentQualifiers 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ComponentQualifiers
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: ff11302b87c144d59129b7041ab75129477e7925b3dd98ce7c740f0c4eda62e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118632602"
---
# <a name="installercomponentqualifiers-property"></a>ComponentQualifiers 屬性

**ComponentQualifiers** 屬性是唯讀屬性，它會傳回 [**StringList**](stringlist-object.md)物件，以列舉指定元件的已註冊限定詞集合。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
propVal = Installer.ComponentQualifiers
```



## <a name="property-value"></a>屬性值

表示 [元件](publishcomponent-table.md)類別目錄的字串 GUID。

## <a name="remarks"></a>備註

若要列舉限定詞，應用程式會使用 For Each 結構逐一查看 [**StringList**](stringlist-object.md) 物件。 因為不會排序限定詞，所以任何新的限定詞都會有任意的索引，這表示函式可以依照任何順序傳回限定詞。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa)
</dt> </dl>

 

 




