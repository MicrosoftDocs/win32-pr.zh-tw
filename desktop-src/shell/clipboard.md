---
description: Shell 剪貼簿格式是用來識別透過剪貼簿傳輸之 Shell 資料的類型。
ms.assetid: fb8ce5d3-3215-4e05-a916-4d4a803464d2
title: Shell 剪貼簿格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 674ccc33db3a35a1a60abb549f5e1ab5b5c96760
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689811"
---
# <a name="shell-clipboard-formats"></a>Shell 剪貼簿格式

Shell 剪貼簿格式是用來識別透過剪貼簿傳輸之 Shell 資料的類型。 大部分的 Shell 剪貼簿格式都會識別資料類型，例如檔案名或專案識別碼清單的指標清單 (Pidl) 。 不過，某些格式會用於來源與目標之間的通訊。 藉由支援 Shell 作業（例如 [優化的移動](datascenarios.md) 和 [delete_on_paste](datascenarios.md)），他們可以加速資料傳輸流程。 Shell 資料一律包含在使用 [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc)結構作為資料特性之一般方式的 [資料物件](dataobject.md)中。 結構的 **cfFormat** 成員會設定為特定資料項目目的剪貼簿格式。 其他成員則提供其他資訊，例如資料傳輸機制。 資料會包含在隨附的 [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) 結構中。

> [!Note]  
> 標準剪貼簿格式識別碼的格式為 CF_ *XXX*。 常見的範例是 CF_TEXT，用來傳送 ANSI 文字資料。 這些識別碼具有預先定義的值，而且可以直接搭配 [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) 結構使用。 除了 [CF_HDROP](#cf_hdrop)之外，不會預先定義 Shell 格式識別碼。 除了 DragWindow 之外，它們的格式 CFSTR_ *XXX*。 為了區分這些值與預先定義的格式，這些值通常稱為單純 *格式*。 不過，與預先定義的格式不同的是，它們必須由來源和目標注冊，才能用來傳送資料。 若要註冊 Shell 格式，請包含 Shlobj.h .h 標頭檔，並將 CFSTR_ *XXX* 格式識別碼傳遞至 [RegisterClipboardFormat](/windows/win32/api/winuser/nf-winuser-registerclipboardformata)。 此函式會傳回有效的剪貼簿格式值，然後用來做為 **FORMATETC** 結構的 **cfFormat** 成員。

 

Shell 剪貼簿格式會根據使用方式，分成三個群組。

-   [傳送檔案系統物件的格式](#formats-for-transferring-file-system-objects)
    -   [CF_HDROP](#cf_hdrop)
    -   [CFSTR_FILECONTENTS](#cfstr_filecontents)
    -   [CFSTR_FILEDESCRIPTOR](#cfstr_filedescriptor)
    -   [CFSTR_FILENAME](#cfstr_filename)
    -   [CFSTR_FILENAMEMAP](#cfstr_filenamemap)
    -   [CFSTR_MOUNTEDVOLUME](#cfstr_mountedvolume)
    -   [CFSTR_SHELLIDLIST](#cfstr_shellidlist)
    -   [CFSTR_SHELLIDLISTOFFSET](#cfstr_shellidlistoffset)
-   [傳輸虛擬物件的格式](#formats-for-transferring-virtual-objects)
    -   [CFSTR_NETRESOURCES](#cfstr_netresources)
    -   [CFSTR_PRINTERGROUP](#cfstr_printergroup)
    -   [CFSTR_INETURL](#cfstr_ineturl)
    -   [CFSTR_SHELLURL (已淘汰) ](#cfstr_shellurl-deprecated)
-   [來源與目標之間通訊的格式](#formats-for-communication-between-source-and-target)
    -   [CFSTR_INDRAGLOOP](#cfstr_indragloop)
    -   [CFSTR_LOGICALPERFORMEDDROPEFFECT](#cfstr_logicalperformeddropeffect)
    -   [CFSTR_PASTESUCCEEDED](#cfstr_pastesucceeded)
    -   [CFSTR_PERFORMEDDROPEFFECT](#cfstr_performeddropeffect)
    -   [CFSTR_PREFERREDDROPEFFECT](#cfstr_preferreddropeffect)
    -   [CFSTR_TARGETCLSID](#cfstr_targetclsid)
    -   [CFSTR_UNTRUSTEDDRAGDROP](#cfstr_untrusteddragdrop)
    -   [DragWindow](#dragwindow)

## <a name="formats-for-transferring-file-system-objects"></a>傳送檔案系統物件的格式

這些格式是用來傳送一個或多個檔案或其他 Shell 物件。

-   [CF_HDROP](#cf_hdrop)
-   [CFSTR_FILECONTENTS](#cfstr_filecontents)
-   [CFSTR_FILEDESCRIPTOR](#cfstr_filedescriptor)
-   [CFSTR_FILENAME](#cfstr_filename)
-   [CFSTR_FILENAMEMAP](#cfstr_filenamemap)
-   [CFSTR_MOUNTEDVOLUME](#cfstr_mountedvolume)
-   [CFSTR_SHELLIDLIST](#cfstr_shellidlist)
-   [CFSTR_SHELLIDLISTOFFSET](#cfstr_shellidlistoffset)

### <a name="cf_hdrop"></a>CF_HDROP

傳送現有檔案群組的位置時，會使用此剪貼簿格式。 與其他 Shell 格式不同的是，它是預先定義的，因此不需要呼叫 [RegisterClipboardFormat](/windows/win32/api/winuser/nf-winuser-registerclipboardformata)。 資料是由包含全域記憶體物件的 [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) 結構所組成。 結構的 **hGlobal** 成員會指向 [**DROPFILES**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropfiles) 結構作為其 **hGlobal** 成員。

[**DROPFILES**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropfiles)結構的 **pFiles** 成員包含雙精度浮點數（以 **null** 結束的字元陣列）的位移，該陣列包含檔案名。 如果您要從資料物件中解壓縮 CF_HDROP 格式，您可以使用 [**DragQueryFile**](/windows/desktop/api/Shellapi/nf-shellapi-dragqueryfilea) 從全域記憶體物件中解壓縮個別的檔案名。 如果您要建立要在資料物件中放置 CF_HDROP 格式，就必須建立檔案名陣列。

檔案名陣列是由一連串的字串所組成，每個字串都包含一個檔案的完整路徑，包括結束的 **Null** 字元。 最後一個字串會附加 **null** 字元，以終止陣列。 例如，如果正在傳送檔案 c： \\temp1.txt 和 c： \\temp2.txt，則字元陣列看起來像這樣：


```CMD
c:\temp1.txt'\0'c:\temp2.txt'\0''\0'
```

> [!Note]  
> 在此範例中，' \\ 0 ' 是用來表示 **null** 字元，而不是應該包含的常值字元。


如果將物件複製到剪貼簿做為拖放作業的一部分， [**DROPFILES**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropfiles)結構的 **pt** 成員就會包含卸載物件之點的座標。 您可以使用 [**DragQueryPoint**](/windows/desktop/api/Shellapi/nf-shellapi-dragquerypoint) 來將資料指標座標解壓縮。

如果資料物件中有此格式，OLE 拖曳迴圈會模擬具有非 OLE 卸載目標的 [**WM_DROPFILES**](wm-dropfiles.md) 功能。 如果您的應用程式是 Windows 3.1 系統上拖放作業的來源，這就很重要。

### <a name="cfstr_filecontents"></a>CFSTR_FILECONTENTS

此格式識別碼會搭配 [CFSTR_FILEDESCRIPTOR](#cfstr_filedescriptor) 格式使用，以像是檔案一樣傳送資料，而不論實際儲存的方式為何。 資料包含代表一個檔案內容的 [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) 結構。 檔案通常會表示為數據流物件，以避免必須將檔案的內容放在記憶體中。 在這種情況下， **STGMEDIUM** 結構的 **tymed** 成員會設定為 TYMED_ISTREAM，而檔案是由 [**ISTREAM**](/windows/win32/api/objidl/nn-objidl-istream)介面表示。 檔案也可以是儲存或全域記憶體物件 (TYMED_ISTORAGE 或 TYMED_HGLOBAL) 。 相關聯的 CFSTR_FILEDESCRIPTOR 格式會包含每個檔案的 [**FILEDESCRIPTOR**](/windows/win32/api/shlobj_core/ns-shlobj_core-filedescriptora) 結構，以指定檔案的名稱和屬性。

目標會將與 CFSTR_FILECONTENTS 格式相關聯的資料視為檔案。 當目標呼叫 [**IDataObject：：**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) FILEDESCRIPTOR 來解壓縮資料時，它會藉由將 FORMATETC 結構的 lindex 成員設定為隨附的 [CFSTR_FILEDESCRIPTOR](#cfstr_filedescriptor)格式，將 [](/windows/win32/api/objidl/ns-objidl-formatetc)結構的成員設定為檔案 [](/windows/win32/api/shlobj_core/ns-shlobj_core-filedescriptora)結構的以零為起始的索引，以指定特定的檔案。 目標接著會使用傳回的介面指標或全域記憶體控制碼來將資料解壓縮。

### <a name="cfstr_filedescriptor"></a>CFSTR_FILEDESCRIPTOR

此格式識別碼會搭配 [CFSTR_FILECONTENTS](#cfstr_filecontents) 格式使用，以將資料當做一組檔案來傳送。 這兩種格式是傳輸 Shell 物件（不會儲存為檔案系統檔案）的慣用方法。 例如，這些格式可以用來將一組電子郵件訊息當作個別檔案來傳送，即使每封電子郵件實際上都儲存為資料庫中的資料區塊也是一樣。 資料是由包含全域記憶體物件的 [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) 結構所組成。 結構的 **hGlobal** 成員指向 [**FILEGROUPDESCRIPTOR**](/windows/win32/api/shlobj_core/ns-shlobj_core-filegroupdescriptora) 結構，後面接著一個陣列，其中包含群組中每個檔案的一個 [**FILEDESCRIPTOR**](/windows/win32/api/shlobj_core/ns-shlobj_core-filedescriptora) 結構。 針對每個 **FILEDESCRIPTOR** 結構，有一個包含檔案內容的個別 CFSTR_FILECONTENTS 格式。 若要識別特定檔案的 CFSTR_FILECONTENTS 格式，請將 [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc)結構的 **lIndex** 值設定為檔案 **FILEDESCRIPTOR** 結構的以零為基底的索引。

CFSTR_FILEDESCRIPTOR 格式通常用來傳送資料，就像是一組檔案一樣，不論實際儲存的方式為何。 從目標的觀點來看，每個 CFSTR_FILECONTENTS 格式都代表一個檔案，並據此處理。 不過，來源可以用任何選擇的方式來儲存資料。 雖然 CSFTR_FILECONTENTS 格式可能對應至單一檔案，但它也可能代表從資料庫或文字檔中的來源所解壓縮的資料。

### <a name="cfstr_filename"></a>CFSTR_FILENAME

此格式識別碼是用來傳送單一檔案。 資料是由包含全域記憶體物件的 [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) 結構所組成。 結構的 **hGlobal** 成員指向單一以 **null** 終止的字串，其中包含檔案的完整檔案路徑。 [CF_HDROP](#cf_hdrop)已取代此格式，但支援與 Windows 3.1 應用程式的回溯相容性。

### <a name="cfstr_filenamemap"></a>CFSTR_FILENAMEMAP

當 [CF_HDROP](#cf_hdrop) 格式的檔案群組重新命名及傳輸時，就會使用此格式識別碼。 資料是由包含全域記憶體物件的 [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) 結構所組成。 結構的 **hGlobal** 成員指向雙 **null** 結束的字元陣列。 此陣列包含每個檔案的新名稱，順序與隨附的 CF_HDROP 格式相同。 字元陣列的格式與 CF_HDROP 用來列出已傳送檔案的格式相同。

### <a name="cfstr_mountedvolume"></a>CFSTR_MOUNTEDVOLUME

此格式識別碼是用來在載入的磁片區上傳送路徑。 它類似于 [CF_HDROP](#cf_hdrop)，但它只包含單一路徑，而且可以處理在資料夾上掛接磁片區時，可能需要用來代表路徑的較長路徑字串。 資料是由包含全域記憶體物件的 [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) 結構所組成。 結構的 **hGlobal** 成員指向單一以 **null** 終止的字串，其中包含完整的檔案路徑。 路徑字串的結尾必須是 ' \\ ' 字元，後面接著終止的 **Null**。

在 Windows 2000 之前，只能將磁片區掛接在磁碟機號上。 針對具有 NTFS 格式化磁片磁碟機的 Windows 2000 和更新版本的系統，您也可以在空的資料夾上裝載磁片區。 這項功能可讓您掛接磁片區，而不需要佔用磁碟機號。 載入的磁片區可以使用任何目前支援的格式，包括 FAT、FAT32、NTFS 和 CDFS.SYS。

您可以藉由執行 [屬性工作表處理常式](propsheet-handlers.md)，將頁面加入至磁片磁碟機屬性屬性工作表。 如果磁片區是掛接在磁碟機號上，Shell 會將路徑資訊傳遞給具有 [CF_HDROP](#cf_hdrop) 格式的處理常式。 在 Windows 2000 和更新版本的系統中，將磁片區掛接到磁碟機號時，就會使用 CF_HDROP 格式，就像舊版系統一樣。 但是，如果磁片區掛接在資料夾上，則會使用 [CFSTR_MOUNTEDVOLUME](#cfstr_mountedvolume) 格式識別碼，而不是 CF_HDROP。

如果只會使用磁碟機號來裝載磁片區，則只會使用 [CF_HDROP](#cf_hdrop) ，而現有的屬性工作表處理常式會像處理舊版系統一樣運作。 但是，如果您想要讓處理常式針對掛接于資料夾以及磁碟機號的磁片區顯示頁面，則處理常式必須能夠同時瞭解 CSFTR_MOUNTEDVOLUME 和 CF_HDROP 格式。

### <a name="cfstr_shellidlist"></a>CFSTR_SHELLIDLIST

傳送一個或多個現有命名空間物件的位置時，會使用此格式識別碼。 它的使用方式與 [CF_HDROP](#cf_hdrop)很類似，但它包含 pidl，而不是檔案系統路徑。 使用 Pidl 可讓 CFSTR_SHELLIDLIST 格式處理虛擬物件以及檔案系統物件。 資料是包含全域記憶體物件的 [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) 結構。 結構的 **hGlobal** 成員會指向 [**CIDA**](/windows/win32/api/shlobj_core/ns-shlobj_core-cida) 結構。

[**CIDA**](/windows/win32/api/shlobj_core/ns-shlobj_core-cida)結構的 **aoffset** 成員是一個陣列，其中包含要傳送之每個 PIDL 的 [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist)結構開頭位移。 若要解壓縮特定的 PIDL，請先決定其索引。 然後，將對應至該索引的 **aoffset** 值加入至 **CIDA** 結構的位址。

**Aoffset** 的第一個元素包含父資料夾完整 PIDL 的位移。 如果這個 PIDL 是空的，則上層資料夾是桌面。 陣列其餘的每個元素都包含要傳送的其中一個 Pidl 的位移。 這些 Pidl 都是相對於父資料夾的 PIDL。

下列兩個宏可以用來從 [**CIDA**](/windows/win32/api/shlobj_core/ns-shlobj_core-cida) 結構取出 pidl。 第一個會接受結構的指標，並抓取父資料夾的 PIDL。 第二個會使用結構的指標，並取得以零為基底之索引所識別的其他 Pidl 之一。


```C++
#define GetPIDLFolder(pida) (LPCITEMIDLIST)(((LPBYTE)pida)+(pida)->aoffset[0])

#define GetPIDLItem(pida, i) (LPCITEMIDLIST)(((LPBYTE)pida)+(pida)->aoffset[i+1])
```

> [!Note]  
> 這些宏所傳回的值是 PIDL 之 [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) 結構的指標。 因為這些結構的長度不同，所以您必須透過逐步執行每個 **ITEMIDLIST** 結構的 [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) 結構來判斷結構的結尾，直到達到標示結尾的雙位元組 **Null** 為止。

### <a name="cfstr_shellidlistoffset"></a>CFSTR_SHELLIDLISTOFFSET

此格式識別碼會搭配 [CF_HDROP](#cf_hdrop)、 [CFSTR_SHELLIDLIST](#cfstr_shellidlist)和 [CFSTR_FILECONTENTS](#cfstr_filecontents) 等格式使用，以指定在傳輸之後物件群組的位置。 資料是由包含全域記憶體物件的 [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) 結構所組成。 結構的 **hGlobal** 成員指向 [**點**](/previous-versions//dd162805(v=vs.85)) 結構的陣列。 第一個結構指定包圍群組之矩形左上角的螢幕座標（以圖元為單位）。 結構的其餘部分會指定相對於群組位置之個別物件的位置。 它們的順序必須與用來列出相關格式之物件的順序相同。

## <a name="formats-for-transferring-virtual-objects"></a>傳輸虛擬物件的格式

CFSTR_SHELLIDLIST 格式可以用來傳送檔案系統和虛擬物件。 不過，也有數種特殊格式可用於傳輸特定類型的虛擬物件。

-   [CFSTR_NETRESOURCES](#cfstr_netresources)
-   [CFSTR_PRINTERGROUP](#cfstr_printergroup)
-   [CFSTR_INETURL](#cfstr_ineturl)
-   [CFSTR_SHELLURL (已淘汰) ](#cfstr_shellurl-deprecated)

### <a name="cfstr_netresources"></a>CFSTR_NETRESOURCES

傳輸網路資源（例如網域或伺服器）時，會使用此格式識別碼。 資料是包含全域記憶體物件的 [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) 結構。 結構的 **hGlobal** 成員會指向 [**NRESARRAY**](/windows/desktop/api/shlobj_core/ns-shlobj_core-nresarray) 結構。 該結構的 **nr** 成員表示 [**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) 結構，其 **lpRemoteName** 成員包含可識別網路資源的以 **null** 終止的字串。 然後，卸載目標可將資料與任何 [Windows 網路 (WNet)](../wnet/windows-networking-wnet-.md) API 函式（例如 [**WNetAddConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnectiona)）搭配使用，以在物件上執行網路作業。

### <a name="cfstr_printergroup"></a>CFSTR_PRINTERGROUP

傳送易記的印表機名稱時，會使用此格式識別碼。 資料是包含全域記憶體物件的 [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) 結構。 結構的 **hGlobal** 成員會指向與 [CF_HDROP](#cf_hdrop)搭配使用之格式相同的字串。 但是， [**DROPFILES**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropfiles)結構的 **pFiles** 成員會包含一或多個易記的印表機名稱，而不是檔案路徑。

### <a name="cfstr_ineturl"></a>CFSTR_INETURL

此格式識別碼會取代 [CFSTR_SHELLURL (已淘汰的) ](#cfstr_shellurl-deprecated)。 如果您想要讓應用程式操作剪貼簿 Url，請使用 CFSTR_INETURL 而不是 CFSTR_SHELLURL (已淘汰的) 。 這種格式可提供最佳的單一 URL 剪貼簿表示。 如果未定義 UNICODE，則應用程式會抓取 URL 的 CF_TEXT/CFSTR_SHELLURL 版本。 如果已定義 UNICODE，則應用程式會抓取 URL 的 CF_UNICODE 版本。

### <a name="cfstr_shellurl-deprecated"></a>CFSTR_SHELLURL (已淘汰) 

> [!Note]  
> 此格式識別碼已被取代;請改用 CFSTR_INETURL。

 

## <a name="formats-for-communication-between-source-and-target"></a>來源與目標之間通訊的格式

這些格式識別碼允許來源與目標之間的通訊。 伴隨資料的格式，並讓應用程式更能掌控與 Shell 物件有關的移動-複製貼上或拖放作業。

-   [CFSTR_INDRAGLOOP](#cfstr_indragloop)
-   [CFSTR_LOGICALPERFORMEDDROPEFFECT](#cfstr_logicalperformeddropeffect)
-   [CFSTR_PASTESUCCEEDED](#cfstr_pastesucceeded)
-   [CFSTR_PERFORMEDDROPEFFECT](#cfstr_performeddropeffect)
-   [CFSTR_PREFERREDDROPEFFECT](#cfstr_preferreddropeffect)
-   [CFSTR_TARGETCLSID](#cfstr_targetclsid)
-   [CFSTR_UNTRUSTEDDRAGDROP](#cfstr_untrusteddragdrop)
-   [DragWindow](#dragwindow)

### <a name="cfstr_indragloop"></a>CFSTR_INDRAGLOOP

資料物件會使用此格式識別碼來指出它是否在拖放迴圈中。 資料是包含全域記憶體物件的 [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) 結構。 結構的 **hGlobal** 成員指向 **DWORD** 值。 如果 **DWORD** 值為非零值，則資料物件在拖放迴圈內。 如果值設定為零，則資料物件不在拖放迴圈內。

某些卸載目標可能會呼叫 [**IDataObject：：**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) ，並在物件仍在拖放迴圈內時嘗試將資料解壓縮。 針對每個這種情況完全呈現物件，可能會導致拖曳游標停止。 如果資料物件支援 [CFSTR_INDRAGLOOP](#cfstr_indragloop)，目標可以改為使用該格式來檢查拖放迴圈的狀態，並避免物件的記憶體密集轉譯，直到實際卸載為止。 記憶體密集轉譯的格式應該仍包含在 [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) 列舉值中，以及 [**IDataObject：： QueryGetData**](/windows/win32/api/objidl/nf-objidl-idataobject-querygetdata)的呼叫中。 如果資料物件未設定 CFSTR_INDRAGLOOP，則應該將值設定為零。

### <a name="cfstr_logicalperformeddropeffect"></a>CFSTR_LOGICALPERFORMEDDROPEFFECT

[版本5.0。](versions.md)此格式識別碼可讓卸載來源呼叫資料物件的 [**IDataObject：：**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) 的方法，以判斷 Shell 資料傳輸的結果。 資料是包含全域記憶體物件的 [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) 結構。 結構的 **hGlobal** 成員會指向包含 [**DROPEFFECT**](../com/dropeffect-constants.md) 值的 DWORD。

[CFSTR_PERFORMEDDROPEFFECT](#cfstr_performeddropeffect)格式識別碼的目的是要讓目標向資料物件指出實際發生的作業。 不過，Shell 會盡可能針對檔案系統物件使用 [優化的移動](datascenarios.md) 。 在此情況下，Shell 通常會將 CFSTR_PERFORMEDDROPEFFECT 值設定為 DROPEFFECT_NONE，以向資料物件表示已刪除原始資料。 因此，來源無法使用 CFSTR_PERFORMEDDROPEFFECT 值來判斷發生了哪些作業。 雖然大部分的來源都不需要這項資訊，但還是有一些例外狀況。 例如，即使優化的移動不需要讓來源刪除任何資料，來源可能仍需要更新相關的資料庫，以指出檔案已移動或複製。

如果來源需要知道發生的是哪一個作業，它可以呼叫資料物件的 [**IDataObject：：**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) 的方法，並要求 CFSTR_LOGICALPERFORMEDDROPEFFECT 格式。 這種格式基本上會反映在作業完成之後，從使用者的觀點來看，會發生什麼事。 如果已建立新的檔案，並刪除原始檔案，則使用者會看見移動作業，而且格式的資料值會設定為 DROPEFFECT_MOVE。 如果原始檔案仍在該處，則使用者會看到複製作業，而且格式的資料值會設定為 DROPEFFECT_COPY。 如果已建立連結，將會 DROPEFFECT_LINK 格式的資料值。

### <a name="cfstr_pastesucceeded"></a>CFSTR_PASTESUCCEEDED

目標會使用此格式識別碼，透過其 [**IDataObject：： SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) 方法來通知資料物件，即刪除貼上作業已成功。 資料是包含全域記憶體物件的 [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) 結構。 結構的 **hGlobal** 成員會指向包含 [**DROPEFFECT**](../com/dropeffect-constants.md)值的 **DWORD** 。 這種格式是用來通知資料物件應完成剪下作業，並視需要刪除原始資料。 如需詳細資訊，請參閱「 [刪除時刪除」作業](datascenarios.md)。

### <a name="cfstr_performeddropeffect"></a>CFSTR_PERFORMEDDROPEFFECT

目標會使用此格式識別碼，透過資料傳輸結果的 [**IDataObject：： SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) 方法來通知資料物件。 資料是包含全域記憶體物件的 [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) 結構。 結構的 **hGlobal** 成員會指向設定為適當 [**DROPEFFECT**](../com/dropeffect-constants.md)值的 **DWORD** ，通常是 DROPEFFECT_MOVE 或 DROPEFFECT_COPY。

這種格式通常會在作業的結果可以是移動或複製時使用，例如在 [優化的移動](datascenarios.md) 或刪除貼上作業中。 它提供可靠的方式，讓目標知道實際發生的資料物件。 這是因為 [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop)所傳回的 *pdwEffect* 值未可靠地指出發生了哪些作業而引進的。 [CFSTR_PERFORMEDDROPEFFECT](#cfstr_performeddropeffect)格式是表示已進行未優化移動的可靠方式。

### <a name="cfstr_preferreddropeffect"></a>CFSTR_PREFERREDDROPEFFECT

來源會使用此格式識別碼來指定其慣用的資料傳輸方法是移動或複製。 放置目標會藉由呼叫資料物件的 [**IDataObject：：：：：：**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) 的方法來要求此格式。 資料是包含全域記憶體物件的 [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) 結構。 結構的 **hGlobal** 成員指向 **DWORD** 值。 如果慣用移動作業，則此值會設定為 DROPEFFECT_MOVE，如果偏好複製作業則為 DROPEFFECT_COPY。

當來源可以支援移動或複製作業時，就會使用這項功能。 它會使用 [CFSTR_PREFERREDDROPEFFECT](#cfstr_preferreddropeffect) 格式，將其喜好設定與目標通訊。 因為目標並不負責接受要求，所以目標必須以 [CFSTR_PERFORMEDDROPEFFECT](#cfstr_performeddropeffect)格式呼叫來源的 [**IDataObject：： SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata)方法，以告知資料物件實際執行的作業。

使用「 [刪除時刪除](datascenarios.md) 」作業時，CFSTR_PREFERREDDROPFORMAT 格式會用來告知目標來源是否已剪下或複製。 使用拖放作業時，您可以使用 CFSTR_PREFERREDDROPFORMAT 來指定 Shell 的動作。 如果不存在此格式，Shell 會根據內容執行預設動作。 比方說，如果使用者從某個磁片區拖曳檔案，然後將它放在另一個磁片區上，則 Shell 的預設動作是複製檔案。 藉由在資料物件中包含 CFSTR_PREFERREDDROPFORMAT 格式，您可以覆寫預設動作，並明確地指示 Shell 複製、移動或連結檔案。 如果使用者選擇使用右邊的按鈕拖曳，CFSTR_PREFERREDDROPFORMAT 會在 [拖放](context-menu-handlers.md) 快捷方式功能表上指定預設命令。 使用者仍然可以自由選擇功能表上的其他命令。

在 Microsoft Internet Explorer 4.0 之前，應用程式會藉由在 [**FILEDESCRIPTOR**](/windows/win32/api/shlobj_core/ns-shlobj_core-filedescriptora)結構的 **dwFlags** 成員中設定 FD_LINKUI，來指出它正在傳送快捷方式檔案類型。 目標接著必須使用可能耗時的 [**IDataObject：：**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) 呼叫，以找出是否已設定 FD_LINKUI 旗標。 現在，要用來表示快速鍵的慣用方式是使用設定為 DROPEFFECT_LINK 的 CFSTR_PREFERREDDROPEFFECT 格式。 不過，為了與舊版系統回溯相容，來源仍應設定 FD_LINKUI 旗標。

### <a name="cfstr_targetclsid"></a>CFSTR_TARGETCLSID

目標會使用此格式識別碼，將其 CLSID 提供給來源。 資料是包含全域記憶體物件的 [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) 結構。 結構的 **hGlobal** 成員指向放置目標的 CLSID GUID。

此格式主要用於將物件拖曳至資源回收筒，以允許將物件刪除。 在資源回收筒中卸載物件時，會呼叫來源的 [**IDataObject：： SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) 方法，並將 CFSTR_TARGETCLSID 格式設定為資源回收筒的 CLSID (CLSID_RecycleBin) 。 然後，來源可以刪除原始物件。

### <a name="cfstr_untrusteddragdrop"></a>CFSTR_UNTRUSTEDDRAGDROP

Windows Internet Explorer 和 Windows Shell 會使用此格式識別碼，以提供一種機制，用來封鎖或提示源自 Internet Explorer 的拖放作業，以及 [**URLACTION_SHELL_ENHANCED_DRAGDROP_SECURITY**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537178(v=vs.85)) 旗標。

**CFSTR_UNTRUSTEDDRAGDROP** 是由拖放作業的來源加入，以指定資料物件可能包含不信任的資料。 資料是由包含全域記憶體物件的 [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) 結構所表示。 結構的 **hGlobal** 成員會指向一個 **DWORD** 設定為適當的 [**URL 動作**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537178(v=vs.85))旗標，以使用 [**PUAF_ENFORCERESTRICTED**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537171(v=vs.85))旗標，透過 [**IInternetSecurityManager：:P rocessurlaction**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537136(v=vs.85))方法來檢查原則。

### <a name="dragwindow"></a>DragWindow

這種格式會在拖放作業中用來識別物件的拖曳影像 (視窗) ，讓其視覺效果資訊可以動態更新。 將物件拖曳至放置目標上時，應用程式會更新其 [**DROPDESCRIPTION**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription) 結構，以回應 [**IDropTarget：:D ragover**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) 或 [**IDropSource：： system.windows.dragdrop.givefeedback>**](/windows/win32/api/oleidl/nf-oleidl-idropsource-givefeedback) 方法。 **DROPDESCRIPTION** 會更新為新的 [**DROPIMAGETYPE**](/windows/desktop/api/shlobj_core/ne-shlobj_core-dropimagetype)值，指出要套用至拖曳視窗視覺效果的裝飾;例如，指出檔案正在複製而不是移動，或物件無法卸載至該位置。 不過，在物件收到 [**DDWM_UPDATEWINDOW**](ddwm-updatewindow.md) 訊息之前，不會更新視覺效果。 此格式會將收件者拖曳視窗的 **HWND** 提供給 **DDWM_UPDATEWINDOW** 訊息的傳送者。

剪貼簿資料的類型 [**TYMED_HGLOBAL**](/windows/win32/api/objidl/ne-objidl-tymed)。 它是 **HWND** 的 **DWORD** 標記法。 資料可以傳遞至 **ULongToHandle** 函數（定義于 Basetsd 中），以提供要在64位 Windows 上使用的64位 **HWND** 。

此格式不需要包含 Shlobj.h。

 

 
