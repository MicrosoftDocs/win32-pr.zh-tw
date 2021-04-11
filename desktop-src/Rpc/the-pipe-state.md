---
title: 管道狀態
description: 在伺服器上，MIDL 編譯器會建立可協調 push、pull 和配置程式的狀態變數。
ms.assetid: 7cc59cb3-cf41-40f7-a28f-b896c319ae64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6d7ec8af1907c98b7cf2098f4979dac62ef573a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092904"
---
# <a name="the-pipe-state"></a><span data-ttu-id="0deff-103">管道狀態</span><span class="sxs-lookup"><span data-stu-id="0deff-103">The Pipe State</span></span>

<span data-ttu-id="0deff-104">在伺服器上，MIDL 編譯器會建立可協調 push、pull 和配置程式的 *狀態* 變數。</span><span class="sxs-lookup"><span data-stu-id="0deff-104">On the server, the MIDL compiler creates a *state* variable that coordinates push, pull, and alloc procedures.</span></span> <span data-ttu-id="0deff-105">在用戶端上，開發人員必須建立 *狀態* 變數。</span><span class="sxs-lookup"><span data-stu-id="0deff-105">On the client side, the developer must create the *state* variable.</span></span> <span data-ttu-id="0deff-106">因此， *狀態* 變數是兩端的區域—亦即，用戶端和伺服器都維持自己的管道狀態。</span><span class="sxs-lookup"><span data-stu-id="0deff-106">Therefore, the *state* variable is local to both sides—that is, the client and server each maintain their own pipe state.</span></span> <span data-ttu-id="0deff-107">伺服器 stub 程式碼會維護伺服器上的狀態變數。</span><span class="sxs-lookup"><span data-stu-id="0deff-107">The server stub code maintains the state variable on the server.</span></span> <span data-ttu-id="0deff-108">您不應該嘗試直接修改它的內容。</span><span class="sxs-lookup"><span data-stu-id="0deff-108">You should not attempt to modify its contents directly.</span></span> <span data-ttu-id="0deff-109">用戶端必須初始化管道控制結構中的欄位，並維護其 *狀態* 變數。</span><span class="sxs-lookup"><span data-stu-id="0deff-109">The client must initialize the fields in the pipe control structure and maintain its *state* variable.</span></span> <span data-ttu-id="0deff-110">它會使用 *狀態* 變數來識別要找出或放置資料的位置。</span><span class="sxs-lookup"><span data-stu-id="0deff-110">It uses the *state* variable to identify where to locate or place data.</span></span>

<span data-ttu-id="0deff-111">如果您要將資料從某個檔案傳送到另一個檔案，用戶端 *狀態* 變數可以像檔案控制代碼一樣簡單。</span><span class="sxs-lookup"><span data-stu-id="0deff-111">The client *state* variable can be as simple as a file handle, if you are transferring data from one file to another.</span></span> <span data-ttu-id="0deff-112">它也可以是指向陣列中之元素的整數。</span><span class="sxs-lookup"><span data-stu-id="0deff-112">It can also be an integer that points to an element in an array.</span></span> <span data-ttu-id="0deff-113">或者，您可以定義相當複雜的狀態結構來執行其他工作，例如協調 \[ [in](/windows/desktop/Midl/in)、 [out](/windows/desktop/Midl/out-idl)參數的推送和提取常式 \] 。</span><span class="sxs-lookup"><span data-stu-id="0deff-113">Or you can define a fairly complex state structure to perform additional tasks, such as coordinating the push and pull routines on an \[ [in](/windows/desktop/Midl/in), [out](/windows/desktop/Midl/out-idl)\] parameter.</span></span>

 

 