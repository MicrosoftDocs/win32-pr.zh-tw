---
title: 開發用戶端
description: 開發 RPC 用戶端程式與開發伺服器程式類似。 如需有關開發 RPC 伺服器程式的詳細資訊，請參閱開發伺服器。
ms.assetid: 92276326-d478-479e-8fa4-02a2fce58eb6
keywords:
- 遠端程序呼叫 RPC、工作、開發用戶端
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10ceddedc4ccfd1d068e3452b64ed8c6b54a621d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933519"
---
# <a name="developing-the-client"></a><span data-ttu-id="367b8-105">開發用戶端</span><span class="sxs-lookup"><span data-stu-id="367b8-105">Developing the Client</span></span>

<span data-ttu-id="367b8-106">開發 RPC 用戶端程式與開發伺服器程式類似。</span><span class="sxs-lookup"><span data-stu-id="367b8-106">Developing an RPC client program is similar to developing the server program.</span></span> <span data-ttu-id="367b8-107">如需有關開發 RPC 伺服器程式的詳細資訊，請參閱 [開發伺服器](developing-the-server.md)。</span><span class="sxs-lookup"><span data-stu-id="367b8-107">For information on developing an RPC server program, see [Developing the Server](developing-the-server.md).</span></span>

<span data-ttu-id="367b8-108">在伺服器開發中，您的用戶端程式必須包含 MIDL 編譯器從 .idl 檔產生的標頭檔。</span><span class="sxs-lookup"><span data-stu-id="367b8-108">As in server development, your client program must include the header file that the MIDL compiler generates from your .idl file.</span></span> <span data-ttu-id="367b8-109">MIDL 編譯器也會產生包含用戶端存根的 C 來源檔案。</span><span class="sxs-lookup"><span data-stu-id="367b8-109">The MIDL compiler also generates a C source file containing the client stub.</span></span> <span data-ttu-id="367b8-110">您必須編譯此 C 原始程式檔，並將它連結至您的用戶端程式。</span><span class="sxs-lookup"><span data-stu-id="367b8-110">You must compile this C source file and link it to your client program.</span></span> <span data-ttu-id="367b8-111"> (此外，MIDL 編譯器會產生包含伺服器 stub 的 C 原始程式檔，但與此討論無關。 ) </span><span class="sxs-lookup"><span data-stu-id="367b8-111">(In addition, the MIDL compiler generates a C source file containing the server stub, but that is not relevant to this discussion.)</span></span>

<span data-ttu-id="367b8-112">除了使用程式檔編譯和連結用戶端 stub 之外，您還必須將匯入程式庫 (以及用戶端程式所需的任何其他程式庫) 至用戶端程式。</span><span class="sxs-lookup"><span data-stu-id="367b8-112">In addition to compiling and linking the client stub with your program files, you must link the import library (and any other libraries your client program needs) to your client program.</span></span> <span data-ttu-id="367b8-113">下圖說明建立 RPC 用戶端程式的流程。</span><span class="sxs-lookup"><span data-stu-id="367b8-113">The process of creating an RPC client program is illustrated in the following diagram.</span></span>

![建立分散式應用程式之用戶端程式的流程](images/clntdev.png)

<span data-ttu-id="367b8-115">上圖中的範例將示範如何建立稱為 MyClnt.exe 的 RPC 用戶端程式。</span><span class="sxs-lookup"><span data-stu-id="367b8-115">The example in the preceding illustration demonstrates the creation of an RPC client program called MyClnt.exe.</span></span> <span data-ttu-id="367b8-116">第一個步驟是在檔案 MyApp 中定義介面。</span><span class="sxs-lookup"><span data-stu-id="367b8-116">The first step is to define the interface in the file MyApp.idl.</span></span> <span data-ttu-id="367b8-117">MIDL 編譯器會使用 MyApp 來產生 \_ 包含用戶端 stub 的檔案 myapp c.。</span><span class="sxs-lookup"><span data-stu-id="367b8-117">The MIDL compiler uses MyApp.idl to generate the file MyApp\_c.c, which contains the client stub.</span></span> <span data-ttu-id="367b8-118">它也會產生一個 MyApp，也就是用戶端程式必須包含的檔案 MyApp。</span><span class="sxs-lookup"><span data-stu-id="367b8-118">It also generates the file MyApp.h, which the client program must include.</span></span> <span data-ttu-id="367b8-119">用戶端程式也必須包含檔案的 RPC 和 RPCNDR。</span><span class="sxs-lookup"><span data-stu-id="367b8-119">The client program will also need to include the files RPC.h and RPCNDR.h.</span></span>

<span data-ttu-id="367b8-120">用戶端程式本身是在 MyClnt 檔案中建立的。</span><span class="sxs-lookup"><span data-stu-id="367b8-120">The client program itself is created in the file MyClnt.c.</span></span> <span data-ttu-id="367b8-121">在實際的專案中，用戶端程式通常是由數個 C 原始程式檔所組成。</span><span class="sxs-lookup"><span data-stu-id="367b8-121">In a real project, the client program would typically be composed of several C source files.</span></span> <span data-ttu-id="367b8-122">所有這些都必須一起編譯和連結。</span><span class="sxs-lookup"><span data-stu-id="367b8-122">All of them would need to be compiled and linked together.</span></span> <span data-ttu-id="367b8-123">不過，此範例只會使用一個檔案，以簡化程式。</span><span class="sxs-lookup"><span data-stu-id="367b8-123">However, this example uses only one file for simplicity.</span></span>

<span data-ttu-id="367b8-124">MyClnt \_ 檔案會進行編譯並連結至 RPC 執行時間程式庫，以及用戶端程式所需的任何其他程式庫。</span><span class="sxs-lookup"><span data-stu-id="367b8-124">The files MyClnt.c and MyApp\_c.c are compiled and linked together with the RPC run-time library, and any other libraries that the client program needs.</span></span> <span data-ttu-id="367b8-125">結果會是名為 MyClnt.exe 的可執行用戶端程式。</span><span class="sxs-lookup"><span data-stu-id="367b8-125">The result is an executable client program named MyClnt.exe.</span></span>

<span data-ttu-id="367b8-126">如果您沒有在憑證相容性模式中編譯 IDL 檔案 ([**/osf**](/windows/desktop/Midl/-osf)) ，您的用戶端程式必須提供用來配置記憶體的函式，以及用來解除配置的功能。</span><span class="sxs-lookup"><span data-stu-id="367b8-126">If you do not compile your IDL file in OSF compatibility mode ([**/osf**](/windows/desktop/Midl/-osf)), your client program must provide a function for allocating memory and a function for deallocating it.</span></span> <span data-ttu-id="367b8-127">若為 Windows 2000 和更新版本，建議模式為 [**/Oicf**](/windows/desktop/Midl/-oi)。</span><span class="sxs-lookup"><span data-stu-id="367b8-127">For Windows 2000 and later versions, the recommended mode is [**/Oicf**](/windows/desktop/Midl/-oi).</span></span> <span data-ttu-id="367b8-128">如需詳細資訊，請參閱 [如何配置和解除配置記憶體](how-memory-is-allocated-and-deallocated.md)，以及 [指標和記憶體配置](pointers-and-memory-allocation.md)。</span><span class="sxs-lookup"><span data-stu-id="367b8-128">For details, see [How Memory Is Allocated and Deallocated](how-memory-is-allocated-and-deallocated.md), and [Pointers and Memory Allocation](pointers-and-memory-allocation.md).</span></span>

 

 