---
description: 表示辨識器用來繪製筆墨的區域。 此區域稱為辨識指南。
ms.assetid: c4990aa5-8c8b-4206-8376-b5c0d0c8e0a7
title: 'InkRecognizerGuide 類別 (Msinkaut) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkRecognizerGuide
- InkRecognizerGuide.IInkRecognizerGuide
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 758c2ac58803b0086a4a4083545a66d250799b414bd44e3814c90de37ca9d082
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117675659"
---
# <a name="inkrecognizerguide-class"></a>InkRecognizerGuide 類別

表示辨識器用來繪製筆墨的區域。 此區域稱為辨識指南。

**InkRecognizerGuide** 具有下列類型的成員：

-   [介面](#interfaces)
-   [屬性](#properties)

### <a name="interfaces"></a>介面

**InkRecognizerGuide** 類別會定義這些介面。



| 介面               | 描述                                                                  |
|:------------------------|:-----------------------------------------------------------------------------|
| **IInkRecognizerGuide** | 這個物件會實 **IInkRecognizerGuide** COM 介面。<br/> |



 

### <a name="properties"></a>屬性

**InkRecognizerGuide** 類別具有這些屬性。



| 屬性                                                       | 存取類型           | Description                                                                                                                    |
|:---------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [**資料行**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_columns)<br/>       | 讀取/寫入<br/> | 取得或設定節目表方塊中的資料行數目。<br/>                                                                |
| [**DrawnBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_drawnbox)<br/>     | 讀取/寫入<br/> | 取得或設定在平板電腦螢幕上實際繪製的方塊，以及寫入的位置。<br/>              |
| [**GuideData**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_guidedata)<br/>   | 讀取/寫入<br/> | 取得或設定 c + + 開發人員的參考資料。<br/>                                                                         |
| [**中線**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_midline)<br/>       | 讀取/寫入<br/> | 取得或設定中線高度。 中線高度是繪製方塊的距離，與基線之間的距離。<br/> |
| [**行**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_rows)<br/>             | 讀取/寫入<br/> | 取得或設定節目表方塊中的資料列數目。<br/>                                                                   |
| [**WritingBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_writingbox)<br/> | 讀取/寫入<br/> | 取得或設定節目表方塊中的隱藏寫入區域，在此區域中可以實際進行寫入。<br/>                  |



 

## <a name="remarks"></a>備註

您可以藉由呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 方法來具現化此物件。

依預設，沒有任何辨識器指南。 預設的指南會將所有屬性值設定為0。 您必須使用這個物件的屬性來設定節目表。

如果應用程式已在使用者應寫入的畫面上繪製指導方針，則應用程式應該設定辨識器指南的屬性值，以通知辨識器。 這些屬性僅適用于辨識器的使用。 設定它們本身並不會在顯示時繪製視覺線索。 應用程式或控制項會繪製視覺線索。

辨識器指南可以包含資料列和資料行，而這些資料行會讓辨識器成為執行辨識的較佳內容。 使用輔助線將內容提供給筆墨時，可以更容易辨識像是 "t" 和 "I" 的字母。 例如，您可以在螢幕上繪製水平線，以顯示應該發生書寫的位置 (這種類型的指南只會包含資料列，而且不會) 任何資料行。 藉由撰寫程式程式碼，而不是某些任意空間，辨識精確度也會有所改善。

本指南會以筆墨空間座標來指定筆墨的界限。

[**DrawnBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_drawnbox)屬性可以定義一個方塊，其大小等於或小於 [**WritingBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_writingbox)屬性所定義的方塊。

下圖顯示辨識器指南的元素，其中包含兩個數據列和沒有任何資料行。

![顯示辨識器指南元素的圖例](images/927cc2f3-549f-4279-aab9-bd5ade070eaf.jpg)

除了在螢幕上繪製可顯示要寫入之使用者的線條之外，您還可以在用來撰寫字元或單字的畫面上繪製儲存格。 這稱為已裝箱的輸入，適用于某些亞洲語言。 若要判斷辨識器是否能夠進行已裝箱的輸入，請呼叫 [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer)物件的 [[**功能**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_capabilities)] 屬性。

下圖顯示具有四個數據行的辨識器指南。

![圖例顯示具有四個數據行的辨識器指南](images/de44c07e-4b55-42d0-8e8b-997e2da79e52.jpg)

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                       |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                           |
| 標頭<br/>                   | <dl> <dt>Msinkaut (也需要 Msinkaut \_ c) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IInkRecognizer 介面**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer)
</dt> <dt>

[**InkRecognizerCoNtext 類別**](inkrecognizercontext-class.md)
</dt> </dl>

 

