---
title: 更新架構快取的範例程式碼
description: 下列 C/c + + 函式會取得架構主機 (GetSchemaMasterDNSName) 的 DNS 名稱，並更新架構主機 (UpdateSchemaMasterCache) 的架構快取。
ms.assetid: e955588d-a92c-4406-a197-bb8c36329f88
ms.tgt_platform: multiple
keywords:
- 用來更新架構快取 AD 的範例程式碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c9ebbf721bc8d3e960b02de14ac7f9179bf5787
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020848"
---
# <a name="example-code-for-updating-the-schema-cache"></a><span data-ttu-id="59b3b-104">更新架構快取的範例程式碼</span><span class="sxs-lookup"><span data-stu-id="59b3b-104">Example Code for Updating the Schema Cache</span></span>

<span data-ttu-id="59b3b-105">下列 C/c + + 函式會取得架構主機 (GetSchemaMasterDNSName) 的 DNS 名稱，並更新架構主機 (UpdateSchemaMasterCache) 的架構快取。</span><span class="sxs-lookup"><span data-stu-id="59b3b-105">The following C/C++ functions get the DNS name of the schema master (GetSchemaMasterDNSName) and update the schema cache at the schema master (UpdateSchemaMasterCache).</span></span> <span data-ttu-id="59b3b-106">若要使用這些函式，請呼叫 GetSchemaMasterDNSName 來取得架構主機 DNS 名稱，將架構主要 DNS 名稱傳遞給 UpdateSchemaMasterCache，並在包含架構主機 DNS 名稱的字串上呼叫 CoTaskMemFree。</span><span class="sxs-lookup"><span data-stu-id="59b3b-106">To use these functions, call GetSchemaMasterDNSName to get the schema master DNS name, pass the schema master DNS name to UpdateSchemaMasterCache, call CoTaskMemFree on string containing the schema master DNS name.</span></span>

<span data-ttu-id="59b3b-107">如需詳細資訊，請參閱 [更新架構](updating-the-schema-cache.md)快取。</span><span class="sxs-lookup"><span data-stu-id="59b3b-107">For more information, see [Updating the Schema Cache](updating-the-schema-cache.md).</span></span>


```C++
HRESULT UpdateSchemaMasterCache(LPOLESTR szSchemaMasterDNSName)
{
if (!szSchemaMasterDNSName)
   return E_POINTER;
HRESULT hr = E_FAIL;
IADs *pObject = NULL;
VARIANT var;
LPOLESTR szPath = new OLECHAR[MAX_PATH];
wcscpy_s(szPath,L"LDAP://");
wcscat_s(szPath,szSchemaMasterDNSName);
wcscat_s(szPath,L"/rootDSE");
hr = ADsOpenObject(szPath,
         NULL,
         NULL,
         ADS_SECURE_AUTHENTICATION, // Use Secure Authentication.
         IID_IADs,
         (void**)&pObject);
if (SUCCEEDED(hr))
{
  VariantInit(&var);
  var.vt = VT_I4;
  var.lVal = 1L;
  hr = pObject->Put(CComBSTR("schemaUpdateNow"), var);
  if (SUCCEEDED(hr))
  {
    hr = pObject->SetInfo();
    if (SUCCEEDED(hr))
      MessageBox(NULL,L"Updated",L"Extend Schema Wizard",MB_OK|MB_ICONEXCLAMATION);
    else
      MessageBox(NULL,L"Update Failed",L"Extend Schema Wizard",MB_OK|MB_ICONEXCLAMATION);
  }
}
if (pObject)
  pObject->Release();
 
return hr;
}
 
HRESULT GetSchemaMasterDNSName(LPOLESTR *pszSchemaMasterDNSName)
{
if (!pszSchemaMasterDNSName)
   return E_POINTER;
HRESULT hr = E_FAIL;
IADs *pObject = NULL;
IADs *pTempSchema = NULL;
IADs *pNTDS = NULL;
IADs *pServer = NULL;
BSTR bstrParent;
LPOLESTR szPath = new OLECHAR[MAX_PATH];
VARIANT var, varRole,varComputer;
hr = ADsOpenObject(L"LDAP://rootDSE",
         NULL,
         NULL,
         ADS_SECURE_AUTHENTICATION, // Use Secure Authentication.
         IID_IADs,
         (void**)&pObject);
if (SUCCEEDED(hr))
{
  hr = pObject->Get(CComBSTR("schemaNamingContext"), &var);
  if (SUCCEEDED(hr))
  {
    wcscpy_s(szPath,L"LDAP://");
    wcscat_s(szPath,var.bstrVal);
    hr = ADsOpenObject(szPath,
             NULL,
             NULL,
             ADS_SECURE_AUTHENTICATION, // Use Secure Authentication.
             IID_IADs,
             (void**)&pTempSchema);
 
    if (SUCCEEDED(hr))
    {
      // Read the fsmoRoleOwner attribute to see which server is the schema master.
      hr = pTempSchema->Get(CComBSTR("fsmoRoleOwner"), &varRole);
      if (SUCCEEDED(hr))
      {
        // fsmoRoleOwner attribute returns the nTDSDSA object.
        // The parent is the server object.
        // Bind to NTDSDSA object and get the parent object.
        wcscpy_s(szPath,L"LDAP://");
        wcscat_s(szPath,varRole.bstrVal);
        hr = ADsOpenObject(szPath,
             NULL,
             NULL,
             ADS_SECURE_AUTHENTICATION, // Use Secure Authentication.
             IID_IADs,
             (void**)&pNTDS);
        if (SUCCEEDED(hr))
        {
          hr = pNTDS->get_Parent(&bstrParent);
          if (SUCCEEDED(hr))
          {
            // Bind to server object
            // and get the reference to the computer object.
            wcscpy_s(szPath,bstrParent);
            hr = ADsOpenObject(szPath,
               NULL,
               NULL,
               ADS_SECURE_AUTHENTICATION, // Use Secure Authentication.
               IID_IADs,
               (void**)&pServer);
            if (SUCCEEDED(hr))
            {
              // Get the dns name of the server.
              hr = pServer->Get(CCOmBSTR("dNSHostName"), &varComputer);
              if (SUCCEEDED(hr))
              {
                *pszSchemaMasterDNSName = (OLECHAR *)CoTaskMemAlloc (sizeof(OLECHAR)*(wcslen(varComputer.bstrVal)+1));
                if (*pszSchemaMasterDNSName)
                {
                  wcscpy_s(*pszSchemaMasterDNSName, varComputer.bstrVal);
                }
                else
                {
                  hr = E_OUTOFMEMORY;
                }
              }
              VariantClear(&varComputer);
            }
            if (pServer)
              pServer->Release();
          }
          SysFreeString(bstrParent);
        }
        if (pNTDS)
          pNTDS->Release();
      }
      VariantClear(&varRole);
    }
    if (pTempSchema)
      pTempSchema->Release();
  }
  VariantClear(&var);
}
if (pObject)
    pObject->Release();
 
return hr;
}
```



 

 




