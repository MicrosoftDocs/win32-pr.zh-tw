---
title: 執行網路功能
description: 執行網路功能
ms.assetid: 908e269b-63be-4666-a364-a894f6dcd86f
keywords:
- Windows Media Format SDK，執行網路功能
- Windows Media Format SDK，網路功能
- 先進的系統格式 (ASF) ，執行網路功能
- ASF (Advanced Systems Format) ，執行網路功能
- Advanced Systems Format (ASF) ，網路功能
- ASF (Advanced Systems Format) ，網路功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e631b6a322293bffe71ce92afcb684901cc60d16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507384"
---
# <a name="implementing-network-functionality"></a><span data-ttu-id="8e2fa-109">執行網路功能</span><span class="sxs-lookup"><span data-stu-id="8e2fa-109">Implementing Network Functionality</span></span>

<span data-ttu-id="8e2fa-110">本節說明如何使用可透過 Windows Media Format SDK 取得的網路功能。</span><span class="sxs-lookup"><span data-stu-id="8e2fa-110">This section describes how to use the networking features available through the Windows Media Format SDK.</span></span> <span data-ttu-id="8e2fa-111">應用程式可以使用這些功能，從網路讀取 ASF 串流、將 ASF 串流廣播到網路，或將 ASF 串流推送至執行 Windows Media Services 之伺服器上的發行端點。</span><span class="sxs-lookup"><span data-stu-id="8e2fa-111">An application can use these features to read ASF streams from a network, broadcast ASF streams to a network, or push ASF streams to a publishing point on a server running Windows Media Services.</span></span>

<span data-ttu-id="8e2fa-112">下列各節說明此 SDK 的網路功能。</span><span class="sxs-lookup"><span data-stu-id="8e2fa-112">The following sections describe the networking features of this SDK.</span></span>



| <span data-ttu-id="8e2fa-113">區段</span><span class="sxs-lookup"><span data-stu-id="8e2fa-113">Section</span></span>                                                                    | <span data-ttu-id="8e2fa-114">描述</span><span class="sxs-lookup"><span data-stu-id="8e2fa-114">Description</span></span>                                                                                                          |
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8e2fa-115">網路介面的概觀</span><span class="sxs-lookup"><span data-stu-id="8e2fa-115">Overview of Networking Interfaces</span></span>](overview-of-networking-interfaces.md) | <span data-ttu-id="8e2fa-116">命名並描述支援網路方法的每個介面。</span><span class="sxs-lookup"><span data-stu-id="8e2fa-116">Names and describes each interface that supports networking methods.</span></span>                                                 |
| [<span data-ttu-id="8e2fa-117">透過網路讀取 ASF 資料</span><span class="sxs-lookup"><span data-stu-id="8e2fa-117">Reading ASF Data Over a Network</span></span>](reading-asf-data-over-a-network.md)     | <span data-ttu-id="8e2fa-118">說明如何從網路來源播放檔案，以及如何設定讀取器物件上的網路設定。</span><span class="sxs-lookup"><span data-stu-id="8e2fa-118">Describes how to play files from a network source and how to configure the network settings on the reader object.</span></span>    |
| [<span data-ttu-id="8e2fa-119">透過網路傳送 ASF 資料</span><span class="sxs-lookup"><span data-stu-id="8e2fa-119">Sending ASF Data Over a Network</span></span>](sending-asf-data-over-a-network.md)     | <span data-ttu-id="8e2fa-120">說明如何透過網路廣播 ASF 資料，或將 ASF 資料傳送至 Windows Media 伺服器上的發行端點。</span><span class="sxs-lookup"><span data-stu-id="8e2fa-120">Describes how to broadcast ASF data over a network or send ASF data to a publishing point on a Windows Media server.</span></span> |
| [<span data-ttu-id="8e2fa-121">預設網路設定</span><span class="sxs-lookup"><span data-stu-id="8e2fa-121">Default Networking Settings</span></span>](default-networking-settings.md)             | <span data-ttu-id="8e2fa-122">提供 SDK 所使用之預設設定的快速參考。</span><span class="sxs-lookup"><span data-stu-id="8e2fa-122">Provides a quick reference for the default settings used by the SDK.</span></span>                                                 |



 

## <a name="related-topics"></a><span data-ttu-id="8e2fa-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="8e2fa-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e2fa-124">**程式設計指南**</span><span class="sxs-lookup"><span data-stu-id="8e2fa-124">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 




