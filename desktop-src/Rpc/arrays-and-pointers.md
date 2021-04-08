---
title: 陣列和指標
description: 遠端程序呼叫 (RPC) 是設計來對開發人員而言是透明的。
ms.assetid: 5ad5a51d-a821-44a5-bbc3-14409cb42cb4
keywords:
- 遠端程序呼叫 RPC、描述、陣列和指標
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cb6bc3f4a2ec4af85156bf15160b0ce7d1efc33
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673756"
---
# <a name="arrays-and-pointers"></a><span data-ttu-id="4607c-104">陣列和指標</span><span class="sxs-lookup"><span data-stu-id="4607c-104">Arrays and Pointers</span></span>

<span data-ttu-id="4607c-105">遠端程序呼叫 (RPC) 是設計來對開發人員而言是透明的。</span><span class="sxs-lookup"><span data-stu-id="4607c-105">Remote Procedure Call (RPC) is designed to be mostly transparent to developers.</span></span> <span data-ttu-id="4607c-106">為了達成這個透明度，用戶端存根會將指標和指向的資料物件傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="4607c-106">To achieve this transparency, the client stub transmits to the server both the pointer and the data object to which it points.</span></span> <span data-ttu-id="4607c-107">如果遠端程式變更資料，伺服器必須將新的資料傳送回用戶端，讓用戶端可以透過原始資料複製新的資料。</span><span class="sxs-lookup"><span data-stu-id="4607c-107">If the remote procedure changes the data, the server must transmit the new data back to the client so that the client can copy the new data over the original data.</span></span>

<span data-ttu-id="4607c-108">一般情況下，遠端程序呼叫的行為就像是本機程序呼叫一樣。</span><span class="sxs-lookup"><span data-stu-id="4607c-108">In general, a remote procedure call behaves just like a local procedure call.</span></span> <span data-ttu-id="4607c-109">也就是說，當指標是參數時，遠端程式可以存取指標所參考的資料物件，就像本機程式一樣。</span><span class="sxs-lookup"><span data-stu-id="4607c-109">That is, when a pointer is a parameter, the remote procedure can access the data object the pointer refers to in the same way that a local procedure can.</span></span>

<span data-ttu-id="4607c-110">由於用戶端和伺服器程式是在不同的位址空間中執行，因此開發人員必須使用 Microsoft 介面定義語言 (MIDL) 屬性來描述在用戶端與伺服器之間傳輸陣列和指標資料的方式。</span><span class="sxs-lookup"><span data-stu-id="4607c-110">Since client and server programs run in different address spaces, developers must use Microsoft Interface Definition Language (MIDL) attributes to describe how array and pointer data is transmitted between the client and the server.</span></span> <span data-ttu-id="4607c-111">本節將概述如何在分散式應用程式中使用陣列和指標，請參考下列主題：</span><span class="sxs-lookup"><span data-stu-id="4607c-111">This section presents an overview of how to use arrays and pointers in distributed applications, in the following topics:</span></span>

-   [<span data-ttu-id="4607c-112">陣列和 RPC</span><span class="sxs-lookup"><span data-stu-id="4607c-112">Arrays and RPC</span></span>](arrays-and-rpc.md)
-   [<span data-ttu-id="4607c-113">指標和 RPC</span><span class="sxs-lookup"><span data-stu-id="4607c-113">Pointers and RPC</span></span>](pointers-and-rpc.md)
-   [<span data-ttu-id="4607c-114">使用陣列、字串和指標</span><span class="sxs-lookup"><span data-stu-id="4607c-114">Using Arrays, Strings, and Pointers</span></span>](using-arrays-strings-and-pointers.md)

 

 




