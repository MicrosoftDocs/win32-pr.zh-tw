---
description: 網路監視器會將所有的捕獲框架傳遞給剖析器，然後開始針對其識別的所有通訊協定呼叫取消註冊函式。 每個剖析器 DLL 都必須針對剖析器 DLL 支援的每個通訊協定，執行取消註冊函式。
ms.assetid: 936d5b00-b0ee-4a29-9396-1e2a7a91a2dd
title: 執行取消註冊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 444502ba3ab19921a6372d4cda872aed85e879cbbdadc2f0176a7187bfc24491
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890478"
---
# <a name="implementing-deregister"></a>執行取消註冊

網路監視器會將所有的捕獲框架傳遞給剖析器，然後開始針對其識別的所有通訊協定呼叫取消 [**註冊**](deregister.md) 函式。 每個剖析器 DLL 都必須針對剖析器 DLL 支援的每個通訊協定，執行取消 **註冊** 函式。

取消 [**註冊**](deregister.md) 函式的每個執行都必須呼叫 [**DestroyProtocolDatabase**](destroypropertydatabase.md) 函數，以釋放用來建立資料庫的資源。

下列程式識別執行取消 [**註冊**](deregister.md)所需的一個步驟。

**針對一個通訊協定執行取消註冊**

-   呼叫 [**DestroyProtocolDatabase**](destroypropertydatabase.md) 以釋放資料庫資源。

以下是取消 [**註冊**](deregister.md)的基本執行。 請注意，程式碼範例會顯示用來建立屬性資料庫的資源版本。

``` syntax
#include <windows.h>

VOID WINAPI MyProtocolDeregister (HPROTOCOL hProtocol)
{
  DestroyPropertyDatabase (hProtocol);
}
```

 

 



