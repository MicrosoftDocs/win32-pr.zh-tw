---
description: 本檔提供常見的 Shell 資料傳輸案例，並討論如何在應用程式中執行每一個。
ms.assetid: 7fce555c-a93d-4414-9119-7ae9acdd4d89
title: 處理命令介面資料傳輸案例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35855b66e4108580d5bac305855837563ca59785
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972029"
---
# <a name="handling-shell-data-transfer-scenarios"></a>處理命令介面資料傳輸案例

[Shell 資料物件](dataobject.md)檔探討用來透過拖放或剪貼簿傳輸 Shell 資料的一般方法。 不過，若要在您的應用程式中執行 Shell 資料傳輸，您也必須瞭解如何將這些一般原則和技術套用到各種不同的方式來傳送 Shell 資料。 本檔提供常見的 Shell 資料傳輸案例，並討論如何在應用程式中執行每一個。

-   [一般指導方針](#general-guidelines)
-   [將檔案名稱從剪貼簿複製到應用程式](#copying-file-names-from-the-clipboard-to-an-application)
    -   [從資料物件中解壓縮檔案名稱](#extracting-the-file-names-from-the-data-object)
-   [將已放置檔案的內容複寫到應用程式中](#copying-the-contents-of-a-dropped-file-into-an-application)
    -   [使用 CFSTR \_ FILECONTENTS 格式將檔案中的資料解壓縮](/windows)
-   [處理優化的移動作業](#handling-optimized-move-operations)
-   [處理刪除作業-貼上作業](#handling-delete-on-paste-operations)
-   [從虛擬資料夾傳輸資料](#transfering-data-to-and-from-virtual-folders)
    -   [接受虛擬資料夾中的資料](#accepting-data-from-a-virtual-folder)
    -   [從命名空間延伸模組來回傳送資料](#transferring-data-to-and-from-a-namespace-extension)
-   [將檔案放在資源回收筒](#dropping-files-on-the-recycle-bin)
-   [建立和匯入片段檔案](#creating-and-importing-scrap-files)
    -   [來回支援](#round-trip-support)
    -   [快取的資料格式](#cached-data-formats)
    -   [延遲轉譯](#delayed-rendering)
-   [非同步地拖放 Shell 物件](#dragging-and-dropping-shell-objects-asynchronously)
    -   [使用 Iasyncoperation<tresult>HTTP/IDataObjectAsyncCapability](#using-iasyncoperationidataobjectasynccapability)

> [!Note]  
> 雖然每個案例都討論特定的資料傳輸作業，但其中有許多都適用于各種相關的案例。 例如，大部分剪貼簿與拖放傳輸之間的主要差異在於資料物件抵達目標的方式。 一旦目標有指向資料物件 [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) 介面的指標，則這兩種資料傳輸類型的解壓縮資訊程式大致相同。 不過，某些案例僅限於特定類型的作業。 如需詳細資料，請參閱個別案例。

 

## <a name="general-guidelines"></a>一般準則

下列各節將討論單一、相當特定的資料傳輸案例。 不過，資料傳輸通常更複雜，而且可能牽涉到幾個案例的層面。 您通常不知道實際需要處理的案例。 以下是一些要牢記在心的一般方針。

針對資料來源：

-   Shell 剪貼簿格式（除了 [CF \_ HDROP](clipboard.md)）不會預先定義。 您要使用的每一種格式都必須透過呼叫 [RegisterClipboardFormat](/windows/win32/api/winuser/nf-winuser-registerclipboardformata)來註冊。
-   資料物件中的格式是以來源的喜好設定順序提供。 列舉資料物件，並挑選您可以取用的第一個物件。
-   包含您可以支援的任意數量格式。 您通常不知道資料物件將會放在哪裡。 這種作法可改善資料物件包含放置目標可接受之格式的機率。
-   您應以 [CF \_ HDROP](clipboard.md) 格式提供現有的檔案。
-   使用[CFSTR \_ FILECONTENTS](clipboard.md) / [CFSTR \_ FILEDESCRIPTOR](clipboard.md)格式提供類似檔案的資料。 這種方法可讓目標從資料物件建立檔案，而不需要知道有關基礎資料儲存的任何資訊。 您通常應該將資料顯示為 [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) 介面。 這種資料傳輸機制比全域記憶體物件更有彈性，而且使用的記憶體更少。
-   拖曳 Shell 專案時，拖曳來源應該提供 [CFSTR \_ SHELLIDLIST](clipboard.md) 格式。 您可以透過 [**IShellFolder：： GetUIObjectOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof) 或 [**IShellItem：： BindToHandler**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler) 方法取得專案的資料物件。 資料來源可以使用 [**SHCreateDataObject**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedataobject)來建立支援 [CFSTR \_ SHELLIDLIST](clipboard.md)格式的標準資料物件執行。
-   使用 shell 專案程式設計模型來放置要拖曳之專案的目標，可以使用 [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject)將 IDataObject 轉換成 [**IShellItemArray**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray) 。
-   使用標準的意見反應資料指標。
-   支援向左和向右拖曳。
-   從内嵌物件使用資料物件本身。 這種方法可讓您的應用程式取出資料物件提供的任何額外格式，並避免建立額外的內含專案層。 例如，來自伺服器 A 的内嵌物件會從伺服器/容器 B 拖曳出來，並放在容器 C 上。 C 應建立伺服器 A 的内嵌物件，而不是伺服器 B 的内嵌物件（包含伺服器 A 的内嵌物件）。
-   請記住，Shell 可能會在移動檔案時使用 [優化移動](#handling-optimized-move-operations) 或 [刪除貼上](#handling-delete-on-paste-operations) 作業。 您的應用程式應該能夠辨識這些作業並適當地回應。

針對資料目標：

-   Shell 剪貼簿格式（除了 [CF \_ HDROP](clipboard.md)）不會預先定義。 您要使用的每一種格式都必須透過呼叫 [RegisterClipboardFormat](/windows/win32/api/winuser/nf-winuser-registerclipboardformata)來註冊。
-   執行並註冊 OLE 放置目標。 如果可能的話，請避免使用 Windows 3.1 目標或 [**WM \_ DROPFILES**](wm-dropfiles.md) 訊息。
-   資料物件所包含的格式會根據物件的來源而有所不同。 因為您通常不事先知道資料物件的來源，所以不會假設會有特定的格式。 資料物件應該以品質的順序來列舉格式，從最佳的開始。 因此，若要取得最佳的可用格式，應用程式通常會列舉可用的格式，並使用列舉中可支援的第一種格式。
-   支援由右拖曳。 您可以藉由建立 [拖放處理常式](context-menu-handlers.md)來自訂拖曳快捷方式功能表。
-   如果您的應用程式將接受現有的檔案，它必須能夠處理 [CF \_ HDROP](clipboard.md) 格式。
-   一般情況下，接受檔案的應用程式也應該處理[CFSTR \_ FILECONTENTS](clipboard.md) / [CFSTR \_ FILEDESCRIPTOR](clipboard.md)格式。 雖然檔案系統的檔案具有[CF \_ HDROP](clipboard.md)格式，但命名空間延伸模組等提供者的檔案通常會使用[CFSTR \_ FILECONTENTS](clipboard.md) / [CFSTR \_ FILEDESCRIPTOR](clipboard.md)。 範例包括 Windows CE 資料夾、檔案傳輸通訊協定 (FTP) 資料夾、web 資料夾和 CAB 資料夾。 來源通常會實執行 [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) 介面，以檔案形式呈現其儲存區中的資料。
-   請記住，Shell 可能會在移動檔案時使用 [優化移動](#handling-optimized-move-operations) 或 [刪除貼上](#handling-delete-on-paste-operations) 作業。 您的應用程式應該能夠辨識這些作業並適當地回應。

## <a name="copying-file-names-from-the-clipboard-to-an-application"></a>將檔案名稱從剪貼簿複製到應用程式

**案例：** 使用者選取 Windows 檔案總管中的一或多個檔案，並將其複製到剪貼簿。 您的應用程式會解壓縮檔案名，並將其貼到檔中。

例如，您可以將檔案剪下並貼到您的應用程式中，以允許使用者建立 HTML 連結。 然後，您的應用程式可以從資料物件中解壓縮檔案名稱，並加以處理以建立錨點標記。

當使用者選取 Windows 檔案總管中的檔案，並將它複製到剪貼簿時，Shell 會建立資料物件。 然後，它會呼叫 [**OleSetClipboard**](/windows/win32/api/ole2/nf-ole2-olesetclipboard) ，將資料物件的 [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) 介面指標放到剪貼簿上。

當使用者從您的應用程式功能表或工具列中選取 [ **貼** 上] 命令時：

1.  呼叫 [**OleGetClipboard**](/windows/win32/api/ole2/nf-ole2-olegetclipboard) 以取得資料物件的 [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) 介面。
2.  呼叫 [**IDataObject：： EnumFormatEtc**](/windows/win32/api/objidl/nf-objidl-idataobject-enumformatetc) 來要求列舉值物件。
3.  使用列舉值物件的 [**IEnumFORMATETC**](/windows/win32/api/objidl/nn-objidl-ienumformatetc) 介面來列舉資料物件所包含的格式。

> [!Note]  
> 這項程式中的最後兩個步驟是為了完整性而納入。 簡單的檔案傳輸通常不需要它們。 這種資料傳輸類型所使用的所有資料物件，都應該包含 [CF \_ HDROP](clipboard.md) 格式，可用來判斷物件所包含的檔案名稱。 不過，若要進行更一般的資料傳輸，您應該列舉格式，然後選取您的應用程式可以處理的最佳格式。

 

### <a name="extracting-the-file-names-from-the-data-object"></a>從資料物件中解壓縮檔案名稱

下一步是從資料物件中解壓縮一或多個檔案名，並將其貼到您的應用程式中。 請注意，在本節中討論從資料物件解壓縮檔案名稱的程式同樣適用于拖放傳輸。

從資料物件取出檔案名的最簡單方式是 [CF \_ HDROP](clipboard.md) 格式：

1.  呼叫 [**IDataObject：：**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata)。 將 [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc)結構的 **cfFormat** 成員設定為 [CF \_ HDROP](clipboard.md) ，並將 **tymed** 成員設定為 [tymed \_ HGLOBAL](dataobject.md)。 **DwAspect** 成員通常會設定為 >dvaspect \_ 內容。 但是，如果您需要以簡短的 (8.3) 格式來取得檔案的路徑，請將 **dwAspect** 設定為 >dvaspect \_ short。

    當 [**IDataObject：：**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) hGlobal 成員傳回時， [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1)結構的成員會指向包含資料的全域記憶體物件。

2.  建立 HDROP 變數，並將它設定為 [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1)結構的 **hGlobal** 成員。 HDROP 變數現在是 [**DROPFILES**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropfiles) 結構的控制碼，後面接著雙以 null 終止的字串，其中包含已複製檔案的完整檔案路徑。
3.  藉由呼叫 [**DragQueryFile**](/windows/desktop/api/Shellapi/nf-shellapi-dragqueryfilea) ，並將 *iFile* 參數設定為0xffffffff，判斷清單中有多少個檔案路徑。 函數會傳回清單中的檔案路徑數目。 在下一個步驟中，會使用此清單中以零為基底的檔案路徑來識別特定路徑。
4.  針對每個檔案呼叫 [**DragQueryFile**](/windows/desktop/api/Shellapi/nf-shellapi-dragqueryfilea) 一次，將檔案路徑從全域記憶體物件中解壓縮，並將 *iFile* 設定為檔案的索引。
5.  視需要處理檔案路徑，並將其貼入您的應用程式。
6.  呼叫 [**ReleaseStgMedium**](/windows/win32/api/ole2/nf-ole2-releasestgmedium) ，然後將指標傳遞至您在步驟1中傳遞給 [**IDataObject：：**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata)的 [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1)結構。 一旦您發行結構之後，您在步驟2中建立的 HDROP 值將不再有效，且不應該使用。

## <a name="copying-the-contents-of-a-dropped-file-into-an-application"></a>將已放置檔案的內容複寫到應用程式中

**案例：** 使用者從 Windows 檔案總管拖曳一或多個檔案，並將它們放在應用程式的視窗上。 您的應用程式會將檔案的內容解壓縮 (的) ，並將其貼入應用程式。

此案例使用拖放將檔案從 Windows 檔案總管傳送至應用程式。 在操作之前，您的應用程式必須：

1.  呼叫 [RegisterClipboardFormat](/windows/win32/api/winuser/nf-winuser-registerclipboardformata) 以註冊任何需要的 Shell 剪貼簿格式。
2.  呼叫 [**RegisterDragDrop**](/windows/win32/api/ole2/nf-ole2-registerdragdrop) 以註冊目標視窗和您應用程式的 [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) 介面。

使用者啟動作業之後，請選取一或多個檔案，然後開始拖曳：

1.  Windows 檔案總管會建立資料物件，並將支援的格式載入其中。
2.  Windows 檔案總管會呼叫 [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) 來起始拖曳迴圈。
3.  當拖曳影像到達您的目標視窗時，系統會呼叫 [**IDropTarget：:D ragenter**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter)來通知您。
4.  若要判斷資料物件包含的內容，請呼叫資料物件的 [**IDataObject：： EnumFormatEtc**](/windows/win32/api/objidl/nf-objidl-idataobject-enumformatetc) 方法。 使用方法所傳回的列舉值物件來列舉資料物件所包含的格式。 如果您的應用程式不想接受其中任何一種格式，則傳回 DROPEFFECT \_ NONE。 基於此案例的目的，您的應用程式應該忽略任何不包含用來傳輸檔案之格式的資料物件，例如 [CF \_ HDROP](clipboard.md)。
5.  當使用者拖放資料時，系統會呼叫 [**IDropTarget：:D rop**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop)。
6.  使用 [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) 介面解壓縮檔案的內容。

有幾種不同的方式可從資料物件解壓縮 Shell 物件的內容。 一般情況下，請使用下列順序：

-   如果檔案包含 [CF \_ 文字](clipboard.md) 格式，則資料是 ANSI 文字。 您可以使用 CF \_ 文字格式來解壓縮資料，而不是開啟檔案本身。
-   如果檔案包含連結或內嵌的 OLE 物件，資料物件會包含 CF \_ EMBEDDEDOBJECT 格式。 使用標準的 OLE 技術來將資料解壓縮。 [廢料](#creating-and-importing-scrap-files) 檔案一律包含 CF \_ EMBEDDEDOBJECT 格式。
-   如果 Shell 物件來自檔案系統，資料物件會包含 [CF \_ HDROP](clipboard.md) 格式以及檔案的名稱。 從 [CF \_ HDROP](clipboard.md) 中解壓縮檔案名稱，並呼叫 [**OleCreateFromFile**](/windows/win32/api/ole2/nf-ole2-olecreatefromfile) 以建立新的連結或內嵌的物件。 如需如何從 [CF \_ HDROP](clipboard.md) 格式取得檔案名的討論，請參閱 [將檔案名從剪貼簿複製到應用程式](#copying-file-names-from-the-clipboard-to-an-application)。
-   如果資料物件包含 [CFSTR \_ FILEDESCRIPTOR](clipboard.md) 格式，您可以從檔案的 [CFSTR \_ FILECONTENTS](clipboard.md) 格式解壓縮檔案的內容。 如需此程式的討論，請參閱 [使用 CFSTR \_ FILECONTENTS 格式將資料從檔案解壓縮](/windows)。
-   在 Shell [版本 4.71](versions.md)之前，應用程式會藉由在 [**FILEDESCRIPTOR**](/windows/win32/api/shlobj_core/ns-shlobj_core-filedescriptora)結構的 **dwFlags** 成員中設定 **FD \_ LINKUI** ，來指出它正在傳送快捷方式檔案類型。 針對較新版本的 Shell，表示要傳送快捷方式的慣用方式是使用 [ [CFSTR \_ PREFERREDDROPEFFECT](clipboard.md) 格式] 設定為 [DROPEFFECT] \_ 連結。 這種方法比只為了檢查旗標而解壓縮 **FILEDESCRIPTOR** 結構更有效率。

如果資料解壓縮程式很長，您可能會想要以非同步方式在背景執行緒上進行作業。 然後，您的主要執行緒就可以繼續進行，不需要延遲。 如需如何處理非同步資料解壓縮的討論，請參閱 [非同步地拖放 Shell 物件](#dragging-and-dropping-shell-objects-asynchronously)。

### <a name="using-the-cfstr_filecontents-format-to-extract-data-from-a-file"></a>使用 CFSTR \_ FILECONTENTS 格式將檔案中的資料解壓縮

[CFSTR \_ FILECONTENTS](clipboard.md)格式提供極具彈性且功能強大的方式來傳送檔案的內容。 您甚至不需要將資料儲存為單一檔案。 這種格式所需的全部都是資料物件將資料呈現至目標，就像是檔案一樣。 例如，實際的資料可能是文字檔的區段，或是從資料庫解壓縮的資料區塊。 目標可以將資料視為檔案，而且不需要知道基礎儲存機制的任何資訊。

命名空間延伸模組通常會使用 [CFSTR \_ FILECONTENTS](clipboard.md) 來傳送資料，因為此格式不會採用任何特定的儲存機制。 命名空間延伸可以使用任何便利的儲存機制，並使用此格式將其物件呈現給應用程式，就好像它們是檔案一樣。

[CFSTR \_ FILECONTENTS](clipboard.md)的資料傳輸機制通常是[TYMED \_ ISTREAM](dataobject.md)。 傳輸 [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) 介面指標所需的記憶體比將資料載入至全域記憶體物件的記憶體少得多，而且 **IStream** 是表示資料比 [**IStorage**](/windows/win32/api/objidl/nn-objidl-istorage)更簡單的方法。

[CFSTR \_ FILECONTENTS](clipboard.md)格式一律會伴隨[CFSTR \_ FILEDESCRIPTOR](clipboard.md)格式。 您必須先檢查此格式的內容。 如果正在傳送多個檔案，資料物件實際上會包含多個 [CFSTR \_ FILECONTENTS](clipboard.md) 格式，每個檔案各有一個格式。 [CFSTR \_ FILEDESCRIPTOR](clipboard.md)格式包含每個檔案的名稱和屬性，並提供解壓縮特定檔案的[CFSTR \_ FILECONTENTS](clipboard.md)格式所需的每個檔案的索引值。

若要將 [CFSTR \_ FILECONTENTS](clipboard.md) 格式解壓縮：

1.  將 [CFSTR \_ FILEDESCRIPTOR](clipboard.md) 格式解壓縮為 [TYMED \_ HGLOBAL](dataobject.md) 值。
2.  傳回之 [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1)結構的 **hGlobal** 成員會指向全域記憶體物件。 藉由將 **hGlobal** 值傳遞給 [**GlobalLock**](/windows/win32/api/winbase/nf-winbase-globallock)來鎖定該物件。
3.  將 [**GlobalLock**](/windows/win32/api/winbase/nf-winbase-globallock) 傳回的指標轉換為 [**FILEGROUPDESCRIPTOR**](/windows/win32/api/shlobj_core/ns-shlobj_core-filegroupdescriptora) 指標。 它會指向 **FILEGROUPDESCRIPTOR** 結構，後面接著一或多個 [**FILEDESCRIPTOR**](/windows/win32/api/shlobj_core/ns-shlobj_core-filedescriptora) 結構。 每個 **FILEDESCRIPTOR** 結構都包含一個隨附的 [CFSTR \_ FILECONTENTS](clipboard.md) 格式所包含的檔案描述。
4.  檢查 [**FILEDESCRIPTOR**](/windows/win32/api/shlobj_core/ns-shlobj_core-filedescriptora) 結構，以判斷哪一個對應至您要解壓縮的檔案。 該 **FILEDESCRIPTOR** 結構以零為起始的索引，用來識別檔案的 [CFSTR \_ FILECONTENTS](clipboard.md) 格式。 因為全域記憶體區塊的大小不是位元組精確的，所以請使用結構的 **nFileSizeLow** 和 **nFileSizeHigh** 成員來判斷全域記憶體物件中代表檔案的位元組數目。
5.  呼叫 [**IDataObject：：**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) ，並將 [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc)結構的 **cfFormat** 成員設為 [CFSTR \_ FILECONTENTS](clipboard.md)值，並將 **lIndex** 成員設定為您在上一個步驟中決定的索引。 **Tymed** 成員通常會設定為 [tymed \_ HGLOBAL](dataobject.md) \| tymed \_ ISTREAM \| tymed \_ ISTORAGE。 然後，資料物件可以選擇其慣用的資料傳輸機制。
6.  [**IDataObject：：**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata)硬碟傳回的 [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1)結構將包含檔案資料的指標。 檢查結構的 **tymed** 成員，以決定資料傳輸機制。
7.  如果 **tymed** 設定為 [TYMED \_ ISTREAM](dataobject.md) 或 tymed \_ ISTORAGE，請使用介面來將資料解壓縮。 如果 **tymed** 設定為 tymed \_ HGLOBAL，資料就會包含在全域記憶體物件中。 如需如何從全域記憶體物件中解壓縮資料的討論，請參閱從 [Shell 資料物件](dataobject.md)的 *資料物件區段解壓縮全域記憶體物件*。
8.  呼叫 [**GlobalLock**](/windows/win32/api/winbase/nf-winbase-globallock) 來解除鎖定您在步驟2中鎖定的全域記憶體物件。

## <a name="handling-optimized-move-operations"></a>處理優化的移動作業

**案例：** 使用優化的移動，將檔案從檔案系統移至命名空間延伸模組。

在傳統移動作業中，目標會建立資料的複本，而來源會刪除原始的。 此程式可能沒有效率，因為它需要兩個數據複本。 使用大型物件（例如資料庫）時，傳統的移動作業可能無法實際運作。

藉由優化的移動，目標會使用其對資料儲存方式的瞭解，以處理整個移動作業。 資料永遠不會有第二個複本，也不需要來源刪除原始資料。 Shell 資料很適合用於優化移動，因為目標可以使用 Shell API 來處理整個作業。 移動檔案的一般範例。 一旦目標具有要移動之檔案的路徑，它就可以使用 [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) 來移動它。 來源不需要刪除原始檔案。

> [!Note]  
> Shell 通常會使用優化的移動來移動檔案。 若要適當地處理 Shell 資料傳輸，您的應用程式必須能夠偵測和處理優化的移動。

 

優化的移動會以下列方式處理：

1.  來源會呼叫 [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) ，並將 *dwEffect* 參數設定為 DROPEFFECT \_ MOVE，以表示可以移動來源物件。
2.  目標 \_ 會透過其 [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) 方法的其中一個來接收 DROPEFFECT 移動值，表示允許移動。
3.  目標是複製物件 (未優化的移動) 或移動物件 (優化的移動) 。
4.  然後，目標會告知來源是否需要刪除原始資料。

    優化的移動是預設作業，並由目標刪除資料。 若要通知來源已執行優化的移動：

    -   -   目標會將它透過其 [**:D IDropTarget**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop)所收到的 *pdwEffect* 值設定為 DROPEFFECT MOVE 以外的某個值 \_ 。 它通常會設定為 DROPEFFECT \_ NONE 或 DROPEFFECT \_ COPY。 [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop)會將值傳回到來源。
        -   目標也會呼叫資料物件的 [**IDataObject：： SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) 方法，並將 [CFSTR \_ PERFORMEDDROPEFFECT](clipboard.md) 格式識別碼設定為 DROPEFFECT \_ NONE。 這個方法呼叫是必要的，因為某些卸載目標可能不會正確地設定 [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop)的 *pdwEffect* 參數。 [CFSTR \_ PERFORMEDDROPEFFECT](clipboard.md)格式是用來表示已進行優化移動的可靠方式。

    如果目標執行未優化的移動，則必須由來源刪除資料。 若要通知來源已執行未優化的移動：

    -   -   目標會將它透過其 [**:D IDropTarget**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop)所收到的 *pdwEffect* 值設定為 DROPEFFECT \_ 移動。 [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop)會將值傳回到來源。
        -   目標也會呼叫資料物件的 [**IDataObject：： SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) 方法，並將 [CFSTR \_ PERFORMEDDROPEFFECT](clipboard.md) 格式識別碼設定為 DROPEFFECT \_ MOVE。 這個方法呼叫是必要的，因為某些卸載目標可能不會正確地設定 [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop)的 *pdwEffect* 參數。 [CFSTR \_ PERFORMEDDROPEFFECT](clipboard.md)格式是表示已進行未優化移動的可靠方式。

5.  來源會檢查目標所能傳回的兩個值。 如果兩者都設定為 DROPEFFECT \_ move，則會藉由刪除原始資料來完成未優化的移動。 否則，目標會進行優化的移動，並刪除原始資料。

## <a name="handling-delete-on-paste-operations"></a>處理刪除作業-貼上作業

**案例：** 從 Windows 檔案總管中的資料夾剪下一或多個檔案，並貼到命名空間延伸模組中。 Windows 檔案總管會將檔案保留在反白顯示，直到其收到貼上作業結果的意見反應為止。

傳統上，當使用者剪下資料時，它會立即從 view 中消失。 這可能不會很有效率，而且如果使用者對資料所做的事很在意，可能會導致可用性問題。 替代方法是使用「刪除時貼上」作業。

使用「刪除時複製」作業時，不會立即從 view 中移除選取的資料。 相反地，來源應用程式會將它標示為已選取，或許是藉由變更字型或背景色彩。 目標應用程式貼上資料之後，會通知來源有關作業的結果。 如果目標執行了 [優化的移動](#handling-optimized-move-operations)，則來源可以直接更新其顯示。 如果目標執行的是一般的移動，則來源也必須刪除其資料複本。 如果貼上失敗，來源應用程式會將選取的資料還原為其原始外觀。

> [!Note]  
> 當使用剪下/貼上作業來移動檔案時，Shell 通常會使用「刪除時貼上」。 使用 Shell 物件的刪除開啟貼上作業通常會使用 [優化的移動](#handling-optimized-move-operations) 來移動檔案。 若要適當地處理 Shell 資料傳輸，您的應用程式必須能夠偵測和處理刪除貼上作業。

 

「刪除時刪除」的基本需求是目標必須向來源報告作業的結果。 不過，標準剪貼簿技術無法用來執行「刪除時貼上」，因為它們無法提供目標與來源進行通訊的方式。 相反地，目標應用程式會使用資料物件的 [**IDataObject：： SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) 方法將結果報告給資料物件。 然後，資料物件可以透過私用介面與來源進行通訊。

刪除貼上操作的基本程式如下：

1.  來源會標示所選取資料的螢幕顯示。
2.  來源會建立資料物件。 它會藉由新增 [CFSTR \_ PREFERREDDROPEFFECT](clipboard.md) 格式和 DROPEFFECT MOVE 的資料值，來指出剪下作業 \_ 。
3.  來源會使用 [**OleSetClipboard**](/windows/win32/api/ole2/nf-ole2-olesetclipboard)將資料物件放在剪貼簿上。
4.  目標會使用 [**OleGetClipboard**](/windows/win32/api/ole2/nf-ole2-olegetclipboard)從剪貼簿抓取資料物件。
5.  目標會將 [CFSTR \_ PREFERREDDROPEFFECT](clipboard.md) 資料解壓縮。 如果設定為 [僅 DROPEFFECT \_ 移動]，目標可以進行優化的移動，或只複製資料。
6.  如果目標沒有優化的移動，它會呼叫 [**IDataObject：： SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) 方法，並將 [CFSTR \_ PERFORMEDDROPEFFECT](clipboard.md) 格式設定為 DROPEFFECT \_ move。
7.  當貼上完成時，目標會呼叫 [**IDataObject：： SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) 方法，並將 [CFSTR \_ PASTESUCCEEDED](clipboard.md) 格式設定為 DROPEFFECT \_ MOVE。
8.  當呼叫 [**IDataObject：： SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) 方法，並將 [CFSTR \_ PASTESUCCEEDED](clipboard.md) 格式設定為 DROPEFFECT \_ MOVE 時，它必須檢查它是否也會收到 [CFSTR \_ PERFORMEDDROPEFFECT](clipboard.md) 格式設定為 DROPEFFECT \_ move。 如果這兩種格式都是由目標傳送，來源就必須刪除資料。 如果只收到 [CFSTR \_ PASTESUCCEEDED](clipboard.md) 格式，則來源可以直接從其顯示中移除資料。 如果傳輸失敗，來源會將顯示更新為其原始外觀。

## <a name="transfering-data-to-and-from-virtual-folders"></a>從虛擬資料夾傳輸資料

**案例：** 使用者將物件拖曳到虛擬資料夾，或將它放在虛擬資料夾中。

虛擬資料夾包含通常不屬於檔案系統的物件。 某些虛擬資料夾（例如資源回收筒）可以代表儲存在硬碟上，但不是一般檔案系統物件的資料。 有些可以代表位於遠端系統上的儲存資料，例如掌上型電腦或 FTP 網站。 其他（例如 [印表機] 資料夾）包含不代表儲存資料的物件。 雖然某些虛擬資料夾是系統的一部分，但開發人員也可以藉由執行命名空間延伸來建立和安裝自訂虛擬資料夾。

無論資料類型或其儲存方式為何，命令介面都會將虛擬資料夾所包含的資料夾和檔案物件顯示為一般檔案和資料夾。 虛擬資料夾會負責取得其所包含的任何資料，並適當地呈現給 Shell。 這項需求表示虛擬資料夾通常支援拖放和剪貼簿資料傳輸。

因此，有兩個開發人員需要關注虛擬資料夾的資料傳輸：

-   應用程式需要接受從虛擬資料夾傳輸之資料的開發人員。
-   其命名空間延伸模組需要適當支援資料傳輸的開發人員。

### <a name="accepting-data-from-a-virtual-folder"></a>接受虛擬資料夾中的資料

虛擬資料夾幾乎可代表任何類型的資料，而且可以用任何選擇的方式儲存該資料。 某些虛擬資料夾實際上可能包含一般的檔案系統檔案和資料夾。 比方說，有些人可能會將所有的物件封裝成單一檔或資料庫。

當檔案系統物件傳輸至應用程式時，資料物件通常會包含具有物件完整路徑的 [CF \_ HDROP](clipboard.md) 格式。 您的應用程式可以將此字串解壓縮，並使用一般檔案系統函式來開啟檔案並將其資料解壓縮。 不過，由於虛擬資料夾通常不包含一般的檔案系統物件，因此通常不會使用 [CF \_ HDROP](clipboard.md)。

資料通常會從具有[CFSTR \_ FILEDESCRIPTOR](clipboard.md)CFSTR FILECONTENTS 格式的虛擬資料夾傳輸，而不是[CF \_ HDROP](clipboard.md) / [ \_ ](clipboard.md) 。 [CFSTR \_ FILECONTENTS](clipboard.md)格式有兩個優於[CF \_ HDROP](clipboard.md)的優點：

-   未採用任何特定的資料儲存方法。
-   格式較有彈性。 它支援三種資料傳輸機制：全域記憶體物件、 [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) 介面或 [**IStorage**](/windows/win32/api/objidl/nn-objidl-istorage) 介面。

全域記憶體物件很少用來將資料傳送至虛擬物件或從中傳送資料，因為資料必須完整複製到記憶體中。 傳送介面指標幾乎不需要記憶體，而且效率更高。 使用非常大型的檔案時，介面指標可能是唯一實用的資料傳輸機制。 通常，資料是以 [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) 指標表示，因為該介面比 [**IStorage**](/windows/win32/api/objidl/nn-objidl-istorage)更有彈性。 目標會從資料物件中解壓縮指標，並使用介面方法來將資料解壓縮。

如需如何處理[CFSTR \_ FILEDESCRIPTOR](clipboard.md) / [CFSTR \_ FILECONTENTS](clipboard.md)格式的進一步討論，請參閱[使用 CFSTR \_ FILECONTENTS 格式將資料從檔案解壓縮](/windows)。

### <a name="transferring-data-to-and-from-a-namespace-extension"></a>從命名空間延伸模組來回傳送資料

當您執行命名空間延伸模組時，您通常會想要支援拖放功能。 遵循 [一般指導方針](#general-guidelines)中所討論之卸載來源和目標的建議。 尤其是命名空間延伸模組必須：

-   可以處理[CFSTR \_ FILEDESCRIPTOR](clipboard.md) / [CFSTR \_ FILECONTENTS](clipboard.md)格式。 這兩種格式通常用來在命名空間延伸中傳送物件。
-   可以處理優化的 [移動](#handling-optimized-move-operations)。 Shell 預期會使用優化的移動來移動 Shell 物件。
-   可以處理 [刪除貼上](#handling-delete-on-paste-operations) 作業。 當使用剪下/貼上作業從 Shell 移動物件時，Shell 會使用「刪除時貼上」。
-   能夠處理透過 [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) 或 [**IStorage**](/windows/win32/api/objidl/nn-objidl-istorage) 介面的資料傳輸。 通常會透過傳送這兩個介面指標的其中一個（通常是 **IStream** 指標）來處理從虛擬資料夾傳輸到或傳出的資料。 然後，目標會呼叫介面方法來將資料解壓縮：
    -   -   作為卸載來源，命名空間延伸模組必須從儲存體解壓縮資料，並透過此介面將資料傳遞至目標。
        -   做為放置目標，命名空間延伸必須透過此介面接受來自來源的資料，並正確地儲存。

## <a name="dropping-files-on-the-recycle-bin"></a>將檔案放在資源回收筒

**案例：** 使用者會將檔案放在 **資源回收筒** 上。 您的應用程式或命名空間延伸模組會刪除原始檔案。

資源回收筒是虛擬資料夾，用來做為不再需要之檔案的儲存機制。 只要資源回收筒尚未清空，使用者就可以在稍後復原檔案，並將它傳回檔案系統。

在大部分的情況下，將 Shell 物件傳送至資源回收筒的運作方式與任何其他資料夾相同。 不過，當使用者卸載 **資源回收筒** 上的檔案時，來源必須刪除原始的，即使來自資料夾的意見反應表示複製作業。 通常，卸載來源無法得知其資料物件已卸載的資料夾。 不過，對於 Windows 2000 和更新版本的系統，當資料物件放在 **資源回收筒** 上時，Shell 會呼叫資料物件的 [**IDataObject：： SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) 方法，並將 [CFSTR \_ TARGETCLSID](clipboard.md) 格式設定為資源回收筒的類別識別碼 (clsid)  (clsid \_ clear-recyclebin) 。 若要適當地處理資源回收筒案例，您的資料物件應該能夠辨識此格式，並透過私用介面將資訊傳達給來源。

> [!Note]  
> 當呼叫 [**IDataObject：： SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) 時，如果將 [CFSTR \_ TARGETCLSID](clipboard.md) 格式設定為 CLSID \_ clear-recyclebin，資料來源應該會關閉從方法傳回之前所傳送之物件的任何開啟控制碼。 否則，您可能會建立共用違規。

 

## <a name="creating-and-importing-scrap-files"></a>建立和匯入片段檔案

**案例：** 使用者從 OLE 應用程式的資料檔案拖曳一些資料，然後將它放在桌面上或 Windows 檔案總管。

Windows 可讓使用者從 OLE 應用程式的資料檔案拖曳物件，並將它放在桌面或檔系統資料夾中。 此作業會建立一個包含資料的 *廢料* 檔或資料的連結。 檔案名取自針對物件 CLSID 和 [CF \_ 文字](clipboard.md) 資料註冊的簡短名稱。 若要讓 Shell 建立包含資料的碎片檔案，應用程式的 [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) 介面必須支援 CF \_ EMBEDSOURCE 剪貼簿格式。 若要建立包含連結的檔案， **IDataObject** 必須支援 CF \_ LINKSOURCE 格式。

另外還有三個選擇性功能，可讓應用程式執行以支援片段檔案：

-   來回支援
-   快取的資料格式
-   延遲轉譯

### <a name="round-trip-support"></a>來回支援

*來回行程* 牽涉到將資料物件傳送到另一個容器，然後再送回原始檔案。 例如，使用者可以從試算表將資料格群組傳送至桌面，並以資料建立片段檔案。 如果使用者接著將碎片轉移回電子表格，則必須將資料整合到原始傳輸之前的檔。

當 Shell 建立片段檔案時，它會將資料表示為內嵌物件。 當您將片段傳送至另一個容器時，它會以内嵌物件的形式傳送，即使是傳回原始檔案亦同。 您的應用程式會負責判斷片段中包含的資料格式，並視需要將資料放回其原生格式。

若要建立内嵌物件的格式，請藉由取出物件的 CF OBJECTDESCRIPTOR 格式來判斷其 CLSID \_ 。 如果 CLSID 指出屬於應用程式的資料格式，則應該傳送原生資料，而不是呼叫 [**OleCreateFromData**](/windows/win32/api/ole2/nf-ole2-olecreatefromdata)。

### <a name="cached-data-formats"></a>快取的資料格式

當 Shell 建立碎片檔案時，它會檢查登錄中是否有可用的格式清單。 根據預設，有兩種可用的格式： CF \_ EMBEDSOURCE 和 cf \_ LINKSOURCE。 不過，在許多情況下，應用程式可能需要使用不同格式的片段檔案：

-   允許將片段傳送至非 OLE 容器（無法接受内嵌物件格式）。
-   允許應用程式套件與私用格式進行通訊。
-   讓來回行程更容易處理。

應用程式可以在登錄中快取格式，以將格式新增至片段。 有兩種類型的快取格式：

-   優先權快取格式。 針對這些格式，資料會從資料物件完整複製到片段。
-   延遲呈現格式。 針對這些格式，資料物件不會複製到片段。 相反地，轉譯會延遲，直到目標要求資料為止。 下一節會更詳細地討論延遲轉譯。

若要新增優先順序快取或延遲轉譯格式，請在資料來源的應用程式的 **CLSID** 機碼底下建立 **DataFormat** 子機碼。 在該子機碼下，建立 **PriorityCacheFormats** 或 **DelayRenderFormats** 子機碼。 針對每個優先順序快取或延遲轉譯格式，建立編號子機碼，從零開始。 將此機碼的值設定為具有已註冊之格式名稱或 x 值的字串 \# ，其中 X 表示標準剪貼簿格式的格式號碼。

下列範例顯示兩個應用程式的快取格式。 MyProg1 應用程式將 rtf 格式設定為優先權快取格式，以及使用私用格式 "My Format" 作為延遲轉譯格式。 MyProg2 應用程式的 CF \_ 點陣圖格式 (\# 8」 ) 為優先權快取格式。

```
HKEY_CLASSES_ROOT
   CLSID
      {GUID}
         (Default) = MyProg1
         DataFormats
            PriorityCacheFormats
               0
                  (Default) = Rich Text Format
            DelayRenderFormats
               0
                  (Default) = My Format
      {GUID}
         (Default) = MyProg2
         DataFormats
            PriorityCacheFormats
               0
                  (Default) = #8
```

您可以藉由建立額外的編號子機碼來新增其他格式。

### <a name="delayed-rendering"></a>延遲轉譯

延遲轉譯格式可讓應用程式建立碎片檔案，但會延遲資料轉譯的費用，直到目標要求為止。 片段的 [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) 介面將會提供延遲的轉譯格式給目標，以及原生和快取的資料。 如果目標要求延遲轉譯格式，則 Shell 會執行應用程式，並從使用中物件將資料提供給目標。

> [!Note]  
> 因為延遲轉譯的風險很高，所以應謹慎使用。 如果伺服器無法使用，或未啟用 OLE 的應用程式，它將無法運作。

 

## <a name="dragging-and-dropping-shell-objects-asynchronously"></a>非同步地拖放 Shell 物件

**案例：** 使用者將大型資料區塊從來源傳輸至目標。 為了避免在很長的時間內封鎖這兩個應用程式，目標會以非同步方式將資料解壓縮。

通常，拖放作業是一項同步作業。 簡單地說︰

1.  卸載來源會呼叫 [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) 並封鎖其主要執行緒，直到函數傳回為止。 封鎖主要執行緒通常會封鎖 UI 處理。
2.  在呼叫目標的 [**IDropTarget：:D rop**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) 方法之後，目標會將資料從其主要執行緒上的資料物件中解壓縮。 此程式通常會在解壓縮進程期間封鎖目標的 UI 處理。
3.  資料解壓縮之後，目標會傳回 [**IDropTarget：:D rop**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) 呼叫、系統會傳回 [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop)，而且這兩個執行緒都可以繼續。

簡單地說，同步資料傳輸可以封鎖這兩個應用程式的主要執行緒一段很長的時間。 特別是，這兩個執行緒必須等待，而目標則是將資料解壓縮。 針對少量的資料，將資料解壓縮所需的時間很小，且同步資料傳輸的運作方式很好。 不過，同步解壓縮大量資料可能會造成冗長的延遲，並干擾目標和來源的 UI。

[**Iasyncoperation<tresult>HTTP**](/previous-versions//bb776309(v=vs.85)) / [**IDataObjectAsyncCapability**](/windows/desktop/api/Shldisp/nn-shldisp-idataobjectasynccapability)介面是選擇性的介面，可由資料物件來執行。 它讓放置目標能夠以非同步方式在背景執行緒上解壓縮資料物件中的資料。 一旦將資料解壓縮遞交給背景執行緒，這兩個應用程式的主要執行緒都可以自由地進行。

### <a name="using-iasyncoperationidataobjectasynccapability"></a>使用 Iasyncoperation<tresult>HTTP/IDataObjectAsyncCapability

> [!Note]  
> 此介面最初名為 [**iasyncoperation<tresult>HTTP**](/previous-versions//bb776309(v=vs.85))，但稍後變更為 [**IDataObjectAsyncCapability**](/windows/desktop/api/Shldisp/nn-shldisp-idataobjectasynccapability)。 否則，這兩個介面相同。

 

[**Iasyncoperation<tresult>HTTP**](/previous-versions//bb776309(v=vs.85)) / [**IDataObjectAsyncCapability**](/windows/desktop/api/Shldisp/nn-shldisp-idataobjectasynccapability)的目的是要讓卸載來源和卸載目標能進行協商，以進行非同步資料解壓縮。 下列程式概述 drop source 如何使用介面：

1.  建立公開 [**iasyncoperation<tresult>HTTP**](/previous-versions//bb776309(v=vs.85)) / [**IDataObjectAsyncCapability**](/windows/desktop/api/Shldisp/nn-shldisp-idataobjectasynccapability)的資料物件。
2.  將 *fDoOpAsync* 設定為 **VARIANT \_ TRUE** 來呼叫 [**SetAsyncMode**](/windows/desktop/api/Shldisp/nf-shldisp-idataobjectasynccapability-setasyncmode) ，表示支援非同步作業。
3.  [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop)傳回之後，請呼叫 [**InOperation**](/windows/desktop/api/Shldisp/nf-shldisp-idataobjectasynccapability-inoperation)：
    -   如果 [**InOperation**](/windows/desktop/api/Shldisp/nf-shldisp-idataobjectasynccapability-inoperation) 失敗或傳回 **VARIANT \_ FALSE**，則會進行一般同步資料傳輸，並完成資料解壓縮程式。 來源應該執行任何必要的清除作業，然後繼續進行。
    -   如果 [**InOperation**](/windows/desktop/api/Shldisp/nf-shldisp-idataobjectasynccapability-inoperation) 傳回 **VARIANT \_ TRUE**，就會以非同步方式將資料解壓縮。 清除作業應該由 [**EndOperation**](/windows/desktop/api/Shldisp/nf-shldisp-idataobjectasynccapability-endoperation)處理。
4.  釋放資料物件。
5.  非同步資料傳輸完成時，資料物件通常會透過私用介面通知來源。

下列程式概述 drop target 如何使用 [**iasyncoperation<tresult>HTTP**](/previous-versions//bb776309(v=vs.85)) / [**IDataObjectAsyncCapability**](/windows/desktop/api/Shldisp/nn-shldisp-idataobjectasynccapability)介面，以非同步方式將資料解壓縮：

1.  當系統呼叫 [**IDropTarget：:D rop**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop)時，請呼叫 [**IDataObject：： QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) ，並 [](/previous-versions//bb776309(v=vs.85)) / [](/windows/desktop/api/Shldisp/nn-shldisp-idataobjectasynccapability) \_ \_ 從資料物件要求 (IID IDataObjectAsyncCapability/IID iasyncoperation<tresult>HTTP) 的 iasyncoperation<tresult>HTTP IDataObjectAsyncCapability 介面。
2.  呼叫 [**GetAsyncMode**](/windows/desktop/api/Shldisp/nf-shldisp-idataobjectasynccapability-getasyncmode)。 如果方法傳回 **VARIANT \_ TRUE**，則資料物件支援非同步資料解壓縮。
3.  建立個別的執行緒來處理資料解壓縮和呼叫 [**StartOperation**](/windows/desktop/api/Shldisp/nf-shldisp-idataobjectasynccapability-startoperation)。
4.  傳回 [**IDropTarget：:D rop**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) 呼叫，就像一般資料傳輸作業一樣。 [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) 將會傳回並解除封鎖放置來源。 請勿呼叫 [**IDataObject：： SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) 來指出優化移動或刪除貼上作業的結果。 等候作業完成。
5.  將背景執行緒上的資料解壓縮。 目標的主要執行緒已解除封鎖，並可自由繼續。
6.  如果資料傳輸是優化的 [移動](#handling-optimized-move-operations) 或 [刪除貼上](#handling-delete-on-paste-operations) 作業，請呼叫 [**IDataObject：： SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) 來指出結果。
7.  藉由呼叫 [**EndOperation**](/windows/desktop/api/Shldisp/nf-shldisp-idataobjectasynccapability-endoperation)，通知資料物件已完成解壓縮。

 

 
