---
title: 記憶體管理 ACF 屬性
description: 下表所列的屬性可讓您從用戶端執行記憶體管理。
ms.assetid: ca03c7fe-6649-431b-89dc-5d07a3c8d591
keywords:
- ACF MIDL、屬性、記憶體管理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d12a0ee6d11a2b10e1c0fad7cd1a42411670b508
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933184"
---
# <a name="memory-management-acf-attributes"></a><span data-ttu-id="74015-104">記憶體管理 ACF 屬性</span><span class="sxs-lookup"><span data-stu-id="74015-104">Memory Management ACF Attributes</span></span>

<span data-ttu-id="74015-105">下表所列的屬性可讓您從用戶端執行記憶體管理。</span><span class="sxs-lookup"><span data-stu-id="74015-105">The attributes listed in the following table enable you to perform memory management from the client side.</span></span>



| <span data-ttu-id="74015-106">屬性</span><span class="sxs-lookup"><span data-stu-id="74015-106">Attribute</span></span>                                   | <span data-ttu-id="74015-107">使用方式</span><span class="sxs-lookup"><span data-stu-id="74015-107">Usage</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="74015-108">**分配**</span><span class="sxs-lookup"><span data-stu-id="74015-108">**allocate**</span></span>](allocate.md)                | <span data-ttu-id="74015-109">針對指標指定用戶端應用程式和存根配置和釋放記憶體的方式。</span><span class="sxs-lookup"><span data-stu-id="74015-109">Specifies the way the client application and stub allocate and release memory for pointers.</span></span> <span data-ttu-id="74015-110">當您想要在遠端程序呼叫返回用戶端之後，讓伺服器應用程式能夠存取某些指標結構時，這個屬性會特別有用。</span><span class="sxs-lookup"><span data-stu-id="74015-110">This attribute is particularly useful when you want certain pointer structures to remain accessible to the server application after the remote procedure call returns to the client.</span></span> <span data-ttu-id="74015-111">您也可以使用 [ [**配置**](allocate.md) ] 屬性來指示存根，以計算透過指定型別之指標參考的所有記憶體大小，以及對 [**midl \_ 使用者 \_ 配置**](/windows/desktop/Rpc/the-midl-user-allocate-function)進行單一呼叫。</span><span class="sxs-lookup"><span data-stu-id="74015-111">You can also use the [**allocate**](allocate.md) attribute to direct the stub to compute the size of all memory referenced through the pointer of the specified type and to make a single call to [**midl\_user\_allocate**](/windows/desktop/Rpc/the-midl-user-allocate-function).</span></span> |
| [<span data-ttu-id="74015-112">**位元組 \_ 計數**</span><span class="sxs-lookup"><span data-stu-id="74015-112">**byte\_count**</span></span>](byte-count.md)           | <span data-ttu-id="74015-113">可讓您建立持續性的連續記憶體區塊，以在多個遠端程序呼叫上重複使用。</span><span class="sxs-lookup"><span data-stu-id="74015-113">Enables you to create a persistent, contiguous block of memory that can be reused over multiple remote procedure calls.</span></span> <span data-ttu-id="74015-114">這可釋出用戶端應用程式，避免重複配置和釋放記憶體的額外負荷，其中可能包含多個指標和其他複雜的資料結構。</span><span class="sxs-lookup"><span data-stu-id="74015-114">This frees the client application from the overhead of repeatedly allocating and releasing memory that may include multiple pointers and other complex data structures.</span></span>                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="74015-115">**啟用 \_ 配置**</span><span class="sxs-lookup"><span data-stu-id="74015-115">**enable\_allocate**</span></span>](enable-allocate.md) | <span data-ttu-id="74015-116">指定伺服器 stub 程式碼應啟用存根記憶體管理環境。</span><span class="sxs-lookup"><span data-stu-id="74015-116">Specifies that the server stub code should enable the stub memory-management environment.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

 

 