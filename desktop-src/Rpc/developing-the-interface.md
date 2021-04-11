---
title: 開發介面
description: RPC 介面會描述伺服器程式所實行的遠端函式。
ms.assetid: f0dfe9d1-fe84-461c-8684-147fbd0bdefe
keywords:
- 遠端程序呼叫 RPC、工作、開發介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68b6f720bcd492e784ad07fe20e221ac54951680
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104093059"
---
# <a name="developing-the-interface"></a><span data-ttu-id="aca4b-104">開發介面</span><span class="sxs-lookup"><span data-stu-id="aca4b-104">Developing the Interface</span></span>

<span data-ttu-id="aca4b-105">RPC 介面會描述伺服器程式所實行的遠端函式。</span><span class="sxs-lookup"><span data-stu-id="aca4b-105">An RPC interface describes the remote functions that the server program implements.</span></span> <span data-ttu-id="aca4b-106">介面可確保用戶端和伺服器會在用戶端叫用伺服器提供的遠端程式時，使用相同的規則進行通訊。</span><span class="sxs-lookup"><span data-stu-id="aca4b-106">The interface ensures that the client and server communicate using the same rules when the client invokes a remote procedure that the server offers.</span></span> <span data-ttu-id="aca4b-107">介面是由介面名稱、某些屬性、選擇性類型或常數定義，以及一組程式聲明所組成。</span><span class="sxs-lookup"><span data-stu-id="aca4b-107">An interface consists of an interface name, some attributes, optional type or constant definitions, and a set of procedure declarations.</span></span> <span data-ttu-id="aca4b-108">每個程式宣告都必須包含程式名稱、傳回型別和參數清單。</span><span class="sxs-lookup"><span data-stu-id="aca4b-108">Each procedure declaration must contain a procedure name, return type, and parameter list.</span></span>

<span data-ttu-id="aca4b-109">介面是以 Microsoft 介面定義語言 (MIDL) 來定義。</span><span class="sxs-lookup"><span data-stu-id="aca4b-109">Interfaces are defined in the Microsoft Interface Definition Language (MIDL).</span></span> <span data-ttu-id="aca4b-110">如果您熟悉 C 或 c + +，MIDL 介面定義看起來會相當簡單。</span><span class="sxs-lookup"><span data-stu-id="aca4b-110">If you are familiar with C or C++, MIDL interface definitions will seem fairly straightforward.</span></span> <span data-ttu-id="aca4b-111">MIDL 在許多方面類似 C 和 c + +。</span><span class="sxs-lookup"><span data-stu-id="aca4b-111">MIDL resembles C and C++ in many ways.</span></span>

<span data-ttu-id="aca4b-112">開發 RPC 應用程式時，會使用文字編輯器來定義介面，並將它儲存在副檔名為 .idl 的文字檔中。</span><span class="sxs-lookup"><span data-stu-id="aca4b-112">When developing an RPC application, a text editor is used to define the interface and store it in a text file with an .idl extension.</span></span> <span data-ttu-id="aca4b-113">如需詳細資訊，請參閱 [IDL 和 ACF](the-idl-and-acf-files.md)檔。</span><span class="sxs-lookup"><span data-stu-id="aca4b-113">For more information, see [The IDL and ACF Files](the-idl-and-acf-files.md).</span></span> <span data-ttu-id="aca4b-114">MIDL 編譯器會產生您的程式在用戶端和伺服器原始程式檔中所包含的標頭檔。</span><span class="sxs-lookup"><span data-stu-id="aca4b-114">The MIDL compiler generates a header file that your program includes in the client and server source files.</span></span> <span data-ttu-id="aca4b-115">MIDL 編譯器也會產生兩個 C 來源檔案。</span><span class="sxs-lookup"><span data-stu-id="aca4b-115">The MIDL compiler also generates two C source files.</span></span> <span data-ttu-id="aca4b-116">您可以將其中一個連結至您的用戶端程式，並將另一個連結至您的伺服器程式。</span><span class="sxs-lookup"><span data-stu-id="aca4b-116">You compile and link one of these to your client program, and the other to your server program.</span></span> <span data-ttu-id="aca4b-117">這兩個 C 來源檔案是用戶端和伺服器 stub。</span><span class="sxs-lookup"><span data-stu-id="aca4b-117">These two C source files are the client and server stubs.</span></span> <span data-ttu-id="aca4b-118">如需用戶端和伺服器 stub 的總覽，請參閱 [RPC 的運作方式](how-rpc-works.md)。</span><span class="sxs-lookup"><span data-stu-id="aca4b-118">For an overview of the client and server stubs, see [How RPC Works](how-rpc-works.md).</span></span> <span data-ttu-id="aca4b-119">如需 MIDL 編譯器的總覽，請參閱 [編譯 midl](using-midl.md)檔案。</span><span class="sxs-lookup"><span data-stu-id="aca4b-119">For an overview on the MIDL compiler, see [Compiling a MIDL File](using-midl.md).</span></span>

<span data-ttu-id="aca4b-120">根據預設，用戶端和伺服器 stub 都有相同的名稱，如果用戶端與伺服器 stub 連結，則可能會造成問題，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="aca4b-120">By default, the client and server stub have the same name, which can cause problems if the client links with the server stub, or vice-versa.</span></span> <span data-ttu-id="aca4b-121">使用 MIDL [**/prefix**](/windows/desktop/Midl/-prefix) 選項可防止發生這個常見的錯誤。</span><span class="sxs-lookup"><span data-stu-id="aca4b-121">Using the MIDL [**/prefix**](/windows/desktop/Midl/-prefix) option prevents this common error from occurring.</span></span>

<span data-ttu-id="aca4b-122">下圖顯示建立介面的程式。</span><span class="sxs-lookup"><span data-stu-id="aca4b-122">The following illustration shows the process of creating an interface.</span></span>

![使用/prefix 選項建立用戶端和伺服器 stub，以防止意外的編譯問題](images/idldev.png)

<span data-ttu-id="aca4b-124">您也可能需要指定應用程式佈建檔， (ACF) ，以輸入 MIDL 編譯器。</span><span class="sxs-lookup"><span data-stu-id="aca4b-124">It is possible that you will also need to specify an application configuration file (ACF) for input to the MIDL compiler as well.</span></span> <span data-ttu-id="aca4b-125">如需應用程式佈建檔的詳細資訊，請參閱 [IDL 和 ACF](the-idl-and-acf-files.md)檔。</span><span class="sxs-lookup"><span data-stu-id="aca4b-125">For more information on application configuration files, see [The IDL and ACF Files](the-idl-and-acf-files.md).</span></span>

<span data-ttu-id="aca4b-126">除了 MIDL 編譯器之外，您通常還需要使用 Uuidgen.exe 公用程式來產生 (UUID 的通用唯一識別碼，並與「GUID) 」一詞交換。</span><span class="sxs-lookup"><span data-stu-id="aca4b-126">In addition to the MIDL compiler, you will typically need to use the Uuidgen utility to generate a Universal Unique Identifier (UUID, interchangeable with the term GUID).</span></span> <span data-ttu-id="aca4b-127">本節提供這兩種工具的相關資訊，分為下列主題：</span><span class="sxs-lookup"><span data-stu-id="aca4b-127">This section presents information on both of these tools, divided into the following topics:</span></span>

-   [<span data-ttu-id="aca4b-128">產生介面 Uuid</span><span class="sxs-lookup"><span data-stu-id="aca4b-128">Generating Interface UUIDs</span></span>](generating-interface-uuids.md)
-   [<span data-ttu-id="aca4b-129">使用 MIDL</span><span class="sxs-lookup"><span data-stu-id="aca4b-129">Using MIDL</span></span>](using-midl.md)

 

 