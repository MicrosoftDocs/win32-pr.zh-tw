---
title: 執行內容功能表 COM 物件的範例程式碼
description: 下列程式碼範例可用來執行 Active Directory 內容功能表延伸模組。 單一內容功能表項目會顯示訊息方塊，其中包含所選取之每個專案的 ADsPath。
ms.assetid: dc8f2c31-6031-4c7d-a173-5cedcedbfb26
ms.tgt_platform: multiple
keywords:
- Active Directory AD、範例程式碼 C/c + +、內容功能表 COM 物件的執行
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e69be602e5a1d62eca495e682a68ccfe80d31483df71d7c8ee7349c359bedd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118018239"
---
# <a name="example-code-for-implementation-of-the-context-menu-com-object"></a>執行內容功能表 COM 物件的範例程式碼

下列程式碼範例可用來執行 Active Directory 內容功能表延伸模組。 單一內容功能表項目會顯示訊息方塊，其中包含所選取之每個專案的 ADsPath。

## <a name="ishellextinit-implementation"></a>IShellExtInit 執行

下列程式碼範例可以用來執行 [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) 方法。


```C++
///////////////////////////////////////////////////////////////////////////
//
// IShellExtInit Implementation
//

/**************************************************************************

   CContMenuExt::Initialize()

**************************************************************************/

STDMETHODIMP CContMenuExt::Initialize(  LPCITEMIDLIST pidlFolder,
                                        LPDATAOBJECT pDataObj,
                                        HKEY  hKeyProgId)
{
    STGMEDIUM   stm;
    FORMATETC   fe;
    HRESULT     hr;

    if(NULL == pDataObj)
    {
        return E_INVALIDARG;
    }

    fe.cfFormat = RegisterClipboardFormat(CFSTR_DSOBJECTNAMES);
    fe.ptd = NULL;
    fe.dwAspect = DVASPECT_CONTENT;
    fe.lindex = -1;
    fe.tymed = TYMED_HGLOBAL;
    hr = pDataObj->GetData(&fe, &stm);
    if(SUCCEEDED(hr))
    {
        LPDSOBJECTNAMES pdson = (LPDSOBJECTNAMES)GlobalLock(stm.hGlobal);

        if(pdson)
        {
            DWORD   dwBytes = GlobalSize(stm.hGlobal);

            m_pObjectNames = (DSOBJECTNAMES*)GlobalAlloc(GPTR, dwBytes);
            if(m_pObjectNames)
            {
                CopyMemory(m_pObjectNames, pdson, dwBytes);
            }
            
            GlobalUnlock(stm.hGlobal);
        }
        
        ReleaseStgMedium(&stm);
    }

    fe.cfFormat = RegisterClipboardFormat(CFSTR_DS_DISPLAY_SPEC_OPTIONS);
    fe.ptd = NULL;
    fe.dwAspect = DVASPECT_CONTENT;
    fe.lindex = -1;
    fe.tymed = TYMED_HGLOBAL;
    hr = pDataObj->GetData(&fe, &stm);
    if(SUCCEEDED(hr))
    {
        PDSDISPLAYSPECOPTIONS   pdso;
        
        pdso = (PDSDISPLAYSPECOPTIONS)GlobalLock(stm.hGlobal);
        if(pdso)
        {
            DWORD   dwBytes = GlobalSize(stm.hGlobal);

            m_pDispSpecOpts = (PDSDISPLAYSPECOPTIONS)GlobalAlloc(GPTR, dwBytes);
            if(m_pDispSpecOpts)
            {
                CopyMemory(m_pDispSpecOpts, pdso, dwBytes);
            }
            
            GlobalUnlock(stm.hGlobal);
        }

        ReleaseStgMedium(&stm);
    }

    return hr;
}

```



## <a name="icontextmenu-implementation"></a>ICoNtextMenu 執行

下列程式碼範例可以用來執行 [**ICoNtextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) 方法。


```C++
///////////////////////////////////////////////////////////////////////////
//
// IContextMenu Implementation
//

/**************************************************************************

   CContMenuExt::QueryContextMenu()

**************************************************************************/

STDMETHODIMP CContMenuExt::QueryContextMenu(    HMENU hMenu,
                                                UINT indexMenu,
                                                UINT idCmdFirst,
                                                UINT idCmdLast,
                                                UINT uFlags)
{
    if(m_pObjectNames && !(CMF_DEFAULTONLY & uFlags))
    {
        InsertMenu( hMenu, 
                    indexMenu, 
                    MF_STRING | MF_BYPOSITION, 
                    idCmdFirst + IDM_CONTMENU, 
                    TEXT("AD Sample Context Menu"));

        return MAKE_HRESULT(SEVERITY_SUCCESS, 0, USHORT(IDM_CONTMENU + 1));
    }

    return MAKE_HRESULT(SEVERITY_SUCCESS, 0, USHORT(0));
}

/**************************************************************************

   CContMenuExt::InvokeCommand()

**************************************************************************/

STDMETHODIMP CContMenuExt::InvokeCommand(LPCMINVOKECOMMANDINFO lpcmi)
{
    if(LOWORD(lpcmi->lpVerb) > IDM_CONTMENU)
    {
        return E_INVALIDARG;
    }

    switch (LOWORD(lpcmi->lpVerb))
    {
    case IDM_CONTMENU:
        {
            LPWSTR  pwszName;
            DWORD   dwBytes;
            UINT    i;

            for(i = 0, dwBytes = 0; i < m_pObjectNames->cItems; i++)
            {
                pwszName = (LPWSTR)((LPBYTE)m_pObjectNames + m_pObjectNames->aObjects[i].offsetName);
                dwBytes += (lstrlenW(pwszName) + 2) * sizeof(WCHAR);
            }

            LPWSTR  pwszText = (LPWSTR)GlobalAlloc(GPTR, dwBytes);

            if(pwszText)
            {
                pwszText[0] = 0;
                for(i = 0; i < m_pObjectNames->cItems; i++)
                {
                    pwszName = (LPWSTR)((LPBYTE)m_pObjectNames + m_pObjectNames->aObjects[i].offsetName);
                    wcscat_s(pwszText, pwszName);
                    wcscat_s(pwszText, L"\n");
                }
                
                MessageBoxW(lpcmi->hwnd, 
                            pwszText, 
                            L"Sample Command", 
                            MB_OK | MB_ICONINFORMATION);

                GlobalFree(pwszText);
            }
        }
        break;
    }

    return NOERROR;
}

/**************************************************************************

   CContMenuExt::GetCommandString()

**************************************************************************/

STDMETHODIMP CContMenuExt::GetCommandString(    UINT idCommand,
                                                UINT uFlags,
                                                LPUINT lpReserved,
                                                LPSTR lpszName,
                                                UINT uMaxNameLen)
{
    HRESULT hr = E_INVALIDARG;
    TCHAR   szHelp[] = TEXT("Sample Context Menu Command");
    TCHAR   szVerb[] = TEXT("adcontmenu");

    switch(uFlags)
    {
    case GCS_HELPTEXTA:
        switch(idCommand)
        {
        case IDM_CONTMENU:
            LocalToAnsi((LPSTR)lpszName, szHelp, uMaxNameLen);
            hr = S_OK;
            break;
         }
        break;
   
    case GCS_HELPTEXTW:
        switch(idCommand)
        {
        case IDM_CONTMENU:
            LocalToWideChar((LPWSTR)lpszName, szHelp, uMaxNameLen);
            hr = S_OK;
            break;
         }
        break;
   
    case GCS_VERBA:
        switch(idCommand)
        {
        case IDM_CONTMENU:
            LocalToAnsi((LPSTR)lpszName, szVerb, uMaxNameLen);
            hr = S_OK;
            break;
        }
        break;
   
    case GCS_VERBW:
        switch(idCommand)
        {
        case IDM_CONTMENU:
            LocalToWideChar((LPWSTR)lpszName, szVerb, uMaxNameLen);
            hr = S_OK;
            break;
        }
        break;
   
    case GCS_VALIDATE:
        hr = S_OK;
        break;
    }

    return hr;
}

```



 

 