---
description: 下列範例程式碼示範如何建立自訂通訊協定處理常式的 Shell 擴充功能。
ms.assetid: 4b65ced8-8dc9-43f6-bfe1-3703aea3459f
title: 程式碼範例：通訊協定處理常式的 Shell 擴充功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e436f1d7ad746181be8cb3c43375abe3656c544b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973025"
---
# <a name="code-sample-shell-extensions-for-protocol-handlers"></a><span data-ttu-id="a1321-103">程式碼範例：通訊協定處理常式的 Shell 擴充功能</span><span class="sxs-lookup"><span data-stu-id="a1321-103">Code Sample: Shell Extensions for Protocol Handlers</span></span>

<span data-ttu-id="a1321-104">下列範例程式碼示範如何建立自訂通訊協定處理常式的 Shell 擴充功能。</span><span class="sxs-lookup"><span data-stu-id="a1321-104">The following sample code shows how to create Shell extensions for a custom protocol handler.</span></span>

## <a name="sample-code"></a><span data-ttu-id="a1321-105">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="a1321-105">Sample code</span></span>

> [!Note]
>
> <span data-ttu-id="a1321-106">**此程式碼和資訊是以「原樣」提供，不含任何明示或默示擔保，包括但不限於特定用途的適售性及/或適用性默示擔保。**</span><span class="sxs-lookup"><span data-stu-id="a1321-106">**THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A PARTICULAR PURPOSE.**</span></span>
>
> <span data-ttu-id="a1321-107">著作權 (c) Microsoft Corporation。</span><span class="sxs-lookup"><span data-stu-id="a1321-107">Copyright (c)Microsoft Corporation.</span></span> <span data-ttu-id="a1321-108">著作權所有，並保留一切權利。</span><span class="sxs-lookup"><span data-stu-id="a1321-108">All rights reserved.</span></span>

 


```
// ********************** IDL structure **********************

#include <pshpack1.h>

typedef struct
{
    WORD    cbSize;
    WORD    cchUrl;      // Store the length of the URL.
    WCHAR   pwszUrl[1];  // Store the URL.
} URLIDL;


#include <poppack.h>

class ATL_NO_VTABLE CSampleShellFolder :
    public CComTearOffObjectBase<CSampleSearchProtocol>,
    public IPersistFolder,
    public IShellFolder
{
public:
    DECLARE_PROTECT_FINAL_CONSTRUCT()

    BEGIN_COM_MAP(CSampleShellFolder)
        COM_INTERFACE_ENTRY(IPersistFolder)
        COM_INTERFACE_ENTRY(IShellFolder)
    END_COM_MAP()

    CSampleShellFolder();
    virtual ~CSampleShellFolder();
    HRESULT FinalConstruct() {return S_OK;};
    void FinalRelease() {};

    // IPersist
    STDMETHOD(GetClassID)(CLSID* pCLSID);

    // IPersistFolder
    STDMETHOD(Initialize)(const ITEMIDLIST* pidl);

    // IShellFolder
    STDMETHOD(ParseDisplayName)
 (HWND hwnd, IBindCtx* pbc, OLECHAR* pszName, 
ULONG* pchEaten, ITEMIDLIST** ppidl, ULONG* pdwAttributes);
    STDMETHOD(EnumObjects)
 (HWND hwnd, DWORD grfFlags, IEnumIDList** ppenmIDList);
    STDMETHOD(BindToObject)
(const ITEMIDLIST* pidl, IBindCtx* pbc, REFIID riid, void** ppvObj);
    STDMETHOD(BindToStorage)
(const ITEMIDLIST* pidl, IBindCtx* pbc, REFIID riid, void** ppvObj);
    STDMETHOD(CompareIDs)
(LPARAM lParam, const ITEMIDLIST* pidl1, const ITEMIDLIST* pidl2);
    STDMETHOD(CreateViewObject)
(HWND hwndOwner, REFIID riid, void** ppvObj) ;
    STDMETHOD(GetAttributesOf)
(UINT cidl, const ITEMIDLIST** ppidl, SFGAOF* prgfInOut);
    STDMETHOD(GetUIObjectOf)
(HWND hwndOwner, UINT cidl, const ITEMIDLIST** ppidl,
 REFIID riid, UINT* prgfInOut, void** ppvObj);
    STDMETHOD(GetDisplayNameOf)
(const ITEMIDLIST* pidl, DWORD dwFlags, STRRET* pstrName);
    STDMETHOD(SetNameOf)
(HWND hwnd, const ITEMIDLIST* pidl, const OLECHAR* pszName,
 DWORD dwFlags, ITEMIDLIST** ppidlOut);

// IDL Helper Routines
private:
    static HRESULT CreateIDL(CString & strUrl, ITEMIDLIST** ppidl);
    static SampleIDL *IsURLIDL(const ITEMIDLIST* pidl);
    static HRESULT GetUrlFromIDL (const ITEMIDLIST *pidl, CString & strUrl); 
};

// ******************* IDL Helper routines *******************

//------------------------------------------------------------
//  GetUrlFromIDL()
//
// Return the URL for the specified PIDL.
//------------------------------------------------------------

HRESULT CSampleShellFolder::GetUrlFromIDL(
      const ITEMIDL * pidl,
      CString &strUrl)
{
    if (IsURLIDL(pidl) == NULL)
        return E_FAIL;

    URLIDL *pURLIDL=(URLIDL *)pidl;
    strUrl.SetString(pURLIDL->pwszUrl,pURLIDL->cchUrl);
    return S_OK;
}

//------------------------------------------------------------
//  CreateIDL()
//
// Create a PIDL for the specified URL.
//------------------------------------------------------------

HRESULT CSampleShellFolder::CreateIDL(
      CString &strUrl, 
      ITEMIDL** ppidl)
{
    HRESULT hr = S_OK;

    // Check assertions.
    _ASSERTE(ppidl);

    // Initialize the return value.
    *ppidl = NULL;

    // Get the size of the URL
    WORD cb;
    WORD cbUrl = strUrl.GetLength() * sizeof(WCHAR);
    cb = (WORD)sizeof(URLIDL) + cbUrl;

    // Allocate an additional WORD, which is the "next"
    // PIDL (one of cb==0).
    URLIDL* pURLIDL = (URLIDL*)LocalAlloc(LPTR, cb + sizeof(WORD));
    hr = (pURLIDL ? S_OK : E_FAIL);
    if (SUCCEEDED(hr))
    {
        pURLIDL->cbSize = cb;
        // Store the number of characters in the URL.
        pURLIDL->cchUrl = (WORD)strUrl.GetLength(); 

        // NOTE: CopyChars copies the exact number of characters
        // *including* the terminating null character.

        CString::CopyChars(
                  pURLIDL->pwszUrl, 
                  (LPCTSTR)strUrl, 
                  strUrl.GetLength() + 1);

        // Terminate the IDL.
        ITEMIDL *pidlNext = (ITEMIDL *)
                  (((LPBYTE)pURLIDL) + pURLIDL->cbSize);
        *((WORD *)pidlNext) = 0;

        // Return a clone of the IDL.
        *ppidl = ILClone((ITEMIDL*)pURLIDL);
        hr = (*ppidl ? S_OK : E_OUTOFMEMORY);

        // Free the IDL.
        LocalFree((HLOCAL)pURLIDL);
    }

    return hr;
}

//------------------------------------------------------------
//  IsURLIDL()
//
// Check the validity of a PIDL, returning a pointer to the
// URLIDL portion of the PIDL.
//------------------------------------------------------------

URLIDL *CSampleShellFolder::IsURLIDL(const ITEMIDL* pidl)
{
    URLIDL * pURLIDL = NULL;
    CString strSample = L"sample:";
    
    // Check for the presence and length of a PIDL.
    // If the PIDL is present and of sufficient length,
    // compare it to the start URL.
    if (pidl && 
        (ILGetSize(pidl) > strSample.GetLength()*sizeof(WCHAR)) )
    {
        pURLIDL = (URLIDL *)pidl;
        CString strUrl;
        strUrl.SetString(pURLIDL->pwszUrl, 7);
        if (strUrl.CompareNoCase(strSample) == 0)
        {
            return pURLIDL;
        }
    }

    return NULL;
}

// ************************ IPersist *************************
//------------------------------------------------------------
// IPersist::GetClassID
//
// Retrieve the class identifier (CLSID) of an object. The
// CLSID is a unique value that identifies the code that can
// manipulate the persistent data.
//------------------------------------------------------------
STDMETHODIMP CSampleShellFolder::GetClassID(CLSID* pCLSID)
{
    if (pCLSID == NULL)
        return E_POINTER;

    *pCLSID = CLSID_SampleProtocol;
    return S_OK;
}

// ********************* IPersistFolder **********************

//------------------------------------------------------------
// IPersistFolder::Initialize
//
// Instruct a ShellFolder object to initialize itself based
// on the information provided. 
//------------------------------------------------------------

STDMETHODIMP CSampleShellFolder::Initialize(const ITEMIDL* pidl)
{
    // Since we have only one folder in this sample, there
    // is nothing to store.
    return S_OK;
}

// ******************** IShellFolder *************************

//------------------------------------------------------------
// IShellFolder::ParseDisplayName
//
// Translate a file object's display name or a folder's
// display name into an item identifier list.
//------------------------------------------------------------

STDMETHODIMP CSampleShellFolder::ParseDisplayName(
      HWND hwnd, IBindCtx* pbc,
      OLECHAR* pszName,
      ULONG* pchEaten,
      ITEMIDL** ppidl,
      ULONG* pdwAttributes)
{
    HRESULT hr = E_FAIL;

    if ((pszName == NULL) || (ppidl == NULL))
        return E_POINTER;

    *ppidl = NULL;

    CString strName = L"";
    
    // Get the first seven bytes of the name.
    strName.SetString(pszName, 7);
    
    // Determine whether the name starts with "outlook",
    // the first seven characters of outlookexpress.
    if (strName.CompareNoCase(L"sample:") == 0)
    {

        // If TRUE, we can assume this is an outlookexpress URL.
        CString strUrl = pszName;

        // Create the PIDL.
        hr = CSampleShellFolder::CreateURLIDL(strUrl, ppidl);

        if (SUCCEEDED(hr))
        {
            if (pchEaten != NULL)
                *pchEaten = strUrl.GetLength();

            if (pdwAttributes != NULL)
                *pdwAttributes = 0;
        }
    }
    return hr;
}

//------------------------------------------------------------
// IShellFolder::EnumObjects
//
// Enable a client to determine the contents of a folder by
// creating an item identifier enumeration object and returning
// its IEnumIDL interface. The methods supported by that
// interface can then be used to enumerate the folder's contents.
//------------------------------------------------------------

STDMETHODIMP CSampleShellFolder::EnumObjects(
      HWND hwnd,
      DWORD grfFlags,
      IEnumIDL** ppenmIDL)
{
    return E_NOTIMPL;
}

//------------------------------------------------------------
// IShellFolder::BindToObject
//
// Retrieve an IShellFolder object for a subfolder.
//------------------------------------------------------------

STDMETHODIMP CSampleShellFolder::BindToObject(
      const ITEMIDL* pidl,
      IBindCtx* pbc,
      REFIID riid, void** ppvObj)
{
    return E_NOTIMPL;
}

//------------------------------------------------------------
// IShellFolder::BindToStorage
//
// Request a pointer to an object's storage interface.
//------------------------------------------------------------

STDMETHODIMP CSampleShellFolder::BindToStorage(
      const ITEMIDL* pidl,
      IBindCtx* pbc,
      REFIID riid, void** ppvObj)
{
    // NOTE: Although this code is not implemented in the sample, 
    // it is possible to bind to IUrlAccessor->BindToStream()
    // to bind to the storage.
    return E_NOTIMPL;
}

//------------------------------------------------------------
// IShellFolder::CompareIDs
//
// Determine the relative order of two file objects or folders,
// given their item identifier lists.
//------------------------------------------------------------

STDMETHODIMP CSampleShellFolder::CompareIDs(
      LPARAM lParam,
      const ITEMIDL* pidl1,
      const ITEMIDL* pidl2)
{
    if ((pidl1 == NULL) || (pidl2 == NULL))
        return E_POINTER;

    // Ensure that these are our PIDLs
    URLIDL * pURLIDL1 = IsURLIDL(pidl1);
    URLIDL * pURLIDL2 = IsURLIDL(pidl2);
    if (!pURLIDL1 || !pURLIDL2)
    {
        return S_FALSE;
    }

    // Check the query for equality
    CString strUrl1;
    CString strUrl2;
    strUrl1.SetString(pURLIDL1->pwszUrl, pURLIDL1->cchUrl);
    strUrl2.SetString(pURLIDL2->pwszUrl, pURLIDL2->cchUrl);
    return (strUrl1.CompareNoCase(strUrl2));
}

//------------------------------------------------------------
// IShellFolder::CreateViewObject
//
// Request an object that can be used to obtain information
// from or interact with a folder object.
//------------------------------------------------------------

STDMETHODIMP CSampleShellFolder::CreateViewObject(
      HWND hwndOwner,
      REFIID riid,
      void** ppvObj)
{
    return E_NOTIMPL;
}

//------------------------------------------------------------
// IShellFolder::GetAttributesOf
//
// Retrieve the attributes of one or more file objects or
// subfolders.
//------------------------------------------------------------

STDMETHODIMP CSampleShellFolder::GetAttributesOf(
      UINT cidl,
      const ITEMIDL** ppidl,
      SFGAOF* prgfInOut)
{
    for ( UINT i = 0; i < cidl; i++)
    {
        DWORD dwAttrs = 0;
            
        // SFGAO_FOLDER | SFGAO_CANLINK;
        dwAttrs |= SFGAO_NONENUMERATED|SFGAO_READONLY; 

        *prgfInOut &= dwAttrs;
    }
    return S_OK;
}

//------------------------------------------------------------
// IShellFolder::GetUIObjectOf
//
// Retrieve an OLE interface that can be used to carry out
// actions on the specified file objects or folders.
//------------------------------------------------------------

STDMETHODIMP CSampleShellFolder::GetUIObjectOf(
      HWND hwndOwner, 
      UINT cidl, 
      const ITEMIDL** ppidl, 
      REFIID riid, 
      UINT* prgfInOut, 
      void** ppvObj)
{
    if ((ppidl == NULL) || (ppvObj == NULL))
        return E_POINTER;

    *ppvObj = NULL;

    // Create the appropriate object.
    HRESULT hr=S_OK;

    // By design, we handle only one object at a time.
    if (cidl > 1)
        return E_INVALIDARG;

    CString strUrl;
    hr = GetUrlFromIDL(*ppidl, strUrl);

    if (SUCCEEDED(hr))
    {
         if (riid == __uuidof(IContextMenu))
         {
                // Return the IContextMenu for this URL
          }
         else
         if (riid == __uuidof(IExtractIcon))
         {
                // Return the IExtractIcon for this URL
         }
         else
             Hr = E_NOINTERFACE;        
    }
    return hr;
}

//------------------------------------------------------------
// IShellFolder::GetDisplayNameOf
//
// Retrieve the display name for the specified file object
// or subfolder.
//------------------------------------------------------------

STDMETHODIMP CSampleShellFolder::GetDisplayNameOf(
      const ITEMIDL* pidl,
      DWORD dwFlags, 
      STRRET* pstrName)
{
    HRESULT hr = S_OK;
    URLIDL * pURLIDL = IsURLIDL(pidl);

    if (pURLIDL)
    {
        pstrName->uType = STRRET_OFFSET;
        pstrName->uOffset = sizeof(WORD) + sizeof(WORD);
    }
    return hr;
}

//------------------------------------------------------------
// IShellFolder::SetNameOf
//
// Set the display name of a file object or subfolder,
// changing the item identifier in the process.
//------------------------------------------------------------

STDMETHODIMP CSampleShellFolder::SetNameOf(
      HWND hwnd,
      const ITEMIDL* pidl,
      const OLECHAR* pszName, 
      DWORD dwFlags, 
      ITEMIDL** ppidlOut)
{
    return E_NOTIMPL;
}
        
```



## <a name="additional-resources"></a><span data-ttu-id="a1321-109">其他資源</span><span class="sxs-lookup"><span data-stu-id="a1321-109">Additional Resources</span></span>

-   <span data-ttu-id="a1321-110">如需搜尋程式碼範例，請參閱 [WINDOWS SEARCH SDK 範例](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8)。</span><span class="sxs-lookup"><span data-stu-id="a1321-110">For Search code samples, see [Windows Search SDK Samples](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8).</span></span>
-   <span data-ttu-id="a1321-111">針對 Shell 程式碼範例，請參閱 [SHELL SDK 範例](/previous-versions/windows/desktop/legacy/dd940376(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="a1321-111">For Shell code samples, see [Shell SDK Samples](/previous-versions/windows/desktop/legacy/dd940376(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a1321-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="a1321-112">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="a1321-113">**概念**</span><span class="sxs-lookup"><span data-stu-id="a1321-113">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a1321-114">開發通訊協定處理常式</span><span class="sxs-lookup"><span data-stu-id="a1321-114">Developing Protocol Handlers</span></span>](-search-3x-wds-phaddins.md)
</dt> <dt>

[<span data-ttu-id="a1321-115">瞭解通訊協定處理常式</span><span class="sxs-lookup"><span data-stu-id="a1321-115">Understanding Protocol Handlers</span></span>](-search-3x-wds-extidx-prot-implementing.md)
</dt> <dt>

[<span data-ttu-id="a1321-116">通知索引變更</span><span class="sxs-lookup"><span data-stu-id="a1321-116">Notifying the Index of Changes</span></span>](-search-3x-wds-notifyingofchanges.md)
</dt> <dt>

[<span data-ttu-id="a1321-117">新增圖示和快顯功能表</span><span class="sxs-lookup"><span data-stu-id="a1321-117">Adding Icons and Context Menus</span></span>](-search-3x-wds-ph-ui-extensions.md)
</dt> <dt>

[<span data-ttu-id="a1321-118">安裝和註冊通訊協定處理常式</span><span class="sxs-lookup"><span data-stu-id="a1321-118">Installing and Registering Protocol Handlers</span></span>](-search-3x-wds-ph-install-registration.md)
</dt> <dt>

[<span data-ttu-id="a1321-119">建立通訊協定處理常式的搜尋連接器</span><span class="sxs-lookup"><span data-stu-id="a1321-119">Creating a Search Connector for a Protocol Handler</span></span>](-search-3x-wds-ph-search-connector.md)
</dt> <dt>

[<span data-ttu-id="a1321-120">偵錯工具通訊協定處理常式</span><span class="sxs-lookup"><span data-stu-id="a1321-120">Debugging Protocol Handlers</span></span>](-search-ws-protocolhandlertesting.md)
</dt> </dl>

 

 
