---
description: 指定當使用者選擇將應用程式釘選到工作列或透過按鈕的捷徑清單啟動新實例時，在工作列上建立的快捷方式所使用的顯示名稱。
ms.assetid: a149838b-83b6-44ce-b705-e2804efb3d31
title: AppUserModel. RelaunchDisplayNameResource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d79c22d0ccecb8bac86fe5ca3636ed10ed2ca50b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104192842"
---
# <a name="systemappusermodelrelaunchdisplaynameresource"></a>AppUserModel. RelaunchDisplayNameResource

指定當使用者選擇將應用程式釘選到工作列或透過按鈕的捷徑清單啟動新實例時，在工作列上建立的快捷方式所使用的顯示名稱。 這個屬性的值必須是下列其中一項：

-   間接資源字串，例如 "@% systemdir% \\ system32 \\shell32.dll，-19263"。 請注意，必須有 ' @ ' 字元，才能區別純文字字串中的間接字串 (下一個點符段落) 所述。 這個間接字串是由二進位檔案和該二進位檔中所包含之字串的資源識別碼所組成。 強烈建議您使用這個間接字串表單，以確保當系統語言透過多語系消費者介面 (MUI) 變更時，顯示名稱會適當地變更。 需要資源識別碼之前的 '-' 字元。
-   未指向資源的純文字字串。 只有當顯示名稱是動態計算，或從不支援 MUI 的資料來源取得時，才應該使用此方法。 例如，如果應用程式在裝置連接到電腦時出現，則字串可能是裝置的名稱（例如 "Microsoft Zune"）。

> [!Note]  
> [AppUserModel. RelaunchCommand](./props-system-appusermodel-relaunchcommand.md) 和 [AppUserModel. RelaunchDisplayNameResource]() 一律必須一起設定。 如果未設定其中一個屬性，則不會使用這兩個屬性。

 

只有當視窗具有明確的應用程式使用者模型識別碼 (AppUserModelID)  ([System.AppUserModel.ID](./props-system-appusermodel-id.md)（透過 [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)) 設定）時，才會使用這個屬性。 如果視窗沒有明確的 AppUserModelID，則會忽略此屬性，並將視窗分組並釘選，就好像它是擁有它的進程的一部分一樣。 如需明確 AppUserModelIDs 及其對工作列釘選效果的詳細資訊，請參閱 [應用程式使用者模型識別碼 (AppUserModelIDs) ](../shell/appids.md)。 這個屬性的目的是要讓想要提供非預設重新開機資訊的應用程式或視窗使用。 如需詳細資訊，請參閱 [AppUserModel。 RelaunchCommand](./props-system-appusermodel-relaunchcommand.md)。

> [!Note]  
> 如果設定了 [AppUserModel. PreventPinning](./props-system-appusermodel-preventpinning.md) ，就會忽略這個屬性。 這可讓應用程式藉由指派明確的 AppUserModelIDs 來控制其視窗的群組，但無法釘選這些視窗。

 

若要在視窗上設定此屬性，請使用 [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) 抓取視窗的屬性存放區，然後使用該抓取 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 物件的方法來設定該視窗的 [AppUserModel. RelaunchDisplayNameResource]() 屬性。

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7 版

```
propertyDescription
   name = System.AppUserModel.RelaunchDisplayNameResource
   shellPKey = PKEY_AppUserModel_RelaunchDisplayNameResource
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 4
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

 

 
