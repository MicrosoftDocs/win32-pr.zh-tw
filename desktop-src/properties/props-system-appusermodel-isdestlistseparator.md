---
description: 在捷徑清單的 Tasks 區段中插入分隔符號。
ms.assetid: 6cee1c20-865c-4d53-98c5-5402855a0004
title: AppUserModel. IsDestListSeparator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf64c287f9a8623e283894b32a9e8b07f449d306d21d25e7c206158f4c69df87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118970867"
---
# <a name="systemappusermodelisdestlistseparator"></a>AppUserModel. IsDestListSeparator

在捷徑清單的 **Tasks** 區段中插入分隔符號。 在 [**IShellLink**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllinka) 物件上設定此屬性，並將其傳遞至 [**ICustomDestinationList：： AddUserTasks**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-addusertasks)。

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7 版

```
propertyDescription
   name = System.AppUserModel.IsDestListSeparator
   shellPKey = PKEY_AppUserModel_IsDestListSeparator
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 6
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
      IsInnate = false
```

## <a name="remarks"></a>備註

PKEY 值定義于 Propkey 中。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[System.AppUserModel.ID](./props-system-appusermodel-id.md)
</dt> <dt>

[propertyDescriptionList](./propdesc-schema-propertydescriptionlist.md)
</dt> <dt>

[propertyDescription](./propdesc-schema-propertydescription.md)
</dt> <dt>

[searchInfo](./propdesc-schema-searchinfo.md)
</dt> <dt>

[labelInfo](./propdesc-schema-labelinfo.md)
</dt> <dt>

[typeInfo](./propdesc-schema-typeinfo.md)
</dt> <dt>

[displayInfo](./propdesc-schema-displayinfo.md)
</dt> <dt>

[System.management.automation.aliasinfo](./propdesc-schema-aliasinfo.md)
</dt> <dt>

[stringFormat](./propdesc-schema-stringformat.md)
</dt> <dt>

[booleanFormat](./propdesc-schema-booleanformat.md)
</dt> <dt>

[>cultureinfo.numberformat](./propdesc-schema-numberformat.md)
</dt> <dt>

[dateTimeFormat](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[enumeratedList](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[枚舉](./propdesc-schema-enum.md)
</dt> <dt>

[enumRange](./propdesc-schema-enumrange.md)
</dt> <dt>

[image](./propdesc-schema-image.md)
</dt> <dt>

[drawControl](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[editControl](./propdesc-schema-editcontrol.md)
</dt> <dt>

[filterControl](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[queryControl](./propdesc-schema-querycontrol.md)
</dt> <dt>

[relatedPropertyInfo](./propdesc-schema-relatedpropertyinfo.md)
</dt> <dt>

[relatedProperty](./propdesc-schema-relatedproperty.md)
</dt> </dl>

 

 
