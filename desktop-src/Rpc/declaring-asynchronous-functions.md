---
title: 宣告非同步函式
description: 若要將 RPC 函式宣告為非同步，請先在介面定義語言 (IDL) 檔中，將函式宣告為介面定義的一部分。
ms.assetid: 8fc627ce-ccf1-40d9-a540-14461c7fc5e1
keywords:
- 遠端程序呼叫 RPC、工作、宣告非同步函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fafc1208d53763835d72f527723d00816f38db9
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/08/2020
ms.locfileid: "103933687"
---
# <a name="declaring-asynchronous-functions"></a><span data-ttu-id="cf423-104">宣告非同步函式</span><span class="sxs-lookup"><span data-stu-id="cf423-104">Declaring Asynchronous Functions</span></span>

<span data-ttu-id="cf423-105">若要將 RPC 函式宣告為非同步，請先在介面定義語言 (IDL) 檔中，將函式宣告為介面定義的一部分。</span><span class="sxs-lookup"><span data-stu-id="cf423-105">To declare an RPC function as asynchronous, first declare the function as part of an interface definition in an Interface Definition Language (IDL) file.</span></span> <span data-ttu-id="cf423-106">使用非同步 RPC 函式不需要對 IDL 檔案進行任何特殊變更。</span><span class="sxs-lookup"><span data-stu-id="cf423-106">The use of asynchronous RPC functions does not require any special alterations to your IDL file.</span></span> <span data-ttu-id="cf423-107">下列範例顯示使用一個非同步函式的應用程式的 IDL 檔案。</span><span class="sxs-lookup"><span data-stu-id="cf423-107">The following example shows an IDL file for an application that uses one asynchronous function.</span></span>

``` syntax
[ 
    uuid (7f6c4340-eb67-11d1-b9d7-00c04fad9a3b),
    version(1.0),
    pointer_default(unique)
]
interface AsyncRPC
{
    const long DEFAULT_ASYNC_DELAY        = 10000;
    const short APP_ERROR                 = -1;
    const char* DEFAULT_PROTOCOL_SEQUENCE = "ncacn_ip_tcp";
    const char* DEFAULT_ENDPOINT          = "8765";
 
    void NonAsyncFunc(handle_t hBinding,
                      [in, string] unsigned char * pszMessage);
 
    void AsyncFunc(handle_t hBinding,
                   [in] unsigned long nAsychDelay);
 
    void Shutdown(handle_t hBinding);
}
```

<span data-ttu-id="cf423-108">針對您的應用程式使用的所有非同步 RPC 函式，您必須在應用程式的 ACF 檔內修改非同步函式的宣告。</span><span class="sxs-lookup"><span data-stu-id="cf423-108">For all asynchronous RPC functions that your application uses, you will need to modify the declaration of the asynchronous functions within your application's ACF file.</span></span> <span data-ttu-id="cf423-109">將 [**\[ async \]**](../midl/async.md)屬性套用至每個非同步函式名稱，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="cf423-109">Apply the [**\[async\]**](../midl/async.md) attribute to each asynchronous function name, as shown in the following example:</span></span>

``` syntax
interface AsyncRPC
{
    [async] AsyncFunc();
}
```

<span data-ttu-id="cf423-110">當您在 ACF 檔中套用 **\[ async \]** 屬性時，MIDL 編譯器會在存根程式碼中自動產生額外的非同步控制碼參數。</span><span class="sxs-lookup"><span data-stu-id="cf423-110">When you apply the **\[async\]** attribute in the ACF file, the MIDL compiler automatically generates an additional asynchronous handle parameter in the stub code.</span></span>

 

 