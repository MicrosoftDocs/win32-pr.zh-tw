---
title: 如何在 Rich Edit 控制項中使用 OLE
description: 本章節包含在 rich edit 控制項中使用物件連結和內嵌 (OLE) 的相關資訊。
ms.assetid: bfcecbf5-cc35-47b8-a713-7e5fd03f60cc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7868bd62044c87765a25f6033499460ed044e57
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/17/2020
ms.locfileid: "104092601"
---
# <a name="how-to-use-ole-in-rich-edit-controls"></a><span data-ttu-id="83f96-103">如何在 Rich Edit 控制項中使用 OLE</span><span class="sxs-lookup"><span data-stu-id="83f96-103">How to Use OLE in Rich Edit Controls</span></span>

<span data-ttu-id="83f96-104">本章節包含在 rich edit 控制項中使用物件連結和內嵌 (OLE) 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="83f96-104">This section contains information about using object linking and embedding (OLE) in rich edit controls.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="83f96-105">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="83f96-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="83f96-106">技術</span><span class="sxs-lookup"><span data-stu-id="83f96-106">Technologies</span></span>

-   [<span data-ttu-id="83f96-107">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="83f96-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="83f96-108">必要條件</span><span class="sxs-lookup"><span data-stu-id="83f96-108">Prerequisites</span></span>

-   <span data-ttu-id="83f96-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="83f96-109">C/C++</span></span>
-   <span data-ttu-id="83f96-110">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="83f96-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="83f96-111">指示</span><span class="sxs-lookup"><span data-stu-id="83f96-111">Instructions</span></span>

### <a name="use-a-rich-edit-interface"></a><span data-ttu-id="83f96-112">使用 Rich Edit 介面</span><span class="sxs-lookup"><span data-stu-id="83f96-112">Use a Rich Edit Interface</span></span>

<span data-ttu-id="83f96-113">Rich edit 控制項會透過元件物件模型 (COM) 介面來公開部分功能。</span><span class="sxs-lookup"><span data-stu-id="83f96-113">Rich edit controls expose some of their functionality through Component Object Model (COM) interfaces.</span></span> <span data-ttu-id="83f96-114">藉由從控制項取得介面，您就能夠在控制項內使用其他物件。</span><span class="sxs-lookup"><span data-stu-id="83f96-114">By obtaining an interface from a control, you gain the ability to work with other objects within the control.</span></span> <span data-ttu-id="83f96-115">您可以藉由傳送 [**EM \_ GETOLEINTERFACE**](em-getoleinterface.md) 訊息來取得這個介面。</span><span class="sxs-lookup"><span data-stu-id="83f96-115">You can obtain this interface by sending the [**EM\_GETOLEINTERFACE**](em-getoleinterface.md) message.</span></span> <span data-ttu-id="83f96-116">您可以從 [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) 介面取得用於 [Text 物件模型](text-object-model.md)中的介面。</span><span class="sxs-lookup"><span data-stu-id="83f96-116">From the [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) interface, you can then obtain interfaces used in the [Text Object Model](text-object-model.md).</span></span>

<span data-ttu-id="83f96-117">當應用程式與物件互動時，應用程式會執行另一個介面 [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback)來定義控制項的行為。</span><span class="sxs-lookup"><span data-stu-id="83f96-117">Another interface, [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback), is implemented by applications to define the behavior of the control when it interacts with objects.</span></span>

### <a name="insert-an-object-into-a-rich-edit-control"></a><span data-ttu-id="83f96-118">將物件插入至 Rich Edit 控制項</span><span class="sxs-lookup"><span data-stu-id="83f96-118">Insert an Object into a Rich Edit Control</span></span>

<span data-ttu-id="83f96-119">下列程式碼範例會將檔案物件插入至 rich edit 控制項。</span><span class="sxs-lookup"><span data-stu-id="83f96-119">The following code example inserts a file object into a rich edit control.</span></span> <span data-ttu-id="83f96-120">如果程式與使用者電腦上的檔案類型相關聯 (例如，Microsoft Excel 的 .xls 檔案) ，則檔案的內容會顯示在控制項中;否則，就會出現圖示。</span><span class="sxs-lookup"><span data-stu-id="83f96-120">If a program is associated with the file type on the user's machine (for example, Microsoft Excel for an .xls file), the contents of the file display in the control; otherwise, an icon appears.</span></span>

1.  <span data-ttu-id="83f96-121">取得 [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) 介面。</span><span class="sxs-lookup"><span data-stu-id="83f96-121">Get the [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) interface.</span></span>

    ```
    BOOL InsertObject(HWND hRichEdit, LPCTSTR pszFileName)
    {
        HRESULT hr;

        LPRICHEDITOLE pRichEditOle;
        SendMessage(hRichEdit, EM_GETOLEINTERFACE, 0, (LPARAM)&pRichEditOle);
        
        ...
    ```

    

2.  <span data-ttu-id="83f96-122">建立結構化儲存體。</span><span class="sxs-lookup"><span data-stu-id="83f96-122">Create structured storage.</span></span>

    ```
        LPLOCKBYTES pLockBytes = NULL;
        hr = CreateILockBytesOnHGlobal(NULL, TRUE, &pLockBytes);
        
        LPSTORAGE pStorage;
        hr = StgCreateDocfileOnILockBytes(pLockBytes, 
                                          STGM_SHARE_EXCLUSIVE | STGM_CREATE | STGM_READWRITE, 
                                          0, &pStorage);
        ...
    ```

    

3.  <span data-ttu-id="83f96-123">設定資料格式。</span><span class="sxs-lookup"><span data-stu-id="83f96-123">Set up the data format.</span></span>

    ```
        FORMATETC formatEtc;
        
        formatEtc.cfFormat = 0;
        formatEtc.ptd      = NULL;
        formatEtc.dwAspect = DVASPECT_CONTENT;
        formatEtc.lindex   = -1;
        formatEtc.tymed    = TYMED_NULL;
        
        ...
    ```

    

4.  <span data-ttu-id="83f96-124">取得顯示位置的指標。</span><span class="sxs-lookup"><span data-stu-id="83f96-124">Get a pointer to the display site.</span></span>

    ```
        LPOLECLIENTSITE pClientSite;
        hr = pRichEditOle->GetClientSite(&pClientSite);
        
        ...
    ```

    

5.  <span data-ttu-id="83f96-125">建立物件並取出其 **IUnknown** 介面。</span><span class="sxs-lookup"><span data-stu-id="83f96-125">Create the object and retrieve its **IUnknown** interface.</span></span>

    ```
        LPUNKNOWN pUnk;
        CLSID clsid = CLSID_NULL;
        
        hr = OleCreateFromFile(clsid, 
                               pszFileName, 
                               IID_IUnknown, 
                               OLERENDER_DRAW, 
                               &formatEtc, 
                               pClientSite, 
                               pStorage, 
                               (void**)&pUnk);
        
        pClientSite->Release();
                  
        ...
    ```

    

6.  <span data-ttu-id="83f96-126">取得物件的 IOleObject 介面。</span><span class="sxs-lookup"><span data-stu-id="83f96-126">Get the IOleObject interface to the object.</span></span>

    ```
        LPOLEOBJECT pObject;
        
        hr = pUnk->QueryInterface(IID_IOleObject, (void**)&pObject);
        
        pUnk->Release();

        ...
    ```

    

7.  <span data-ttu-id="83f96-127">若要確定已正確計算參考，請通知物件包含它。</span><span class="sxs-lookup"><span data-stu-id="83f96-127">To ensure that references are counted correctly, notify the object that it is contained.</span></span>

    ```
        OleSetContainedObject(pObject, TRUE);

        ...
    ```

    

8.  <span data-ttu-id="83f96-128">設定物件資訊。</span><span class="sxs-lookup"><span data-stu-id="83f96-128">Set up object info.</span></span>

    ```
        REOBJECT reobject = { sizeof(REOBJECT)};
        
        hr = pObject->GetUserClassID(&clsid);
        
        reobject.clsid    = clsid;
        reobject.cp       = REO_CP_SELECTION;
        reobject.dvaspect = DVASPECT_CONTENT;
        reobject.dwFlags  = REO_RESIZABLE | REO_BELOWBASELINE;
        reobject.dwUser   = 0;
        reobject.poleobj  = pObject;
        reobject.polesite = pClientSite;
        reobject.pstg     = pStorage;
        
        SIZEL sizel       = { 0 };
        reobject.sizel    = sizel;

        ...
    ```

    

9.  <span data-ttu-id="83f96-129">將插入號移至文字的結尾，並加入換行字元。</span><span class="sxs-lookup"><span data-stu-id="83f96-129">Move the caret to the end of the text and add a carriage return.</span></span>

    ```
        SendMessage(hRichEdit, EM_SETSEL, 0, -1);
        
        DWORD dwStart, dwEnd;
        
        SendMessage(hRichEdit, EM_GETSEL, (WPARAM)&dwStart, (LPARAM)&dwEnd);
        SendMessage(hRichEdit, EM_SETSEL, dwEnd+1, dwEnd+1);
        SendMessage(hRichEdit, EM_REPLACESEL, TRUE, (WPARAM)L"\n"); 

        ...
    ```

    

10. <span data-ttu-id="83f96-130">插入物件。</span><span class="sxs-lookup"><span data-stu-id="83f96-130">Insert the object.</span></span>

    ```
        hr = pRichEditOle->InsertObject(&reobject);

        ...
    ```

    

11. <span data-ttu-id="83f96-131">清除。</span><span class="sxs-lookup"><span data-stu-id="83f96-131">Clean up.</span></span>

    ```
        pObject->Release();
        
        pRichEditOle->Release();

        return TRUE;
        
    }
    ```

    

### <a name="using-iricheditolecallback"></a><span data-ttu-id="83f96-132">使用 IRichEditOleCallback</span><span class="sxs-lookup"><span data-stu-id="83f96-132">Using IRichEditOleCallback</span></span>

<span data-ttu-id="83f96-133">應用程式會執行 [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) 介面，以回應豐富編輯控制項所執行的 OLE 相關查詢或動作。</span><span class="sxs-lookup"><span data-stu-id="83f96-133">Applications implement the [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) interface to respond to OLE-related queries or actions that are performed by a rich edit control.</span></span> <span data-ttu-id="83f96-134">您可以藉由傳送 [**EM \_ SETOLECALLBACK**](em-setolecallback.md) 訊息，將介面的執行與控制項產生關聯。</span><span class="sxs-lookup"><span data-stu-id="83f96-134">You associate your implementation of the interface with the control by sending an [**EM\_SETOLECALLBACK**](em-setolecallback.md) message.</span></span> <span data-ttu-id="83f96-135">控制項接著會適當地在您的介面執行上呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="83f96-135">The control then calls methods on your implementation of the interface as appropriate.</span></span>

<span data-ttu-id="83f96-136">例如，當使用者嘗試將物件拖曳或貼到控制項時，會呼叫 [**QueryAcceptData**](/windows/desktop/api/Richole/nf-richole-iricheditolecallback-queryacceptdata) 。</span><span class="sxs-lookup"><span data-stu-id="83f96-136">For example, [**QueryAcceptData**](/windows/desktop/api/Richole/nf-richole-iricheditolecallback-queryacceptdata) is called when the user attempts to drag or paste an object into the control.</span></span> <span data-ttu-id="83f96-137">如果您的應用程式可以接受資料，您的方法的執行會傳回 S \_ OK，否則會傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="83f96-137">If your application can accept the data, your implementation of the method returns S\_OK; otherwise, it returns an error code.</span></span> <span data-ttu-id="83f96-138">方法可能也會採取其他動作，例如警告使用者該類型的檔案不能放在控制項中。</span><span class="sxs-lookup"><span data-stu-id="83f96-138">The method might also take some other action, such as warning the user that files of that type cannot be placed in the control.</span></span>

## <a name="complete-insertobject-example-function"></a><span data-ttu-id="83f96-139">Complete InsertObject 範例函式</span><span class="sxs-lookup"><span data-stu-id="83f96-139">Complete InsertObject Example Function</span></span>

<span data-ttu-id="83f96-140">下列程式碼範例示範如何將先前的程式碼片段合併為一個包含錯誤處理的完整函式。</span><span class="sxs-lookup"><span data-stu-id="83f96-140">The following code example demonstrates the previous code snippets combined into one complete function that includes error handling.</span></span>


```C++
BOOL InsertObject(HWND hRichEdit, LPCTSTR pszFileName)
{
    HRESULT hr;

    LPRICHEDITOLE pRichEditOle;
    SendMessage(hRichEdit, EM_GETOLEINTERFACE, 0, (LPARAM)&pRichEditOle);

    if (pRichEditOle == NULL)
    {
        return FALSE;
    }

    LPLOCKBYTES pLockBytes = NULL;
    hr = CreateILockBytesOnHGlobal(NULL, TRUE, &pLockBytes);

    if (FAILED(hr))
    {
        return FALSE;
    }

    LPSTORAGE pStorage;
    hr = StgCreateDocfileOnILockBytes(pLockBytes, 
           STGM_SHARE_EXCLUSIVE | STGM_CREATE | STGM_READWRITE, 
           0, &pStorage);

    if (FAILED(hr))
    {
        return FALSE;
    }

    FORMATETC formatEtc;
    formatEtc.cfFormat = 0;
    formatEtc.ptd = NULL;
    formatEtc.dwAspect = DVASPECT_CONTENT;
    formatEtc.lindex = -1;
    formatEtc.tymed = TYMED_NULL;

    LPOLECLIENTSITE pClientSite;
    hr = pRichEditOle->GetClientSite(&pClientSite);

    if (FAILED(hr))
    {
        return FALSE;
    }

    LPUNKNOWN pUnk;
    CLSID clsid = CLSID_NULL;

    hr = OleCreateFromFile(clsid, pszFileName, IID_IUnknown, OLERENDER_DRAW, 
           &formatEtc, pClientSite, pStorage, (void**)&pUnk);

    pClientSite->Release();

    if (FAILED(hr))
    {
        return FALSE;
    }

    LPOLEOBJECT pObject;
    hr = pUnk->QueryInterface(IID_IOleObject, (void**)&pObject);
    pUnk->Release();

    if (FAILED(hr))
    {
        return FALSE;
    }

    OleSetContainedObject(pObject, TRUE);
    REOBJECT reobject = { sizeof(REOBJECT)};
    hr = pObject->GetUserClassID(&clsid);

    if (FAILED(hr))
    {
        pObject->Release();
        return FALSE;
    }

    reobject.clsid = clsid;
    reobject.cp = REO_CP_SELECTION;
    reobject.dvaspect = DVASPECT_CONTENT;
    reobject.dwFlags = REO_RESIZABLE | REO_BELOWBASELINE;
    reobject.dwUser = 0;
    reobject.poleobj = pObject;
    reobject.polesite = pClientSite;
    reobject.pstg = pStorage;
    SIZEL sizel = { 0 };
    reobject.sizel = sizel;

    SendMessage(hRichEdit, EM_SETSEL, 0, -1);
    DWORD dwStart, dwEnd;
    SendMessage(hRichEdit, EM_GETSEL, (WPARAM)&dwStart, (LPARAM)&dwEnd);
    SendMessage(hRichEdit, EM_SETSEL, dwEnd+1, dwEnd+1);
    SendMessage(hRichEdit, EM_REPLACESEL, TRUE, (WPARAM)L"\n"); 

    hr = pRichEditOle->InsertObject(&reobject);
    pObject->Release();
    pRichEditOle->Release();

    if (FAILED(hr))
    {
        return FALSE;
    }
    
    return TRUE;
}
```



## <a name="related-topics"></a><span data-ttu-id="83f96-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="83f96-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83f96-142">使用 Rich Edit 控制項</span><span class="sxs-lookup"><span data-stu-id="83f96-142">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="83f96-143">[Windows 通用控制項示範 (CppWindowsCommonControls) ](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="83f96-143">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




