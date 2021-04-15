---
description: 您可以使用 PropertyItem 物件的協助來儲存和取出影像中繼資料。 PropertyItem 物件的類型資料成員會指定儲存在相同 PropertyItem 物件之值資料成員中值的資料類型。
ms.assetid: d05cdf42-4b30-45ce-85a1-025d4f4e9d13
title: '影像屬性標記類型常數 (Gdiplusimaging. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b1870ad117d8c6f84af9e48f88e94f812c59467
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "104992463"
---
# <a name="image-property-tag-type-constants"></a>影像屬性標記類型常數

您可以使用 [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) 物件的協助來儲存和取出影像中繼資料。 **PropertyItem** 物件的 **類型** 資料成員會指定儲存在相同 **PropertyItem** 物件之值資料成員中值的資料類型。

下列常數定義于 Gdiplusimaging 中，可以指派給 [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem)物件的 **類型** 資料成員。



| 常數                                                                                                                                                                                                                                 | 描述                                                                                                                                                                                                                                                                                                                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PixelFormat4bppIndexed"></span><span id="pixelformat4bppindexed"></span><span id="PIXELFORMAT4BPPINDEXED"></span><dl> <dt>**PixelFormat4bppIndexed**</dt> </dl>         | 指定格式為每像素 4 位元的索引色彩。<br/>                                                                                                                                                                                                                                                                                                                       |
| <span id="PropertyTagTypeASCII"></span><span id="propertytagtypeascii"></span><span id="PROPERTYTAGTYPEASCII"></span><dl> <dt>**PropertyTagTypeASCII**</dt> </dl>                 | 指定 **值** 資料成員是以 null 結束的 ASCII 字串。 如果您將 [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem)物件的 **類型** 資料成員設定為 PropertyTagTypeASCII，則應該將 **長度** 資料成員設定為字串的長度，包括 Null 結束字元。 例如，字串的 `HELLO` 長度為6。<br/> |
| <span id="PropertyTagTypeByte"></span><span id="propertytagtypebyte"></span><span id="PROPERTYTAGTYPEBYTE"></span><dl> <dt>**PropertyTagTypeByte**</dt> </dl>                     | 指定 **值** 資料成員為位元組陣列。<br/>                                                                                                                                                                                                                                                                                                                |
| <span id="PropertyTagTypeLong"></span><span id="propertytagtypelong"></span><span id="PROPERTYTAGTYPELONG"></span><dl> <dt>**PropertyTagTypeLong**</dt> </dl>                     | 指定 **值** 資料成員為不帶正負號的 long (32 位) 整數的陣列。<br/>                                                                                                                                                                                                                                                                                      |
| <span id="PropertyTagTypeRational"></span><span id="propertytagtyperational"></span><span id="PROPERTYTAGTYPERATIONAL"></span><dl> <dt>**PropertyTagTypeRational**</dt> </dl>     | 指定 **值** 資料成員為不帶正負號的長整數配對陣列。 每個配對都代表一個分數;第一個整數為分子，而第二個整數為分母。<br/>                                                                                                                                                                       |
| <span id="PropertyTagTypeShort"></span><span id="propertytagtypeshort"></span><span id="PROPERTYTAGTYPESHORT"></span><dl> <dt>**PropertyTagTypeShort**</dt> </dl>                 | 指定 **值** 資料成員為不帶正負號的短 (16 位) 整數的陣列。<br/>                                                                                                                                                                                                                                                                                     |
| <span id="PropertyTagTypeSLONG"></span><span id="propertytagtypeslong"></span><span id="PROPERTYTAGTYPESLONG"></span><dl> <dt>**PropertyTagTypeSLONG**</dt> </dl>                 | 指定 **值** 資料成員是帶正負號的 long (32 位) 整數的陣列。<br/>                                                                                                                                                                                                                                                                                        |
| <span id="PropertyTagTypeSRational"></span><span id="propertytagtypesrational"></span><span id="PROPERTYTAGTYPESRATIONAL"></span><dl> <dt>**PropertyTagTypeSRational**</dt> </dl> | 指定 **值** 資料成員為帶正負號的長整數配對陣列。 每個配對都代表一個分數;第一個整數為分子，而第二個整數為分母。<br/>                                                                                                                                                                         |
| <span id="PropertyTagTypeUndefined"></span><span id="propertytagtypeundefined"></span><span id="PROPERTYTAGTYPEUNDEFINED"></span><dl> <dt>**PropertyTagTypeUndefined**</dt> </dl> | 指定 **值** 資料成員是可保存任何資料類型值的位元組陣列。 <br/>                                                                                                                                                                                                                                                                         |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Gdiplusimaging。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[影像屬性標記常數](-gdiplus-constant-image-property-tag-constants.md)
</dt> <dt>

[影像檔案格式規格](-gdiplus-constant-image-file-format-specifications.md)
</dt> <dt>

[讀取和寫入中繼資料](-gdiplus-reading-and-writing-metadata-use.md)
</dt> </dl>

 

 
