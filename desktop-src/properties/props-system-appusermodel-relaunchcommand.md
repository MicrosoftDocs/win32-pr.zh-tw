---
description: 指定可透過 ShellExecute 執行的命令，以在應用程式釘選到工作列時啟動應用程式，或透過應用程式的捷徑清單啟動應用程式的新實例。
ms.assetid: 83aab060-0629-48e3-a2db-9ba96a8631e5
title: AppUserModel. RelaunchCommand
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cc2ce3783aa9ab3d76124b8d62f9d9d9ad2e1f5d4b92622716df111456dbabd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119554518"
---
# <a name="systemappusermodelrelaunchcommand"></a>AppUserModel. RelaunchCommand

指定可透過 [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) 執行的命令，以在應用程式釘選到工作列時啟動應用程式，或透過應用程式的捷徑清單啟動應用程式的新實例。

範例包括：


```
shell:::{ED228FDF-9EA8-4870-83B1-96B02CFE0D52}

virtualhost.exe /virtualapp:12345

notepad.exe
```



只有當視窗具有明確的應用程式使用者模型識別碼 (AppUserModelID)  ([System.AppUserModel.ID](./props-system-appusermodel-id.md)（透過 [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)) 設定）時，才會使用這個屬性。 如果視窗沒有明確的 AppUserModelID，則會忽略此屬性，並將視窗分組並釘選，就好像它是擁有它的進程的一部分一樣。 如需明確 AppUserModelIDs 的應用程式及其對工作列釘選效果的詳細資訊，請參閱 [應用程式使用者模型識別碼 (AppUserModelIDs) ](../shell/appids.md)。

這個屬性的目的是要讓想要提供非預設重新開機資訊的應用程式或視窗使用。

> [!Note]  
> [AppUserModel. RelaunchCommand]() 和 [AppUserModel. RelaunchDisplayNameResource](./props-system-appusermodel-relaunchdisplaynameresource.md) 一律必須一起設定。 如果未設定其中一個屬性，則不會使用這兩個屬性。

 

這個屬性（property）連同 [AppUserModel （RelaunchDisplayNameResource](./props-system-appusermodel-relaunchdisplaynameresource.md) ）和 [AppUserModel （RelaunchIconResource](./props-system-appusermodel-relaunchiconresource.md) ）可用來以視覺方式將視窗定義為使用者的應用程式。 這適用于裝載應用程式案例，其中單一主控制項實例會執行多個子應用程式。 例如，裝載數個虛擬化應用程式的虛擬機器可能會想要讓這些虛擬化應用程式以個別的應用程式顯示給使用者。 虛擬機器可以用明確的 AppUserModelID 和適當的重新開機屬性為每個視窗加上標籤，使其顯示為應用程式。 然後使用者可以將它們釘選到工作列，然後「重新開機」已釘選的實例。

> [!Note]  
> 如果設定了 [AppUserModel. PreventPinning](./props-system-appusermodel-preventpinning.md) ，就會忽略這個屬性。 這可讓應用程式藉由指派明確的 AppUserModelIDs 來控制其視窗的群組，但無法釘選這些視窗。

 

若要在視窗上設定此屬性，請使用 [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) 抓取視窗的屬性存放區，然後使用該抓取 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 物件的方法來設定該視窗的 [AppUserModel. RelaunchCommand]() 屬性。

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7 版

```
propertyDescription
   name = System.AppUserModel.RelaunchCommand
   shellPKey = PKEY_AppUserModel_RelaunchCommand
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 2
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
      IsInnate = false
```

## <a name="remarks"></a>備註

PKEY 值定義于 Propkey 中。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[應用程式使用者模型識別碼 (AppUserModelIDs) ](../shell/appids.md)
</dt> <dt>

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

 

 
