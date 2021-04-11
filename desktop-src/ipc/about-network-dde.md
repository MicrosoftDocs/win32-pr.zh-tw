---
description: 網路 DDE 可用來在網路中不同電腦上執行的應用程式之間，起始和維護 DDE 交談所需的網路連線。
ms.assetid: f9eee391-2b4a-4c17-bea5-72cda5124e1c
title: 關於網路 DDE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 412971f6bef8d2782dce38b5aef413e4d073f6b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319011"
---
# <a name="about-network-dde"></a><span data-ttu-id="d8014-103">關於網路 DDE</span><span class="sxs-lookup"><span data-stu-id="d8014-103">About Network DDE</span></span>

<span data-ttu-id="d8014-104">\[不再支援網路 DDE。</span><span class="sxs-lookup"><span data-stu-id="d8014-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="d8014-105">Windows Vista 上有 Nddeapi.dll，但是所有的函式呼叫都會傳回 NDDE \_ 未 \_ 執行。\]</span><span class="sxs-lookup"><span data-stu-id="d8014-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="d8014-106">網路 DDE 可用來在網路中不同電腦上執行的應用程式之間，起始和維護 DDE 交談所需的網路連線。</span><span class="sxs-lookup"><span data-stu-id="d8014-106">Network DDE is used to initiate and maintain the network connections needed for DDE conversations between applications running on different computers in a network.</span></span> <span data-ttu-id="d8014-107">DDE *對話* 是用戶端與伺服器應用程式之間的互動。</span><span class="sxs-lookup"><span data-stu-id="d8014-107">A DDE *conversation* is the interaction between client and server applications.</span></span> <span data-ttu-id="d8014-108">您可以在應用程式中使用網路 DDE 搭配 DDE 和 DDE 管理程式庫 (DDEML) 。</span><span class="sxs-lookup"><span data-stu-id="d8014-108">You use network DDE along with DDE and the DDE management library (DDEML) in your application.</span></span>

<span data-ttu-id="d8014-109">DDE 是一種處理序間通訊形式，使用共用記憶體來交換應用程式之間的資料。</span><span class="sxs-lookup"><span data-stu-id="d8014-109">DDE is a form of interprocess communication that uses shared memory to exchange data between applications.</span></span> <span data-ttu-id="d8014-110">應用程式可以使用 DDE 進行一次資料傳輸，或是進行中的交換和更新資料。</span><span class="sxs-lookup"><span data-stu-id="d8014-110">Applications can use DDE for one time data transfers or for ongoing exchanges and updating data.</span></span> <span data-ttu-id="d8014-111">如需有關 DDE 的詳細資訊，請參閱 [動態資料交換](../dataxchg/dynamic-data-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="d8014-111">For more information on DDE, see [Dynamic Data Exchange](../dataxchg/dynamic-data-exchange.md).</span></span>

<span data-ttu-id="d8014-112">DDEML 可簡化將 DDE 功能新增至應用程式的工作。</span><span class="sxs-lookup"><span data-stu-id="d8014-112">DDEML simplifies the task of adding DDE capability to an application.</span></span> <span data-ttu-id="d8014-113">應用程式會使用 DDEML 所提供的函式來管理 DDE 交談，而不是直接傳送、張貼和處理 DDE 訊息。</span><span class="sxs-lookup"><span data-stu-id="d8014-113">Instead of sending, posting, and processing DDE messages directly, an application uses the functions provided by the DDEML to manage DDE conversations.</span></span> <span data-ttu-id="d8014-114">如需 DDEML 的詳細資訊，請參閱 [動態資料交換管理程式庫](../dataxchg/dynamic-data-exchange-management-library.md)。</span><span class="sxs-lookup"><span data-stu-id="d8014-114">For more information on DDEML, see [Dynamic Data Exchange Management Library](../dataxchg/dynamic-data-exchange-management-library.md).</span></span>

## <a name="network-dde-files"></a><span data-ttu-id="d8014-115">網路 DDE 檔案</span><span class="sxs-lookup"><span data-stu-id="d8014-115">Network DDE Files</span></span>

<span data-ttu-id="d8014-116">若要使用網路 DDE 的 API 元素，您必須在原始程式檔中包含 NDDEApi 標頭檔，並在連結行上包含 NDDEApi .lib 檔案。</span><span class="sxs-lookup"><span data-stu-id="d8014-116">To use the API elements of network DDE, you must include the NDDEApi.h header file in your source files and include NDDEApi.lib file on your link line.</span></span> <span data-ttu-id="d8014-117">您也必須確認已載入 NDDEApi.dll 的檔案。</span><span class="sxs-lookup"><span data-stu-id="d8014-117">You must also make sure that the NDDEApi.dll file is loaded.</span></span>

<span data-ttu-id="d8014-118">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="d8014-118">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="d8014-119">網路 DDE 代理程式</span><span class="sxs-lookup"><span data-stu-id="d8014-119">Network DDE Agent</span></span>](network-dde-agent.md)
-   [<span data-ttu-id="d8014-120">DDE 共用</span><span class="sxs-lookup"><span data-stu-id="d8014-120">DDE Shares</span></span>](dde-shares.md)
-   [<span data-ttu-id="d8014-121">受信任的共用和安全性</span><span class="sxs-lookup"><span data-stu-id="d8014-121">Trusted Shares and Security</span></span>](trusted-shares-and-security.md)
-   [<span data-ttu-id="d8014-122">管理 DDE 共用</span><span class="sxs-lookup"><span data-stu-id="d8014-122">Managing DDE Shares</span></span>](managing-dde-shares.md)

 

 
