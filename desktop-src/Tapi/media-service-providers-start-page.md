---
description: " (MSP 的媒體服務提供者) 可讓應用程式控制特定傳輸機制的媒體。"
ms.assetid: f886380f-d970-4511-bf71-fb1eb767e4f4
title: 媒體服務提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dd78f5ff4a13da4365f99bd2cb539738b6f3fd6
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106985806"
---
# <a name="media-service-providers"></a><span data-ttu-id="d1981-103">媒體服務提供者</span><span class="sxs-lookup"><span data-stu-id="d1981-103">Media Service Providers</span></span>

## <a name="purpose"></a><span data-ttu-id="d1981-104">目的</span><span class="sxs-lookup"><span data-stu-id="d1981-104">Purpose</span></span>

<span data-ttu-id="d1981-105"> (MSP 的媒體服務提供者) 可讓應用程式控制特定傳輸機制的媒體。</span><span class="sxs-lookup"><span data-stu-id="d1981-105">A media service provider (MSP) enables an application to control media for a particular transport mechanism.</span></span> <span data-ttu-id="d1981-106">MSP 一律與電話語音服務提供者 (TSP) 配對。</span><span class="sxs-lookup"><span data-stu-id="d1981-106">An MSP is always paired with a Telephony Service Provider (TSP).</span></span>

<span data-ttu-id="d1981-107">媒體服務提供者介面 (MSPI) 是一組由 MSP 所執行的介面和方法，可讓應用程式在通訊會話期間對媒體傳輸進行控制。</span><span class="sxs-lookup"><span data-stu-id="d1981-107">The Media Service Provider Interface (MSPI) is a set of interfaces and methods implemented by an MSP to allow an application control over media transport during a communications session.</span></span> <span data-ttu-id="d1981-108">MSP 會處理制定這些控制項所需的裝置特定和通訊協定特定機制，並透過使用 MSPI 中提供的方法，與其配對的 TSP 或應用程式進行通訊。</span><span class="sxs-lookup"><span data-stu-id="d1981-108">An MSP handles the device-specific and protocol-specific mechanisms required to enact these controls, and communicates with its paired TSP or an application through use of the methods provided in the MSPI.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="d1981-109">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="d1981-109">Developer audience</span></span>

<span data-ttu-id="d1981-110">需要熟悉 COM。</span><span class="sxs-lookup"><span data-stu-id="d1981-110">Familiarity with COM is required.</span></span> <span data-ttu-id="d1981-111">電信或其他電話語音應用程式的開發經驗很有説明，但並非必要。</span><span class="sxs-lookup"><span data-stu-id="d1981-111">Development experience with telecommunications or other telephony applications is helpful, but not necessary.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="d1981-112">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="d1981-112">Run-time requirements</span></span>

<span data-ttu-id="d1981-113">MSPI 可讓您針對在 Windows Server 2003 作業系統、Windows XP 及 Windows 2000 上執行的特定通訊協定或裝置，進行媒體服務提供者的開發。</span><span class="sxs-lookup"><span data-stu-id="d1981-113">MSPI enables development of media service providers for particular protocols or devices running on Windows Server 2003 operating systems, Windows XP, and Windows 2000.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d1981-114">本節內容</span><span class="sxs-lookup"><span data-stu-id="d1981-114">In this section</span></span>



| <span data-ttu-id="d1981-115">主題</span><span class="sxs-lookup"><span data-stu-id="d1981-115">Topic</span></span>                                                                       | <span data-ttu-id="d1981-116">描述</span><span class="sxs-lookup"><span data-stu-id="d1981-116">Description</span></span>                                                           |
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="d1981-117">概觀</span><span class="sxs-lookup"><span data-stu-id="d1981-117">Overview</span></span>](about-the-media-service-provider-msp-.md)<br/>            | <span data-ttu-id="d1981-118">MSP 架構和元件的一般資訊。</span><span class="sxs-lookup"><span data-stu-id="d1981-118">General information about MSP architecture and components.</span></span><br/> |
| [<span data-ttu-id="d1981-119">參考</span><span class="sxs-lookup"><span data-stu-id="d1981-119">Reference</span></span>](media-service-provider-interface-mspi-reference.md)<br/> | <span data-ttu-id="d1981-120">MSPI 介面的檔。</span><span class="sxs-lookup"><span data-stu-id="d1981-120">Documentation for the MSPI interfaces.</span></span><br/>                     |



 

## <a name="related-topics"></a><span data-ttu-id="d1981-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="d1981-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1981-122">Microsoft 電話語音總覽</span><span class="sxs-lookup"><span data-stu-id="d1981-122">Microsoft Telephony Overview</span></span>](microsoft-telephony-overview.md)
</dt> <dt>

[<span data-ttu-id="d1981-123">TAPI 3。1</span><span class="sxs-lookup"><span data-stu-id="d1981-123">TAPI 3.1</span></span>](tapi-3-1-start-page.md)
</dt> <dt>

[<span data-ttu-id="d1981-124">電話語音服務提供者</span><span class="sxs-lookup"><span data-stu-id="d1981-124">Telephony Service Providers</span></span>](./telephony-service-providers-start-page.md)
</dt> </dl>

 

