---
description: 從 Windows Vista 開始，[一般專案] 對話方塊會在用來開啟或儲存檔案時取代舊版的 [一般檔案] 對話方塊。
title: 一般專案對話方塊
ms.topic: article
ms.date: 05/31/2018
ms.assetid: f8846148-89a5-4b9b-ad68-56137a5c2f65
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 2956bf7329ff9c92b777199d040d1275aa827cfa9ea9c8bfbec175d234b204f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943518"
---
# <a name="common-item-dialog"></a>一般專案對話方塊

從 Windows Vista 開始，[一般專案] 對話方塊會在用來開啟或儲存檔案時取代舊版的 [一般檔案] 對話方塊。 [一般專案] 對話方塊用於兩種變化： [ **開啟** ] 對話方塊和 [ **儲存** ] 對話方塊。 這兩個對話方塊共用大部分的功能，但每個都有自己的唯一方法。

雖然這個較新的版本命名為 [一般專案] 對話方塊，但在大部分的檔中，它仍會繼續稱為 [一般檔案] 對話方塊。 除非您處理的是舊版 Windows，否則您應該假設任何提及的 [一般檔案] 對話方塊都會參考這個 [一般專案] 對話方塊。

以下將討論下列主題：

-   [IFileDialog、IFileOpenDialog 和 IFileSaveDialog](#ifiledialog-ifileopendialog-and-ifilesavedialog)
    -   [範例使用方式](#sample-usage)
-   [從對話方塊接聽事件](#listening-to-events-from-the-dialog)
    -   [OnFileOk](#onfileok)
    -   [OnShareViolation 和 OnOverwrite](#onshareviolation-and-onoverwrite)
-   [自訂對話方塊](#customizing-the-dialog)
    -   [將選項新增至 [確定] 按鈕](#adding-options-to-the-ok-button)
    -   [回應新增控制項中的事件](#responding-to-events-in-added-controls)
-   [完整範例](#full-samples)
-   [相關主題](#related-topics)

## <a name="ifiledialog-ifileopendialog-and-ifilesavedialog"></a>IFileDialog、IFileOpenDialog 和 IFileSaveDialog

WindowsVista 提供 [**開啟**] 和 [**儲存**] 對話方塊的實作為： clsid \_ FileOpenDialog 和 clsid \_ FileSaveDialog。 這些對話方塊如下所示。

![[開啟] 對話方塊的螢幕擷取畫面](images/cid/openfiledialog.png)

![[另存新檔] 對話方塊的螢幕擷取畫面](images/cid/savefiledialog.png)

[**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) 和 [**IFileSaveDialog**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog) 繼承自 [**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) ，並共用許多功能。 此外，[ **開啟** ] 對話方塊支援 **IFileOpenDialog**，而 [ **儲存** ] 對話方塊支援 **IFileSaveDialog**。

在 Windows Vista 中找到的常見專案對話方塊可提供數個優點，而不是舊版提供的實作為：

-   支援透過 [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) 直接使用 Shell 命名空間，而不是使用檔案系統路徑。
-   啟用對話方塊的簡單自訂，例如在 [ **確定]** 按鈕上設定標籤，而不需要進行勾點程式。
-   藉由新增一組在不使用 Win32 對話方塊範本運作的資料驅動控制項，支援更廣泛的對話自訂。 這個自訂配置會釋出 UI 配置的呼叫進程。 由於對話方塊設計的任何變更會繼續使用此資料模型，因此對話的執行不會系結至特定的目前版本對話方塊。
-   支援對話方塊內事件的呼叫端通知，例如選取範圍變更或檔案類型變更。 也可讓呼叫進程攔截對話方塊中的特定事件，例如剖析。
-   引進新的對話方塊功能，例如將呼叫者指定的位置新增至 **位置** 列。
-   在 [**儲存**] 對話方塊中，開發人員可以利用 Windows Vista Shell 的新中繼資料功能。

此外，開發人員也可以選擇執行下列介面：

-   [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents) ，以接收對話方塊內的事件通知。
-   [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) ，將控制項加入對話方塊中。
-   [**IFileDialogControlEvents**](/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialogcontrolevents) ，以在這些新增的控制項中收到事件的通知。

[ **開啟** ] 或 [ **儲存** ] 對話方塊會將 [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) 或 [**IShellItemArray**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray) 物件傳回給呼叫進程。 接著，呼叫者可以使用個別的 **IShellItem** 物件取得檔案系統路徑，或開啟專案上的資料流程來讀取或寫入資訊。

新對話方法可用的旗標和選項非常類似于 [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)結構中找到的舊版 **OFN** 旗標，並用於 [**GetOpenFileName**](/windows/win32/api/commdlg/nf-commdlg-getopenfilenamea)和 [**GetSaveFileName**](/windows/win32/api/commdlg/nf-commdlg-getsavefilenamea)。 其中有許多都是一樣的，不同之處在于它們是以 FOS 前置詞開頭。 您可以在 [**IFileDialog：： GetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getoptions) 和 [**IFileDialog：： >setoptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions) 主題中找到完整的清單。 [**開啟**] 和 [**儲存**] 對話方塊預設會以最常見的旗標建立。 針對 [ **開啟** ] 對話方塊，這是 (fos \_ PATHMUSTEXIST \| fos \_ FILEMUSTEXIST \| fos \_ NOCHANGEDIR) ，而針對 [ **儲存** ] 對話方塊，這是 (fos \_ OVERWRITEPROMPT \| fos \_ NOREADONLYRETURN \| fos \_ PATHMUSTEXIST \| fos \_ NOCHANGEDIR) 。

[**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) 和其子系介面繼承自並擴充 [**IModalWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-imodalwindow)。 [**Show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show) 會以它唯一的參數做為父視窗的控制碼。 如果 **Show** 傳回成功，則會有有效的結果。 如果傳回 `HRESULT_FROM_WIN32(ERROR_CANCELLED)` ，則表示使用者已取消對話方塊。 它也可能會合法傳回另一個錯誤碼，例如 **E \_ OUTOFMEMORY**。

### <a name="sample-usage"></a>範例用法

下列各節顯示各種對話工作的範例程式碼。

-   [基本使用方式](#basic-usage)
-   [將結果限制為檔案系統專案](#limiting-results-to-file-system-items)
-   [指定對話方塊的檔案類型](#specifying-file-types-for-a-dialog)
-   [控制預設資料夾](#controlling-the-default-folder)
-   [將專案加入至位置列](#adding-items-to-the-places-bar)
-   [狀態持續性](#state-persistence)
-   [多重複選功能](#multiselect-capabilities)

大部分的範例程式碼都可以在 Windows SDK 一般檔案[對話方塊範例](samples-commonfiledialog.md)中找到。

### <a name="basic-usage"></a>基本使用方式

下列範例說明如何啟動 **開啟** 的對話方塊。 在此範例中，它受限於 Microsoft Word 檔。

> [!Note]  
> 本主題中的數個範例會使用 `CDialogEventHandler_CreateInstance` helper 函式來建立 [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents) 執行的實例。 若要在您自己的程式碼中使用此函式，請 `CDialogEventHandler_CreateInstance` 從 [ [一般檔案] 對話方塊範例](samples-commonfiledialog.md)複製函式的原始程式碼，此範例取自本主題中的所有範例。

 


```C++
HRESULT BasicFileOpen()
{
    // CoCreate the File Open Dialog object.
    IFileDialog *pfd = NULL;
    HRESULT hr = CoCreateInstance(CLSID_FileOpenDialog, 
                      NULL, 
                      CLSCTX_INPROC_SERVER, 
                      IID_PPV_ARGS(&pfd));
    if (SUCCEEDED(hr))
    {
        // Create an event handling object, and hook it up to the dialog.
        IFileDialogEvents *pfde = NULL;
        hr = CDialogEventHandler_CreateInstance(IID_PPV_ARGS(&pfde));
        if (SUCCEEDED(hr))
        {
            // Hook up the event handler.
            DWORD dwCookie;
            hr = pfd->Advise(pfde, &dwCookie);
            if (SUCCEEDED(hr))
            {
                // Set the options on the dialog.
                DWORD dwFlags;

                // Before setting, always get the options first in order 
                // not to override existing options.
                hr = pfd->GetOptions(&dwFlags);
                if (SUCCEEDED(hr))
                {
                    // In this case, get shell items only for file system items.
                    hr = pfd->SetOptions(dwFlags | FOS_FORCEFILESYSTEM);
                    if (SUCCEEDED(hr))
                    {
                        // Set the file types to display only. 
                        // Notice that this is a 1-based array.
                        hr = pfd->SetFileTypes(ARRAYSIZE(c_rgSaveTypes), c_rgSaveTypes);
                        if (SUCCEEDED(hr))
                        {
                            // Set the selected file type index to Word Docs for this example.
                            hr = pfd->SetFileTypeIndex(INDEX_WORDDOC);
                            if (SUCCEEDED(hr))
                            {
                                // Set the default extension to be ".doc" file.
                                hr = pfd->SetDefaultExtension(L"doc;docx");
                                if (SUCCEEDED(hr))
                                {
                                    // Show the dialog
                                    hr = pfd->Show(NULL);
                                    if (SUCCEEDED(hr))
                                    {
                                        // Obtain the result once the user clicks 
                                        // the 'Open' button.
                                        // The result is an IShellItem object.
                                        IShellItem *psiResult;
                                        hr = pfd->GetResult(&psiResult);
                                        if (SUCCEEDED(hr))
                                        {
                                            // We are just going to print out the 
                                            // name of the file for sample sake.
                                            PWSTR pszFilePath = NULL;
                                            hr = psiResult->GetDisplayName(SIGDN_FILESYSPATH, 
                                                               &pszFilePath);
                                            if (SUCCEEDED(hr))
                                            {
                                                TaskDialog(NULL,
                                                           NULL,
                                                           L"CommonFileDialogApp",
                                                           pszFilePath,
                                                           NULL,
                                                           TDCBF_OK_BUTTON,
                                                           TD_INFORMATION_ICON,
                                                           NULL);
                                                CoTaskMemFree(pszFilePath);
                                            }
                                            psiResult->Release();
                                        }
                                    }
                                }
                            }
                        }
                    }
                }
                // Unhook the event handler.
                pfd->Unadvise(dwCookie);
            }
            pfde->Release();
        }
        pfd->Release();
    }
    return hr;
}
```



### <a name="limiting-results-to-file-system-items"></a>將結果限制為檔案系統專案

下列範例取自上述範例，示範如何將結果限制為檔案系統專案。 請注意， [**IFileDialog：： >setoptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions) 會將新的旗標加入至透過 [**IFileDialog：： GetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getoptions)取得的值。 這是建議的方法。


```C++
                // Set the options on the dialog.
                DWORD dwFlags;

                // Before setting, always get the options first in order 
                // not to override existing options.
                hr = pfd->GetOptions(&dwFlags);
                if (SUCCEEDED(hr))
                {
                    // In this case, get shell items only for file system items.
                    hr = pfd->SetOptions(dwFlags | FOS_FORCEFILESYSTEM);
```



### <a name="specifying-file-types-for-a-dialog"></a>指定對話方塊的檔案類型

若要設定對話方塊可以處理的特定檔案類型，請使用 [**IFileDialog：： SetFileTypes**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setfiletypes) 方法。 該方法會接受 [**COMDLG \_ FILTERSPEC**](/windows/desktop/api/Shtypes/ns-shtypes-comdlg_filterspec) 結構的陣列，其中每個結構都代表一種檔案類型。

對話方塊中的預設擴充機制與 [**GetOpenFileName**](/windows/win32/api/commdlg/nf-commdlg-getopenfilenamea) 和 [**GetSaveFileName**](/windows/win32/api/commdlg/nf-commdlg-getsavefilenamea)不一樣。 當對話方塊開啟時，會初始化附加至 [檔案名] 編輯方塊中使用者所輸入之文字的副檔名。 它應該符合 (在對話方塊開啟) 時選取的預設檔案類型。 如果預設檔案類型為 " \* . \* " () 的所有檔案，則檔案可以是您選擇的副檔名。 如果使用者選擇不同的檔案類型，擴充功能會自動更新為與該檔案類型相關聯的第一個副檔名。 如果使用者選擇 " \* . \* " () 的所有檔案，則延伸模組會還原為其原始值。

下列範例說明如何完成這項作業。


```C++
                        // Set the file types to display only. 
                        // Notice that this is a 1-based array.
                        hr = pfd->SetFileTypes(ARRAYSIZE(c_rgSaveTypes), c_rgSaveTypes);
                        if (SUCCEEDED(hr))
                        {
                            // Set the selected file type index to Word Docs for this example.
                            hr = pfd->SetFileTypeIndex(INDEX_WORDDOC);
                            if (SUCCEEDED(hr))
                            {
                                // Set the default extension to be ".doc" file.
                                hr = pfd->SetDefaultExtension(L"doc;docx");
```



### <a name="controlling-the-default-folder"></a>控制預設資料夾

Shell 命名空間中的任何資料夾都可以作為對話方塊的預設資料夾， (當使用者選擇開啟或儲存檔案) 時所顯示的資料夾。 呼叫 [**IFileDialog：： SetDefaultFolder**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setdefaultfolder) ，然後再呼叫 [**Show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show) 來執行此動作。

預設資料夾是在使用者第一次從您的應用程式開啟對話方塊時，對話方塊啟動的資料夾。 之後，對話方塊會在使用者開啟的最後一個資料夾或用來儲存專案的最後一個資料夾中開啟。 如需詳細資訊，請參閱 [狀態持續](#state-persistence) 性。

您可以藉由呼叫 [**IFileDialog：： SetFolder**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setfolder)，強制對話方塊在開啟時一律顯示相同的資料夾（不論先前的使用者動作為何）。 不過，我們不建議這麼做。 如果您在顯示對話方塊之前呼叫 **SetFolder** ，則不會顯示使用者所儲存或開啟的最新位置。 除非此行為有很明確的原因，否則它不是良好或預期的使用者經驗，應予以避免。 在幾乎所有的情況下， [**IFileDialog：： SetDefaultFolder**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setdefaultfolder) 是較佳的方法。

當您第一次在 [ **儲存** ] 對話方塊中儲存檔時，您應該遵循相同的指導方針來決定初始資料夾，就像在 [ **開啟** ] 對話方塊中所做的一樣。 如果使用者正在編輯先前現有的檔，請在儲存該檔的資料夾中開啟對話方塊，然後在編輯方塊中填入該檔的名稱。 呼叫 [**IFileSaveDialog：： SetSaveAsItem**](/windows/desktop/api/Shobjidl_core/nf-shobjidl_core-ifilesavedialog-setsaveasitem) 與目前的專案，然後再呼叫 [**Show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show)。

### <a name="adding-items-to-the-places-bar"></a>將專案加入至位置列

下列範例示範如何將專案加入至 **位置** 列：


```C++
HRESULT AddItemsToCommonPlaces()
{
    // CoCreate the File Open Dialog object.
    IFileDialog *pfd = NULL;
    HRESULT hr = CoCreateInstance(CLSID_FileOpenDialog, 
                      NULL, 
                      CLSCTX_INPROC_SERVER, 
                      IID_PPV_ARGS(&pfd));
    if (SUCCEEDED(hr))
    {
        // Always use known folders instead of hard-coding physical file paths.
        // In this case we are using Public Music KnownFolder.
        IKnownFolderManager *pkfm = NULL;
        hr = CoCreateInstance(CLSID_KnownFolderManager, 
                      NULL, 
                      CLSCTX_INPROC_SERVER, 
                      IID_PPV_ARGS(&pkfm));
        if (SUCCEEDED(hr))
        {
            // Get the known folder.
            IKnownFolder *pKnownFolder = NULL;
            hr = pkfm->GetFolder(FOLDERID_PublicMusic, &pKnownFolder);
            if (SUCCEEDED(hr))
            {
                // File Dialog APIs need an IShellItem that represents the location.
                IShellItem *psi = NULL;
                hr = pKnownFolder->GetShellItem(0, IID_PPV_ARGS(&psi));
                if (SUCCEEDED(hr))
                {
                    // Add the place to the bottom of default list in Common File Dialog.
                    hr = pfd->AddPlace(psi, FDAP_BOTTOM);
                    if (SUCCEEDED(hr))
                    {
                        // Show the File Dialog.
                        hr = pfd->Show(NULL);
                        if (SUCCEEDED(hr))
                        {
                            //
                            // You can add your own code here to handle the results.
                            //
                        }
                    }
                    psi->Release();
                }
                pKnownFolder->Release();
            }
            pkfm->Release();
        }
        pfd->Release();
    }
    return hr;
}
```



### <a name="state-persistence"></a>狀態持續性

在 Windows Vista 之前，會以每個進程為基礎來儲存狀態，例如最後流覽的資料夾。 不過，無論特定動作為何，都會使用該資訊。 例如，影片編輯應用程式會在 [轉譯 **為** ] 對話方塊中顯示相同的資料夾，就像在 [匯 **入媒體** ] 對話方塊中一樣。 在 Windows Vista 中，您可以透過使用 guid 來更加明確。 若要將 **GUID** 指派給對話，請呼叫 [**IFileDialog：： SetClientGuid**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setclientguid)。

### <a name="multiselect-capabilities"></a>多重複選功能

您可以使用 [**GetResults**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifileopendialog-getresults)方法，在 [**開啟**] 對話方塊中找到多重複選功能，如下所示。


```C++
HRESULT MultiselectInvoke()
{
    IFileOpenDialog *pfd;
    
    // CoCreate the dialog object.
    HRESULT hr = CoCreateInstance(CLSID_FileOpenDialog, 
                                  NULL, 
                                  CLSCTX_INPROC_SERVER, 
                                  IID_PPV_ARGS(&pfd));

    if (SUCCEEDED(hr))
    {
        DWORD dwOptions;
        // Specify multiselect.
        hr = pfd->GetOptions(&dwOptions);
        
        if (SUCCEEDED(hr))
        {
            hr = pfd->SetOptions(dwOptions | FOS_ALLOWMULTISELECT);
        }

        if (SUCCEEDED(hr))
        {
            // Show the Open dialog.
            hr = pfd->Show(NULL);

            if (SUCCEEDED(hr))
            {
                // Obtain the result of the user interaction.
                IShellItemArray *psiaResults;
                hr = pfd->GetResults(&psiaResults);
                
                if (SUCCEEDED(hr))
                {
                    //
                    // You can add your own code here to handle the results.
                    //
                    psiaResults->Release();
                }
            }
        }
        pfd->Release();
    }
    return hr;
}
```



## <a name="listening-to-events-from-the-dialog"></a>從對話方塊接聽事件

呼叫進程可以使用 [**IFileDialog：： Advise**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-advise)和 [**IFileDialog：： Unadvise**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-unadvise)方法，以對話方塊註冊 [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents)介面，如下所示。

這是取自 [基本使用](#basic-usage) 範例。


```C++
        // Create an event handling object, and hook it up to the dialog.
        IFileDialogEvents *pfde = NULL;
        hr = CDialogEventHandler_CreateInstance(IID_PPV_ARGS(&pfde));
        if (SUCCEEDED(hr))
        {
            // Hook up the event handler.
            DWORD dwCookie;
            hr = pfd->Advise(pfde, &dwCookie);
```



大部分的對話處理都是放在這裡。


```C++
                // Unhook the event handler.
                pfd->Unadvise(dwCookie);
            }
            pfde->Release();
        }
        pfd->Release();
    }
    return hr;
}
```



當使用者變更資料夾、檔案類型或選取專案時，呼叫進程可以使用事件來進行通知。 當呼叫進程已將控制項新增至對話方塊時，這些事件特別有用 (請參閱 [自訂對話方塊](#customizing-the-dialog)) ，而且必須變更這些控制項的狀態，以回應這些事件。 在所有情況下都很有用，那就是呼叫進程提供自訂程式碼來處理狀況的功能，例如共用違規、覆寫檔案，或在對話方塊關閉之前判斷檔案是否有效。 本節將說明其中一些案例。

### <a name="onfileok"></a>OnFileOk

當使用者選擇專案之後，就會呼叫這個方法，就在對話方塊關閉之前。 然後，應用程式可以呼叫 [**IFileDialog：： GetResult**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult) 或 [**IFileOpenDialog：： GetResults**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifileopendialog-getresults) ，就像在對話方塊關閉後才會完成。 如果選擇的專案是可接受的，則可以傳回 \_ [確定]。 否則，它們會傳回 \_ FALSE 和顯示 UI，告訴使用者為何選擇的專案無效。 如果 \_ 傳回 FALSE，則不會關閉對話方塊。

呼叫進程可以使用對話方塊本身的視窗控制碼作為 UI 的父系。 您可以先呼叫 [**IOleWindow：： QueryInterface**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) 來取得該控制碼，然後使用此範例所示的控制碼來呼叫 [**IOleWindow：： GetWindow**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) 。


```C++
HRESULT CDialogEventHandler::OnFileOk(IFileDialog *pfd) 
{ 
    IShellItem *psiResult;
    HRESULT hr = pfd->GetResult(&psiResult);
    
    if (SUCCEEDED(hr))
    {
        SFGAOF attributes;
        hr = psiResult->GetAttributes(SFGAO_COMPRESSED, &attributes);
    
        if (SUCCEEDED(hr))
        {
            if (attributes & SFGAO_COMPRESSED)
            {
                // Accept the file.
                hr = S_OK;
            }
            else
            {
                // Refuse the file.
                hr = S_FALSE;
                
                _DisplayMessage(pfd, L"Not a compressed file.");
            }
        }
        psiResult->Release();
    }
    return hr;
};

HRESULT CDialogEventHandler::_DisplayMessage(IFileDialog *pfd, PCWSTR pszMessage)
{
    IOleWindow *pWindow;
    HRESULT hr = pfd->QueryInterface(IID_PPV_ARGS(&pWindow));
    
    if (SUCCEEDED(hr))
    {
        HWND hwndDialog;
        hr = pWindow->GetWindow(&hwndDialog);
    
        if (SUCCEEDED(hr))
        {
            MessageBox(hwndDialog, pszMessage, L"An error has occurred", MB_OK);
        }
        pWindow->Release();
    }
    return hr;
}
```



### <a name="onshareviolation-and-onoverwrite"></a>OnShareViolation 和 OnOverwrite

如果使用者選擇要在 [ **儲存** ] 對話方塊中覆寫檔案，或正在儲存或取代的檔案正在使用中，而且無法寫入 (共用違規) ，則應用程式可以提供自訂功能來覆寫對話方塊的預設行為。 根據預設，覆寫檔案時，對話方塊會顯示提示，讓使用者驗證此動作。 對於共用違規，對話方塊預設會顯示錯誤訊息，而不會關閉，而且使用者必須進行其他選擇。 呼叫進程可以覆寫這些預設值，並視需要顯示自己的 UI。 您可以指示對話方塊拒絕檔案，並保持開啟或接受檔案並成功關閉。

## <a name="customizing-the-dialog"></a>自訂對話方塊

您可以將各種控制項新增至對話方塊，而不需要提供 Win32 對話方塊範本。 這些控制項包括按鈕、ComboBox、編輯方塊、CheckButton、選項按鈕清單、群組、分隔符號和靜態文字控制項。 呼叫 ([**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog)、 [**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog)或 [**IFileSaveDialog**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog)) 的對話方塊物件上的 **QueryInterface** ，以取得 [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize)指標。 使用該介面來新增控制項。 每個控制項都有相關聯的呼叫端提供的識別碼，以及可由呼叫進程設定的 *可見* 和 *已啟用* 狀態。 某些控制項（例如按鈕）也有相關聯的文字。

您可以將多個控制項加入至「視覺效果群組」中，以在對話方塊的版面配置中以單一單位移動。 群組可以有與其相關聯的標籤。

只有在顯示對話方塊之前，才可以加入控制項。 不過，一旦出現對話方塊，就可以視需要隱藏或顯示控制項，以回應使用者動作。 下列範例示範如何將選項按鈕清單新增至對話方塊。


```C++
// Controls
#define CONTROL_GROUP           2000
#define CONTROL_RADIOBUTTONLIST 2
#define CONTROL_RADIOBUTTON1    1
#define CONTROL_RADIOBUTTON2    2       // It is OK for this to have the same ID
                    // as CONTROL_RADIOBUTTONLIST, because it 
                    // is a child control under CONTROL_RADIOBUTTONLIST


// This code snippet demonstrates how to add custom controls in the Common File Dialog.
HRESULT AddCustomControls()
{
    // CoCreate the File Open Dialog object.
    IFileDialog *pfd = NULL;
    HRESULT hr = CoCreateInstance(CLSID_FileOpenDialog, 
                                  NULL, 
                                  CLSCTX_INPROC_SERVER, 
                                  IID_PPV_ARGS(&pfd));
    if (SUCCEEDED(hr))
    {
        // Create an event handling object, and hook it up to the dialog.
        IFileDialogEvents   *pfde       = NULL;
        DWORD               dwCookie    = 0;
        hr = CDialogEventHandler_CreateInstance(IID_PPV_ARGS(&pfde));
        if (SUCCEEDED(hr))
        {
            // Hook up the event handler.
            hr = pfd->Advise(pfde, &dwCookie);
            if (SUCCEEDED(hr))
            {
                // Set up a Customization.
                IFileDialogCustomize *pfdc = NULL;
                hr = pfd->QueryInterface(IID_PPV_ARGS(&pfdc));
                if (SUCCEEDED(hr))
                {
                    // Create a Visual Group.
                    hr = pfdc->StartVisualGroup(CONTROL_GROUP, L&quot;Sample Group&quot;);
                    if (SUCCEEDED(hr))
                    {
                        // Add a radio-button list.
                        hr = pfdc->AddRadioButtonList(CONTROL_RADIOBUTTONLIST);
                        if (SUCCEEDED(hr))
                        {
                            // Set the state of the added radio-button list.
                            hr = pfdc->SetControlState(CONTROL_RADIOBUTTONLIST, 
                                               CDCS_VISIBLE | CDCS_ENABLED);
                            if (SUCCEEDED(hr))
                            {
                                // Add individual buttons to the radio-button list.
                                hr = pfdc->AddControlItem(CONTROL_RADIOBUTTONLIST,
                                                          CONTROL_RADIOBUTTON1,
                                                          L&quot;Change Title to ABC&quot;);
                                if (SUCCEEDED(hr))
                                {
                                    hr = pfdc->AddControlItem(CONTROL_RADIOBUTTONLIST,
                                                              CONTROL_RADIOBUTTON2,
                                                              L&quot;Change Title to XYZ&quot;);
                                    if (SUCCEEDED(hr))
                                    {
                                        // Set the default selection to option 1.
                                        hr = pfdc->SetSelectedControlItem(CONTROL_RADIOBUTTONLIST,
                                                                          CONTROL_RADIOBUTTON1);
                                    }
                                }
                            }
                        }
                        // End the visual group.
                        pfdc->EndVisualGroup();
                    }
                    pfdc->Release();
                }

                if (FAILED(hr))
                {
                    // Unadvise here in case we encounter failures 
                    // before we get a chance to show the dialog.
                    pfd->Unadvise(dwCookie);
                }
            }
            pfde->Release();
        }

        if (SUCCEEDED(hr))
        {
            // Now show the dialog.
            hr = pfd->Show(NULL);
            if (SUCCEEDED(hr))
            {
                //
                // You can add your own code here to handle the results.
                //
            }
            // Unhook the event handler.
            pfd->Unadvise(dwCookie);
        }
        pfd->Release();
    }
    return hr;
}
```





### <a name="adding-options-to-the-ok-button"></a>將選項新增至 [確定] 按鈕

同樣地，您也可以將選擇新增至 [ **開啟** ] 或 [ **儲存** ] 按鈕，這是其各自對話方塊類型的 **[確定]** 按鈕。 您可以透過附加至按鈕的下拉式清單方塊來存取這些選項。 清單中的第一個專案會變成按鈕的文字。 下列範例示範如何提供有兩種可能性的 **開啟** 按鈕：「開啟」和「以唯讀方式開啟」。


```C++
// OpenChoices options
#define OPENCHOICES 0
#define OPEN 0
#define OPEN_AS_READONLY 1


HRESULT AddOpenChoices()
{
    // CoCreate the File Open Dialog object.
    IFileDialog *pfd = NULL;
    HRESULT hr = CoCreateInstance(CLSID_FileOpenDialog, 
                      NULL, 
                      CLSCTX_INPROC_SERVER, 
                      IID_PPV_ARGS(&pfd));
    if (SUCCEEDED(hr))
    {
        // Create an event handling object, and hook it up to the dialog.
        IFileDialogEvents   *pfde       = NULL;
        DWORD               dwCookie    = 0;
        hr = CDialogEventHandler_CreateInstance(IID_PPV_ARGS(&pfde));
        if (SUCCEEDED(hr))
        {
            // Hook up the event handler.
            hr = pfd->Advise(pfde, &dwCookie);
            if (SUCCEEDED(hr))
            {
                // Set up a Customization.
                IFileDialogCustomize *pfdc = NULL;
                hr = pfd->QueryInterface(IID_PPV_ARGS(&pfdc));
                if (SUCCEEDED(hr))
                {
                    hr = pfdc->EnableOpenDropDown(OPENCHOICES);
                    if (SUCCEEDED(hr))
                    {
                        hr = pfdc->AddControlItem(OPENCHOICES, OPEN, L&quot;&Open&quot;);
                    }                    
                    if (SUCCEEDED(hr))
                    {
                        hr = pfdc->AddControlItem(OPENCHOICES, 
                                                OPEN_AS_READONLY, 
                                                L&quot;Open as &read-only&quot;);
                    }
                    if (SUCCEEDED(hr))
                    {
                        pfd->Show(NULL);
                    }
                }
                pfdc->Release();
            }
            pfd->Unadvise(dwCookie);
        }
        pfde->Release();
    }
    pfd->Release();
    return hr;
}
```





使用者的選擇可以在對話方塊從 Show 方法傳回後，如同您針對 ComboBox 所做的一樣驗證，也可以 [**透過**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show) [**IFileDialogEvents：： OnFileOk**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogevents-onfileok)確認為處理的一部分。

### <a name="responding-to-events-in-added-controls"></a>回應新增控制項中的事件

除了 [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents)以外，呼叫進程所提供的事件處理常式還可以執行 [**IFileDialogControlEvents**](/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialogcontrolevents) 。 **IFileDialogControlEvents** 可讓呼叫進程回應這些事件：

-   按一下按鈕
-   CheckButton 狀態已變更
-   從功能表、ComboBox 或選項按鈕清單中選取的專案
-   控制啟用。 當呼叫進程想要變更清單中的專案時，當功能表即將顯示下拉式清單時，就會傳送這項資訊。

## <a name="full-samples"></a>完整範例

以下是 Windows 軟體開發套件 () SDK 的完整可下載 c + + 範例，其示範如何使用和與 [一般專案] 對話方塊的互動。

-   [一般檔案對話方塊範例](samples-commonfiledialog.md)
-   [一般檔案對話方塊模式範例](samples-commonfiledialogmodes.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IID \_ PPV 引數 \_**](/windows/win32/api/combaseapi/nf-combaseapi-iid_ppv_args)
</dt> </dl>

 

 
