---
description: Microsoft 電話語音應用程式開發介面 (TAPI) 3.1 版是一種元件物件模型 (以 COM) 為基礎的 API，可合併傳統和 IP 電話語音。
ms.assetid: 79c4d2c9-953e-4e68-98b7-6a0dd9a04e0b
title: 電話語音應用程式設計介面版本3。1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31d302f6ffe67094d436caf94cc8cf109e1e3c9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980436"
---
# <a name="telephony-application-programming-interface-version-31"></a><span data-ttu-id="f833b-103">電話語音應用程式設計介面版本3。1</span><span class="sxs-lookup"><span data-stu-id="f833b-103">Telephony Application Programming Interface Version 3.1</span></span>

## <a name="purpose"></a><span data-ttu-id="f833b-104">目的</span><span class="sxs-lookup"><span data-stu-id="f833b-104">Purpose</span></span>

<span data-ttu-id="f833b-105">Microsoft 電話語音應用程式開發介面 (TAPI) 3.1 版是一種元件物件模型 (以 COM) 為基礎的 API，可合併傳統和 IP 電話語音。</span><span class="sxs-lookup"><span data-stu-id="f833b-105">The Microsoft Telephony Application Programming Interface (TAPI) version 3.1 is a Component Object Model (COM)-based API that merges classic and IP telephony.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="f833b-106">適用時</span><span class="sxs-lookup"><span data-stu-id="f833b-106">Where applicable</span></span>

<span data-ttu-id="f833b-107">可能的 TAPI 應用程式包括：</span><span class="sxs-lookup"><span data-stu-id="f833b-107">Possible TAPI applications include:</span></span>

-   <span data-ttu-id="f833b-108">具有服務品質 (QOS) 的多播多媒體 IP 會議</span><span class="sxs-lookup"><span data-stu-id="f833b-108">Multicast multimedia IP conferencing with quality of service (QOS)</span></span>
-   <span data-ttu-id="f833b-109">使用 H. 323 通訊協定在網際網路上進行語音通話</span><span class="sxs-lookup"><span data-stu-id="f833b-109">Voice calls over the Internet using the H.323 protocol</span></span>
-   <span data-ttu-id="f833b-110">能夠追蹤多個代理程式的電話中心應用程式</span><span class="sxs-lookup"><span data-stu-id="f833b-110">Call center applications capable of tracking multiple agents</span></span>
-   <span data-ttu-id="f833b-111">公用交換電話網絡上的基本語音電話 (PSTN) </span><span class="sxs-lookup"><span data-stu-id="f833b-111">Basic voice calls on the Public Switched Telephone Network (PSTN)</span></span>
-   <span data-ttu-id="f833b-112">PBX 控制項</span><span class="sxs-lookup"><span data-stu-id="f833b-112">PBX control</span></span>
-   <span data-ttu-id="f833b-113">互動式語音回應 (IVR) 系統</span><span class="sxs-lookup"><span data-stu-id="f833b-113">Interactive voice response (IVR) systems</span></span>
-   <span data-ttu-id="f833b-114">語音信箱</span><span class="sxs-lookup"><span data-stu-id="f833b-114">Voice mail</span></span>

## <a name="developer-audience"></a><span data-ttu-id="f833b-115">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="f833b-115">Developer audience</span></span>

<span data-ttu-id="f833b-116">您可以用多種語言撰寫啟用 TAPI 的應用程式，包括 JAVA、Visual Basic 和 C/c + +。</span><span class="sxs-lookup"><span data-stu-id="f833b-116">You can write TAPI-enabled applications in many languages, including Java, Visual Basic, and C/C++.</span></span> <span data-ttu-id="f833b-117">需要熟悉 COM。</span><span class="sxs-lookup"><span data-stu-id="f833b-117">Familiarity with COM is required.</span></span> <span data-ttu-id="f833b-118">電信或其他電話語音應用程式的開發經驗很有説明，但並非必要。</span><span class="sxs-lookup"><span data-stu-id="f833b-118">Development experience with telecommunications or other telephony applications is helpful, but not necessary.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="f833b-119">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="f833b-119">Run-time requirements</span></span>

<span data-ttu-id="f833b-120">TAPI 3.1 版可讓您開發適用于 Windows Server 2003 作業系統、Windows XP 及 Windows 2000 的通訊應用程式。</span><span class="sxs-lookup"><span data-stu-id="f833b-120">TAPI version 3.1 enables development of communications applications for Windows Server 2003 operating systems, Windows XP, and Windows 2000.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f833b-121">本節內容</span><span class="sxs-lookup"><span data-stu-id="f833b-121">In this section</span></span>



<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th><span data-ttu-id="f833b-122">主題</span><span class="sxs-lookup"><span data-stu-id="f833b-122">Topic</span></span></th><th><span data-ttu-id="f833b-123">描述</span><span class="sxs-lookup"><span data-stu-id="f833b-123">Description</span></span></th></tr></thead><tbody><tr class="odd"><td><span data-ttu-id="f833b-124"><a href="tapi-3-1-overview.md">概觀</a></span><span class="sxs-lookup"><span data-stu-id="f833b-124"><a href="tapi-3-1-overview.md">Overview</a></span></span><br/></td><td><span data-ttu-id="f833b-125">有關 TAPI 架構和元件的一般資訊。</span><span class="sxs-lookup"><span data-stu-id="f833b-125">General information about TAPI architecture and components.</span></span><br/></td></tr><tr class="even"><td><span data-ttu-id="f833b-126">參考</span><span class="sxs-lookup"><span data-stu-id="f833b-126">Reference</span></span><br/></td><td><span data-ttu-id="f833b-127">檔：</span><span class="sxs-lookup"><span data-stu-id="f833b-127">Documentation for:</span></span><br/><ul><li><span data-ttu-id="f833b-128"><a href="call-and-media-controls-reference.md">呼叫和媒體控制項參考</a></span><span class="sxs-lookup"><span data-stu-id="f833b-128"><a href="call-and-media-controls-reference.md">Call and Media Controls Reference</a></span></span></li><li><span data-ttu-id="f833b-129"><a href="call-center-controls-reference.md">撥置控制參考</a></span><span class="sxs-lookup"><span data-stu-id="f833b-129"><a href="call-center-controls-reference.md">Call Center Controls Reference</a></span></span></li><li><span data-ttu-id="f833b-130"><a href="rendezvous-ip-telephony-conferencing-reference.md">會合參考</a></span><span class="sxs-lookup"><span data-stu-id="f833b-130"><a href="rendezvous-ip-telephony-conferencing-reference.md">Rendezvous Reference</a></span></span></li></ul></td></tr></tbody></table>



 

## <a name="related-topics"></a><span data-ttu-id="f833b-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="f833b-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f833b-132">Microsoft 電話語音總覽</span><span class="sxs-lookup"><span data-stu-id="f833b-132">Microsoft Telephony Overview</span></span>](microsoft-telephony-overview.md)
</dt> <dt>

[<span data-ttu-id="f833b-133">TAPI 2。2</span><span class="sxs-lookup"><span data-stu-id="f833b-133">TAPI 2.2</span></span>](./tapi-2-2-start-page.md)
</dt> <dt>

[<span data-ttu-id="f833b-134">TAPI 服務提供者</span><span class="sxs-lookup"><span data-stu-id="f833b-134">TAPI Service Providers</span></span>](./tapi-service-providers.md)
</dt> </dl>

 

