---
title: " (RPC) 的字串屬性"
description: '\ 字串 \ 屬性和遠端程序呼叫 (RPC) 。'
ms.assetid: 794e03f2-b1e9-42dc-8536-9ced5c0e3dad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e413c0b3b8f5a379dc3448f07aed4a5a7a6aba07
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933515"
---
# <a name="string-attribute-rpc"></a><span data-ttu-id="62e92-103"> (RPC) 的字串屬性</span><span class="sxs-lookup"><span data-stu-id="62e92-103">string attribute (RPC)</span></span>

<span data-ttu-id="62e92-104">\[[字串](/windows/desktop/Midl/string) \] 屬性指出參數是 [char](/windows/desktop/Midl/char-idl)、 [byte](/windows/desktop/Midl/byte)或 **w \_ 字元** 類型陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="62e92-104">The \[ [string](/windows/desktop/Midl/string)\] attribute indicates that the parameter is a pointer to an array of type [char](/windows/desktop/Midl/char-idl), [byte](/windows/desktop/Midl/byte), or **w\_char**.</span></span> <span data-ttu-id="62e92-105">如同符合標準的陣列，會在執行時間決定 **\[ 字串 \]** 參數的大小。</span><span class="sxs-lookup"><span data-stu-id="62e92-105">As with a conformant array, the size of a **\[string\]** parameter is determined at run time.</span></span> <span data-ttu-id="62e92-106">與符合標準的陣列不同的是，開發人員不需要提供與陣列相關聯的長度，而 **\[ \] 字串** 屬性會藉由呼叫 **strlen**，告訴存根判斷陣列的大小。</span><span class="sxs-lookup"><span data-stu-id="62e92-106">Unlike a conformant array, the developer does not have to provide the length associated with the array—the **\[string\]** attribute tells the stub to determine the array size by calling **strlen**.</span></span> <span data-ttu-id="62e92-107">當 **\[ \]** \[ [長度 \_ 為](/windows/desktop/Midl/length-is) \] 或 \[ [最後一個 \_ 是](/windows/desktop/Midl/last-is)屬性時，不能同時使用字串屬性 \] 。</span><span class="sxs-lookup"><span data-stu-id="62e92-107">A **\[string\]** attribute cannot be used at the same time as the \[ [length\_is](/windows/desktop/Midl/length-is)\] or \[ [last\_is](/windows/desktop/Midl/last-is)\] attributes.</span></span>

<span data-ttu-id="62e92-108">**\[ 在中，字串 \]** 屬性組合會指示存根只將字串從用戶端傳遞至伺服器。</span><span class="sxs-lookup"><span data-stu-id="62e92-108">The **\[in, string\]** attribute combination directs the stub to pass the string from client to server only.</span></span> <span data-ttu-id="62e92-109">伺服器上配置的記憶體數量與傳送的字串大小加1。</span><span class="sxs-lookup"><span data-stu-id="62e92-109">The amount of memory allocated on the server is the same as the transmitted string size plus one.</span></span>

<span data-ttu-id="62e92-110">\[ [Out](/windows/desktop/Midl/out-idl)、 **string** \] 屬性會導向存根，只將字串從伺服器傳遞至用戶端。</span><span class="sxs-lookup"><span data-stu-id="62e92-110">The \[ [out](/windows/desktop/Midl/out-idl), **string**\] attributes direct the stub to pass the string from server to client only.</span></span> <span data-ttu-id="62e92-111">C 語言堅持的呼叫方式設計，所有 **\[ out \]** 參數都必須是指標。</span><span class="sxs-lookup"><span data-stu-id="62e92-111">The call-by-value design of the C language insists that all **\[out\]** parameters must be pointers.</span></span>

<span data-ttu-id="62e92-112">**\[ Out \]** 參數必須是指標，且根據預設，所有指標參數都是參考指標。</span><span class="sxs-lookup"><span data-stu-id="62e92-112">The **\[out\]** parameter must be a pointer and, by default, all pointer parameters are reference pointers.</span></span> <span data-ttu-id="62e92-113">參考指標在呼叫期間不會變更，它會指向與呼叫之前相同的記憶體。</span><span class="sxs-lookup"><span data-stu-id="62e92-113">The reference pointer does not change during the call—it points to the same memory as before the call.</span></span> <span data-ttu-id="62e92-114">針對字串指標，參考指標的其他條件約束表示用戶端必須在進行遠端程序呼叫之前配置足夠的有效記憶體。</span><span class="sxs-lookup"><span data-stu-id="62e92-114">For string pointers, the additional constraint of the reference pointer means the client must allocate sufficient valid memory before making the remote procedure call.</span></span> <span data-ttu-id="62e92-115">存根會將 **\[ out、string \]** 屬性指出的字串傳送至已在用戶端上配置的記憶體中。</span><span class="sxs-lookup"><span data-stu-id="62e92-115">The stubs transmit the string that the **\[out, string\]** attributes indicate into the memory already allocated on the client side.</span></span>

<span data-ttu-id="62e92-116">下列主題描述字串的遠端過程參數原型：</span><span class="sxs-lookup"><span data-stu-id="62e92-116">The following topics describe the remote procedure parameter prototypes for strings:</span></span>

-   <span data-ttu-id="62e92-117">[\[in、out、string \] 原型](-in-out-string-prototype.md)</span><span class="sxs-lookup"><span data-stu-id="62e92-117">[\[in, out, string\] Prototype](-in-out-string-prototype.md)</span></span>
-   <span data-ttu-id="62e92-118">[\[在、字串 \] 和 \[ 輸出中，字串 \] 原型](-in-string-and-out-string-prototype.md)</span><span class="sxs-lookup"><span data-stu-id="62e92-118">[\[in, string\] and \[out, string\] Prototype](-in-string-and-out-string-prototype.md)</span></span>

 

 