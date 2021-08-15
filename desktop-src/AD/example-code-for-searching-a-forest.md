---
title: 搜尋樹系的範例程式碼
description: 本主題包含搜尋樹系的範例程式碼。
ms.assetid: 56740e95-548a-4e84-ab2e-2bb7a51b7e1e
ms.tgt_platform: multiple
keywords:
- 搜尋樹系的 Active Directory 範例 Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c92c71afeecebf96ba123e909ad408835de083b8d45cb259a7b371b8214cc5b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118190285"
---
# <a name="example-code-for-searching-a-forest"></a>搜尋樹系的範例程式碼

本主題包含搜尋樹系的範例程式碼。

下列 C/c + + 程式碼範例會系結至通用類別目錄的根目錄，並列舉單一物件（樹系的根目錄），以便用來搜尋整個樹系。


```C++
Set gc = GetObject("GC:")
For each child in gc
    Set entpr = child
Next
' Now entpr is an object that can be used
' to search the entire forest.
```



下列 C/c + + 程式碼範例包含一個函式，該函式會傳回用來搜尋整個樹系的 [**>idirectorysearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) 指標。

此函式會執行無伺服器系結至通用類別目錄的根目錄、列舉單一專案，也就是樹系的根目錄，並且可以用來搜尋整個樹系，呼叫 [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 以取得物件的 [**>idirectorysearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) 指標，並傳回該指標供呼叫端用來搜尋樹系。


```C++
HRESULT GetGC(IDirectorySearch **ppDS)
{
HRESULT hr;
IEnumVARIANT *pEnum = NULL;
IADsContainer *pCont = NULL;
VARIANT var;
IDispatch *pDisp = NULL;
ULONG lFetch;
 
// Set IDirectorySearch pointer to NULL.
*ppDS = NULL;
 
// First, bind to the GC: namespace container object. 
hr = ADsOpenObject(TEXT("GC:"),
                NULL,
                NULL,
                ADS_SECURE_AUTHENTICATION, // Use Secure Authentication.
                IID_IADsContainer,
                (void**)&pCont);
if (FAILED(hr)) {
    _tprintf(TEXT("ADsOpenObject failed: 0x%x\n"), hr);
    goto cleanup;
} 
 
// Get an enumeration interface for the GC container to enumerate the 
// contents. The actual GC is the only child of the GC container.
hr = ADsBuildEnumerator(pCont, &pEnum);
if (FAILED(hr)) {
    _tprintf(TEXT("ADsBuildEnumerator failed: 0x%x\n"), hr);
    goto cleanup;
} 
 
// Now enumerate. There is only one child of the GC: object.
hr = pEnum->Next(1, &var, &lFetch);
if (FAILED(hr)) {
    _tprintf(TEXT("ADsEnumerateNext failed: 0x%x\n"), hr);
    goto cleanup;
} 
 
// Get the IDirectorySearch pointer.
if (( hr == S_OK ) && ( lFetch == 1 ) )     
{    
    pDisp = V_DISPATCH(&var);
    hr = pDisp->QueryInterface( IID_IDirectorySearch, (void**)ppDS); 
}
 
cleanup:
 
if (pEnum)
    ADsFreeEnumerator(pEnum);
if (pCont)
    pCont->Release();
if (pDisp)
    (pDisp)->Release();
return hr;
}
```



 

 