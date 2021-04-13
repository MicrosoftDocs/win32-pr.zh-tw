---
title: 程式序列化
description: 當您使用程式序列化時，會使用 \ 編碼 \ 或 \ 解碼 \ 屬性來標記程式。 編譯器不會產生一般的遠端存根，而是會產生常式的序列化存根。
ms.assetid: 98367b00-696b-44c4-a747-92ecac34ba1e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77696761a9aa5fe1471e9ebf24a57303b15d0ff3
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "104386333"
---
# <a name="procedure-serialization"></a><span data-ttu-id="09c55-104">程式序列化</span><span class="sxs-lookup"><span data-stu-id="09c55-104">Procedure Serialization</span></span>

<span data-ttu-id="09c55-105">當您使用程式序列化時，會使用 \[ [**編碼**](/windows/desktop/Midl/encode) \] 或解碼 \[ [](/windows/desktop/Midl/decode) \] 屬性來標記程式。</span><span class="sxs-lookup"><span data-stu-id="09c55-105">When you use procedure serialization, a procedure is labeled with the \[[**encode**](/windows/desktop/Midl/encode)\] or \[[**decode**](/windows/desktop/Midl/decode)\] attribute.</span></span> <span data-ttu-id="09c55-106">編譯器不會產生一般的遠端存根，而是會產生常式的序列化存根。</span><span class="sxs-lookup"><span data-stu-id="09c55-106">Instead of generating the usual remote stub, the compiler generates a serialization stub for the routine.</span></span>

<span data-ttu-id="09c55-107">就像遠端程式必須使用系結控制碼進行遠端呼叫，序列化程式必須使用序列化控制碼來使用序列化服務。</span><span class="sxs-lookup"><span data-stu-id="09c55-107">Just as a remote procedure must use a binding handle to make a remote call, a serialization procedure must use a serialization handle to use serialization services.</span></span> <span data-ttu-id="09c55-108">如果未指定序列化控制碼，則會使用預設的隱含控制碼來指示呼叫。</span><span class="sxs-lookup"><span data-stu-id="09c55-108">If a serialization handle is not specified, a default implicit handle is used to direct the call.</span></span> <span data-ttu-id="09c55-109">另一方面，如果指定了序列化控制碼（以做為常式的明確 [**控制碼 \_ t**](/windows/desktop/Midl/handle-t)引數，或使用 \[ [**明確 \_ 控制碼**](/windows/desktop/Midl/explicit-handle) \] 屬性），則您必須傳遞有效的控制碼做為呼叫的引數。</span><span class="sxs-lookup"><span data-stu-id="09c55-109">On the other hand, if the serialization handle is specified, either as an explicit [**handle\_t**](/windows/desktop/Midl/handle-t) argument of the routine or by using the \[[**explicit\_handle**](/windows/desktop/Midl/explicit-handle)\] attribute, you must pass a valid handle as an argument of the call.</span></span> <span data-ttu-id="09c55-110">如需有關如何建立有效序列化控制碼的詳細資訊，請參閱 [序列化控制碼](serialization-handles.md)、 [固定緩衝區編碼範例](fixed-buffer-serialization.md)和累加 [式編碼範例](examples-of-incremental-encoding.md)。</span><span class="sxs-lookup"><span data-stu-id="09c55-110">For additional information on how to create a valid serialization handle, see [Serialization Handles](serialization-handles.md), [Examples of Fixed Buffer Encoding](fixed-buffer-serialization.md), and [Examples of Incremental Encoding](examples-of-incremental-encoding.md).</span></span>

> [!Note]
> <span data-ttu-id="09c55-111">Microsoft RPC 允許將遠端和序列化程式混合在一個介面中。</span><span class="sxs-lookup"><span data-stu-id="09c55-111">Microsoft RPC allows remote and serialization procedures to be mixed in one interface.</span></span> <span data-ttu-id="09c55-112">但是，當您這麼做時，請特別小心。</span><span class="sxs-lookup"><span data-stu-id="09c55-112">However, use caution when doing so.</span></span>
> 
> <span data-ttu-id="09c55-113">針對具有隱含系結控制碼的遠端程式，MIDL 編譯器會產生型 [**別控制碼 \_ t**](/windows/desktop/Midl/handle-t)的全域控制碼變數。</span><span class="sxs-lookup"><span data-stu-id="09c55-113">For remote procedures with implicit binding handles, the MIDL compiler generates a global handle variable of type [**handle\_t**](/windows/desktop/Midl/handle-t).</span></span> <span data-ttu-id="09c55-114">具有隱含序列化控制碼的程式和類型會使用這個相同的全域控制碼變數。</span><span class="sxs-lookup"><span data-stu-id="09c55-114">Procedures and types with implicit serialization handles use this same global handle variable.</span></span>
> 
> <span data-ttu-id="09c55-115">若為隱含控制碼，全域隱含控制碼必須設定為有效的系結控制碼，才能進行遠端呼叫。</span><span class="sxs-lookup"><span data-stu-id="09c55-115">For implicit handles, the global implicit handle must be set to a valid binding handle before a remote call.</span></span> <span data-ttu-id="09c55-116">在序列化呼叫之前，隱含控制碼必須設定為有效的序列化控制碼。</span><span class="sxs-lookup"><span data-stu-id="09c55-116">The implicit handle must be set to a valid serialization handle before a serialization call.</span></span> <span data-ttu-id="09c55-117">因此，程式不能同時為遠端和序列化。</span><span class="sxs-lookup"><span data-stu-id="09c55-117">Therefore, a procedure cannot be both remote and serialized.</span></span> <span data-ttu-id="09c55-118">它必須是一個或另一個。</span><span class="sxs-lookup"><span data-stu-id="09c55-118">It must be one or the other.</span></span>

 

 

 