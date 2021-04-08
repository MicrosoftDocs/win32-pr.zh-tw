---
title: 產生 UUID
description: 定義介面的第一個步驟是使用 uuidgen.exe 公用程式來產生 (UUID) 的通用唯一識別碼。
ms.assetid: 870641b7-affc-4de4-bc7f-4c8ca2873fb6
keywords:
- 遠端程序呼叫 RPC、工作、產生 UUID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e263bfe21c4a564106c0d6328c0de891c18bca1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839951"
---
# <a name="generating-the-uuid"></a><span data-ttu-id="8adfc-104">產生 UUID</span><span class="sxs-lookup"><span data-stu-id="8adfc-104">Generating the UUID</span></span>

<span data-ttu-id="8adfc-105">定義介面的第一個步驟是使用 **uuidgen.exe** 公用程式來產生 (UUID) 的通用唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="8adfc-105">The first step in defining the interface is to use the **uuidgen** utility to generate a universally unique identifier (UUID).</span></span> <span data-ttu-id="8adfc-106">UUID 可讓用戶端和伺服器應用程式彼此識別。</span><span class="sxs-lookup"><span data-stu-id="8adfc-106">A UUID enables the client and server applications identify each other.</span></span> <span data-ttu-id="8adfc-107">當您安裝平臺軟體發展工具組 (SDK) 時，會自動安裝 **uuidgen.exe** 公用程式 (Uuidgen.exe) 。</span><span class="sxs-lookup"><span data-stu-id="8adfc-107">The **uuidgen** utility (Uuidgen.exe) is automatically installed when you install the Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="8adfc-108">下列命令會產生 UUID，並建立名為 Hello 的範本檔案。</span><span class="sxs-lookup"><span data-stu-id="8adfc-108">The following command generates a UUID and creates a template file called Hello.idl.</span></span>

<span data-ttu-id="8adfc-109">**uuidgen.exe/i/ohello.idl**</span><span class="sxs-lookup"><span data-stu-id="8adfc-109">**uuidgen /i /ohello.idl**</span></span>

<span data-ttu-id="8adfc-110">當然，您的 hello .idl 範本看起來會像這樣 (使用不同的 UUID) 。</span><span class="sxs-lookup"><span data-stu-id="8adfc-110">Your hello.idl template will look like this (with a different UUID, of course).</span></span>

``` syntax
[
    uuid(7a98c250-6808-11cf-b73b-00aa00b677a7),
    version(1.0)
]
interface INTERFACENAME
{
 
}
```

 

 




