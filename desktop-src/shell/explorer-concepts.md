---
description: 當您想要擴充 Windows 檔案總管（Windows Shell UI 中的許多擴充性選項之一）時，請瞭解一般概念。
title: Common Explorer 概念
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 78136c36-bd3c-4114-8b69-fef4e307566d
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 5bd0c641e1e265b50180aa6ce4e98eeafbf3f6dc86f4f499dee5267161842e9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118050519"
---
# <a name="common-explorer-concepts"></a>Common Explorer 概念

Shell *命名空間* 會將檔案系統和其他由 shell 管理的物件組織成單一樹狀結構階層。 就概念而言，它是較大且較多的檔案系統版本。

-   [簡介](#introduction)
-   [識別命名空間物件](#identifying-namespace-objects)
    -   [專案識別碼](#item-ids)
    -   [專案識別碼清單](#item-id-lists)
    -   [Pidl](#pidls)
    -   [配置 Pidl](#allocating-pidls)

## <a name="introduction"></a>簡介

Shell 的主要職責之一就是管理和提供對組成系統的各種物件的存取權。 這些物件最多與熟悉的是位於電腦磁片磁碟機上的資料夾和檔案。 不過，Shell 也會管理許多非系統或 *虛擬* 物件。 部分範例包括：

-   網路印表機
-   其他網路電腦
-   主控台應用程式
-   資源回收筒

某些虛擬物件完全不牽涉到實體儲存體。 例如，印表機物件包含網路印表機的連結集合。 其他虛擬物件（例如資源回收筒）可能包含儲存在磁片磁碟機上的資料，但必須以不同于一般檔案的方式來處理。 例如，虛擬物件可以用來代表儲存在資料庫中的資料。 就命名空間而言，資料庫中的各種專案可能會以個別物件的形式出現在 Windows 檔案總管中，即使它們全都儲存在單一磁片檔案中也一樣。

虛擬物件甚至可能位於遠端電腦上。 例如，為了促進漫遊，使用者的檔檔案可能會儲存在伺服器上。 為了讓使用者從多部桌上型電腦存取他們的檔案，他們目前使用的桌上型電腦上的我的檔資料夾會指向伺服器，而不是桌上型電腦的硬碟。 其路徑將包含對應的網路磁碟機機或 UNC 路徑名稱。

命名空間和檔案系統一樣，包含兩種基本類型的物件：資料夾和檔案。 資料夾物件是樹狀結構的 *節點* ;它們是檔物件和其他資料夾的容器。 檔案物件是樹狀結構的 *葉* ;它們是一般磁片檔案或虛擬物件，例如印表機連結。 不屬於檔案系統的資料夾有時稱為 *虛擬資料夾*。

如同檔系統資料夾，虛擬資料夾的集合通常會因系統而異。 虛擬資料夾有三個類別：

-   在所有系統上都能找到的標準虛擬資料夾，例如資源回收筒。
-   選用的虛擬資料夾，具有標準名稱和功能，但可能不會出現在所有系統上。
-   使用者所安裝的非標準資料夾。

不同于檔系統資料夾，使用者無法自行建立新的虛擬資料夾。 他們只能安裝非 Microsoft 開發人員所建立的使用者。 因此，虛擬資料夾的數目通常比檔系統資料夾的數目少得多。 如需如何執行虛擬資料夾的討論，請參閱 [命名空間延伸](nse-works.md)。

您可以在 Windows 檔案總管的瀏覽器列中，看到命名空間結構的視覺化標記法。 例如，下列 Windows 檔案總管的螢幕擷取畫面會顯示相對簡單的命名空間。

![顯示 shell 命名空間視圖的螢幕擷取畫面](images/prog1.png)

命名空間階層的終極根目錄是桌面。 根目錄正下方會有數個虛擬資料夾，例如我的電腦和資源回收筒。

各種磁片磁碟機的檔案系統可以被視為較大的命名空間階層的子集。 這些檔案系統的根目錄是我的電腦資料夾的子資料夾。 我的電腦也包含任何對應網路磁碟機機的根。 樹狀結構中的其他節點（例如我的檔）是虛擬資料夾。

## <a name="identifying-namespace-objects"></a>識別命名空間物件

在您可以使用命名空間物件之前，您必須先有方法可以進行識別。 檔案系統中的物件可以有 MyFile.htm 之類的名稱。 由於系統中的其他位置可能會有其他檔案，因此可唯一識別檔案或資料夾，需要完整路徑（例如 "C： \\ MyDocs \\MyFile.htm"）。 這個路徑基本上是路徑中所有資料夾的排序清單，從檔案系統根目錄（C：）以檔案 \\ 結尾。

在命名空間的內容中，路徑仍相當適合用來識別位於命名空間之檔案系統部分中的物件。 不過，它們無法用於虛擬物件。 相反地，Shell 會提供另一種可搭配任何命名空間物件使用的識別方法。

### <a name="item-ids"></a>專案識別碼

在資料夾內，每個物件都有一個 *專案識別碼*，也就是檔案或資料夾名稱的功能對等專案。 專案識別碼實際上是 [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) 結構：


```
typedef struct _SHITEMID { 
    USHORT cb; 
    BYTE   abID[1]; 
} SHITEMID, * LPSHITEMID;
```



**AbID** 成員是物件的識別碼。 未定義 **abID** 的長度，而且其值取決於包含物件的資料夾。 因為資料夾不會指派 **abID** 值的標準定義，所以它們只對相關聯的資料夾物件有意義。 應用程式應該直接將它們視為權杖，以識別特定資料夾中的物件。 由於 **abID** 的長度不同，因此 **cb** 成員會保存 [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) 結構的大小（以位元組為單位）。

因為專案識別碼對於顯示用途沒有説明，所以包含物件的資料夾通常會為它指定顯示名稱。 這是 Windows 檔案總管在顯示資料夾內容時所使用的名稱。 如需如何處理顯示名稱的詳細資訊，請參閱 [從資料夾取得資訊](folder-info.md)。

### <a name="item-id-lists"></a>專案識別碼清單

專案識別碼很少使用。 通常，它是專案識別碼清單的一部分，與檔案系統路徑的用途相同。 但是，不是路徑所使用的字元字串，而是專案 ID 清單是 [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) 結構。 此結構是一或多個專案 Id 的排序次序，以兩個位元組的 **Null** 結束。 專案識別碼清單中的每個專案識別碼都會對應至命名空間物件。 它們的順序定義了命名空間中的路徑，與檔案系統路徑很類似。

下圖顯示對應至 C： MyDocsMyFile.htm 之 [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) 結構的示意標記法 \\ \\ 。 每個專案識別碼的顯示名稱會顯示在其上方。 不同的 **abID** 成員寬度是任意的;它們說明這個成員的大小可能不同的事實。

![pidl 的圖解圖解](images/shell2.png)

### <a name="pidls"></a>Pidl

針對 Shell API，命名空間物件通常是以其 [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) 結構的指標來識別，或指向專案識別碼清單的指標， (PIDL) 。 為了方便起見，PIDL 一詞通常會在此檔中參考結構本身，而不是指向它的指標。

上圖所示的 PIDL 稱為 *full* 或 *絕對* PIDL。 完整 PIDL 會從桌面開始，並包含路徑中所有中繼資料夾的專案識別碼。 它的結尾是物件的專案識別碼，後面接著終止的雙位元組 **Null**。 完整的 PIDL 與完整路徑類似，並且可唯一識別 Shell 命名空間中的物件。

不常使用完整 Pidl。 許多函式和方法都需要 *相對 PIDL*。 相對 PIDL 的根目錄是資料夾，而不是桌面。 如同相對路徑，組成結構的專案識別碼系列會在命名空間中定義兩個物件之間的路徑。 雖然它們無法唯一識別物件，但它們通常會小於完整 PIDL，而且足以滿足許多用途。

最常使用的相對 Pidl （ *單一層級 pidl*）是相對於物件的父資料夾。 它們只包含物件的專案識別碼和終止的 **Null**。 多層級的 Pidl 也可用於許多用途。 它們包含兩個或多個專案識別碼，通常會透過一或多個子資料夾的一連串，定義從父資料夾到物件的路徑。 請注意，單一層級的 PIDL 仍然可以是完整的 PIDL。 尤其是桌面物件是桌面的子系，因此其完整 Pidl 只包含一個專案識別碼。

如同 [取得資料夾識別碼](folder-id.md)所述，Shell API 提供了許多方法來取得物件的 PIDL。 一旦有了此功能，您通常只會在呼叫其他 Shell API 函式和方法時，使用它來識別物件。 在此內容中，PIDL 的內部內容不透明且不相關。 基於此討論的目的，請將 Pidl 視為代表特定命名空間物件的權杖，並將焦點放在如何將它們用於一般工作。

### <a name="allocating-pidls"></a>配置 Pidl

雖然 Pidl 與路徑有一些相似之處，但使用它們需要稍微不同的方法。 主要差異在於如何為它們配置和解除配置記憶體。

就像路徑所用的字串一樣，必須為 PIDL 配置記憶體。 如果應用程式建立 PIDL，則必須為 [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) 結構配置足夠的記憶體。 在這裡討論的大部分案例中，Shell 會建立 PIDL 並處理記憶體配置。 無論配置 PIDL 的內容為何，應用程式通常會在不再需要時，負責將 PIDL 解除配置。

您可以使用 [**CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc) 函式來配置 PIDL，並使用 [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) 函式將它解除配置。

 

 
