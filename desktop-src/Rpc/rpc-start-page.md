---
title: 遠端程序呼叫
description: Microsoft Remote Procedure Call (RPC) 定義了一種強大的技術，可用於建立分散式用戶端/伺服器程式。
ms.assetid: 27c7c352-5fc1-47cf-99b1-fdf3eca986bc
keywords:
- RPC
- 'RPC， (查看遠端程序呼叫) '
- 遠端程序呼叫 RPC，起始頁
- 遠端程序呼叫 RPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3461116468bf1d686d1a5695924e5fe66007b35
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382494"
---
# <a name="remote-procedure-call"></a><span data-ttu-id="83cf2-107">遠端程序呼叫</span><span class="sxs-lookup"><span data-stu-id="83cf2-107">Remote Procedure Call</span></span>

## <a name="purpose"></a><span data-ttu-id="83cf2-108">目的</span><span class="sxs-lookup"><span data-stu-id="83cf2-108">Purpose</span></span>

<span data-ttu-id="83cf2-109">Microsoft Remote Procedure Call (RPC) 定義了一種強大的技術，可用於建立分散式用戶端/伺服器程式。</span><span class="sxs-lookup"><span data-stu-id="83cf2-109">Microsoft Remote Procedure Call (RPC) defines a powerful technology for creating distributed client/server programs.</span></span> <span data-ttu-id="83cf2-110">RPC 執行時間存根和程式庫會管理與網路通訊協定和通訊相關的大部分處理常式。</span><span class="sxs-lookup"><span data-stu-id="83cf2-110">The RPC run-time stubs and libraries manage most of the processes relating to network protocols and communication.</span></span> <span data-ttu-id="83cf2-111">這可讓您將焦點放在應用程式的詳細資料，而不是網路的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="83cf2-111">This enables you to focus on the details of the application rather than the details of the network.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="83cf2-112">適用時</span><span class="sxs-lookup"><span data-stu-id="83cf2-112">Where applicable</span></span>

<span data-ttu-id="83cf2-113">RPC 可以在所有以 Windows 作業系統為基礎的用戶端/伺服器應用程式中使用。</span><span class="sxs-lookup"><span data-stu-id="83cf2-113">RPC can be used in all client/server applications based on Windows operating systems.</span></span> <span data-ttu-id="83cf2-114">它也可以用來建立適用于異類網路環境的用戶端和伺服器程式，這些環境包含 Unix 和 Apple 等作業系統。</span><span class="sxs-lookup"><span data-stu-id="83cf2-114">It can also be used to create client and server programs for heterogeneous network environments that include such operating systems as Unix and Apple.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="83cf2-115">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="83cf2-115">Developer audience</span></span>

<span data-ttu-id="83cf2-116">RPC 是設計來供 C/c + + 程式設計人員使用。</span><span class="sxs-lookup"><span data-stu-id="83cf2-116">RPC is designed to be used by C/C++ programmers.</span></span> <span data-ttu-id="83cf2-117">熟悉 Microsoft 介面定義語言 (MIDL) 和 MIDL 編譯器是必要的。</span><span class="sxs-lookup"><span data-stu-id="83cf2-117">Familiarity with the Microsoft Interface Definition Language (MIDL) and the MIDL compiler are required.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="83cf2-118">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="83cf2-118">Run-time requirements</span></span>

<span data-ttu-id="83cf2-119">RPC 執行時間程式庫隨附于 Windows。</span><span class="sxs-lookup"><span data-stu-id="83cf2-119">The RPC run-time libraries are included with Windows.</span></span> <span data-ttu-id="83cf2-120">當您安裝 Microsoft Windows 軟體開發套件 (SDK) 時，會安裝 RPC 開發環境的元件。</span><span class="sxs-lookup"><span data-stu-id="83cf2-120">The components of the RPC development environment are installed when you install the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="83cf2-121">如需詳細資訊，請參閱 [安裝 RPC 程式設計環境](installing-the-rpc-programming-environment.md)。</span><span class="sxs-lookup"><span data-stu-id="83cf2-121">For details, see [Installing the RPC Programming Environment](installing-the-rpc-programming-environment.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="83cf2-122">本節內容</span><span class="sxs-lookup"><span data-stu-id="83cf2-122">In this section</span></span>



| <span data-ttu-id="83cf2-123">主題</span><span class="sxs-lookup"><span data-stu-id="83cf2-123">Topic</span></span>                                                                           | <span data-ttu-id="83cf2-124">描述</span><span class="sxs-lookup"><span data-stu-id="83cf2-124">Description</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="83cf2-125">最佳的 RPC 程式設計實務</span><span class="sxs-lookup"><span data-stu-id="83cf2-125">Best RPC Programming Practices</span></span>](best-rpc-programming-practices.md)<br/> | <span data-ttu-id="83cf2-126">有關 RPC 程式設計實務的指引，可協助建立最可能的 RPC 應用程式。</span><span class="sxs-lookup"><span data-stu-id="83cf2-126">Guidance on RPC programming practices that help create the best possible RPC applications.</span></span><br/>                            |
| [<span data-ttu-id="83cf2-127">概觀</span><span class="sxs-lookup"><span data-stu-id="83cf2-127">Overview</span></span>](overviews.md)<br/>                                            | <span data-ttu-id="83cf2-128">將 RPC 併入用戶端/伺服器應用程式的一般資訊。</span><span class="sxs-lookup"><span data-stu-id="83cf2-128">General information about incorporating RPC into your client/server applications.</span></span><br/>                                     |
| [<span data-ttu-id="83cf2-129">參考</span><span class="sxs-lookup"><span data-stu-id="83cf2-129">Reference</span></span>](reference.md)<br/>                                           | <span data-ttu-id="83cf2-130">RPC 類型、函數和常數的檔。</span><span class="sxs-lookup"><span data-stu-id="83cf2-130">Documentation of RPC types, functions, and constants.</span></span><br/>                                                                 |
| [<span data-ttu-id="83cf2-131">RPC NDR 引擎</span><span class="sxs-lookup"><span data-stu-id="83cf2-131">RPC NDR Engine</span></span>](rpc-ndr-engine.md)<br/>                                 | <span data-ttu-id="83cf2-132">RPC 和 DCOM 元件的封送處理引擎檔，RPC 網路資料標記法 (NDR) 引擎。</span><span class="sxs-lookup"><span data-stu-id="83cf2-132">Documentation of the marshaling engine for RPC and DCOM components, the RPC Network Data Representation (NDR) Engine.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="83cf2-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="83cf2-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83cf2-134">Microsoft 介面定義語言 (MIDL) </span><span class="sxs-lookup"><span data-stu-id="83cf2-134">Microsoft Interface Definition Language (MIDL)</span></span>](/windows/desktop/Midl/midl-start-page)
</dt> </dl>

 

