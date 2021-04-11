---
description: 在 Windows Vista 中，Tablet PC 輸入面板整合了新的自動完成功能，可讓應用程式的自動完成清單在輸入面板中辨識出使用者的筆墨時即時更新。
ms.assetid: 0f01f546-f76b-4c61-a204-2a06079a374a
title: 使用輸入面板自動完成
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c9e7f108631eb2723b71bf8ed919c17a0eabff5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112877"
---
# <a name="using-input-panel-autocomplete"></a>使用輸入面板自動完成

在 Windows Vista 中，Tablet PC 輸入面板整合了新的自動完成功能，可讓應用程式的自動完成清單在輸入面板中辨識出使用者的筆墨時即時更新。 此外，應用程式的自動完成清單會定位於輸入面板使用者方便使用的位置。 若沒有輸入面板自動完成功能，在輸入面板中使用自動完成功能是很困難的程式，要求使用者一次插入一個字元，並移動輸入面板以存取自動完成建議。 透過整合，自動完成功能是一項功能強大的工具，可讓 Tablet PC 使用者使用輸入面板加速並提高輸入文字的便利性。

![具有 ie 自動完成清單的輸入面板](images/9e769482-543a-4e29-b274-8f19ae10250d.jpg)

有三個選項可讓應用程式利用輸入面板自動完成整合。 包含使用 Shell 自動完成功能建立的自動完成功能的應用程式 (透過 [**IAutoComplete**](/windows/win32/api/shldisp/nn-shldisp-iautocomplete) 介面) 或透過 [autocompletemode.none](/dotnet/api/system.windows.forms.autocompletemode?view=netcore-3.1)) 列舉來 .NET Framework 自動完成 (，而不需要變更程式碼。 包含自訂自動完成文字欄位的應用程式可以使用輸入面板自動完成 API 來取得相同的功能。

在所有情況下，您都可以對應用程式的自動完成清單進行這些修改，而不需要複製或修改應用程式用來產生自動完成清單的 UI 或預測邏輯。 自動完成清單會繼續是應用程式所繪製的擁有者，而自動完成清單的內容則與直接輸入編輯欄位中的文字一樣。

Windows Vista 作業系統或更新版本支援輸入面板自動完成整合。 從 Windows Vista 開始，輸入面板自動完成整合內建于 Shell 自動完成整合，並從 .NET Framework 3.0 版開始 Windows Forms 開發。 雖然 [**IAutoComplete**](/windows/win32/api/shldisp/nn-shldisp-iautocomplete) 和 [autocompletemode.none](/dotnet/api/system.windows.forms.autocompletemode?view=netcore-3.1) 都是在舊版 Windows 上執行，但 MICROSOFT Windows XP Tablet PC Edition 或舊版作業系統不支援輸入面板自動完成整合。 如果您在舊版 Tablet PC 上執行輸入面板自動完成功能，應用程式會還原為預先整合的行為。

## <a name="reasons-to-integrate-application-autocomplete-lists-with-input-panel"></a>整合應用程式自動完成清單與輸入面板的原因

整合應用程式的自動完成清單，可讓使用者輸入文字欄位中包含自動完成功能的最大程度和速度。 此外，包含輸入面板自動完成整合的應用程式會立即看起來像是以 Tablet PC 進行開發，讓應用程式更吸引 Tablet PC 使用者使用。

### <a name="how-input-panel-and-autocomplete-list-interact-without-integration"></a>輸入面板和自動完成清單如何在沒有整合的情況下互動

使用 [輸入面板]，將文字輸入包含自動完成清單但未與 [輸入面板] 整合的文字欄位中：

1.  使用者將焦點放在文字欄位中，並開啟輸入面板。
2.  使用者寫入一或兩個字元。
3.  使用者請按 [ **插入**]。 輸入面板會將文字輸入應用程式的文字欄位。 應用程式的自動完成清單隨即出現，而且最可能部分或完全隱藏于輸入面板。
4.  使用者可以拖曳輸入面板，以找出應用程式的自動完成清單。
5.  假設自動完成清單中包含正確的專案，使用者現在可以選取該專案;否則，使用者必須重複步驟2和3。

這顯然是很麻煩的過程。 使用者對於自動完成清單應如何運作的期望是虛線，而且其執行工作的能力也會受到影響。

### <a name="how-input-panel-and-autocomplete-list-interaction-improves-with-integration"></a>輸入面板和自動完成清單互動如何透過整合來改善

使用 [輸入面板]，在文字欄位中輸入文字，其中包含與輸入面板整合的自動完成清單：

1.  使用者將焦點放在文字欄位中，並開啟輸入面板。
2.  使用者寫入一或兩個字元。 當使用者寫入文字時，應用程式的自動完成清單會直接出現在輸入面板的上方或正下方。
3.  使用者從自動完成清單中選取專案;專案會直接插入應用程式的文字欄位中，或使用者重複步驟2，直到正確的專案出現為止。

由於整合的緣故，當使用者在 [輸入面板] 中寫入時，自動完成清單隨即出現並更新。 此外，此清單已定位，讓使用者在輸入面板中書寫時可以輕鬆存取，而不會遮蔽。 最後，當使用者從自動完成清單中選取專案時，會直接將專案插入應用程式的文字輸入欄位，因此可讓使用者略過從輸入面板插入文字的步驟。

![具有 outlook express 自動完成清單的輸入面板](images/ba59a513-e538-4092-89a6-6d691424dc3d.jpg)

## <a name="standard-autocomplete-components-that-include-input-panel-autocomplete-integration"></a>包含輸入面板自動完成整合的標準自動完成元件

[**IAutoComplete**](/windows/win32/api/shldisp/nn-shldisp-iautocomplete)和 [Autocompletemode.none](/dotnet/api/system.windows.forms.autocompletemode?view=netcore-3.1)都包含輸入面板自動完成的內建整合。 使用其中一種標準自動完成元件的應用程式，可以利用輸入面板的自動完成功能，幾乎不需要額外的工作。 此外，雖然只有在 Windows Vista 或新版的 Windows 作業系統上才支援輸入面板自動完成，但在 windows vista 發行之前使用 **IAutoComplete** 建立的應用程式會在 windows vista 上執行時，自動取得輸入面板自動完成整合。 下列各節包含特定 **IAutoComplete** 的詳細資訊，以及包含輸入面板自動完成整合的 autocompletemode.none 元素。

### <a name="shell-autocomplete-with-input-panel-autocomplete-integration"></a>使用輸入面板自動完成整合的 Shell 自動完成整合

使用 [**IAutoComplete**](/windows/win32/api/shldisp/nn-shldisp-iautocomplete) 的應用程式可免費取得輸入面板自動完成整合。 雖然 Shell 自動完成 Api 包含在 Windows 2000 中，但輸入面板自動完成整合只支援 Windows Vista 和更新版本。 不過，在 windows Vista 發行之前建立且使用 **IAutoComplete** 的應用程式，在 windows vista 上執行時，會自動取得輸入面板自動完成整合。

為了利用這種方式來利用 Tablet 自動完成功能，您必須使用 [自動完成] 物件 (**CLSID \_ 自動完成**) 。 如果您想要提供 Url 或檔案名的自動完成功能，請使用 [**SHAutoComplete**](/windows/win32/api/shlwapi/nf-shlwapi-shautocomplete) 函式來建立自動完成物件。

除了 [**IAutoComplete**](/windows/win32/api/shldisp/nn-shldisp-iautocomplete)之外，您還可以直接執行 [**IAutoComplete2**](/windows/win32/api/shldisp/nn-shldisp-iautocomplete2) 或 [**IAutoCompleteDropDown**](/windows/win32/api/shobjidl/nn-shobjidl-iautocompletedropdown)，而且仍會自動取得輸入面板自動完成整合。

### <a name="input-panel-autocomplete-integration-with-net-framework-applications"></a>輸入面板自動完成與 .NET Framework 應用程式的整合

從 .NET Framework 3.0 開始，Windows Forms 文字方塊包含自動完成。 Windows Forms textbox 自動完成建立在 Shell 自動完成之上，也就是內建的輸入面板自動完成整合。 在 Windows Vista 之前發行的 Windows 版本上，支援的 .NET Framework 3.0 層級。 不過，因為只有在 Windows Vista 或更新版本上才支援輸入面板自動完成整合，所以輸入面板自動完成整合只適用于在 Windows Vista 或更新版本上安裝的 .NET Framework 3.0 應用程式。

希望利用 .NET Framework 3.0 中輸入面板自動完成整合的應用程式，必須使用已啟用[autocompletemode.none](/dotnet/api/system.windows.forms.textbox.autocompletemode?view=netcore-3.1)屬性的 Windows Forms [TextBox](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) 。 您不需要執行任何額外的工作，就能讓 Windows Forms 自動完成工作，以利用輸入面板自動完成整合。

## <a name="using-input-panel-autocomplete-apis-directly"></a>直接使用輸入面板自動完成 Api

自訂自動完成文字方塊的開發人員必須直接使用輸入面板自動完成 Api，才能獲得改進的文字輸入經驗，讓輸入面板自動完成整合可在其應用程式中啟用。 輸入面板自動完成 Api 隨附于 Windows Vista 作業系統中，屬於平板電腦平臺 SDK 1.9 版或更新版本。 輸入面板自動完成介面是以 COM 為基礎的介面。

下一節將詳細說明如何針對 c + + 應用程式使用這些介面。 不過，您可以 \# 透過使用 Com Interop，以大部分的語言（包括 C）來執行這些 COM 介面。

為了在自訂自動完成文字方塊中執行輸入面板自動完成整合，這兩個必要的介面是 [**ITipAutocompleteProvider 介面**](itipautocompleteprovider.md) 和 [**ITipAutocompleteClient 介面**](itipautocompleteclient.md)。 這些介面的定義可在 TipAutoComplete 和 TipAutoComplete i.c. 中找到。 \_

首先，應用程式必須定義並具現化自動完成提供者類別，其會針對每個包含自動完成清單的文字輸入欄位來執行 [**ITipAutocompleteProvider**](itipautocompleteprovider.md) 。 此類別會管理自動完成整合的應用程式端。 輸入面板的所有自動完成要求都會透過應用程式的自動完成提供者，從自動完成用戶端傳送至應用程式。 應用程式的自動完成提供者必須能夠存取應用程式自動完成清單的 HWND，以及相關聯文字輸入欄位的 HWIND。 此外，您必須執行下列 **ITipAutocompleteProvider** 方法：

-   [**ITipAutocompleteProvider：： UpdatePendingText 方法**](itipautocompleteprovider-updatependingtext.md)：此方法是由自動完成用戶端用來通知應用程式使用者已寫入輸入面板中的文字。 收到此通知時，提供者會負責產生自動完成清單，如同文字已輸入到應用程式的文字輸入欄位一樣。 透過 **ITipAutocompleteProvider：： UpdatePendingText 方法** 傳遞給自動完成提供者的字串，只包含目前在輸入面板中的文字。 因此，如果文字輸入欄位中有其他文字，則提供者必須負責正確地將它附加至用戶端傳送的文字。 **ITipAutocompleteProvider：： UpdatePendingText 方法** 的字串傳遞應視為欄位中目前選取範圍的取代專案。 如果目前沒有選取範圍，則應放置在目前插入點的位置。 一旦產生自動完成清單之後，提供者應該呼叫 [**ITipAutocompleteProvider：： Show 方法**](itipautocompleteprovider-show.md) 傳入 **TRUE** ，以顯示自動完成清單。 應用程式不應該快取對 **UpdatePendingText** 的呼叫，而是會將對 **UpdatePendingText** 的每個額外呼叫視為取消先前的呼叫，以避免在過期的自動完成清單 UI 中閃爍。下列範例程式碼說明這些作法。

    ```C++
    HRESULT SampleProvider::UpdatePendingText(BSTR bstrPendingText)
    {
       //Discard previously cached pending text from Input Panel
       m_bstrPending.Empty();
        //Store the new pending text from Input Panel as m_bstrPending
    m_bstrPending = bstrPendingText;

        //Get the text from the field in two chunks. The characters to
    //the left of the selection and the characters to the right.
    CComBSTR bstrLeftContext = //Text to the left of the selection
            CComBSTR bstrRightContext = //Text to the right of the selection

    //Discard previously cached complete text
        m_bstrCompleteText.Empty();
        //Append to the field text from the left of the selection
        //the text from Input Panel and then append to that
        //the field text to the right of the selection
        m_bstrCompleteText.Append(bstrLeftContext);
        m_bstrCompleteText.Append(m_bstrPending);
        m_bstrCompleteText.Append(bstrRigtContext);

        //Update the app's AC list based on m_bstrCompleteText
        //...

        //Show the updated AC list by calling the provider's Show method
       Show(true);
       return S_OK;
    }
    ```

    

-   [**ITipAutocompleteProvider：： Show 方法**](itipautocompleteprovider-show.md)：會從 [**UpdatePendingText**](itipautocompleteprovider-updatependingtext.md)呼叫這個方法，但也可以隨時由自動完成用戶端呼叫。 收到此呼叫時，自動完成提供者必須隱藏或顯示自動完成提供者（如參數所指示）。 在顯示自動完成清單之前，「自動完成提供者」應該會向「自動完成」用戶端諮詢自動完成清單的位置。 本文稍後會顯示有關放置自動完成清單的詳細資訊。

接下來，應用程式應該使用 Active Template Library (ATL) [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 函式來產生 [**ITipAutocompleteClient 介面**](itipautocompleteclient.md) 的實例，並以類別 **識別碼 \_ CLSID TipAutoCompleteClient** 作為同進程伺服器，然後向用戶端註冊該提供者。 自動完成用戶端 [**ITipAutocompleteClient：： AdviseProvider 方法**](itipautocompleteclient-adviseprovider.md) 會向用戶端註冊提供者，以讓用戶端呼叫應用程式的自動完成提供者物件。 如果系統上沒有 tiptsf.dll， **CoCreateInstance** 函數會失敗，並傳回 **REGDB \_ E \_ CLASSNOTREG**。 此時，應用程式可以捨棄其 [**ITipAutocompleteProvider**](itipautocompleteprovider.md) 物件，並繼續進行，因為輸入面板不存在，因為它不在這類系統上。

應用程式可以選擇建立一個 [**ITipAutocompleteClient**](itipautocompleteclient.md) 的實例，或每個文字欄位一個實例。 第一個選項會要求在每次焦點變更時，將提供者註冊並註冊。 本主題稍後會顯示有關取消註冊自動完成提供者的詳細資訊。

有幾個步驟牽涉到自動完成清單的定位，必須協調自動完成提供者 (應用程式) 和自動完成用戶端 (輸入面板) 。 在顯示自動完成清單之前（因為呼叫自動完成提供者的 [**Show**](itipautocompleteprovider-show.md) 方法或由於使用者使用鍵盤輸入文字的緣故），需要提供者洽詢用戶端，以瞭解要將自動完成清單放置於哪裡。 提供者應該採取下列步驟：

-   使用自動完成用戶端的 [**ITipAutocompleteClient：： RequestShowUI 方法**](itipautocompleteclient-requestshowui.md) ，來判斷輸入面板是否已準備好顯示自動完成清單。 **RequestShowUI** 會採用 *hwnd* 參數，也就是自動完成清單視窗的 hwnd，方法會傳回 **TRUE** 或 **FALSE** ，指出它是否為可顯示自動完成清單的狀態。 如果用戶端傳回 **FALSE**，則提供者不應嘗試顯示自動完成清單。
-   呼叫 [**RequestShowUI**](itipautocompleteclient-requestshowui.md) 來設定快顯自動完成清單視窗控制碼，然後再呼叫 [**ITipAutocompleteClient：:P referredrects 方法**](itipautocompleteclient-preferredrects.md)。 若未這麼做，將會在呼叫 **PreferredRects** 時造成 **E \_ INVALIDARG** 錯誤。
-   如果 [**RequestShowUI**](itipautocompleteclient-requestshowui.md) 傳回 **TRUE**，則提供者應該根據文字輸入欄位的位置來計算自動完成清單的預設螢幕座標矩形，然後呼叫自動完成用戶端的 [**ITipAutocompleteClient：:P referredrects 方法**](itipautocompleteclient-preferredrects.md)。 這可讓自動完成用戶端調整矩形，以避免自動完成清單與輸入面板重迭。 **PreferredRects** 方法會採用四個參數：

    -   RECT *rcACList*：自動完成清單的預設螢幕座標矩形。
    -   RECT *rcField*：對應文字輸入欄位的螢幕座標矩形。
    -   矩形 *\* PrcModifiedACList*：自動完成的已調整螢幕座標矩形
    -   BOOL *\* pfShowAbove*：此參數會向提供者指出 *PrcModifiedACList* 矩形是否將自動完成清單放置於輸入面板上方或下方。 應用程式可以使用這項資訊，正確地繪製 UI 專案，例如調整大小控點和捲軸。 提供者一開始應該會以 *rcACList* 的相對於文字輸入欄位的順序來傳遞自動完成清單的方向。 如果用戶端設定 *prcModifiedACList* 等於 *rcACList*，則不會變更 *pfShowAbove* 。

    使用 *prcModifiedACList* 和 *pfShowAbove* out 引數的傳回值，以定位並顯示 [自動完成清單] 視窗。 如果輸入面板不在使用中， [**RequestShowUI**](itipautocompleteclient-requestshowui.md) 一律會傳回 **TRUE** ，而且 *prcModifiedACList* 一律會與 *rcACList* 相同。 *pfShowAbove* 也不會變更，因此呼叫不會影響應用程式行為。 下列範例程式碼說明這些作法。


```C++
HRESULT SampleProvider::Show(BOOL fShow)
{
    //Ask the AC client if it is OK to show the Autocomplete list.
    BOOL fAllowShowing = FALSE;
    m_spACClient->RequestShowUI(m_hWndList, &fAllowShowing);

    if (fShow && fAllowingShowing)
        {
            // Create the parameters required to call PreferredRects
            RECT rcField = //Rectangle for app's text field
            RECT rcACList = //Default rectangle for app's AC list
            RECT rcModifiedACList = {0, 0, 0, 0};
            BOOL fShowAbove = TRUE;

//Ask the AC client to modify the position of the AC list
m_spACClient->PreferredRects(&rcACList, &rcField,
&rcModifiedACList, &fShowAbove);

            //Show the Autocomplete UI at the modified preferred rectangle
            //from rcModifiedACList and the directional info provide by
//fShowAbove
            //...
        }
    else
        {
        //Hide the Autocomplete list and clean up
        //...
        }
    return S_OK;
}
```



當使用者在自動完成清單中選取專案時，除了將選取的專案文字插入文字輸入欄位之外，提供者還需要呼叫用戶端的 [**ITipAutocompleteClient：： UserSelection 方法**](itipautocompleteclient-userselection.md) 。 輸入面板會使用此通知來捨棄尚未從 [輸入面板] 插入的所有剩餘文字。

最後，當不再需要提供者時，應呼叫自動完成用戶端的 [**ITipAutocompleteClient：： UnadviseProvider 方法**](itipautocompleteclient-unadviseprovider.md) ，取消註冊提供者，以取消與自動完成用戶端的連結。 提供者可能會因為下列兩個原因之一而取消註冊：因為提供者相關聯的文字輸入欄位已終結，或因為應用程式選擇只建立一個自動完成用戶端，而不是每個文字輸入欄位一個。 在此情況下，每次焦點從文字欄位切換時，都必須取消註冊提供者。

## <a name="conclusion"></a>結論

輸入面板自動完成整合是一項功能強大的工具，可改善在 Tablet Pc 上包含自動完成清單的 Windows 應用程式使用者體驗。 如果沒有整合，輸入面板使用者必須經過繁瑣的程式，一次插入一個字元，然後重新置放輸入面板，才能使用自動完成。 透過整合，自動完成清單會以使用者筆跡的形式出現在 [輸入面板] 的方便位置，同時增加速度和文字輸入的便利性。 在包含以 Shell 自動完成或 .NET Framework 3.0 自動完成功能為基礎的自動完成功能的應用程式中，輸入面板自動完成整合是一項免費且吸引人的功能。 此外，也提供一組簡單的 COM 型介面，以針對選擇使用自訂自動完成控制項的應用程式啟用相同的整合式體驗。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[文字輸入面板參考](text-input-panel-reference.md)
</dt> </dl>

 

 
