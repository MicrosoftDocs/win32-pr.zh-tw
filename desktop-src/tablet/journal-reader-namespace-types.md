---
description: 本節記載「日誌讀取器」元件所使用的 XML 類型。
ms.assetid: 08b45fe0-a505-4cc0-9791-764a87e8f1eb
title: 日誌讀取器命名空間類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c4e8e3d812eea879ca9dd31680aa2834d6dfe50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193148"
---
# <a name="journal-reader-namespace-types"></a>日誌讀取器命名空間類型

本節記載「日誌讀取器」元件所使用的 XML 類型。

## <a name="in-this-section"></a>本節內容



| 類型                                                                                  | Description                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AlternatesListType complexType**](alternateslisttype-complex-type.md)             | 定義型別，其中包含筆墨字組的辨識替代項清單。<br/>                                                                                                                  |
| [**BackgroundImageType complexType**](backgroundimagetype-complex-type.md)           | 定義類型，這個類型會保存筆記本附注（如果有的話）所使用之背景影像的相關資訊。<br/>                                                                                                |
| [**BackgroundType complexType**](backgroundtype-complex-type.md)                     | 定義包含筆記本便箋之背景資訊的類型。<br/>                                                                                                                     |
| [**BaselineType complexType**](baselinetype-complex-type.md)                         | 定義包含段落基準相關資訊的類型。<br/>                                                                                                                       |
| [BoundsType attributeGroup](boundstype-attributegroup.md)                            | 定義日誌 XML 檔案中各種專案所使用的屬性群組。<br/>                                                                                                             |
| [**ColorType simpleType**](colortype-simple-type.md)                                 | 定義型別，這個型別是用來針對日誌 XML 檔案中特定專案的色彩指定有效值。<br/>                                                                                      |
| [ContentGroup 群組](contentgroup-group.md)                                          | 定義在筆記本便箋中包含一組分組內容的類型。<br/>                                                                                                                          |
| [**ContentType complexType**](contenttype-complex-type.md)                           | 定義在日誌 XML 檔案內包含某種格式內容的型別。<br/>                                                                                                                      |
| [**ContentTypeType simpleType**](contenttypetype-simple-type.md)                     | 定義型別，該型別定義 [Content 專案 \[ 日誌讀取 \] 器](content-element--journal-reader.md)之 **type** 屬性的有效值。<br/>                                             |
| [**DrawingType complexType**](drawingtype-complex-type.md)                           | 定義型別，其中包含由日誌分析引擎分類為 [繪圖元素](drawing-element.md) (的筆墨，而不是) 的 [InkWord 元素](inkword-element.md) 。<br/>  |
| [**FlagType complexType**](flagtype-complex-type.md)                                 | 定義型別，其中包含內嵌在筆記本檔中之旗標的編碼二進位影像和位置資訊。<br/>                                                                         |
| [**GroupNodeType complexType**](groupnodetype-complex-type.md)                       | 定義在筆記本便箋中包含一組分組內容的類型。<br/>                                                                                                                          |
| [**HorizontalType complexType**](horizontaltype-complex-type.md)                     | 定義類型，其中包含筆記本便箋中的信紙所使用的水平線相關資訊。<br/>                                                                                         |
| [**ImageType complexType**](imagetype-complex-type.md)                               | 定義包含筆記本便箋中影像之二進位資訊的類型。 另請參閱 [**BackgroundImageType 的 complexType**](backgroundimagetype-complex-type.md)。<br/>                     |
| [**InkWordType complexType**](inkwordtype-complex-type.md)                           | 定義型別，其中包含 [InkWord](inkword-element.md) 專案的筆墨資料、替代專案和信賴度， (相對於) 的 [繪圖元素](drawing-element.md) 。<br/> |
| [**JournalPageType complexType**](journalpagetype-complex-type.md)                   | 定義在筆記本便箋中包含個別頁面的型別。<br/>                                                                                                                                |
| [**LineLayoutType complexType**](linelayouttype-complex-type.md)                     | 定義類型，其中包含指定筆記本便箋之信紙中所使用之程式程式碼的相關資訊。<br/>                                                                                      |
| [**LineLayoutStyleType simpleType**](linelayoutstyletype-simple-type.md)             | 定義 [LineLayout 元素](linelayout-element.md)之 **Style** 屬性的有效值。<br/>                                                                                           |
| [**LineType complexType**](linetype-complex-type.md)                                 | 定義包含一系列段落的型別。<br/>                                                                                                                                                 |
| [**MarginType complexType**](margintype-complex-type.md)                             | 定義型別，其中包含筆記本便箋中任何邊界的詳細資料，例如 style、color 和 position。<br/>                                                                               |
| [**MarginTypeType simpleType**](margintypetype-simple-type.md)                       | 定義包含 [Margin 元素](margin-element.md)之 **type** 屬性有效值的型別。<br/>                                                                                |
| [**ParagraphType complexType**](paragraphtype-complex-type.md)                       | 定義在筆記本便箋中保存段落的型別。<br/>                                                                                                                                          |
| [**ParagraphLineMetricsType complexType**](paragraphlinemetricstype-complex-type.md) | 定義包含段落之線條度量資訊的類型，例如基準。<br/>                                                                                             |
| [**ReflowType complexType**](reflowtype-complex-type.md)                             | 定義表示已 reflowed 群組的類型。<br/>                                                                                                                                        |
| [**ScalarTransformType complexType**](scalartransformtype-complex-type.md)           | 定義類型，這個類型會保存套用至筆墨之任何轉換的相關資訊。<br/>                                                                                                                |
| [**StationeryType complexType**](stationerytype-complex-type.md)                     | 定義包含筆記本便箋所用之信紙的型別。<br/>                                                                                                                             |
| [**TextType complexType**](texttype-complex-type.md)                                 | 定義[內容專案 \[ 日誌 \] 讀取器](content-element--journal-reader.md)中包含文字值的型別。<br/>                                                                       |
| [**TitleAreaType complexType**](titleareatype-complex-type.md)                       | 定義型別，其中包含筆記本便箋中標題的位置和界限資訊。<br/>                                                                                                     |
| [**TitleInfoType complexType**](titleinfotype-complex-type.md)                       | 定義類型，其中包含筆記本便箋中標題的相關資訊。<br/>                                                                                                                       |
| [**TitleType complexType**](titletype-complex-type.md)                               | 定義包含筆記本便箋之標題資訊的類型。<br/>                                                                                                                              |
| [**VerticalType complexType**](verticaltype-complex-type.md)                         | 定義包含在筆記本便箋之信紙中使用之垂直線詳細資料的類型。<br/>                                                                                                |



 

 

 




