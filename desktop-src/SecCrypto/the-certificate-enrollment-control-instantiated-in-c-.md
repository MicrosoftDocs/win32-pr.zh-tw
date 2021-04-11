---
description: 在 c + + 中具現化的憑證註冊控制項
ms.assetid: 19dd2fce-b4a9-44fd-9572-897ee7943914
title: 在 c + + 中具現化的憑證註冊控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 868f89e0a285460c587a924e84a5ed21c202eb0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695619"
---
# <a name="the-certificate-enrollment-control-instantiated-in-c"></a><span data-ttu-id="aa69a-103">在 c + + 中具現化的憑證註冊控制項</span><span class="sxs-lookup"><span data-stu-id="aa69a-103">The Certificate Enrollment Control Instantiated in C++</span></span>

<span data-ttu-id="aa69a-104">下列 c + + 範例會初始化 COM、建立 [憑證註冊控制項](certificate-enrollment-control.md)的實例、使用憑證註冊控制項，以及釋出資源。</span><span class="sxs-lookup"><span data-stu-id="aa69a-104">The following C++ example initializes COM, creates an instance of the [Certificate Enrollment Control](certificate-enrollment-control.md), uses the Certificate Enrollment Control, and frees resources.</span></span>

## <a name="example-in-c"></a><span data-ttu-id="aa69a-105">C + + 中的範例</span><span class="sxs-lookup"><span data-stu-id="aa69a-105">Example in C++</span></span>

<span data-ttu-id="aa69a-106">下列範例會建立 [憑證註冊控制項](certificate-enrollment-control.md) 的實例，並顯示 [**MyStoreName**](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_mystorename) 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="aa69a-106">The following example creates an instance of the [Certificate Enrollment Control](certificate-enrollment-control.md) and displays the value of the [**MyStoreName**](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_mystorename) property.</span></span> <span data-ttu-id="aa69a-107">這個範例會使用 [**ICEnroll4**](/windows/desktop/api/Xenroll/nn-xenroll-icenroll4) 介面。</span><span class="sxs-lookup"><span data-stu-id="aa69a-107">This example uses the [**ICEnroll4**](/windows/desktop/api/Xenroll/nn-xenroll-icenroll4) interface.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <xenroll.h>

// Copyright (C) Microsoft.  All rights reserved.
HRESULT __cdecl main(void)
{
    HRESULT hr = 0;
    ICEnroll4 *pEnroll = NULL;
    BSTR bstrStoreName = NULL;

    // Initialize COM.
    hr = CoInitializeEx( NULL, COINIT_APARTMENTTHREADED );
    if ( FAILED( hr ) )
    {
        printf("Failed CoInitializeEx - [0x%x]\n", hr);
        exit(hr);
    }

    // Create an instance of the object.
    hr = CoCreateInstance( __uuidof(CEnroll),
                           NULL,
                           CLSCTX_INPROC_SERVER,
                           __uuidof(ICEnroll4),
                           (void **)&pEnroll);
    if ( FAILED( hr ) )
    {
        printf("Failed CoCreateInstance - pEnroll [0x%x]\n", hr);
        exit(hr);
    }

    hr = pEnroll->get_MyStoreName(&bstrStoreName);
    if (SUCCEEDED(hr))
    {
        printf("The value of MyStoreName is %ws\n", bstrStoreName);
    }
    else
    {
        printf("pEnroll->GetMyStoreName failed: 0x%x\n", hr);
    }

    pEnroll->Release();
    SysFreeString(bstrStoreName);
    CoUninitialize();

    return hr;
}
```



 

 
