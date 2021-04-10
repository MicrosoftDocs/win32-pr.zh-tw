---
title: 讀取 attributeSchema 和 classSchema 物件
description: 本主題提供直接從架構容器中的 attributeSchema 和 classSchema 物件讀取的程式碼範例和指導方針。
ms.assetid: a60558e1-88a1-493c-9340-a90143b11f60
ms.tgt_platform: multiple
keywords:
- 讀取 attributeSchema 和 classSchema 物件 AD
- 物件 AD、讀取 attributeSchema 和 classSchema 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 910d387809f7be8af22d494974021e5e6a47d0ab
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104092628"
---
# <a name="reading-attributeschema-and-classschema-objects"></a><span data-ttu-id="ed608-105">讀取 attributeSchema 和 classSchema 物件</span><span class="sxs-lookup"><span data-stu-id="ed608-105">Reading attributeSchema and classSchema Objects</span></span>

<span data-ttu-id="ed608-106">本主題提供直接從架構容器中的 **attributeSchema** 和 **classSchema** 物件讀取的程式碼範例和指導方針。</span><span class="sxs-lookup"><span data-stu-id="ed608-106">This topic provides code examples and guidelines for reading directly from **attributeSchema** and **classSchema** objects in the schema container.</span></span> <span data-ttu-id="ed608-107">請注意，在大部分的程式設計情況下，當您必須讀取有關類別或屬性定義的資料時，從抽象架構讀取資料，如 [讀取抽象架構](reading-the-abstract-schema.md)中所述更有效。</span><span class="sxs-lookup"><span data-stu-id="ed608-107">Be aware that, in most programming situations, when you must read data about a class or attribute definition, it is more effective to read data from the abstract schema as described in [Reading the Abstract Schema](reading-the-abstract-schema.md).</span></span>

<span data-ttu-id="ed608-108">用來讀取架構容器的介面和技術，就是用來讀取 Active Directory Domain Services 中任何物件的介面和技術。</span><span class="sxs-lookup"><span data-stu-id="ed608-108">The interfaces and techniques used to read from the schema container are those used to read any object in Active Directory Domain Services.</span></span> <span data-ttu-id="ed608-109">這些指導方針包括：</span><span class="sxs-lookup"><span data-stu-id="ed608-109">The guidelines include:</span></span>

-   <span data-ttu-id="ed608-110">若要系結至架構容器，請取得其辨別名稱，此名稱可透過系結至 rootDSE 並讀取 **schemaNamingCoNtext** 屬性（如 [無伺服器系結和 rootDSE](serverless-binding-and-rootdse.md)中所述）來抓取。</span><span class="sxs-lookup"><span data-stu-id="ed608-110">To bind to the schema container, obtain its distinguished name which can be retrieved by binding to rootDSE and reading the **schemaNamingContext** property, as described in [Serverless Binding and RootDSE](serverless-binding-and-rootdse.md).</span></span>
-   <span data-ttu-id="ed608-111">使用架構容器的 [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) 指標來列舉 **attributeSchema** 和 **classSchema** 物件。</span><span class="sxs-lookup"><span data-stu-id="ed608-111">Use an [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) pointer for the schema container to enumerate the **attributeSchema** and **classSchema** objects.</span></span>
-   <span data-ttu-id="ed608-112">使用 [**IADs**](/windows/desktop/api/iads/nn-iads-iads) 或 [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) 介面取出 **attributeSchema** 和 **classSchema** 物件的屬性。</span><span class="sxs-lookup"><span data-stu-id="ed608-112">Use the [**IADs**](/windows/desktop/api/iads/nn-iads-iads) or [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) interface to retrieve the properties of an **attributeSchema** and **classSchema** object.</span></span>
-   <span data-ttu-id="ed608-113">使用 [**ADsOpenObject**](/windows/desktop/api/adshlp/nf-adshlp-adsopenobject) 或 [**ADsGetObject**](/windows/desktop/api/adshlp/nf-adshlp-adsgetobject) 函數直接系結至 **attributeSchema** 或 **classSchema** 物件。</span><span class="sxs-lookup"><span data-stu-id="ed608-113">Use the [**ADsOpenObject**](/windows/desktop/api/adshlp/nf-adshlp-adsopenobject) or [**ADsGetObject**](/windows/desktop/api/adshlp/nf-adshlp-adsgetobject) functions to bind directly to an **attributeSchema** or **classSchema** object.</span></span>
-   <span data-ttu-id="ed608-114">如果您正在讀取多個 **attributeSchema** 或 **classSchema** 物件，您可以藉由系結至架構容器上的 [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) 指標並使用 [**IADsContainer**](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject) 來系結至個別類別和屬性物件，來提高效能。</span><span class="sxs-lookup"><span data-stu-id="ed608-114">If you are reading multiple **attributeSchema** or **classSchema** objects, you can increase performance by binding to an [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) pointer on the schema container and using the [**IADsContainer.GetObject**](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject) method to bind to the individual class and attribute objects.</span></span> <span data-ttu-id="ed608-115">這比進行重複的 [**ADsOpenObject**](/windows/desktop/api/adshlp/nf-adshlp-adsopenobject) 或 [**ADsGetObject**](/windows/desktop/api/adshlp/nf-adshlp-adsgetobject) 呼叫以系結至個別類別和屬性物件更有效率。</span><span class="sxs-lookup"><span data-stu-id="ed608-115">This is more efficient than making repeated [**ADsOpenObject**](/windows/desktop/api/adshlp/nf-adshlp-adsopenobject) or [**ADsGetObject**](/windows/desktop/api/adshlp/nf-adshlp-adsgetobject) calls to bind to the individual class and attribute objects.</span></span> <span data-ttu-id="ed608-116">使用 **cn** 屬性來建立 IADsContainer 的相對路徑 (**。** 例如，"cn = user" 代表 user 類別的 **classSchema** 物件) 。</span><span class="sxs-lookup"><span data-stu-id="ed608-116">Use the **cn** attribute to build the relative path for the **IADsContainer.GetObject** call (for example, "cn=user" for the **classSchema** object for the user class).</span></span>
-   <span data-ttu-id="ed608-117">針對架構容器使用 [**>idirectorysearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) 指標，以查詢符合搜尋篩選準則的屬性或類別的架構。</span><span class="sxs-lookup"><span data-stu-id="ed608-117">Use an [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) pointer for the schema container to query the schema for attributes or classes that match a search filter.</span></span>

<span data-ttu-id="ed608-118">如需示範搜尋架構物件之不同方法的程式碼範例，請參閱 [搜尋架構物件的範例程式碼](example-code-for-searching-for-schema-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="ed608-118">For a code example that demonstrates different methods of searching for schema objects, see [Example Code for Searching for Schema Objects](example-code-for-searching-for-schema-objects.md).</span></span>

<span data-ttu-id="ed608-119">下列 c + + 程式碼範例會系結至架構容器上的 [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) 指標，然後使用 [**ADsBuildEnumerator**](/windows/desktop/api/adshlp/nf-adshlp-adsbuildenumerator) 和 [**ADsEnumerateNext**](/windows/desktop/api/adshlp/nf-adshlp-adsenumeratenext) 函式來列舉其內容。</span><span class="sxs-lookup"><span data-stu-id="ed608-119">The following C++ code example binds to an [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) pointer on the schema container and then uses the [**ADsBuildEnumerator**](/windows/desktop/api/adshlp/nf-adshlp-adsbuildenumerator) and [**ADsEnumerateNext**](/windows/desktop/api/adshlp/nf-adshlp-adsenumeratenext) functions to enumerate its contents.</span></span> <span data-ttu-id="ed608-120">請注意，列舉包含所有的 **attributeSchema** 和 **classSchema** 物件，以及單一 **ubschema** 物件，也就是抽象架構。</span><span class="sxs-lookup"><span data-stu-id="ed608-120">Be aware that the enumeration includes all **attributeSchema** and **classSchema** objects as well as a single **subSchema** object, which is the abstract schema.</span></span>

<span data-ttu-id="ed608-121">針對每個列舉物件，程式碼範例會使用 [**IADs 類別**](/windows/desktop/ADSI/iads-property-methods) 屬性來判斷它是否為 **attributeSchema** 或 **classSchema** 物件。</span><span class="sxs-lookup"><span data-stu-id="ed608-121">For each enumerated object, the code example uses the [**IADs.Class**](/windows/desktop/ADSI/iads-property-methods) property to determine whether it is an **attributeSchema** or **classSchema** object.</span></span> <span data-ttu-id="ed608-122">程式碼範例會示範如何讀取抽象架構中無法使用的屬性。</span><span class="sxs-lookup"><span data-stu-id="ed608-122">The code example shows how to read the properties that are unavailable from the abstract schema.</span></span>


```C++
//  Add activeds.lib to the project.
//  Add adsiid.lib to the project.

#include "stdafx.h"
#include <windows.h>
#include <stdio.h>
#include <ole2.h>
#include <activeds.h>
#include <atlbase.h>

//  Forward declarations.
void ProcessAttribute(IADs *pChild);
void ProcessClass(IADs *pChild);

//  Entry point for the application.
int wmain(int argc, WCHAR* argv[])
{
    HRESULT hr;

    hr = CoInitialize(NULL);
    if(SUCCEEDED(hr))
    {
        CComBSTR sbstrDSPath;
        CComVariant svar;
        IADs *pRootDSE = NULL;
        IADsContainer *pSchema = NULL;  
        IEnumVARIANT *pEnum = NULL;
        ULONG lFetch;
        CComBSTR sbstrClass; 
        DWORD dwClasses = 0, dwAttributes = 0, dwUnknownClass = 0;

        //  Bind to rootDSE to get the schemaNamingContext property.
        hr = ADsGetObject(L"LDAP://rootDSE", IID_IADs, (void**)&pRootDSE);
        if (FAILED(hr)) 
        {
            wprintf(L"ADsGetObject failed: 0x%x\n", hr);
            goto cleanup;
        }

        hr = pRootDSE->Get(CComBSTR("schemaNamingContext"), &svar);
        sbstrDSPath = "LDAP://";
        sbstrDSPath += svar.bstrVal;

        //  Bind to the actual schema container.
        wprintf(L"Binding to %s\n", sbstrDSPath);
        hr = ADsGetObject(sbstrDSPath, IID_IADsContainer, (void**) &pSchema);
        if (FAILED(hr)) 
        {
            wprintf(L"ADsGetObject to schema failed: 0x%x\n", hr);
            goto cleanup;
        }

        //  Enumerate the attribute and class objects in the schema container.
        hr = ADsBuildEnumerator(pSchema, &pEnum);
        if (FAILED(hr)) 
        {
            wprintf(L"ADsBuildEnumerator failed: 0x%x\n", hr);
            goto cleanup;
        }

        hr = ADsEnumerateNext(pEnum, 1, &svar, &lFetch);
        while(S_OK == hr && 1 == lFetch)
        {
            IADs *pChild = NULL;

            //  Get an IADs pointer on the child object.
            hr = V_DISPATCH(&svar)->QueryInterface(IID_IADs, (void**) &pChild);
            if (SUCCEEDED(hr)) 
            {
                //  Verify that this is a class, attribute, or subSchema object.
                hr = pChild->get_Class(&sbstrClass);
                if (SUCCEEDED(hr)) 
                {
                    //  Get data. This depends on type of schema element.
                    if (_wcsicmp(L"classSchema", sbstrClass) == 0)
                    {
                        dwClasses++;
                        wprintf(L"%s\n", sbstrClass);
                        ProcessClass(pChild);
                        wprintf(L"\n");
                    }
                    else if (_wcsicmp(L"attributeSchema", sbstrClass) == 0)
                    {
                        dwAttributes++;
                        wprintf(L"%s\n", sbstrClass);
                        ProcessAttribute(pChild);
                        wprintf(L"\n");
                    }
                    else if (_wcsicmp(L"subSchema", sbstrClass) == 0) 
                    {
                        wprintf(L"abstract schema");
                        wprintf(L"\n");
                    }
                    else
                    {
                        dwUnknownClass++;
                    }
                }

                pChild->Release();
            }

            hr = ADsEnumerateNext(pEnum, 1, &svar, &lFetch);
        }

        wprintf(L"Classes: %u\nAttributes: %u\nUnknown: %u\n", dwClasses, dwAttributes, dwUnknownClass);

cleanup:
        if (pRootDSE)
        {
            pRootDSE->Release();
        }

        if (pEnum)
        {
            ADsFreeEnumerator(pEnum);
        }

        if (pSchema)
        {
            pSchema->Release();
        }

    }    

    CoUninitialize();

    return 0;
}


//  PrintGUIDFromVariant
//  Prints a GUID in string format.
void PrintGUIDFromVariant(VARIANT varGUID)
{
    HRESULT hr;
    void HUGEP *pArray;
    WCHAR szGUID[40];
    LPGUID pGUID;

    DWORD dwLen = sizeof(GUID);

    hr = SafeArrayAccessData(V_ARRAY(&varGUID), &pArray);
    if(SUCCEEDED(hr))
    {
        pGUID = (LPGUID)pArray;

        //  Convert GUID to string.
        StringFromGUID2(*pGUID, szGUID, 40); 

        //  Print GUID.
        wprintf(L",%s",szGUID);

        SafeArrayUnaccessData(V_ARRAY(&varGUID));
    }
}


// PrintADSPropertyValue
void PrintADSPropertyValue(VARIANT var, BSTR bstrPropName, HRESULT hr) 
{
    if (E_ADS_PROPERTY_NOT_FOUND == hr)
    {
        wprintf(L"-- not set --\n");
    }
    else if (FAILED(hr))
    {
        wprintf(L"get %s failed: 0x%x\n", bstrPropName, hr);
    }
    else 
    {
        switch (var.vt) 
        {
        case VT_BSTR:
            wprintf(L"%s\n", var.bstrVal);
            break;

        case VT_I4:
            wprintf(L"%u\n", var.iVal);
            break;

        case VT_BOOL:
            wprintf(L"%s\n", var.boolVal ? L"TRUE" : L"FALSE");
            break;

        default:
            wprintf(L"-- ??? --\n");
        }
    }
}

//  ProcessAttribute
//  Gets information about an attributeClass object.
void ProcessAttribute(IADs *pChild)
{
    HRESULT hr;
    CComVariant svar;
    CComBSTR sbstrPropName;

    //  Get the attribute Common-Name (cn) property. 
    sbstrPropName = "cn";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);

    //  Get the attribute lDAPDisplayName.
    sbstrPropName = "lDAPDisplayName";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);

    //  Get the class linkID. 
    sbstrPropName = "linkID";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);

    //  Get the attribute schemaIDGUID. 
    sbstrPropName = "schemaIDGUID";
    hr = pChild->Get(sbstrPropName, &svar);
    if (E_ADS_PROPERTY_NOT_FOUND == hr)
    {
        wprintf(L"-- not set --\n");
    }
    else if(SUCCEEDED(hr))
    {
        PrintGUIDFromVariant(svar);
    }

    //  Get the attribute attributeSecurityGUID. 
    sbstrPropName = "attributeSecurityGUID";
    hr = pChild->Get(sbstrPropName, &svar);
    if (E_ADS_PROPERTY_NOT_FOUND == hr)
    {
        wprintf(L"-- not set --\n");
    }
    else if (SUCCEEDED(hr))
    {
        PrintGUIDFromVariant(svar);
    }

    //  Get the attribute attributeSyntax property. 
    sbstrPropName = "attributeSyntax";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);

    //  Get the attribute's oMSyntax property. 
    sbstrPropName = "oMSyntax";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);
}


//  ProcessClass
//  Gets information about a schema class.
void ProcessClass(IADs *pChild)
{
    HRESULT hr;
    CComVariant svar;
    CComBSTR sbstrPropName;

    //  Get the class cn.
    sbstrPropName = "cn";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);

    //  Get the class lDAPDisplayName.
    sbstrPropName = "lDAPDisplayName";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);

    //  Get the class schemaIDGUID. 
    sbstrPropName = "schemaIDGUID";
    hr = pChild->Get(sbstrPropName, &svar);
    if (FAILED(hr))
    {
        wprintf(L",get schemaIDGUID failed: 0x%x", hr);
    }
    else 
    {
        PrintGUIDFromVariant(svar);
    }

    //  Get the class adminDescription property. 
    sbstrPropName = "adminDescription";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);

    //  Get the class adminDisplayName property. 
    sbstrPropName = "adminDisplayName";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);

    //  Get the class rDNAttID. 
    sbstrPropName = "rDNAttID";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);

    //  Get the class defaultHidingValue. 
    sbstrPropName = "defaultHidingValue";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);

    //  Get the class defaultObjectCategory. 
    sbstrPropName = "defaultObjectCategory";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);

    //  Get the class systemOnly value.
    sbstrPropName = "systemOnly";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);

    //  Get the class defaultSecurityDescriptor.
    sbstrPropName = "defaultSecurityDescriptor";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);
}
```



 

 