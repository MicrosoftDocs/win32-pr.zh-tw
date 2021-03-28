---
description: 執行命名空間延伸的程式類似于任何其他同進程元件物件模型 (COM) 物件。
title: 執行基本資料夾物件介面
ms.topic: article
ms.date: 05/31/2018
ms.assetid: a45b8011-5355-429b-8935-4a7bdb5d2316
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c05f5d2e4c21a923856c7324ad2d407230fa7595
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973373"
---
# <a name="implementing-the-basic-folder-object-interfaces"></a>執行基本資料夾物件介面

執行命名空間延伸的程式類似于任何其他同進程元件物件模型 (COM) 物件。 所有延伸模組都必須支援三個主要介面，為 Windows 檔案總管提供在樹狀檢視中顯示延伸模組資料夾所需的基本資訊。 不過，若要充分利用 Windows 檔案總管的功能，您的延伸模組也必須公開一個或多個選用的介面，以支援更複雜的功能，例如快速鍵功能表或拖放功能，以及提供資料夾檢視。

本檔將討論如何執行 Windows 檔案總管呼叫您的延伸模組內容相關資訊的主要和選用介面。 如需如何執行資料夾檢視和如何自訂 Windows 檔案總管的討論，請參閱 [執行資料夾檢視](../lwef/nse-folderview.md)。

-   [基本執行和註冊](#basic-implementation-and-registration)
    -   [註冊擴充功能](#registering-an-extension)
-   [處理 Pidl](#handling-pidls)
    -   [建立 SHITEMID 結構](#creating-an-shitemid-structure)
    -   [建立 PIDL](#constructing-a-pidl)
    -   [解讀 Pidl](#interpreting-pidls)
-   [執行主要介面](#implementing-the-primary-interfaces)
    -   [IPersistFolder 介面](#ipersistfolder-interface)
    -   [IShellFolder 介面](#ishellfolder-interface)
    -   [IEnumIDList 介面](#ienumidlist-interface)
-   [執行選用介面](#implementing-the-optional-interfaces)
    -   [IExtractIcon](#iextracticon)
    -   [ICoNtextMenu](#icontextmenu)
    -   [IQueryInfo](#iqueryinfo)
    -   [IDataObject 和 IDropTarget](#idataobject-and-idroptarget)
-   [使用預設的 Shell 資料夾檢視執行](#working-with-the-default-shell-folder-view-implementation)

## <a name="basic-implementation-and-registration"></a>基本執行和註冊

作為同進程 COM 伺服器，您的 DLL 必須公開數個標準函式和介面：

-   [**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow)
-   [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject)
-   [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)
-   [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)

這些函式和介面的實與大部分其他 COM 物件的執行方式相同。 如需詳細資訊，請參閱 [COM 檔](../com/the-component-object-model.md)。

### <a name="registering-an-extension"></a>註冊擴充功能

如同所有 COM 物件，您必須為您的延伸模組建立 (CLSID) GUID 的類別識別碼。 藉由針對延伸模組的 CLSID，建立名為的 **HKEY \_ 類別 \_ 根** CLSID 的子機碼，以註冊物件 \\  。 DLL 應該註冊為同進程伺服器，而且應該指定單元執行緒模型。 您可以藉由將各種子機碼和值新增至延伸模組的 CLSID 機碼，來自訂延伸模組根資料夾的行為。

其中有幾個值僅適用于具有虛擬連接點的擴充功能。 這些值不適用於連接點為檔系統資料夾的延伸模組。 如需進一步討論，請參閱 [指定命名空間延伸模組的位置](nse-junction.md)。 若要使用虛擬連接點來修改擴充功能的行為，請將下列一或多個值新增至延伸模組的 CLSID 索引鍵：

-   WantsFORPARSING. 具有虛擬連接點的延伸模組剖析名稱通常會有格式：： {*GUID*}。 此類型的延伸模組通常包含虛擬專案。 不過，某些延伸模組（例如我的檔）實際上會對應到檔系統資料夾，即使它們有虛擬連接點也一樣。 如果您的延伸模組以這種方式表示檔案系統物件，您可以設定 WantsFORPARSING 值。 Windows 檔案總管接著會呼叫資料夾物件的 [**IShellFolder：： GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) 方法，並將 *UFlags* 設定為 **SHGDN \_ FORPARSING** ，並將 *pidl* 設定為專案識別碼清單 (pidl) 的單一空白指標，藉此要求根資料夾的剖析名稱。 空的 PIDL 僅包含結束字元。 然後，您的方法應該會傳回根資料夾的：： {*GUID*} 剖析名稱。
-   HideFolderVerbs. 在 **HKEY \_ 類別 \_ 根** 資料夾下註冊的動詞 \\ 通常會與所有延伸模組相關聯。 它們會出現在擴充功能的快捷方式功能表上，可由 [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)叫用。 若要防止任何這些動詞與您的延伸模組相關聯，請設定 HideFolderVerbs 值。
-   HideAsDelete. 如果使用者嘗試刪除您的延伸模組，Windows 檔案總管會改為隱藏延伸模組。
-   HideAsDeletePerUser. 此值的效果與 HideAsDelete 相同，但以每個使用者為基礎。 只有已嘗試刪除的使用者，才會隱藏此延伸模組。 所有其他使用者都可以看到此延伸模組。
-   QueryForOverlay. 設定此值以指出根資料夾的圖示可以有圖示重迭。 資料夾物件必須支援 [**IShellIconOverlay**](/windows/win32/api/shlobj_core/nn-shlobj_core-ishelliconoverlay) 介面。 在 Windows 檔案總管顯示根資料夾的圖示之前，它會呼叫兩個 **IShellIconOverlay** 方法的其中一個，並將 *pidlItem* 設定為空白 PIDL，以要求重迭圖示。

其餘的值和子機碼適用于所有延伸模組：

-   若要指定延伸模組的連接點資料夾的顯示名稱，請將擴充功能的 CLSID 子機碼預設值設定為適當的字串。
-   當游標停留在資料夾上時，通常會顯示描述資料夾內容的提示。 若要為您的延伸模組根資料夾提供提示，請建立延伸模組之 CLSID 索引鍵的提示字元 **REG \_** 值，並將它設定為適當的字串。
-   若要為您的延伸模組根資料夾指定自訂圖示，請建立名為 **DefaultIcon** 的延伸模組 CLSID 子機碼的子機碼。 將 **DefaultIcon** 的預設值設定為 **REG \_ SZ** 值，其中包含包含圖示之檔案的名稱，後面接著一個逗號，後面接著減號，後面接著該檔案中的圖示索引。
-   根據預設，擴充功能根資料夾的快捷方式功能表將包含在 [ **HKEY \_ 類別 \_ 根 \\ 資料夾**] 底下定義的專案。 如果您已設定適當的 SFGAO XXX 旗標，則會新增 [ **刪除**]、[ **重新命名**] 和 [ **屬性** ] 專案 \_ 。 您可以將其他專案新增至根資料夾的快捷方式功能表，或覆寫現有的專案，就像您針對 [檔案類型](fa-file-types.md)所做的一樣。 在延伸模組的 CLSID 機碼底下建立 **Shell** 子機碼，並定義命令，如 [擴充快速鍵功能表](context.md)中所述。
-   如果您需要更有彈性的方式來處理根資料夾的快捷方式功能表，您可以執行 [快捷方式功能表處理常式](context-menu-handlers.md)。 若要註冊快捷方式功能表處理常式，請在擴充功能的 CLSID 機碼底下建立 **ShellEx** 索引鍵。 如同傳統 [建立 Shell 延伸模組處理常式](handlers.md)一樣，註冊處理常式的 CLSID。
-   若要將頁面加入至根資料夾的 [屬性] 屬性工作表中，請為資料夾提供 **SFGAO \_ HASPROPSHEET** 屬性，並執行 [屬性工作表處理常式](propsheet-handlers.md)。 若要註冊屬性工作表處理常式，請在擴充功能的 CLSID 機碼底下建立 **ShellEx** 索引鍵。 如同傳統 [建立 Shell 延伸模組處理常式](handlers.md)一樣，註冊處理常式的 CLSID。
-   若要指定根資料夾的屬性，請將 **ShellFolder** 子機碼新增至延伸模組的 CLSID 子機碼。 建立屬性值，並將它設定為適當的 [**SFGAO \_ XXX**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof) 旗標組合。

下表列出根資料夾的一些常用屬性。



| 旗標                | 值      | 描述                                                                                                                                                                                                                                                                                                       |
|---------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SFGAO \_ 資料夾       | 0x20000000 | 擴充功能的根資料夾包含一或多個專案。                                                                                                                                                                                                                                                           |
| SFGAO \_ HASSUBFOLDER | 0x80000000 | 擴充功能的根資料夾包含一或多個子資料夾。 Windows 檔案總管會在資料夾圖示旁邊放置一個加號 ( + ) 。                                                                                                                                                                               |
| SFGAO \_ CANDELETE    | 0x00000020 | 使用者可以刪除擴充功能的根資料夾。 資料夾的快捷方式功能表會有 [ **刪除** ] 專案。 此旗標應針對放置於其中一個 [虛擬資料夾](nse-junction.md)下的連接點進行設定。                                                                                 |
| SFGAO \_ CANRENAME    | 0x00000010 | 使用者可以重新命名延伸的根資料夾。 資料夾的快捷方式功能表會有 [ **重新命名** ] 專案。                                                                                                                                                                                                   |
| SFGAO \_ HASPROPSHEET | 0x00000040 | 擴充功能的根資料夾具有 [ **屬性** ] 屬性工作表。 資料夾的快捷方式功能表將會有 **屬性** 專案。 若要提供屬性工作表，您必須執行 [屬性工作表處理常式](propsheet-handlers.md)。 如先前所述，在擴充功能的 CLSID 機碼下註冊處理常式。 |



 

下列範例會顯示名稱為 MyExtension 之延伸模組的 CLSID 登錄專案。 擴充功能有一個自訂圖示，其包含在具有索引1的延伸模組 DLL 中。 已設定 **SFGAO \_ 資料夾**、 **SFGAO \_ HASSUBFOLDER** 和 **SFGAO \_ CANDELETE** 屬性。

```
HKEY_CLASSES_ROOT
   CLSID
      {Extension CLSID}
         (Default) = MyExtension
         InfoTip = Some appropriate text
      DefaultIcon
         (Default) = c:\MyDir\MyExtension.dll,-1
      InProcServer32
         (Default) = c:\MyDir\MyExtension.dll
         ThreadingModel = Apartment
      ShellFolder
         Attributes = 0xA00000020
```

## <a name="handling-pidls"></a>處理 Pidl

Shell 命名空間中的每個專案都必須有唯一的 PIDL。 Windows 檔案總管將 PIDL 指派給根資料夾，並在初始化期間將值傳遞至您的延伸模組。 然後，您的擴充功能會負責將正確建立的 PIDL 指派給它的每一個物件，並提供這些 Pidl 來 Windows 檔案總管要求。 當 Shell 使用 PIDL 來識別您的其中一個延伸模組物件時，您的延伸模組必須能夠解讀 PIDL 並識別特定的物件。 您的延伸模組也必須將 [**顯示名稱**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-setnameof) 和 *剖析名稱* 指派給每個物件。 由於 Pidl 是由幾乎每個資料夾介面使用，因此擴充功能通常會執行單一 *PIDL 管理員* 來處理所有這些工作。

PIDL 一詞是 [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) 結構的縮寫，或是這類結構的指標（視內容而定）。 如同宣告， **ITEMIDLIST** 結構具有單一成員（ [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) 結構）。 物件的 **ITEMIDLIST** 結構實際上是兩個或多個 **SHITEMID** 結構的封裝陣列。 這些結構的順序會定義透過命名空間的路徑，與 c： \\ MyDirectory \\ myfile.txt 定義整個檔案系統路徑的方式大致相同。 一般而言，物件的 PIDL 會包含一系列的 **SHITEMID** 結構，這些結構會對應到定義命名空間路徑的資料夾，後面接著物件的 **SHITEMID** 結構，後面接著結束字元。

結束字元是 [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) 結構，其 *cb* 成員設為 **Null**。 結束字元是必要的，因為物件 PIDL 中的 **SHITEMID** 結構數目取決於 Shell 命名空間中物件的位置，以及路徑的起點。 此外，各種 **SHITEMID** 結構的大小可能會有所不同。 當您收到 PIDL 時，您沒有簡單的方法可以判斷其大小，甚至是 **SHITEMID** 結構的總數。 相反地，您必須在到達結束字元之前，以結構的結構來「逐步」封裝的陣列。

若要建立 PIDL，您的應用程式必須：

1.  為每個物件建立 [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) 結構。
2.  將相關的 [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) 結構組合成 PIDL。

### <a name="creating-an-shitemid-structure"></a>建立 SHITEMID 結構

物件的 [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) 結構可唯一地識別其資料夾內的物件。 事實上，許多 [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) 方法所使用的 PIDL 類型只包含物件的 **SHITEMID** 結構，後面接著結束字元。 **SHITEMID** 結構的定義如下：


```C++
typedef struct _SHITEMID { 
    USHORT cb; 
    BYTE   abID[1]; 
} SHITEMID, * LPSHITEMID;
```



*AbID* 成員是物件的識別碼。 因為 *abID* 的長度並未定義且可能不同，所以 *cb* 成員會設定為 [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) 結構的大小（以位元組為單位）。

因為 *abID* 的長度和內容都不是標準化的，所以您可以使用任何您想要指派 *abID* 值給物件的配置。 唯一的需求是，您不能在相同的資料夾中有兩個具有相同值的物件。 不過，基於效能考慮，您的 [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) 結構應為 **DWORD** 對齊。 換句話說，您應該建立 *abID* 值，讓 *cb* 成為4的整數倍數。

一般而言， *abID* 會指向擴充功能定義的結構。 除了物件的識別碼之外，這個結構通常用來保存各種相關資訊，例如物件的型別或屬性。 然後，您的擴充功能資料夾物件可以從 PIDL 快速解壓縮資訊，而不需要查詢它。

> [!Note]  
> 設計 PIDL 資料結構的其中一個最重要層面，就是讓結構能夠持久且可轉移。 在 Pidl 的內容中，這些詞彙的意義如下：
>
> -   持久. 系統經常會將 Pidl 放在各種類型的長期儲存體中，例如快速鍵檔。 然後，它可以在系統重新開機之後，稍後再從儲存體復原這些 Pidl。 從儲存體復原的 PIDL 仍然必須有效且對您的延伸模組有意義。 這項需求表示，您不應該在 PIDL 結構中使用指標或控制碼。 當系統稍後從儲存體復原時，包含這種資料類型的 Pidl 通常會沒有意義。
> -   運輸。 從一部電腦傳輸到另一部電腦時，PIDL 必須保持有意義。 例如，PIDL 可以寫入至快捷方式檔案，複製到磁片磁碟機，然後傳輸到另一部電腦。 該 PIDL 對您在第二部電腦上執行的延伸模組仍然有意義。 例如，若要確保您的 Pidl 可轉移，請明確使用 ANSI 或 Unicode 字元。 避免資料類型，例如 **TCHAR** 或 **LPTSTR**。 如果您使用這些資料類型，在不同電腦上執行之延伸模組的 ANSI 版本將無法讀取在執行副檔名 Unicode 的電腦上所建立的 PIDL。

 

下列宣告顯示資料結構的簡單範例。


```C++
typedef struct tagMYPIDLDATA {
  USHORT cb;
  DWORD dwType;
  WCHAR wszDisplayName[40];
} MYPIDLDATA, *LPMYPIDLDATA;
```



**Cb** 成員會設定為 **MYPIDLDATA** 結構的大小。 這個成員會使 **MYPIDLDATA** 成為有效的 [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) 結構，也就是本身的。 其餘成員等同于 **SHITEMID** 結構的 **abID** 成員並保存私用資料。 **DwType** 成員是延伸模組定義的值，表示物件的型別。 在此範例中，資料夾的 **dwType** 設為 **TRUE** ，否則為 **FALSE** 。 例如，這個成員可讓您快速判斷物件是否為資料夾。 **WszDisplayName** 成員包含物件的顯示名稱。 由於您不會將相同的顯示名稱指派給相同資料夾中的兩個不同物件，因此顯示名稱也會當做物件識別碼。 在此範例中， **wszDisplayName** 會設定為40個字元，以保證 **SHITEMID** 結構會對齊 **DWORD**。 若要限制 Pidl 的大小，您可以改為使用可變長度的字元陣列，並據以調整 cb 的值。 以足夠的 ' \\ 0 ' 字元填補顯示字串，以維護結構的 **DWORD** 對齊。 其他可能有助於放置結構的成員包括物件的大小、屬性或剖析名稱。

### <a name="constructing-a-pidl"></a>建立 PIDL

一旦為物件定義了 [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) 結構之後，您就可以使用它們來建立 PIDL。 Pidl 可基於各種用途來建立，但大部分的工作會使用兩種 PIDL 類型的其中一種。 最簡單的單一層級 PIDL 會識別相對於其父資料夾的物件。 許多 [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) 方法會使用這種類型的 PIDL。 單一層級的 PIDL 包含物件的 **SHITEMID** 結構，後面接著結束字元。 完整的 PIDL 會定義從桌面到物件的命名空間階層路徑。 這種類型的 PIDL 會從桌面開始，並且針對路徑中的每個資料夾包含一個 **SHITEMID** 結構，後面接著物件和結束字元。 完整的 PIDL 可唯一識別整個 Shell 命名空間內的物件。

若要建立 PIDL，最簡單的方法就是直接使用 [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) 結構本身。 建立 **ITEMIDLIST** 結構，但配置足夠的記憶體來保存所有 [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) 結構。 此結構的位址會指向初始 **SHITEMID** 結構。 為此初始結構的成員定義值，然後以適當的順序附加所需數量的額外 **SHITEMID** 結構。 下列程式概述如何建立單一層級的 PIDL。 它包含兩個 **SHITEMID** 結構- **MYPIDLDATA** 結構後面接著結束字元：

1.  您可以使用 [**CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc) 函數來配置 PIDL 的記憶體。 為您的私用資料配置足夠的記憶體，再加上 **USHORT** (兩個位元組) 作為結束字元。 將結果轉換為 LPMYPIDLDATA。
2.  將第一個 **MYPIDLDATA** 結構的 cb 成員設定為該結構的大小。 在此範例中，您會將 **cb** 設定為 SIZEOF (MYPIDLDATA) 。 如果您想要使用可變長度的結構，就必須計算 **cb** 的值。
3.  將適當的值指派給私用資料成員。
4.  計算下一個 [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) 結構的位址。 將目前 MYPIDLDATA 結構的位址轉換為 LPBYTE，並將該值新增至在步驟3中判斷的 **cb** 值。
5.  在此案例中，下一個 [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) 結構是結束字元。 將結構的 **cb** 成員設定為零。

針對較長的 Pidl，請配置足夠的記憶體，然後針對每個額外的 [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) 結構重複步驟3-5。

下列範例函式會採用物件的類型和顯示名稱，並傳回物件的單一層級 PIDL。 函數假設顯示名稱（包括其結束的 **null** 字元）不超過針對 **MYPIDLDATA** 結構宣告的字元數。 如果該假設結果是錯誤的， [**StringCbCopyW**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopya) 函式將會截斷顯示名稱。 **G \_ pMalloc** 變數是在其他地方建立並儲存在全域變數中的 [**IMalloc**](/windows/win32/api/objidlbase/nn-objidlbase-imalloc)指標。


```C++
LPITEMIDLIST CreatePIDL(DWORD dwType, LPCWSTR pwszDisplayName)
{
    LPMYPIDLDATA   pidlOut;
    USHORT         uSize;

    pidlOut = NULL;

    //Calculate the size of the MYPIDLDATA structure.
    uSize = sizeof(MYPIDLDATA);

    // Allocate enough memory for the PIDL to hold a MYPIDLDATA structure 
    // plus the terminator
    pidlOut = (LPMYPIDLDATA)m_pMalloc->Alloc(uSize + sizeof(USHORT));

    if(pidlOut)
    {
       //Assign values to the members of the MYPIDLDATA structure
       //that is the PIDL's first SHITEMID structure
       pidlOut->cb = uSize;
       pidlOut->dwType = dwType;
       hr = StringCbCopyW(pidlOut->wszDisplayName, 
                          sizeof(pidlOut->wszDisplayName), pwszDisplayName);
       
       // TODO: Add error handling here to verify the HRESULT returned 
       // by StringCbCopyW.

       //Advance the pointer to the start of the next SHITEMID structure.
       pidlOut = (LPMYPIDLDATA)((LPBYTE)pidlOut + pidlOut->cb);

       //Create the terminating null character by setting cb to 0.
       pidlOut->cb = 0;
    }

    return pidlOut;
```



完整的 PIDL 必須將每個物件的 [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) 結構，從桌面連接到您的物件。 當 Shell 呼叫 [**IPersistFolder：： Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder-initialize)時，您的擴充功能會收到根資料夾的完整 PIDL。 若要建立物件的完整 PIDL，請取得 Shell 已指派給根資料夾的 PIDL，然後將您從根資料夾中取得的 **SHITEMID** 結構附加至物件。

### <a name="interpreting-pidls"></a>解讀 Pidl

當 Shell 或應用程式呼叫其中一個擴充功能介面來要求物件的相關資訊時，通常會透過 PIDL 來識別物件。 某些方法（例如 [**IShellFolder：： GetUIObjectOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof)）會使用相對於父資料夾的 pidl，而且很容易解讀。 不過，您的延伸模組可能也會收到完整的 Pidl。 然後，您的 PIDL manager 必須判斷 PIDL 參考的物件。

將物件與完整 PIDL 相關聯的工作會變得更複雜，那就是 PIDL 中的一或多個初始 [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) 結構可能屬於在 Shell 命名空間的延伸範圍之外的物件。 您沒有辦法解讀這些結構的 *abID* 成員意義。 您的延伸模組必須做的就是「逐步」 **SHITEMID** 結構清單，直到您到達對應到根資料夾的結構為止。 接著，您將瞭解如何解讀 **SHITEMID** 結構中的資訊。

若要進行 PIDL，請採用第一個 *cb* 值，並將它新增至 PIDL 的位址，以將指標前進至下一個 [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) 結構的開頭。 然後，它會指向該結構的 *cb* 成員，您可以使用此成員將指標前進到下一個 **SHITEMID** 結構的開頭，依此類推。 每次您前進指標時，請檢查 **SHITEMID** 結構，以判斷您是否已到達延伸模組命名空間的根目錄。

## <a name="implementing-the-primary-interfaces"></a>執行主要介面

如同所有 COM 物件，執行擴充功能的方式大多是執行介面集合。 本節討論所有延伸模組都必須執行的三個主要介面。 它們是用來初始化和提供 Windows 檔案總管，其中包含有關延伸模組內容的基本資訊。 這些介面和 [資料夾檢視](../lwef/nse-folderview.md)都是功能延伸模組所需的所有介面。 不過，若要充分利用 Windows 檔案總管的功能，大部分的延伸模組也會執行一或多個選用的介面。

### <a name="ipersistfolder-interface"></a>IPersistFolder 介面

呼叫 [**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) 介面來初始化新的資料夾物件。 [**IPersistFolder：： Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder-initialize)方法會將完整的 PIDL 指派給新的物件。 儲存此 PIDL 以供稍後使用。 例如，資料夾物件必須使用這個 PIDL 來為物件的子系建立完整的 Pidl。 資料夾物件的建立者也可以呼叫 [**IPersist：： GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) 來要求物件的 CLSID。

一般而言，資料夾物件是由其父資料夾的 [**IShellFolder：： BindToObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) 方法建立和初始化。 不過，當使用者流覽至您的延伸模組時，Windows 檔案總管會建立並初始化擴充功能的根資料夾物件。 根資料夾物件透過 [**IPersistFolder：： Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder-initialize) 接收的 PIDL 包含從桌面到根資料夾的路徑，您將必須為您的延伸模組建立完整的 pidl。

### <a name="ishellfolder-interface"></a>IShellFolder 介面

Shell 會將擴充功能視為資料夾物件的階層式排序集合。 [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder)介面是任何延伸模組執行的核心。 它代表資料夾物件，並提供 Windows 檔案總管所需的大部分資訊，以顯示資料夾的內容。

[**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) 通常是資料夾物件直接公開之 [**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) 以外的唯一資料夾介面。 雖然 Windows 檔案總管使用各種必要和選用的介面來取得資料夾內容的相關資訊，但它會透過 **IShellFolder** 取得這些介面的指標。

Windows 檔案總管會以各種不同的方式取得延伸模組根資料夾的 CLSID。 如需詳細資訊，請參閱 [指定命名空間延伸的位置](nse-junction.md) 或 [顯示命名空間延伸模組的 Self-Contained 視圖](nse-view.md)。 Windows 檔案總管接著會使用該 CLSID 來建立和初始化根資料夾的實例，並查詢 [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) 介面。 您的擴充功能會建立資料夾物件來代表根資料夾，並傳回物件的 **IShellFolder** 介面。 擴充功能與 Windows 檔案總管之間的大部分互動都是透過 **IShellFolder** 進行。 Windows 檔案總管會呼叫 **IShellFolder** 以：

-   要求可以列舉根資料夾內容的物件。
-   取得根資料夾內容的各種資訊類型。
-   要求公開其中一個選用介面的物件。 然後可以查詢這些介面，以取得其他資訊，例如圖示或快捷方式功能表。
-   要求一個資料夾物件，代表根資料夾的子資料夾。

當使用者開啟根資料夾的子資料夾時，Windows 檔案總管會呼叫 [**IShellFolder：： BindToObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject)。 您的擴充功能會建立並初始化新的資料夾物件，以代表子資料夾並傳回其 [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) 介面。 Windows 檔案總管接著會針對各種類型的資訊呼叫這個介面，依此類推，直到使用者決定在 Shell 命名空間中的其他位置流覽或關閉 Windows 檔案總管為止。

本節的其餘部分將簡短討論更重要的 [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) 方法，以及如何執行這些方法。

### <a name="enumobjects"></a>EnumObjects

在樹狀檢視中顯示資料夾的內容之前，Windows 檔案總管必須先藉由呼叫 [**IShellFolder：： EnumObjects**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects) 方法來判斷資料夾包含的內容。 這個方法會建立一個標準的 OLE 列舉物件，此物件會公開 [**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) 介面並傳回該介面指標。 **IEnumIDList** 介面可讓 Windows 檔案總管取得資料夾所包含之所有物件的 pidl。 這些 Pidl 接著會用來取得資料夾所包含之物件的相關資訊。 如需詳細資訊，請參閱 [IEnumIDList 介面](#ienumidlist-interface)。

> [!Note]  
> [**IEnumIDList：： Next**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-next)方法應該只傳回相對於父資料夾的 pidl。 PIDL 只能包含物件的 [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) 結構，後面接著結束字元。

 

### <a name="createviewobject"></a>CreateViewObject

在顯示資料夾的內容之前，Windows 檔案總管會呼叫這個方法來要求 [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) 介面的指標。 Windows 檔案總管使用此介面來管理資料夾檢視。 建立資料夾 view 物件，並傳回其 **IShellView** 介面。

也會呼叫 [**IShellFolder：： CreateViewObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-createviewobject) 方法來要求資料夾本身的其中一個選用介面，例如 [**ICoNtextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)。 您的這個方法的執行應該建立一個物件，此物件會公開所要求的介面，並傳回介面指標。 如果 Windows 檔案總管需要資料夾所包含的其中一個物件的選擇性介面，則會呼叫 [**IShellFolder：： GetUIObjectOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof)。

### <a name="getuiobjectof"></a>GetUIObjectOf

雖然您可以透過 [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) 方法使用資料夾內容的基本資訊，但您的延伸模組也可以提供不同類型的額外資訊 Windows 檔案總管。 例如，您可以指定資料夾內容或物件快捷方式功能表的圖示。 Windows 檔案總管會呼叫 [**IShellFolder：： GetUIObjectOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof) 方法，以嘗試抓取資料夾所包含之物件的其他資訊。 Windows 檔案總管指定要取得資訊的物件，以及相關介面的 IID。 資料夾物件接著會建立物件，此物件會公開所要求的介面，並傳回介面指標。

如果您的延伸模組允許使用者使用拖放或剪貼簿來傳送物件，Windows 檔案總管會呼叫 [**IShellFolder：： GetUIObjectOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof) 來要求 [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) 或 [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) 介面。 如需詳細資訊，請參閱 [使用拖放和剪貼簿來傳送 Shell 物件](dragdrop.md)。

Windows 檔案總管會在需要與資料夾本身相同的資訊類型時，呼叫 [**IShellFolder：： CreateViewObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-createviewobject) 。

### <a name="bindtoobject"></a>BindToObject

當使用者嘗試開啟您的其中一個延伸的子資料夾時，Windows 檔案總管會呼叫 [**IShellFolder：： BindToObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) 方法。 如果 *riid* 設定為 IID \_ IShellFolder，您應該建立並初始化代表子資料夾的資料夾物件，並傳回物件的 [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) 介面。

> [!Note]  
> 目前，Windows 檔案總管只會呼叫這個方法來要求 [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) 介面。 但是，請勿假設這種情況一律會是如此。 您應該一律先檢查 *riid* 的值，再繼續進行。

 

### <a name="getdisplaynameof"></a>GetDisplayNameOf

Windows 檔案總管會呼叫 [**IShellFolder：： GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) 方法，將其中一個資料夾物件的 PIDL 轉換成名稱。 該 PIDL 必須相對於物件的父資料夾。 換句話說，它必須包含單一非 **Null** 的 [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) 結構。 因為有一個以上的方法可以命名物件，Windows 檔案總管藉由在 *uFlags* 參數中設定一或多個 [**SHGDNF**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shgdnf)旗標來指定名稱的類型。 **SHGDN \_ NORMAL** 或 **SHGDN \_ INFOLDER** 這兩個值的其中一個，將設定為指定名稱是否應相對於資料夾或相對於桌面。 您可以設定其他三個值的其中之一： **SHGDN \_ FOREDITING**、 **SHGDN \_ FORADDRESSBAR** 或 **SHGDN \_ FORPARSING**，以指定名稱將使用的名稱。

您必須以 [**STRRET**](/windows/desktop/api/Shtypes/ns-shtypes-strret) 結構的形式傳回名稱。 如果未設定 **SHGDN \_ FOREDITING**、 **SHGDN \_ FORADDRESSBAR** 和 **SHGDN \_ FORPARSING** ，則會傳回物件的顯示名稱。 如果已設定 **SHGDN \_ FORPARSING** 旗標，Windows 檔案總管會要求剖析名稱。 剖析名稱會傳遞至 [**IShellFolder：:P arsedisplayname**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) 來取得物件的 PIDL，即使它可能位於命名空間階層中目前資料夾的一或多個層級，也是一樣。 例如，檔案系統物件的剖析名稱是它的路徑。 您可以將檔案系統中任何物件的完整路徑傳遞至桌面的 **IShellFolder：:P arsedisplayname** 方法，它會傳回物件的完整 PIDL。

雖然剖析名稱是文字字串，但不一定要包含顯示名稱。 當呼叫 IShellFolder 時，您應該根據最有效率的運作方式來指派剖析名稱 [**：:P arsedisplayname**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) 。 比方說，許多 Shell 的虛擬資料夾不是檔案系統的一部分，而且沒有完整路徑。 相反地，會將 GUID 指派給每個資料夾，而且剖析名稱的格式如下：： {GUID}。 無論您使用何種配置，都應該能夠可靠地「往返」。 比方說，如果呼叫者將剖析名稱傳遞給 **IShellFolder：:P arsedisplayname** 抓取物件的 PIDL，然後將該 PIDL 傳遞給 [**IShellFolder：： GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) ，並設定 **SHGDN \_ FORPARSING** 旗標，則呼叫端應該復原原始剖析名稱。

### <a name="getattributesof"></a>GetAttributesOf

Windows 檔案總管會呼叫 [**IShellFolder：： GetAttributesOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof) 方法來判斷資料夾物件所包含的一或多個專案的屬性。 *Cidl* 的值會提供查詢中的專案數，而 *aPidl* 則會指向其 pidl 的清單。

因為某些屬性的測試可能相當耗時，Windows 檔案總管通常會在 *rfgInOut* 中設定其值，以將查詢限制為可用旗標的子集。 您的方法應該只測試在 *rfgInOut* 中設定旗標的屬性。 保留有效的旗標集，並清除餘數。 如果查詢中包含一個以上的專案，請只設定適用于所有專案的旗標。

> [!Note]  
> 必須正確設定屬性，才能正確顯示專案。 比方說，如果專案是包含子資料夾的資料夾，您必須設定 **SFGAO \_ HASSUBFOLDER** 旗標。 否則，Windows 檔案總管不會在樹狀檢視中顯示專案圖示旁的 +。

 

### <a name="parsedisplayname"></a>ParseDisplayName

[**IShellFolder：:P arsedisplayname**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname)方法在某種意義上是 [**IShellFolder：： GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof)的鏡像影像。 這個方法最常見的用法是將物件的剖析名稱轉換成相關聯的 PIDL。 剖析名稱可以參考位於命名空間階層中資料夾底下的任何物件。 傳回的 PIDL 是相對於公開方法的資料夾物件，而且通常不是完整的。 換句話說，雖然 PIDL 可以包含數個 [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) 結構，但第一個是物件本身或路徑中的第一個子資料夾，也就是該物件的資料夾。 呼叫端必須將此 PIDL 附加至資料夾的完整 PIDL，才能取得物件的完整 PIDL。

[**IShellFolder：**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) 也可以呼叫:P arsedisplayname 來要求物件的屬性。 由於判斷所有適用的屬性可能相當耗時，因此呼叫者只會設定代表呼叫者感興趣之資訊的 [**SFGAO \_ XXX**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof) 旗標。 您應判斷物件的哪些屬性是 true，並清除其餘的旗標。

### <a name="ienumidlist-interface"></a>IEnumIDList 介面

當 Windows 檔案總管需要列舉資料夾所包含的物件時，它會呼叫 [**IShellFolder：： EnumObjects**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects)。 資料夾物件必須建立公開 [**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) 介面的列舉物件，並傳回該介面指標。 然後，Windows 檔案總管通常會使用 **IEnumIDList** 來列舉資料夾所包含之所有物件的 pidl。

[**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) 是標準的 OLE 列舉介面，並且會以一般方式執行。 不過請記住，您傳回的 Pidl 必須相對於資料夾，而且只包含物件的 [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) 結構和結束字元。

## <a name="implementing-the-optional-interfaces"></a>執行選用介面

有一些選用的 Shell 介面可供延伸模組的資料夾物件支援。 其中有許多專案（例如 [**IExtractIcon**](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona)）可讓您自訂使用者查看延伸模組的方式的各種層面。 其他（例如 [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject)）可讓您的延伸模組支援拖放功能。

資料夾物件不會直接公開任何選用的介面。 相反地，Windows 檔案總管會呼叫兩個 [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) 方法的其中一個來要求介面：

-   Windows 檔案總管會呼叫資料夾物件的 [**IShellFolder：： GetUIObjectOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof) ，以針對該資料夾所包含的其中一個物件要求介面。
-   Windows 檔案總管會呼叫資料夾物件的 [**IShellFolder：： CreateViewObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-createviewobject) 來要求資料夾本身的介面。

為了提供資訊，folder 物件會建立公開所要求介面的物件，並傳回介面指標。 Windows 檔案總管接著會呼叫該介面以取得所需的資訊。 本節將討論最常使用的選用介面。

### <a name="iextracticon"></a>IExtractIcon

Windows 檔案總管會在顯示資料夾內容之前要求 [**IExtractIcon**](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona) 介面。 介面可讓您的延伸模組為資料夾所包含的物件指定自訂圖示。 否則，將會使用標準的檔案和資料夾圖示。 若要提供自訂圖示，請建立顯示 **IExtractIcon** 的圖示抽取物件，並將指標傳回至該介面。 如需進一步討論，請參閱 **IExtractIcon** 參考檔或 [建立圖示處理常式](./how-to-create-icon-handlers.md)。

### <a name="icontextmenu"></a>ICoNtextMenu

當使用者以滑鼠右鍵按一下物件時，Windows 檔案總管會要求 [**ICoNtextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) 介面。 若要提供物件的快捷方式功能表，請建立功能表處理常式物件，並傳回其 **ICoNtextMenu** 介面。

建立功能表處理常式物件的程式與用來建立功能表處理常式 Shell 延伸模組的程式非常類似。 如需詳細資訊，請參閱 [建立內容功能表處理常式](context-menu-handlers.md) 或 [**ICoNtextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)、 [**ICoNtextMenu2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2)或 [**ICoNtextMenu3**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu3) 參考。

### <a name="iqueryinfo"></a>IQueryInfo

Windows 檔案總管會呼叫 [**IQueryInfo**](/windows/win32/api/shlobj_core/nn-shlobj_core-iqueryinfo) 介面，以抓取提示文字字串。

### <a name="idataobject-and-idroptarget"></a>IDataObject 和 IDropTarget

當 Windows 檔案總管顯示物件時，資料夾物件無法直接知道使用者何時嘗試剪下、複製或拖曳物件。 相反地，Windows 檔案總管會要求 [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) 介面。 若要允許傳送物件，請建立資料物件，並傳回其 **IDataObject** 介面的指標。

同樣地，使用者可能會嘗試將資料物件放在其中一個物件的 Windows 檔案總管標記法，例如圖示或網址列路徑。 Windows 檔案總管接著會要求 [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) 介面。 若要允許卸載資料物件，請建立公開 **IDropTarget** 介面的物件，並傳回介面指標。

處理資料傳輸是撰寫命名空間延伸模組的最棘手層面之一。 如需詳細的討論，請參閱 [使用拖放和剪貼簿來傳送 Shell 物件](dragdrop.md)。

## <a name="working-with-the-default-shell-folder-view-implementation"></a>使用預設的 Shell 資料夾檢視執行

使用預設 Shell 資料夾 view 物件 (DefView) 的資料來源必須執行這些介面：

-   [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder)
-   [**IShellFolder2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder2)
-   [**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder)
-   [**IPersistFolder2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder2)

也可以選擇執行 [**IPersistFolder3**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder3)。

 

 
