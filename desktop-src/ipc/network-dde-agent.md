---
description: 如果網路 dde 代理程式偵測到區域網路 DDE 活動，則會啟動網路 dde。
ms.assetid: bc1e6a06-be07-4ae8-94da-9603a885b3a5
title: 網路 DDE 代理程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87a6259b512782102936f54f65646454509c6b37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107001658"
---
# <a name="network-dde-agent"></a><span data-ttu-id="a25d4-103">網路 DDE 代理程式</span><span class="sxs-lookup"><span data-stu-id="a25d4-103">Network DDE Agent</span></span>

<span data-ttu-id="a25d4-104">\[不再支援網路 DDE。</span><span class="sxs-lookup"><span data-stu-id="a25d4-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="a25d4-105">Windows Vista 上有 Nddeapi.dll，但是所有的函式呼叫都會傳回 NDDE \_ 未 \_ 執行。\]</span><span class="sxs-lookup"><span data-stu-id="a25d4-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="a25d4-106">如果網路 dde 代理程式偵測到區域網路 DDE 活動，則會啟動網路 dde。</span><span class="sxs-lookup"><span data-stu-id="a25d4-106">The network DDE agent starts network DDE if it detects local network DDE activity.</span></span> <span data-ttu-id="a25d4-107">它不會偵測到嘗試連接的遠端用戶端。</span><span class="sxs-lookup"><span data-stu-id="a25d4-107">It does not detect a remote client trying to connect.</span></span> <span data-ttu-id="a25d4-108">因此，在任何用戶端可以成功連接之前，必須先在伺服器電腦上啟動網路 DDE。</span><span class="sxs-lookup"><span data-stu-id="a25d4-108">Therefore, before any client can successfully connect, network DDE must be started on the server computer.</span></span> <span data-ttu-id="a25d4-109">請注意，網路 DDE 預設並不會啟動。</span><span class="sxs-lookup"><span data-stu-id="a25d4-109">Note that network DDE is not started by default.</span></span> <span data-ttu-id="a25d4-110">若要啟動網路 DDE，請執行 NETDDE.EXE。</span><span class="sxs-lookup"><span data-stu-id="a25d4-110">To start network DDE, run NETDDE.EXE.</span></span> <span data-ttu-id="a25d4-111">這個檔案位於您的 Windows 目錄中。</span><span class="sxs-lookup"><span data-stu-id="a25d4-111">This file is located in your Windows directory.</span></span>

<span data-ttu-id="a25d4-112">網路 DDE 代理程式也會啟動網路 DDE 所需的應用程式。</span><span class="sxs-lookup"><span data-stu-id="a25d4-112">The network DDE agent also starts the applications necessary for network DDE.</span></span> <span data-ttu-id="a25d4-113">在網路 DDE 啟動之後，DDE 交談是透過與其中一個網路 DDE 應用程式相關聯的網路 DDE 視窗來控制。</span><span class="sxs-lookup"><span data-stu-id="a25d4-113">After network DDE is started, DDE conversations are controlled through a network DDE window associated with one of the network DDE applications.</span></span> <span data-ttu-id="a25d4-114">此應用程式會作為 proxy。</span><span class="sxs-lookup"><span data-stu-id="a25d4-114">This application acts as a proxy.</span></span> <span data-ttu-id="a25d4-115">它會與所有本機和遠端 DDE 應用程式進行通訊。</span><span class="sxs-lookup"><span data-stu-id="a25d4-115">It communicates with all local and remote DDE applications.</span></span>

 

 



