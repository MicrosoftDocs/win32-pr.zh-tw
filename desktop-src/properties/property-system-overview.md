---
description: Windows 屬性系統是資料定義的可擴充讀取/寫入系統，可提供統一的方式來表示 Shell 專案的中繼資料。
ms.assetid: eb2dc2be-fc53-40aa-81f6-f353ab1d3a57
title: 屬性系統概觀
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dab3a17eacdbaa9a5d0255004ba544b7c3f7ff2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977838"
---
# <a name="property-system-overview"></a>屬性系統概觀

Windows 屬性系統是資料定義的可擴充讀取/寫入系統，可提供統一的方式來表示 Shell 專案的中繼資料。 Windows Vista 和更新版本中的 Windows 屬性系統可讓您儲存和取得 Shell 專案的中繼資料。 Shell 專案是任何一段內容，例如檔案、資料夾、電子郵件或連絡人。 屬性是與 Shell 專案相關聯之中繼資料的個別部分。 屬性值會以 [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) 結構表示。

本主題的組織方式如下：

-   [簡介](#introduction)
-   [開發案例](#development-scenarios)
-   [屬性和 Windows Search](#properties-and-windows-search)
-   [實施者注意事項](#note-to-implementers)
-   [Windows 屬性系統檔](#windows-property-system-documentation)
-   [其他資源](#additional-resources)
-   [相關主題](#related-topics)

## <a name="introduction"></a>簡介

屬性是由其正式名稱唯一識別 (例如 `System.Document.LastAuthor`) 和屬性索引鍵 (例如 `PKEY_Document_LastAuthor`) 。 屬性索引鍵 (PKEY) 是名稱/值組的名稱部分，其包含 PKEY/PROPVARIANT 或字串/PROPVARIANT，其中字串是 PKEY (的正式名稱，例如 `System.Document.LastAuthor`) 。 PKEY 是一種定義，可告知屬性系統它需要知道屬性的所有專案，而值則是屬性的實際實例。 PKEY 內部包含 formatID 和 propID。

個別屬性包含下列三個部分：

-   標準名稱，例如 `System.Music.Artist` 。
-   架構描述（以 propdesc XML 檔案格式指定），並以程式設計方式透過 [**IPropertyDescription**](/windows/desktop/api/Propsys/nn-propsys-ipropertydescription)表示。
-   值，例如 singer 的名稱。

架構描述包含屬性的相關資訊，例如屬性名稱、資料類型、條件約束、屬性如何與視圖和搜尋系統互動的相關資訊等等。 名稱和架構描述是全域定義的，而且所有專案和類型都相同。 值是個別專案的特定值。 也就是說， `System.Music.Artist` 屬性一律定義為多重值字串，但可能會有不同的值 (或每個專案的所有) 都沒有值。

屬性處理常式會將儲存在檔案中的資料轉譯成可辨識的結構化架構，並且可由 Windows 檔案總管、Windows Search 和其他應用程式存取。 這些系統接著可以與屬性處理常式互動，以在檔案中寫入和讀取屬性。 轉譯的資料會以程式設計方式公開，並透過 Windows 檔案總管在各種內容中顯示，包括詳細資料檢視、提示、詳細資料窗格、屬性頁等等。 每個屬性處理常式都與特定檔案類型相關聯，該檔案類型是由副檔名來識別。 開發人員應該採用產生和取用其檔案類型原生格式（例如 .jpg 或 .png）的屬性處理常式，或使用 In-Memory 屬性儲存區，它會產生和取用 MS PROPSTORE 二進位格式。

Windows 屬性系統會建立從個別檔案格式提供抽象層級的抽象資料模型。 Windows 屬性系統所提供的抽象資料模型是一種方法，用來讀取和寫入與 Shell 專案相關聯之可延伸的命名值集。 值運算式具有彈性，可支援許多資料類型，而且可延伸，可讓任意資料 (**VT \_ BLOB**) 和物件以值表示。

由於抽象概念，您可以查詢任何專案的屬性或中繼資料。 可以抽象化的專案範例包括 Microsoft Office 檔、ID3 標記、AutoCAD 和其他協力廠商專屬軟體。 同樣地，如果您有一個 jpeg 檔案，您可以使用 jpeg 和 EXIF 編解碼器來讀取檔案的位元組，以找出影像的維度。 如果您改為使用 .png 檔案，則需要不同的編解碼器和不同的程式碼。 使用 Windows 屬性系統可避免這類問題。 如果您要執行新的檔案類型，您可以選擇插入 Windows 屬性系統所提供的統一抽象概念，並指定如何讓您的中繼資料可供使用。 基於這些理由，最好是使用 Windows 屬性系統所提供的通用平臺。

## <a name="development-scenarios"></a>開發案例

屬性是由生產者和取用者表示。 在此內容中，生產者是 Windows 屬性系統中的屬性發明者之一該項，而取用者是應用程式 (和其開發人員) 取用此系統中的屬性資訊。 下表指出 Windows 屬性系統中的和參與者的用法。



| 使用 Windows 屬性系統                                                                                                                                                                                            | 參與者 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------|
| 一個建立區塊，可提供屬性描述的可延伸登錄、記憶體內部屬性存放區的執行，以及用來系結至屬性處理常式、轉換型別和序列化屬性存放區的服務。 | 消費者    |
| 想要以抽象的方式讀取和寫入屬性的應用程式。                                                                                                                                                       | 消費者    |
| 屬性發明者之一該項，定義自訂屬性架構並開發自己的屬性處理常式，藉此定義屬性系統的新屬性。                                                                          | 產生器 (producer)    |
| 檔案格式擁有者，想要啟用其自訂檔案格式所儲存之屬性的存取權。                                                                                                                           | 產生器 (producer)    |



 

取用者會使用現有的屬性、架構和屬性處理常式。 可用的屬性包括支援的檔案類型的屬性處理常式的讀取/寫入屬性，也可能包含一些自訂屬性。 可用的架構也包含至少系統架構，有時也包含其他架構。 取用者可以建立應用程式來取用中繼資料，並根據演出者建立視圖，而不論專案儲存在哪些資料夾中。 檔案資料夾階層是不相關的。 例如，您可以指定特定 singer 的所有歌曲專案，而不需要擔心這類專案的位置。 這種複雜的端對端案例不限於 Windows 屬性系統，但牽涉到數個不同的元件，例如編制索引和搜尋資料夾。

屬性發明者之一該項（或協力廠商開發人員）是 Windows 屬性系統中的生產者。 準備定義新的屬性時，請先檢查 Windows 定義的屬性集。 如果您發現符合您需求的型別和語義符合您的需要，請使用該屬性，而且不會建立新的屬性。 如果您要定義新的自訂內容，請嘗試與其他開發人員取得合約，這些開發人員可能會想要使用該屬性併發布該合約的結果，讓他們可以加入該屬性的使用者群。

生產者可以利用 Windows 檔案總管的功能。 例如，如果您要撰寫新的影像格式，並執行屬性處理常式，您的新檔案格式會在 Windows 檔案總管中變成可用。 然後，使用者可以根據 Windows 屬性系統中的任何屬性，標記相片並將其相片集合資料透視。 事實上，Shell 針對屬性所執行的任何動作，協力廠商開發人員都可以在自己的應用程式中執行。 這包括群組、排序、查詢及顯示完整屬性。 Windows 檔案總管提供的使用者體驗，大部分都是由具有公開可用 Api 的協力廠商所執行。 您可以使用這些 Api 來取代或擴充 Windows 檔案總管。

從使用 Shell 資料模型的應用程式觀點來看，有許多案例都牽涉到使用 Windows 屬性系統。 媒體管理應用程式是很重要的範例。 核心屬性系統案例包括讀取相片的關鍵字屬性或設定 datetaken 屬性等案例。 Windows 屬性系統啟用的端對端整合案例範例，但需要其他數個元件才能運作，包括顯示所有圖片，或尋找包含關鍵字的檔。

## <a name="properties-and-windows-search"></a>屬性和 Windows Search

當生產者和取用者與 Windows Search 和編制索引進行互動時，這些屬性會提供服務。 Windows Search 具有屬性值的快取，這些值是用於 Windows Search 服務 (WSS) 的執行。 您可以使用 Windows Search OLE DB 提供者或透過 [**ISearchFolderItemFactory**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory)（代表搜尋結果和查詢型視圖中的專案），以程式設計方式查詢這些屬性值。 然後，Windows Search 會在建立檔（例如 Word 檔）的索引時，收集並儲存由篩選處理常式或屬性處理常式所發出的屬性。 重建索引時，會捨棄並重建此存放區。

> [!Note]  
> 請記住，當您重新註冊架構時，索引子可能不會遵守先前定義之屬性的屬性變更。 解決方法是重建索引，或引進新的屬性來反映變更，而不是更新舊的屬性 (不建議) 。 如需詳細資訊，請參閱本主題稍後的「提供 [者注意](#note-to-implementers) 」。

 

例如，建立媒體應用程式的開發人員想要顯示特定演出者的應用程式使用者所有可用的音樂。 應用程式會為使用者提供可用的演出者清單，然後由使用者選取的演出者產生所有可用音樂的清單。 或者，使用者可能會想要對？演出者： Beethoven？進行查詢，並在其 searche 過程中公開給可用屬性的完整清單。 此範例牽涉到使用 Shell 命名空間、屬性處理常式，以及/或透過下列其中一種方式來查詢索引：

-   Shell 資料來源。
-   OLE DB 提供者。
-   已儲存的搜尋檔案 (. 搜尋-ms) ，藉由流覽至 Windows 檔案總管中的搜尋檔案，或以程式設計方式系結至 [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) 來起始查詢。

> [!Note]  
> 雖然 `System.Kind` 屬性不會參與此媒體應用程式案例，但它可用來建立查詢，以傳回特定範圍中的所有. 搜尋-ms 檔案。

 

存取搜尋 Api 和建立 Windows Search 應用程式的慣用方法是透過 Shell 資料來源。 [**ISearchFolderItemFactory**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory) 是一種元件，可建立搜尋資料夾資料來源的實例，這是由 shell 所提供的一種「虛擬」資料來源，可對 shell 命名空間中的其他資料來源執行查詢並列舉結果。 它可以藉由使用索引子，或手動列舉和檢查指定範圍中的專案來完成。

協力廠商開發人員可以建立應用程式，以透過程式設計方式查詢來取用索引中的資料，而且可以在索引中擴充自訂檔案和專案類型的資料，以 Windows Search 來編制索引。 如果您想要在 Windows 檔案總管中顯示查詢結果，您必須先執行 Shell 資料來源，才能建立通訊協定處理常式來擴充索引。 但是，如果所有查詢都是以程式設計方式 (透過 OLE DB 例如) ，並由應用程式的程式碼（而非 Shell）所解釋，則會優先使用 Shell 命名空間，但不是必要的。 需要有通訊協定處理常式，Windows 才能取得檔案內容的相關資訊，例如資料庫或自訂檔案類型中的專案。 雖然 Windows Search 可以為檔案的名稱和屬性編制索引，但 Windows 沒有檔案內容的相關資訊。 如此一來，就無法在 Windows Shell 中建立索引或公開這類專案。 藉由執行自訂通訊協定處理常式，您可以公開這些專案。 如需您嘗試達成之開發人員案例所識別的處理常式清單，請參閱 Windows Search 中的「處理常式總覽」 [作為開發平臺](../search/-search-3x-wds-development-ovr.md)。

> [!Note]  
> Shell 資料來源有時也稱為 Shell 命名空間延伸模組。 處理常式有時也稱為 Shell 擴充或 Shell 擴充處理常式。

 

## <a name="note-to-implementers"></a>實施者注意事項

由於索引子在取用屬性系統架構時可能會遇到的問題，因此您必須謹慎地定義屬性，並策略性地針對第一版的架構來定義屬性。 在架構註冊之後，資料庫的任何變更 (類型、資料行寬度、indexible) 是否都不會反映在資料庫中。 當架構在系統上註冊一次之後，唯一可辨識這些變更的方法就是重建索引，然後註冊新的架構，或是註冊架構，然後為每個後續的版本建立新的屬性。例如， `PKEY_GroupName_PropertyNameV2` `PKEY_GroupName_PropertyNameV3` 和等等。 我們不建議以這種方式建立新的屬性，因為多個額外的資料行可能會影響系統效能。

## <a name="windows-property-system-documentation"></a>Windows 屬性系統檔

本檔的其餘部分包含下列各節：

-   [Windows 屬性系統開發人員指南](property-system-developer-s-guide.md)

    詳細說明如何使用 Windows 屬性系統來執行主要開發案例。

-   [屬性系統參考](property-system-reference.md)

    記錄 Windows 屬性系統的 [Windows 屬性](props.md)、 [屬性描述架構](property-description-schema.md)、 [介面](interfaces.md)、 [函數](functions.md)、 [結構](structures.md)和 [常數、列舉和旗標](constants--enumerations--and-flags.md) 。

-   [屬性系統程式碼範例](property-system-code-samples.md)

    描述示範如何使用 Windows 屬性系統的範例。

## <a name="additional-resources"></a>其他資源

-   如需重複使用 In-Memory 屬性儲存區的詳細資訊，請參閱 [初始化屬性處理常式](building-property-handlers-property-handlers.md) 和 [**PSCreateMemoryPropertyStore**](/windows/desktop/api/Propsys/nf-propsys-pscreatememorypropertystore)。
-   如需 Microsoft 屬性儲存區二進位檔案格式的規格，請參閱[ \[ MS \_ PROPSTORE \] ](/openspecs/windows_protocols/ms-propstore/39ea873f-7af5-44dd-92f9-bc1f293852cc)。
-   Windows Search 與編制索引之間的關聯性，以及如何擴充索引，會在 Windows Search 的下列主題中說明：
    -   [針對 Windows Search 開發篩選處理常式](../search/-search-ifilter-conceptual.md)
    -   [開發 Windows Search 的通訊協定處理常式](../search/-search-3x-wds-phaddins.md)
    -   [開發 Windows Search 的屬性處理常式](../search/-search-3x-wds-extidx-propertyhandlers.md)
    -   若為 Windows 7 或更新版 Windows Vista SDK 下載，請參閱 [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows 屬性系統開發人員指南](property-system-developer-s-guide.md)
</dt> <dt>

[屬性系統參考](property-system-reference.md)
</dt> <dt>

[屬性系統程式碼範例](property-system-code-samples.md)
</dt> </dl>

 

 
