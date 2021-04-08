---
title: 函式屬性
description: '\ 回呼 \ 和 \ 本機 \ 屬性可以套用為函式屬性。'
ms.assetid: 05e19164-072c-4a5a-878d-845273975854
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75ef199b937d5a3e9a8444be9ed65749da007ced
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682943"
---
# <a name="function-attributes"></a><span data-ttu-id="54375-103">函式屬性</span><span class="sxs-lookup"><span data-stu-id="54375-103">Function Attributes</span></span>

<span data-ttu-id="54375-104">**\[**[**回呼**](/windows/desktop/Midl/callback) **\]** 和 **\[** [**本機**](/windows/desktop/Midl/local) **\]** 屬性可以套用為函式屬性。</span><span class="sxs-lookup"><span data-stu-id="54375-104">The **\[**[**callback**](/windows/desktop/Midl/callback)**\]** and **\[**[**local**](/windows/desktop/Midl/local)**\]** attributes can be applied as function attributes.</span></span>

<span data-ttu-id="54375-105">回呼是從伺服器到用戶端的遠端呼叫，此用戶端會在概念單一執行執行緒中執行。</span><span class="sxs-lookup"><span data-stu-id="54375-105">A callback is a remote call from server to client that executes as part of a conceptual single-execution thread.</span></span> <span data-ttu-id="54375-106">回呼一律會在遠端呼叫的內容中發出 (或回呼) ，而且是由發出原始遠端呼叫的執行緒 (或回呼) 所執行。</span><span class="sxs-lookup"><span data-stu-id="54375-106">A callback is always issued in the context of a remote call (or callback) and is executed by the thread that issued the original remote call (or callback).</span></span>

<span data-ttu-id="54375-107">通常最好將本機程式宣告放在 IDL 檔案中，因為這是描述封裝介面的邏輯位置。</span><span class="sxs-lookup"><span data-stu-id="54375-107">It is often desirable to place a local procedure declaration in the IDL file, since this is the logical place to describe interfaces to a package.</span></span> <span data-ttu-id="54375-108">**\[** [**Local**](/windows/desktop/Midl/local) **\]** 屬性指出程式聲明實際上不是遠端函式，而是本機程式。</span><span class="sxs-lookup"><span data-stu-id="54375-108">The **\[**[**local**](/windows/desktop/Midl/local)**\]** attribute indicates that a procedure declaration is not actually a remote function, but a local procedure.</span></span> <span data-ttu-id="54375-109">MIDL 編譯器不會為具有 **\[ 區域 \]** 屬性的函式產生任何 stub。</span><span class="sxs-lookup"><span data-stu-id="54375-109">The MIDL compiler does not generate any stubs for functions with the **\[local\]** attribute.</span></span>

<span data-ttu-id="54375-110">請務必注意， **\[** [](/windows/desktop/Midl/callback) **\]** 不建議在多執行緒程式設計中使用回呼。</span><span class="sxs-lookup"><span data-stu-id="54375-110">It is important to note that the use of **\[**[**callback**](/windows/desktop/Midl/callback)**\]** is not recommended in multi-thread programming.</span></span> <span data-ttu-id="54375-111">作為單一執行緒程式設計功能，它並不支援多執行緒環境所提供的安全性需求。</span><span class="sxs-lookup"><span data-stu-id="54375-111">As a single-thread programming function, it is not equipped to support the security demands a multi-thread environment provides.</span></span>

 

 