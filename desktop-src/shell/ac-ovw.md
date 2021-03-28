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
ms.openlocfilehash: fbbf0c53fc1b26002d1b46a9a6a6f67cd15e3ead
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972084"
---
# <a name="using-autocomplete"></a><span data-ttu-id="d87f2-103">使用自動完成</span><span class="sxs-lookup"><span data-stu-id="d87f2-103">Using Autocomplete</span></span>

<span data-ttu-id="d87f2-104">自動完成會將已部分在 [編輯控制項](/windows/desktop/Controls/edit-controls) 中輸入的字串展開為完整字串。</span><span class="sxs-lookup"><span data-stu-id="d87f2-104">Autocompletion expands strings that have been partially entered in an [edit control](/windows/desktop/Controls/edit-controls) into complete strings.</span></span> <span data-ttu-id="d87f2-105">例如，當使用者開始在 [Windows Internet Explorer] 工具列中內嵌的 [位址] 編輯控制項中輸入 URL 時，自動完成功能會將字串展開為一或多個與現有部分字串一致的完整 URL 選項。</span><span class="sxs-lookup"><span data-stu-id="d87f2-105">For example, when a user starts to enter a URL in the Address edit control that is embedded in the Windows Internet Explorer toolbar, autocompletion expands the string into one or more complete URL options that are consistent with the existing partial string.</span></span> <span data-ttu-id="d87f2-106">部分 URL 字串（例如 "mic"）可能會展開為 " https://www.microsoft.com " 或 " https://www.microsoft.com/windows "。</span><span class="sxs-lookup"><span data-stu-id="d87f2-106">A partial URL string such as "mic" might be expanded to "https://www.microsoft.com" or "https://www.microsoft.com/windows".</span></span> <span data-ttu-id="d87f2-107">自動完成通常會搭配編輯控制項或具有內嵌編輯控制項的控制項（例如 [ComboBoxEx](/windows/desktop/Controls/comboboxex-control-reference) 控制項）使用。</span><span class="sxs-lookup"><span data-stu-id="d87f2-107">Autocompletion is typically used with edit controls or with controls that have an embedded edit control, such as the [ComboBoxEx](/windows/desktop/Controls/comboboxex-control-reference) control.</span></span>

## <a name="adding-autocomplete-functionality-to-your-application"></a><span data-ttu-id="d87f2-108">將自動完成功能新增至您的應用程式</span><span class="sxs-lookup"><span data-stu-id="d87f2-108">Adding Autocomplete Functionality to Your Application</span></span>

<span data-ttu-id="d87f2-109">應用程式可以透過兩種方式，將自動完成功能新增至編輯控制項：</span><span class="sxs-lookup"><span data-stu-id="d87f2-109">An application can add autocomplete functionality to an edit control in two ways:</span></span>

-   <span data-ttu-id="d87f2-110">[**SHAutoComplete**](/windows/desktop/api/shlwapi/nf-shlwapi-shautocomplete) 是簡單的函式，可自動完成檔案路徑或 URL。</span><span class="sxs-lookup"><span data-stu-id="d87f2-110">[**SHAutoComplete**](/windows/desktop/api/shlwapi/nf-shlwapi-shautocomplete) is a simple function that can autocomplete a file path or URL.</span></span>
-   <span data-ttu-id="d87f2-111">[**IAutoComplete**](/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete) 介面是由 (CLSID 自動完成) 的自動完成物件所公開 \_ 。</span><span class="sxs-lookup"><span data-stu-id="d87f2-111">[**IAutoComplete**](/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete) interface is exposed by the autocomplete object (CLSID\_AutoComplete).</span></span> <span data-ttu-id="d87f2-112">它可讓應用程式初始化、啟用和停用物件。</span><span class="sxs-lookup"><span data-stu-id="d87f2-112">It allows applications to initialize, enable, and disable the object.</span></span> <span data-ttu-id="d87f2-113">**IAutoComplete** 可讓您更充分掌控自動完成來源，包括新增自訂來源的能力。</span><span class="sxs-lookup"><span data-stu-id="d87f2-113">**IAutoComplete** allows more control over autocomplete sources, including the ability to add a custom source.</span></span> <span data-ttu-id="d87f2-114">本主題的其餘部分將討論 **IAutoComplete** 的使用。</span><span class="sxs-lookup"><span data-stu-id="d87f2-114">The remainder of this topic discusses the use of **IAutoComplete**.</span></span> <span data-ttu-id="d87f2-115">請參閱如何針對特定使用範例 [手動啟用自動完成](how-to-enable-autocomplete-manually.md) 。</span><span class="sxs-lookup"><span data-stu-id="d87f2-115">See [How To Enable Autocomplete Manually](how-to-enable-autocomplete-manually.md) for specific usage examples.</span></span>

## <a name="autocomplete-modes"></a><span data-ttu-id="d87f2-116">自動完成模式</span><span class="sxs-lookup"><span data-stu-id="d87f2-116">Autocomplete Modes</span></span>

<span data-ttu-id="d87f2-117">使用 [**IAutoComplete**](/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete)時，自動完成可以用兩種模式顯示完成的字串： autoappend 和自動建議。</span><span class="sxs-lookup"><span data-stu-id="d87f2-117">When using [**IAutoComplete**](/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete), autocompletion can display the completed string in two modes: autoappend and autosuggest.</span></span> <span data-ttu-id="d87f2-118">模式是獨立的;您可以啟用其中一項或兩者。</span><span class="sxs-lookup"><span data-stu-id="d87f2-118">The modes are independent; you can enable either or both.</span></span> <span data-ttu-id="d87f2-119">若要指定模式，請呼叫 [**IAutoComplete2：： >setoptions**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete2-setoptions)。</span><span class="sxs-lookup"><span data-stu-id="d87f2-119">To specify the mode, call [**IAutoComplete2::SetOptions**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete2-setoptions).</span></span>

<dl> <dt>

<span data-ttu-id="d87f2-120"><span id="Autoappend"></span><span id="autoappend"></span><span id="AUTOAPPEND"></span>Autoappend</span><span class="sxs-lookup"><span data-stu-id="d87f2-120"><span id="Autoappend"></span><span id="autoappend"></span><span id="AUTOAPPEND"></span>Autoappend</span></span>
</dt> <dd>

<span data-ttu-id="d87f2-121">在 autoappend 模式中，自動完成會將最有可能候選字串的其餘部分附加至現有的字元，並反白顯示附加的字元。</span><span class="sxs-lookup"><span data-stu-id="d87f2-121">In autoappend mode, autocompletion appends the remainder of the most likely candidate string to the existing characters, highlighting the appended characters.</span></span> <span data-ttu-id="d87f2-122">如果使用者繼續輸入字元，則會將它們加入至現有的部分字串。</span><span class="sxs-lookup"><span data-stu-id="d87f2-122">If the user continues to enter characters, they are added to the existing partial string.</span></span> <span data-ttu-id="d87f2-123">如果使用者新增的字元與下一個反白顯示的字元相同，則會關閉該字元的反白顯示。</span><span class="sxs-lookup"><span data-stu-id="d87f2-123">If the user adds a character that is identical to the next highlighted character, the highlighting for that character is turned off.</span></span> <span data-ttu-id="d87f2-124">其餘的字元仍會反白顯示。</span><span class="sxs-lookup"><span data-stu-id="d87f2-124">The remaining characters will still be highlighted.</span></span> <span data-ttu-id="d87f2-125">如果使用者新增的字元不符合下一個反白顯示的字元，自動完成功能便會嘗試根據較大的部分字串來產生新的候選字串，並將新候選字串的其餘部分附加至目前的部分字串。</span><span class="sxs-lookup"><span data-stu-id="d87f2-125">If the user adds a character that does not match the next highlighted character, autocompletion attempts to generate a new candidate string based on the larger partial string and appends the remainder of the new candidate string to the current partial string.</span></span> <span data-ttu-id="d87f2-126">如果找不到候選字串，則只有具類型的字元會出現，而且編輯方塊的行為會如同沒有自動完成。</span><span class="sxs-lookup"><span data-stu-id="d87f2-126">If no candidate string can be found, only the typed characters appear and the edit box behaves as it would without autocompletion.</span></span> <span data-ttu-id="d87f2-127">此程式會繼續進行，直到使用者接受字串為止。</span><span class="sxs-lookup"><span data-stu-id="d87f2-127">This process continues until the user accepts a string.</span></span>

</dd> <dt>

<span data-ttu-id="d87f2-128"><span id="Autosuggest"></span><span id="autosuggest"></span><span id="AUTOSUGGEST"></span>自動建議</span><span class="sxs-lookup"><span data-stu-id="d87f2-128"><span id="Autosuggest"></span><span id="autosuggest"></span><span id="AUTOSUGGEST"></span>Autosuggest</span></span>
</dt> <dd>

<span data-ttu-id="d87f2-129">在自動建議模式中，自動完成會在編輯控制項下方顯示下拉式清單，其中包含一或多個建議的完整字串。</span><span class="sxs-lookup"><span data-stu-id="d87f2-129">In autosuggest mode, autocompletion displays a drop-down list, with one or more suggested complete strings, beneath the edit control.</span></span> <span data-ttu-id="d87f2-130">使用者可以選取其中一個建議的字串，或繼續鍵入。</span><span class="sxs-lookup"><span data-stu-id="d87f2-130">The user can select one of the suggested strings or continue typing.</span></span> <span data-ttu-id="d87f2-131">當輸入進展時，可能會根據目前的部分字串來修改下拉式清單。</span><span class="sxs-lookup"><span data-stu-id="d87f2-131">As typing progresses, the drop-down list might be modified based on the current partial string.</span></span> <span data-ttu-id="d87f2-132">如果您 \_ 在 [**IAutoComplete2：： >setoptions**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete2-setoptions)中設定 ACO 搜尋旗標，[自動完成] 會在下拉式清單底部提供選項，以搜尋目前的部分字串。</span><span class="sxs-lookup"><span data-stu-id="d87f2-132">If you set the ACO\_SEARCH flag in [**IAutoComplete2::SetOptions**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete2-setoptions), autocomplete provides an option, at the bottom of the drop-down list, to search for the current partial string.</span></span> <span data-ttu-id="d87f2-133">即使沒有任何建議的字串，仍會顯示此選項。</span><span class="sxs-lookup"><span data-stu-id="d87f2-133">This option is displayed even if there are no suggested strings.</span></span> <span data-ttu-id="d87f2-134">如果使用者選取搜尋選項，您的應用程式應該會啟動搜尋引擎來協助使用者。</span><span class="sxs-lookup"><span data-stu-id="d87f2-134">If the user selects the search option, your application should launch a search engine to assist the user.</span></span>

</dd> </dl>

## <a name="using-predefined-autocomplete-sources"></a><span data-ttu-id="d87f2-135">使用預先定義的自動完成來源</span><span class="sxs-lookup"><span data-stu-id="d87f2-135">Using Predefined Autocomplete Sources</span></span>

<span data-ttu-id="d87f2-136">自動完成取決於有提供字串的來源，以符合使用者的部分字串。</span><span class="sxs-lookup"><span data-stu-id="d87f2-136">Autocompletion depends on having a source that provides it with strings to match against the user's partial string.</span></span> <span data-ttu-id="d87f2-137">您可以選擇提供自訂的自動完成來源，但是有幾個最常見的來源是由系統所提供。</span><span class="sxs-lookup"><span data-stu-id="d87f2-137">You have the option of providing a custom autocomplete source, but several of the most common sources are provided by the system.</span></span>

<dl> <dt>

<span data-ttu-id="d87f2-138"><span id="CLSID_ACLHistory"></span><span id="clsid_aclhistory"></span><span id="CLSID_ACLHISTORY"></span>CLSID \_ ACLHistory</span><span class="sxs-lookup"><span data-stu-id="d87f2-138"><span id="CLSID_ACLHistory"></span><span id="clsid_aclhistory"></span><span id="CLSID_ACLHISTORY"></span>CLSID\_ACLHistory</span></span>
</dt> <dd>

<span data-ttu-id="d87f2-139">符合使用者歷程記錄清單中 URL 清單的自動完成來源。</span><span class="sxs-lookup"><span data-stu-id="d87f2-139">An autocomplete source that matches against the URL list in the user's History list.</span></span>

</dd> <dt>

<span data-ttu-id="d87f2-140"><span id="CLSID_ACLMRU"></span><span id="clsid_aclmru"></span>CLSID \_ ACLMRU</span><span class="sxs-lookup"><span data-stu-id="d87f2-140"><span id="CLSID_ACLMRU"></span><span id="clsid_aclmru"></span>CLSID\_ACLMRU</span></span>
</dt> <dd>

<span data-ttu-id="d87f2-141">符合使用者最近使用清單中 URL 清單的自動完成來源。</span><span class="sxs-lookup"><span data-stu-id="d87f2-141">An autocomplete source that matches against the URL list in the user's Recently Used list.</span></span>

</dd> <dt>

<span data-ttu-id="d87f2-142"><span id="CLSID_ACListISF"></span><span id="clsid_aclistisf"></span><span id="CLSID_ACLISTISF"></span>CLSID \_ ACListISF</span><span class="sxs-lookup"><span data-stu-id="d87f2-142"><span id="CLSID_ACListISF"></span><span id="clsid_aclistisf"></span><span id="CLSID_ACLISTISF"></span>CLSID\_ACListISF</span></span>
</dt> <dd>

<span data-ttu-id="d87f2-143">符合 Shell 命名空間中專案的自動完成來源：使用者電腦上的檔案，以及虛擬資料夾中的專案（例如主控台）。</span><span class="sxs-lookup"><span data-stu-id="d87f2-143">An autocomplete source that matches against items in the Shell namespace: files on the user's computer as well as items in virtual folders such as Control Panel.</span></span>

</dd> </dl>

<span data-ttu-id="d87f2-144">在某些情況下，您可能會想要保留與自動完成相關之各種物件的介面指標，而不是立即釋放資源。</span><span class="sxs-lookup"><span data-stu-id="d87f2-144">There are occasions when, rather than immediately freeing the resources, you might want to retain the interface pointers to the various objects involved in autocomplete.</span></span> <span data-ttu-id="d87f2-145">尤其是當您想要動態調整自動完成行為時，會執行這項操作。</span><span class="sxs-lookup"><span data-stu-id="d87f2-145">In particular, this is done when you want to adjust the autocomplete behavior dynamically.</span></span> <span data-ttu-id="d87f2-146">當使用 CLSID ACListISF 物件（從 Shell 命名空間自動完成）時，會發生這種情況最常見的實例 \_ ，而且也可以從目前目錄列舉的選項 ([**ACLO \_ CURRENTDIR**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist2)) 。</span><span class="sxs-lookup"><span data-stu-id="d87f2-146">The most common instance of this occurs when using the CLSID\_ACListISF object, which autocompletes from the Shell namespace and has the option ([**ACLO\_CURRENTDIR**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist2)) of enumerating from the current directory as well.</span></span> <span data-ttu-id="d87f2-147">例如，當您流覽至新的資料夾時，Internet Explorer 會變更位址列的目前的目錄，因此必須動態變更這些設定。</span><span class="sxs-lookup"><span data-stu-id="d87f2-147">For example, when you navigate to a new folder, Internet Explorer changes the Address bar's current directory and therefore the settings need to be changed dynamically.</span></span> <span data-ttu-id="d87f2-148">有兩種方式可指定 CLSID \_ ACListISF 物件應視為目前目錄的目錄：</span><span class="sxs-lookup"><span data-stu-id="d87f2-148">There are two ways to specify the directory that the CLSID\_ACListISF object should treat as the current directory:</span></span>

-   <span data-ttu-id="d87f2-149">[**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) 會透過 [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist)指定目錄。</span><span class="sxs-lookup"><span data-stu-id="d87f2-149">[**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) specifies the directory through an [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist).</span></span>
-   <span data-ttu-id="d87f2-150">[**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory) 會透過路徑字串指定目錄。</span><span class="sxs-lookup"><span data-stu-id="d87f2-150">[**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory) specifies the directory through a path string.</span></span>

<span data-ttu-id="d87f2-151">在下列情況下，假設 **pal** 是 CLSID ACListISF 物件之 [**IACList**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist) 介面的指標 \_ ：</span><span class="sxs-lookup"><span data-stu-id="d87f2-151">In the following, assume that **pal** is a pointer to the [**IACList**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist) interface of a CLSID\_ACListISF object:</span></span>

-   <span data-ttu-id="d87f2-152">使用 [**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder)：</span><span class="sxs-lookup"><span data-stu-id="d87f2-152">Using [**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder):</span></span>

    <span data-ttu-id="d87f2-153">若要告訴 CLSID \_ ACListISF 物件應將特定 [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) 視為目前的目錄，您可以使用物件的 [**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) 介面。</span><span class="sxs-lookup"><span data-stu-id="d87f2-153">To tell the CLSID\_ACListISF object that a particular [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) should be treated as the current directory, you can use the object's [**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) interface.</span></span> <span data-ttu-id="d87f2-154">因為 **ITEMIDLIST** 可參考虛擬資料夾，所以這個方法比使用 [**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory)更有彈性。</span><span class="sxs-lookup"><span data-stu-id="d87f2-154">Since an **ITEMIDLIST** can refer to a virtual folder, this method is more flexible than using [**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory).</span></span>

    <span data-ttu-id="d87f2-155">請注意，下列範例會使用範本化 QueryInterface，以允許簡化的參數清單。</span><span class="sxs-lookup"><span data-stu-id="d87f2-155">Note that the following examples use the templatized QueryInterface, which allows for a simplified parameter list.</span></span>

    ```C++
    IPersistFolder *ppf;

    hr = pal2->QueryInterface(IID_PPV_ARGS(&ppf));   
    if (SUCCEEDED(hr))
    {
        hr = ppf->Initialize(pidlCurrentDirectory);
        ppf->Release();
    }
    ```

    

-   <span data-ttu-id="d87f2-156">使用 [**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory)：</span><span class="sxs-lookup"><span data-stu-id="d87f2-156">Using [**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory):</span></span>

    <span data-ttu-id="d87f2-157">若要為 CLSID \_ ACListISF 物件提供目前的目錄的路徑，您可以使用物件的 [**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory) 介面。</span><span class="sxs-lookup"><span data-stu-id="d87f2-157">To give the CLSID\_ACListISF object a path as the current directory, you can use the object's [**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory) interface.</span></span>

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

    

 

 
