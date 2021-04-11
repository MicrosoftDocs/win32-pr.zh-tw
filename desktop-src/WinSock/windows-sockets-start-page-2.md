---
description: Windows 通訊端 2 (Winsock) 可讓程式設計人員建立先進的網際網路、內部網路和其他具備網路功能的應用程式，以在網路上傳輸應用程式資料，而不受使用的網路通訊協定影響。
ms.assetid: 1ec8758a-40fd-4c98-b839-c2409ef712d6
title: Windows 通訊端2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df253572d2fca117dbc8b45b451f8c3bacc2f360
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114293"
---
# <a name="windows-sockets-2"></a><span data-ttu-id="63d14-103">Windows 通訊端2</span><span class="sxs-lookup"><span data-stu-id="63d14-103">Windows Sockets 2</span></span>

## <a name="purpose"></a><span data-ttu-id="63d14-104">目的</span><span class="sxs-lookup"><span data-stu-id="63d14-104">Purpose</span></span>

<span data-ttu-id="63d14-105">Windows 通訊端 2 (Winsock) 可讓程式設計人員建立先進的網際網路、內部網路和其他具備網路功能的應用程式，以在網路上傳輸應用程式資料，而不受使用的網路通訊協定影響。</span><span class="sxs-lookup"><span data-stu-id="63d14-105">Windows Sockets 2 (Winsock) enables programmers to create advanced Internet, intranet, and other network-capable applications to transmit application data across the wire, independent of the network protocol being used.</span></span> <span data-ttu-id="63d14-106">有了 Winsock，程式設計人員就可以存取 advanced Microsoft® Windows®的網路功能，例如多播和服務品質 (QoS) 。</span><span class="sxs-lookup"><span data-stu-id="63d14-106">With Winsock, programmers are provided access to advanced Microsoft® Windows® networking capabilities such as multicast and Quality of Service (QoS).</span></span>

<span data-ttu-id="63d14-107">Winsock 遵循 Windows Open System 架構 (WOSA) 模型;它會定義應用程式開發介面 (API) 之間的標準服務提供者介面 (SPI) ，以及其匯出的函式和通訊協定堆疊。</span><span class="sxs-lookup"><span data-stu-id="63d14-107">Winsock follows the Windows Open System Architecture (WOSA) model; it defines a standard service provider interface (SPI) between the application programming interface (API), with its exported functions and the protocol stacks.</span></span> <span data-ttu-id="63d14-108">它會使用第一次由 Berkeley Software 散發 (BSD) UNIX 所普及化的通訊端範例。</span><span class="sxs-lookup"><span data-stu-id="63d14-108">It uses the sockets paradigm that was first popularized by Berkeley Software Distribution (BSD) UNIX.</span></span> <span data-ttu-id="63d14-109">它稍後是針對 windows 通訊端1.1 中的 Windows 進行調整，Windows 通訊端2應用程式可回溯相容。</span><span class="sxs-lookup"><span data-stu-id="63d14-109">It was later adapted for Windows in Windows Sockets 1.1, with which Windows Sockets 2 applications are backward compatible.</span></span> <span data-ttu-id="63d14-110">Winsock 程式設計之前是以 TCP/IP 為中心。</span><span class="sxs-lookup"><span data-stu-id="63d14-110">Winsock programming previously centered around TCP/IP.</span></span> <span data-ttu-id="63d14-111">某些搭配 TCP/IP 使用的程式設計實務無法用於每個通訊協定。</span><span class="sxs-lookup"><span data-stu-id="63d14-111">Some programming practices that worked with TCP/IP do not work with every protocol.</span></span> <span data-ttu-id="63d14-112">因此，Windows 通訊端 2 API 會在需要處理數個通訊協定的情況下新增函式。</span><span class="sxs-lookup"><span data-stu-id="63d14-112">As a result, the Windows Sockets 2 API adds functions where necessary to handle several protocols.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="63d14-113">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="63d14-113">Developer audience</span></span>

<span data-ttu-id="63d14-114">Windows 通訊端2是設計來供 C/c + + 程式設計人員使用。</span><span class="sxs-lookup"><span data-stu-id="63d14-114">Windows Sockets 2 is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="63d14-115">需要熟悉 Windows 網路功能。</span><span class="sxs-lookup"><span data-stu-id="63d14-115">Familiarity with Windows networking is required.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="63d14-116">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="63d14-116">Run-time requirements</span></span>

<span data-ttu-id="63d14-117">Windows 通訊端2可以在所有 Windows 平臺上使用。</span><span class="sxs-lookup"><span data-stu-id="63d14-117">Windows Sockets 2 can be used on all Windows platforms.</span></span> <span data-ttu-id="63d14-118">當 Windows 通訊端2平臺限制的特定執行或功能存在時，就會在檔中清楚注明它們。</span><span class="sxs-lookup"><span data-stu-id="63d14-118">Where certain implementations or capabilities of Windows Sockets 2 platform restrictions do exist, they are clearly noted in the documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="63d14-119">本節內容</span><span class="sxs-lookup"><span data-stu-id="63d14-119">In this section</span></span>



| <span data-ttu-id="63d14-120">主題</span><span class="sxs-lookup"><span data-stu-id="63d14-120">Topic</span></span>                                                                                             | <span data-ttu-id="63d14-121">描述</span><span class="sxs-lookup"><span data-stu-id="63d14-121">Description</span></span>                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="63d14-122">Windows 通訊端的新功能</span><span class="sxs-lookup"><span data-stu-id="63d14-122">What's New for Windows Sockets</span></span>](what-s-new-for-windows-sockets-2.md)<br/>                 | <span data-ttu-id="63d14-123">Windows 通訊端新功能的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="63d14-123">Information on new features for Windows Sockets.</span></span><br/>                                                                                                                                                                                                                                 |
| [<span data-ttu-id="63d14-124">Windows 中的 Winsock 網路通訊協定支援</span><span class="sxs-lookup"><span data-stu-id="63d14-124">Winsock Network Protocol Support in Windows</span></span>](network-protocol-support-in-windows.md)<br/> | <span data-ttu-id="63d14-125">不同 Windows 通訊端在不同版本的 Windows 上的網路通訊協定支援的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="63d14-125">Information on network protocol support for Windows Sockets on different versions of Windows.</span></span><br/>                                                                                                                                                                                    |
| [<span data-ttu-id="63d14-126">關於 Winsock</span><span class="sxs-lookup"><span data-stu-id="63d14-126">About Winsock</span></span>](about-winsock.md)<br/>                                                     | <span data-ttu-id="63d14-127">適用于開發人員的 Windows 通訊端程式設計考慮、架構和功能的一般資訊。</span><span class="sxs-lookup"><span data-stu-id="63d14-127">General information on Windows Sockets programming considerations, architecture, and capabilities available to developers.</span></span><br/>                                                                                                                                                       |
| [<span data-ttu-id="63d14-128">使用 Winsock</span><span class="sxs-lookup"><span data-stu-id="63d14-128">Using Winsock</span></span>](using-winsock.md)<br/>                                                     | <span data-ttu-id="63d14-129">搭配 Windows 通訊端使用的程式和程式設計技術。</span><span class="sxs-lookup"><span data-stu-id="63d14-129">Procedures and programming techniques used with Windows Sockets.</span></span> <span data-ttu-id="63d14-130">本節包含基本的 Winsock 程式設計技術，例如 [使用 winsock 開始使用](getting-started-with-winsock.md)，以及適用于有經驗的 winsock 開發人員的先進技術。</span><span class="sxs-lookup"><span data-stu-id="63d14-130">This section includes basic Winsock programming techniques, such as [Getting Started With Winsock](getting-started-with-winsock.md), as well as advanced techniques useful for experienced Winsock developers.</span></span><br/> |
| [<span data-ttu-id="63d14-131">Winsock 參考</span><span class="sxs-lookup"><span data-stu-id="63d14-131">Winsock Reference</span></span>](winsock-reference.md)<br/>                                             | <span data-ttu-id="63d14-132">Windows 通訊端 API 的檔。</span><span class="sxs-lookup"><span data-stu-id="63d14-132">Documentation of the Windows Sockets API.</span></span><br/>                                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="63d14-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="63d14-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63d14-134">IP 協助程式</span><span class="sxs-lookup"><span data-stu-id="63d14-134">IP Helper</span></span>](../iphlp/ip-helper-start-page.md)
</dt> <dt>

[<span data-ttu-id="63d14-135">服務品質</span><span class="sxs-lookup"><span data-stu-id="63d14-135">Quality of Service</span></span>](/previous-versions/windows/desktop/qos/qos-start-page)
</dt> </dl>

 

 
