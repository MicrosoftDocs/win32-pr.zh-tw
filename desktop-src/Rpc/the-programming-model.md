---
title: 程式設計模型
description: 在早期的電腦程式設計中，每個程式都是以大型的整合式區塊來撰寫，並以 goto 語句填滿。
ms.assetid: b64d5338-a06a-4a27-bedb-c9011fa5a5a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bcc0fd51404290b3d673982001cb3ee91bf1747
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673463"
---
# <a name="the-programming-model"></a><span data-ttu-id="c9548-103">程式設計模型</span><span class="sxs-lookup"><span data-stu-id="c9548-103">The Programming Model</span></span>

<span data-ttu-id="c9548-104">在早期的電腦程式設計中，每個程式都是以大型的整合式區塊來撰寫，並以 **goto** 語句填滿。</span><span class="sxs-lookup"><span data-stu-id="c9548-104">In the early days of computer programming, each program was written as a large monolithic chunk, filled with **goto** statements.</span></span> <span data-ttu-id="c9548-105">每個程式都必須將自己的輸入和輸出管理到不同的硬體裝置。</span><span class="sxs-lookup"><span data-stu-id="c9548-105">Each program had to manage its own input and output to different hardware devices.</span></span> <span data-ttu-id="c9548-106">隨著程式設計專業領域的發展，此整合型程式碼已組織成程式，其中最常使用的程式會封裝在程式庫中，以供共用和重複使用。</span><span class="sxs-lookup"><span data-stu-id="c9548-106">As the programming discipline matured, this monolithic code was organized into procedures, with the most commonly used procedures packed in libraries for sharing and reuse.</span></span>

![整合到共用程式庫的整合式 goto 語句與程式](images/prog-a06.png)

<span data-ttu-id="c9548-108">C 程式設計語言支援程式導向程式設計。</span><span class="sxs-lookup"><span data-stu-id="c9548-108">The C programming language supports procedure-oriented programming.</span></span> <span data-ttu-id="c9548-109">在 C 中，主要程式與所有其他程式都有黑色方塊。</span><span class="sxs-lookup"><span data-stu-id="c9548-109">In C, the main procedure relates to all other procedures as black boxes.</span></span> <span data-ttu-id="c9548-110">例如，主要程式找不到程式 A、B 和 X 如何執行其工作。</span><span class="sxs-lookup"><span data-stu-id="c9548-110">For example, the main procedure cannot find out how procedures A, B, and X do their work.</span></span> <span data-ttu-id="c9548-111">Main 程式只會呼叫另一個程式;它沒有如何執行該程式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c9548-111">The main procedure only calls another procedure; it has no information about how that procedure is implemented.</span></span>

![隔離在外部程式中執行的活動](images/prog-a08.png)

<span data-ttu-id="c9548-113">程式導向程式設計語言提供簡單的機制來指定和撰寫程式。</span><span class="sxs-lookup"><span data-stu-id="c9548-113">Procedure-oriented programming languages provide simple mechanisms for specifying and writing procedures.</span></span> <span data-ttu-id="c9548-114">例如，ANSI 標準的 C 函式原型是用來指定程式名稱的結構、它傳回的結果類型 (如果有任何) 和其參數的數目、順序和類型。</span><span class="sxs-lookup"><span data-stu-id="c9548-114">For example, the ANSI-standard C-function prototype is a construct used to specify the name of a procedure, the type of the result it returns (if any) and the number, sequence, and type of its parameters.</span></span> <span data-ttu-id="c9548-115">使用函數原型是在程式之間指定介面的正式方式。</span><span class="sxs-lookup"><span data-stu-id="c9548-115">Using the function prototype is a formal way to specify an interface between procedures.</span></span>

<span data-ttu-id="c9548-116">Microsoft RPC 以該程式設計模型為基礎，其允許在介面中群組在一起的程式，與呼叫者位於不同的進程中。</span><span class="sxs-lookup"><span data-stu-id="c9548-116">Microsoft RPC builds on that programming model by allowing procedures, grouped together in interfaces, to reside in different processes than the caller.</span></span> <span data-ttu-id="c9548-117">Microsoft RPC 也會新增更正式的程式定義方法，讓呼叫端和被呼叫的常式採用合約來遠端交換資料及叫用功能。</span><span class="sxs-lookup"><span data-stu-id="c9548-117">Microsoft RPC also adds a more formal approach to procedure definition that allows the caller and the called routine to adopt a contract for remotely exchanging data and invoking functionality.</span></span> <span data-ttu-id="c9548-118">在 Microsoft RPC 程式設計模型中，傳統的函式呼叫會以兩個額外的元素補充。</span><span class="sxs-lookup"><span data-stu-id="c9548-118">In the Microsoft RPC programming model, traditional function calls are supplemented with two additional elements.</span></span>

-   <span data-ttu-id="c9548-119">第一個元素是 .idl/acf 檔案，可精確描述呼叫端和呼叫程式之間的資料交換和參數傳遞機制。</span><span class="sxs-lookup"><span data-stu-id="c9548-119">The first element is an .idl/.acf file that precisely describes the data exchange and parameter-passing mechanism between the caller and called procedure.</span></span>
-   <span data-ttu-id="c9548-120">第二個元素是一組執行時間 Api，可讓開發人員更精確地控制遠端程序呼叫，包括安全性層面、管理伺服器上的狀態、指定可與伺服器通訊的用戶端等等。</span><span class="sxs-lookup"><span data-stu-id="c9548-120">The second element is a set of run-time APIs that provide developers with granular control of the remote procedure call, including security aspects, managing state on the server, specifying which clients can talk to the server, and so on.</span></span>

 

 




