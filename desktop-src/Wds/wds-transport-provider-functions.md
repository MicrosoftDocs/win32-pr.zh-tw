---
title: WDS 傳輸提供者函式
description: 使用者定義內容提供者可以將下列回呼函數公開給多播伺服器。
ms.assetid: 30ec1969-4e90-458e-8a9f-39a7bbf4cd79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a2e67747d8ef5738a4bf3bee8ff2ffb3b35cf43
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675436"
---
# <a name="wds-transport-provider-functions"></a><span data-ttu-id="8af6d-103">WDS 傳輸提供者函式</span><span class="sxs-lookup"><span data-stu-id="8af6d-103">WDS Transport Provider Functions</span></span>

<span data-ttu-id="8af6d-104">使用者定義內容提供者可以將下列回呼函數公開給多播伺服器。</span><span class="sxs-lookup"><span data-stu-id="8af6d-104">User-defined content providers can expose the following callback functions to the multicast server.</span></span>



| <span data-ttu-id="8af6d-105">函式</span><span class="sxs-lookup"><span data-stu-id="8af6d-105">Function</span></span>                                                                               | <span data-ttu-id="8af6d-106">描述</span><span class="sxs-lookup"><span data-stu-id="8af6d-106">Description</span></span>                                                                                                             |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8af6d-107">*WdsTransportProviderCloseContent*</span><span class="sxs-lookup"><span data-stu-id="8af6d-107">*WdsTransportProviderCloseContent*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderclosecontent)             | <span data-ttu-id="8af6d-108">關閉控制碼所指定的內容資料流程。</span><span class="sxs-lookup"><span data-stu-id="8af6d-108">Closes a content stream specified by a handle.</span></span>                                                                          |
| [<span data-ttu-id="8af6d-109">*WdsTransportProviderCloseInstance*</span><span class="sxs-lookup"><span data-stu-id="8af6d-109">*WdsTransportProviderCloseInstance*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidercloseinstance)           | <span data-ttu-id="8af6d-110">關閉由控制碼所指定之內容提供者的實例。</span><span class="sxs-lookup"><span data-stu-id="8af6d-110">Closes an instance of a content provider specified by a handle.</span></span>                                                         |
| [<span data-ttu-id="8af6d-111">*WdsTransportProviderCompareContent*</span><span class="sxs-lookup"><span data-stu-id="8af6d-111">*WdsTransportProviderCompareContent*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidercomparecontent)         | <span data-ttu-id="8af6d-112">將指定的內容名稱和實例與開啟的內容資料流程進行比較，以判斷它們是否相同。</span><span class="sxs-lookup"><span data-stu-id="8af6d-112">Compares a specified content name and instance to an open content stream to determine if they are the same.</span></span>             |
| [<span data-ttu-id="8af6d-113">*WdsTransportProviderCreateInstance*</span><span class="sxs-lookup"><span data-stu-id="8af6d-113">*WdsTransportProviderCreateInstance*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidercreateinstance)         | <span data-ttu-id="8af6d-114">開啟內容提供者的新實例。</span><span class="sxs-lookup"><span data-stu-id="8af6d-114">Opens a new instance of a content provider.</span></span>                                                                             |
| [<span data-ttu-id="8af6d-115">*WdsTransportProviderDumpState*</span><span class="sxs-lookup"><span data-stu-id="8af6d-115">*WdsTransportProviderDumpState*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderdumpstate)                   | <span data-ttu-id="8af6d-116">指示傳輸提供者將其狀態的摘要以及任何其他相關資訊列印到追蹤記錄檔。</span><span class="sxs-lookup"><span data-stu-id="8af6d-116">Instructs the transport provider to print a summary of its state and any other relevant information to the tracing log.</span></span> |
| [<span data-ttu-id="8af6d-117">*WdsTransportProviderGetContentMetadata*</span><span class="sxs-lookup"><span data-stu-id="8af6d-117">*WdsTransportProviderGetContentMetadata*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidergetcontentmetadata) | <span data-ttu-id="8af6d-118">抓取開啟內容資料流程的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="8af6d-118">Retrieves metadata for an open content stream.</span></span>                                                                          |
| [<span data-ttu-id="8af6d-119">*WdsTransportProviderGetContentSize*</span><span class="sxs-lookup"><span data-stu-id="8af6d-119">*WdsTransportProviderGetContentSize*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidergetcontentsize)         | <span data-ttu-id="8af6d-120">抓取開啟內容資料流程的大小。</span><span class="sxs-lookup"><span data-stu-id="8af6d-120">Retrieves the size of an open content stream.</span></span>                                                                           |
| [<span data-ttu-id="8af6d-121">*WdsTransportProviderInitialize*</span><span class="sxs-lookup"><span data-stu-id="8af6d-121">*WdsTransportProviderInitialize*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize)                 | <span data-ttu-id="8af6d-122">初始化內容提供者。</span><span class="sxs-lookup"><span data-stu-id="8af6d-122">Initializes a content provider.</span></span>                                                                                         |
| [<span data-ttu-id="8af6d-123">*WdsTransportProviderOpenContent*</span><span class="sxs-lookup"><span data-stu-id="8af6d-123">*WdsTransportProviderOpenContent*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovideropencontent)               | <span data-ttu-id="8af6d-124">開啟內容資料流程的新靜態視圖。</span><span class="sxs-lookup"><span data-stu-id="8af6d-124">Opens a new static view of a content stream.</span></span>                                                                            |
| [<span data-ttu-id="8af6d-125">*WdsTransportProviderReadContent*</span><span class="sxs-lookup"><span data-stu-id="8af6d-125">*WdsTransportProviderReadContent*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderreadcontent)               | <span data-ttu-id="8af6d-126">從開啟的內容資料流程讀取內容。</span><span class="sxs-lookup"><span data-stu-id="8af6d-126">Reads content from an open content stream.</span></span>                                                                              |
| [<span data-ttu-id="8af6d-127">*WdsTransportProviderRefreshSettings*</span><span class="sxs-lookup"><span data-stu-id="8af6d-127">*WdsTransportProviderRefreshSettings*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderrefreshsettings)       | <span data-ttu-id="8af6d-128">指示傳輸提供者重新讀取任何相關的設定。</span><span class="sxs-lookup"><span data-stu-id="8af6d-128">Instructs the transport provider to reread any relevant settings.</span></span>                                                       |
| [<span data-ttu-id="8af6d-129">*WdsTransportProviderShutdown*</span><span class="sxs-lookup"><span data-stu-id="8af6d-129">*WdsTransportProviderShutdown*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidershutdown)                     | <span data-ttu-id="8af6d-130">Shutsdown 內容提供者。</span><span class="sxs-lookup"><span data-stu-id="8af6d-130">Shutsdown the content provider.</span></span>                                                                                         |
| [<span data-ttu-id="8af6d-131">*WdsTransportProviderUserAccessCheck*</span><span class="sxs-lookup"><span data-stu-id="8af6d-131">*WdsTransportProviderUserAccessCheck*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovideruseraccesscheck)       | <span data-ttu-id="8af6d-132">根據使用者的權杖，指定內容資料流程的存取權。</span><span class="sxs-lookup"><span data-stu-id="8af6d-132">Specifies access to a content stream based on a user's token.</span></span>                                                           |



 

 

 




