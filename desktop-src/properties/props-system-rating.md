---
description: 使用介於1到99之間的整數值的評等系統。 這是 Windows Vista Shell 所使用的分級系統。
ms.assetid: a6288d29-1ef3-4da1-bd30-577336ab6817
title: 系統評分
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9adc62e69ced0f82426f19badb1aebef0453084a9b951b749aed256aa64820a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119598128"
---
# <a name="systemrating"></a>系統評分

使用介於1到99之間的整數值的評等系統。 這是 Windows Vista Shell 所使用的分級系統。

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7 版

```
propertyDescription
   name = System.Rating
   shellPKey = PKEY_Rating
   formatID = 64440492-4C8B-11D1-8B70-080036B11A03
   propID = 9
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt32
      EnumeratedList
         UseValueForDefault = True
         enumRange
            name = OneStar
            minValue = 1
            setValue = 1
            defineMaxValue = 12
            text = 1 Star
            defineToken = RATING_ONE_STAR
         enumRange
            name = TwoStars
            minValue = 13
            setValue = 25
            defineMaxValue = 37
            text = 2 Stars
            defineToken = RATING_TWO_STARS
         enumRange
            name = ThreeStars
            minValue = 38
            setValue = 50
            defineMaxValue = 62
            text = 3 Stars
            defineToken = RATING_THREE_STARS
         enumRange
            name = FourStars
            minValue = 63
            setValue = 75
            defineMaxValue = 87
            text = 4 Stars
            defineToken = RATING_FOUR_STARS
         enumRange
            name = FiveStars
            minValue = 88
            setValue = 99
            defineMaxValue = 99
            text = 5 Stars
            defineToken = RATING_FIVE_STARS
         enumRange
            name
            minValue = 100
```

## <a name="windows-vista"></a>Windows Vista

```
propertyDescription
   name = System.Rating
   shellPKey = PKEY_Rating
   formatID = 64440492-4C8B-11D1-8B70-080036B11A03
   propID = 9
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt32
      EnumeratedList
         UseValueForDefault = True
         enumRange
            minValue = 0
            defineMinName = RATING_UNRATED_MIN
            setValue = 0
            defineSetName = RATING_UNRATED_SET
            defineMaxValue = 0
            defineMaxName = RATING_UNRATED_MAX
            text = Unrated
         enumRange
            minValue = 1
            defineMinName = RATING_ONE_STAR_MIN
            setValue = 1
            defineSetName = RATING_ONE_STAR_SET
            defineMaxValue = 12
            defineMaxName = RATING_ONE_STAR_MAX
            text = 1 Star
         enumRange
            minValue = 13
            defineMinName = RATING_TWO_STARS_MIN
            setValue = 25
            defineSetName = RATING_TWO_STARS_SET
            defineMaxValue = 37
            defineMaxName = RATING_TWO_STARS_MAX
            text = 2 Stars
         enumRange
            minValue = 38
            defineMinName = RATING_THREE_STARS_MIN
            setValue = 50
            defineSetName = RATING_THREE_STARS_SET
            defineMaxValue = 62
            defineMaxName = RATING_THREE_STARS_MAX
            text = 3 Stars
         enumRange
            minValue = 63
            defineMinName = RATING_FOUR_STARS_MIN
            setValue = 75
            defineSetName = RATING_FOUR_STARS_SET
            defineMaxValue = 87
            defineMaxName = RATING_FOUR_STARS_MAX
            text = 4 Stars
         enumRange
            minValue = 88
            defineMinName = RATING_FIVE_STARS_MIN
            setValue = 99
            defineSetName = RATING_FIVE_STARS_SET
            defineMaxValue = 99
            defineMaxName = RATING_FIVE_STARS_MAX
            text = 5 Stars
         enumRange
            minValue = 100
```

## <a name="remarks"></a>備註

PKEY 值定義于 Propkey 中。

若要與使用值介於1到5之間的分級系統相容，請參閱 [SimpleRating](./props-system-simplerating.md)屬性。 不過請注意，SimpleRating 不會在 Windows Vista Shell 中使用。

下表說明 Shell UI 中所使用的星星評等系統，其代表的是 [system. 評分]() 值。



| 系統評分 | 星級評等 |
|---------------|-------------|
| 1-12          | 1 顆星      |
| 13-37         | 2 顆星     |
| 38-62         | 3 顆星     |
| 63-87         | 4 顆星     |
| 88-99         | 5 顆星     |



 

當使用者在 UI 中選擇星狀分級值來評分專案時，系統會指派實際的 [系統評分]() 值，如下表所示：



| 星級評等 | 透過 UI 指派的值 |
|-------------|---------------------------|
| 1 顆星      | 1                         |
| 2 顆星     | 25                        |
| 3 顆星     | 50                        |
| 4 顆星     | 75                        |
| 5 顆星     | 99                        |



 

如果您的檔案有 [SimpleRating](./props-system-simplerating.md) 值，而不是 [system. 評分]() 值，請使用下表來轉換和指定 system.object 的值。



| System. SimpleRating | 系統評分 |
|---------------------|---------------|
| 1                   | 1             |
| 2                   | 25            |
| 3                   | 50            |
| 4                   | 75            |
| 5                   | 99            |



 

如果您的檔案同時具有 system.string 和[SimpleRating](./props-system-simplerating.md)保存值，請一律在直接要求時[使用 system.]()分級值，而不需參考 SimpleRating。

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

 

 
