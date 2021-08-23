---
title: 宣告非同步函式
description: 若要將 RPC 函式宣告為非同步，請先在介面定義語言 (IDL) 檔中，將函式宣告為介面定義的一部分。
ms.assetid: 8fc627ce-ccf1-40d9-a540-14461c7fc5e1
keywords:
- 遠端程序呼叫 RPC、工作、宣告非同步函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fc0978156fe91291b91937082690258550b7f02f1d7b6e5334dd0741a9f0211
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118931046"
---
# <a name="declaring-asynchronous-functions"></a>宣告非同步函式

若要將 RPC 函式宣告為非同步，請先在介面定義語言 (IDL) 檔中，將函式宣告為介面定義的一部分。 使用非同步 RPC 函式不需要對 IDL 檔案進行任何特殊變更。 下列範例顯示使用一個非同步函式的應用程式的 IDL 檔案。

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

針對您的應用程式使用的所有非同步 RPC 函式，您必須在應用程式的 ACF 檔內修改非同步函式的宣告。 將 [**\[ async \]**](../midl/async.md)屬性套用至每個非同步函式名稱，如下列範例所示：

``` syntax
interface AsyncRPC
{
    [async] AsyncFunc();
}
```

當您在 ACF 檔中套用 **\[ async \]** 屬性時，MIDL 編譯器會在存根程式碼中自動產生額外的非同步控制碼參數。

 

 