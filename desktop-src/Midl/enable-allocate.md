---
title: enable_allocate 屬性
description: '\ Enable \_ allocate \ ACF 屬性指定伺服器 stub 程式碼應啟用存根記憶體管理環境。'
ms.assetid: 3a232a82-f114-4d8c-8b71-cf8860c77db3
keywords:
- enable_allocate 屬性 MIDL
topic_type:
- apiref
api_name:
- enable_allocate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f43e8c10592fcf99ea294327c400c579ce45bf6b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104092664"
---
# <a name="enable_allocate-attribute"></a><span data-ttu-id="86f73-104">啟用 \_ 配置屬性</span><span class="sxs-lookup"><span data-stu-id="86f73-104">enable\_allocate attribute</span></span>

<span data-ttu-id="86f73-105">[ **\[ 啟用 \_ 配置 \]** ACF] 屬性會指定伺服器 stub 程式碼應啟用存根記憶體管理環境。</span><span class="sxs-lookup"><span data-stu-id="86f73-105">The **\[enable\_allocate\]** ACF attribute specifies that the server stub code should enable the stub memory management environment.</span></span>

> [!Note]  
> <span data-ttu-id="86f73-106">**\[ 啟用 \_ 配置 \]** 屬性已淘汰，不再支援。</span><span class="sxs-lookup"><span data-stu-id="86f73-106">The **\[enable\_allocate\]** attribute is obsolete and is no longer supported.</span></span>

 

``` syntax
[
    enable_allocate
  [ , optional-attribute-list]
]
interface interface-name
{
    . . .
};
```

## <a name="parameters"></a><span data-ttu-id="86f73-107">參數</span><span class="sxs-lookup"><span data-stu-id="86f73-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86f73-108">*選用-屬性-清單*</span><span class="sxs-lookup"><span data-stu-id="86f73-108">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="86f73-109">指定零個或多個其他 MIDL 屬性的清單。</span><span class="sxs-lookup"><span data-stu-id="86f73-109">Specifies a list of zero or more additional MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="86f73-110">*介面-名稱*</span><span class="sxs-lookup"><span data-stu-id="86f73-110">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="86f73-111">將套用 **\[ enable \_ allcoate \]** 屬性的介面名稱。</span><span class="sxs-lookup"><span data-stu-id="86f73-111">The name of the interface to which the **\[enable\_allcoate\]** attribute will be applied.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="86f73-112">備註</span><span class="sxs-lookup"><span data-stu-id="86f73-112">Remarks</span></span>

<span data-ttu-id="86f73-113">在預設模式下，只有在使用「 **\[ 啟用 \_ 配置 \]** 」屬性時，伺服器 stub 才會啟用記憶體環境。</span><span class="sxs-lookup"><span data-stu-id="86f73-113">In default mode, the server stub enables the memory environment only when the **\[enable\_allocate\]** attribute is used.</span></span> <span data-ttu-id="86f73-114">記憶體管理環境必須先啟用，才能使用 [**RpcSmAllocate**](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmallocate)來配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="86f73-114">The memory management environment must be enabled before memory can be allocated using [**RpcSmAllocate**](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmallocate).</span></span> <span data-ttu-id="86f73-115">在 **憑證** 模式中 (當您使用 [**/osf**](-osf.md)參數) 進行編譯時，存根會自動啟用此環境，或在使用 **\[ 啟用 \_ 配置 \]** 屬性時，于要求上啟用。</span><span class="sxs-lookup"><span data-stu-id="86f73-115">In **osf** mode (when you compile using the [**/osf**](-osf.md) switch), the stub enables this environment automatically, or on request when the **\[enable\_allocate\]** attribute is used.</span></span>

<span data-ttu-id="86f73-116">用戶端 stub 可能會對「 **Rpcss** 記憶體管理」環境很敏感。</span><span class="sxs-lookup"><span data-stu-id="86f73-116">The client side stub may be sensitive to the **Rpcss** memory management environment.</span></span> <span data-ttu-id="86f73-117">如果在停用 **Rpcss** 套件時執行敏感性用戶端存根，則會 (呼叫預設的使用者配置器/解除配置器，例如 [midl \_ 使用者 \_ 配置](/windows/desktop/Rpc/the-midl-user-allocate-function) /  [midl \_ 使用者 \_ free](/windows/desktop/Rpc/the-midl-user-free-function)) 。</span><span class="sxs-lookup"><span data-stu-id="86f73-117">If a sensitive client stub is executed when the **Rpcss** package is disabled, the default user allocator/deallocators are called (for example, [midl\_user\_allocate](/windows/desktop/Rpc/the-midl-user-allocate-function)/ [midl\_user\_free](/windows/desktop/Rpc/the-midl-user-free-function)).</span></span> <span data-ttu-id="86f73-118">啟用時， **Rpcss** 封裝會使用套件中的配置器/釋放器組。</span><span class="sxs-lookup"><span data-stu-id="86f73-118">When enabled, the **Rpcss** package uses the allocator/deallocator pair from the package.</span></span> <span data-ttu-id="86f73-119">在預設模式下，只有在使用「 **\[ 啟用 \_ 配置 \]** 」屬性時，用戶端才是敏感的。</span><span class="sxs-lookup"><span data-stu-id="86f73-119">In the default mode, the client is sensitive only when the **\[enable\_allocate\]** attribute is used.</span></span> <span data-ttu-id="86f73-120">一般而言，用戶端 stub 會在停用的環境中運作。</span><span class="sxs-lookup"><span data-stu-id="86f73-120">Typically, the client side stub operates in the disabled environment.</span></span> <span data-ttu-id="86f73-121">在 **憑證** 模式中 (當您使用 [**/osf**](-osf.md)參數) 進行編譯時，用戶端一律會受到 **Rpcss** 記憶體管理環境的影響，因此， **\[ 啟用 \_ 配置 \]** 屬性不會影響用戶端存根。</span><span class="sxs-lookup"><span data-stu-id="86f73-121">In **osf** mode (when you compile using the [**/osf**](-osf.md) switch), the client is always sensitive to the **Rpcss** memory management environment and, therefore, the **\[enable\_allocate\]** attribute will not affect the client stubs.</span></span>

## <a name="see-also"></a><span data-ttu-id="86f73-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="86f73-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86f73-123">應用程式佈建檔 (ACF) </span><span class="sxs-lookup"><span data-stu-id="86f73-123">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="86f73-124">midl \_ 使用者 \_ 配置</span><span class="sxs-lookup"><span data-stu-id="86f73-124">midl\_user\_allocate</span></span>](/windows/desktop/Rpc/the-midl-user-allocate-function)
</dt> <dt>

[<span data-ttu-id="86f73-125">midl \_ 使用者 \_ 免費</span><span class="sxs-lookup"><span data-stu-id="86f73-125">midl\_user\_free</span></span>](/windows/desktop/Rpc/the-midl-user-free-function)
</dt> <dt>

[<span data-ttu-id="86f73-126">**/osf**</span><span class="sxs-lookup"><span data-stu-id="86f73-126">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="86f73-127">RpcSmDisableAllocate</span><span class="sxs-lookup"><span data-stu-id="86f73-127">RpcSmDisableAllocate</span></span>](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmdisableallocate)
</dt> <dt>

[<span data-ttu-id="86f73-128">RpcSmEnableAllocate</span><span class="sxs-lookup"><span data-stu-id="86f73-128">RpcSmEnableAllocate</span></span>](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmenableallocate)
</dt> <dt>

[<span data-ttu-id="86f73-129">RpcSmFree</span><span class="sxs-lookup"><span data-stu-id="86f73-129">RpcSmFree</span></span>](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmfree)
</dt> </dl>

 

 