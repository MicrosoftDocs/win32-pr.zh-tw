---
title: 多執行緒用戶端和內容控制碼
description: 當您的多執行緒用戶端有多個執行緒使用相同的內容控制碼實例時，預設會在伺服器上序列化內容控制碼實例的存取。
ms.assetid: 192be467-b1e0-422b-878a-738cb7d72b5b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67c621d75d8cc48ca1f71719066f455e0efce39f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023789"
---
# <a name="multithreaded-clients-and-context-handles"></a><span data-ttu-id="ef901-103">多執行緒用戶端和內容控制碼</span><span class="sxs-lookup"><span data-stu-id="ef901-103">Multithreaded Clients and Context Handles</span></span>

<span data-ttu-id="ef901-104">當您的多執行緒用戶端有多個執行緒使用相同的內容控制碼實例時，預設會在伺服器上序列化內容控制碼實例的存取。</span><span class="sxs-lookup"><span data-stu-id="ef901-104">When you have a multithreaded client where multiple threads are using the same context handle instance, access to the context handle instance is serialized at the server by default.</span></span> <span data-ttu-id="ef901-105">如此一來，伺服器管理員就不需要針對來自相同用戶端的另一個執行緒進行防護，也就是在分派呼叫時，變更內容或正在執行的內容。</span><span class="sxs-lookup"><span data-stu-id="ef901-105">This saves the server manager from having to guard against another thread from the same client changing the context or the context running down while a call is dispatched.</span></span> <span data-ttu-id="ef901-106">不過，在某些情況下，序列化可能會影響效能。</span><span class="sxs-lookup"><span data-stu-id="ef901-106">However, in certain cases serialization may impact performance.</span></span>

<span data-ttu-id="ef901-107">請考慮下列各項：兩個用戶端執行緒叫用不會變更內容狀態的遠端程序呼叫 (例如，呼叫只會從它) 取得一些值。</span><span class="sxs-lookup"><span data-stu-id="ef901-107">Consider the following: two client threads invoke a remote procedure call that does not change the state of the context (for example, the call simply obtains some values from it).</span></span> <span data-ttu-id="ef901-108">這類呼叫不需要序列化。</span><span class="sxs-lookup"><span data-stu-id="ef901-108">Such calls do not need to be serialized.</span></span>

<span data-ttu-id="ef901-109">在這種情況下，Windows XP 會提供混合模式的序列化模型，其中每個方法都可以宣告為具有內容控制碼的獨佔或共用存取。</span><span class="sxs-lookup"><span data-stu-id="ef901-109">For such situations, Windows XP offers a mixed mode serialization model, where each method may be declared to have exclusive or shared access to a context handle.</span></span> <span data-ttu-id="ef901-110">如需詳細資料，請參閱 [內容 \_ 控制碼 \_ 序列化](/windows/desktop/Midl/context-handle-serialize) 和 [內容 \_ 控制碼 \_ noserialize](/windows/desktop/Midl/context-handle-noserialize) 。</span><span class="sxs-lookup"><span data-stu-id="ef901-110">See [context\_handle\_serialize](/windows/desktop/Midl/context-handle-serialize) and [context\_handle\_noserialize](/windows/desktop/Midl/context-handle-noserialize) for details.</span></span>

<span data-ttu-id="ef901-111">在 Windows XP 之前的 Windows 版本中，允許平行存取內容控制碼的唯一方法，就是呼叫 [**RpcSsDontSerializeCoNtext**](/previous-versions/aa378473(v=vs.80)) 函式，以允許在單一內容控制碼上分派多個呼叫。</span><span class="sxs-lookup"><span data-stu-id="ef901-111">In versions of Windows prior to Windows XP, the only means of allowing concurrent access to a context handle is to call the [**RpcSsDontSerializeContext**](/previous-versions/aa378473(v=vs.80)) function to allow multiple calls to be dispatched on a single context handle.</span></span> <span data-ttu-id="ef901-112">呼叫 **RpcSsDontSerializeCoNtext** 函數並不會完全停用序列化;當發生內容執行時，只有在所有未完成的用戶端要求都已完成時，才會執行內容執行常式。</span><span class="sxs-lookup"><span data-stu-id="ef901-112">Calling the **RpcSsDontSerializeContext** function does not disable serialization entirely; when a context run-down occurs, the context run-down routine runs only when all outstanding client requests have completed.</span></span> <span data-ttu-id="ef901-113">對 **RpcScDontSerializeCoNtext** 的呼叫會影響整個進程，且不會還原。</span><span class="sxs-lookup"><span data-stu-id="ef901-113">A call to **RpcScDontSerializeContext** affects the entire process, and is not revertible.</span></span> <span data-ttu-id="ef901-114">不建議在 Windows XP 和更新版本中使用 **RpcScDontSerializeCoNtext** ;它會讓伺服器程式碼在處理完全非序列化環境固有的競爭條件時變得非常複雜。</span><span class="sxs-lookup"><span data-stu-id="ef901-114">Using **RpcScDontSerializeContext** in Windows XP and later versions is not recommended; it makes server code very complicated when dealing reliably with race conditions inherent in completely non-serialized environments.</span></span>

 

 