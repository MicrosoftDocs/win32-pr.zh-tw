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
# <a name="how-to-use-ole-in-rich-edit-controls"></a>如何在 Rich Edit 控制項中使用 OLE

本章節包含在 rich edit 控制項中使用物件連結和內嵌 (OLE) 的相關資訊。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows 控制項](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows 消費者介面程式設計

## <a name="instructions"></a>指示

### <a name="use-a-rich-edit-interface"></a>使用 Rich Edit 介面

Rich edit 控制項會透過元件物件模型 (COM) 介面來公開部分功能。 藉由從控制項取得介面，您就能夠在控制項內使用其他物件。 您可以藉由傳送 [**EM \_ GETOLEINTERFACE**](em-getoleinterface.md) 訊息來取得這個介面。 您可以從 [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) 介面取得用於 [Text 物件模型](text-object-model.md)中的介面。

當應用程式與物件互動時，應用程式會執行另一個介面 [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback)來定義控制項的行為。

### <a name="insert-an-object-into-a-rich-edit-control"></a>將物件插入至 Rich Edit 控制項

下列程式碼範例會將檔案物件插入至 rich edit 控制項。 如果程式與使用者電腦上的檔案類型相關聯 (例如，Microsoft Excel 的 .xls 檔案) ，則檔案的內容會顯示在控制項中;否則，就會出現圖示。

1.  取得 [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) 介面。

    ```
    BOOL InsertObject(HWND hRichEdit, LPCTSTR pszFileName)
    {
        HRESULT hr;

        LPRICHEDITOLE pRichEditOle;
        SendMessage(hRichEdit, EM_GETOLEINTERFACE, 0, (LPARAM)&pRichEditOle);
        
        ...
    ```

    

2.  建立結構化儲存體。

    ```
        LPLOCKBYTES pLockBytes = NULL;
        hr = CreateILockBytesOnHGlobal(NULL, TRUE, &pLockBytes);
        
        LPSTORAGE pStorage;
        hr = StgCreateDocfileOnILockBytes(pLockBytes, 
                                          STGM_SHARE_EXCLUSIVE | STGM_CREATE | STGM_READWRITE, 
                                          0, &pStorage);
        ...
    ```

    

3.  設定資料格式。

    ```
        FORMATETC formatEtc;
        
        formatEtc.cfFormat = 0;
        formatEtc.ptd      = NULL;
        formatEtc.dwAspect = DVASPECT_CONTENT;
        formatEtc.lindex   = -1;
        formatEtc.tymed    = TYMED_NULL;
        
        ...
    ```

    

4.  取得顯示位置的指標。

    ```
        LPOLECLIENTSITE pClientSite;
        hr = pRichEditOle->GetClientSite(&pClientSite);
        
        ...
    ```

    

5.  建立物件並取出其 **IUnknown** 介面。

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

    

6.  取得物件的 IOleObject 介面。

    ```
        LPOLEOBJECT pObject;
        
        hr = pUnk->QueryInterface(IID_IOleObject, (void**)&pObject);
        
        pUnk->Release();

        ...
    ```

    

7.  若要確定已正確計算參考，請通知物件包含它。

    ```
        OleSetContainedObject(pObject, TRUE);

        ...
    ```

    

8.  設定物件資訊。

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

    

9.  將插入號移至文字的結尾，並加入換行字元。

    ```
        SendMessage(hRichEdit, EM_SETSEL, 0, -1);
        
        DWORD dwStart, dwEnd;
        
        SendMessage(hRichEdit, EM_GETSEL, (WPARAM)&dwStart, (LPARAM)&dwEnd);
        SendMessage(hRichEdit, EM_SETSEL, dwEnd+1, dwEnd+1);
        SendMessage(hRichEdit, EM_REPLACESEL, TRUE, (WPARAM)L"\n"); 

        ...
    ```

    

10. 插入物件。

    ```
        hr = pRichEditOle->InsertObject(&reobject);

        ...
    ```

    

11. 清除。

    ```
        pObject->Release();
        
        pRichEditOle->Release();

        return TRUE;
        
    }
    ```

    

### <a name="using-iricheditolecallback"></a>使用 IRichEditOleCallback

應用程式會執行 [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) 介面，以回應豐富編輯控制項所執行的 OLE 相關查詢或動作。 您可以藉由傳送 [**EM \_ SETOLECALLBACK**](em-setolecallback.md) 訊息，將介面的執行與控制項產生關聯。 控制項接著會適當地在您的介面執行上呼叫方法。

例如，當使用者嘗試將物件拖曳或貼到控制項時，會呼叫 [**QueryAcceptData**](/windows/desktop/api/Richole/nf-richole-iricheditolecallback-queryacceptdata) 。 如果您的應用程式可以接受資料，您的方法的執行會傳回 S \_ OK，否則會傳回錯誤碼。 方法可能也會採取其他動作，例如警告使用者該類型的檔案不能放在控制項中。

## <a name="complete-insertobject-example-function"></a>Complete InsertObject 範例函式

下列程式碼範例示範如何將先前的程式碼片段合併為一個包含錯誤處理的完整函式。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 Rich Edit 控制項](using-rich-edit-controls.md)
</dt> <dt>

[Windows 通用控制項示範 (CppWindowsCommonControls) ](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




