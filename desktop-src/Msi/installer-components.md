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
ms.openlocfilehash: b8538e594ed02a1bc355ed4cf57db1befb1443e58d7afe2038b16e08eb9e4659
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118632406"
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
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MsiEnumComponents**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsa)
</dt> </dl>

 

 




