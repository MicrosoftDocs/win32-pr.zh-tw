---
description: 本節記載「日誌讀取器」元件所使用的 XML 命名空間元素。
ms.assetid: 18fe7f81-a039-44e4-9a98-1dd137e4e97a
title: 日誌讀取器命名空間元素
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f98d5964702cb6cd1574359fa7c0310b0140241ee15974d797493a34fa3a4282
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883468"
---
# <a name="journal-reader-namespace-elements"></a>日誌讀取器命名空間元素

本節記載「日誌讀取器」元件所使用的 XML 命名空間元素。

## <a name="in-this-section"></a>本節內容



| 元素                                                                   | 描述                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [替代元素](alternate-element.md)                                | 包含 [InkWord 元素](inkword-element.md)的辨識替代專案。<br/>                                                                                                                                                                                                                                 |
| [AlternateList 元素](alternatelist-element.md)                        | 包含 [替代](alternate-element.md)專案的集合，其中包含由辨識器針對父 [InkWord 元素](inkword-element.md)傳回的替代專案。<br/>                                                                                                                                      |
| [Background 元素](background-element.md)                              | 包含 [JournalDocument 元素](journaldocument-element.md) 或 [JournalPage 元素](journalpage-element.md)的背景。<br/>                                                                                                                                                                         |
| [基準元素](baseline-element.md)                                  | 針對筆記本檔中段落基準的起始點和結束點，提供 (x，y) 資訊。 這些值所使用的座標空間是 HIMETRIC。<br/>                                                                                                                                  |
| [Bitmap 元素](bitmap-element.md)                                      | 包含包含在日誌檔案中做為背景影像之點陣圖的 Base64 編碼資料。<br/>                                                                                                                                                                                                              |
| [CanReClassify 元素](canreclassify-element.md)                        | 若 **為 true**，表示可以重新分析筆墨。 如果使用者已使用 [將手寫轉換成文字] 或 [變更] 圖形設定為 [筆記本] 的功能，則此元素為 **false** 。<br/>                                                                                     |
| [信賴元素](confidence-element.md)                              | 包含筆記本筆墨分析器針對 [InkWord 元素](inkword-element.md)所傳回的信賴評等。<br/>                                                                                                                                                                                             |
| [Content 元素 \[ 日誌讀取器\]](content-element--journal-reader.md) | 包含日誌頁面的內容。<br/>                                                                                                                                                                                                                                                                        |
| [Date 元素](date-element.md)                                          | 包含建立日誌便箋的日期。<br/>                                                                                                                                                                                                                                                                 |
| [DocImage 元素](docimage-element.md)                                  | 如果要讀取的筆記本便箋是使用筆記本便箋寫入器印表機驅動程式所建立，則背景檔影像會保留在此元素中。<br/>                                                                                                                                                         |
| [繪圖元素](drawing-element.md)                                    | 包含已由分析器或使用者分類為繪圖的內容。<br/>                                                                                                                                                                                                                             |
| [旗標元素](flag-element.md)                                          | 包含與筆記本便箋區段相關聯之旗標的 base64 編碼點陣圖。<br/>                                                                                                                                                                                                                           |
| [GroupNode 元素](groupnode-element.md)                                | 包含一組專案-[段落](paragraph-element.md)專案、 [InkWord](inkword-element.md)專案、 [繪圖元素](drawing-element.md)、 [文字元素](text-element.md)、 [影像](image-element.md)專案或旗標 [元素](flag-element.md)，這些專案會在筆記本便箋中群組在一起。<br/> |
| [水準元素](horizontal-element.md)                              | 包含在筆記本便箋中用於信紙的水平線格式資訊。<br/>                                                                                                                                                                                                             |
| [Image 元素](image-element.md)                                        | 在日誌檔中包含影像的編碼二進位資料（如果有的話）。<br/>                                                                                                                                                                                                                                  |
| [InkClass 元素](inkclass-element.md)                                  | 表示筆墨空間內所收集的筆墨筆劃。<br/>                                                                                                                                                                                                                                                    |
| [InkObject 元素](inkobject-element.md)                                | 針對 [InkWord 元素](inkword-element.md)或 [繪圖元素](drawing-element.md)，包含 [**筆墨**](inkdisp-class.md)物件的 Base64 編碼二進位資料。<br/>                                                                                                                                     |
| [InkWord 元素](inkword-element.md)                                    | 包含筆記本便箋中指定筆墨單字的相關資訊，包括位置、替代項和實際筆墨資料。<br/>                                                                                                                                                                                       |
| [JournalDocument 元素](journaldocument-element.md)                    | 筆記本便箋 XML 檔案中的最上層元素。<br/>                                                                                                                                                                                                                                                               |
| [JournalPage 元素](journalpage-element.md)                            | 包含筆記本便箋中個別頁面的詳細資料。<br/>                                                                                                                                                                                                                                                |
| [Line 元素](line-element.md)                                          | 在 [段落](paragraph-element.md)專案內包含一行。<br/>                                                                                                                                                                                                                                            |
| [LineLayout 元素](linelayout-element.md)                              | 包含適用于筆記本便箋之信紙中所使用之線條版面配置的相關資訊。<br/>                                                                                                                                                                                                                     |
| [Margin 元素](margin-element.md)                                      | 定義在頁面上繪製的邊界線。<br/>                                                                                                                                                                                                                                                                     |
| [段落元素](paragraph-element.md)                                | 包含段落。<br/>                                                                                                                                                                                                                                                                                           |
| [ParagraphLineMetrics 元素](paragraphlinemetrics-element.md)          | 包含段落各行的相關資訊。<br/>                                                                                                                                                                                                                                                            |
| [Path 元素](path-element.md)                                          | 用於筆記本便箋背景的影像路徑。<br/>                                                                                                                                                                                                                                                |
| [重排元素](reflow-element.md)                                      | 表示已 reflowed 群組。<br/>                                                                                                                                                                                                                                                                          |
| [ScalarTransform 元素](scalartransform-element.md)                    | 繪圖或 InkWord 所使用的純量轉換。<br/>                                                                                                                                                                                                                                                                |
| [信紙元素](stationery-element.md)                              | 包含筆記本便箋中使用之信紙的相關資訊，包括背景色彩或影像、標題資訊和線條版面配置資訊（例如窄規則和邊界規則）。<br/>                                                                                                     |
| [Text 元素](text-element.md)                                          | 包含筆記本便箋中的文字資訊。<br/>                                                                                                                                                                                                                                                                |
| [Title 元素](title-element.md)                                        | 包含筆記本便箋的標題資訊。<br/>                                                                                                                                                                                                                                                              |
| [TitleArea 元素](titlearea-element.md)                                | 包含附注 [標題](title-element.md)專案的位置和周框資訊（如果有的話）。<br/>                                                                                                                                                                                                         |
| [TitleInfo 元素](titleinfo-element.md)                                | 包含便箋的標題以及標題中的日期（如果有的話）。<br/>                                                                                                                                                                                                                                           |
| [垂直元素](vertical-element.md)                                  | 包含描述筆記本便箋所用信紙中線條垂直元件的資訊。<br/>                                                                                                                                                                                         |



 

 

 




