---
description: 指定當使用者選擇將應用程式釘選到工作列或透過按鈕的捷徑清單啟動新實例時，在工作列上建立的快捷方式所使用的圖示。
ms.assetid: 3559d1f5-988c-41d9-ba9a-dfa4ba643ee2
title: AppUserModel. RelaunchIconResource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b43394bd5ee7dca6084526224dac268500f6881317215d63d6fc0e9a126c5b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118970837"
---
# <a name="systemappusermodelrelaunchiconresource"></a>AppUserModel. RelaunchIconResource

指定當使用者選擇將應用程式釘選到工作列或透過按鈕的捷徑清單啟動新實例時，在工作列上建立的快捷方式所使用的圖示。 這是用於工作列群組的圖示，會針對已釘選的應用程式顯示（無論應用程式是否正在執行）。 這應該以下列其中一種格式來指定：

-   標準資源格式，例如 "% systemdir% \\ system32 \\shell32.dll，-128"。 需要資源識別碼之前的 '-' 字元。 請勿在路徑字串的前方使用 ' @ ' 字元。
-   圖示檔的直接路徑，例如 "% programfiles% \\ Microsoft \\ 記事本 \\ 記事本 .ico、0"。 請注意，因為 .ico 檔案可以包含多個圖示資源，所以字串中必須有資源識別碼。 如果 .ico 檔案是單一映射，請使用 "0" (不含 '-' 字元) 作為資源識別碼。

[AppUserModel. RelaunchIconResource]() 是選擇性屬性。 如果未設定，則會使用重新開機命令的靶心圖表標 ([AppUserModel. RelaunchCommand](./props-system-appusermodel-relaunchcommand.md)) 。 不過，因為這可能會導致不想要的結果，所以強烈建議您透過這個屬性明確提供圖示。

只有當視窗具有明確的應用程式使用者模型識別碼 (AppUserModelID)  ([System.AppUserModel.ID](./props-system-appusermodel-id.md)（透過 [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)) 設定）時，才會使用這個屬性。 如果視窗沒有明確的 AppUserModelID (System.AppUserModel.ID) ，則會忽略此屬性，並將視窗分組並釘選，就好像它是其擁有進程的一部分一樣。 如需明確 AppUserModelIDs 及其對工作列釘選效果的詳細資訊，請參閱 [應用程式使用者模型識別碼 (AppUserModelIDs) ](../shell/appids.md)。 這個屬性的目的是要讓想要提供非預設重新開機資訊的應用程式或視窗使用。 如需詳細資訊，請參閱 [AppUserModel。 RelaunchCommand](./props-system-appusermodel-relaunchcommand.md)。

如果在視窗上設定了明確的 AppUserModelID，但是未設定此屬性，系統就會嘗試尋找具有相同 AppUserModelID 的快捷方式，並將快捷方式釘選到工作列以表示視窗。 如果找不到這種快捷方式，則會使用擁有它之進程的支援可執行檔。

> [!Note]  
> 如果設定了 [AppUserModel. PreventPinning](./props-system-appusermodel-preventpinning.md) ，就會忽略這個屬性。 這可讓應用程式藉由指派明確的 AppUserModelIDs 來控制其視窗的群組，但無法釘選這些視窗。

 

若要在視窗上設定此屬性，請使用 [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) 抓取視窗的屬性存放區，然後使用該抓取 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 物件的方法來設定該視窗的 [AppUserModel. RelaunchIconResource]() 屬性。

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81"></a>Windows 10，1703版、Windows 10、1607版、Windows 10、1511版、Windows 10、1507版、Windows 8。1

```
propertyDescription
   name = System.AppUserModel.RelaunchIconResource
   shellPKey = PKEY_AppUserModel_RelaunchIconResource
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 3
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = String
      IsInnate = false
```

## <a name="windows-8-windows-7"></a>Windows 8，Windows 7

```
propertyDescription
   name = System.AppUserModel.RelaunchIconResource
   shellPKey = PKEY_AppUserModel_RelaunchIconResource
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 3
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
      IsInnate = false
```

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

 

 
