---
description: '[唯讀元件] 屬性會傳回 StringList 物件，以列舉所有產品的已安裝元件集合。'
ms.assetid: c84e4329-428a-440a-bd65-097588a86932
title: 安裝程式. Components 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Components
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e6767be5182b15836c071bf8b00ed8441f6031dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997775"
---
# <a name="installercomponents-property"></a>安裝程式. Components 屬性

[唯讀 **元件** ] 屬性會傳回 [**StringList**](stringlist-object.md) 物件，以列舉所有產品的已安裝元件集合。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
propVal = Installer.Components
```



## <a name="property-value"></a>屬性值

## <a name="remarks"></a>備註

若要列舉元件，應用程式可以使用 For Each 結構來逐一查看 [**StringList**](stringlist-object.md) 物件。 因為不會排序元件，所以任何新元件都有任意的索引。 這表示函數可以依任何順序傳回元件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MsiEnumComponents**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsa)
</dt> </dl>

 

 




