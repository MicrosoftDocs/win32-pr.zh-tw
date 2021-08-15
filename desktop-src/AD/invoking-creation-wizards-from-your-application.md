---
title: 從您的應用程式叫用建立嚮導
description: 應用程式或元件可以使用 Active Directory 系統管理 MMC 嵌入式管理單元所使用的相同目錄服務物件建立嚮導。這是透過 IDsAdminCreateObj 介面完成的。
ms.assetid: be4b6101-f795-403b-b93e-960759ac4f14
ms.tgt_platform: multiple
keywords:
- 從您的應用程式 AD 叫用建立嚮導
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba1d5f8c722e3f673d998d3baaf33b4110293c70875a68fd03e8117f667351bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118187072"
---
# <a name="invoking-creation-wizards-from-your-application"></a>從您的應用程式叫用建立嚮導

應用程式或元件可以使用 Active Directory 系統管理 MMC 嵌入式管理單元所使用的相同目錄服務物件建立嚮導。這是透過 [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) 介面完成的。

## <a name="using-the-idsadmincreateobj-interface"></a>使用 IDsAdminCreateObj 介面

應用程式或元件 (用戶端) 使用 **CLSID \_ DsAdminCreateObj** 類別識別碼呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)來建立 [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj)介面的實例。 在呼叫 **CoCreateInstance** 之前，必須先呼叫 [**COINITIALIZE**](/windows/win32/api/objbase/nf-objbase-coinitialize)來初始化 COM。

然後，用戶端會呼叫 [**IDsAdminCreateObj：： initialize**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadmincreateobj-initialize) 來初始化 [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) 物件。 **IDsAdminCreateObj：： Initialize** 接受 [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) 介面指標，該指標代表應該在其中建立物件的容器，以及要建立之物件的類別名稱。 建立使用者物件時，也可以指定將複製到新物件的現有物件。

當 [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) 物件已初始化時，用戶端會呼叫 [**IDsAdminCreateObj：： CreateModal**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadmincreateobj-createmodal) 以顯示物件建立嚮導。

不同于大部分的類別和介面識別碼， **CLSID \_ DsAdminCreateObj** 和 **IID \_ ADsAdminCreateObj** 並未定義于程式庫檔案中。 這表示您必須在應用程式內定義這些識別碼的儲存體。 若要這樣做，您必須在包含 dsadmin 之前立即包含 initguid 檔案。 Initguid .h 檔案只能包含在應用程式中。 下列程式碼範例顯示如何包含這些檔案。


```C++
#include <initguid.h>
#include <dsadmin.h>
```



下列程式碼範例會示範如何建立 [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) 介面，以及如何使用這些介面來啟動使用者物件的物件建立 wizard。


```C++
//  Add activeds.lib to your project
//  Add adsiid.lib to your project

#include "stdafx.h"
#include <atlbase.h>
#include <atlstr.h>
#include "activeds.h"
#include <initguid.h> // Only include this in one source file
#include <dsadmin.h>

//  GetUserContainer() function binds to the user container
IADsContainer* GetUserContainer(void)
{
    IADsContainer *pUsers = NULL;
    HRESULT hr;
    IADs *pRoot;

    //  Bind to the rootDSE.
    hr = ADsGetObject(L"LDAP://rootDSE", IID_IADs, (LPVOID*)&pRoot);

    if(SUCCEEDED(hr))
    {
        VARIANT var;
        VariantInit(&var);
        CComBSTR sbstr(L"defaultNamingContext");

        //  Get the default naming context (domain) DN.
        hr = pRoot->Get(sbstr, &var);
        if(SUCCEEDED(hr) && (VT_BSTR == var.vt))
        {
            CStringW sstr(L"LDAP://CN=Users,");
            sstr += var.bstrVal;

            //  Bind to the User container.
            hr = ADsGetObject(sstr, IID_IADsContainer, (LPVOID*)&pUsers);

            VariantClear(&var);
        }
    }

    return pUsers;
}


//  The LaunchNewUserWizard() function launches the user wizard.
HRESULT LaunchNewUserWizard(IADs** ppAdsOut)
{
    if(NULL == ppAdsOut)
    {
        return E_INVALIDARG;
    }

    HRESULT hr;
    IDsAdminCreateObj* pCreateObj = NULL;

    hr = ::CoCreateInstance(CLSID_DsAdminCreateObj,
                            NULL, 
                            CLSCTX_INPROC_SERVER,
                            IID_IDsAdminCreateObj,
                            (void**)&pCreateObj);

    if(SUCCEEDED(hr))
    {
        IADsContainer *pContainer;

        pContainer = GetUserContainer();

        if(pContainer)
        {
            hr = pCreateObj->Initialize(pContainer, NULL, L"user");
            if(SUCCEEDED(hr))
            {
                HWND    hwndParent;

                hwndParent = GetDesktopWindow();

                hr = pCreateObj->CreateModal(hwndParent, ppAdsOut);
            }

            pContainer->Release();
        }

        pCreateObj->Release();
    }

    return hr;    
}

//  Entry point to the application
int main(void)
{
    HRESULT hr;
    IADs *pAds = NULL;

    CoInitialize(NULL);

    hr = LaunchNewUserWizard(&pAds);
    if((S_OK == hr) && (NULL != pAds))
    {
        pAds->Release();
    }

    CoUninitialize();

    return 0;
}
```



 

 