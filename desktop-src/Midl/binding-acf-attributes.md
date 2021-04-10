---
title: 系結 ACF 屬性
description: 使用下表所列的屬性，指定用戶端如何連接到伺服器以進行遠端程序呼叫。
ms.assetid: 2a9fdd2f-c646-4ccd-bfa8-66fe973ef911
keywords:
- ACF MIDL、屬性、系結
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2a2e9ac9ada0ee33c4930005add6a1ca031ee5a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021846"
---
# <a name="binding-acf-attributes"></a><span data-ttu-id="dd8b1-104">系結 ACF 屬性</span><span class="sxs-lookup"><span data-stu-id="dd8b1-104">Binding ACF Attributes</span></span>

<span data-ttu-id="dd8b1-105">使用下表所列的屬性，指定用戶端如何連接到伺服器以進行遠端程序呼叫。</span><span class="sxs-lookup"><span data-stu-id="dd8b1-105">Specify how the client connects to the server for remote procedure calls with the attributes listed in the following table.</span></span>



| <span data-ttu-id="dd8b1-106">屬性</span><span class="sxs-lookup"><span data-stu-id="dd8b1-106">Attribute</span></span>                                                          | <span data-ttu-id="dd8b1-107">使用方式</span><span class="sxs-lookup"><span data-stu-id="dd8b1-107">Usage</span></span>                                                                                                                                                                                                              |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dd8b1-108">**async**</span><span class="sxs-lookup"><span data-stu-id="dd8b1-108">**async**</span></span>](async.md)                                             | <span data-ttu-id="dd8b1-109">定義控制碼，這個控制碼可讓呼叫者進行非同步呼叫，並在不等候結果的情況下立即傳回，然後在呼叫完成之後，再重新同步處理被呼叫的函式以接收資料。</span><span class="sxs-lookup"><span data-stu-id="dd8b1-109">Defines a handle that allows the caller to make an asynchronous call and return immediately without waiting for results, and then resynchronize with the called function to receive data after the call completes.</span></span> |
| [<span data-ttu-id="dd8b1-110">**自動 \_ 處理**</span><span class="sxs-lookup"><span data-stu-id="dd8b1-110">**auto\_handle**</span></span>](auto-handle.md)                                | <span data-ttu-id="dd8b1-111">告知 MIDL 讓存根程式碼可自動控制系結。</span><span class="sxs-lookup"><span data-stu-id="dd8b1-111">Tells MIDL to let the stub code control the binding automatically.</span></span> <span data-ttu-id="dd8b1-112">如果您未指定任何系結控制碼，這就是預設值。</span><span class="sxs-lookup"><span data-stu-id="dd8b1-112">This is the default if you don't specify any binding handle.</span></span>                                                                                    |
| [<span data-ttu-id="dd8b1-113">**內容 \_ 控制碼 \_ noserialize**</span><span class="sxs-lookup"><span data-stu-id="dd8b1-113">**context\_handle\_noserialize**</span></span>](context-handle-noserialize.md) | <span data-ttu-id="dd8b1-114">保證不論應用程式的預設行為為何，都不會序列化內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="dd8b1-114">Guarantees that a context handle will never be serialized, regardless of the application's default behavior.</span></span>                                                                                                       |
| [<span data-ttu-id="dd8b1-115">**內容 \_ 控制碼 \_ 序列化**</span><span class="sxs-lookup"><span data-stu-id="dd8b1-115">**context\_handle\_serialize**</span></span>](context-handle-serialize.md)     | <span data-ttu-id="dd8b1-116">保證無論應用程式的預設行為為何，都將一律序列化內容控制碼</span><span class="sxs-lookup"><span data-stu-id="dd8b1-116">Guarantees that a context handle will always be serialized, regardless of the application's default behavior</span></span>                                                                                                       |
| [<span data-ttu-id="dd8b1-117">**明確 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="dd8b1-117">**explicit\_handle**</span></span>](explicit-handle.md)                        | <span data-ttu-id="dd8b1-118">讓用戶端應用程式使用每個程式中的明確參數來控制系結。</span><span class="sxs-lookup"><span data-stu-id="dd8b1-118">Lets the client application control the binding with an explicit parameter in each procedure.</span></span>                                                                                                                      |
| [<span data-ttu-id="dd8b1-119">**隱含 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="dd8b1-119">**implicit\_handle**</span></span>](implicit-handle.md)                        | <span data-ttu-id="dd8b1-120">指定沒有明確控制碼參數之程式的控制碼。</span><span class="sxs-lookup"><span data-stu-id="dd8b1-120">Specifies a handle for procedures that do not have an explicit handle parameter.</span></span> <span data-ttu-id="dd8b1-121">用戶端應用程式仍然會控制系結。</span><span class="sxs-lookup"><span data-stu-id="dd8b1-121">The client application still controls the binding.</span></span>                                                                                |
| [<span data-ttu-id="dd8b1-122">**strict \_ 內容 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="dd8b1-122">**strict\_context\_handle**</span></span>](strict-context-handle.md)           | <span data-ttu-id="dd8b1-123">保證介面中的方法只會接受該介面的方法所建立的內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="dd8b1-123">Guarantees that the methods in the interface will only accept context handles that were created by a method of that interface.</span></span>                                                                                     |



 

 

 




