---
description: 檔案或媒體的取得日期。
ms.assetid: 7c673d21-5243-4e41-91df-c5d84aaf620a
title: System. DateAcquired
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1a78ae9ccfe938551ab6c4a265972e48c3aad1c1791f02cfa933c583c6d4b0d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119599178"
---
# <a name="systemdateacquired"></a>System. DateAcquired

檔案或媒體的取得日期。 這個屬性與特定使用者或使用者群組有關。 例如，這項資料是用來做為虛擬資料夾 **新音樂** 的主要排序軸，可讓使用者流覽其集合的最新新增專案。

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7 版

```
propertyDescription
   name = System.DateAcquired
   shellPKey = PKEY_DateAcquired
   formatID = 2CBAA8F5-D81F-47CA-B17A-F8D822300131
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = DateTime
```

## <a name="windows-vista"></a>Windows Vista

```
propertyDescription
   name = System.DateAcquired
   shellPKey = PKEY_DateAcquired
   formatID = 2CBAA8F5-D81F-47CA-B17A-F8D822300131
   propID = 100
   SearchInfo
      IsColumn = true
   typeInfo
      type = DateTime
```

## <a name="remarks"></a>備註

PKEY 值定義于 Propkey 中。

[DateAcquired]() 會以值的形式儲存在檔案的主要資料流程中，但不一定會存在。 在這些情況下，取得日期可以根據其他已知的內容日期來近似值。 元資料處理程式應該使用一組規則來決定要傳回的日期。 下列範例示範音樂檔案的這項工作。

-   針對已購買的音樂，如果未取得任何日期，則應該使用檔案的建立時間。 不過，下載提供者應該在檔案中設定 [DateAcquired]() 屬性。
-   若為使用者或群組「已翻錄」 (將音樂或影片從 CD 或 DVD 複製到硬碟) 的音樂檔案，則取得日期應該是動作發生的日期。 例如， [WM/EncodingTime](../wmp/wm-encodingtime-attribute.md) 屬性。
-   若為從另一個位置複製的音樂，則應該使用檔案的建立時間做為取得日期。

[DateAcquired]()的範例是從相機取得圖片或在線上購買音樂時的日期和時間。 這與 [DateImported](./props-system-dateimported.md)不同。

## <a name="related-topics"></a>相關主題

<dl> <dt>

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

[drawControl](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[editControl](./propdesc-schema-editcontrol.md)
</dt> <dt>

[filterControl](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[queryControl](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
