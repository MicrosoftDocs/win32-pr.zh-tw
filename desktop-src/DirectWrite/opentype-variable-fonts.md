---
title: OpenType 變數字型
description: 本主題說明 OpenType 變數字型、其在 DirectWrite 和 Direct2D 中的支援，以及如何在您的應用程式中使用它們。 .
ms.assetid: 788558a7-efe7-b075-942f-ac75a5b86b84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c671bebce73cf3bdec42d1f7f570add914db7eb33b8a6bfd1b196d569b9975d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118649388"
---
# <a name="opentype-variable-fonts"></a>OpenType 變數字型

本主題說明 OpenType 變數字型、其在 DirectWrite 和 Direct2D 中的支援，以及如何在您的應用程式中使用它們。 

-   [什麼是 OpenType 變數字型？](#what-are-opentype-variable-fonts)
-   [DirectWrite 中的 OpenType 變數字型支援](#opentype-variable-font-support-in-directwrite)
-   [使用 OpenType 變數字型](#using-opentype-variable-fonts)

## <a name="what-are-opentype-variable-fonts"></a>什麼是 OpenType 變數字型？

[Opentype 字型格式規格](https://www.microsoft.com/typography/otspec/)的1.8 版引進了新的格式延伸模組，稱為[OpenType 字型變化](/typography/opentype/spec/otvaroverview)。 使用這些延伸模組的字型稱為「OpenType 變數字型」。 OpenType 變數字型是單一字型，其行為就像數個字型一樣，方法是使用不同設計之間的連續插補，全都定義在單一字型內。

OpenType 變數字型可以在一或多個獨立軸（例如權數或寬度）上定義其設計的連續變化： 

 

![顯示使用字母 ' G ' 的 OpenType 變數字型，並顯示水準寬度軸和垂直權數軸的不同變化。](images/opentype-width-weight.png)

字型開發人員會決定要在指定字型中使用的一組變化軸。 這些軸可以包含一組知名的 (或「已註冊」 ) 的變異軸，例如權數和寬度，但也可以包含字型開發人員所定義的任意自訂座標軸。  

藉由選取字型的一組變化軸，字型開發人員會為字型定義設計變化的抽象、多元的空間。 文字引擎可以在用來配置和轉譯文字的連續空間中指定可能的任何位置或「實例」。 

字型開發人員也可以選取名稱，並將其指派給設計變化空間內的特定實例;這些稱為「命名實例」。 例如，具有權數變化的字型可能會在非常輕量和非常繁重的筆劃之間支援連續變化，而字型開發人員已選取特定權數，以及將其指派給它們的名稱，例如 "Light"、"Regular" 和 "Semibold"。 

OpenType 變數字型格式會使用在傳統 OpenType 字型中找到的資料表，再加上一些額外的表格，說明不同的資料項目值如何針對不同的實例而變更。 此格式會將一個變化實例指定為「預設實例」，這會使用傳統資料表來取得預設值。 所有其他實例都相依于預設資料和其他差異資料。 例如，「glyf」資料表可以有一個「名義」圖像圖形描述，也就是用於預設實例的圖形，而「gvar」資料表則會說明如何針對其他實例調整圖像的貝塞爾線控制點。 同樣地，其他字型值也可以有名義值加上差異資料，以描述這些值如何針對不同的實例而變更;例如，x 高度和其他全字型的度量，或字元特定的標記錨定位置和字偶間距調整。 

因為變數字型可支援任意一組變異軸，所以它們需要可延伸的字型系列模型，更直接反映字型設計工具建立字型系列的方式：字型家族是由家族名稱和某些常數的設計特性所定義，而且有任一數字 (由字型開發人員) ，以設計的變化方式來決定。 您可以使用權數的變異來建立一個字型系列，但是可以使用 x-height、serif 大小、"funkiness" 或任何字型開發人員想要的變數來建立不同的字型系列。 在此模型中，使用一般或「慣用」或「印刷樣式」、系列名稱加上一組成對的索引鍵/值組，其中每個索引鍵/值組都代表一種不同的變化和特定值，且一般是一種可延伸的集合，就能描述字型選取範圍。 字型家族的一般概念可以套用至傳統、非變數字型以及變數字型。 例如，在此一般的印刷樣式系列模型中，「Selawik VF」系列可能會有權數、光學大小和 serif 設計的變化，例如「Semilight 做橫幅 San」。 

不過，某些現有的軟體實施（包括現有的 DirectWrite api）可能會以較有限的字型系列模型設計。 例如，有些應用程式可能會假設字型家族最多隻能有一般、粗體、斜體和粗體字。 現有的 [**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) 和 [**IDWriteFontFamily**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) 介面採用權數/延展/樣式 ( "WSS" ) 系列模型，讓您可以使用 [**DWRITE \_ 字型 \_ 粗細**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_weight)、 [**DWRITE \_ 字型 \_ 延展**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_stretch) 或 [**DWRITE \_ 字型 \_ 樣式**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_style) 列舉作為參數，來指定系列內的變體。 在上述範例中，不會將光學大小和 serif 軸視為 WSS 模型中變化的系列內部軸。 

完整支援變數字型需要 Api，讓您能夠以字型所決定的數個參數來指定家庭成員。 但現有的 API 設計可以藉由將變數字型中定義的命名實例投射到更受限的字型系列模型中，來提供變數字型的部分支援。 在上述範例中，"Selawik VF Semilight 做橫幅 San" 可投影至 WSS 模型，作為「Selawik VF 橫幅 San」系列（具有 "Semilight 做" 作為權數變化）。 

針對另一個範例，請考慮使用印刷樣式的字型系列（例如 Sitka），其粗細和光學大小變化。 系列內的命名變數包括 Sitka 文字一般和 Sitka 橫幅粗體 (再加上許多其他) 。 印刷樣式系列名稱為 "Sitka"，而印刷樣式系列模型中這些變異的臉部名稱會是「文字一般」和「橫幅粗體」。 四個成員和 WSS 系列模型不允許家族內的光學大小變化，因此必須將光學大小的區別視為家庭層級的差異。 下表說明如何將 Sitka 印刷樣式系列中的字型選取範圍視為 WSS 系列模型： 



印刷樣式系列模型

WSS 系列模型

系列

臉部

系列

臉部

錫特卡

一般文字

Sitka 文字

定期

錫特卡

橫幅粗體

Sitka 橫幅

粗體

錫特卡

標題斜體

Sitka 標題

斜體



 

從印刷樣式系列模型到 WSS 系列模型的名稱投影可以套用至非變數字型，並套用至變數字型的已命名實例。 但是，您無法從變數字型的持續設計變化空間，針對其他非命名的實例進行這項操作。 基於這個理由，支援變數字型的完整功能，需要 Api 設計來參考印刷樣式系列內的臉部，而不受限制的變異軸和軸值集。 

## <a name="opentype-variable-font-support-in-directwrite"></a>DirectWrite 中的 OpenType 變數字型支援

在 Windows 10 Creators Update 版本中，OpenType 變數字型格式仍然是非常新的，而字型廠商、平臺和應用程式仍在執行新格式的流程中。 此更新會在 DirectWrite 中提供此格式的初始執行。 

DirectWrite 內部已更新為支援 OpenType 變數字型。 使用目前的 Api，這會提供變數字型之任何命名實例的支援。 這項支援可用於完整的工作流程，從列舉的實例列舉、已命名實例的選取專案、用於版面配置和成形，到轉譯和列印。 為了讓也針對某些作業使用 GDI 文字 interop 的應用程式受益，也在現有的 GDI Api 中新增了類似的支援。 

在 Windows 10 Creators Update 中，DirectWrite 不支援利用變數字型之連續變化功能的任意實例。

在許多作業中，變數字型的命名實例 DirectWrite 中的行為，不能與非變數字型的行為進行區別。 由於支援是使用現有的 DirectWrite api 所提供，因此，已命名的變數字型實例甚至可以在許多現有的 DirectWrite 應用程式中運作，而不需要進行任何變更。 不過，在某些情況下可能會發生例外狀況：  

-   如果應用程式直接處理特定作業的字型資料。 例如，如果應用程式直接從字型檔案讀取圖像大綱資料，以建立某些視覺效果。
-   如果應用程式使用協力廠商程式庫來進行某些作業。 例如，如果應用程式使用 DirectWrite 進行版面配置，則會取得最終的字元索引和位置，但接著會使用協力廠商程式庫來呈現。
-   如果應用程式將字型資料內嵌至檔，或以其他方式將字型資料傳遞給下游處理常式。

如果使用不支援變數字型的執行來執行作業，則這些作業可能不會產生預期的結果。 例如，可能會為變數字型的一個命名實例計算圖像位置，但可能會以不同的已命名實例來呈現圖像。 視應用程式的執行而定，結果可能會在某些環境中運作，但無法在其他可能使用其他程式庫的內容中運作。 例如，文字可能會在螢幕上正確顯示，但在列印時則不會正確顯示。 如果只使用 DirectWrite 來執行端對端工作流程，則可能會對變數字型的命名實例進行正確的行為。 

由於現有的 DirectWrite api 支援使用權數/延展/樣式模型的臉部選取，因此使用其他變異軸的已命名字型實例將會從一般的印刷樣式系列模型投射到 WSS 模型中，如上所述。 這會依賴變數字型，包括「樣式屬性」 ( ' STAT ' ) 資料表（具有軸值 subtables），而 DWrite 會使用此標記來區別臉部名稱標記，以從與其他軸變異相關的標記中指定權數、stretch 或樣式屬性。  

如果變數字型不含 OpenType 規格所需的「STAT」資料表，則 DirectWrite 會將字型視為包含預設實例的非變數字型。  

如果字型包含 ' STAT ' 資料表，但不包含適當的軸值 subtables，這可能會導致非預期的結果，例如擁有具有相同臉部名稱的多個臉部。 這一次不支援這類字型。 

OpenType 規格允許以兩種格式的其中一種來表示字元外框資料：使用 ' glyf ' 資料表（使用 TrueType 大綱和提示格式），或使用 ' CFF ' 資料表（使用壓縮字型格式 ( "CFF" ) 標記法）。 在具有 TrueType 大綱的變數字型中，會繼續使用 ' glyf ' 資料表，並且會使用提供外框之變異資料的 ' gvar ' 資料表來補充。 這表示具有 TrueType 大綱的變數字型預設實例只會使用不具變數字型支援的舊版軟體所支援的傳統 OpenType 資料表。 不過，在具有 CFF 大綱的變數字型中，' CFF ' 資料表會被 ' CFF2 ' 資料表取代，這會將預設大綱資料和相關聯的變化資料封裝在一個資料表中。 CFF 資料是由適用于 TrueType 資料的個別轉譯器所處理，而 ' CFF2 ' 資料表則需要具有 ' CFF2 ' 支援的更新 CFF 轉譯器。 較舊的 CFF rasterizers 無法處理 ' CFF2 ' 資料表。 針對具有 CFF 大綱資料的變數字型，這表示即使是預設實例也無法在較舊的軟體中運作。 

在 Windows 10 Creators Update 中，DirectWrite 不支援使用 ' CFF2 ' 資料表 CFF 大綱資料的變數字型。 

## <a name="using-opentype-variable-fonts"></a>使用 OpenType 變數字型

您可以輕鬆地使用 OpenType 變數字型，並記住上面所述的目前限制： 

-   目前只支援變數字型的命名實例。
-   目前只支援使用 TrueType 字元外框大綱資料 (未 CFF 大綱的變數字型) 。 
-   如果字型使用權數、stretch 或 style 以外的設計變化軸，則會將名為 instance 的實例投射到 WSS 系列模型中，這可能會導致某些命名的實例顯示為個別的系列， (在過去針對非變數字型) 的情況。 若要支援這種情況，變數字型必須有包含適當軸值 subtables 的 ' STAT ' 資料表。
-   DirectWrite api 中支援變數字型的命名實例，但如果某些作業是在不支援變數字型的較舊版本中執行，則可能會產生不正確的結果。 
-   某些 DirectWrite api 會使用 [**DWRITE \_ 字型 \_ 粗細**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_weight)、 [**DWRITE \_ 字型 \_ 延展**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_stretch)和 [**DWRITE \_ 字型 \_ 樣式**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_style)列舉，在選取臉部時指定權數、延展和樣式屬性。 如果變數字型使用對應的變異軸，但是有許多命名的實例需要更細微的資料細微性，則並非所有的命名實例都可在這些 Api 中選取。

符合這些需求的 OpenType 變數字型可以從 Windows shell 安裝，就像其他 OpenType 字型一樣，也可以在應用程式所建立的自訂字型集中使用。  

當安裝在系統中時，變數字型的所有命名實例都將包含在呼叫 IDWriteFontFamily3：：[**GetSystemFontSet**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-getsystemfontset) 方法所傳回的字型集中。 請注意，字型組是沒有家族群組階層的一般清單，但集合中的每個專案都有以 WSS 系列模型為基礎的系列名稱屬性。 您可以使用 [**IDWriteFontSet：： GetMatchingFonts**](idwritefontset-getmatchingfonts-overload.md) 方法，針對特定的變數字型（名為 instance）篩選字型集。 但是，如果使用採用 familyName 的 **GetMatchingFonts** 多載，則指定的 familyName 必須使用符合 WSS 字型系列模型的名稱。 您可以使用 [**IDWriteFontSet：： system.configuration.settingsprovider.getpropertyvalues**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist)) 方法，使用 DWRITE \_ 字型 \_ 屬性 \_ 識別碼 \_ 系列 \_ 名稱來取得在字型集中出現之 WSS 相容系列名稱的完整清單。  

同樣地，變數字型的所有已命名實例都會在 IDWriteFactory：：[**GetSystemFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) 方法所傳回的字型集合中表示。 因為字型集合的元素是以 WSS 模型為基礎的字型系列，所以變數字型的命名實例可能會在集合中表示為兩個或多個字型系列的成員。 如果使用 [**IDWriteFontCollection：： FindFamilyName**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollection-findfamilyname) 方法，則 familyName 參數必須是 WSS 相容的系列名稱。 若要從字型集合中尋找所有 WSS 相容的系列名稱，應用程式可以在每個系列中執行迴圈，並呼叫 [**IDWriteFontFamily：： GetFamilyNames**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfamily-getfamilynames)，不過，您可以更輕鬆地取得對應的字型集，並使用上述的 [**system.configuration.settingsprovider.getpropertyvalues**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist)) 方法。 

使用自訂字型時，可使用 [自訂字型組](custom-font-sets-win10.md) 主題中所述的各種方法來建立字型集。 若要將變數字型加入自訂字型集，建議使用 [**IDWriteFontSetBuilder1：： AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) 方法，因為它支援變數字型，並會在單一呼叫中加入變數字型的所有已命名實例。 目前沒有任何方法可以使用 [**IDWriteFontSetBuilder：： AddFontFaceReference**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference)) 方法，將自訂變數字型的個別名稱實例新增至字型集，因為無法建立字型臉部參考，以指定要從變數字型檔案指定的命名實例。 這表示目前沒有任何方法可將自訂字型的命名實例加入至已指派自訂屬性的自訂字型集。 也就是說，自訂變數字型目前無法輕易地與遠端字型的 DirectWrite api 搭配使用。 如果系統字型集中包含變數字型的命名實例，則每個已命名實例的字型臉部參考都會存在，而且可以加入自訂的字型集，包括使用自訂屬性值。 如需詳細資訊，請參閱自訂字型組主題。 

使用可變字型時，DirectWrite [**DWRITE \_ 字型 \_ 粗細**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_weight)和 [**DWRITE \_ 字型 \_ 延展**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_stretch)列舉會緊密地連接至 OpenType 規格中定義的權數和寬度變化軸，但不相同。 首先，任何變化軸的數值小數位數一律支援小數值，而 fontWeight 和 fontStretch 則使用整數。 OpenType 權數軸刻度使用的值範圍從1到1000，這也是 fontWeight 所支援的值。 因此，從變異的權數軸值變更為 fontWeight 相對較小：針對命名實例所報告的 fontWeight 可能會從用來在字型內定義已命名實例的精確值中四捨五入。 DirectWrite fontStretch 和 OpenType 寬度軸刻度之間的差異較大： DirectWrite 使用從1到9的值，並遵循 OpenType OS/2 資料表的[usWidthClass](/typography/opentype/spec/os2#uswidthclass)值，而 opentype 寬度軸尺規則使用代表正常寬度百分比的正值。 OpenType 規格中的 [usWidthClass](/typography/opentype/spec/os2#uswidthclass) 檔會提供介於1到9之間的值與百分比標準值之間的對應。 從寬度軸值進行轉換時，針對命名實例所報告的 fontStretch 值可能牽涉到四捨五入。 

建立 [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat)時，必須指定字型集合和 WSS 相容的字型屬性 (系列名稱、權數、延展和樣式) 。 這也適用于設定 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) 文字範圍的字型格式屬性時。 您可以從 [**IDWriteFontFace3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface3) 物件或 [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) 和 [**IDWriteFontFamily**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) 物件（代表特定的已命名實例）中取得屬性。 如上所述，GetWeight 和 GetStretch 方法所傳回的值，可能會針對用來定義已命名之實例的實際座標軸值進行四捨五入，但是 DirectWrite 會將屬性的組合對應回所需的已命名實例。 

同樣地，如果應用程式使用 [**IDWriteFontFallbackBuilder**](idwritefontfallbackbuilder.md) 來建立自訂字型回資料，則會使用與 WSS 相容的系列名稱來指定字元範圍對應的系列。 DirectWrite 內的字型回復是以家族為基礎，DirectWrite 在一個備用系列內選取變異，這是與起始系列變異最相符的範圍。 對於涉及加權、stretch 和 style 以外維度的變體，除非特別建立自訂的回溯資料來為具有特定非 WSS 屬性的系列（例如 "Caption" 光學大小變化）提供回溯對應，否則 DirectWrite 目前無法在該回系列內選取這類變異。

 

 