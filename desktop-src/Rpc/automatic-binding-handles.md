---
title: 自動系結控制碼
description: 當應用程式不需要特定伺服器，且不需要維護用戶端與伺服器之間的任何狀態資訊時，自動系結控制碼會很有用。
ms.assetid: ba049369-6c8b-4313-a266-e0364a30056e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fe83d3f9029e0384c87e5e409583ff70f1e91ac
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316114"
---
# <a name="automatic-binding-handles"></a><span data-ttu-id="35043-103">自動系結控制碼</span><span class="sxs-lookup"><span data-stu-id="35043-103">Automatic Binding Handles</span></span>

<span data-ttu-id="35043-104">當應用程式不需要特定伺服器，且不需要維護用戶端與伺服器之間的任何狀態資訊時，自動系結控制碼會很有用。</span><span class="sxs-lookup"><span data-stu-id="35043-104">Automatic binding handles are useful when the application does not require a specific server and when it does not need to maintain any state information between the client and server.</span></span> <span data-ttu-id="35043-105">當您使用自動系結控制碼時，不需要撰寫任何用戶端應用程式程式碼來處理系結和控制碼，只要在應用程式佈建檔中指定自動系結控制碼的使用 (ACF) 。</span><span class="sxs-lookup"><span data-stu-id="35043-105">When you use an automatic binding handle, you do not have to write any client application code to deal with binding and handles—you simply specify the use of the automatic binding handle in the application configuration file (ACF).</span></span> <span data-ttu-id="35043-106">然後，存根會定義控制碼並管理系結。</span><span class="sxs-lookup"><span data-stu-id="35043-106">The stub then defines the handle and manages the binding.</span></span>

<span data-ttu-id="35043-107">例如，您可以使用自動控制碼來執行時間戳記作業。</span><span class="sxs-lookup"><span data-stu-id="35043-107">For example, a time-stamp operation can be implemented using an auto handle.</span></span> <span data-ttu-id="35043-108">它不會與用戶端應用程式產生任何差異，因為它可以接受來自任何可用伺服器的時間戳記，而伺服器會提供時間戳記。</span><span class="sxs-lookup"><span data-stu-id="35043-108">It makes no difference to the client application which server provides it with the time stamp because it can accept the time from any available server.</span></span>

> [!Note]  
> <span data-ttu-id="35043-109">Macintosh 平臺不支援自動控制碼。</span><span class="sxs-lookup"><span data-stu-id="35043-109">Auto handles are not supported for the Macintosh platform.</span></span>

 

<span data-ttu-id="35043-110">您可以 \[ 在 ACF 中包含 [**auto \_ 控制碼**](/windows/desktop/Midl/auto-handle)屬性，藉以指定自動控制碼的使用方式 \] 。</span><span class="sxs-lookup"><span data-stu-id="35043-110">You specify the use of auto handles by including the \[[**auto\_handle**](/windows/desktop/Midl/auto-handle)\] attribute in the ACF.</span></span> <span data-ttu-id="35043-111">時間戳記範例會使用下列 ACF：</span><span class="sxs-lookup"><span data-stu-id="35043-111">The time-stamp example uses the following ACF:</span></span>

``` syntax
/* ACF file */
[
  auto_handle
]
interface autoh
{
}
```

<span data-ttu-id="35043-112">當 ACF 不包含任何其他控制碼屬性時，以及遠端程式未使用明確控制碼時，MIDL 編譯器預設會使用自動控制碼。</span><span class="sxs-lookup"><span data-stu-id="35043-112">When the ACF does not include any other handle attribute, and when the remote procedures do not use explicit handles, the MIDL compiler uses automatic handles by default.</span></span> <span data-ttu-id="35043-113">當 ACF 不存在時，它也會使用自動控制碼作為預設值。</span><span class="sxs-lookup"><span data-stu-id="35043-113">It also uses automatic handles as the default when the ACF is not present.</span></span>

<span data-ttu-id="35043-114">遠端程式是在 IDL 檔案中指定。</span><span class="sxs-lookup"><span data-stu-id="35043-114">The remote procedures are specified in the IDL file.</span></span> <span data-ttu-id="35043-115">Auto 控制碼不能顯示為遠端程式的引數。</span><span class="sxs-lookup"><span data-stu-id="35043-115">The auto handle must not appear as an argument to the remote procedure.</span></span> <span data-ttu-id="35043-116">例如：</span><span class="sxs-lookup"><span data-stu-id="35043-116">For example:</span></span>

``` syntax
/* IDL file */
[ 
  uuid (6B29FC40-CA47-1067-B31D-00DD010662DA),
  version(1.0),
  pointer_default(unique)
]
interface autoh
{
  void GetTime([out] long * time);
  void Shutdown(void);
}
```

<span data-ttu-id="35043-117">自動控制碼的優點是，開發人員不需要撰寫任何程式碼來管理控制碼;存根會自動管理系結。</span><span class="sxs-lookup"><span data-stu-id="35043-117">The benefit of the auto handle is that the developer does not have to write any code to manage the handle; the stubs manage the binding automatically.</span></span> <span data-ttu-id="35043-118">這與 [Hello，World 範例](tutorial.md)截然不同，因為用戶端會管理 ACF 中定義的隱含基本控制碼，而且必須呼叫數個執行時間函數來建立系結控制碼。</span><span class="sxs-lookup"><span data-stu-id="35043-118">This is significantly different from the [Hello, World example](tutorial.md), where the client manages the implicit primitive handle defined in the ACF and must call several run-time functions to establish the binding handle.</span></span>

 

 