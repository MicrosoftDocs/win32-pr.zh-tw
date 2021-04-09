---
description: Microsoft 電話語音應用程式開發介面 (TAPI) 2.2 版是以 C 為基礎的介面，可讓開發人員執行一系列的通訊應用程式。
ms.assetid: bc67ffbf-c29c-4545-911e-b70ecd43cdfc
title: TAPI 2.2 總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a8f6dfce45b3445dd78767984fadb5c7326da2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849579"
---
# <a name="tapi-22-overview"></a><span data-ttu-id="1cc12-103">TAPI 2.2 總覽</span><span class="sxs-lookup"><span data-stu-id="1cc12-103">TAPI 2.2 Overview</span></span>

<span data-ttu-id="1cc12-104">Microsoft 電話語音應用程式開發介面 (TAPI) 2.2 版是以 C 為基礎的介面，可讓開發人員執行一系列的通訊應用程式。</span><span class="sxs-lookup"><span data-stu-id="1cc12-104">The Microsoft Telephony Application Programming Interface (TAPI) version 2.2 is a C-based interface that allows developers to implement a range of communications applications.</span></span> <span data-ttu-id="1cc12-105">下列內容提供使用 TAPI 2.2 的特定總覽資訊。</span><span class="sxs-lookup"><span data-stu-id="1cc12-105">The following material presents overview information specific to using TAPI 2.2.</span></span> <span data-ttu-id="1cc12-106">主要總覽內容包含在 [Microsoft 電話語音程式設計模型](./microsoft-telephony-programming-model.md)中。</span><span class="sxs-lookup"><span data-stu-id="1cc12-106">Primary overview material is contained in [Microsoft Telephony Programming Model](./microsoft-telephony-programming-model.md).</span></span> <span data-ttu-id="1cc12-107">我們會假設您熟悉這項教材。</span><span class="sxs-lookup"><span data-stu-id="1cc12-107">Familiarity with this material is assumed.</span></span>

-   <span data-ttu-id="1cc12-108">[Tapi 版本控制](tapi-versioning.md) 涵蓋 tapi 的可用版本、其散發方式，以及您的應用程式如何協商要使用的 tapi 版本。</span><span class="sxs-lookup"><span data-stu-id="1cc12-108">[TAPI Versioning](tapi-versioning.md) covers the available versions of TAPI, how they are distributed, and how your application can negotiate the version of TAPI to be used..</span></span>
-   <span data-ttu-id="1cc12-109">[會話存取](session-access.md) 涵蓋了 tapi 2.2 (Tapi/C) 特定的一些通話會話內容。</span><span class="sxs-lookup"><span data-stu-id="1cc12-109">[Session Access](session-access.md) covers some call session material specific to TAPI 2.2 (TAPI/C).</span></span> <span data-ttu-id="1cc12-110">如需有關呼叫會話作業和資訊的主要參考，請參閱 [會話控制](./session-control.md) 的一般總覽。</span><span class="sxs-lookup"><span data-stu-id="1cc12-110">See the general overview on [Session Control](./session-control.md) for primary reference on call session operations and information.</span></span>
-   <span data-ttu-id="1cc12-111">[裝置存取](device-access.md) 涵蓋 tapi 2.2 (Tapi/C) 的特定功能。</span><span class="sxs-lookup"><span data-stu-id="1cc12-111">[Device Access](device-access.md) covers capabilities specific to TAPI 2.2 (TAPI/C).</span></span> <span data-ttu-id="1cc12-112">請參閱裝置 [控制](./device-control.md) 的一般總覽，以取得裝置資訊和作業的主要參考。</span><span class="sxs-lookup"><span data-stu-id="1cc12-112">See the general overview on [Device Control](./device-control.md) for primary reference on device information and operations.</span></span>
-   <span data-ttu-id="1cc12-113">[媒體存取](media-access.md) 涵蓋可用於 TAPI 2.2 應用程式之媒體資訊和控制項的內容。</span><span class="sxs-lookup"><span data-stu-id="1cc12-113">[Media Access](media-access.md) covers material on the media information and controls available to a TAPI 2.2 application.</span></span> <span data-ttu-id="1cc12-114">媒體服務提供者可讓您存取更詳細的控制項，但只有 TAPI 3 (TAPI/COM) 應用程式才能使用其功能。</span><span class="sxs-lookup"><span data-stu-id="1cc12-114">The media service providers give you access to more detailed controls, but only TAPI 3 (TAPI/COM) applications can use their capabilities.</span></span> <span data-ttu-id="1cc12-115">如需其他資訊，請參閱 [媒體服務提供者](./about-the-media-service-provider-msp-.md) 。</span><span class="sxs-lookup"><span data-stu-id="1cc12-115">See [About the Media Service Provider](./about-the-media-service-provider-msp-.md) for additional information.</span></span>
-   <span data-ttu-id="1cc12-116">[話務中心控制](call-center-control.md) 涵蓋使用 TAPI 2.2 ACD) 應用程式時，建立自動呼叫散發 (的材質。</span><span class="sxs-lookup"><span data-stu-id="1cc12-116">[Call Center Control](call-center-control.md) covers material on building Automatic Call Distribution (ACD) applications using TAPI 2.2.</span></span> <span data-ttu-id="1cc12-117">針對 TAPI 3.x，請參閱 [撥置中心控制項](./about-call-center-controls.md)。</span><span class="sxs-lookup"><span data-stu-id="1cc12-117">For TAPI 3.x, see [Call Center Controls](./about-call-center-controls.md).</span></span>
-   <span data-ttu-id="1cc12-118">[電話裝置](phone-devices.md) 涵蓋 tapi 2.2 (Tapi/C) 所提供的補充電話裝置控制項。</span><span class="sxs-lookup"><span data-stu-id="1cc12-118">[Phone Devices](phone-devices.md) covers the supplementary phone device controls supplied by TAPI 2.2 (TAPI/C).</span></span>

 

 
