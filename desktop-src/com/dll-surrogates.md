---
title: DLL 代理
description: DLL 代理
ms.assetid: fe30c0ae-1d19-4a5f-8ee3-8a5337c79c44
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 313c3fcbd07b4c6317dfb6ac8ede772fc62035f0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969880"
---
# <a name="dll-surrogates"></a><span data-ttu-id="8a3d1-103">DLL 代理</span><span class="sxs-lookup"><span data-stu-id="8a3d1-103">DLL Surrogates</span></span>

<span data-ttu-id="8a3d1-104">COM 可讓您建立可載入至代理 EXE 進程的 DLL 伺服器。</span><span class="sxs-lookup"><span data-stu-id="8a3d1-104">COM makes it possible to create DLL servers that can be loaded into a surrogate EXE process.</span></span> <span data-ttu-id="8a3d1-105">這結合了撰寫 DLL 伺服器的便利性與可執行檔的優點。</span><span class="sxs-lookup"><span data-stu-id="8a3d1-105">This combines the ease of writing DLL servers with the benefits of executable implementation.</span></span> <span data-ttu-id="8a3d1-106">Microsoft Visual Studio 等開發工具有助於撰寫 DLL 伺服器，但是 DLL 伺服器本身也有限制。</span><span class="sxs-lookup"><span data-stu-id="8a3d1-106">Development tools like Microsoft Visual Studio facilitate the writing of DLL servers, but a DLL server in itself has limits.</span></span> <span data-ttu-id="8a3d1-107">在代理程式中執行 DLL 伺服器可提供數個可能的優點：</span><span class="sxs-lookup"><span data-stu-id="8a3d1-107">Running the DLL server in a surrogate process offers several possible benefits:</span></span>

-   <span data-ttu-id="8a3d1-108">錯誤隔離和同時服務多個用戶端的能力。</span><span class="sxs-lookup"><span data-stu-id="8a3d1-108">Fault isolation and the ability to service multiple clients simultaneously.</span></span>
-   <span data-ttu-id="8a3d1-109">在分散式環境中，可以使用 DLL 伺服器執行來服務遠端用戶端。</span><span class="sxs-lookup"><span data-stu-id="8a3d1-109">In a distributed environment, a DLL server implementation could be used to service remote clients.</span></span>
-   <span data-ttu-id="8a3d1-110">它可以允許用戶端保護自己免于受信任的伺服器程式碼，同時讓他們能夠存取 DLL 伺服器所提供的服務。</span><span class="sxs-lookup"><span data-stu-id="8a3d1-110">It could permit clients to help protect themselves from untrusted server code while allowing them access to the services the DLL server provides.</span></span>
-   <span data-ttu-id="8a3d1-111">在代理中執行 DLL 伺服器會提供具有代理程式安全性的 DLL。</span><span class="sxs-lookup"><span data-stu-id="8a3d1-111">Running a DLL server in a surrogate provides the DLL with the surrogate's security.</span></span>

<span data-ttu-id="8a3d1-112">COM 提供預設的代理程式，或者如果您有特殊需求，則可以撰寫自訂的代理。</span><span class="sxs-lookup"><span data-stu-id="8a3d1-112">COM provides a default surrogate process, or you can write a custom surrogate if you have special needs.</span></span>

<span data-ttu-id="8a3d1-113">下列主題提供 DLL 代理連結的詳細資訊：</span><span class="sxs-lookup"><span data-stu-id="8a3d1-113">The following topics provide more information on DLL surrogates:</span></span>

-   [<span data-ttu-id="8a3d1-114">DLL 伺服器需求</span><span class="sxs-lookup"><span data-stu-id="8a3d1-114">DLL Server Requirements</span></span>](dll-server-requirements.md)
-   [<span data-ttu-id="8a3d1-115">使用 System-Supplied 代理</span><span class="sxs-lookup"><span data-stu-id="8a3d1-115">Using the System-Supplied Surrogate</span></span>](using-the-system-supplied-surrogate.md)
-   [<span data-ttu-id="8a3d1-116">撰寫自訂代理</span><span class="sxs-lookup"><span data-stu-id="8a3d1-116">Writing a Custom Surrogate</span></span>](writing-a-custom-surrogate.md)

 

 




