---
description: TAPI 3 呼叫和媒體控制項是一組一般的 COM 物件、介面和方法，可在兩部或多部電腦之間進行呼叫。
ms.assetid: e345df2f-1b68-41be-ac2d-b771136ee831
title: 關於呼叫和媒體控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae65d1a10d004cb16e0ba8753c27665cb7a30ff3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "103853448"
---
# <a name="about-call-and-media-controls"></a><span data-ttu-id="da311-103">關於呼叫和媒體控制項</span><span class="sxs-lookup"><span data-stu-id="da311-103">About Call And Media Controls</span></span>

<span data-ttu-id="da311-104">TAPI 3 呼叫和媒體控制項是一組一般的 COM 物件、介面和方法，可在兩部或多部電腦之間進行呼叫。</span><span class="sxs-lookup"><span data-stu-id="da311-104">TAPI 3 call and media controls are a generic set of COM objects, interfaces, and methods for making calls between two or more machines.</span></span> <span data-ttu-id="da311-105">在 TAPI 3 的內容中， *電話* 指的並非只是透過交換交換電話網絡的語音傳輸 (PSTN) ，而是指服務提供者所在的任何中度和傳輸機制：例如，在公司內部網路上執行的多媒體多播會議。</span><span class="sxs-lookup"><span data-stu-id="da311-105">In the context of TAPI 3, *call* refers not just to voice transmission over the public switched telephone network (PSTN) but to any medium and transport mechanism for which service providers exist: for example, a multimedia multicast conference running on a corporate intranet.</span></span>

<span data-ttu-id="da311-106">TAPI 3 呼叫和媒體控制架構中的五個主要物件是 [tapi](tapi-object.md)、 [位址](address-object.md)、 [終端](terminal-object.md)機、 [電話](call-object.md)和 [CallHub](callhub-object.md)。</span><span class="sxs-lookup"><span data-stu-id="da311-106">The five main objects in the TAPI 3 call and media control architecture are [TAPI](tapi-object.md), [Address](address-object.md), [Terminal](terminal-object.md), [Call](call-object.md), and [CallHub](callhub-object.md).</span></span> <span data-ttu-id="da311-107">此外，也已針對 [提供者特定介面](provider-specific-interfaces.md)進行布建。</span><span class="sxs-lookup"><span data-stu-id="da311-107">In addition, provision has been made for [provider-specific interfaces](provider-specific-interfaces.md).</span></span>

<span data-ttu-id="da311-108">下圖說明這些物件的互動方式。</span><span class="sxs-lookup"><span data-stu-id="da311-108">The following diagram illustrates how these objects interact.</span></span>

![tapi 3.0 呼叫和媒體控制物件之間的互動](images/sdkobj2.png)

## <a name="features"></a><span data-ttu-id="da311-110">功能</span><span class="sxs-lookup"><span data-stu-id="da311-110">Features</span></span>

-   <span data-ttu-id="da311-111">將呼叫和媒體功能抽象化，以允許不同和看似不相容的通訊協定，將通用介面公開給應用程式。</span><span class="sxs-lookup"><span data-stu-id="da311-111">Abstracts both call and media functionality to allow different and seemingly incompatible communication protocols to expose a common interface to applications.</span></span>
-   <span data-ttu-id="da311-112">根據元件物件模型 (COM) 因此，應用程式幾乎可以用任何語言來撰寫。</span><span class="sxs-lookup"><span data-stu-id="da311-112">Based on the Component Object Model (COM) so applications can be written in nearly any language.</span></span> <span data-ttu-id="da311-113">如果您需要有關 COM 的其他資訊，請參閱平臺軟體發展工具組 (SDK) 。</span><span class="sxs-lookup"><span data-stu-id="da311-113">If you require additional information on COM, please consult the Platform Software Development Kit (SDK).</span></span>
-   <span data-ttu-id="da311-114">電話語音服務提供者所提供的呼叫控制 (Tsp) ，其可執行傳輸特定的機制。</span><span class="sxs-lookup"><span data-stu-id="da311-114">Call control provided by Telephony Service Providers (TSPs), which implement transport-specific mechanisms.</span></span>
-   <span data-ttu-id="da311-115">媒體服務提供者所提供的媒體控制項 (Msp) 。</span><span class="sxs-lookup"><span data-stu-id="da311-115">Media control provided by Media Service providers (MSPs).</span></span> <span data-ttu-id="da311-116">目前的 Msp 使用 DirectShow。</span><span class="sxs-lookup"><span data-stu-id="da311-116">Current MSPs use DirectShow.</span></span> <span data-ttu-id="da311-117">DirectShow 是一種模組化系統，稱為篩選器，以稱為篩選圖形的設定排列。</span><span class="sxs-lookup"><span data-stu-id="da311-117">DirectShow is a modular system of pluggable components called filters, arranged in a configuration called a filter graph.</span></span> <span data-ttu-id="da311-118">篩選圖形管理員會監看這些篩選的連接，並控制資料流程的資料流程。</span><span class="sxs-lookup"><span data-stu-id="da311-118">The filter graph manager oversees the connection of these filters and controls the stream's data flow.</span></span> <span data-ttu-id="da311-119">如果您需要 DirectShow 的其他資訊，請參閱 Platform SDK。</span><span class="sxs-lookup"><span data-stu-id="da311-119">If you require additional information on DirectShow, please consult the Platform SDK.</span></span>

 

 



