---
description: 網際網路通訊協定協助程式 (IP 協助程式) API 可讓您對本機電腦的網路設定進行抓取和修改。
ms.assetid: 4896a9f8-0486-4380-bf49-d1c9ef114acc
title: IP 協助程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1d50153e1ad890063f33a473058f6a850a9f171
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847955"
---
# <a name="ip-helper"></a><span data-ttu-id="b29db-103">IP 協助程式</span><span class="sxs-lookup"><span data-stu-id="b29db-103">IP Helper</span></span>

## <a name="purpose"></a><span data-ttu-id="b29db-104">目的</span><span class="sxs-lookup"><span data-stu-id="b29db-104">Purpose</span></span>

<span data-ttu-id="b29db-105">網際網路通訊協定協助程式 (IP 協助程式) API 可讓您對本機電腦的網路設定進行抓取和修改。</span><span class="sxs-lookup"><span data-stu-id="b29db-105">The Internet Protocol Helper (IP Helper) API enables the retrieval and modification of network configuration settings for the local computer.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="b29db-106">適用時</span><span class="sxs-lookup"><span data-stu-id="b29db-106">Where applicable</span></span>

<span data-ttu-id="b29db-107">IP 協助程式 API 適用于任何以程式設計方式操作網路和 TCP/IP 設定的計算環境。</span><span class="sxs-lookup"><span data-stu-id="b29db-107">The IP Helper API is applicable in any computing environment where programmatically manipulating network and TCP/IP configuration is useful.</span></span> <span data-ttu-id="b29db-108">一般的應用程式包括 IP 路由通訊協定，以及簡單的網路管理通訊協定 (SNMP) 代理程式。</span><span class="sxs-lookup"><span data-stu-id="b29db-108">Typical applications include IP routing protocols and Simple Network Management Protocol (SNMP) agents.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="b29db-109">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="b29db-109">Developer audience</span></span>

<span data-ttu-id="b29db-110">IP Helper API 是設計來供 C/c + + 程式設計人員使用。</span><span class="sxs-lookup"><span data-stu-id="b29db-110">The IP Helper API is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="b29db-111">程式設計人員也應該熟悉 Windows 網路和 TCP/IP 網路概念。</span><span class="sxs-lookup"><span data-stu-id="b29db-111">Programmers should also be familiar with Windows networking and TCP/IP networking concepts.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="b29db-112">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="b29db-112">Run-time requirements</span></span>

<span data-ttu-id="b29db-113">IP 協助程式 API 可在所有 Windows 平臺上使用。</span><span class="sxs-lookup"><span data-stu-id="b29db-113">The IP Helper API can be used on all Windows platforms.</span></span> <span data-ttu-id="b29db-114">並非所有的作業系統都支援所有功能。</span><span class="sxs-lookup"><span data-stu-id="b29db-114">Not all operating systems support all functions.</span></span> <span data-ttu-id="b29db-115">當 Windows 通訊端2平臺限制的特定執行或功能存在時，就會在檔中清楚注明它們。</span><span class="sxs-lookup"><span data-stu-id="b29db-115">Where certain implementations or capabilities of Windows Sockets 2 platform restrictions do exist, they are clearly noted in the documentation.</span></span> <span data-ttu-id="b29db-116">如果在不支援函數的平臺上呼叫 IP Helper 函式， \_ \_ 則會傳回不支援的錯誤。</span><span class="sxs-lookup"><span data-stu-id="b29db-116">If an IP Helper function is called on a platform that does not support the function, ERROR\_NOT\_SUPPORTED is returned.</span></span> <span data-ttu-id="b29db-117">如需有關哪些作業系統支援特定功能的詳細資訊，請參閱檔中的需求一節。</span><span class="sxs-lookup"><span data-stu-id="b29db-117">For more specific information about which operating systems support a particular function, refer to the Requirements sections in the documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b29db-118">本節內容</span><span class="sxs-lookup"><span data-stu-id="b29db-118">In this section</span></span>



| <span data-ttu-id="b29db-119">主題</span><span class="sxs-lookup"><span data-stu-id="b29db-119">Topic</span></span>                                                              | <span data-ttu-id="b29db-120">描述</span><span class="sxs-lookup"><span data-stu-id="b29db-120">Description</span></span>                                                                                                                                                                                                       |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b29db-121">IP Helper 的新功能</span><span class="sxs-lookup"><span data-stu-id="b29db-121">What's New in IP Helper</span></span>](what-s-new-in-ip-helper.md)<br/>  | <span data-ttu-id="b29db-122">IP Helper 的新功能相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b29db-122">Information on new features for IP Helper.</span></span><br/>                                                                                                                                                             |
| [<span data-ttu-id="b29db-123">關於 IP Helper</span><span class="sxs-lookup"><span data-stu-id="b29db-123">About IP Helper</span></span>](about-ip-helper.md)<br/>                  | <span data-ttu-id="b29db-124">適用于開發人員的 IP 協助程式程式設計考慮和功能的一般資訊。</span><span class="sxs-lookup"><span data-stu-id="b29db-124">General information about IP Helper programming considerations and capabilities available to developers.</span></span><br/>                                                                                               |
| [<span data-ttu-id="b29db-125">使用 IP Helper</span><span class="sxs-lookup"><span data-stu-id="b29db-125">Using IP Helper</span></span>](using-ip-helper.md)<br/>                  | <span data-ttu-id="b29db-126">搭配 IP Helper 使用的程式和程式設計技術。</span><span class="sxs-lookup"><span data-stu-id="b29db-126">Procedures and programming techniques used with IP Helper.</span></span> <span data-ttu-id="b29db-127">本節包含基本 IP 協助程式程式設計技術，例如 [開始使用與 ip 協助程式的關聯](getting-started-with-ip-helper.md)。</span><span class="sxs-lookup"><span data-stu-id="b29db-127">This section includes basic IP Helper programming techniques, such as [Getting Started With IP Helper](getting-started-with-ip-helper.md).</span></span><br/> |
| [<span data-ttu-id="b29db-128">IP 協助程式參考</span><span class="sxs-lookup"><span data-stu-id="b29db-128">IP Helper reference</span></span>](ip-helper-function-reference.md)<br/> | <span data-ttu-id="b29db-129">IP Helper 函數、結構和列舉的參考檔。</span><span class="sxs-lookup"><span data-stu-id="b29db-129">Reference documentation for the IP Helper functions, structures, and enumerations.</span></span><br/>                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="b29db-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="b29db-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b29db-131">Windows 通訊端2</span><span class="sxs-lookup"><span data-stu-id="b29db-131">Windows Sockets 2</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[<span data-ttu-id="b29db-132">路由及遠端存取服務</span><span class="sxs-lookup"><span data-stu-id="b29db-132">Routing and Remote Access Service</span></span>](../rras/routing-start-page.md)
</dt> </dl>

 

