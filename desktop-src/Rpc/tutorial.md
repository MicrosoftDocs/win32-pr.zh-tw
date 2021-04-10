---
title: 教學課程
description: 本教學課程會引導您完成從現有的獨立應用程式建立簡單、單一用戶端單一伺服器分散式應用程式所需的步驟。
ms.assetid: afdfa037-58c0-4dcf-aa27-6839db0515e6
keywords:
- 遠端程序呼叫 RPC，教學課程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7c19b0d8ec3b3eb55cf29ccfd87eca43775c2ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021813"
---
# <a name="tutorial"></a><span data-ttu-id="dce35-104">教學課程</span><span class="sxs-lookup"><span data-stu-id="dce35-104">Tutorial</span></span>

<span data-ttu-id="dce35-105">本教學課程會引導您完成從現有的獨立應用程式建立簡單、單一用戶端單一伺服器分散式應用程式所需的步驟。</span><span class="sxs-lookup"><span data-stu-id="dce35-105">This tutorial takes you through the steps required to create a simple, single-client, single-server distributed application from an existing standalone application.</span></span> <span data-ttu-id="dce35-106">這些步驟包括：</span><span class="sxs-lookup"><span data-stu-id="dce35-106">These steps are:</span></span>

-   <span data-ttu-id="dce35-107">建立介面定義和應用程式佈建檔。</span><span class="sxs-lookup"><span data-stu-id="dce35-107">Create interface definition and application configuration files.</span></span>
-   <span data-ttu-id="dce35-108">使用 MIDL 編譯器，從這些檔案產生 C 語言用戶端和伺服器 stub 和標頭。</span><span class="sxs-lookup"><span data-stu-id="dce35-108">Use the MIDL compiler to generate C-language client and server stubs and headers from those files.</span></span>
-   <span data-ttu-id="dce35-109">撰寫用戶端應用程式，以管理其與伺服器的連接。</span><span class="sxs-lookup"><span data-stu-id="dce35-109">Write a client application that manages its connection to the server.</span></span>
-   <span data-ttu-id="dce35-110">撰寫包含實際遠端程式的伺服器應用程式。</span><span class="sxs-lookup"><span data-stu-id="dce35-110">Write a server application that contains the actual remote procedures.</span></span>
-   <span data-ttu-id="dce35-111">將這些檔案編譯並連結至 RPC 執行時間程式庫，以產生分散式應用程式。</span><span class="sxs-lookup"><span data-stu-id="dce35-111">Compile and link these files to the RPC run-time library to produce the distributed application.</span></span>

<span data-ttu-id="dce35-112">用戶端應用程式會在遠端程序呼叫中，將字元字串傳遞給伺服器，而伺服器會將字串 "Hello，World" 列印到其標準輸出。</span><span class="sxs-lookup"><span data-stu-id="dce35-112">The client application passes a character string to the server in a remote procedure call, and the server prints the string "Hello, World" to its standard output.</span></span>

<span data-ttu-id="dce35-113">這個範例應用程式的完整原始程式檔，以及用來處理命令列輸入的額外程式碼，以及將各種狀態訊息輸出到使用者的程式，都位於 \\ 平臺軟體發展工具組 (SDK) 的 RPC Hello 目錄中。</span><span class="sxs-lookup"><span data-stu-id="dce35-113">The complete source files for this example application, with additional code to handle command-line input and to output various status messages to the user, are in the RPC\\Hello directory of the Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="dce35-114">本節提供下列主題的討論：</span><span class="sxs-lookup"><span data-stu-id="dce35-114">This section presents its discussion in the following topics:</span></span>

-   [<span data-ttu-id="dce35-115">獨立應用程式</span><span class="sxs-lookup"><span data-stu-id="dce35-115">The Standalone Application</span></span>](the-standalone-application.md)
-   [<span data-ttu-id="dce35-116">定義介面</span><span class="sxs-lookup"><span data-stu-id="dce35-116">Defining the Interface</span></span>](defining-the-interface.md)
-   [<span data-ttu-id="dce35-117">產生 UUID</span><span class="sxs-lookup"><span data-stu-id="dce35-117">Generating the UUID</span></span>](generating-the-uuid.md)
-   [<span data-ttu-id="dce35-118">IDL 檔案</span><span class="sxs-lookup"><span data-stu-id="dce35-118">The IDL File</span></span>](the-idl-file.md)
-   [<span data-ttu-id="dce35-119">ACF 檔案</span><span class="sxs-lookup"><span data-stu-id="dce35-119">The ACF File</span></span>](the-acf-file.md)
-   [<span data-ttu-id="dce35-120">產生存根檔案</span><span class="sxs-lookup"><span data-stu-id="dce35-120">Generating the Stub Files</span></span>](generating-the-stub-files.md)
-   [<span data-ttu-id="dce35-121">用戶端應用程式</span><span class="sxs-lookup"><span data-stu-id="dce35-121">The Client Application</span></span>](the-client-application.md)
-   [<span data-ttu-id="dce35-122">伺服器應用程式</span><span class="sxs-lookup"><span data-stu-id="dce35-122">The Server Application</span></span>](the-server-application.md)
-   [<span data-ttu-id="dce35-123">停止伺服器應用程式</span><span class="sxs-lookup"><span data-stu-id="dce35-123">Stopping the Server Application</span></span>](stopping-the-server-application.md)
-   [<span data-ttu-id="dce35-124">編譯和連結</span><span class="sxs-lookup"><span data-stu-id="dce35-124">Compiling and Linking</span></span>](compiling-and-linking.md)
-   [<span data-ttu-id="dce35-125">執行應用程式</span><span class="sxs-lookup"><span data-stu-id="dce35-125">Running the Application</span></span>](running-the-application.md)

 

 




