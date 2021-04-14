---
title: 自訂字型集
description: 本主題說明您可以在應用程式中使用自訂字型的各種方式。
ms.assetid: 50842838-d150-df9a-f1b7-67ce5ea2bc80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a79f1ccfcb1dadd355c5f582417aacb5041ecf8b
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/21/2020
ms.locfileid: "104383238"
---
# <a name="custom-font-sets"></a>自訂字型集

本主題說明您可以在應用程式中使用自訂字型的各種方式。

-   [介紹 ](#introduction)
-   [API 的摘要](#summary-of-apis)
-   [重要概念](#key-concepts)
-   [字型和字型檔案格式](#fonts-and-font-file-formats)
-   [字型組和字型集合](#font-sets-and-font-collections)
-   [常見案例](#common-scenarios)
    -   [使用本機檔案系統中的任意字型建立字型組](#creating-a-font-set-using-arbitrary-fonts-in-the-local-file-system)
    -   [使用本機檔案系統中的已知字型建立字型組](#creating-a-font-set-using-known-fonts-in-the-local-file-system)
    -   [在 Web 上使用已知的遠端字型來建立自訂字型組](#creating-a-custom-font-set-using-known-remote-fonts-on-the-web)
    -   [使用載入至記憶體的字型資料來建立自訂字型組](#creating-a-custom-font-set-using-font-data-loaded-into-memory)
-   [進階案例](#advanced-scenarios)
    -   [組合字型組](#combining-font-sets)
    -   [使用本機 WOFF 或 WOFF2 字型資料 ](#using-local-woff-or-woff2-font-data)
    -   [使用 DirectWrite 遠端字型機制搭配自訂的低層級網路執行 ](#using-directwrite-remote-font-mechanisms-with-custom-low-level-network-implementation)
    -   [舊版 Windows 上的支援案例 ](#supporting-scenarios-on-earlier-windows-versions)

## <a name="introduction"></a>簡介

大部分的情況下，應用程式會使用安裝在本機系統上的字型。 DirectWrite 可讓您使用 [**IDWriteFactory3：： GetSystemFontSet**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-getsystemfontset) 或 [**IDWriteFactory：： GetSystemFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) 方法存取這些字型。 在某些情況下，應用程式可能也會想要使用包含在 Windows 10 中的字型，但目前系統並未安裝該字型。 您可以使用 **GetSystemFontSet** 方法，或藉由呼叫 [**IDWriteFactory3：： GetSystemFontCollection**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-getsystemfontcollection) （includeDownloadableFonts 設定為 TRUE），從 Windows 字型服務存取這類字型。 

不過，在某些應用程式案例中，應用程式需要使用未安裝在系統中且不是由 Windows 字型服務提供的字型。 以下是這類案例的範例：

-   字型會內嵌為應用程式二進位檔內的資源。
-   字型檔案會在應用程式套件中配套，並儲存在應用程式安裝資料夾下的磁片上。
-   應用程式是需要載入使用者指定字型檔案的字型開發工具。 
-   字型內嵌于可在應用程式中查看或編輯的檔檔案。 
-   應用程式會使用從公用 Web 字型服務取得的字型。 
-   應用程式會使用透過私人網路協定進行資料流程處理的字型資料。 

DirectWrite 提供 Api，可在這些和其他類似的案例中使用自訂字型。 自訂字型資料可能來自本機檔案系統中的檔案;從使用 HTTP 存取的遠端雲端式來源;或從任意來源載入至記憶體緩衝區之後。 

> [!Note]  
> 雖然 DirectWrite 提供了自 Windows 7 之後使用自訂字型的 Api，但新的 Api 已新增至 Windows 10，並同樣在 Windows 10 Creators Update (preview 組建15021或更新版本) 中，可讓您更輕鬆地執行所述的數個案例。 本主題著重于 Windows 10 中提供的 Api。 對於需要在舊版 Windows 上運作的應用程式，請參閱 [ (Windows 7/8) 的自訂字型集合 ](custom-font-collections.md)。 

 

## <a name="summary-of-apis"></a>API 的摘要

本主題著重于下列 Api 所提供的功能： 

-   [**IDWriteFontSet**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset) 介面
-   [**IDWriteFontSetBuilder**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder) 介面
-   [**IDWriteFontSetBuilder1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder1) 介面 
-   [**IDWriteFontFaceReference**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference) 介面
-   [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) 介面
-   [**IDWriteFactory：： CreateFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createfontfilereference) 方法 
-   [**IDWriteFactory：： CreateCustomFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontfilereference) 方法 
-   [**IDWriteFactory3：： CreateFontFaceReference**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontresource-createfontfacereference) 方法 
-   [**DWRITE \_字型 \_ 屬性**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_property) 結構 
-   [**DWRITE \_字型 \_ 屬性 \_ 識別碼**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_property_id) 列舉 
-   [**IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) 介面 
-   [**IDWriteFactory：： RegisterFontFileLoader**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-registerfontfileloader) 方法 
-   [**IDWriteFactory：： UnregisterFontFileLoader**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-unregisterfontfileloader) 方法 
-   [**IDWriteFactory5：： CreateInMemoryFontFileLoader**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory5-createinmemoryfontfileloader) 方法 
-   [**IDWriteInMemoryFontFileLoader**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteinmemoryfontfileloader) 介面 
-   [**IDWriteFactory5：： CreateHttpFontFileLoader**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory5-createhttpfontfileloader) 方法 
-   [**IDWriteRemoteFontFileLoader**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfileloader) 介面 
-   [**IDWriteFontDownloadQueue**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadqueue) 介面 
-   [**IDWriteFontDownloadListener**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener) 介面 
-   [**IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) 介面 
-   [**IDWriteRemoteFontFileStream**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfilestream) 介面 
-   [**IDWriteAsyncResult**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteasyncresult) 介面 
-   [**IDWriteFactory5：： AnalyzeContainerType**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory5-analyzecontainertype) 方法 
-   [**IDWriteFactory5：： UnpackFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory5-unpackfontfile) 方法 

 

## <a name="key-concepts"></a>重要概念

若要瞭解使用自訂字型的 DirectWrite Api，瞭解這些 Api 基礎的概念模型可能會很有説明。 重要概念將在此說明。 

當 DirectWrite 進行實際的文字版面配置或轉譯時，它需要存取實際的字型資料。 字型臉部物件會保存實際的字型資料，而這些資料必須存在於本機系統中。 但是針對其他作業（例如檢查特定字型的可用性或向使用者呈現字型選項），只需要特定字型的參考，而不是實際字型資料本身。 在 DirectWrite 中，字型參考物件只會包含尋找和具現化字型所需的資訊。 因為字體臉部參考不會保存實際的資料，所以 DirectWrite 可以處理字型臉部參考，讓實際資料在遠端網路位置，以及實際資料在本機。

字型組是一組字型臉部參考，以及某些基本的參考屬性，可用來參考字型或與其他字型（例如，系列名稱或字型粗細值）進行比較。 各種字型的實際資料可能是本機的，也可能是遠端或某些混合。

字型組可以用來取得對應的字型集合物件。 如需詳細資訊，請參閱下方的字型組和字型集合。 

IDWriteFontSet 介面所提供的方法，可讓您查詢屬性值（例如系列名稱或字型粗細），或符合特定屬性值的字型臉部參考。 篩選到特定選取專案之後，就可以取得 [**IDWriteFontFaceReference**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference) 介面的實例，並使用方法來下載 (如果實際的字型資料目前是遠端) ，以取得可用於版面配置和轉譯的對應 [**IDWriteFontFace3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface3) 物件。 

IDWriteFontFile 介面會為每個字型或字型臉部參考進行基礎。 這代表字型檔案的位置，並有兩個元件：字型檔案載入器和字型檔案索引鍵。 [字型檔案載入器] ([**IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader)) 可用來開啟檔案（如有需要），並傳回具有資料 ([**IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream)) 的資料流程。 視載入器而定，資料可能位於本機檔案路徑、遠端 URL 或記憶體緩衝區中。 此索引鍵是載入器定義的值，可在載入器內容中唯一識別檔案，讓載入器找出資料並為其建立資料流程。 

您可以輕鬆地將自訂字型加入自訂字型集中，以用於篩選或組織字型資訊，例如建立字型選擇器使用者介面。 字型組也可用來建立用於高階 Api （例如 [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) 和 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)）的字型集合。 [**IDWriteFontSetBuilder**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder)介面可以用來建立包含數個自訂字型的自訂字型集。 它也可以用來建立混合自訂字型和系統提供字型的自訂字型組;或者，將不同來源的字型與實際資料（本機儲存體、遠端 Url 和記憶體）混合。 

如前所述，字型臉部參考可能會參考遠端來源的字型資料，但是資料必須是區域，才能取得可用於版面配置和轉譯的字型臉部物件。 下載遠端資料是由字型下載佇列所處理。 應用程式可以使用 [**IDWriteFontDownloadQueue**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadqueue) 介面將下載遠端字型的要求排入佇列，以起始下載程式，並在下載程式完成時註冊 [**IDWriteFontDownloadListener**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener) 物件以採取動作。 

針對此處所述的大部分介面，DirectWrite 提供系統實現。 其中一個例外狀況是 [**IDWriteFontDownloadListener**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener) 介面，應用程式會在本機下載遠端字型時，執行此介面來執行應用程式特定的動作。 應用程式可能會有理由為某些其他介面提供自己的自訂執行，不過這只需要在特定、更先進的案例中使用。 例如，應用程式必須提供 [**IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) 介面的自訂執行，以在使用 WOFF2 容器格式的本機儲存體中處理字型檔案。 以下將提供其他詳細資料。 

## <a name="fonts-and-font-file-formats"></a>字型和字型檔案格式

另一個有助於瞭解的重要概念，就是個別字型臉部和包含它們的字型檔案之間的關聯性。 Ttf 或 otf) 的 OpenType 字型檔案 ( 概念很熟悉。 但 OpenType 字型格式也可讓 OpenType 字型集合 (. simsun18030.ttc 或. otc-n-us-sat-bsa-press) ，也就是包含多個字型的單一檔案。 OpenType 集合檔案通常用於與緊密相關且對特定字型資料具有相同值的大型字型：藉由將字型合併成單一檔案，可以將通用資料重復資料刪除。 基於這個理由，字型或字型臉部參考不僅需要參考字型檔案 (或對等的資料來源) ，還必須指定該檔案內的字型索引，因為檔案可能是集合檔案。 

針對網路上所使用的字型，字型資料通常會封裝成特定的容器格式 WOFF 或 WOFF2，以提供一些壓縮的字型資料，以及某種程度的保護，以防範字型授權的盜版和違規。 功能上，WOFF 或 WOFF2 檔案相當於 OpenType 字型或字型集合檔案，但資料會以不同的格式進行編碼，而這種格式需要先解壓縮才能使用。 

某些 DirectWrite Api 可能會處理個別字型的臉部，而其他 Api 則可以處理可能包含包含多個臉部之 OpenType 集合檔案的檔案。 同樣地，某些 Api 只會處理未經處理的 OpenType 格式資料，而其他 Api 則可以處理封裝的、WOFF 和 WOFF2 容器格式。 下列討論提供這些詳細資料。 

## <a name="font-sets-and-font-collections"></a>字型組和字型集合

某些應用程式可能會實作為使用 [**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) 介面的字型。 字型集合與字型組之間有直接的對應關係。 每個都可以保存相同的字型，但會將它們呈現給不同的組織。 您可以從任何字型集合取得對應的字型集，反之亦然。

使用多個自訂字型時，最簡單的方式是使用字型組產生器介面來建立自訂字型集，然後在建立字型之後取得字型集合。 以下將詳細說明建立自訂字型集的程式。 若要從字型集取得 [**IDWriteFontCollection1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontcollection1) 介面，請使用 [**IDWriteFactory3：： CreateFontCollectionFromFontSet**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-createfontcollectionfromfontset) 方法。

如果應用程式具有集合物件，且需要取得對應的字型集，則可以使用 [**IDWriteFontCollection1：： GetFontSet**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontcollection1-getfontset) 方法來完成此動作。 

## <a name="common-scenarios"></a>常見的案例

本節說明一些涉及自訂字型組的最常見案例：

-   在本機檔案系統的路徑上使用任意字型來建立自訂字型集。
-   使用已知字型建立自訂字型 (可能與儲存在本機檔案系統中的應用程式) 配套。
-   在 Web 上使用已知的遠端字型來建立自訂字型集。
-   使用載入記憶體的字型資料來建立自訂字型集。

這些案例的完整執行是在 [DirectWrite 自訂字型集範例](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DirectWriteCustomFontSets/)中提供。 該範例也會說明處理以 WOFF 或 WOFF2 容器格式封裝之字型資料的一個更先進案例，如下所述。 

### <a name="creating-a-font-set-using-arbitrary-fonts-in-the-local-file-system"></a>使用本機檔案系統中的任意字型建立字型組

在本機儲存體中處理任意一組字型檔案時， [**IDWriteFontSetBuilder1：： AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) 方法很方便，因為在單一呼叫中，它可以處理 Opentype 字型集合檔案內的所有字型，以及 opentype 變數字型的所有實例。 這項功能可在 Windows 10 Creators Update (preview 組建15021或更新版本的) 中取得，建議您隨時使用。 

若要使用此方法，請使用下列進程。

<dl> 1. 從建立 <a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory5">IDWriteFactory5</a> 介面開始： 


```C++
IDWriteFactory5* pDWriteFactory; 
HRESULT hr = DWriteCreateFactory( 
  DWRITE_FACTORY_TYPE_SHARED, 
  __uuidof(IDWriteFactory5), 
  reinterpret_cast<IUnknown**>(&pDWriteFactory) 
); 
```



   
2. 使用 factory 來取得 <a href=""></a> [**IDWriteFontSetBuilder1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder1)介面： 


```C++
IDWriteFontSetBuilder1* pFontSetBuilder; 
if (SUCCEEDED(hr)) 
{ 
  hr = pDWriteFactory->CreateFontSetBuilder(&pFontSetBuilder); 
}  
                
```



  
3. 針對本機檔案系統中的每個字型檔案，建立參考該檔案的 [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) ： 


```C++
IDWriteFontFile* pFontFile; 
if (SUCCEEDED(hr)) 
{ 
  hr = pDWriteFactory->CreateFontFileReference(pFilePath, /* lastWriteTime*/ nullptr, &pFontFile); 
} 
```



   
4. 使用 [**AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile)方法，將 [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile)物件新增至字型 set builder： 


```C++
hr = pFontSetBuilder->AddFontFile(pFontFile); 
```

如果在 [**CreateFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createfontfilereference) 的呼叫中指定的檔案路徑參考了支援的 OpenType 檔案以外的內容，則對 [**AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) 的呼叫會傳回錯誤 DWRITE \_ E \_ >fileformat。

5. 當所有檔案都已新增至字型集建立器之後，即可建立自訂字型組： 


```C++
IDWriteFontSet* pFontSet; 
hr = pFontSetBuilder->CreateFontSet(&pFontSet); 
```



   
</dl>

如果應用程式需要在 Windows 10 Creators Update 之前的 Windows 10 版本上執行，則 AddFontFile 方法將無法使用。 您可以藉由建立 [**IDWriteFactory3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory3) 介面，然後使用 QueryInterface 來嘗試取得 [**IDWriteFactory5**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory5) 介面，來偵測可用性：如果成功，則也會提供 [**IDWriteFontSetBuilder1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder1) 介面和 [**AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) 方法。

如果無法使用 AddFontFile 方法，則必須使用 [**IDWriteFontSetBuilder：： AddFontFaceReference**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference)) 方法來新增個別字型臉部。 若要允許包含多個臉部的 OpenType 字型集合檔案，您可以使用 [**IDWriteFontFile：：分析**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfile-analyze) 方法來判斷檔案中包含的臉部數目。 程式如下所示。

<dl> 1. 從建立 <a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory3">IDWriteFactory3</a> 介面開始： 


```C++
IDWriteFactory3* pDWriteFactory; 
HRESULT hr = DWriteCreateFactory( 
DWRITE_FACTORY_TYPE_SHARED, 
  __uuidof(IDWriteFactory5), 
  reinterpret_cast<IUnknown**>(&pDWriteFactory) 
); 
```



  
2. 使用 factory 來取得 [**IDWriteFontSetBuilder**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder) 介面： 


```C++
IDWriteFontSetBuilder* pFontSetBuilder; 
if (SUCCEEDED(hr)) 
{ 
  hr = pDWriteFactory->CreateFontSetBuilder(&pFontSetBuilder); 
} 
```



  
3. 針對每個字型檔案，建立 [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile)，如下所示： 


```C++
IDWriteFontFile* pFontFile; 
if (SUCCEEDED(hr)) 
{ 
  hr = pDWriteFactory->CreateFontFileReference(pFilePath, /* lastWriteTime*/ nullptr, &pFontFile); 
} 
```



我們不會將檔案直接新增至字型組產生器，而是必須判斷臉部數目並建立個別的 [**IDWriteFontFaceReference**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference) 物件。   
4. 使用 [ [**分析**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfile-analyze) ] 方法來取得檔案中的臉部數目。 


```C++
BOOL isSupported; 
DWRITE_FONT_FILE_TYPE fileType; 
UINT32 numberOfFonts; 
hr = pFontFile->Analyze(&isSupported, &fileType, /* face type */ nullptr, &numberOfFonts); 
```



[**分析**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfile-analyze)方法也會設定 isSupported 和資料類型參數的值。 如果檔案不是支援的格式，則 isSupported 會是 FALSE，而且可以採取適當的動作，例如忽略檔案。   
5. 對 numberOfFonts 參數中所設定的字型數目進行迴圈。 在迴圈中，為每個檔案/索引組建立 [**IDWriteFontFaceReference**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference) ，並將其加入至字型 set builder。 


```C++
for (uint32_t fontIndex = 0; fontIndex < numberOfFonts; fontIndex++) 
{ 
  IDWriteFontFaceReference* pFontFaceReference;
  hr = pDWriteFactory->CreateFontFaceReference(pFontFile, fontIndex, DWRITE_FONT_SIMULATIONS_NONE, &pFontFaceReference);

  if (SUCCEEDED(hr))
  {
    hr = pFontSetBuilder->AddFontFaceReference(pFontFaceReference);
  }
} 
```



  
6. 將所有臉部都新增至字型組產生器之後，請建立自訂字型集，如上所示。  
</dl>

您可以設計應用程式，讓它在 Windows 10 Creators Update 上執行時使用慣用的 [**AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) 方法，但在舊版 Windows 10 上執行時，會改回使用 [**AddFontFaceReference**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference)) 方法。 如上面所述，測試 [**IDWriteFactory5**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory5) 介面的可用性，然後據以進行分支。 這種方法會在 [DirectWrite 自訂字型組範例](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DirectWriteCustomFontSets/)中說明。 

### <a name="creating-a-font-set-using-known-fonts-in-the-local-file-system"></a>使用本機檔案系統中的已知字型建立字型組

如上所述，字型集中的每個字型臉部參考都會與特定的資訊屬性相關聯，例如系列名稱和字型粗細。 使用上面所列的 API 呼叫，將自訂字型加入至字型組產生器時，會直接從實際的字型資料取得這些參考屬性，該資料會在新增字型時讀取。 不過，在某些情況下，如果某個應用程式有另一個字型相關資訊來源，則可能會想要為這些屬性提供自己的自訂值。 

例如，假設應用程式會針對在應用程式內呈現特定使用者介面專案的某些字型進行組合。 有時，例如使用新的應用程式版本，應用程式針對這些元素所使用的特定字型可能需要變更。 如果應用程式已對特定字型進行編碼參考，則將某個字型取代為另一個字型需要變更這些參考的每一個字型。 相反地，如果應用程式使用自訂屬性，根據所呈現的元素類型或文字來指派功能別名，則會將每個別名對應到一個位置中的特定字型，然後在建立和操作字型的所有內容中使用別名，然後以另一個字型取代字型，只需要變更別名對應至特定字型的一個位置。 

呼叫 [**IDWriteFontSetBuilder：： AddFontFaceReference**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference)) 方法時，可以指派資訊屬性的自訂值。 執行這項操作的方法如下所示：這可用於任何 Windows 10 版本。 

如上所示，從取得 [**IDWriteFactory3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory3) 和 [**IDWriteFontSet**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset) 介面開始。 針對要新增的每個自訂字型，建立 [**IDWriteFontFaceReference**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference)，如上所示。 不過，在步驟5中的迴圈內（如上所示），將這項新增至字型 set builder (中) ，不過，應用程式會定義要使用的自訂屬性值。 

您可以使用 [**DWRITE \_ 字型 \_ 屬性**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_property) 結構的陣列來定義一組自訂屬性值。 其中每個都會從 [**DWRITE \_ FONT \_ 屬性 \_ 識別碼**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_property_id) 列舉識別特定的屬性，以及要使用的對應屬性值。  

請注意，所有的屬性值都會被指派為字串。 如果稍後可能會向使用者顯示，則可能會設定不同語言的特定屬性替代值，但這並非必要。 另請注意，如果有任何自訂屬性值是由應用程式所設定，則只會在字型集內使用指定的值;DirectWrite 不會直接從字型集合中使用的資訊屬性的字型衍生任何值。 

下列範例會定義三個資訊屬性的自訂值：系列名稱、完整名稱和字型粗細。 


```C++
DWRITE_FONT_PROPERTY props[] = 
{ 
  { DWRITE_FONT_PROPERTY_ID_FAMILY_NAME, L"My Icon Font", L"en-US" }, 
  { DWRITE_FONT_PROPERTY_ID_FULL_NAME, L"My Icon Font", L"en-US" }, 
  { DWRITE_FONT_PROPERTY_ID_WEIGHT, L"400", nullptr } 
}; 
               
            
```



為字型定義所需的屬性值陣列之後，請呼叫 AddFontFaceRefence，傳遞屬性陣列以及字型臉部參考。 


```C++
hr = pFontSetBuilder->AddFontFaceReference(pFontFaceReference, props, ARRAYSIZE(props)); 
```



 

一旦將所有自訂字型新增至字型組產生器，以及其自訂屬性，請建立自訂字型集，如上所示。 

### <a name="creating-a-custom-font-set-using-known-remote-fonts-on-the-web"></a>在 Web 上使用已知的遠端字型來建立自訂字型組

自訂屬性對於使用遠端字型而言很重要。 每個字型臉部參考都必須有一些參考屬性來描述字型，並與其他字型區別。 由於遠端字型的字型資料不是本機的，因此 DirectWrite 無法直接從字型資料衍生屬性。 因此，當您將遠端字型新增至字型組產生器時，必須明確地提供屬性。

將遠端字型新增至字型組的 API 呼叫順序，類似于前一個案例所述的順序。 但是由於字型資料是遠端的，因此讀取實際字型資料所涉及的作業將會與使用本機儲存體中的檔案時不同。 在此情況下，Windows 10 Creators Update 中新增了較低層級的介面 [**IDWriteRemoteFontFileLoader**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfileloader)。 

若要使用遠端字型檔案載入器，它必須先向 DirectWrite factory 註冊。 只要使用與其相關聯的字型，應用程式就必須保留載入器。 當字型不再使用，且在處理站終結之前的某個時間點，必須將載入器取消註冊。 這可以在擁有載入器物件之類別的函式中完成。 這些步驟將如下所示。 

使用遠端字型建立自訂字型集的方法如下所示：這需要 Windows 10 Creators Update。  

<dl> 1. 建立 IDWriteFactory5 介面，如上所示。   
2. 建立 <a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder">IDWriteFontSetBuilder</a> 介面，如上所示。   
3. 使用 factory 取得 <a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfileloader">IDWriteRemoteFontFileLoader</a>。 


```C++
IDWriteRemoteFontFileLoader* pRemoteFontFileLoader; 
if (SUCCEEDED(hr)) 
{ 
    hr = pDWriteFactory->CreateHttpFontFileLoader( 
        /* referrerURL */ nullptr, 
        /* extraHeaders */ nullptr, 
        &pRemoteFontFileLoader 
    ); 
} 
```



這會傳回系統提供的遠端字型檔案載入器介面，此介面能夠處理 HTTP 互動以代表應用程式下載字型資料。 如果字型服務或字型來源的服務需要，可以指定查閱者 URL 或額外的標頭。    

> [!IMPORTANT]
> 安全性注意事項：嘗試提取遠端字型時，攻擊者可能會偽造將被呼叫的目標伺服器。 在這種情況下，會對攻擊者公開目標和查閱者 Url 和標頭詳細資料。 應用程式開發人員負責降低此風險。 建議使用 HTTPS 通訊協定，而不是 HTTP。 

 

單一遠端字型檔案載入器可以用於多個字型，不過如果字型是從多個具有不同要求者 URL 或額外標頭的服務取得，則可以使用不同的載入器。   
4. 向 factory 註冊遠端字型檔案載入器。 


```C++
 if (SUCCEEDED(hr)) 
 { 
     hr = pDWriteFactory->RegisterFontFileLoader(pRemoteFontFileLoader); 
 } 
```



從現在開始，建立自訂字型組的步驟類似于已知的本機字型檔案所述的步驟，但有兩個重要的例外。 首先， [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) 物件是使用遠端字型檔案載入器介面來建立，而不是使用 factory。 其次，因為字型資料不是在本機，所以無法流量分析方法。 相反地，應用程式必須知道遠端字型檔案是否為 OpenType 字型集合檔案，如果是，則它必須知道所要使用之集合中的字型，以及每個字型的索引。 因此，其餘步驟如下所示。   
5. 針對每個遠端字型檔案，使用遠端字型檔案載入器介面來建立 [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile)，並指定存取字型檔案所需的 URL。 


```C++
 IDWriteFontFile* pFontFile; 
 hr = pRemoteFontFileLoader->CreateFontFileReferenceFromUrl( 
     pDWriteFactory, 
     /* baseUrl */ L"https://github.com/", 
     /* fontFileUrl */ L"winjs/winjs/blob/master/src/fonts/Symbols.ttf?raw=true", 
     &pFontFile 
 ); 
```



請注意，您可以在 fontFileUrl 參數中指定完整的 URL，也可以將它分割成基底和相對部分。 如果指定基底 URL，則 baseUrl 和 fontFileUrl 值的串連必須提供完整的 URL，DirectWrite 將不會提供任何其他分隔符號。  

> [!IMPORTANT]
> 安全性/效能附注：嘗試提取遠端字型時，不保證 Windows 會收到伺服器的回應。 在某些情況下，伺服器可能會回應無效相對 URL 的檔案找不到錯誤，但如果收到多個不正確要求，就會停止回應。 如果伺服器沒有回應，Windows 最終將會過期，但如果已起始多個提取，這可能需要幾分鐘的時間。 進行呼叫時，您應該執行哪些動作，以確保 Url 會是有效的。 

 

另請注意，此 URL 可以指向原始的 OpenType 字型檔案 (. ttf、. otf、. simsun18030.ttc、. otc-n-us-sat-bsa-press) ，但它也可以指向 WOFF 或 WOFF2 容器檔案中的字型。 如果參考 WOFF 或 WOFF2 檔案，則遠端字型檔案載入器的 DirectWrite 執行會自動將容器檔案中的字型資料解壓縮。   
6. 針對要使用的遠端字型檔案中的每個字型臉部索引，建立 [**IDWriteFontFaceReference**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference)。 


```C++
 IDWriteFontFaceReference* pFontFaceReference; 
 hr = pDWriteFactory->CreateFontFaceReference(pFontFile, /* faceIndex */ 0, DWRITE_FONT_SIMULATIONS_NONE, &pFontFaceReference);
```



  
7. 定義字型的自訂屬性，如上所示。   
8. 如上面所示，將字型臉部參考連同自訂屬性新增至字型 set builder。   
9. 將所有字型新增至字型組產生器之後，請建立字型集，如上所示。   
10. 在某個時間點，將不再使用遠端字型時，請取消註冊遠端字型檔案載入器。 


```C++
hr = pDWriteFactory->UnregisterFontFileLoader(pRemoteFontFileLoader); 
```



  
</dl>

建立具有自訂遠端字型的自訂字型之後，字型集會包含遠端字型的參考和參考屬性，但實際的資料仍會在遠端。 遠端字型的 DirectWrite 支援可讓您在字型集中維護字型臉部參考，並在配置和轉譯中選取要使用的字型，但是實際的資料必須在實際使用時才會下載，例如在執行文字配置時。  

應用程式可透過要求 DirectWrite 下載字型資料，然後在開始進行字型的任何處理之前等候成功下載的確認，來採取預先的方法。 但網路下載意指某些延遲的時間無法預期，而且也不確定成功。 基於這個理由，通常最好採用不同的方法，讓版面配置和轉譯一開始先使用已在本機的替代或備用字型，同時要求以平行方式下載所需的遠端字型，然後在所需的字型下載之後更新結果。 

若要要求在使用之前先下載整個字型，可以使用 [**IDWriteFontFaceReference：： EnqueueFontDownloadRequest**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontfacereference-enqueuefontdownloadrequest) 方法。 如果字型很大，則可能只需要部分資料來處理特定字串。 DirectWrite 提供其他方法，可用來要求特定內容、 [**EnqueueCharacterDownloadRequest**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontfacereference-enqueuecharacterdownloadrequest) 和 [**EnqueueGlyphDownloadRequest**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontfacereference-enqueueglyphdownloadrequest)所需的字型資料部分。  

假設在應用程式中採取的方法，是讓處理一開始就使用本機、替代或備用字型來完成。 IDWriteFontFallback：：[**MapCharacters**](idwritefontfallback-mapcharacters.md) 方法可以用來識別本機的恢復字型，也會自動將要求排入佇列，以下載慣用的字型。 此外，如果使用 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) ，且版面配置中的部分或全部文字是使用遠端字型參考格式化，則 DirectWrite 會自動使用 **MapCharacters** 方法來取得本機的回復字型，並將下載遠端字型資料的要求排入佇列。 

DirectWrite 會維護每個處理站的字型下載佇列，而使用上述方法所提出的要求會新增至該佇列。 您可以使用 [**IDWriteFactory3：： GetFontDownloadQueue**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-getfontdownloadqueue) 方法來取得字型下載佇列。 

如果已建立下載要求，但字型資料已在本機，則會導致無法執行的作業：不會將任何專案新增至下載佇列。 應用程式可以藉由呼叫 [**IDWriteFontDownloadQueue：： IsEmpty**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontdownloadqueue-isempty) 方法，檢查佇列是否為空的，或是否有擱置中的下載要求。 

將遠端字型要求新增至佇列之後，必須起始下載程式。 在 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)中使用遠端字型時，會在應用程式呼叫強制版面配置或轉譯作業的 **IDWriteTextLayout** 方法（例如 GetLineMetrics 或 Draw 方法）時自動起始下載。 在其他情況下，應用程式必須藉由呼叫 [**IDWriteFontDownloadQueue：： BeginDownload**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontdownloadqueue-begindownload)來直接起始下載。  

當下載完成時，應用程式會由應用程式採取適當的動作（繼續進行暫止的作業），或一開始使用回復字型完成的重複作業。  (如果使用 DirectWrite 的文字版面配置，則可以使用 [**IDWriteTextLayout3：： InvalidateLayout**](idwritetextlayout3-invalidatelayout.md) 清除使用回復字型計算的暫存結果。 ) 為了讓應用程式在下載程式完成時收到通知，並採取適當的動作，應用程式必須提供 [**IDWriteFontDownloadListener**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener) 介面的執行，並將其傳遞至 BeginDownload 呼叫。 

> [!IMPORTANT]
> 安全性/效能附注：嘗試提取遠端字型時，不保證 Windows 會收到伺服器的回應。 如果伺服器沒有回應，Windows 最終將會出現時間，但如果有多個遠端字型正在提取但失敗，可能需要幾分鐘的時間。 BeginDownload 呼叫會立即傳回。 應用程式不應該在等候 IDWriteFontDownloadListener 時封鎖 UI [**：:D 的 ownloadcompleted**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontdownloadlistener-downloadcompleted) 呼叫。 

 

您可以在 [DirectWrite 自訂字型組範例](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DirectWriteCustomFontSets/)和 [DirectWrite 可下載字型範例](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/DWriteTextLayoutCloudFont)中，看到這些與 DirectWrite 的字型下載佇列和 [**IDWriteFontDownloadListener**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener)介面互動的範例。 

### <a name="creating-a-custom-font-set-using-font-data-loaded-into-memory"></a>使用載入至記憶體的字型資料來建立自訂字型組

就像從字型檔案讀取資料的低層級作業不同于本機磁片上的檔案與 Web 上的遠端檔案不同，將字型資料載入記憶體緩衝區同樣也是如此。 Windows 10 Creators Update 的 [**IDWriteInMemoryFontFileLoader**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteinmemoryfontfileloader)中加入了新的低層級介面，以處理記憶體中的字型資料。 

如同遠端字型檔案載入器，記憶體中的字型檔案載入器必須先向 DirectWrite factory 註冊。 只要使用與其相關聯的字型，應用程式就必須保留載入器。 當字型不再使用，且在處理站終結之前的某個時間點，必須將載入器取消註冊。 這可以在擁有載入器物件之類別的函式中完成。 這些步驟將如下所示。 

如果應用程式具有資料所代表字型字型的個別相關資訊，則可以將個別字型臉部參考新增至字型集產生器，並指定自訂屬性。 不過，由於字型資料位於本機記憶體中，因此不需要這樣做;DirectWrite 將能夠直接讀取資料，以衍生屬性值。 

DirectWrite 假設字型資料是原始的 OpenType 格式，相當於 OpenType 檔案 (. ttf、otf、simsun18030.ttc、otc-n-us-sat-bsa-press) ，但在記憶體中，而不是在磁片上。 資料不能是 WOFF 或 WOFF2 容器格式。 資料可以表示 OpenType 字型集合。 如果未使用自訂屬性，則可以使用 [**IDWriteFontSetBuilder1：： AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) 方法，在單一呼叫中將所有字型臉部新增至資料。 

記憶體內部案例的重要考慮是資料的存留期。 如果提供緩衝區的指標給 DirectWrite，而沒有明確指出有擁有者，則 DirectWrite 會將資料的複本複製到它所擁有的新記憶體緩衝區。 為了避免複製資料和額外的記憶體配置，應用程式可以傳遞可執行 IUnknown 的資料擁有者物件，並擁有包含字型資料的記憶體緩衝區。 藉由執行這個介面，DirectWrite 可以新增至物件的參考計數，藉此確保擁有資料的存留期。 

使用記憶體中字型資料建立自訂字型集的方法如下所示：這需要 Windows 10 Creators Update。 這會假設是由應用程式所執行的資料擁有者物件，它會執行 IUnknown，而且也有傳回記憶體緩衝區指標和緩衝區大小的方法。 

<dl> 1. 建立 IDWriteFactory5 介面，如上所示。  
2. 建立 [**IDWriteFontSetBuilder1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder1) 介面，如上所示。  
3. 使用 factory 取得 IDWriteInMemoryFontFileLoader。 


```C++
 IDWriteInMemoryFontFileLoader* pInMemoryFontFileLoader; 
if (SUCCEEDED(hr)) 
{ 
    hr = pDWriteFactory->CreateInMemoryFontFileLoader(&pInMemoryFontFileLoader); 
}
```



這會傳回系統提供的記憶體中字型檔案載入器介面的執行。   
4. 使用 factory 註冊記憶體中的字型檔案載入器。 


```C++
if (SUCCEEDED(hr)) 
{ 
    hr = pDWriteFactory->RegisterFontFileLoader(pInMemoryFontFileLoader); 
}
```



   
5. 針對每個記憶體中的字型檔案，使用記憶體中的字型檔案載入器來建立 [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile)。 


```C++
IDWriteFontFile* pFontFile; 
hr = pInMemoryFontFileLoader->CreateInMemoryFontFileReference( 
    pDWriteFactory, 
    pFontDataOwner->fontData /* returns void* */, 
    pFontDataOwner->fontDataSize /* returns UINT32 */, 
    pFontDataOwner /* ownerObject, owns the memory with font data and implements IUknown */, 
    &pFontFile 
); 
```



   
6. 使用 [**AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile)方法將 [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile)物件新增至字型 set builder，如上所示。  如果有需要，應用程式可以改為根據 **IDWriteFontFile** 建立個別的 [**IDWriteFontFaceReference**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference)物件，並選擇性地定義每個字型臉部參考的自訂屬性，然後使用 [**AddFontFaceReference**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference))方法將自訂屬性的字型臉部參考新增至字型集，如上所示。   
7. 將所有字型新增至字型組產生器之後，請建立自訂字型組，如上所示。   
8. 在某個時間點，將無法再使用記憶體中的字型時，請取消註冊記憶體中的字型檔案載入器。 


```C++
hr = pDWriteFactory->UnregisterFontFileLoader(pInMemoryFontFileLoader);
```



  
</dl>

 

## <a name="advanced-scenarios"></a>進階案例

有些應用程式可能會有特殊需求，需要比上述程式更先進的處理。 

### <a name="combining-font-sets"></a>組合字型組

有些應用程式可能需要建立一組字型，其包含其他字型集中的一些專案組合。 例如，應用程式可能會想要建立一組字型，將安裝在系統上的所有字型與選取的自訂字型合併，或是將符合特定準則的已安裝字型與其他字型合併。 DirectWrite 具有 Api，可支援操作和組合字型組。 

若要結合兩個或多個字型集， [**IDWriteFontSetBuilder：： AddFontSet**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontset) 方法會加入指定字型中的所有字型，以在單一呼叫中新增至字型組產生器。 如果新的字型集中只需要現有字型的特定字型，則可以使用 [**IDWriteFontSet：： GetMatchingFonts**](idwritefontset-getmatchingfonts-overload.md) 方法來衍生已篩選成隻包含符合指定屬性之字型的新字型集物件。 這些方法可讓您輕鬆地建立自訂字型組，以結合兩個或多個現有字型集中的字型。 

### <a name="using-local-woff-or-woff2-font-data"></a>使用本機 WOFF 或 WOFF2 字型資料

如果應用程式在本機檔案系統或記憶體緩衝區中有字型檔案，但它們使用 WOFF 或 WOFF2 容器格式，則 DirectWrite (Windows 10 Creator Update 或更新版本) 會提供解除封裝容器格式的方法， [**IDWriteFactory5：： UnpackFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory5-unpackfontfile)會傳回 [**IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream)。 

不過，應用程式需要一種方式，讓 [**IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) 進入字型檔案載入器物件。 其中一個方法是建立包裝資料流程的自訂 [**IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) 執行。 和其他字型檔案載入器一樣，這必須在使用之前註冊，並在處理站超出範圍之前取消註冊。  

如果自訂載入器也將與原始 (搭配使用，而不是封裝) 字型檔案，則應用程式也需要提供 [**IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) 介面的自訂執行，以處理這些檔案。 不過，使用上述 Api 來處理原始字型檔案的方法更簡單。 針對壓縮的字型檔案使用不同的程式碼路徑，而不是原始字型檔案，就可以避免自訂資料流程執行的需求。 

建立自訂字型檔案載入器物件之後，會依應用程式特定的方式將壓縮的字型檔案資料新增至載入器。 載入器可以處理多個字型檔案，其中每個都是使用 DirectWrite 不透明的應用程式定義索引鍵來識別。 將壓縮的字型檔案新增至載入器之後，會使用 [**IDWriteFactory：： CreateCustomFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontfilereference) 方法，根據指定索引鍵所識別之字型資料的載入器來取得 [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) 。  

當字型新增至載入器時，可以將字型資料的實際解除封裝完成，但是也可以在 [**IDWriteFontFileLoader：： CreateStreamFromKey**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileloader-createstreamfromkey) 方法中處理，DirectWrite 將會在第一次需要讀取字型資料時呼叫。 

建立 IDWriteFontFile 物件之後，將字型新增至自訂字型集的其餘步驟將會如上所述。 

使用此方法的實作為 [DirectWrite 自訂字型組範例](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DirectWriteCustomFontSets/)中的說明。 

### <a name="using-directwrite-remote-font-mechanisms-with-custom-low-level-network-implementation"></a>使用 DirectWrite 遠端字型機制搭配自訂的低層級網路執行

處理遠端字型的 DirectWrite 機制可以分為較高層級的機制，包括包含遠端字型字型參考的字型、檢查字型資料的位置，以及管理字型下載要求的佇列，以及處理實際下載的較低層級機制。 有些應用程式可能會想要利用較高層級的遠端字型機制，但也需要自訂網路互動，例如使用 HTTP 以外的通訊協定與伺服器通訊。 

在這種情況下，應用程式必須建立 [**IDWriteRemoteFontFileLoader**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfileloader) 介面的自訂執行，以所需的方式與其他較低層級的介面互動。 應用程式也必須提供這些較低層級介面的自訂執行： [**IDWriteRemoteFontFileStream**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfilestream)和 [**IDWriteAsyncResult**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteasyncresult)。 這三個介面具有回呼方法，DirectWrite 會在下載作業期間呼叫此方法。 

當呼叫 [**IDWriteFontDownloadQueue：： BeginDownload**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontdownloadqueue-begindownload) 時，DirectWrite 會對遠端字型檔案載入器進行有關資料位置的查詢，並且會要求遠端資料流。 如果資料不是本機資料，則會呼叫資料流程的 BeginDownload 方法。 資料流程的執行不應該在該呼叫上封鎖，但應該立即傳回，傳回提供等候控制碼的 [**IDWriteAsyncResult**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteasyncresult) 物件，DirectWrite 會使用此物件來等候非同步下載作業。 自訂資料流程的執行負責處理遠端通訊。 當完成事件發生時，DirectWrite 會呼叫 [**IDWriteAsyncResult：： GetResult**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwriteasyncresult-getresult) 來判斷作業的結果。 如果結果成功，則預期針對下載範圍的後續 ReadFragment 呼叫串流將會成功。 

> [!IMPORTANT]
> 安全性/效能附注：嘗試提取遠端字型時，可能是因為攻擊者可能會偽造要呼叫的目標伺服器，或是伺服器可能沒有回應。 如果您正在執行自訂網路互動，您可能會比處理協力廠商伺服器更能掌控緩和措施。 不過，您必須考慮適當的緩和措施，以避免資訊洩漏或阻斷服務。 建議使用安全的通訊協定，例如 HTTPS。 此外，您應該以一些時間來建立，讓傳回給 DirectWrite 的事件控制碼最後會被設定。 

 

### <a name="supporting-scenarios-on-earlier-windows-versions"></a>舊版 Windows 上的支援案例

舊版 Windows 上的 DirectWrite 可支援所述的案例，但在應用程式的元件上需要更多自訂的程式，使用 Windows 10 之前可用的較有限 Api。 如需詳細資訊，請參閱 [自訂字型集合 (Windows 7/8) ](custom-font-collections.md)。

 

 