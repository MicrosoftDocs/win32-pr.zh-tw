---
title: RPC 元件
description: 遠端程序呼叫 (RPC) 元件。
ms.assetid: 7caaf01a-7f20-470f-afcf-478146cae5eb
keywords:
- 遠端程序呼叫 RPC、描述的元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11c715a4f454ef28db20ee527e5e8f33f66200b2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932268"
---
# <a name="rpc-components"></a><span data-ttu-id="623aa-104">RPC 元件</span><span class="sxs-lookup"><span data-stu-id="623aa-104">RPC Components</span></span>

<span data-ttu-id="623aa-105">RPC 包含下列主要元件：</span><span class="sxs-lookup"><span data-stu-id="623aa-105">RPC includes the following major components:</span></span>

-   <span data-ttu-id="623aa-106">MIDL 編譯器</span><span class="sxs-lookup"><span data-stu-id="623aa-106">MIDL compiler</span></span>
-   <span data-ttu-id="623aa-107">執行時間程式庫和標頭檔</span><span class="sxs-lookup"><span data-stu-id="623aa-107">Run-time libraries and header files</span></span>
-   <span data-ttu-id="623aa-108">名稱服務提供者 (有時稱為定位器) </span><span class="sxs-lookup"><span data-stu-id="623aa-108">Name service provider (sometimes referred to as the Locator)</span></span>
-   <span data-ttu-id="623aa-109">端點對應程式 (有時稱為埠對應程式) </span><span class="sxs-lookup"><span data-stu-id="623aa-109">Endpoint mapper (sometimes referred to as the port mapper)</span></span>

<span data-ttu-id="623aa-110">在 RPC 模型中，您可以使用針對此用途設計的語言，正式指定遠端程式的介面。</span><span class="sxs-lookup"><span data-stu-id="623aa-110">In the RPC model, you can formally specify an interface to the remote procedures using a language designed for this purpose.</span></span> <span data-ttu-id="623aa-111">這種語言稱為介面定義語言或 IDL。</span><span class="sxs-lookup"><span data-stu-id="623aa-111">This language is called the Interface Definition Language, or IDL.</span></span> <span data-ttu-id="623aa-112">這種語言的 Microsoft 執行稱為「Microsoft 介面定義語言」或「MIDL」。</span><span class="sxs-lookup"><span data-stu-id="623aa-112">The Microsoft implementation of this language is called the Microsoft Interface Definition Language, or MIDL.</span></span>

<span data-ttu-id="623aa-113">建立介面之後，您必須透過 MIDL 編譯器來傳遞它。</span><span class="sxs-lookup"><span data-stu-id="623aa-113">After you create an interface, you must pass it through the MIDL compiler.</span></span> <span data-ttu-id="623aa-114">此編譯器會產生可將本機程序呼叫轉譯為遠端程序呼叫的存根。</span><span class="sxs-lookup"><span data-stu-id="623aa-114">This compiler generates the stubs that translate local procedure calls into remote procedure calls.</span></span> <span data-ttu-id="623aa-115">存根是可對執行時間程式庫函式進行呼叫的預留位置函式，該函式會管理遠端程序呼叫。</span><span class="sxs-lookup"><span data-stu-id="623aa-115">Stubs are placeholder functions that make the calls to the run-time library functions, which manage the remote procedure call.</span></span> <span data-ttu-id="623aa-116">這種方法的優點是，網路對您的分散式應用程式幾乎是完全透明的。</span><span class="sxs-lookup"><span data-stu-id="623aa-116">The advantage of this approach is that the network becomes almost completely transparent to your distributed application.</span></span> <span data-ttu-id="623aa-117">您的用戶端程式會呼叫看似本機程式的內容;將其轉換為遠端呼叫的工作會自動完成。</span><span class="sxs-lookup"><span data-stu-id="623aa-117">Your client program calls what appear to be local procedures; the work of turning them into remote calls is done for you automatically.</span></span> <span data-ttu-id="623aa-118">所有轉譯資料、存取網路和取得結果的程式碼，會由 MIDL 編譯器為您產生，而您的應用程式不會看到這些結果。</span><span class="sxs-lookup"><span data-stu-id="623aa-118">All the code that translates data, accesses the network, and retrieves results is generated for you by the MIDL compiler and is invisible to your application.</span></span>

 

 




