---
description: 您可以使用下列指示，為您的 COM + 應用程式設定 COM + 應用程式共用值。
ms.assetid: faba5cb7-745e-4fdf-a3e0-62132da4a843
title: 設定 COM + 應用程式共用值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98922699fff7af7146250bdb504a1f46be08718e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187658"
---
# <a name="configuring-com-application-pooling-values"></a><span data-ttu-id="22c29-103">設定 COM + 應用程式共用值</span><span class="sxs-lookup"><span data-stu-id="22c29-103">Configuring COM+ Application Pooling Values</span></span>

<span data-ttu-id="22c29-104">您可以使用下列指示，為您的 COM + 應用程式設定 COM + 應用程式共用值。</span><span class="sxs-lookup"><span data-stu-id="22c29-104">You can use the following instructions to configure COM+ application pooling values for your COM+ application.</span></span>

> [!Note]  
> <span data-ttu-id="22c29-105">程式庫應用程式具有其主機進程的回收和共用屬性。</span><span class="sxs-lookup"><span data-stu-id="22c29-105">Library applications have the recycling and pooling properties of their host process.</span></span>

 

## <a name="component-services-administrative-tool"></a><span data-ttu-id="22c29-106">元件服務系統管理工具</span><span class="sxs-lookup"><span data-stu-id="22c29-106">Component Services Administrative Tool</span></span>

<span data-ttu-id="22c29-107">若要設定 com + 應用程式的 COM + 應用程式共用，請使用下列步驟：</span><span class="sxs-lookup"><span data-stu-id="22c29-107">To configure COM+ application pooling for a COM+ application, use the following steps:</span></span>

1.  <span data-ttu-id="22c29-108">在 [元件服務] 系統管理工具的主控台樹中，以滑鼠右鍵按一下您想要共用的 COM + 應用程式， **然後按一下 [** 內容]。</span><span class="sxs-lookup"><span data-stu-id="22c29-108">In the console tree of the Component Services administrative tool, right-click the COM+ application you want to be pooled and then click **Properties**.</span></span>

2.  <span data-ttu-id="22c29-109">在 [共用 **& 回收** ] 索引標籤的 [ **應用程式** 共用] 下，根據您想要執行的應用程式實例數目，輸入 [ **集區大小**] 的值。</span><span class="sxs-lookup"><span data-stu-id="22c29-109">On the **Pooling & Recycling** tab, under **Application Pooling**, enter a value for **Pool Size**, depending on the number of instances of your application that you want to have running.</span></span>

3.  <span data-ttu-id="22c29-110">按一下 [確定]  。</span><span class="sxs-lookup"><span data-stu-id="22c29-110">Click **OK**.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="22c29-111">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="22c29-111">Visual Basic</span></span>

<span data-ttu-id="22c29-112">Visual Basic 中的下列函式示範如何針對您選擇的任何 COM + 伺服器應用程式，設定 COM + 應用程式共用值 (以其 ConcurrentApps 屬性) 表示。</span><span class="sxs-lookup"><span data-stu-id="22c29-112">The following function in Visual Basic demonstrates how you can set the COM+ application pooling value (represented by its ConcurrentApps property) for any COM+ server application that you choose.</span></span> <span data-ttu-id="22c29-113">若要從 Visual Basic 使用它，請將參考新增至 COM + 系統管理員類型程式庫。</span><span class="sxs-lookup"><span data-stu-id="22c29-113">To use it from Visual Basic, add a reference to the COM+ Admin Type Library.</span></span>


```VB
Function SetMyApplicationPooling( _
  strApplicationName As String, _
  lngPoolValue As Long _
) As Boolean  ' Return False if any errors occur.

    SetMyApplicationPooling = False  ' Initialize the function.
    On Error GoTo My_Error_Handler  ' Initialize error handling.

    Dim objCatalog As COMAdmin.COMAdminCatalog
    Dim objAppCollection As COMAdmin.COMAdminCatalogCollection
    Dim objApplication As COMAdmin.COMAdminCatalogObject
    Set objCatalog = CreateObject("COMAdmin.COMAdminCatalog")
    Set objAppCollection = objCatalog.GetCollection("Applications")
    objAppCollection.Populate 
    For Each objApplication in objAppCollection
        If objApplication.Name = strApplicationName Then
            objApplication.Value("ConcurrentApps") = lngPoolValue
            MsgBox strApplicationName & _
              " pooling value set to " & lngPoolValue
            Exit For
        End If
    Next
    objAppCollection.SaveChanges

    Set objApplication = Nothing
    Set objAppCollection = Nothing
    Set objCatalog = Nothing
    SetMyApplicationPooling = True  ' Successful end to procedure
    Exit Function

My_Error_Handler:  ' Replace with specific error handling.
    MsgBox "Error # " & Err.Number & " (Hex: " & Hex(Err.Number) _
      & ")" & vbNewLine & Err.Description
    Set objApplication = Nothing
    Set objAppCollection = Nothing
    Set objCatalog = Nothing
End Function

```



<span data-ttu-id="22c29-114">若要使用函式，請提供 COM + 伺服器應用程式名稱的字串值，以及所需應用程式共用設定的整數值。</span><span class="sxs-lookup"><span data-stu-id="22c29-114">To use the function, provide a string value for the COM+ server application name and an integer value for the desired application pooling setting.</span></span> <span data-ttu-id="22c29-115">下列 Visual Basic 程式碼示範如何針對名為 "MyApplication" 的應用程式，將應用程式共用值設定為15：</span><span class="sxs-lookup"><span data-stu-id="22c29-115">The following Visual Basic code shows how to set the application pooling value to 15 for the application named "MyApplication":</span></span>


```VB
Sub Main()
    If Not SetMyApplicationPooling("MyApplication", 15) Then
        MsgBox "SetMyApplicationPooling failed."
    End If
End Sub

```



## <a name="cc"></a><span data-ttu-id="22c29-116">C/C++</span><span class="sxs-lookup"><span data-stu-id="22c29-116">C/C++</span></span>

<span data-ttu-id="22c29-117">C + + 中的下列函式示範如何針對您選擇的任何 COM + 伺服器應用程式，將 COM + 應用程式共用值 (以其 ConcurrentApps 屬性) 來表示。</span><span class="sxs-lookup"><span data-stu-id="22c29-117">The following function in C++ demonstrates how you can set the COM+ application pooling value (represented by its ConcurrentApps property) for any COM+ server application that you choose.</span></span> <span data-ttu-id="22c29-118">ErrorDescription 方法說明于 [解釋錯誤碼](interpreting-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="22c29-118">The ErrorDescription method is described at [Interpreting Error Codes](interpreting-error-codes.md).</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#import "C:\WINDOWS\system32\Com\ComAdmin.dll"
#include "ComAdmin.h"
#include "StrSafe.h"  // For the StringCchLengthW function

BOOL SetMyApplicationPooling (OLECHAR* szMyApp, LONG lPool) {
    IUnknown * pUnknown = NULL;
    ICOMAdminCatalog * pCatalog = NULL;
    ICatalogCollection * pAppColl = NULL;
    ICatalogObject * pApplication = NULL;
    HRESULT hr = S_OK;
    BSTR bstrMyApp = NULL;
    unsigned int uMaxLen = 255;  // Maximum length of szMyApp
    LCID lLan = 1024;// Use the default language for comparing strings.

try {
    // Test the input pool value.
    if ((lPool < 1) || (lPool > 1048576)) throw(E_INVALIDARG);
    
    // Test the input szMyApp to make sure it's OK to use.
    hr = StringCchLengthW(szMyApp, uMaxLen, NULL);
    if (FAILED (hr)) throw(hr);
    
    // Convert szMyApp to a BSTR.
    bstrMyApp = SysAllocString(szMyApp);

    // Create a COMAdminCatalog object and get its IUnknown.
    hr = CoCreateInstance(CLSID_COMAdminCatalog, NULL, 
      CLSCTX_INPROC_SERVER, IID_IUnknown, (void**)&pUnknown);
    if (FAILED (hr)) throw(hr);

    // Get the ICOMAdminCatalog interface.
   hr = pUnknown->QueryInterface(IID_ICOMAdminCatalog, 
      (void**)&pCatalog); 
    if (FAILED (hr)) throw(hr);

    // Get an interface to the Applications collection.
    hr = pCatalog->GetCollection(L"Applications", (IDispatch**)&pAppColl);
    if (FAILED (hr)) throw(hr);

    // Populate all of the Applications collection.
    hr = pAppColl->Populate();
    if (FAILED (hr)) throw(hr);

    // Get the number of applications in the collection.
    LONG lCount = -1;
    hr = pAppColl->get_Count(&lCount);
    if (FAILED (hr)) throw(hr);

    // Iterate through each application in the collection.
    VARIANT varName;
    VariantInit(&varName);
    for (LONG lIdx = 0; lIdx < lCount; lIdx++) {
        hr = pAppColl->get_Item(lIdx, (IDispatch**)&pApplication);
        if (FAILED (hr)) throw(hr);

        // Get the Name value of each application.
       hr = pApplication->get_Name(&varName);
        if (FAILED (hr)) throw(hr);

        // Compare the application name to bstrMyApp.
        hr = VarBstrCmp(varName.bstrVal, bstrMyApp, lLan, NULL);
        if (FAILED (hr)) throw(hr);
        if (VARCMP_EQ == hr) {  // The strings are equal.
            // Set the new pooling value.
            VARIANT varPool;
            VariantInit(&varPool);
            varPool.vt = VT_I4;  // Tell the VARIANT it's holding a LONG.
            varPool.lVal = lPool;
            hr = pApplication->put_Value(L"ConcurrentApps", varPool);
            if (FAILED (hr)) throw(hr);
            printf("%S pooling value set to %ld.\n", bstrMyApp, lPool);
            break;
        }
    }
    LONG lNum;
    hr = pAppColl->SaveChanges(&lNum);
    if (FAILED (hr)) throw(hr);

    // Clean up.
    SysFreeString(bstrMyApp);
    pUnknown->Release();
    pUnknown = NULL;
    pApplication->Release();
    pApplication = NULL;
    pAppColl->Release();
    pAppColl = NULL;
    pCatalog->Release();
    pCatalog = NULL;
    return (TRUE);
}  // Try

catch(HRESULT hr) {  // Replace with specific error handling.
    printf("Error # %#x: ", hr);
    ErrorDescription(hr);
    SysFreeString(bstrMyApp);
    if (NULL != pUnknown) pUnknown>Release();
    pUnknown = NULL;
    if (NULL != pApplication) pApplication->Release();
    pApplication = NULL;
    if (NULL != pAppColl) pAppColl->Release();
    pAppColl = NULL;
    if (NULL != pCatalog) pCatalog->Release();
    pCatalog = NULL;
    return (FALSE);
}catch(...) {
    printf("An unexpected exception occurred.\n");
    throw;
}
}  // SetMyApplicationPooling

```



<span data-ttu-id="22c29-119">若要使用函式，請提供 COM + 伺服器應用程式名稱的字串值，以及所需應用程式共用設定的整數值。</span><span class="sxs-lookup"><span data-stu-id="22c29-119">To use the function, provide a string value for the COM+ server application name and an integer value for the desired application pooling setting.</span></span> <span data-ttu-id="22c29-120">下列 c + + 程式碼示範如何針對名為 "MyApplication" 的應用程式，將應用程式共用值設定為15：</span><span class="sxs-lookup"><span data-stu-id="22c29-120">The following C++ code shows how to set the application pooling value to 15 for the application named "MyApplication":</span></span>

``` syntax
#define _WIN32_DCOM  // To use CoInitializeEx()
void main() {
    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
    if (FAILED (hr)) {
        printf("CoInitializeEx failed: Error # %#x\n", hr);
        exit(0);  // Replace with specific error handling.
    }
    if (! SetMyApplicationPooling (L"MyApplication", 15))
        printf("SetMyApplicationPooling failed.\n");
    CoUninitialize();
}
```

## <a name="related-topics"></a><span data-ttu-id="22c29-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="22c29-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22c29-122">COM + 應用程式共用概念</span><span class="sxs-lookup"><span data-stu-id="22c29-122">COM+ Application Pooling Concepts</span></span>](com--application-pooling-concepts.md)
</dt> </dl>

 

 



