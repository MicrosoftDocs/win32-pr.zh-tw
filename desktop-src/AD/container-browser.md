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
# <a name="container-browser"></a><span data-ttu-id="099ea-105">容器瀏覽器</span><span class="sxs-lookup"><span data-stu-id="099ea-105">Container Browser</span></span>

<span data-ttu-id="099ea-106">應用程式可以使用 [**DsBrowseForContainer**](/windows/desktop/api/Dsclient/nf-dsclient-dsbrowseforcontainera) 函式來顯示對話方塊，該對話方塊可用於流覽 Active Directory 網域服務中的容器。</span><span class="sxs-lookup"><span data-stu-id="099ea-106">An application can use the [**DsBrowseForContainer**](/windows/desktop/api/Dsclient/nf-dsclient-dsbrowseforcontainera) function to display a dialog box that can be used to browse through the containers in an Active Directory Domain Service.</span></span> <span data-ttu-id="099ea-107">對話方塊會以樹狀格式顯示容器，並可讓使用者使用鍵盤和滑鼠流覽樹狀結構。</span><span class="sxs-lookup"><span data-stu-id="099ea-107">The dialog box displays the containers in a tree format and enables the user to navigate through the tree using the keyboard and mouse.</span></span> <span data-ttu-id="099ea-108">當使用者在對話方塊中選取專案時，會提供使用者所選取之容器的 ADsPath。</span><span class="sxs-lookup"><span data-stu-id="099ea-108">When the user selects an item in the dialog box, the ADsPath of the container selected by the user is provided.</span></span>

<span data-ttu-id="099ea-109">[**DsBrowseForContainer**](/windows/desktop/api/Dsclient/nf-dsclient-dsbrowseforcontainera) 會取得 [**DSBROWSEINFO**](/windows/desktop/api/Dsclient/ns-dsclient-dsbrowseinfoa) 結構的指標，該結構包含對話方塊的相關資料，並傳回所選取專案的 ADsPath。</span><span class="sxs-lookup"><span data-stu-id="099ea-109">[**DsBrowseForContainer**](/windows/desktop/api/Dsclient/nf-dsclient-dsbrowseforcontainera) takes a pointer to a [**DSBROWSEINFO**](/windows/desktop/api/Dsclient/ns-dsclient-dsbrowseinfoa) structure that contains data about the dialog box and returns the ADsPath of the selected item.</span></span>

<span data-ttu-id="099ea-110">**PszRoot** 成員是 Unicode 字串的指標，其中包含樹狀結構的根容器。</span><span class="sxs-lookup"><span data-stu-id="099ea-110">The **pszRoot** member is a pointer to a Unicode string that contains the root container of the tree.</span></span> <span data-ttu-id="099ea-111">如果 **pszRoot** 為 **Null**，則樹狀結構會包含整個樹狀結構。</span><span class="sxs-lookup"><span data-stu-id="099ea-111">If **pszRoot** is **NULL**, the tree will contain the entire tree.</span></span>

<span data-ttu-id="099ea-112">**PszPath** 成員會收到所選物件的 ADsPath。</span><span class="sxs-lookup"><span data-stu-id="099ea-112">The **pszPath** member receives the ADsPath of the selected object.</span></span> <span data-ttu-id="099ea-113">您可以指定要顯示的特定容器，並在第一次顯示對話方塊時選取。</span><span class="sxs-lookup"><span data-stu-id="099ea-113">It is possible to specify a particular container to be visible and selected when the dialog box is first displayed.</span></span> <span data-ttu-id="099ea-114">將 **pszPath** 設定為要選取之專案的 ADsPath，並在 **DwFlags** 中設定 **DSBI \_ EXPANDONOPEN** 旗標，即可完成這項作業。</span><span class="sxs-lookup"><span data-stu-id="099ea-114">This is accomplished by setting **pszPath** to the ADsPath of the item to be selected and setting the **DSBI\_EXPANDONOPEN** flag in **dwFlags**.</span></span>

<span data-ttu-id="099ea-115">您也可以藉由執行 [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) 函式，在執行時間控制對話方塊的內容和行為。</span><span class="sxs-lookup"><span data-stu-id="099ea-115">The contents and behavior of the dialog box can also be controlled at runtime by implementing a [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) function.</span></span> <span data-ttu-id="099ea-116">**BFFCallBack** 函式是由應用程式所執行，而且會在特定事件發生時呼叫。</span><span class="sxs-lookup"><span data-stu-id="099ea-116">The **BFFCallBack** function is implemented by the application and is called when certain events occur.</span></span> <span data-ttu-id="099ea-117">應用程式可以使用這些事件來控制對話方塊中專案的顯示方式，以及對話方塊的實際內容。</span><span class="sxs-lookup"><span data-stu-id="099ea-117">An application can use these events to control how the items in the dialog box are displayed as well as the actual contents of the dialog box.</span></span> <span data-ttu-id="099ea-118">例如，應用程式可以藉由執行可處理 **DSBM \_ QUERYINSERT** 通知的 **BFFCallBack** 函式，來篩選對話方塊中顯示的專案。</span><span class="sxs-lookup"><span data-stu-id="099ea-118">For example, an application can filter the items displayed in the dialog box by implementing a **BFFCallBack** function that can handle the **DSBM\_QUERYINSERT** notification.</span></span> <span data-ttu-id="099ea-119">收到 **DSBM \_ QUERYINSERT** 通知時，請使用 [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema)結構的 **pszADsPath** 成員來判斷即將插入的專案。</span><span class="sxs-lookup"><span data-stu-id="099ea-119">When a **DSBM\_QUERYINSERT** notification is received, use the **pszADsPath** member of the [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) structure to determine which item is about to be inserted.</span></span> <span data-ttu-id="099ea-120">如果應用程式判斷不應該顯示專案，則可以執行下列步驟來隱藏專案。</span><span class="sxs-lookup"><span data-stu-id="099ea-120">If the application determines that the item should not be displayed, it can hide the item by performing the following steps.</span></span>

1.  <span data-ttu-id="099ea-121">將 **DSBF \_ 狀態** 旗標加入至 [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema)結構的 **dwMask** 成員。</span><span class="sxs-lookup"><span data-stu-id="099ea-121">Add the **DSBF\_STATE** flag to the **dwMask** member of the [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) structure.</span></span>
2.  <span data-ttu-id="099ea-122">將 **DSBS \_ 隱藏** 旗標加入至 [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema)結構的 **dwStateMask** 成員。</span><span class="sxs-lookup"><span data-stu-id="099ea-122">Add the **DSBS\_HIDDEN** flag to the **dwStateMask** member of the [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) structure.</span></span>
3.  <span data-ttu-id="099ea-123">將 **DSBS \_ 隱藏** 旗標加入至 [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema)結構的 **dwState** 成員。</span><span class="sxs-lookup"><span data-stu-id="099ea-123">Add the **DSBS\_HIDDEN** flag to the **dwState** member of the [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) structure.</span></span>
4.  <span data-ttu-id="099ea-124">從 [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) 函數傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="099ea-124">Return a nonzero value from the [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) function.</span></span>

<span data-ttu-id="099ea-125">除了隱藏特定專案之外，應用程式也可以藉由處理 **DSBM \_ QUERYINSERT** 通知，來修改針對專案顯示的文字和圖示。</span><span class="sxs-lookup"><span data-stu-id="099ea-125">In addition to hiding certain items, an application can modify the text and icon displayed for the item by handling the **DSBM\_QUERYINSERT** notification.</span></span> <span data-ttu-id="099ea-126">如需詳細資訊，請參閱 [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema)。</span><span class="sxs-lookup"><span data-stu-id="099ea-126">For more information, see [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema).</span></span>

<span data-ttu-id="099ea-127">[**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback)函式可以使用 **BFFM \_ 初始化** 的通知來取得對話方塊的控制碼。</span><span class="sxs-lookup"><span data-stu-id="099ea-127">The [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) function can use the **BFFM\_INITIALIZED** notification to obtain the handle of the dialog box.</span></span> <span data-ttu-id="099ea-128">應用程式可以使用此控制碼，將訊息（例如 **BFFM \_ ENABLEOK**）傳送至對話方塊。</span><span class="sxs-lookup"><span data-stu-id="099ea-128">The application can use this handle to send messages, such as **BFFM\_ENABLEOK**, to the dialog box.</span></span> <span data-ttu-id="099ea-129">如需可傳送至對話方塊之訊息的詳細資訊，請參閱 [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback)。</span><span class="sxs-lookup"><span data-stu-id="099ea-129">For more information about the messages that can be sent to the dialog box, see [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback).</span></span>

<span data-ttu-id="099ea-130">對話方塊控制碼也可以用來取得對話方塊中控制項的直接存取權。</span><span class="sxs-lookup"><span data-stu-id="099ea-130">The dialog box handle can also be used to gain direct access to the controls in the dialog box.</span></span> <span data-ttu-id="099ea-131">**DSBID \_橫幅** 是靜態文字控制項的識別碼，會在其中顯示 [**DSBROWSEINFO**](/windows/desktop/api/Dsclient/ns-dsclient-dsbrowseinfoa)結構的 **pszTitle** 成員。</span><span class="sxs-lookup"><span data-stu-id="099ea-131">**DSBID\_BANNER** is the identifier for the static text control that the **pszTitle** member of the [**DSBROWSEINFO**](/windows/desktop/api/Dsclient/ns-dsclient-dsbrowseinfoa) structure is displayed in.</span></span> <span data-ttu-id="099ea-132">**DSBID \_CONTAINERLIST** 是用來顯示樹狀目錄內容之樹狀檢視控制項的識別碼。</span><span class="sxs-lookup"><span data-stu-id="099ea-132">**DSBID\_CONTAINERLIST** is the identifier of the tree view control used to display the tree contents.</span></span> <span data-ttu-id="099ea-133">盡可能避免使用這些專案，以避免未來的應用程式相容性問題。</span><span class="sxs-lookup"><span data-stu-id="099ea-133">Use of these items should be avoided, if possible, to prevent future application compatibility problems.</span></span>

<span data-ttu-id="099ea-134">下列 c + + 程式碼範例示範如何使用 [**DsBrowseForContainer**](/windows/desktop/api/Dsclient/nf-dsclient-dsbrowseforcontainera) 函式來建立 [容器瀏覽器] 對話方塊，並執行 [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) 函數。</span><span class="sxs-lookup"><span data-stu-id="099ea-134">The following C++ code example shows how to use the [**DsBrowseForContainer**](/windows/desktop/api/Dsclient/nf-dsclient-dsbrowseforcontainera) function to create the container browser dialog box and implement a [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) function.</span></span> <span data-ttu-id="099ea-135">[**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback)會使用 **DSBM \_ QUERYINSERT** 通知，將每個專案的顯示名稱變更為專案的分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="099ea-135">The [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) uses the **DSBM\_QUERYINSERT** notification to change the display name for each item to the distinguished name of the item.</span></span>


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



 

 