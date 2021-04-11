---
title: 容器瀏覽器
description: 應用程式可以使用 DsBrowseForContainer 函式來顯示對話方塊，該對話方塊可用於流覽 Active Directory 網域服務中的容器。
ms.assetid: aa88d565-ff25-4082-964a-9a230d2607f2
ms.tgt_platform: multiple
keywords:
- 容器瀏覽器廣告
- 容器 AD、瀏覽器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 964c67873cc7936a75e2b9c1cdf331d0fa1fdae1
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104023276"
---
# <a name="container-browser"></a>容器瀏覽器

應用程式可以使用 [**DsBrowseForContainer**](/windows/desktop/api/Dsclient/nf-dsclient-dsbrowseforcontainera) 函式來顯示對話方塊，該對話方塊可用於流覽 Active Directory 網域服務中的容器。 對話方塊會以樹狀格式顯示容器，並可讓使用者使用鍵盤和滑鼠流覽樹狀結構。 當使用者在對話方塊中選取專案時，會提供使用者所選取之容器的 ADsPath。

[**DsBrowseForContainer**](/windows/desktop/api/Dsclient/nf-dsclient-dsbrowseforcontainera) 會取得 [**DSBROWSEINFO**](/windows/desktop/api/Dsclient/ns-dsclient-dsbrowseinfoa) 結構的指標，該結構包含對話方塊的相關資料，並傳回所選取專案的 ADsPath。

**PszRoot** 成員是 Unicode 字串的指標，其中包含樹狀結構的根容器。 如果 **pszRoot** 為 **Null**，則樹狀結構會包含整個樹狀結構。

**PszPath** 成員會收到所選物件的 ADsPath。 您可以指定要顯示的特定容器，並在第一次顯示對話方塊時選取。 將 **pszPath** 設定為要選取之專案的 ADsPath，並在 **DwFlags** 中設定 **DSBI \_ EXPANDONOPEN** 旗標，即可完成這項作業。

您也可以藉由執行 [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) 函式，在執行時間控制對話方塊的內容和行為。 **BFFCallBack** 函式是由應用程式所執行，而且會在特定事件發生時呼叫。 應用程式可以使用這些事件來控制對話方塊中專案的顯示方式，以及對話方塊的實際內容。 例如，應用程式可以藉由執行可處理 **DSBM \_ QUERYINSERT** 通知的 **BFFCallBack** 函式，來篩選對話方塊中顯示的專案。 收到 **DSBM \_ QUERYINSERT** 通知時，請使用 [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema)結構的 **pszADsPath** 成員來判斷即將插入的專案。 如果應用程式判斷不應該顯示專案，則可以執行下列步驟來隱藏專案。

1.  將 **DSBF \_ 狀態** 旗標加入至 [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema)結構的 **dwMask** 成員。
2.  將 **DSBS \_ 隱藏** 旗標加入至 [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema)結構的 **dwStateMask** 成員。
3.  將 **DSBS \_ 隱藏** 旗標加入至 [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema)結構的 **dwState** 成員。
4.  從 [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) 函數傳回非零值。

除了隱藏特定專案之外，應用程式也可以藉由處理 **DSBM \_ QUERYINSERT** 通知，來修改針對專案顯示的文字和圖示。 如需詳細資訊，請參閱 [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema)。

[**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback)函式可以使用 **BFFM \_ 初始化** 的通知來取得對話方塊的控制碼。 應用程式可以使用此控制碼，將訊息（例如 **BFFM \_ ENABLEOK**）傳送至對話方塊。 如需可傳送至對話方塊之訊息的詳細資訊，請參閱 [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback)。

對話方塊控制碼也可以用來取得對話方塊中控制項的直接存取權。 **DSBID \_橫幅** 是靜態文字控制項的識別碼，會在其中顯示 [**DSBROWSEINFO**](/windows/desktop/api/Dsclient/ns-dsclient-dsbrowseinfoa)結構的 **pszTitle** 成員。 **DSBID \_CONTAINERLIST** 是用來顯示樹狀目錄內容之樹狀檢視控制項的識別碼。 盡可能避免使用這些專案，以避免未來的應用程式相容性問題。

下列 c + + 程式碼範例示範如何使用 [**DsBrowseForContainer**](/windows/desktop/api/Dsclient/nf-dsclient-dsbrowseforcontainera) 函式來建立 [容器瀏覽器] 對話方塊，並執行 [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) 函數。 [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback)會使用 **DSBM \_ QUERYINSERT** 通知，將每個專案的顯示名稱變更為專案的分辨名稱。


```C++
#include <shlobj.h>
#include <dsclient.h>
#include <atlbase.h>

/**********

    WideCharToLocal()
   
***********/

int WideCharToLocal(LPTSTR pLocal, LPWSTR pWide, DWORD dwChars)
{
    *pLocal = NULL;
    size_t nWideLength = 0;
    wchar_t *pwszSubstring;

    nWideLength = wcslen(pWide);

#ifdef UNICODE
    if(nWideLength < dwChars)
    {
        wcsncpy_s(pLocal, pWide, dwChars);
    }
    else
    {
        wcsncpy_s(pLocal, pWide, dwChars-1);
        pLocal[dwChars-1] = NULL;
    }
#else
    if(nWideLength < dwChars)
    {
        WideCharToMultiByte(    CP_ACP, 
                                0, 
                                pWide, 
                                -1, 
                                pLocal, 
                                dwChars, 
                                NULL, 
                                NULL);
    }
    else
    {
        pwszSubstring = new WCHAR[dwChars];
        wcsncpy_s(pwszSubstring,pWide,dwChars-1);
        pwszSubstring[dwChars-1] = NULL;

        WideCharToMultiByte(    CP_ACP, 
                                0, 
                                pwszSubstring, 
                                -1, 
                                pLocal, 
                                dwChars, 
                                NULL, 
                                NULL);

    delete [] pwszSubstring;
    }
#endif

    return lstrlen(pLocal);
}

/**********

    BrowseCallback()

***********/

int CALLBACK BrowseCallback(HWND hWnd, 
                            UINT uMsg, 
                            LPARAM lParam, 
                            LPARAM lpData)
{
    switch(uMsg)
    {
    case DSBM_QUERYINSERT:
        {
            BOOL fReturn = FALSE;
            DSBITEM *pItem = (DSBITEM*)lParam;

            /*
            If this is to the root item, get the distinguished name 
            for the object and set the display name to the 
            distinguished name.
            */
            if(!(pItem->dwState & DSBS_ROOT))
            {
                HRESULT hr;
                IADs    *pads;

                hr = ADsGetObject(pItem->pszADsPath , 
                    IID_IADs, (LPVOID*)&pads);
                if(SUCCEEDED(hr))
                {
                    VARIANT var;

                    VariantInit(&var);
                    hr = pads->Get(CComBSTR("distinguishedName"), 
                        &var);
                    if(SUCCEEDED(hr))
                    {
                        if(VT_BSTR == var.vt)
                        {
                            WideCharToLocal(pItem->szDisplayName, 
                                var.bstrVal, 
                                DSB_MAX_DISPLAYNAME_CHARS);
                            pItem->dwMask |= DSBF_DISPLAYNAME;
                            fReturn = TRUE;
                        }
                        
                        VariantClear(&var);
                    }
                    
                    pads->Release();
                }
            }

            return fReturn;
        }

        break;
    }
    
    return FALSE;
}

/***********

    BrowseForContainer()

************/

HRESULT BrowseForContainer(HWND hwndParent, 
    LPOLESTR *ppContainerADsPath)
{
    HRESULT hr = E_FAIL;
    DSBROWSEINFO dsbi;
    OLECHAR wszPath[MAX_PATH * 2];
    DWORD result;
 
    if(!ppContainerADsPath)
    {
        return E_INVALIDARG;
    }
 
    ZeroMemory(&dsbi, sizeof(dsbi));
    dsbi.hwndOwner = hwndParent;
    dsbi.cbStruct = sizeof (DSBROWSEINFO);
    dsbi.pszCaption = TEXT("Browse for a Container");
    dsbi.pszTitle = TEXT("Select an Active Directory container.");
    dsbi.pszRoot = NULL;
    dsbi.pszPath = wszPath;
    dsbi.cchPath = sizeof(wszPath)/sizeof(OLECHAR);
    dsbi.dwFlags = DSBI_INCLUDEHIDDEN |
                    DSBI_IGNORETREATASLEAF|
                    DSBI_RETURN_FORMAT;
    dsbi.pfnCallback = BrowseCallback;
    dsbi.lParam = 0;
    dsbi.dwReturnFormat = ADS_FORMAT_X500;
 
    // Display the browse dialog box.
    // Returns -1, 0, IDOK, or IDCANCEL.
    result = DsBrowseForContainer(&dsbi); 
    if(IDOK == result)
    {
        // Allocate memory for the string.
        *ppContainerADsPath = (OLECHAR*)CoTaskMemAlloc(
            sizeof(OLECHAR)*(wcslen(wszPath) + 1));
        if(*ppContainerADsPath)
        {
            wcscpy_s(*ppContainerADsPath, wszPath);
            // Caller must free using CoTaskMemFree. 
            hr = S_OK;
        }
        else
        {
            hr = E_FAIL;
        }
    }
    else
    {
        hr = E_FAIL;
    }
 
    return hr;
}
```



 

 