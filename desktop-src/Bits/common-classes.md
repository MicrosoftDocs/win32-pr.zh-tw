---
title: 常見類別範例
description: 您可以使用本主題中的程式碼範例，作為許多背景智慧型傳送服務 (位的起點，) 執行 COM 初始化的應用程式、需要錯誤處理，以及接收回呼通知。
ms.assetid: 8fe722a3-fbab-4843-b298-1ea11f54d7a5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 864fe4aa8d7af5bb6a248364b0e2c636e1c250a6
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "103684244"
---
# <a name="example-common-classes"></a><span data-ttu-id="53db8-103">範例：通用類別</span><span class="sxs-lookup"><span data-stu-id="53db8-103">Example: Common Classes</span></span>

<span data-ttu-id="53db8-104">您可以使用本主題中的程式碼範例，作為許多背景智慧型傳送服務 (位的起點，) 執行 COM 初始化的應用程式、需要錯誤處理，以及接收回呼通知。</span><span class="sxs-lookup"><span data-stu-id="53db8-104">You can use the code examples in this topic as a starting point for many Background Intelligent Transfer Service (BITS) applications that perform COM initialization, need error handling, and receive callback notifications.</span></span>


<span data-ttu-id="53db8-105">下列程式碼範例會定義例外狀況類別來處理錯誤。</span><span class="sxs-lookup"><span data-stu-id="53db8-105">The following code example defines an exception class to handle errors.</span></span>


```C++
class MyException
{
public:
    MyException(HRESULT hr, LPWSTR message):Error(hr), Message(message)
    {

    }
    HRESULT Error;
    std::wstring Message;
};
```



<span data-ttu-id="53db8-106">MyException 類別是泛型例外狀況類別，可接受 HRESULT 程式碼和錯誤字串。</span><span class="sxs-lookup"><span data-stu-id="53db8-106">The MyException class is a generic exception class that accepts an HRESULT code and error string.</span></span>


<span data-ttu-id="53db8-107">下列程式碼範例會定義 [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) 函數的資源取得 helper 類別。</span><span class="sxs-lookup"><span data-stu-id="53db8-107">The following code example defines a resource acquisition helper class for the [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) function.</span></span>


```C++
class CCoInitializer 
{
public:
    CCoInitializer( DWORD dwCoInit ) 
    { 
        HRESULT hr = CoInitializeEx( NULL, dwCoInit );
        if (FAILED(hr))
        {
            throw MyException(hr,L"CoInitialize");
        }
    } 

    ~CCoInitializer() throw() 
    { 
        CoUninitialize(); 
    } 
};
```



<span data-ttu-id="53db8-108">CCoInitializer 類別會處理 COM 初始化的資源配置和解除配置。</span><span class="sxs-lookup"><span data-stu-id="53db8-108">The CCoInitializer class deals with resource allocation and deallocation for COM initialization.</span></span> <span data-ttu-id="53db8-109">此類別可讓您在類別超出範圍時呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="53db8-109">This class enables the destructor to be called when the class goes out of scope.</span></span> <span data-ttu-id="53db8-110">這個類別不需要在每個例外狀況區塊之後呼叫 [CoUninitialize](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) 方法。</span><span class="sxs-lookup"><span data-stu-id="53db8-110">This class eliminates the need for the [CoUninitialize](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) method to be called after every exception block.</span></span>


<span data-ttu-id="53db8-111">下列程式碼範例是 CNotifyInterface 回呼介面的宣告。</span><span class="sxs-lookup"><span data-stu-id="53db8-111">The following code example is the declaration of the CNotifyInterface callback interface.</span></span>


```C++
// Implementation of the Callback interface
//
class CNotifyInterface : public IBackgroundCopyCallback
{
    LONG m_lRefCount;

public:
    //Constructor
    CNotifyInterface() {m_lRefCount = 1;};

//Destructor
    ~CNotifyInterface() {};

    //IUnknown methods
    HRESULT __stdcall QueryInterface(REFIID riid, LPVOID *ppvObj);
    ULONG __stdcall AddRef();
    ULONG __stdcall Release();

    //IBackgroundCopyCallback methods
    HRESULT __stdcall JobTransferred(IBackgroundCopyJob* pJob);
    HRESULT __stdcall JobError(IBackgroundCopyJob* pJob, IBackgroundCopyError* pError);
    HRESULT __stdcall JobModification(IBackgroundCopyJob* pJob, DWORD dwReserved);

private:
    CNotifyInterface(const CNotifyInterface&);
    CNotifyInterface& operator=(const CNotifyInterface&);
};
```



<span data-ttu-id="53db8-112">衍生自 [**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) 介面的 CNotifyInterface 類別。</span><span class="sxs-lookup"><span data-stu-id="53db8-112">The CNotifyInterface class derived from the [**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) interface.</span></span> <span data-ttu-id="53db8-113">CNotifyInterface 類別會實作為 IUnknown 介面。</span><span class="sxs-lookup"><span data-stu-id="53db8-113">The CNotifyInterface class implements the IUnknown interface.</span></span> <span data-ttu-id="53db8-114">如需詳細資訊，請參閱 [IUnknown]( /windows/win32/api/unknwn/nn-unknwn-iunknown)。</span><span class="sxs-lookup"><span data-stu-id="53db8-114">For more information, see [IUnknown]( /windows/win32/api/unknwn/nn-unknwn-iunknown).</span></span>

<span data-ttu-id="53db8-115">CNotifyInterface 會使用下列方法來接收作業已完成、已修改或處於錯誤狀態的通知： [**JobTransferred**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobtransferred)、 [**JobModification**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobmodification)和 [**JobError**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-joberror)。</span><span class="sxs-lookup"><span data-stu-id="53db8-115">CNotifyInterface uses the following methods to receive notification that a job is complete, has been modified, or is in an error state: [**JobTransferred**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobtransferred), [**JobModification**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobmodification), and [**JobError**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-joberror).</span></span> <span data-ttu-id="53db8-116">所有這些方法都採用 [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) 工作物件。</span><span class="sxs-lookup"><span data-stu-id="53db8-116">All of these methods take an [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) job object.</span></span>

<span data-ttu-id="53db8-117">此範例會使用 [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) 來釋放記憶體資源。</span><span class="sxs-lookup"><span data-stu-id="53db8-117">This example uses the [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) to free memory resources.</span></span>


<span data-ttu-id="53db8-118">下列程式碼範例是 [**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) 回呼介面的實作為。</span><span class="sxs-lookup"><span data-stu-id="53db8-118">The following code example is the implementation of the [**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) callback interface.</span></span>


```C++
HRESULT CNotifyInterface::QueryInterface(REFIID riid, LPVOID* ppvObj) 
{
    if (riid == __uuidof(IUnknown) || riid == __uuidof(IBackgroundCopyCallback)) 
    {
        *ppvObj = this;
    }
    else
    {
        *ppvObj = NULL; 
        return E_NOINTERFACE;
    }

    AddRef();
    return NOERROR;
}

ULONG CNotifyInterface::AddRef() 
{
    return InterlockedIncrement(&m_lRefCount);
}

ULONG CNotifyInterface::Release() 
{
    // not thread safe
    ULONG  ulCount = InterlockedDecrement(&m_lRefCount);

    if(0 == ulCount) 
    {
        delete this;
    }

    return ulCount;
}

HRESULT CNotifyInterface::JobTransferred(IBackgroundCopyJob* pJob)
{
    HRESULT hr;

    wprintf(L"Job transferred. Completing Job...\n");
    hr = pJob->Complete();
    if (FAILED(hr))
    {
        //BITS probably was unable to rename one or more of the 
        //temporary files. See the Remarks section of the IBackgroundCopyJob::Complete 
        //method for more details.
        wprintf(L"Job Completion Failed with error %x\n", hr);
    }

    PostQuitMessage(0);

    //If you do not return S_OK, BITS continues to call this callback.
    return S_OK;
}

HRESULT CNotifyInterface::JobModification(IBackgroundCopyJob* pJob, DWORD dwReserved)
{
    return S_OK;
}

HRESULT CNotifyInterface::JobError(IBackgroundCopyJob* pJob, IBackgroundCopyError* pError)
{
    WCHAR* pszJobName = NULL;
    WCHAR* pszErrorDescription = NULL;

    //Use pJob and pError to retrieve information of interest. For example,
    //if the job is an upload reply, call the IBackgroundCopyError::GetError method 
    //to determine the context in which the job failed. 

    wprintf(L"Job entered error state...\n");
    HRESULT hr = pJob->GetDisplayName(&pszJobName);
    if (FAILED(hr))
    {
        wprintf(L"Unable to get job name\n");
    }

    hr = pError->GetErrorDescription(GetUserDefaultUILanguage(), &pszErrorDescription);
    if (FAILED(hr))
    {
        wprintf(L"Unable to get error description\n");
    }
    if (pszJobName && pszErrorDescription)
    {
        wprintf(L"Job %s ",pszJobName);
        wprintf(L"encountered the following error:\n");
        wprintf(L"%s\n",pszErrorDescription);
    }
    
    // Clean up
    CoTaskMemFree(pszJobName);
    CoTaskMemFree(pszErrorDescription);

    PostQuitMessage(hr);

    //If you do not return S_OK, BITS continues to call this callback.
    return S_OK;
}
```




<span data-ttu-id="53db8-119">下列標頭檔用於通用程式碼類別。</span><span class="sxs-lookup"><span data-stu-id="53db8-119">The following header file is used for the common code classes.</span></span> <span data-ttu-id="53db8-120">上述程式碼範例會使用這些類別。</span><span class="sxs-lookup"><span data-stu-id="53db8-120">These classes are used in the previous code examples.</span></span>


```C++
// commoncode.h
#pragma once

//
// Exception class used for error handling
//
class MyException
{
public:
    MyException(HRESULT hr, LPWSTR message):Error(hr), Message(message)
    {

    }
    HRESULT Error;
    std::wstring Message;
};

// CoInitialize helper class
class CCoInitializer 
{
public:
    CCoInitializer( DWORD dwCoInit ) 
    { 
        HRESULT hr = CoInitializeEx( NULL, dwCoInit );
        if (FAILED(hr))
        {
            throw MyException(hr,L"CoInitialize");
        }
    } 

    ~CCoInitializer() throw() 
    { 
        CoUninitialize(); 
    } 
};

//
// Implementation of the Callback interface
//
class CNotifyInterface : public IBackgroundCopyCallback
{
    LONG m_lRefCount;

public:
    //Constructor, Destructor
    CNotifyInterface() {m_lRefCount = 1;};
    ~CNotifyInterface() {};

    //IUnknown
    HRESULT __stdcall QueryInterface(REFIID riid, LPVOID *ppvObj);
    ULONG __stdcall AddRef();
    ULONG __stdcall Release();

    //IBackgroundCopyCallback2 methods
    HRESULT __stdcall JobTransferred(IBackgroundCopyJob* pJob);
    HRESULT __stdcall JobError(IBackgroundCopyJob* pJob, IBackgroundCopyError* pError);
    HRESULT __stdcall JobModification(IBackgroundCopyJob* pJob, DWORD dwReserved);
private:
    CNotifyInterface(const CNotifyInterface&);
    CNotifyInterface& operator=(const CNotifyInterface&);
};
```




<span data-ttu-id="53db8-121">下列範例程式碼是通用程式碼類別的實作為。</span><span class="sxs-lookup"><span data-stu-id="53db8-121">The following example code is the implementation of the common code classes.</span></span>


```C++
//commoncode.cpp

#include <bits.h>
#include <bits4_0.h>
#include <stdio.h>
#include <tchar.h>
#include <lm.h>
#include <iostream>
#include <exception>
#include <string>
#include <atlbase.h>
#include <memory>
#include <new>
#include "CommonCode.h"

HRESULT CNotifyInterface::QueryInterface(REFIID riid, LPVOID* ppvObj) 
{
    if (riid == __uuidof(IUnknown) || riid == __uuidof(IBackgroundCopyCallback)) 
    {
        *ppvObj = this;
    }
    else
    {
        *ppvObj = NULL; 
        return E_NOINTERFACE;
    }

    AddRef();
    return NOERROR;
}

ULONG CNotifyInterface::AddRef() 
{
    return InterlockedIncrement(&m_lRefCount);
}

ULONG CNotifyInterface::Release() 
{
    // not thread safe
    ULONG  ulCount = InterlockedDecrement(&m_lRefCount);

    if(0 == ulCount) 
    {
        delete this;
    }

    return ulCount;
}

HRESULT CNotifyInterface::JobTransferred(IBackgroundCopyJob* pJob)
{
    HRESULT hr;

    wprintf(L"Job transferred. Completing Job...\n");
    hr = pJob->Complete();
    if (FAILED(hr))
    {
        //BITS probably was unable to rename one or more of the 
        //temporary files. See the Remarks section of the IBackgroundCopyJob::Complete 
        //method for more details.
        wprintf(L"Job Completion Failed with error %x\n", hr);
    }

    PostQuitMessage(0);

    //If you do not return S_OK, BITS continues to call this callback.
    return S_OK;
}

HRESULT CNotifyInterface::JobModification(IBackgroundCopyJob* pJob, DWORD dwReserved)
{
    return S_OK;
}

HRESULT CNotifyInterface::JobError(IBackgroundCopyJob* pJob, IBackgroundCopyError* pError)
{
    WCHAR* pszJobName = NULL;
    WCHAR* pszErrorDescription = NULL;

    //Use pJob and pError to retrieve information of interest. For example,
    //if the job is an upload reply, call the IBackgroundCopyError::GetError method 
    //to determine the context in which the job failed.

    wprintf(L"Job entered error state...\n");
    HRESULT hr = pJob->GetDisplayName(&pszJobName);
    if (FAILED(hr))
    {
        wprintf(L"Unable to get job name\n");
    }

    hr = pError->GetErrorDescription(GetUserDefaultUILanguage(), &pszErrorDescription);
    if (FAILED(hr))
    {
        wprintf(L"Unable to get error description\n");
    }
    if (pszJobName && pszErrorDescription)
    {
        wprintf(L"Job %s ",pszJobName);
        wprintf(L"encountered the following error:\n");
        wprintf(L"%s\n",pszErrorDescription);
    }

    CoTaskMemFree(pszJobName);
    CoTaskMemFree(pszErrorDescription);

    PostQuitMessage(hr);

    //If you do not return S_OK, BITS continues to call this callback.
    return S_OK;
}
```



## <a name="related-topics"></a><span data-ttu-id="53db8-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="53db8-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53db8-123">IUnknown</span><span class="sxs-lookup"><span data-stu-id="53db8-123">IUnknown</span></span>]( /windows/win32/api/unknwn/nn-unknwn-iunknown)
</dt> <dt>

[<span data-ttu-id="53db8-124">**IBackgroundCopyCallback**</span><span class="sxs-lookup"><span data-stu-id="53db8-124">**IBackgroundCopyCallback**</span></span>](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback)
</dt> <dt>

[<span data-ttu-id="53db8-125">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="53db8-125">**IBackgroundCopyJob**</span></span>](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob)
</dt> <dt>

[<span data-ttu-id="53db8-126">CoInitializeEx</span><span class="sxs-lookup"><span data-stu-id="53db8-126">CoInitializeEx</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex)
</dt> <dt>

[<span data-ttu-id="53db8-127">CoUninitialize</span><span class="sxs-lookup"><span data-stu-id="53db8-127">CoUninitialize</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize)
</dt> </dl>

 

 