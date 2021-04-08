---
title: 基本 RPC 系結術語
description: 為了進一步協助用戶端/伺服器連接程式的討論，瞭解下列詞彙會很有説明。
ms.assetid: 05aca325-87ee-4581-9152-a8a2ff7fb490
keywords:
- 遠端程序呼叫 RPC、描述、系結
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b18b8d3872c830d90079ad740505fead14c1b3c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023926"
---
# <a name="essential-rpc-binding-terminology"></a><span data-ttu-id="60503-104">基本 RPC 系結術語</span><span class="sxs-lookup"><span data-stu-id="60503-104">Essential RPC Binding Terminology</span></span>

<span data-ttu-id="60503-105">為了進一步協助用戶端/伺服器連接程式的討論，瞭解下列詞彙會很有説明。</span><span class="sxs-lookup"><span data-stu-id="60503-105">To better aid in a discussion of the client/server connection process, it is helpful to know the following terms.</span></span>

## <a name="parameters"></a><span data-ttu-id="60503-106">參數</span><span class="sxs-lookup"><span data-stu-id="60503-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60503-107"><span id="Protocol_Sequence"></span><span id="protocol_sequence"></span><span id="PROTOCOL_SEQUENCE"></span>通訊協定順序</span><span class="sxs-lookup"><span data-stu-id="60503-107"><span id="Protocol_Sequence"></span><span id="protocol_sequence"></span><span id="PROTOCOL_SEQUENCE"></span>Protocol Sequence</span></span>
</dt> <dd>

<span data-ttu-id="60503-108">當網路作業系統彼此通訊時，他們必須接聽並說出相同的語言。</span><span class="sxs-lookup"><span data-stu-id="60503-108">When network operating systems communicate with each other, they must listen and speak the same language.</span></span> <span data-ttu-id="60503-109">這些語言稱為 *通訊協定順序*。</span><span class="sxs-lookup"><span data-stu-id="60503-109">These languages are called *protocol sequences*.</span></span> <span data-ttu-id="60503-110">用戶端和伺服器程式必須使用連接它們所支援之網路的通訊協定順序。</span><span class="sxs-lookup"><span data-stu-id="60503-110">Client and server programs must use protocol sequences that the network connecting them supports.</span></span> <span data-ttu-id="60503-111">Microsoft RPC 支援各種不同的通訊協定順序。</span><span class="sxs-lookup"><span data-stu-id="60503-111">Microsoft RPC supports a variety of protocol sequences.</span></span> <span data-ttu-id="60503-112">如需詳細資訊，請參閱 [選取通訊協定順序](selecting-a-protocol-sequence.md)， [指定通訊協定](specifying-protocol-sequences.md)順序和 [**端點**](/windows/desktop/Midl/endpoint)。</span><span class="sxs-lookup"><span data-stu-id="60503-112">For details, see [Selecting a Protocol Sequence](selecting-a-protocol-sequence.md), [Specifying Protocol Sequences](specifying-protocol-sequences.md), and [**endpoint**](/windows/desktop/Midl/endpoint).</span></span>

</dd> <dt>

<span data-ttu-id="60503-113"><span id="Server_Host_Computer_or_Server_Host_System"></span><span id="server_host_computer_or_server_host_system"></span><span id="SERVER_HOST_COMPUTER_OR_SERVER_HOST_SYSTEM"></span>伺服器主機電腦或伺服器主機系統</span><span class="sxs-lookup"><span data-stu-id="60503-113"><span id="Server_Host_Computer_or_Server_Host_System"></span><span id="server_host_computer_or_server_host_system"></span><span id="SERVER_HOST_COMPUTER_OR_SERVER_HOST_SYSTEM"></span>Server Host Computer or Server Host System</span></span>
</dt> <dd>

<span data-ttu-id="60503-114">伺服器程式會在伺服器主機電腦上執行。</span><span class="sxs-lookup"><span data-stu-id="60503-114">The server program runs on the server host computer.</span></span> <span data-ttu-id="60503-115">不過，用戶端/伺服器運算的許多文獻都指的是伺服器程式和伺服器主機電腦做為「伺服器」。</span><span class="sxs-lookup"><span data-stu-id="60503-115">However, much literature on client/server computing refers to both the server program and the server host computer as the "server."</span></span> <span data-ttu-id="60503-116">結果就是，它不一定是很清楚的討論。</span><span class="sxs-lookup"><span data-stu-id="60503-116">The result is that it is not always clear which is being discussed.</span></span>

</dd> <dt>

<span data-ttu-id="60503-117"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>端點</span><span class="sxs-lookup"><span data-stu-id="60503-117"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span>
</dt> <dd>

<span data-ttu-id="60503-118">伺服器程式會接聽伺服器主機電腦上的埠或通訊埠群組，以取得用戶端要求。</span><span class="sxs-lookup"><span data-stu-id="60503-118">Server programs listen to a port or a group of ports on the server host computer for client requests.</span></span> <span data-ttu-id="60503-119">伺服器主機系統會維護這些埠的資料庫，這些埠稱為 RPC 中的端點。</span><span class="sxs-lookup"><span data-stu-id="60503-119">Server host systems maintain a database of these ports, which are called endpoints in RPC.</span></span> <span data-ttu-id="60503-120">資料庫稱為端點對應。</span><span class="sxs-lookup"><span data-stu-id="60503-120">The database is called the endpoint map.</span></span>

</dd> <dt>

<span data-ttu-id="60503-121"><span id="Binding"></span><span id="binding"></span><span id="BINDING"></span>綁定</span><span class="sxs-lookup"><span data-stu-id="60503-121"><span id="Binding"></span><span id="binding"></span><span id="BINDING"></span>Binding</span></span>
</dt> <dd>

<span data-ttu-id="60503-122">用戶端程式會建立伺服器的系結，以建立通訊會話。</span><span class="sxs-lookup"><span data-stu-id="60503-122">Client programs create a binding to the server to establish a communication session.</span></span> <span data-ttu-id="60503-123">系結包含用戶端應用程式建立會話所需的所有資訊。</span><span class="sxs-lookup"><span data-stu-id="60503-123">A binding contains all of the information the client applications needs to create the session.</span></span>

</dd> </dl>

 

 