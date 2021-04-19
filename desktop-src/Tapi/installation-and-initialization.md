---
description: 新服務提供者的安裝是高度裝置和作業系統專用的，因此詳細資料不在此 SDK 範圍內。
ms.assetid: 5b48e144-5092-4462-b74c-d3295d23afe1
title: 安裝和初始化
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4391f8453d17cc70382d3ecb0dff65189b61c310
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978138"
---
# <a name="installation-and-initialization"></a><span data-ttu-id="a0edc-103">安裝和初始化</span><span class="sxs-lookup"><span data-stu-id="a0edc-103">Installation and Initialization</span></span>

<span data-ttu-id="a0edc-104">新服務提供者的安裝是高度裝置和作業系統專用的，因此詳細資料不在此 SDK 範圍內。</span><span class="sxs-lookup"><span data-stu-id="a0edc-104">Installation of a new service provider is highly device- and operating-system-specific, so the details are outside the scope of this SDK.</span></span> <span data-ttu-id="a0edc-105">一般來說，安裝的目標是針對目前的通訊環境設定服務提供者。</span><span class="sxs-lookup"><span data-stu-id="a0edc-105">Generally speaking, the goal of installation is configuration of the service provider for the current communications environment.</span></span> <span data-ttu-id="a0edc-106">這通常牽涉到登錄專案和服務相依性的設定。</span><span class="sxs-lookup"><span data-stu-id="a0edc-106">This usually involves registry entries and the setting of service dependencies.</span></span>

<span data-ttu-id="a0edc-107">電話語音服務提供者的初始化是從版本協商開始。</span><span class="sxs-lookup"><span data-stu-id="a0edc-107">Initialization of a telephony service provider starts with version negotiation.</span></span> <span data-ttu-id="a0edc-108">如需版本協商和目前版本的討論，請參閱 [TSPI 版本控制](tspi-versioning.md) 。</span><span class="sxs-lookup"><span data-stu-id="a0edc-108">See [TSPI Versioning](tspi-versioning.md) for a discussion of version negotiation and current version.</span></span>

<span data-ttu-id="a0edc-109">然後，TAPI 會呼叫 [**TSPI \_ providerInit**](/windows/win32/api/tspi/nf-tspi-tspi_providerinit)，它會將指標傳遞至用來報告非同步函式進度的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="a0edc-109">TAPI then calls [**TSPI\_providerInit**](/windows/win32/api/tspi/nf-tspi-tspi_providerinit), which passes the provider a pointer to a callback function used to report on asynchronous functions progress.</span></span> <span data-ttu-id="a0edc-110">TSP 會傳回與目前裝置識別碼相關聯的線路與電話裝置計數。</span><span class="sxs-lookup"><span data-stu-id="a0edc-110">The TSP returns a count of line and phone devices associated with the current device identifier.</span></span>

<span data-ttu-id="a0edc-111">一般而言，下一個步驟將是由 TAPI 叫用 [**TSPI \_ LineGetDevCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevcaps) 和 [**TSPI \_ lineGetAddressCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddresscaps)所進行的資源清查。</span><span class="sxs-lookup"><span data-stu-id="a0edc-111">Typically, the next step will be resource inventory, conducted by TAPI invoking [**TSPI\_lineGetDevCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevcaps) and [**TSPI\_lineGetAddressCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddresscaps).</span></span> <span data-ttu-id="a0edc-112">服務提供者預期會填入相關的資料結構元素，這些元素與它所支援的裝置和會話功能有關。</span><span class="sxs-lookup"><span data-stu-id="a0edc-112">The service provider is expected to fill in those elements of the data structures involved that pertain to device and session capabilities it supports.</span></span>

<span data-ttu-id="a0edc-113">TAPI 會從各種應用程式收集有關事件通知需求的資訊，並使用 [**TSPI \_ LINESETDEFAULTMEDIADETECTION**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection) 指示 TSP 來指出要偵測哪些媒體類型和 [**TSPI \_ lineSetStatusMessages**](/windows/win32/api/tspi/nf-tspi-tspi_linesetstatusmessages) ，以指出應該報告哪個行和位址事件。</span><span class="sxs-lookup"><span data-stu-id="a0edc-113">TAPI collects information from the various applications concerning event notification requirements, and instructs the TSP using [**TSPI\_lineSetDefaultMediaDetection**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection) to indicate which media types to detect for a line and [**TSPI\_lineSetStatusMessages**](/windows/win32/api/tspi/nf-tspi-tspi_linesetstatusmessages) to indicate which line and address events should be reported.</span></span>

 

 
