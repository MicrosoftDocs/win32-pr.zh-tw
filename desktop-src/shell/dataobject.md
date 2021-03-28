---
description: 資料物件是所有 Shell 資料傳輸的核心。
ms.assetid: c63d339e-ac62-4da1-b5ce-22d45a6a3413
title: 命令介面資料物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 812e5c18f5a2120fbf22682c6e768dc005128630
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191176"
---
# <a name="shell-data-object"></a>命令介面資料物件

資料物件是所有 Shell 資料傳輸的核心。 它主要是用來保存已傳送資料的容器。 不過，目標也可以與資料物件進行通訊，以促進某些特製化類型的 Shell 資料傳輸，例如優化的移動。 本主題提供 Shell 資料物件如何運作的一般討論、來源如何建立它們，以及目標如何處理它們。 如需如何使用資料物件來傳送不同類型之 Shell 資料的詳細討論，請參閱 [處理 Shell 資料傳輸案例](datascenarios.md)。

-   [資料物件的運作方式](#how-data-objects-work)
    -   [剪貼簿格式](#clipboard-formats)
    -   [FORMATETC 結構](#formatetc-structure)
    -   [STGMEDIUM 結構](#stgmedium-structure)
-   [來源如何建立資料物件](#how-a-source-creates-a-data-object)
    -   [如何將全域記憶體物件加入至資料物件](#how-to-add-a-global-memory-object-to-a-data-object)
    -   [執行 IDataObject](#implementing-idataobject)
    -   [執行 IDropSource](#implementing-idropsource)
-   [目標如何處理資料物件](#how-a-target-handles-a-data-object)
    -   [從資料物件解壓縮 Shell 資料](#extracting-shell-data-from-a-data-object)
    -   [執行 IDropTarget](#implementing-idroptarget)
-   [使用拖放 Helper 物件](#using-the-drag-and-drop-helper-object)
    -   [使用 IDragSourceHelper 介面](#using-the-idragsourcehelper-interface)
    -   [使用 IDropTargetHelper 介面](#using-the-idroptargethelper-interface)

## <a name="how-data-objects-work"></a>資料物件的運作方式

資料物件是元件物件模型 (COM) 物件，由資料來源建立，以將資料傳送至目標。 它們通常會包含一個以上的資料項目目。 這種作法有兩個原因：

-   雖然幾乎任何類型的資料都可以使用資料物件傳送，但來源通常不知道目標可接受的資料類型。 例如，資料可能是格式化文字檔的一部分。 雖然目標可能能夠處理複雜的格式設定資訊，但它也可能只接受 ANSI 文字。 基於這個理由，資料物件通常會以數種不同的格式包含相同的資料。 然後，目標可以使用它可以處理的格式來將資料解壓縮。
-   資料物件也可以包含不是來源資料版本的輔助資料項目目。 這種類型的資料項目通常會提供資料傳輸作業的其他相關資訊。 例如，Shell 會使用輔助資料項目來指出是否要複製或移動檔案。

### <a name="clipboard-formats"></a>剪貼簿格式

資料物件中的每個資料項目目都有相關聯的格式，通常稱為「剪貼簿」 *格式*。 在 Winuser 中宣告的一些標準剪貼簿格式，會對應到常用的資料類型。 剪貼簿格式是整數，但通常是以其對等名稱（其格式為 CF \_ *XXX*）參考。 例如，ANSI 文字的剪貼簿格式為 CF \_ 文字。

應用程式可以藉由定義私用格式來擴充可用剪貼簿格式的範圍。 若要定義私用格式，應用程式會使用可識別格式的字串來呼叫 [RegisterClipboardFormat](/windows/win32/api/winuser/nf-winuser-registerclipboardformata) 。 函數傳回的不帶正負號整數是有效的格式值，可以像標準剪貼簿格式一樣使用。 不過，來源和目標都必須註冊格式才能使用它。 有一個例外狀況（[CF \_ HDROP](clipboard.md)），用來傳輸 Shell 資料的剪貼簿格式會定義為私用格式。 它們必須先由來源和目標注冊，才能使用。 如需可用 Shell 剪貼簿格式的描述，請參閱 Shell 剪貼簿格式。

雖然有一些例外狀況，但資料物件通常只會針對每個支援的剪貼簿格式包含一個資料項目目。 格式和資料之間的一對一相互關聯可讓格式值當做相關資料項目的識別碼使用。 事實上，在討論資料物件的內容時，特定的資料項目目通常稱為「格式」，而且是由其格式名稱所參考。 例如，「解壓縮 CF \_ 文字格式 ...」這類片語通常用於討論資料物件的 ANSI 文字資料項目。

當放置目標接收到資料物件的指標時，放置目標會列舉可用的格式，以判斷哪些類型的資料可以使用。 然後，它會要求一或多個可用的格式，並解壓縮資料。 目標從資料物件解壓縮 Shell 資料的特定方式會因格式而異;這會在 [目標處理資料物件的方式](#how-a-target-handles-a-data-object)中詳細討論。

使用簡單的剪貼簿資料傳輸時，資料會放在全域記憶體物件中。 該物件的位址會放置在剪貼簿上，連同其格式。 剪貼簿格式會告訴目標它會在相關聯的位址找到哪種資料。 雖然簡單的剪貼簿傳輸很容易執行：

-   資料物件提供更有彈性的方式來傳輸資料。
-   資料物件更適合傳輸大量資料。
-   使用拖放作業時，必須使用資料物件來傳輸資料。

基於這些原因，所有 Shell 資料傳輸都會使用資料物件。 使用資料物件時，不會直接使用剪貼簿格式。 相反地，資料項目目會以剪貼簿格式的一般化（ [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) 結構）來識別。

### <a name="formatetc-structure"></a>FORMATETC 結構

[**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc)結構是剪貼簿格式的擴充版本。 如同用於 Shell 資料傳輸， **FORMATETC** 結構具有下列特性：

-   資料項目在 **cfFormat** 成員中仍是以其剪貼簿格式來識別。
-   資料傳輸不限於全域記憶體物件。 **Tymed** 成員是用來指出相關聯的 [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1)結構中所包含的資料傳輸機制。 它會設定為其中一個 [**TYMED \_ XXX**](/windows/win32/api/objidl/ne-objidl-tymed) 值。
-   Shell 會使用 **lIndex** 成員及其 [CFSTR \_ FILECONTENTS](clipboard.md) 格式，讓資料物件能夠包含每個格式的一個以上資料項目。 如需如何使用此格式的討論，請參閱 [處理 Shell 資料傳輸案例](datascenarios.md)的 *使用 CFSTR \_ FILECONTENTS 格式從檔案解壓縮資料* 一節。
-   **DwAspect** 成員通常會設定為 >dvaspect \_ 內容。 不過，Shlobj.h 中定義了三個可用於 Shell 資料傳輸的值。 

    |                     |                                                                                                   |
    |---------------------|---------------------------------------------------------------------------------------------------|
    | >DVASPECT \_ 複製      | 用來表示格式代表資料的複本。                                   |
    | >DVASPECT \_ 連結      | 用來表示格式代表資料的快捷方式。                               |
    | >DVASPECT \_ SHORTNAME | 搭配 CF \_ HDROP 格式使用，可要求名稱縮短為8.3 格式的檔案路徑。 |

    

     

-   **Ptd** 成員不會用於 Shell 資料傳輸，而且通常會設定為 **Null**。

### <a name="stgmedium-structure"></a>STGMEDIUM 結構

[**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1)結構會提供所傳送資料的存取權。 Shell 資料支援三種資料傳輸機制：

-   全域記憶體物件。
-   [**IStream**](/windows/win32/api/objidl/nn-objidl-istream)介面。
-   [**IStorage**](/windows/win32/api/objidl/nn-objidl-istorage)介面。

[**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1)結構的 **Tymed** 成員是 [**tymed \_ XXX**](/windows/win32/api/objidl/ne-objidl-tymed)值，用來識別資料傳輸機制。 第二個成員是目標用來將資料解壓縮的指標。 根據 **tymed** 值而定，指標可以是各種類型的其中一個。 下表摘要說明用於 Shell 資料傳輸的三個 **tymed** 值，以及其對應的 **STGMEDIUM** 成員名稱。



| tymed 值     | 成員名稱 | 說明                                                                                                                                                                                                                                                                                                       |
|-----------------|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TYMED \_ HGLOBAL  | **hGlobal** | 全域記憶體物件的指標。 此指標類型通常用來傳輸少量的資料。 例如，Shell 會使用全域記憶體物件來傳送簡短的文字字串，例如檔案名或 Url。                                                                                    |
| TYMED \_ ISTREAM  | **pstm**    | [**IStream**](/windows/win32/api/objidl/nn-objidl-istream)介面的指標。 此指標類型對於大部分的 Shell 資料傳輸而言是慣用的，因為相較于 TYMED HGLOBAL，它需要較少的記憶體 \_ 。 此外，TYMED 的 \_ ISTREAM 資料傳輸機制不需要來源以任何特定方式儲存其資料。 |
| TYMED \_ ISTORAGE | **pstg**    | [**IStorage**](/windows/win32/api/objidl/nn-objidl-istorage)介面的指標。 目標會呼叫介面方法來將資料解壓縮。 如同 TYMED \_ ISTREAM，此指標類型需要較少的記憶體。 不過，由於 TYMED \_ ISTORAGE 的彈性比 TYMED ISTREAM 還低 \_ ，因此它並不常使用。                  |



 

## <a name="how-a-source-creates-a-data-object"></a>來源如何建立資料物件

當使用者起始 Shell 資料傳輸時，來源會負責建立資料物件並載入資料。 下列程式摘要說明此程式：

1.  呼叫 [RegisterClipboardFormat](/windows/win32/api/winuser/nf-winuser-registerclipboardformata) ，以針對將包含在資料物件中的每個 Shell 格式取得有效的剪貼簿格式值。 請記住， [CF \_ HDROP](clipboard.md) 已經是有效的剪貼簿格式，而且不需要註冊。
2.  針對要傳送的每個格式，請將相關聯的資料放入全域記憶體物件，或建立可透過 [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) 或 [**IStorage**](/windows/win32/api/objidl/nn-objidl-istorage) 介面存取該資料的物件。 **IStream** 和 **IStorage** 介面是使用標準 COM 技術所建立。 如需如何處理全域記憶體物件的討論，請參閱 [如何將全域記憶體物件加入至資料物件](#how-to-add-a-global-memory-object-to-a-data-object)。
3.  建立每個格式的 [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) 和 [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) 結構。
4.  具現化資料物件。
5.  針對每個支援的格式呼叫 [**IDataObject：： SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) 方法，並傳入格式的 [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) 和 [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) 結構，以將資料載入資料物件。
6.  使用剪貼簿資料傳輸，呼叫 [**OleSetClipboard**](/windows/win32/api/ole2/nf-ole2-olesetclipboard) 將資料物件的 [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) 介面指標放置在剪貼簿上。 若為拖放傳送，請呼叫 [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop)來起始 *拖曳迴圈*。 卸載資料時，會將 **IDataObject** 指標傳遞至放置目標，並結束拖曳迴圈。

現在可以將資料物件傳輸至目標。 針對剪貼簿資料傳輸，只會保留物件，直到目標透過呼叫 [**OleGetClipboard**](/windows/win32/api/ole2/nf-ole2-olegetclipboard)來要求為止。 若為拖放資料傳輸，資料物件會負責建立表示資料的圖示，並在使用者移動資料指標時移動資料。 當物件在拖曳迴圈中時，來源會透過其 [**IDropSource**](/windows/win32/api/oleidl/nn-oleidl-idropsource) 介面接收狀態資訊。 如需進一步討論，請參閱 [執行 IDropSource](#implementing-idropsource)。

如果目標是從剪貼簿取出資料物件，則來源不會收到任何通知。 當拖放作業在目標上卸載物件時，呼叫來起始拖曳迴圈的 [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) 函式將會傳回。

### <a name="how-to-add-a-global-memory-object-to-a-data-object"></a>如何將全域記憶體物件加入至資料物件

許多 Shell 資料格式都是全域記憶體物件的形式。 使用下列程式建立包含全域記憶體物件的格式，並將它載入資料物件中：

1.  建立 [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) 結構。 將 **cfFormat** 成員設定為適當的剪貼簿格式值，並將 **tymed** 成員設定為 tymed \_ HGLOBAL。
2.  建立 [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) 結構。 將 **tymed** 成員設定為 tymed \_ HGLOBAL。
3.  藉由呼叫 [**GlobalAlloc**](/windows/win32/api/winbase/nf-winbase-globalalloc) 來配置適當大小的記憶體區塊，以建立全域記憶體物件。
4.  指派要傳送至 [**GlobalAlloc**](/windows/win32/api/winbase/nf-winbase-globalalloc)所傳回之位址的資料區塊。
5.  將全域記憶體物件的位址指派給 [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1)結構的 **hGlobal** 成員。
6.  藉由呼叫 [**IDataObject：： SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) 並傳入在先前步驟中建立的 [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) 和 [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) 結構，將格式載入資料物件中。

下列範例函式會建立包含 **DWORD** 值的全域記憶體物件，並將其載入至資料物件。 **Pdtobj** 參數是資料物件的 [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject)介面指標， **cf** 是剪貼簿格式的值，而 **dw** 則是資料值。


```C++
STDAPI DataObj_SetDWORD(IDataObject *pdtobj, UINT cf, DWORD dw)
{
    FORMATETC fmte = {(CLIPFORMAT) cf, 
                      NULL, 
                      DVASPECT_CONTENT, 
                      -1, 
                      TYMED_HGLOBAL};
    STGMEDIUM medium;

    HRESULT hres = E_OUTOFMEMORY;
    DWORD *pdw = (DWORD *)GlobalAlloc(GPTR, sizeof(DWORD));
    
    if (pdw)
    {
        *pdw = dw;       
        medium.tymed = TYMED_HGLOBAL;
        medium.hGlobal = pdw;
        medium.pUnkForRelease = NULL;

        hres = pdtobj->SetData(&fmte, &medium, TRUE);
 
        if (FAILED(hres))
            GlobalFree((HGLOBAL)pdw);
    }
    return hres;
}
```



### <a name="implementing-idataobject"></a>執行 IDataObject

[**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) 是資料物件的主要介面。 它必須由所有資料物件實作為。 來源和目標會使用它來因應各種用途，包括：

-   將資料載入資料物件中。
-   從資料物件中提取資料。
-   判斷資料物件中的資料類型。
-   對資料物件提供資料傳輸結果的意見反應。

[**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) 支援多種方法。 本節討論如何針對 Shell 資料物件、 [SetData](#setdata-method)、 [EnumFormatEtc](#enumformatetc-method)和操作方法，執行三個最重要的[方法。](#getdata-method) 如需其他方法的討論，請參閱 **IDataObject** 參考。

### <a name="setdata-method"></a>SetData 方法

[**IDataObject：： SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata)方法的主要功能是讓來源將資料載入資料物件中。 針對要包含的每一種格式，來源會建立 [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) 結構來識別格式，以及用來保存資料指標的 [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) 結構。 然後，來源會呼叫物件的 **IDataObject：： SetData** 方法，並以格式的 **FORMATETC** 和 **STGMEDIUM** 結構傳遞。 方法必須儲存這項資訊，讓它可以在目標呼叫 [**IDataObject：：**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) 來從物件中解壓縮資料時使用。

不過，當傳輸檔案時，Shell 通常會將每個檔案的資訊傳輸到個別的 [CFSTR \_ FILECONTENTS](clipboard.md) 格式。 為了區分不同的檔案，每個檔案的 [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc)結構的 **lIndex** 成員都會設定為識別特定檔案的索引值。 您的 [**IDataObject：： SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) 實電腦必須能夠儲存 \_ 不同于其 **lIndex** 成員的多個 CFSTR FILECONTENTS 格式。

當游標在目標視窗上時，目標可以使用 [拖放 helper 物件](#using-the-drag-and-drop-helper-object) 來指定拖曳影像。 拖放協助程式物件會呼叫 [**IDataObject：： SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) ，將私用格式載入至用於跨進程支援的資料物件中。 為了支援拖放協助程式物件，您的 **IDataObject：： SetData** 實電腦必須能夠接受並儲存任意私用格式。

資料卸載之後，某些類型的 Shell 資料傳輸需要目標呼叫 [**IDataObject：： SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) ，以提供資料物件與 drop 作業結果的相關資訊。 例如，使用優化的移動作業來移動檔案時，目標通常會刪除原始檔案，但不需要這麼做。 目標會透過呼叫 **IDataObject：： SetData** 和 [CFSTR \_ LOGICALPERFORMEDDROPEFFECT](clipboard.md) 格式來通知資料物件是否已刪除檔案。 還有其他數個 [Shell 剪貼簿格式](clipboard.md) ，目標也會使用這些格式，將資訊傳遞給資料物件。 您的 **IDataObject：： SetData** 實電腦必須能夠辨識這些格式並適當地回應。 如需進一步討論，請參閱 [處理 Shell 資料傳輸案例](datascenarios.md)。

### <a name="enumformatetc-method"></a>EnumFormatEtc 方法

當目標收到資料物件時，它通常會呼叫 [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) 來判斷物件所包含的格式。 方法會建立 OLE 列舉物件，並傳回物件之 [**IEnumFORMATETC**](/windows/win32/api/objidl/nn-objidl-ienumformatetc) 介面的指標。 目標接著會使用介面來列舉可用的格式。

列舉物件應該一律以品質的順序來列舉可用的格式，從最佳的開始。 相對品質的格式是由 drop source 所定義。 一般而言，最高品質的格式包含最豐富且最完整的資料。 比方說，24位色彩影像通常會被視為比該影像的灰階版本更高的品質。 依品質的順序來列舉格式的原因是，目標通常會列舉到其所支援的格式，然後使用該格式來將資料解壓縮。 若要讓此程式產生目標可支援的最佳可用格式，必須依品質的順序來列舉格式。

Shell 資料的列舉物件執行方式與其他資料傳輸類型的方式大致相同，但有一個值得注意的例外狀況。 由於資料物件通常只會針對每個格式包含一個資料項目，因此通常會列舉傳遞給 [**IDataObject：： SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata)的每個格式。 不過，如 [SetData 方法](#setdata-method) 一節中所述，Shell 資料物件可以包含多個 [CFSTR \_ FILECONTENTS](clipboard.md) 格式。

因為 [**IDataObject：： EnumFormatEtc**](/windows/win32/api/objidl/nf-objidl-idataobject-enumformatetc) 的目的是要讓目標判斷哪些類型的資料存在，所以不需要列舉一個以上的 [CFSTR \_ FILECONTENTS](clipboard.md) 格式。 如果目標需要知道資料物件所包含的其中一種格式，則目標可以從隨附的 CFSTR FILEDESCRIPTOR 格式取得該資訊 \_ 。 如需如何執行 **IDataObject：： EnumFormatEtc** 的進一步討論，請參閱方法的參考檔。

### <a name="getdata-method"></a>的一種方法

目標會呼叫 [**IDataObject：：**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) ，以解壓縮特定的資料格式。 目標會藉由傳入適當的 [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) 結構來指定格式。 **IDataObject：：** STGMEDIUM 會傳回格式的 [](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1)結構。

目標可以將 [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc)結構的 **tymed** 成員設定為特定的 tymed \_ *XXX* 值，以指定要使用哪一種資料傳輸機制來將資料解壓縮。 不過，目標也可以進行更一般的要求，並讓資料物件決定。 若要要求資料物件選取資料傳輸機制，目標會設定它所支援的所有 TYMED \_ *XXX* 值。 [**IDataObject：：**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) STGMEDIUM 會選取其中一個資料傳輸機制，並傳回適當的 [](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1)結構。 例如， **tymed** 通常會設定為 tymed \_ HGLOBAL \| tymed \_ ISTREAM \| tymed \_ ISTORAGE，以要求三個 Shell 資料傳輸機制的任一個。

> [!Note]  
> 因為可能會有多 [個 CFSTR \_ FILECONTENTS](clipboard.md)格式，所以 [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc)結構的 **cfFormat** 和 **Tymed** 成員不足以指出應該傳回的 [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1)結構 [**IDataObject：：**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) 。 針對 CFSTR \_ FILECONTENTS 格式， **IDataObject：：** 也必須檢查 **FORMATETC** 結構的 **lIndex** 成員，才能傳回正確的 **STGMEDIUM** 結構。

 

[CFSTR \_ INDRAGLOOP](clipboard.md)格式放置於資料物件中，以允許目標檢查拖放迴圈的狀態，同時避免物件資料的記憶體密集呈現。 如果資料物件是在拖曳迴圈內，則格式的資料就是設定為非零值的 **DWORD** 值。 如果資料已卸載，則格式的資料值會設為零。 如果目標要求此格式，但來源尚未載入，則 [**IDataObject：：：：**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) 會回應，就像來源已載入值為零的格式一樣。

當游標在目標視窗上時，目標可以使用 [拖放 helper 物件](#using-the-drag-and-drop-helper-object) 來指定拖曳影像。 拖放協助程式物件會呼叫 [**IDataObject：： SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) ，將私用格式載入至用於跨進程支援的資料物件中。 稍後會呼叫 [**IDataObject：：**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) 來取出它們。 若要支援拖放協助程式物件，您的 Shell 資料物件實作為要求時，必須能夠傳回任意私用格式。

### <a name="implementing-idropsource"></a>執行 IDropSource

來源必須建立公開 [**IDropSource**](/windows/win32/api/oleidl/nn-oleidl-idropsource) 介面的物件。 此介面可讓來源更新表示游標目前位置的 *拖曳影像* ，並提供意見反應給系統，以瞭解如何終止拖放作業。 **IDropSource** 有兩種方法： [**system.windows.dragdrop.givefeedback>**](/windows/win32/api/oleidl/nf-oleidl-idropsource-givefeedback) 和 [**system.windows.dragdrop.querycontinuedrag>**](/windows/win32/api/oleidl/nf-oleidl-idropsource-querycontinuedrag)。

### <a name="givefeedback-method"></a>GiveFeedback 方法

在拖曳迴圈中，卸載來源負責追蹤游標位置，並顯示適當的拖曳影像。 不過，在某些情況下，您可能會想要在拖曳影像超過放置目標的視窗時，變更它的外觀。

當游標進入或離開目標視窗，而且在目標視窗中移動時，系統會定期呼叫目標的 [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) 介面。 目標會以 [**DROPEFFECT**](../com/dropeffect-constants.md) 值回應，此值會透過 [**system.windows.dragdrop.givefeedback>**](/windows/win32/api/oleidl/nf-oleidl-idropsource-givefeedback) 方法轉送至來源。 如果有的話，來源可以根據 **DROPEFFECT** 值修改資料指標的外觀。 如需詳細資訊，請參閱 **system.windows.dragdrop.givefeedback>** 和 [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) 參考。

### <a name="querycontinuedrag-method"></a>QueryContinueDrag 方法

當資料物件在拖曳迴圈中，而滑鼠按鍵或鍵盤狀態變更時，就會呼叫這個方法。 它會通知來源是否已按下 ESC 鍵，並提供鍵盤輔助按鍵的目前狀態，例如 CTRL 或 SHIFT。 [**System.windows.dragdrop.querycontinuedrag>**](/windows/win32/api/oleidl/nf-oleidl-idropsource-querycontinuedrag)方法的傳回值會指定三個動作的其中一個：

-   S \_ 沒問題。 繼續拖曳作業
-   SYSTEM.WINDOWS.DRAGDROP.DROP> \_ S \_ 下降。 捨棄資料。 系統接著會呼叫目標的 [**IDropTarget：:D rop**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) 方法。
-   SYSTEM.WINDOWS.DRAGDROP.DROP> \_ S \_ 取消。 終止拖曳迴圈而不卸載資料。 如果已按下 ESCAPE 鍵，通常會傳回這個值。

如需進一步討論，請參閱 [**system.windows.dragdrop.querycontinuedrag>**](/windows/win32/api/oleidl/nf-oleidl-idropsource-querycontinuedrag) 和 [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) 參考。

## <a name="how-a-target-handles-a-data-object"></a>目標如何處理資料物件

當目標從剪貼簿抓取資料物件，或由使用者在目標視窗上卸載資料物件時，它會接收資料物件。 然後，目標可以從資料物件中提取資料。 如有必要，目標也可以通知資料物件的作業結果。 在 Shell 資料傳輸之前，卸載目標必須為作業準備自己：

1.  目標必須呼叫 [RegisterClipboardFormat](/windows/win32/api/winuser/nf-winuser-registerclipboardformata) ，以針對可能包含在資料物件中的所有 Shell 格式（除了 [CF \_ HDROP](clipboard.md)以外）取得有效的剪貼簿格式值。 CF \_ HDROP 已經是有效的剪貼簿格式，且不需要註冊。
2.  若要支援拖放作業，目標必須執行 [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) 介面並註冊目標視窗。 為了註冊目標視窗，目標會呼叫 [**RegisterDragDrop**](/windows/win32/api/ole2/nf-ole2-registerdragdrop) ，並在視窗的控制碼和 **IDropTarget** 介面指標中傳遞。

針對剪貼簿傳送，目標不會收到資料物件放在剪貼簿上的任何通知。 一般情況下，應用程式會收到物件在剪貼簿上的使用者動作，例如按一下應用程式工具列上的 [貼上] 按鈕。 目標接著會藉由呼叫 [**OleGetClipboard**](/windows/win32/api/ole2/nf-ole2-olegetclipboard)，從剪貼簿抓取資料物件的 [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject)指標。 若為拖放資料傳輸，系統會使用目標的 [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) 介面，為目標提供資料傳輸進度的相關資訊：

-   當游標進入目標視窗時，系統會呼叫 [**IDropTarget：:D ragenter**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter) 。
-   系統會定期呼叫 [**IDropTarget：:D ragover**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) ，因為游標會在目標視窗上傳遞，以將目標設為目前的資料指標位置。
-   當資料指標離開目標視窗時，系統會呼叫 [**IDropTarget：:D ragleave**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragleave) 。
-   當使用者在目標視窗上放置資料物件時，系統會呼叫 [**IDropTarget：:D rop**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) 。

如需如何執行這些方法的討論，請參閱 [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget)。

卸載資料時， [**IDropTarget：:D rop**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) 會為目標提供資料物件的 [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) 介面指標。 然後，目標會使用這個介面從資料物件中取出資料。

### <a name="extracting-shell-data-from-a-data-object"></a>從資料物件解壓縮 Shell 資料

從剪貼簿卸載或抓取資料物件之後，目標就可以將它所需的資料解壓縮。 提取程式中的第一個步驟通常是列舉資料物件所包含的格式：

-   呼叫 [**IDataObject：： EnumFormatEtc**](/windows/win32/api/objidl/nf-objidl-idataobject-enumformatetc)。 資料物件會建立標準的 OLE 列舉物件，並傳回其 [**IEnumFORMATETC**](/windows/win32/api/objidl/nn-objidl-ienumformatetc) 介面的指標。
-   您可以使用 [**IEnumFORMATETC**](/windows/win32/api/objidl/nn-objidl-ienumformatetc) 方法來列舉資料物件所包含的格式。 這項作業通常會針對物件所包含的每種格式，取得一個 [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) 結構。 不過，無論資料物件包含多少種格式，列舉物件通常只會針對 [CFSTR \_ FILECONTENTS](clipboard.md)格式傳回單一 **FORMATETC** 結構。
-   選取一或多個要解壓縮的格式，並儲存其 [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) 結構。

若要取出特定格式，請將相關聯的 [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) 結構傳遞至 [**IDataObject：：**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata)。 這個方法會傳回 [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) 結構，以提供資料的存取權。 若要指定特定的資料傳輸機制，請將 **FORMATETC** 結構的 **tymed** 值設定為對應的 tymed \_ *XXX* 值。 若要要求資料物件選取資料傳輸機制，目標 \_ 會為目標可以處理的每個資料傳輸機制設定 TYMED *XXX* 值。 資料物件會選取其中一個資料傳輸機制，並傳回適當的 **STGMEDIUM** 結構。

針對大部分的格式，目標都可以藉由傳遞在列舉可用格式時所收到的 [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) 結構來取得資料。 這項規則的例外狀況是 [CFSTR \_ FILECONTENTS](clipboard.md)。 因為資料物件可以包含此格式的多個實例，所以列舉值所傳回的 **FORMATETC** 結構可能不會對應至您想要解壓縮的特定格式。 除了指定 **cfFormat** 和 **tymed** 成員之外，您還必須將 **lIndex** 成員設定為檔案的索引值。 如需進一步討論，請參閱 *使用 CFSTR \_ FILECONTENTS 格式從*[處理 Shell 資料傳輸案例](datascenarios.md)的檔案中解壓縮資料一節。

資料解壓縮進程取決於傳回的 [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) 結構所包含的指標類型。 如果結構包含 [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) 或 [**IStorage**](/windows/win32/api/objidl/nn-objidl-istorage) 介面的指標，請使用介面方法來將資料解壓縮。 下一節將討論從全域記憶體物件中解壓縮資料的程式。

### <a name="extracting-a-global-memory-object-from-a-data-object"></a>從資料物件解壓縮全域記憶體物件

許多 Shell 資料格式都是全域記憶體物件的形式。 使用下列程式，從資料物件解壓縮包含全域記憶體物件的格式，並將其資料指派給本機變數：

1.  建立 [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) 結構。 將 **cfFormat** 成員設定為適當的剪貼簿格式值，並將 **tymed** 成員設定為 tymed \_ HGLOBAL。
2.  建立空的 [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) 結構。
3.  呼叫 [**IDataObject：：**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata)，並傳入 [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) 和 [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) 結構的指標。

    當 [**IDataObject：：**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) STGMEDIUM 結構傳回時， [](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1)結構將包含包含資料之全域記憶體物件的指標。

4.  藉由呼叫 [**GlobalLock**](/windows/win32/api/winbase/nf-winbase-globallock)並傳入 [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1)結構的 **hGlobal** 成員，將資料指派給區域變數。
5.  呼叫 [**GlobalUnlock**](/windows/win32/api/winbase/nf-winbase-globalunlock) 以釋放全域記憶體物件的鎖定。
6.  呼叫 [**ReleaseStgMedium**](/windows/win32/api/ole2/nf-ole2-releasestgmedium) 以釋放全域記憶體物件。

> [!Note]  
> 您必須使用 [**ReleaseStgMedium**](/windows/win32/api/ole2/nf-ole2-releasestgmedium) 來釋放全域記憶體物件，而不是 [**GlobalFree**](/windows/win32/api/winbase/nf-winbase-globalfree)。

 

下列範例示範如何從資料物件將儲存為全域記憶體物件的 **DWORD** 值解壓縮。 **Pdtobj** 參數是資料物件的 [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject)介面指標， **cf** 是用來識別所需資料的剪貼簿格式，而 **pdwOut** 則是用來傳回資料值。


```C++
STDAPI DataObj_GetDWORD(IDataObject *pdtobj, UINT cf, DWORD *pdwOut)
{    STGMEDIUM medium;
   FORMATETC fmte = {(CLIPFORMAT) cf, NULL, DVASPECT_CONTENT, -1, 
       TYMED_HGLOBAL};
    HRESULT hres = pdtobj->GetData(&fmte, &medium);
    if (SUCCEEDED(hres))
   {
       DWORD *pdw = (DWORD *)GlobalLock(medium.hGlobal);
       if (pdw)
       {
           *pdwOut = *pdw;
           GlobalUnlock(medium.hGlobal);
       }
       else
       {
           hres = E_UNEXPECTED;
       }
       ReleaseStgMedium(&medium);
   }
   return hres;
}
```



### <a name="implementing-idroptarget"></a>執行 IDropTarget

當游標位於目標視窗上時，系統會使用 [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) 介面來與目標通訊。 目標的回應會透過其 [**IDropSource**](/windows/win32/api/oleidl/nn-oleidl-idropsource) 介面轉送至來源。 根據回應，來源可以修改代表資料的圖示。 如果放置目標需要指定資料圖示，就可以建立 [拖放](#using-the-drag-and-drop-helper-object)協助程式物件來完成此動作。

使用傳統的拖放作業時，目標會將 [**IDropTarget：:D rop**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop)的 *pdwEffect* 參數設定為適當的 [**DROPEFFECT**](../com/dropeffect-constants.md)值，以通知資料物件結果。 使用 Shell 資料物件時，目標可能也需要呼叫 [**IDataObject：： SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata)。 如需如何針對不同的資料傳輸案例回應目標的討論，請參閱 [處理 Shell 資料傳輸案例](datascenarios.md)。

下列各節將簡短討論如何執行 [**IDropTarget：:D ragenter**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter)、 [**IDropTarget：:D ragover**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover)和 [**IDropTarget：:D rop**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) 方法。 如需詳細資訊，請參閱參考檔。

### <a name="dragenter-method"></a>System.windows.dragdrop.dragenter> 方法

當游標進入目標視窗時，系統會呼叫 [**IDropTarget：:D ragenter**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter) 方法。 它的參數會為目標提供游標位置、鍵盤輔助按鍵的狀態（例如 CTRL 鍵），以及資料物件之 [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) 介面的指標。 目標負責使用該介面來判斷它是否可以接受資料物件所包含的任何格式。 如果可以，通常會將 *pdwEffect* 的值保持不變。 如果它無法接受資料物件中的任何資料，則會將 *pdwEffect* 參數設定為 DROPEFFECT \_ NONE。 系統會將此參數的值傳遞至資料物件的 [**IDropSource**](/windows/win32/api/oleidl/nn-oleidl-idropsource) 介面，以允許它顯示適當的拖曳影像。

目標不應使用 [**IDataObject：：：：：：**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) 的方法來轉譯 Shell 資料，然後再將它卸載。 針對每一種情況，完全呈現物件的資料，可能會導致拖曳游標停止。 為了避免這個問題，某些 Shell 物件包含 [CFSTR \_ INDRAGLOOP](clipboard.md) 格式。 藉由將此格式解壓縮，目標可以檢查拖曳迴圈的狀態，同時避免物件資料的記憶體密集呈現。 如果資料物件是在拖曳迴圈內，則格式的資料值是設定為非零值的 **DWORD** 。 如果資料已卸載，則格式的資料值會設為零。

如果目標可以接受資料物件中的資料，它應該會檢查 **grfKeyState** ，以判斷是否已按下任何輔助按鍵來修改正常的卸載行為。 例如，預設作業通常是移動，但按下 CTRL 鍵通常表示複製操作。

當游標在目標視窗上時，目標可以使用 [拖放協助程式物件](#using-the-drag-and-drop-helper-object) 來取代資料物件的拖曳影像。 如果是， [**IDropTarget：:D ragenter**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter) 應該呼叫 [**IDropTargetHelper：:D Ragenter**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-dragenter) ，將 *system.windows.dragdrop.dragenter>* 參數中包含的資訊傳遞給拖放 helper 物件。

### <a name="dragover-method"></a>System.windows.dragdrop.dragover> 方法

當資料指標在目標視窗內移動時，系統會定期呼叫 [**IDropTarget：:D ragover**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) 方法。 其參數會為目標提供游標的位置，以及鍵盤輔助按鍵（例如 CTRL 鍵）的狀態。 **IDropTarget：:D ragover** 與 [**IDropTarget：:D ragenter**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter)有許多相同的責任，而且這些執行通常很類似。

如果目標是使用拖放協助程式物件， [**IDropTarget：:D ragover**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) 應該呼叫 [**IDropTargetHelper：:D ragover**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-dragover) 將 *system.windows.dragdrop.dragover>* 參數中包含的資訊轉送至拖放 helper 物件。

### <a name="drop-method"></a>Drop 方法

系統會呼叫 [**IDropTarget：:D rop**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) 方法，以通知目標使用者已卸載資料，通常是透過放開滑鼠按鍵。 **IDropTarget：:D rop** 具有與 [**IDropTarget：:D ragenter**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter)相同的參數。 目標通常會從資料物件中解壓縮一或多個格式來回應。 完成時，目標應該將 *pdwEffect* 參數設定為 [**DROPEFFECT**](../com/dropeffect-constants.md) 值，以指出作業的結果。 針對某些類型的 Shell 資料傳輸，目標也必須呼叫 [**IDataObject：： SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) 來傳遞格式，以及將作業結果的其他資訊傳遞至資料物件。 如需詳細的討論，請參閱 [處理 Shell 資料傳輸案例](datascenarios.md)。

如果目標是使用拖放協助程式物件， [**IDropTarget：:D rop**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) 應該呼叫 [**IDropTargetHelper：:D rop**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-drop) 將 [**IDropTargetHelper：:D ragover**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-dragover) 參數中包含的資訊轉送到拖放 helper 物件。

## <a name="using-the-drag-and-drop-helper-object"></a>使用拖放 Helper 物件

 (CLSID DragDropHelper) 的拖放協助程式物件 \_ 會由 Shell 匯出，以允許目標在目標視窗上時指定拖曳影像。 若要使用拖放協助程式物件，請使用 CLSID DragDropHelper 的 CLSID) 呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 來建立 (同進程伺服器物件 \_ 。 拖放協助程式物件會公開兩個以下列方式使用的介面：

-   [**IDragSourceHelper**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idragsourcehelper)介面允許放置目標指定代表資料物件的圖示。
-   [**IDropTargetHelper**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idroptargethelper)介面可讓放置目標通知游標位置的拖放 helper 物件，以及顯示或隱藏資料圖示。

### <a name="using-the-idragsourcehelper-interface"></a>使用 IDragSourceHelper 介面

[**IDragSourceHelper**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idragsourcehelper)介面是由拖放協助程式物件公開，可讓放置目標提供當游標位於目標視窗上方時所顯示的影像。 **IDragSourceHelper** 提供兩種替代方式來指定用來作為拖曳影像的點陣圖：

-   您可以 \_ 使用 [**IDragSourceHelper：： InitializeFromWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idragsourcehelper-initializefromwindow)初始化拖放協助程式物件，藉以為視窗註冊 DI GETDRAGIMAGE 視窗訊息，以放置視窗。 當目標收到 DI \_ GETDRAGIMAGE 訊息時，處理常式會將拖曳影像點陣圖資訊放在傳遞做為訊息 *lParam* 值的 [**SHDRAGIMAGE**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-shdragimage)結構中。
-   無視窗的放置目標會在使用 [**IDragSourceHelper：： InitializeFromBitmap**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idragsourcehelper-initializefrombitmap)初始化拖放協助程式物件時，指定點陣圖。

### <a name="using-the-idroptargethelper-interface"></a>使用 IDropTargetHelper 介面

當游標進入或離開目標時，此介面可讓放置目標通知拖放 helper 物件。 當游標停留在目標視窗上時， [**IDropTargetHelper**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idroptargethelper) 可讓目標為拖放 helper 物件提供目標透過其 [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) 介面接收的資訊。

有四個 [**IDropTargetHelper**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idroptargethelper) 方法（[**IDropTargetHelper：:D ragenter**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-dragenter)、 [**IDropTargetHelper：:D Ragleave**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-dragleave)、 [**IDropTargetHelper：:D ragover**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-dragover)和 [**IDropTargetHelper：:D rop**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-drop)）與相同名稱的 [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) 方法相關聯。 若要使用拖放協助程式物件，每個 **IDropTarget** 方法都應該呼叫對應的 **IDropTargetHelper** 方法，將資訊轉送到拖放 helper 物件。 第五個 **IDropTargetHelper** 方法（ [**IDropTargetHelper：： Show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-show)）會通知拖放協助程式物件顯示或隱藏拖曳影像。 在較低色彩深度的影片模式中拖曳目標視窗時，會使用這個方法。 它可讓目標在繪製視窗時隱藏拖曳影像。

 

 
