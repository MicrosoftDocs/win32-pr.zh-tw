---
title: Active Accessibility 文字服務字典的附錄 E 文字屬性
description: 本附錄提供 IAccDictionary 中所定義之文字屬性的相關資訊。
ms.assetid: 9e405140-c151-4f00-91c5-777c84c41806
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 588c827764d17c2576efaa5e3117527e23d1da26
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104024040"
---
# <a name="appendix-e-text-attributes-for-active-accessibility-text-services-dictionary"></a>附錄 E： Active Accessibility 文字服務字典的 Text 屬性

本附錄提供 [**IAccDictionary**](/windows/desktop/api/msaatext/nn-msaatext-iaccdictionary)中所定義之文字屬性的相關資訊。 它會組織成一系列的資料表。 每個資料表都包含特定屬性類別的相關資訊。 這些類別實際上是嵌套的，但會以下面的分隔，讓您可以看到屬性。

> [!Note]  
> Active Accessibility 的文字服務已淘汰。 如需有關 advanced Text 輸入和自然語言技術的詳細資訊，請參閱 [Microsoft Windows 文字服務架構](../tsf/text-services-framework.md) 。

 

資料表中的每個專案都會提供屬性名稱和易記名稱、類型、階層式樣式表 (CSS) 對等的文字物件模型 (TOM) 相等，以及適當的任何其他批註。 TOM 對等資料行提供與屬性搭配使用的 TOM 方法的相關資訊 (部分 [**ITextFont**](/windows/desktop/api/tom/nn-tom-itextfont)、 [**ITextRange**](/windows/desktop/api/tom/nn-tom-itextrange)或 [**ITextPara**](/windows/desktop/api/tom/nn-tom-itextpara) 介面) 。 每個資料表之前的資訊指出支援屬性的介面;TOM 對等資料表中的資訊表示方法的名稱。 TOM 對應資料行中的每個專案都與兩個方法相關聯。 例如，名稱專案會與 **GetName** 和 **SetName** 方法相關聯。

如需這些介面的詳細資訊，請參閱 Windows 軟體開發套件 (SDK) 中的 [Text 物件模型](../controls/text-object-model.md) 檔。

## <a name="font"></a>字型

下表中的屬性與一般字型屬性相關聯。 TOM 對等專案是 [**ITextFont**](/windows/desktop/api/tom/nn-tom-itextfont) 介面。



| 屬性名稱，易記名稱       | 類型     | CSS 對等專案       | TOM 對等 | 註解           |
|-------------------------------------|----------|----------------------|----------------|-------------------|
| 字型 \_ FaceName、FaceName<br/> | VT \_ BSTR | 字型-系列： Verdana | Name           |                   |
| 字型 \_ SizePts、SizePts<br/>   | VT \_ I4   | Font-size： Xpt       | 大小           | 大小為點 |



 

## <a name="font_style"></a>字型 \_ 樣式

下表中的屬性可解決字型樣式屬性 (例如，文字是設定為粗體或斜體) 。 TOM 對等專案是 [**ITextFont**](/windows/desktop/api/tom/nn-tom-itextfont) 介面。



| 屬性名稱，易記名稱                             | 類型     | CSS 對等專案              | TOM 對等                                            | 註解                   |
|-----------------------------------------------------------|----------|-----------------------------|-----------------------------------------------------------|---------------------------|
| 字型 \_ 樣式 \_ 粗體、粗體<br/>                        | VT \_ BOOL | 字型粗細：粗體           | 粗體                                                      |                           |
| 字型 \_ 樣式 \_ 斜體、斜體<br/>                    | VT \_ BOOL | 字型樣式：斜體          | 斜體                                                    |                           |
| 字型 \_ 樣式 \_ SmallCaps、SmallCaps<br/>              | VT \_ BOOL | 字型-variant： small 大寫字母    | SmallCaps                                                 |                           |
| 字型 \_ 樣式 \_ 大寫、大寫<br/>             | VT \_ BOOL | 文字-轉換：大寫  | 不支援                                             |                           |
| 字型 \_ 樣式 \_ 大寫、大寫<br/>               | VT \_ BOOL | 文字-轉換：大寫   | AllCaps                                                   |                           |
| 字型 \_ 樣式 \_ 小寫、小寫<br/>               | VT \_ BOOL | 文字轉換：小寫   | 不支援                                             |                           |
| 字型 \_ 樣式 \_ 浮凸、浮凸<br/>                     | VT \_ BOOL | 不支援               | Emboss                                                    |                           |
| 字型 \_ 樣式 \_ 陰文，陰文<br/>                   | VT \_ BOOL | 不支援               | 刻                                                   |                           |
| \_隱藏字型樣式 \_                                       | VT \_ BOOL | 不支援               | Hidden                                                    |                           |
| 字型 \_ 樣式 \_ 字偶間距調整、字偶間距調整<br/>                   | VT \_ R4   | 不支援               | 字元                                                   | 與 GetKerning 相同的值 |
| \_ \_ 概述的字型樣式，概述<br/>                 | VT \_ BOOL | 不支援               | 概述                                                  |                           |
| 字型 \_ 樣式 \_ 位置、位置<br/>                 | VT \_ R4   | 不支援               | 位置                                                  |                           |
| \_ \_ 受保護的字型樣式                                    | VT \_ BOOL | 不支援               | Protected                                                 |                           |
| 字型 \_ 樣式 \_ 陰影、陰影<br/>                     | VT \_ BOOL | 行高度 (減號的數位)  | 陰影                                                    |                           |
| 字型 \_ 樣式 \_ 間距、間距<br/>                   | VT \_ R4   | 字母間距              | 間距                                                   | 點                 |
| 字型 \_ 樣式 \_ 權數、權數<br/>                     | VT \_ I4   | 字型粗細                 | 以字型粗細和 GetWeight 形式 WeightSame 值<br/> |                           |
| 字型 \_ 樣式 \_ 高度、高度<br/>                     | VT \_ R4   | Line-height                 | 不支援                                             | 點                 |
| 字型 \_ 樣式 \_ 閃爍，閃爍<br/>                       | VT \_ BOOL | 文字裝飾：閃爍      | 不支援                                             |                           |
| 字型 \_ 樣式注 \_ 標、注標<br/>               | VT \_ BOOL | 垂直對齊： sub         | 注標 (也是位置)                                  |                           |
| 字型 \_ 樣式 \_ 上標、上標<br/>           | VT \_ BOOL | 垂直對齊： super       | 上標 (也是位置)                                |                           |
| 字型 \_ 樣式 \_ 色彩、色彩<br/>                       | VT \_ I4   | Color                       | ForeColor                                                 | RBG COLORREF 樣式        |
| 字型 \_ 樣式 \_ BackgroundColor、背景 \_ 色彩<br/> | VT \_ I4   | 背景色彩            | BackColor                                                 | RBG COLORREF 樣式        |



 

## <a name="font_style_animation"></a>字型 \_ 樣式 \_ 動畫

下表中的屬性會處理字型動畫。 TOM 對等專案是 [**ITextFont**](/windows/desktop/api/tom/nn-tom-itextfont) 介面。



| 屬性名稱，易記名稱                                              | 類型     | CSS 對等專案 | TOM 對等 |
|----------------------------------------------------------------------------|----------|----------------|----------------|
| 字型 \_ 樣式 \_ 動畫 \_ LasVegasLights、LasVegas \_ 燈<br/>         | VT \_ BOOL | 不支援  | 動畫      |
| 字型 \_ 樣式 \_ 動畫 \_ BlinkingBackground、閃爍 \_ 背景<br/> | VT \_ BOOL | 不支援  | 動畫      |
| 字型 \_ 樣式 \_ 動畫 \_ SparkleText、閃爍 \_ 文字<br/>               | VT \_ BOOL | 不支援  | 動畫      |
| 字型 \_ 樣式 \_ 動畫 \_ MarchingBlackAnts、按照 \_ 黑色 \_ ants<br/> | VT \_ BOOL | 不支援  | 動畫      |
| 字型 \_ 樣式 \_ 動畫 \_ MarchingRedAnts、按照 \_ red \_ ants<br/>     | VT \_ BOOL | 不支援  | 動畫      |
| 字型 \_ 樣式 \_ 動畫 \_ Shimmer、Shimmer<br/>                         | VT \_ BOOL | 不支援  | 動畫      |
| 字型 \_ 樣式 \_ 動畫 \_ WipeDown、WipeDown<br/>                       | VT \_ BOOL | 不支援  | 動畫      |
| 字型 \_ 樣式 \_ 動畫 \_ WipeRight、WipeRight<br/>                     | VT \_ BOOL | 不支援  | 動畫      |



 

## <a name="font_style_underline"></a>字型 \_ 樣式 \_ 底線

下表中的屬性會定址字型的底線樣式。 TOM 對等專案是 [**ITextFont**](/windows/desktop/api/tom/nn-tom-itextfont) 介面。



| 屬性名稱，易記名稱                     | 類型     | CSS 對等專案                | TOM 對等 |
|---------------------------------------------------|----------|-------------------------------|----------------|
| 字型 \_ 樣式 \_ 底線 \_ single、single<br/>  | VT \_ BOOL | 文字裝飾：底線    | Underline      |
| 字型 \_ 樣式 \_ 底線 \_ 雙精度浮點數<br/> | VT \_ BOOL | 文字裝飾：逐行 | 雙  |



 

## <a name="font_style_strikethrough"></a>字型 \_ 樣式 \_ 刪除線

下表中的屬性可解決字型的刪除線樣式。



| 屬性名稱，易記名稱                                         | 類型     | CSS 對等專案 | TOM 對等 |
|-----------------------------------------------------------------------|----------|----------------|----------------|
| 字型 \_ 樣式 \_ 刪除線 \_ 單鍵， \_ 刪除 \_<br/> | VT \_ BOOL | 不支援  | 不支援  |
| 字型 \_ 樣式 \_ 刪除線 \_ 雙線 \_ 、 \_ 雙精度浮點數<br/> | VT \_ BOOL | 不支援  | 不支援  |



 

## <a name="font_style_overline"></a>字型 \_ 樣式的上 \_ 劃線

下表中的屬性可解決字型的上劃線樣式。



| 屬性名稱，易記名稱                             | 類型     | CSS 對等專案            | TOM 對等 |
|-----------------------------------------------------------|----------|---------------------------|----------------|
| 字型 \_ 樣式 \_ 的頂線 \_ single、頂線 \_ 單一<br/> | VT \_ BOOL | 文字裝飾：上劃線 | 不支援  |
| 字型 \_ 樣式 \_ \_ 的上劃線雙精度浮 \_ 點數<br/> | VT \_ BOOL | 文字裝飾：上劃線 | 不支援  |



 

## <a name="text"></a>Text

下表中的屬性會處理一般文字格式化屬性。



| 屬性名稱，易記名稱                     | 類型        | CSS 對等專案 | TOM 對等                                       | 註解                                                                               |
|---------------------------------------------------|-------------|----------------|------------------------------------------------------|---------------------------------------------------------------------------------------|
| 文字 \_ VerticalWriting，垂直書寫<br/> | VT \_ BOOL    | 不支援  | 不支援                                        | 依中文/日文使用                                                           |
| 文字 \_ RightToLeft、RightToLeft<br/>          | VT \_ BOOL    | 方向      | 不支援                                        |                                                                                       |
| 文字 \_ ReadOnly、唯讀<br/>               | VT \_ BOOL    | 不支援  | ITextFont：： CanChange、ITextRange：： CanEdit            | 檔的可編輯屬性優先于                                     |
| 文字 \_ 語言、語言<br/>                | VT \_ I4      | 不支援  | ITextFont::GetLanguageID, ITextFont::SetLanguageID   | LANGID                                                                                |
| 文字 \_ 方向，方向<br/>          | VT \_ I4      | 不支援  | 不支援                                        | 10??? 學位                                                                     |
| 文字 \_ EmbeddedObject，內嵌 \_ 物件<br/>  | VT \_ BOOL    | 不支援  | 不支援                                        | 允許搜尋内嵌物件                                                 |
| 文字 \_ 連結，連結<br/>                        | VT \_ 不明 | 連結           | 不支援                                        | 物件的介面指標;針對任何感興趣的介面呼叫 QueryInterface |
| 文字 \_ 斷字、斷字<br/>          | VT \_ BOOL    | 不支援  | ITextPara::GetHyphenation, ITextPara::SetHyphenation |                                                                                       |



 

## <a name="text_alignment"></a>文字 \_ 對齊

下表中的屬性會處理文字對齊。 TOM 對等專案是 [**ITextPara**](/windows/desktop/api/tom/nn-tom-itextpara) 介面。



| 屬性名稱，易記名稱               | 類型     | CSS 對等專案 | TOM 對等 |
|---------------------------------------------|----------|----------------|----------------|
| 文字 \_ 靠 \_ 左對齊、靠左<br/>       | VT \_ BOOL | 文字對齊     | 對齊      |
| 靠 \_ 右對齊文字 \_<br/>     | VT \_ BOOL | 文字對齊     | 對齊      |
| 文字 \_ 對齊 \_ 中心、置中<br/>   | VT \_ BOOL | 文字對齊     | 對齊      |
| 文字 \_ 對齊方式 \_ 、合理性<br/> | VT \_ BOOL | 文字對齊     | 對齊      |



 

## <a name="text_para"></a>文字 \_ 段落

下表中的屬性會處理段落的格式設定。 TOM 對等專案是 [**ITextPara**](/windows/desktop/api/tom/nn-tom-itextpara) 介面。



| 屬性名稱，易記名稱                              | 類型   | CSS 對等專案 | TOM 對等  | 註解 |
|------------------------------------------------------------|--------|----------------|-----------------|---------|
| 文字 \_ 段落 \_ FirstLineIndent，第 \_ 一行 \_ 縮排<br/> | VT \_ R4 | 不支援  | FirstLineIndent | 依磅  |
| 文字 \_ 段落 \_ LeftIndent、左 \_ 縮排<br/>             | VT \_ R4 | 不支援  | LeftIndent      | 依磅  |
| 文字 \_ 段落 \_ RightIndent、靠右 \_ 縮排<br/>           | VT \_ R4 | 不支援  | RightIndent     | 依磅  |
| 文字 \_ 段落 \_ SpaceAfter、後面的空格 \_<br/>             | VT \_ R4 | 不支援  | SpaceAfter      | 依磅  |
| 文字 \_ 段落 \_ SpaceBefore、後面的空格 \_<br/>            | VT \_ R4 | 不支援  | SpaceAfter      | 依磅  |



 

## <a name="text_para_linespacing"></a>文字 \_ 段落 \_ lineSpacing

下表中的屬性會定址段落中的行間距。 TOM 對等專案是 [**ITextPara**](/windows/desktop/api/tom/nn-tom-itextpara) 介面。



| 屬性名稱，易記名稱                               | 類型     | CSS 對等專案 | TOM 對等 | 註解  |
|-------------------------------------------------------------|----------|----------------|----------------|----------|
| 文字 \_ 段落 \_ lineSpacing \_ single、single<br/>           | VT \_ BOOL | 不支援  | LineSpacing    |          |
| 文字 \_ 段落 \_ lineSpacing \_ OnePtFive，一 \_ 到 \_ 五<br/> | VT \_ BOOL | 不支援  | LineSpacing    |          |
| 文字 \_ 段落 \_ lineSpacing \_ 雙精度浮點數<br/>           | VT \_ BOOL | 不支援  | LineSpacing    |          |
| 文字 \_ 段落 \_ lineSpacing \_ 至少 \_<br/>       | VT \_ R4   | 不支援  | LineSpacing    | 行數 |
| 文字 \_ 段落 \_ lineSpacing \_ 完全<br/>         | VT \_ R4   | 不支援  | LineSpacing    | 行數 |
| 文字 \_ 段落 \_ lineSpacing \_ 多個、多重<br/>        | VT \_ R4   | 不支援  | LineSpacing    | 行數 |



 

## <a name="text_list"></a>文字 \_ 清單

下表中的屬性會針對清單和文字清單的層級進行定址。 TOM 對等專案是 [**ITextPara**](/windows/desktop/api/tom/nn-tom-itextpara) 介面。



| 屬性名稱，易記名稱 | 類型   | CSS 對等專案 | TOM 對等 | 註解                                                       |
|-------------------------------|--------|----------------|----------------|---------------------------------------------------------------|
| 文字 \_ 清單 \_ LevelIndex、       | VT \_ I4 | 不支援  | ListLevelIndex | 其中1是最外層的清單，2是下一個層級，依此類推。 |



 

## <a name="text_list_type"></a>文字 \_ 清單 \_ 類型

下表中的屬性會為文字提供清單樣式。 TOM 對等專案是 [**ITextPara**](/windows/desktop/api/tom/nn-tom-itextpara) 介面。



| 屬性名稱，易記名稱                          | 類型     | CSS 對等專案  | TOM 對等 |
|--------------------------------------------------------|----------|-----------------|----------------|
| 文字 \_ 清單 \_ 類型 \_ 專案符號，專案符號<br/>             | VT \_ BOOL | 清單類型       | ListType       |
| 文字 \_ 清單 \_ 類型 \_ 阿拉伯文、阿拉伯文<br/>             | VT \_ BOOL | 清單樣式類型 | ListType       |
| 文字 \_ 清單 \_ 類型 \_ LowerLetter、小寫 \_ 字母<br/> | VT \_ BOOL | 清單樣式類型 | ListType       |
| 文字 \_ 清單 \_ 類型 \_ UpperLetter、大寫字母 \_<br/> | VT \_ BOOL | 清單樣式類型 | ListType       |
| 文字 \_ 清單 \_ 類型 \_ LowerRoman、小寫 \_ 羅馬字<br/>   | VT \_ BOOL | 清單樣式類型 | ListType       |
| 文字 \_ 清單 \_ 類型 \_ UpperRoman、右上 \_ 角<br/>   | VT \_ BOOL | 清單樣式類型 | ListType       |



 

## <a name="app"></a>應用程式



| 屬性名稱，易記名稱                         | 類型     | CSS 對等專案 | TOM 對等 |
|-------------------------------------------------------|----------|----------------|----------------|
| 應用程式 \_ IncorrectSpelling，不正確的 \_ 拼寫<br/> | VT \_ BOOL |                | 不支援  |
| 應用程式 \_ IncorrectGrammar，不正確的 \_ 文法<br/>   | VT \_ BOOL |                | 不支援  |



 

 

