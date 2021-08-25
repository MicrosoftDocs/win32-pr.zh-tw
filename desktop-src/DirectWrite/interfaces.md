---
title: DirectWrite 介面
description: 列出 DirectWrite 所定義的介面。
ms.assetid: 7075e771-ce34-4426-8c07-13e85ff4d453
keywords:
- DirectWrite，介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f1abd75d83fedf29da1bb5f67073dd74ca10816fdeb6ca43a61f40ad8ae26c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048608"
---
# <a name="directwrite-interfaces"></a>DirectWrite 介面

DirectWrite 定義下列介面。

## <a name="in-this-section"></a>本節內容

| 主題 | 描述 |
|-|-|
| [**IDWriteAsyncResult**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteasyncresult) | 表示非同步作業的結果。 用戶端可以使用介面來等候作業完成，並取得結果。  |
| [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) | 封裝可用於轉譯圖像的32位裝置獨立點陣圖和裝置內容。 |
| [**IDWriteBitmapRenderTarget1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritebitmaprendertarget1) | 封裝32位裝置獨立點陣圖和裝置內容，您可以使用它來呈現圖像。 |
| [**IDWriteBitmapRenderTarget2**](/windows/windows-app-sdk/api/win32/dwrite_3/nn-dwrite_3-idwritebitmaprendertarget2) | 封裝可用於轉譯圖像的32位裝置獨立點陣圖和裝置內容。 |
| [**IDWriteColorGlyphRunEnumerator**](idwritecolorglyphrunenumerator.md) | 此介面可讓應用程式透過色彩圖像執行來列舉。 |
| [**IDWriteColorGlyphRunEnumerator1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritecolorglyphrunenumerator1) | 色彩圖像執行之已排序集合的列舉值。 |
| [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) | 用來建立所有後續的 DirectWrite 物件。 這個介面是所有 DirectWrite 物件的根 factory 介面。 |
| [**IDWriteFactory1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefactory1) | 所有[DirectWrite](direct-write-portal.md)物件的根 factory 介面。 |
| [**IDWriteFactory2**](idwritefactory2.md) | 所有[DirectWrite](direct-write-portal.md)物件的根 factory 介面。 |
| [**IDWriteFactory3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory3) | 所有[DirectWrite](direct-write-portal.md)物件的根 factory 介面。 |
| [**IDWriteFactory4**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory4) | 所有 DirectWrite 物件的根 factory 介面。 |
| [**IDWriteFactory5**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory5) | 所有 DirectWrite 物件的根 factory 介面。 |
| [**IDWriteFactory6**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory6) | 這代表建立所有 DirectWrite 物件的 factory 物件。 **IDWriteFactory6** 新增了使用字型和字型資源的功能。 |
| [**IDWriteFactory7**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory7) | 這個介面代表建立所有 DirectWrite 物件的 factory 物件。 **IDWriteFactory7** 新增了使用系統字型的新設備。 |
| [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) | 代表字型集合中的實體字型。 此介面是用來從實體字型建立字型臉部，或從現有字型臉部取得字型臉部度量或臉部名稱等資訊。 |
| [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1) | 代表字型集合中的實體字型。 |
| [**IDWriteFont2**](idwritefont2.md) | 代表字型集合中的實體字型。 |
| [**IDWriteFont3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefont3) | 表示字型集合中的字型。 |
| [**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) | 封裝一組字型的物件，例如安裝在系統上的字型組，或特定目錄中的字型組。 您可以使用字型集合 API 來探索可用的字型系列和字型，以及取得字型的一些相關中繼資料。 |
| [**IDWriteFontCollection1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontcollection1) | 封裝一組字型的物件，例如安裝在系統上的字型組，或特定目錄中的字型組。 您可以使用字型集合 API 來探索可用的字型系列和字型，以及取得字型的一些相關中繼資料。 |
| [**IDWriteFontCollection2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontcollection2) | 此介面會封裝一組字型，例如安裝在系統上的字型組，或特定目錄中的字型組。 |
| [**IDWriteFontCollection3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontcollection3) | 此介面會封裝一組字型，例如安裝在系統上的字型組，或特定目錄中的字型組。 |
| [**IDWriteFontCollectionLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollectionloader) | 用來在指定特定類型的索引鍵時，建立字型的集合。  |
| [**IDWriteFontDownloadListener**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener) | 應用程式定義的回呼介面，可接收來自字型下載佇列的通知 ([**IDWriteFontDownloadQueue**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadqueue) 介面) 。 回呼會在下載的執行緒上進行，而且必須隨時準備物件，以便從其他執行緒其方法的呼叫。 |
| [**IDWriteFontDownloadQueue**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadqueue) | 將下載遠端字型、字元、圖像和字型片段之要求的介面。  |
| [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) | 此介面會公開各種字型資料，例如度量、名稱和字型外框。 它包含字型字型類型、適當的檔案參考和臉部辨識資料。 |
| [**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1) | 包含字型字型類型、適當的檔案參考和臉部辨識資料。  |
| [**IDWriteFontFace2**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontface2) | 此介面包含字型類型、適當的檔案參考，以及臉部辨識資料。 它會新增檢查色彩轉譯路徑是否可能需要的功能。  |
| [**IDWriteFontFace3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface3) | 包含字型字型類型、適當的檔案參考和臉部辨識資料。 |
| [**IDWriteFontFace4**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface4) | 包含字型字型類型、適當的檔案參考和臉部辨識資料。 |
| [**IDWriteFontFace5**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface5) | 此介面包含字型類型、適當的檔案參考，以及臉部辨識資料。 它加入了新的功能，例如比較兩個字型、抓取字型軸值，以及抓取基礎字型資源。 |
| [**IDWriteFontFaceReference**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference) | 表示字型的參考。 可以唯一識別字型的參考，您可以在此建立字型來查詢字型計量和用於轉譯。 字型臉部參考包含字型檔案、字型臉部索引和字型臉部模擬。 檔案資料不一定會實際存在於本機電腦上。  |
| [**IDWriteFontFaceReference1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference1) | 表示字型的參考。 可以唯一識別字型的參考，您可以在此建立字型來查詢字型計量和用於轉譯。 |
| [**IDWriteFontFallback**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontfallback) | 可讓您從 [字型] 清單中存取「回復字型」。 |
| [**IDWriteFontFallbackBuilder**](idwritefontfallbackbuilder.md) | 可讓您建立 Unicode 字型回撥對應，並從這些對應中建立字型的物件。 |
| [**IDWriteFontFamily**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) | 代表一系列的相關字型。 |
| [**IDWriteFontFamily1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfamily1) | 代表一系列的相關字型。 |
| [**IDWriteFontFamily2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfamily2) | 代表一系列的相關字型。 **IDWriteFontFamily2** 會新增新的設備，包括以字型軸值抓取字型。 |
| [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) | 代表字型檔案。 字型管理員或字型檢視器等應用程式可以呼叫 [**IDWriteFontFile：：「分析**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfile-analyze) 」，以找出特定檔案是否為字型檔案，以及它是否為字型系統所支援的字型類型。 |
| [**IDWriteFontFileEnumerator**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileenumerator) | 封裝字型檔案的集合。 字型系統在建立字型集合時，會使用此介面來列舉字型檔案。 |
| [**IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) | 處理將特定類型的字型檔案資源從字型檔案參考金鑰載入至字型檔案資料流程物件。  |
| [**IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) | 從自訂字型檔案載入器載入字型檔案資料。  |
| [**IDWriteFontList**](/windows/win32/api/dwrite/nn-dwrite-idwritefontlist) | 表示字型的清單。 |
| [**IDWriteFontList1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontlist1) | 表示字型的清單。 |
| [**IDWriteFontList2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontlist2) | 表示字型的清單。 **IDWriteFontList2** 會新增新的設備，包括取出清單所使用的基礎字型集。 |
| [**IDWriteFontResource**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontresource) | nn-dwrite_3-idwritefontresource |
| [**IDWriteFontSet**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset) | 表示字型集。 |
| [**IDWriteFontSet1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset1) | 表示字型集。 |
| [**IDWriteFontSet2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset2) | 表示字型集。 |
| [**IDWriteFontSet3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset3) | 表示字型集。 |
| [**IDWriteFontSetBuilder**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder) | 包含用來建立字型集的方法。 |
| [**IDWriteFontSetBuilder1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder1) | 包含用來建立字型集的方法。 |
| [**IDWriteFontSetBuilder2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder2) | 包含用來建立字型集的方法。 |
| [**IDWriteGdiInterop**](/windows/win32/api/dwrite/nn-dwrite-idwritegdiinterop) | 提供與 GDI 的互通性，例如將字型字型轉換成 LOGFONT 結構的方法，或將 GDI 字型描述轉換成字型。 它也可以用來建立點陣圖呈現目標物件。 |
| [**IDWriteGdiInterop1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritegdiinterop1) | 提供與 GDI 的互通性，例如將字型字型轉換成 LOGFONT 結構的方法，或將 GDI 字型描述轉換成字型。 它也可以用來建立點陣圖呈現目標物件。 |
| [**IDWriteGeometrySink**](idwritegeometrysink.md) | [**IDWriteGeometrySink**](idwritegeometrysink.md)是 [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink)介面的 **typedef** 。 如需詳細資訊，請參閱 [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) 參考頁面。 |
| [**IDWriteGlyphRunAnalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis) | 包含用來呈現圖像執行的低層級資訊。 |
| [**IDWriteInlineObject**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject) | 包裝應用程式定義的內嵌圖形，讓 DWrite 能夠查詢計量，如同圖形是以文字內嵌的圖像。 |
| [**IDWriteInMemoryFontFileLoader**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteinmemoryfontfileloader) | 表示可以存取記憶體中字型的字型檔案載入器。 |
| [**IDWriteLocalFontFileLoader**](idwritelocalfontfileloader.md) | [**IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader)介面的內建執行，可在本機字型檔案上運作，並公開字型檔案參考索引鍵的本機字型檔案資訊。 使用 [**CreateFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createfontfilereference) 建立的字型檔案參考會使用這個字型檔案載入器。 |
| [**IDWriteLocalizedStrings**](/windows/win32/api/dwrite/nn-dwrite-idwritelocalizedstrings) | 表示依地區設定名稱編制索引的字串集合。 |
| [**IDWriteNumberSubstitution**](./idwritenumbersubstitution.md) | 針對指定的地區設定保存適當的數位和數位標點符號。 |
| [**IDWritePixelSnapping**](/windows/win32/api/dwrite/nn-dwrite-idwritepixelsnapping) | 定義圖元貼齊屬性，例如每個 DIP 的圖元 (與裝置無關的圖元) ，以及文字轉譯器目前的轉換矩陣。 |
| [**IDWriteRemoteFontFileLoader**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfileloader) | 表示可以存取遠端 (的字型檔案載入器，例如可下載的) 字型。  |
| [**IDWriteRemoteFontFileStream**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfilestream) | 代表字型檔案資料流程，其中的部分可能為非本機。  |
| [**IDWriteRenderingParams**](/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams) | 表示文字轉譯設定，例如 ClearType 層級、增強對比，以及圖像光柵和篩選的 gamma 校正。 應用程式通常會藉由呼叫 [**IDWriteFactory：： CreateMonitorRenderingParams**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createmonitorrenderingparams) 方法來取得轉譯參數物件。 |
| [**IDWriteRenderingParams1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwriterenderingparams1) | 代表圖像光柵和篩選的文字呈現設定。 |
| [**IDWriteRenderingParams2**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwriterenderingparams2) | 代表圖像光柵和篩選的文字呈現設定。 |
| [**IDWriteRenderingParams3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriterenderingparams3) | 代表圖像光柵和篩選的文字呈現設定。 |
| [**IDWriteStringList**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritestringlist) | 表示以數位索引的字串集合。 |
| [**IDWriteTextAnalysisSink**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalysissink) | 此介面是由文字分析器的用戶端所執行，以接收指定文字分析的輸出。  |
| [**IDWriteTextAnalysisSink1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalysissink1) | 您所執行的介面，用來接收文字分析器的輸出。 |
| [**IDWriteTextAnalysisSource**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalysissource) | 由文字分析器的用戶端所執行，以提供文字給分析器。 它允許將文字的邏輯視圖區隔成可由唯一文字位置識別的連續字串流，以及用戶端備份存放區中可能離散文字區塊的實際記憶體配置。  |
| [**IDWriteTextAnalysisSource1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalysissource1) | 您所執行的介面，可將所需的資訊提供給文字分析器，例如文字和相關聯的文字屬性。 |
| [**IDWriteTextAnalyzer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalyzer) | 分析各種文字屬性以進行複雜的腳本處理，例如雙向 (雙向) 支援阿拉伯文、換行、圖像放置和數位替換等語言。 |
| [**IDWriteTextAnalyzer1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1) | 分析不同的文字屬性以進行複雜的腳本處理。 |
| [**IDWriteTextAnalyzer2**](idwritetextanalyzer2.md) | 分析不同的文字屬性以進行複雜的腳本處理。 |
| [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) | [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat)介面會描述用來格式化文字的字型和段落屬性，並說明地區設定資訊。  |
| [**IDWriteTextFormat1**](idwritetextformat1.md) | 描述用來格式化文字的字型和段落屬性，並說明地區設定資訊。  |
| [**IDWriteTextFormat2**](idwritetextformat2.md) | 描述用來格式化文字的字型和段落屬性，並說明地區設定資訊。  |
| [**IDWriteTextFormat3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritetextformat3) | 描述用來格式化文字的字型和段落屬性，並說明地區設定資訊。 |
| [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) | [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)介面表示經過完整分析和格式化之後的一段文字。 |
| [**IDWriteTextLayout1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1) | 表示經過完整分析和格式化之後的一段文字。 |
| [**IDWriteTextLayout2**](idwritetextlayout2.md) | 表示經過完整分析和格式化之後的一段文字。 |
| [**IDWriteTextLayout3**](idwritetextlayout3.md) | 表示經過完整分析和格式化之後的一段文字。  |
| [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) | 表示一組應用程式定義的回呼，可執行文字、内嵌物件和裝飾（例如底線）的呈現。 |
| [**IDWriteTextRenderer1**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritetextrenderer1) | 表示一組應用程式定義的回呼，可執行文字、内嵌物件和裝飾（例如底線）的呈現。  |
| [**IDWriteTypography**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography) | 表示字型印刷樣式設定。 |