---
title: 記憶體損壞
description: 如果您的分散式應用程式使用 \ in、out、unique \ 或 in、out、ptr \ 指標參數，則應用程式的伺服器端可以將指標參數的值變更為 null。
ms.assetid: 65588b4d-6bf4-44f7-994c-29a5b185c6b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32042911695f377e0a628168e91387bfa25f0d79
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106965036"
---
# <a name="memory-orphaning"></a><span data-ttu-id="90038-103">記憶體損壞</span><span class="sxs-lookup"><span data-stu-id="90038-103">Memory Orphaning</span></span>

<span data-ttu-id="90038-104">如果您的分散式應用程式使用 \[ [in](/windows/desktop/Midl/in)、 [out](/windows/desktop/Midl/out-idl)、 [unique](/windows/desktop/Midl/unique) \] 或 \[ **in**、 **out**、 [ptr](/windows/desktop/Midl/ptr) \] 指標參數，則應用程式的伺服器端可以將指標參數的值變更為 null。</span><span class="sxs-lookup"><span data-stu-id="90038-104">If your distributed application uses an \[ [in](/windows/desktop/Midl/in), [out](/windows/desktop/Midl/out-idl), [unique](/windows/desktop/Midl/unique)\] or \[**in**, **out**, [ptr](/windows/desktop/Midl/ptr)\] pointer parameter, the server side of the application can change the value of the pointer parameter to null.</span></span> <span data-ttu-id="90038-105">當伺服器接著將 null 值傳回給用戶端時，在遠端程序呼叫之前，指標所參考的記憶體仍會存在於用戶端，但無法再從該指標存取 (但別名完整指標) 的情況除外。</span><span class="sxs-lookup"><span data-stu-id="90038-105">When the server subsequently returns the null value to the client, memory referenced by the pointer before the remote procedure call is still present on the client side, but is no longer accessible from that pointer (except in the case of an aliased full pointer).</span></span> <span data-ttu-id="90038-106">此記憶體稱為「 *孤立*」。</span><span class="sxs-lookup"><span data-stu-id="90038-106">This memory is said to be *orphaned*.</span></span> <span data-ttu-id="90038-107">這也稱為「 *記憶體* 流失」。</span><span class="sxs-lookup"><span data-stu-id="90038-107">This is also termed a *memory leak*.</span></span> <span data-ttu-id="90038-108">用戶端上的記憶體重複損壞會導致用戶端用盡可用的記憶體資源。</span><span class="sxs-lookup"><span data-stu-id="90038-108">Repeated orphaning of memory on the client causes the client to run out of available memory resources.</span></span>

<span data-ttu-id="90038-109">只要伺服器將內嵌指標變更為 null 值，記憶體也可以是孤立的。</span><span class="sxs-lookup"><span data-stu-id="90038-109">Memory can also be orphaned whenever the server changes an embedded pointer to a null value.</span></span> <span data-ttu-id="90038-110">例如，如果參數指向複雜的資料結構，例如樹狀結構，應用程式的伺服器端就可以刪除樹狀結構的節點，並將樹狀結構中的指標設定為 null。</span><span class="sxs-lookup"><span data-stu-id="90038-110">For example, if the parameter points to a complex data structure such as a tree, the server side of the application can delete nodes of the tree and set pointers inside the tree to null.</span></span>

<span data-ttu-id="90038-111">可能導致記憶體流失的另一種情況，則牽涉到一致、變化和開放的陣列，其中包含指標。</span><span class="sxs-lookup"><span data-stu-id="90038-111">Another situation that can lead to a memory leak involves conformant, varying, and open arrays containing pointers.</span></span> <span data-ttu-id="90038-112">當伺服器應用程式修改指定陣列大小或傳輸範圍的參數，使其代表較小的值時，存根會使用較小的值 (s) 來釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="90038-112">When the server application modifies the parameter that specifies the array size or transmitted range so that it represents a smaller value, the stubs use the smaller value(s) to free memory.</span></span> <span data-ttu-id="90038-113">索引大於 size 參數的陣列元素是孤立的。</span><span class="sxs-lookup"><span data-stu-id="90038-113">The array elements with indices larger than the size parameter are orphaned.</span></span> <span data-ttu-id="90038-114">您的應用程式必須在傳輸的範圍之外釋放元素。</span><span class="sxs-lookup"><span data-stu-id="90038-114">Your application must free elements outside the transmitted range.</span></span>

 

 