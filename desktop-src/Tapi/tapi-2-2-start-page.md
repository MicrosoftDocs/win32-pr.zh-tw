---
description: Microsoft 電話語音應用程式開發介面 (TAPI) 2.2 版 (TAPI/C) 可讓您從基本的數據機控制，到具有多個代理程式和交換器的電話中心進行通訊應用程式的執行。
ms.assetid: 02bfe923-9915-439e-ac7c-a570416d054a
title: 電話語音應用程式設計介面版本2。2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e0dc158210350979105d765dc939f600f61d8bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193074"
---
# <a name="telephony-application-programming-interface-version-22"></a><span data-ttu-id="75021-103">電話語音應用程式設計介面版本2。2</span><span class="sxs-lookup"><span data-stu-id="75021-103">Telephony Application Programming Interface Version 2.2</span></span>

## <a name="purpose"></a><span data-ttu-id="75021-104">目的</span><span class="sxs-lookup"><span data-stu-id="75021-104">Purpose</span></span>

<span data-ttu-id="75021-105">Microsoft 電話語音應用程式開發介面 (TAPI) 2.2 版 (TAPI/C) 可讓您從基本的數據機控制，到具有多個代理程式和交換器的電話中心進行通訊應用程式的執行。</span><span class="sxs-lookup"><span data-stu-id="75021-105">The Microsoft Telephony Application Programming Interface (TAPI) version 2.2 (TAPI/C) enables implementation of communications applications ranging from basic modem control to call centers with multiple agents and switches.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="75021-106">適用時</span><span class="sxs-lookup"><span data-stu-id="75021-106">Where applicable</span></span>

<span data-ttu-id="75021-107">可能的 TAPI 2.2 應用程式包括：</span><span class="sxs-lookup"><span data-stu-id="75021-107">Possible TAPI 2.2 applications include:</span></span>

-   <span data-ttu-id="75021-108">公用交換電話網絡上的基本語音電話 (PSTN) </span><span class="sxs-lookup"><span data-stu-id="75021-108">Basic voice calls on the Public Switched Telephone Network (PSTN)</span></span>
-   <span data-ttu-id="75021-109">用來追蹤多個代理程式的話務中心應用程式</span><span class="sxs-lookup"><span data-stu-id="75021-109">Call center applications for tracking multiple agents</span></span>
-   <span data-ttu-id="75021-110">數據機控制</span><span class="sxs-lookup"><span data-stu-id="75021-110">Modem control</span></span>
-   <span data-ttu-id="75021-111">PBX 控制項</span><span class="sxs-lookup"><span data-stu-id="75021-111">PBX control</span></span>
-   <span data-ttu-id="75021-112">互動式語音回應 (IVR) 系統</span><span class="sxs-lookup"><span data-stu-id="75021-112">Interactive voice response (IVR) systems</span></span>
-   <span data-ttu-id="75021-113">語音信箱</span><span class="sxs-lookup"><span data-stu-id="75021-113">Voice mail</span></span>
-   <span data-ttu-id="75021-114">詳細的電話裝置控制</span><span class="sxs-lookup"><span data-stu-id="75021-114">Detailed phone device control</span></span>

## <a name="developer-audience"></a><span data-ttu-id="75021-115">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="75021-115">Developer audience</span></span>

<span data-ttu-id="75021-116">TAPI/C 是設計來供 C/c + + 程式設計人員使用。</span><span class="sxs-lookup"><span data-stu-id="75021-116">TAPI/C is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="75021-117">電信或其他電話語音應用程式的開發經驗很有説明，但並非必要。</span><span class="sxs-lookup"><span data-stu-id="75021-117">Development experience with telecommunications or other telephony applications is helpful, but not necessary.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="75021-118">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="75021-118">Run-time requirements</span></span>

<span data-ttu-id="75021-119">TAPI 2.2 版可讓您針對 Windows Server 2003 作業系統、Windows XP、Windows 2000、Windows NT、Windows Me、Windows 98 和 Windows 95 進行通訊應用程式的開發。</span><span class="sxs-lookup"><span data-stu-id="75021-119">TAPI version 2.2 enables development of communications applications for the Windows Server 2003 operating systems, Windows XP, Windows 2000, Windows NT, Windows Me, Windows 98, and Windows 95.</span></span> <span data-ttu-id="75021-120">如需有關哪些作業系統支援特定函式的詳細資訊，請參閱該函式檔的需求一節。</span><span class="sxs-lookup"><span data-stu-id="75021-120">For more information about which operating systems support a particular function, see the Requirements section of the documentation for that function.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="75021-121">本節內容</span><span class="sxs-lookup"><span data-stu-id="75021-121">In this section</span></span>



| <span data-ttu-id="75021-122">主題</span><span class="sxs-lookup"><span data-stu-id="75021-122">Topic</span></span>                                          | <span data-ttu-id="75021-123">描述</span><span class="sxs-lookup"><span data-stu-id="75021-123">Description</span></span>                                                                                                       |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="75021-124">概觀</span><span class="sxs-lookup"><span data-stu-id="75021-124">Overview</span></span>](tapi-2-2-overview.md)<br/>   | <span data-ttu-id="75021-125">有關 TAPI 架構和元件的一般資訊。</span><span class="sxs-lookup"><span data-stu-id="75021-125">General information about TAPI architecture and components.</span></span><br/>                                            |
| [<span data-ttu-id="75021-126">參考</span><span class="sxs-lookup"><span data-stu-id="75021-126">Reference</span></span>](tapi-2-2-reference.md)<br/> | <span data-ttu-id="75021-127">TAPI 2.2 中可用的函式、結構、訊息、常數和裝置類別的檔。</span><span class="sxs-lookup"><span data-stu-id="75021-127">Documentation of functions, structures, messages, constants, and device classes available in TAPI 2.2.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="75021-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="75021-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75021-129">TAPI 3。1</span><span class="sxs-lookup"><span data-stu-id="75021-129">TAPI 3.1</span></span>](./tapi-3-1-start-page.md)
</dt> <dt>

[<span data-ttu-id="75021-130">TAPI 服務提供者</span><span class="sxs-lookup"><span data-stu-id="75021-130">TAPI Service Providers</span></span>](./tapi-service-providers.md)
</dt> </dl>

 

