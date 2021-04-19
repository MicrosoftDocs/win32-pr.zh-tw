---
description: 網路監視器會將所有的捕獲框架傳遞給剖析器，然後開始針對其識別的所有通訊協定呼叫取消註冊函式。 每個剖析器 DLL 都必須針對剖析器 DLL 支援的每個通訊協定，執行取消註冊函式。
ms.assetid: 936d5b00-b0ee-4a29-9396-1e2a7a91a2dd
title: 執行取消註冊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ee07c5b6b3c746e9c29811332b9e7674e49db26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106999853"
---
# <a name="implementing-deregister"></a><span data-ttu-id="4c7dc-104">執行取消註冊</span><span class="sxs-lookup"><span data-stu-id="4c7dc-104">Implementing Deregister</span></span>

<span data-ttu-id="4c7dc-105">網路監視器會將所有的捕獲框架傳遞給剖析器，然後開始針對其識別的所有通訊協定呼叫取消 [**註冊**](deregister.md) 函式。</span><span class="sxs-lookup"><span data-stu-id="4c7dc-105">Network Monitor passes all the frames of a capture to the parsers, and then starts calling the [**Deregister**](deregister.md) function for all the protocols it identifies.</span></span> <span data-ttu-id="4c7dc-106">每個剖析器 DLL 都必須針對剖析器 DLL 支援的每個通訊協定，執行取消 **註冊** 函式。</span><span class="sxs-lookup"><span data-stu-id="4c7dc-106">Each parser DLL must implement a **Deregister** function for each protocol that the parser DLL supports.</span></span>

<span data-ttu-id="4c7dc-107">取消 [**註冊**](deregister.md) 函式的每個執行都必須呼叫 [**DestroyProtocolDatabase**](destroypropertydatabase.md) 函數，以釋放用來建立資料庫的資源。</span><span class="sxs-lookup"><span data-stu-id="4c7dc-107">Each implementation of the [**Deregister**](deregister.md) function must call the [**DestroyProtocolDatabase**](destroypropertydatabase.md) function to release the resources that are used to create the database.</span></span>

<span data-ttu-id="4c7dc-108">下列程式識別執行取消 [**註冊**](deregister.md)所需的一個步驟。</span><span class="sxs-lookup"><span data-stu-id="4c7dc-108">The following procedure identifies the one step necessary to implement [**Deregister**](deregister.md).</span></span>

<span data-ttu-id="4c7dc-109">**針對一個通訊協定執行取消註冊**</span><span class="sxs-lookup"><span data-stu-id="4c7dc-109">**To implement Deregister for one protocol**</span></span>

-   <span data-ttu-id="4c7dc-110">呼叫 [**DestroyProtocolDatabase**](destroypropertydatabase.md) 以釋放資料庫資源。</span><span class="sxs-lookup"><span data-stu-id="4c7dc-110">Call [**DestroyProtocolDatabase**](destroypropertydatabase.md) to release the database resources.</span></span>

<span data-ttu-id="4c7dc-111">以下是取消 [**註冊**](deregister.md)的基本執行。</span><span class="sxs-lookup"><span data-stu-id="4c7dc-111">The following is a basic implementation of [**Deregister**](deregister.md).</span></span> <span data-ttu-id="4c7dc-112">請注意，程式碼範例會顯示用來建立屬性資料庫的資源版本。</span><span class="sxs-lookup"><span data-stu-id="4c7dc-112">Note that the code example shows the release of resources that are used to create a property database.</span></span>

``` syntax
#include <windows.h>

VOID WINAPI MyProtocolDeregister (HPROTOCOL hProtocol)
{
  DestroyPropertyDatabase (hProtocol);
}
```

 

 



