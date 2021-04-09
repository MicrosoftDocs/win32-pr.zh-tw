---
title: 套用至參數的指標屬性
description: 每個指標屬性 ( \ ref \、\ unique \ 和 \ ptr \ ) 都有影響記憶體配置的特性。 下表摘要說明這些特性。
ms.assetid: 25a609cd-efe7-4cbb-b80e-b6a3ad8cda38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c7710fb3c39702b2b2fdb789ed1218dc88d44ea
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023923"
---
# <a name="pointer-attributes-applied-to-the-parameter"></a><span data-ttu-id="6d14f-104">套用至參數的指標屬性</span><span class="sxs-lookup"><span data-stu-id="6d14f-104">Pointer Attributes Applied to the Parameter</span></span>

<span data-ttu-id="6d14f-105">每個指標屬性 (\[ [ref](/windows/desktop/Midl/ref) \] 、 \[ [unique](/windows/desktop/Midl/unique) \] 和 \[ [ptr](/windows/desktop/Midl/ptr) \]) 都有影響記憶體配置的特性。</span><span class="sxs-lookup"><span data-stu-id="6d14f-105">Each pointer attribute (\[ [ref](/windows/desktop/Midl/ref)\], \[ [unique](/windows/desktop/Midl/unique)\], and \[ [ptr](/windows/desktop/Midl/ptr)\]) has characteristics that affect memory allocation.</span></span> <span data-ttu-id="6d14f-106">下表摘要說明這些特性。</span><span class="sxs-lookup"><span data-stu-id="6d14f-106">The following table summarizes these characteristics.</span></span>



| <span data-ttu-id="6d14f-107">指標屬性</span><span class="sxs-lookup"><span data-stu-id="6d14f-107">Pointer attribute</span></span>       | <span data-ttu-id="6d14f-108">用戶端</span><span class="sxs-lookup"><span data-stu-id="6d14f-108">Client</span></span>                                                                                                                                                                                                            | <span data-ttu-id="6d14f-109">伺服器</span><span class="sxs-lookup"><span data-stu-id="6d14f-109">Server</span></span>                                                              |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="6d14f-110">參考 (\[ **ref** \]) </span><span class="sxs-lookup"><span data-stu-id="6d14f-110">Reference (\[**ref**\])</span></span> | <span data-ttu-id="6d14f-111">用戶端應用程式必須配置。</span><span class="sxs-lookup"><span data-stu-id="6d14f-111">Client application must allocate.</span></span>                                                                                                                                                                                 | <span data-ttu-id="6d14f-112">僅限 **\[ out \]** nontop 層級指標所需的特殊處理。</span><span class="sxs-lookup"><span data-stu-id="6d14f-112">Special handling needed for **\[out\]**-only nontop-level pointers.</span></span> |
| <span data-ttu-id="6d14f-113">唯一 (\[ **唯一** \]) </span><span class="sxs-lookup"><span data-stu-id="6d14f-113">Unique (\[**unique**\])</span></span> | <span data-ttu-id="6d14f-114">如果是參數，用戶端應用程式必須配置;如果是內嵌的，可以是 null。</span><span class="sxs-lookup"><span data-stu-id="6d14f-114">If a parameter, the client application must allocate; if embedded, can be null.</span></span> <span data-ttu-id="6d14f-115">從 null 變更為非 null 會導致用戶端存根配置;從非 null 變更為 null 可能會導致損壞。</span><span class="sxs-lookup"><span data-stu-id="6d14f-115">Changing from null to non-null causes the client stub to allocate; changing from non-null to null can cause orphaning.</span></span><br/> |                                                                     |
| <span data-ttu-id="6d14f-116">完整 (\[ **ptr** \]) </span><span class="sxs-lookup"><span data-stu-id="6d14f-116">Full (\[**ptr**\])</span></span>      | <span data-ttu-id="6d14f-117">如果是參數，用戶端應用程式必須配置;如果是內嵌的，可以是 null。</span><span class="sxs-lookup"><span data-stu-id="6d14f-117">If a parameter, the client application must allocate; if embedded, can be null.</span></span> <span data-ttu-id="6d14f-118">從 null 變更為非 null 會導致用戶端存根配置;從非 null 變更為 null 可能會導致損壞。</span><span class="sxs-lookup"><span data-stu-id="6d14f-118">Changing from null to non-null causes the client stub to allocate; changing from non-null to null can cause orphaning.</span></span><br/> |                                                                     |



 

<span data-ttu-id="6d14f-119">**\[ Ref \]** 屬性工作表示指標指向有效的記憶體。</span><span class="sxs-lookup"><span data-stu-id="6d14f-119">The **\[ref\]** attribute indicates that the pointer points to valid memory.</span></span> <span data-ttu-id="6d14f-120">根據定義，用戶端應用程式必須配置參考指標所需的所有記憶體。</span><span class="sxs-lookup"><span data-stu-id="6d14f-120">By definition, the client application must allocate all the memory that the reference pointers require.</span></span>

<span data-ttu-id="6d14f-121">唯一指標可從 null 變更為非 null。</span><span class="sxs-lookup"><span data-stu-id="6d14f-121">The unique pointer can change from null to non-null.</span></span> <span data-ttu-id="6d14f-122">如果唯一指標從 null 變更為非 null，則會在用戶端上配置新的記憶體。</span><span class="sxs-lookup"><span data-stu-id="6d14f-122">If the unique pointer changes from null to non-null, new memory is allocated on the client.</span></span> <span data-ttu-id="6d14f-123">如果唯一指標從非 null 變更為 null，則會產生損壞。</span><span class="sxs-lookup"><span data-stu-id="6d14f-123">If the unique pointer changes from non-null to null, orphaning can result.</span></span> <span data-ttu-id="6d14f-124">如需詳細資訊，請參閱 [記憶體損壞](memory-orphaning.md)。</span><span class="sxs-lookup"><span data-stu-id="6d14f-124">For more information, see [Memory Orphaning](memory-orphaning.md).</span></span>

 

