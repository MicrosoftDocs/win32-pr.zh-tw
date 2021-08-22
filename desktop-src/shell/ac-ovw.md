---
description: 自動完成會將已部分在編輯控制項中輸入的字串展開為完整字串。
title: 使用自動完成
ms.topic: article
ms.date: 05/31/2018
ms.assetid: b990395b-fc10-48f9-a718-7cc006e37eb7
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 822f2554f51adfb99b1b4b2ad9d61fe064f802def3c8804371639ec20563b54b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119223708"
---
# <a name="using-autocomplete"></a>使用自動完成

自動完成會將已部分在 [編輯控制項](/windows/desktop/Controls/edit-controls) 中輸入的字串展開為完整字串。 例如，當使用者開始在 [Windows Internet Explorer] 工具列中內嵌的 [位址] 編輯控制項中輸入 URL 時，自動完成功能會將字串展開為一或多個與現有部分字串一致的完整 URL 選項。 部分 URL 字串（例如 "mic"）可能會展開為 " https://www.microsoft.com " 或 " https://www.microsoft.com/windows "。 自動完成通常會搭配編輯控制項或具有內嵌編輯控制項的控制項（例如 [ComboBoxEx](/windows/desktop/Controls/comboboxex-control-reference) 控制項）使用。

## <a name="adding-autocomplete-functionality-to-your-application"></a>將自動完成功能新增至您的應用程式

應用程式可以透過兩種方式，將自動完成功能新增至編輯控制項：

-   [**SHAutoComplete**](/windows/desktop/api/shlwapi/nf-shlwapi-shautocomplete) 是簡單的函式，可自動完成檔案路徑或 URL。
-   [**IAutoComplete**](/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete) 介面是由 (CLSID 自動完成) 的自動完成物件所公開 \_ 。 它可讓應用程式初始化、啟用和停用物件。 **IAutoComplete** 可讓您更充分掌控自動完成來源，包括新增自訂來源的能力。 本主題的其餘部分將討論 **IAutoComplete** 的使用。 請參閱如何針對特定使用範例 [手動啟用自動完成](how-to-enable-autocomplete-manually.md) 。

## <a name="autocomplete-modes"></a>自動完成模式

使用 [**IAutoComplete**](/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete)時，自動完成可以用兩種模式顯示完成的字串： autoappend 和自動建議。 模式是獨立的;您可以啟用其中一項或兩者。 若要指定模式，請呼叫 [**IAutoComplete2：： >setoptions**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete2-setoptions)。

<dl> <dt>

<span id="Autoappend"></span><span id="autoappend"></span><span id="AUTOAPPEND"></span>Autoappend
</dt> <dd>

在 autoappend 模式中，自動完成會將最有可能候選字串的其餘部分附加至現有的字元，並反白顯示附加的字元。 如果使用者繼續輸入字元，則會將它們加入至現有的部分字串。 如果使用者新增的字元與下一個反白顯示的字元相同，則會關閉該字元的反白顯示。 其餘的字元仍會反白顯示。 如果使用者新增的字元不符合下一個反白顯示的字元，自動完成功能便會嘗試根據較大的部分字串來產生新的候選字串，並將新候選字串的其餘部分附加至目前的部分字串。 如果找不到候選字串，則只有具類型的字元會出現，而且編輯方塊的行為會如同沒有自動完成。 此程式會繼續進行，直到使用者接受字串為止。

</dd> <dt>

<span id="Autosuggest"></span><span id="autosuggest"></span><span id="AUTOSUGGEST"></span>自動建議
</dt> <dd>

在自動建議模式中，自動完成會在編輯控制項下方顯示下拉式清單，其中包含一或多個建議的完整字串。 使用者可以選取其中一個建議的字串，或繼續鍵入。 當輸入進展時，可能會根據目前的部分字串來修改下拉式清單。 如果您 \_ 在 [**IAutoComplete2：： >setoptions**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete2-setoptions)中設定 ACO 搜尋旗標，[自動完成] 會在下拉式清單底部提供選項，以搜尋目前的部分字串。 即使沒有任何建議的字串，仍會顯示此選項。 如果使用者選取搜尋選項，您的應用程式應該會啟動搜尋引擎來協助使用者。

</dd> </dl>

## <a name="using-predefined-autocomplete-sources"></a>使用預先定義的自動完成來源

自動完成取決於有提供字串的來源，以符合使用者的部分字串。 您可以選擇提供自訂的自動完成來源，但是有幾個最常見的來源是由系統所提供。

<dl> <dt>

<span id="CLSID_ACLHistory"></span><span id="clsid_aclhistory"></span><span id="CLSID_ACLHISTORY"></span>CLSID \_ ACLHistory
</dt> <dd>

符合使用者歷程記錄清單中 URL 清單的自動完成來源。

</dd> <dt>

<span id="CLSID_ACLMRU"></span><span id="clsid_aclmru"></span>CLSID \_ ACLMRU
</dt> <dd>

符合使用者最近使用清單中 URL 清單的自動完成來源。

</dd> <dt>

<span id="CLSID_ACListISF"></span><span id="clsid_aclistisf"></span><span id="CLSID_ACLISTISF"></span>CLSID \_ ACListISF
</dt> <dd>

符合 Shell 命名空間中專案的自動完成來源：使用者電腦上的檔案，以及虛擬資料夾中的專案（例如主控台）。

</dd> </dl>

在某些情況下，您可能會想要保留與自動完成相關之各種物件的介面指標，而不是立即釋放資源。 尤其是當您想要動態調整自動完成行為時，會執行這項操作。 當使用 CLSID ACListISF 物件（從 Shell 命名空間自動完成）時，會發生這種情況最常見的實例 \_ ，而且也可以從目前目錄列舉的選項 ([**ACLO \_ CURRENTDIR**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist2)) 。 例如，當您流覽至新的資料夾時，Internet Explorer 會變更位址列的目前的目錄，因此必須動態變更這些設定。 有兩種方式可指定 CLSID \_ ACListISF 物件應視為目前目錄的目錄：

-   [**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) 會透過 [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist)指定目錄。
-   [**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory) 會透過路徑字串指定目錄。

在下列情況下，假設 **pal** 是 CLSID ACListISF 物件之 [**IACList**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist) 介面的指標 \_ ：

-   使用 [**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder)：

    若要告訴 CLSID \_ ACListISF 物件應將特定 [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) 視為目前的目錄，您可以使用物件的 [**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) 介面。 因為 **ITEMIDLIST** 可參考虛擬資料夾，所以這個方法比使用 [**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory)更有彈性。

    請注意，下列範例會使用範本化 QueryInterface，以允許簡化的參數清單。

    ```C++
    IPersistFolder *ppf;

    hr = pal2->QueryInterface(IID_PPV_ARGS(&ppf));   
    if (SUCCEEDED(hr))
    {
        hr = ppf->Initialize(pidlCurrentDirectory);
        ppf->Release();
    }
    ```

    

-   使用 [**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory)：

    若要為 CLSID \_ ACListISF 物件提供目前的目錄的路徑，您可以使用物件的 [**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory) 介面。

    ```C++
    WCHAR pwszDirectory[MAX_PATH] = L"C:\\Program Files";
    ICurrentWorkingDirectory *pcwd;

    hr = pal2->QueryInterface(IID_PPV_ARGS(&pcwd));    
    if (SUCCEEDED(hr))
    {
        hr = pcwd->SetDirectory(pwszDirectory);
        pcwd->Release();
    }
    ```

    

 

 
