---
title: Microsoft RPC
description: Microsoft RPC
ms.assetid: a9ca629a-2766-43d5-89da-73d0628b3c5e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53be9d46368ae01aee25815327aafeaf7f44525b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671035"
---
# <a name="microsoft-rpc"></a><span data-ttu-id="403a0-103">Microsoft RPC</span><span class="sxs-lookup"><span data-stu-id="403a0-103">Microsoft RPC</span></span>

<span data-ttu-id="403a0-104">Microsoft RPC 是在分散式運算環境中進行程式設計的模型。</span><span class="sxs-lookup"><span data-stu-id="403a0-104">Microsoft RPC is a model for programming in a distributed computing environment.</span></span> <span data-ttu-id="403a0-105">RPC 的目標是要提供透明通訊，讓用戶端看起來與伺服器直接通訊。</span><span class="sxs-lookup"><span data-stu-id="403a0-105">The goal of RPC is to provide transparent communication so that the client appears to be directly communicating with the server.</span></span> <span data-ttu-id="403a0-106">Microsoft 的 RPC 執行與開放式 Software Foundation (憑證) 分散式運算環境 (DCE) RPC 相容。</span><span class="sxs-lookup"><span data-stu-id="403a0-106">Microsoft's implementation of RPC is compatible with the Open Software Foundation (OSF) Distributed Computing Environment (DCE) RPC.</span></span>

<span data-ttu-id="403a0-107">您可以設定 RPC 使用一或多個傳輸、一或多個名稱服務，以及一或多個安全性伺服器。</span><span class="sxs-lookup"><span data-stu-id="403a0-107">You can configure RPC to use one or more transports, one or more name services, and one or more security servers.</span></span> <span data-ttu-id="403a0-108">這些提供者的介面是由 RPC 處理。</span><span class="sxs-lookup"><span data-stu-id="403a0-108">The interfaces to those providers are handled by RPC.</span></span> <span data-ttu-id="403a0-109">由於 Microsoft RPC 是設計來與多個提供者搭配使用，因此您可以選擇最適合您網路的提供者。</span><span class="sxs-lookup"><span data-stu-id="403a0-109">Because Microsoft RPC is designed to work with multiple providers, you can choose the providers that work best for your network.</span></span> <span data-ttu-id="403a0-110">傳輸會負責在網路上傳輸資料。</span><span class="sxs-lookup"><span data-stu-id="403a0-110">The transport is responsible for transmitting the data across the network.</span></span> <span data-ttu-id="403a0-111">名稱服務會接受物件名稱（例如，標記），並在網路上尋找其位置。</span><span class="sxs-lookup"><span data-stu-id="403a0-111">The name service takes an object name, such as a moniker, and finds its location on the network.</span></span> <span data-ttu-id="403a0-112">安全性伺服器提供應用程式拒絕存取特定使用者及/或群組的選項。</span><span class="sxs-lookup"><span data-stu-id="403a0-112">The security server offers applications the option of denying access to specific users and/or groups.</span></span> <span data-ttu-id="403a0-113">如需應用程式安全性的詳細資訊，請參閱 [介面設計規則](interface-design-rules.md) 。</span><span class="sxs-lookup"><span data-stu-id="403a0-113">See [Interface Design Rules](interface-design-rules.md) for more detailed information about application security.</span></span>

<span data-ttu-id="403a0-114">除了 RPC 執行時間程式庫，Microsoft RPC 還包含介面定義語言 (IDL) 及其編譯器。</span><span class="sxs-lookup"><span data-stu-id="403a0-114">In addition to the RPC run-time libraries, Microsoft RPC includes the Interface Definition Language (IDL) and its compiler.</span></span> <span data-ttu-id="403a0-115">雖然 IDL 檔案是 RPC 的標準元件，但 Microsoft 已增強它以擴充其功能，以支援自訂 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="403a0-115">Although the IDL file is a standard part of RPC, Microsoft has enhanced it to extend its functionality to support custom COM interfaces.</span></span> <span data-ttu-id="403a0-116">Microsoft 介面定義語言 (MIDL) 編譯器使用 IDL 檔案來描述您的自訂介面，以產生 [建立和註冊 PROXY DLL](building-and-registering-a-proxy-dll.md)中所討論的數個檔案。</span><span class="sxs-lookup"><span data-stu-id="403a0-116">The Microsoft Interface Definition Language (MIDL) compiler uses the IDL file that describes your custom interface to generate several files discussed in [Building and Registering a Proxy DLL](building-and-registering-a-proxy-dll.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="403a0-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="403a0-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="403a0-118">通道</span><span class="sxs-lookup"><span data-stu-id="403a0-118">Channel</span></span>](channel.md)
</dt> <dt>

[<span data-ttu-id="403a0-119">物件間通訊</span><span class="sxs-lookup"><span data-stu-id="403a0-119">Inter-Object Communication</span></span>](inter-object-communication.md)
</dt> <dt>

[<span data-ttu-id="403a0-120">封送處理詳細資料</span><span class="sxs-lookup"><span data-stu-id="403a0-120">Marshaling Details</span></span>](marshaling-details.md)
</dt> <dt>

[<span data-ttu-id="403a0-121">Proxy</span><span class="sxs-lookup"><span data-stu-id="403a0-121">Proxy</span></span>](proxy.md)
</dt> <dt>

[<span data-ttu-id="403a0-122">存根</span><span class="sxs-lookup"><span data-stu-id="403a0-122">Stub</span></span>](stub.md)
</dt> </dl>

 

 




