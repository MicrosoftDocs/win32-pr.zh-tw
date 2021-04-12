---
title: 開發伺服器
description: 當您建立分散式應用程式的伺服器程式時，必須使用 MIDL 編譯器所產生的標頭檔和伺服器 stub。
ms.assetid: 2b7b14f5-5692-41b8-bb98-7edd36309d21
keywords:
- 遠端程序呼叫 RPC、工作、開發伺服器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fc3405c52c48f531572ab159ad083bad93f95e0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316075"
---
# <a name="developing-the-server"></a><span data-ttu-id="e7a17-104">開發伺服器</span><span class="sxs-lookup"><span data-stu-id="e7a17-104">Developing the Server</span></span>

<span data-ttu-id="e7a17-105">當您建立分散式應用程式的伺服器程式時，必須使用 MIDL 編譯器所產生的標頭檔和伺服器 stub。</span><span class="sxs-lookup"><span data-stu-id="e7a17-105">When you create a server program for a distributed application, you must use the header file and server stub that the MIDL compiler generates.</span></span> <span data-ttu-id="e7a17-106">如需詳細資訊，請參閱 [開發介面](developing-the-interface.md)。</span><span class="sxs-lookup"><span data-stu-id="e7a17-106">For details, see [Developing the Interface](developing-the-interface.md).</span></span> <span data-ttu-id="e7a17-107">將標頭檔包含在您的伺服器 C 程式檔中。</span><span class="sxs-lookup"><span data-stu-id="e7a17-107">Include the header file in your server C program file.</span></span> <span data-ttu-id="e7a17-108">以撰寫您應用程式的 C 原始程式檔編譯伺服器 stub。</span><span class="sxs-lookup"><span data-stu-id="e7a17-108">Compile the server stub with the C source files that compose your application.</span></span> <span data-ttu-id="e7a17-109">將產生的物件檔案與匯入程式庫連結在一起。</span><span class="sxs-lookup"><span data-stu-id="e7a17-109">Link the resulting object files together with the import library.</span></span> <span data-ttu-id="e7a17-110">下圖說明此程式。</span><span class="sxs-lookup"><span data-stu-id="e7a17-110">This process is illustrated in the following diagram.</span></span>

![為分散式應用程式建立伺服器程式的流程](images/srvrdev.png)

<span data-ttu-id="e7a17-112">您可以從圖例的範例中看到，使用稱為 MyApp 的 MIDL 檔案來定義介面。</span><span class="sxs-lookup"><span data-stu-id="e7a17-112">As you can see from the example in the illustration, a MIDL file called MyApp.idl was used to define the interface.</span></span> <span data-ttu-id="e7a17-113">MIDL 編譯器使用 MyApp 來產生 MyApp. \_ c 和 myapp. h。</span><span class="sxs-lookup"><span data-stu-id="e7a17-113">The MIDL compiler used MyApp.idl to produce MyApp\_s.c and MyApp.h.</span></span> <span data-ttu-id="e7a17-114">它也會產生用戶端存根的 C 來源檔案，但這與這項特定討論無關。</span><span class="sxs-lookup"><span data-stu-id="e7a17-114">It also produces a C source file for the client stub, but that is not relevant to this particular discussion.</span></span> <span data-ttu-id="e7a17-115">伺服器程式的 C 原始程式檔 (在此情況下，Mysrvr) 必須包含檔案 Myapp. h。</span><span class="sxs-lookup"><span data-stu-id="e7a17-115">The C source file for the server program (in this case, Mysrvr.c) must include the file Myapp.h.</span></span> <span data-ttu-id="e7a17-116">此外，它也必須包含檔案 Rpc 和 Rpcndr .h。</span><span class="sxs-lookup"><span data-stu-id="e7a17-116">It will also need to include the files Rpc.h and Rpcndr.h.</span></span>

<span data-ttu-id="e7a17-117">伺服器應用程式是以兩個檔案（Mysrvr .c 和 Rprocs）開發的。</span><span class="sxs-lookup"><span data-stu-id="e7a17-117">The server application was developed in two files, Mysrvr.c and Rprocs.c.</span></span> <span data-ttu-id="e7a17-118">File Mysrvr 包含讓伺服器程式啟動並執行所需的功能。</span><span class="sxs-lookup"><span data-stu-id="e7a17-118">The file Mysrvr.c contains the functions necessary for getting the server program up and running.</span></span> <span data-ttu-id="e7a17-119">伺服器程式所提供的遠端套裝程式含在 file Rprocs 中。</span><span class="sxs-lookup"><span data-stu-id="e7a17-119">The remote procedures that the server program offers are contained in the file Rprocs.c.</span></span>

<span data-ttu-id="e7a17-120">Mysrvr 和 Rprocs 檔案會與 Myapp 一起編譯以產生目的檔。 \_</span><span class="sxs-lookup"><span data-stu-id="e7a17-120">The files Mysrvr.c and Rprocs.c were compiled together with Myapp\_s.c to produce object files.</span></span> <span data-ttu-id="e7a17-121">然後，會將物件檔案與 RPC 執行時間程式庫和其他任何可能需要的程式庫連結在一起。</span><span class="sxs-lookup"><span data-stu-id="e7a17-121">The object files were then linked with the RPC run-time library, and any other libraries that they might need.</span></span> <span data-ttu-id="e7a17-122">結果會是名為 Mysrvr.exe 的可執行伺服器程式。</span><span class="sxs-lookup"><span data-stu-id="e7a17-122">The result is an executable server program named Mysrvr.exe.</span></span>

<span data-ttu-id="e7a17-123">如果您未在 Open Software Foundation 中編譯 IDL 檔案 (憑證) 相容性模式 ([**/osf**](/windows/desktop/Midl/-osf)) ，則您的伺服器程式必須提供用來配置記憶體的函式，以及用來解除配置的功能。</span><span class="sxs-lookup"><span data-stu-id="e7a17-123">If you do not compile your IDL file in Open Software Foundation (OSF) compatibility mode ([**/osf**](/windows/desktop/Midl/-osf)), your server program must provide a function for allocating memory and a function for deallocating it.</span></span> <span data-ttu-id="e7a17-124">若為 Windows 2000 和更新版本的 Windows，建議模式為 [**/Oicf**](/windows/desktop/Midl/-oi)。</span><span class="sxs-lookup"><span data-stu-id="e7a17-124">For Windows 2000 and later versions of Windows, the recommended mode is [**/Oicf**](/windows/desktop/Midl/-oi).</span></span> <span data-ttu-id="e7a17-125">如需詳細資訊，請參閱 [如何配置和解除配置記憶體](how-memory-is-allocated-and-deallocated.md)，以及 [指標和記憶體配置](pointers-and-memory-allocation.md)。</span><span class="sxs-lookup"><span data-stu-id="e7a17-125">For details, see [How Memory Is Allocated and Deallocated](how-memory-is-allocated-and-deallocated.md), and [Pointers and Memory Allocation](pointers-and-memory-allocation.md).</span></span>

 

 