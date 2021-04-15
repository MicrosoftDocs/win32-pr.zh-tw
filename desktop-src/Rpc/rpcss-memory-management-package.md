---
title: RpcSs 記憶體管理套件
description: 在代表應用程式佈建記憶體時，存根和執行時間所使用的預設配置器/釋放器組是 midl \_ 使用者 \_ 配置/midl \_ 使用者 \_ 免費。
ms.assetid: 9477e677-59cb-45d5-b485-ab0171ac17ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26dca10ebea44fbb202240e981612e16e7960216
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463536"
---
# <a name="rpcss-memory-management-package"></a><span data-ttu-id="65c73-103">RpcSs 記憶體管理套件</span><span class="sxs-lookup"><span data-stu-id="65c73-103">RpcSs Memory Management Package</span></span>

<span data-ttu-id="65c73-104">在代表應用程式佈建記憶體時，存根和執行時間所使用的預設配置器/釋放器組是 **midl \_ 使用者 \_** / **\_ \_ 免費配置 midl 使用者**。</span><span class="sxs-lookup"><span data-stu-id="65c73-104">The default allocator/deallocator pair used by the stubs and run time when allocating memory on behalf of the application is **midl\_user\_allocate**/**midl\_user\_free**.</span></span> <span data-ttu-id="65c73-105">不過，您可以使用 ACF 屬性 **\[ 啟用 \_ 配置 \]** 來選擇 RpcSs 封裝，而不是預設值。</span><span class="sxs-lookup"><span data-stu-id="65c73-105">However, you can choose the RpcSs package instead of the default by using the ACF attribute **\[enable\_allocate\]**.</span></span> <span data-ttu-id="65c73-106">此 RpcSs 封裝包含以首碼 **RpcSs** 或 **RPCSM** 開頭的 RPC 函數。</span><span class="sxs-lookup"><span data-stu-id="65c73-106">The RpcSs package consists of RPC functions that begin with the prefix **RpcSs** or **RpcSm**.</span></span> <span data-ttu-id="65c73-107">Windows 應用程式不建議使用此 RpcSs 套件。</span><span class="sxs-lookup"><span data-stu-id="65c73-107">The RpcSs package is not recommended for Windows applications.</span></span>

> [!Note]  
> <span data-ttu-id="65c73-108">Rpcss 記憶體管理套件已過時。</span><span class="sxs-lookup"><span data-stu-id="65c73-108">The Rpcss Memory Management Package is obsolete.</span></span> <span data-ttu-id="65c73-109">建議您在其位置使用 [**midl \_ 使用者 \_ 配置**](/windows/desktop/Midl/midl-user-allocate-1) 和 [**midl \_ 使用者 \_ 免費**](/windows/desktop/Midl/midl-user-free-1) 。</span><span class="sxs-lookup"><span data-stu-id="65c73-109">It is recommended that [**midl\_user\_allocate**](/windows/desktop/Midl/midl-user-allocate-1) and [**midl\_user\_free**](/windows/desktop/Midl/midl-user-free-1) are used in its place.</span></span>

 

<span data-ttu-id="65c73-110">在 **/osf** 模式中，使用完整的指標時，會自動啟用 MIDL 產生的存根、引數需要記憶體配置，或做為使用 [ **\[ 啟用 \_ 配置 \]** ] 屬性的結果。</span><span class="sxs-lookup"><span data-stu-id="65c73-110">In **/osf** mode, the RpcSs package is enabled for MIDL-generated stubs automatically when full pointers are used, when the arguments require memory allocation, or as a result of using the **\[enable\_allocate\]** attribute.</span></span> <span data-ttu-id="65c73-111">在預設 (Microsoft 擴充) 模式下，只有在使用 [ **\[ 啟用 \_ 配置 \]** ] 屬性時，才會啟用 RpcSs 套件。</span><span class="sxs-lookup"><span data-stu-id="65c73-111">In the default (Microsoft extended) mode, the RpcSs package is enabled only when the **\[enable\_allocate\]** attribute is used.</span></span> <span data-ttu-id="65c73-112">[ **\[ 啟用 \_ 配置 \]** ] 屬性會依伺服器端的存根啟用 RpcSs 環境。</span><span class="sxs-lookup"><span data-stu-id="65c73-112">The **\[enable\_allocate\]** attribute enables the RpcSs environment by the server-side stubs.</span></span> <span data-ttu-id="65c73-113">用戶端會收到可能啟用 RpcSs 封裝的警示。</span><span class="sxs-lookup"><span data-stu-id="65c73-113">The client side becomes alerted to the possibility that the RpcSs package may be enabled.</span></span> <span data-ttu-id="65c73-114">在 **/osf** 模式中，用戶端不會受到影響。</span><span class="sxs-lookup"><span data-stu-id="65c73-114">In **/osf** mode, the client side is not affected.</span></span>

<span data-ttu-id="65c73-115">啟用 RpcSs 封裝之後，就會使用私用的 RpcSs 記憶體管理配置器和釋放器配對來完成伺服器端的記憶體配置。</span><span class="sxs-lookup"><span data-stu-id="65c73-115">When the RpcSs package is enabled, allocation of memory on the server side is accomplished with the private RpcSs memory management allocator and deallocator pair.</span></span> <span data-ttu-id="65c73-116">您可以使用相同的機制來配置記憶體，方法是呼叫 [**RpcSmAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmallocate) (或 [**RpcSsAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssallocate)) 。</span><span class="sxs-lookup"><span data-stu-id="65c73-116">You can allocate memory using the same mechanism by calling [**RpcSmAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmallocate) (or [**RpcSsAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssallocate)).</span></span> <span data-ttu-id="65c73-117">從伺服器 stub 傳回時，會自動釋放由 RpcSs 封裝配置的所有記憶體。</span><span class="sxs-lookup"><span data-stu-id="65c73-117">Upon return from the server stub, all the memory allocated by the RpcSs package is automatically freed.</span></span> <span data-ttu-id="65c73-118">下列範例顯示如何啟用 RpcSs 套件：</span><span class="sxs-lookup"><span data-stu-id="65c73-118">The following example shows how to enable the RpcSs package:</span></span>

``` syntax
/* ACF file fragment */

[ 
    implicit_handle(handle_t GlobalHandle),
    enable_allocate
]
interface iface
{
}

/*Server management routine fragment. Replaces p=midl_user_allocate(size); */

    p=RpcSsAllocate(size);                /*raises exception */
    p=RpcSmAllocate(size, &status);       /*returns error code */
```

<span data-ttu-id="65c73-119">您的應用程式可以藉由叫用 [**RpcSsFree**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssfree) 或 [**RpcSmFree**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmfree) 函式來明確釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="65c73-119">Your application can explicitly free memory by invoking the [**RpcSsFree**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssfree) or [**RpcSmFree**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmfree) function.</span></span> <span data-ttu-id="65c73-120">請注意，這些函數實際上並不會釋出記憶體。</span><span class="sxs-lookup"><span data-stu-id="65c73-120">Note that these functions do not actually free memory.</span></span> <span data-ttu-id="65c73-121">他們將其標示為刪除。</span><span class="sxs-lookup"><span data-stu-id="65c73-121">They mark it for deletion.</span></span> <span data-ttu-id="65c73-122">當您的程式呼叫 [**RpcSsDisableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdisableallocate) 或 [**RPCSSDISABLEALLOCATE**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdisableallocate)時，RPC 程式庫會釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="65c73-122">The RPC library releases the memory when your program calls [**RpcSsDisableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdisableallocate) or [**RpcSsDisableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdisableallocate).</span></span>

<span data-ttu-id="65c73-123">您也可以藉由呼叫 [**RpcSmEnableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmenableallocate) 常式 (為您的應用程式啟用記憶體管理環境，也可以藉由呼叫 [**RpcSmDisableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmdisableallocate) 常式) 來停用它。</span><span class="sxs-lookup"><span data-stu-id="65c73-123">You can also enable the memory management environment for your application by calling the [**RpcSmEnableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmenableallocate) routine (and you can disable it by calling the [**RpcSmDisableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmdisableallocate) routine).</span></span> <span data-ttu-id="65c73-124">啟用之後，應用程式程式碼就可以從 RpcSs 封裝呼叫函式，以配置和解除配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="65c73-124">Once enabled, application code can allocate and deallocate memory by calling functions from the RpcSs package.</span></span>

 

 