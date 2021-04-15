---
title: Strict 和 Type Strict 內容控制碼
description: 使用 \_ \_ 所有內容控制碼的 strict 內容控制碼屬性。
ms.assetid: 2483aa76-0814-4f63-9c38-0aa050d73772
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a45b4e7914034e315f2275e1d928293332012fc4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463433"
---
# <a name="strict-and-type-strict-context-handles"></a><span data-ttu-id="76bef-103">Strict 和 Type Strict 內容控制碼</span><span class="sxs-lookup"><span data-stu-id="76bef-103">Strict and Type Strict Context Handles</span></span>

<span data-ttu-id="76bef-104">使用所有內容控制碼的 [**strict \_ 內容 \_ 控制碼**](/windows/desktop/Midl/strict-context-handle) 屬性。</span><span class="sxs-lookup"><span data-stu-id="76bef-104">Use the [**strict\_context\_handle**](/windows/desktop/Midl/strict-context-handle) attribute for all context handles.</span></span> <span data-ttu-id="76bef-105">根據預設，內容控制碼不會與介面相關聯，這表示可以在某個介面上建立內容控制碼，然後傳遞至另一個介面。</span><span class="sxs-lookup"><span data-stu-id="76bef-105">By default, a context handle is not associated with an interface, which means a context handle can be created on one interface, then passed to another.</span></span> <span data-ttu-id="76bef-106">這是一項簡單的攻擊，而許多 RPC 伺服器無法避免。</span><span class="sxs-lookup"><span data-stu-id="76bef-106">This is an easy attack, and many RPC servers fail to prevent it.</span></span>

<span data-ttu-id="76bef-107">如果兩個介面並存于同一個進程中，攻擊者可以開啟某個介面上的內容控制碼，並將其傳遞給另一個介面，而這可能會導致無法預期的資料。</span><span class="sxs-lookup"><span data-stu-id="76bef-107">If two interfaces coexist in the same process, an attacker can open a context handle on one interface, and pass it to another, which may trip over the unexpected data.</span></span> <span data-ttu-id="76bef-108">許多開發人員認為其軟體是程式中唯一的介面，但通常不是這種情況，因為系統和許多協力廠商元件會在內部使用 RPC，而這些介面可以建立內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="76bef-108">Many developers believe their software is the only interface in a process, but very often that is not the case, because both the system and many third-party components use RPC internally, and those interfaces can create context handles.</span></span> <span data-ttu-id="76bef-109">使用 [**strict \_ 內容 \_ 控制碼**](/windows/desktop/Midl/strict-context-handle) 屬性時，RPC 執行時間可確保在某個介面上建立的內容只能做為引數傳遞給該介面的方法。</span><span class="sxs-lookup"><span data-stu-id="76bef-109">When the [**strict\_context\_handle**](/windows/desktop/Midl/strict-context-handle) attribute is used, the RPC run time ensures that a context created on one interface can be passed as an argument only to methods of that interface.</span></span>

<span data-ttu-id="76bef-110">在針對 Windows Vista 開發應用程式的情況下，可以使用 [**類型 \_ strict \_ 內容 \_ 控制碼**](/windows/desktop/Midl/type-strict-context-handle) ，並建議使用。</span><span class="sxs-lookup"><span data-stu-id="76bef-110">In situations where an application is developed for Windows Vista, the use of [**type\_strict\_context\_handle**](/windows/desktop/Midl/type-strict-context-handle) is available and recommended.</span></span> <span data-ttu-id="76bef-111">內容控制碼預設不會與特定類型相關聯。</span><span class="sxs-lookup"><span data-stu-id="76bef-111">Context handles are not associated with a specific type by default.</span></span> <span data-ttu-id="76bef-112">在相同的進程中使用多種類型的內容控制碼時，惡意用戶端可能會傳遞內容控制碼來取代另一個，以產生不想要的結果。</span><span class="sxs-lookup"><span data-stu-id="76bef-112">When multiple types of context handles are used in the same process, it is possible for a malicious client to pass a context handle in place of another to produce undesirable results.</span></span> <span data-ttu-id="76bef-113">使用 **類型 \_ strict \_ 內容 \_ 控制碼** 可讓應用程式強制執行內容控制碼類型一致性，並防止任何不相符的內容控制碼類型使用方式。</span><span class="sxs-lookup"><span data-stu-id="76bef-113">The use of **type\_strict\_context\_handle** allows applications to enforce context handle type consistency and prevent any mismatched context handle type usage.</span></span>

 

 