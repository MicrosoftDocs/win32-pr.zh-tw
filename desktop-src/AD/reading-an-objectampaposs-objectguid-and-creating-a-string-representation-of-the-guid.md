---
title: 讀取物件的 objectGUID 並建立 GUID 的字串標記法
description: 您可以使用 IADs 取得 \_ GUID 方法來取得目錄物件的 objectGUID 的可系結字串形式。
ms.assetid: 4f7f0e9d-3e06-47c9-83ce-cabed8692c15
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77bf9c346585e8604968c3f708dfdc62ee8d248f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103681646"
---
# <a name="reading-an-objects-objectguid-and-creating-a-string-representation-of-the-guid"></a><span data-ttu-id="65d09-103">讀取物件的 objectGUID 並建立 GUID 的字串標記法</span><span class="sxs-lookup"><span data-stu-id="65d09-103">Reading an Object's objectGUID and Creating a String Representation of the GUID</span></span>

<span data-ttu-id="65d09-104">Active Directory Domain Services 中每個物件的 **objectGUID** 屬性會以八位字串的形式儲存在目錄中。</span><span class="sxs-lookup"><span data-stu-id="65d09-104">The **objectGUID** property of each object in Active Directory Domain Services is stored in the directory as an octet string.</span></span> <span data-ttu-id="65d09-105">八位字串是一個位元組字元的陣列。</span><span class="sxs-lookup"><span data-stu-id="65d09-105">An octet string is an array of one-byte characters.</span></span> <span data-ttu-id="65d09-106">您可以使用 [**IADs：： get \_ GUID**](/windows/desktop/ADSI/iads-property-methods) 方法來取得目錄物件的 **objectGUID** 的可系結字串形式。</span><span class="sxs-lookup"><span data-stu-id="65d09-106">Use the [**IADs::get\_GUID**](/windows/desktop/ADSI/iads-property-methods) method to retrieve the bindable string form of a directory object's **objectGUID**.</span></span>

<span data-ttu-id="65d09-107">下列程式碼範例會顯示一個函式，該函式會讀取 **objectGUID** 屬性，並傳回用來系結至物件之 GUID 的字串表示。</span><span class="sxs-lookup"><span data-stu-id="65d09-107">The following code examples show a function that reads the **objectGUID** attribute and returns a string representation of the GUID used to bind to the object.</span></span>

-   [<span data-ttu-id="65d09-108">Visual Basic 範例</span><span class="sxs-lookup"><span data-stu-id="65d09-108">Visual Basic Example</span></span>](#visual-basic-example)
-   [<span data-ttu-id="65d09-109">C + + 範例</span><span class="sxs-lookup"><span data-stu-id="65d09-109">C++ Example</span></span>](#c-example)

## <a name="visual-basic-example"></a><span data-ttu-id="65d09-110">Visual Basic 範例</span><span class="sxs-lookup"><span data-stu-id="65d09-110">Visual Basic Example</span></span>


```VB
Dim sADsPathObject As String
Dim sObjectGUID As String
Dim sBindByGuidStr As String
 
Dim IADsObject As IADs
Dim IADsObject2 As IADs
On Error Resume Next
 
' Query the user for an ADsPath to start.
sADsPathObject = InputBox("This code binds to a directory object by ADsPath, retrieves the GUID, then rebinds by GUID." & vbCrLf & vbCrLf & "Specify the ADsPath of the object to bind to :")
 
If sADsPathObject = "" Then
    GoTo CleanUp
End If
 
MsgBox "Binding to " & sADsPathObject
 
' Bind to initial object.
Set IADsObject = GetObject(sADsPathObject)
 
If (Err.Number <> 0) Then
   MsgBox Err.Number & " on GetObject method"
   GoTo CleanUp
End If
 
' Save the GUID of the object.
sObjectGUID = IADsObject.Guid
 
MsgBox "The GUID for " & vbCrLf & vbCrLf & sADsPathObject & vbCrLf & vbCrLf & " is " & vbCrLf & vbCrLf & sObjectGUID
 
' Release the initial object.
Set IADsObject = Nothing
 
' Build a string for Binding to the object by GUID.
sBindByGuidStr = "LDAP://<GUID=" & sObjectGUID & ">"

MsgBox sBindByGuidStr
 
' Bind BACK to the Same object using the GUID.
Set IADsObject = GetObject(sBindByGuidStr)
 
If (Err.Number <> 0) Then
   MsgBox Err.Number & " on GetObject method "
   GoTo CleanUp
End If
 
MsgBox "Successfully RE bound to " & sADsPathObject & vbCrLf & vbCrLf & " using the path:" & vbCrLf & vbCrLf & sBindByGuidStr
 
' Release bind by GUID Object.
CleanUp:
   Set IADsObject = Nothing

```



## <a name="c-example"></a><span data-ttu-id="65d09-111">C + + 範例</span><span class="sxs-lookup"><span data-stu-id="65d09-111">C++ Example</span></span>


```C++
#define UNICODE
#include <ole2.h>
#include <stdio.h>
#include <activeds.h>

#define PATH_SIZE 1024

void wmain(int argc, wchar_t *argv[])
{
    // Initialize COM.
    CoInitialize(0);
     
    WCHAR wszADsPathObject[PATH_SIZE + 1];
    HRESULT hr;
    IADs *pIADsObject = NULL;
    IADs *pIADsObjectByGuid = NULL;
     
    // If no ADsPath was specified on the command line, query the user for a ADsPath to start.
    if(!argv[1])
    {
        _putws(L"This code binds to a directory object by ADsPath, retrieves the GUID,\n"
            L" then rebinds by GUID. \n\nEnter the ADsPath of the object to bind to :\n");
        fgetws(wszADsPathObject, PATH_SIZE, stdin);
    }
    else
    {
        wcsncpy_s(wszADsPathObject, argv[1], PATH_SIZE - 1);
        wszADsPathObject[PATH_SIZE] = 0;
    }
     
    if (!wszADsPathObject[0])
    {
        return;
    }
     
    wprintf(L"\nBinding to %s\n", wszADsPathObject);
     
    // Bind to initial object.
    hr = ADsGetObject(wszADsPathObject, IID_IADs, (void**)&pIADsObject);
    if (SUCCEEDED(hr))
    {
        BSTR bstrGuid = NULL;
        hr = pIADsObject->get_GUID(&bstrGuid); 
        
        if (SUCCEEDED(hr))
        {
            LPWSTR wszFormat = L"LDAP://<GUID=%s>";
            LPWSTR pwszBindByGuidStr; 

            wprintf(L"\n The GUID for\n\n%s\n\nis\n\n%s\n", wszADsPathObject, bstrGuid);
     
            // Build a string for Binding to the object by GUID.
            pwszBindByGuidStr = new WCHAR[wcslen(wszFormat) + wcslen(bstrGuid) + 1];
            if(pwszBindByGuidStr)
            {
                swprintf_s(pwszBindByGuidStr, wszFormat, bstrGuid);
         
                // Bind BACK to the Same object using the GUID.
                hr = ADsGetObject(pwszBindByGuidStr, IID_IADs, (void**)&pIADsObjectByGuid);
                 
                if (SUCCEEDED(hr))
                {
                    wprintf(L"\nSuccessfully re-bound to\n\n%s\n\nUsing the path:\n\n%s\n", 
                        wszADsPathObject, pwszBindByGuidStr);
         
                    // Release bind by GUID Object.
                    pIADsObjectByGuid->Release();
                    pIADsObjectByGuid = NULL;
                }

                delete pwszBindByGuidStr;
            }
            else
            {
                hr = E_OUTOFMEMORY;
            }
     
            SysFreeString(bstrGuid);
        }
     
        pIADsObject->Release();
        pIADsObject = NULL;
    }
     
    if (FAILED(hr))
    {
        wprintf(L"Failed");
    }
}
```



 

 