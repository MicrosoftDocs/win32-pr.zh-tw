---
description: 裝置的媒體類型 (或模式) 描述可交換的資訊類型，例如互動式語音。 指定的裝置可能只能處理一種媒體類型，或者可以處理各種類型的類型。
ms.assetid: fccf85e9-3889-4ebc-b1bf-a60e27ab4586
title: 媒體類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 369954a4b0d1f78e12f6ea42bcc2ec61ca425012
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106997596"
---
# <a name="media-type"></a><span data-ttu-id="6acac-104">媒體類型</span><span class="sxs-lookup"><span data-stu-id="6acac-104">Media Type</span></span>

<span data-ttu-id="6acac-105">裝置的 *媒體類型* (或模式) 描述可交換的資訊類型，例如互動式語音。</span><span class="sxs-lookup"><span data-stu-id="6acac-105">The *media type* (or mode) of a device describes the type of information that can be exchanged, such as interactive voice.</span></span> <span data-ttu-id="6acac-106">指定的裝置可能只能處理一種媒體類型，或者可以處理各種類型的類型。</span><span class="sxs-lookup"><span data-stu-id="6acac-106">A given device might be able to handle only one media type, or it might be able to deal with a range of types.</span></span>

<span data-ttu-id="6acac-107">服務提供者會公開所控制裝置所支援的媒體類型或類型。</span><span class="sxs-lookup"><span data-stu-id="6acac-107">Service providers expose the media type or types supported by the devices they control.</span></span> <span data-ttu-id="6acac-108">應用程式會查詢媒體類型，然後使用此資訊來選取適當的位址以起始會話。</span><span class="sxs-lookup"><span data-stu-id="6acac-108">Applications query for media type and then use this information to select an appropriate address on which to initiate a session.</span></span> <span data-ttu-id="6acac-109">所提供之會話的應用程式回應可能也會在媒體類型上前提。</span><span class="sxs-lookup"><span data-stu-id="6acac-109">Application response to a session offered may also be predicated on media type.</span></span>

<span data-ttu-id="6acac-110">指定的通訊會話或呼叫可能牽涉到數種媒體類型。</span><span class="sxs-lookup"><span data-stu-id="6acac-110">A given communications session, or call, can involve several media types.</span></span> <span data-ttu-id="6acac-111">如需詳細資訊，請參閱會話的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="6acac-111">For further information, see Media type for a session.</span></span>

<span data-ttu-id="6acac-112">**TAPI 2.x：** 請參閱 *lpAddressCaps*、 [LINEMEDIAMODE \_ 常數](./linemediamode--constants.md)所指向之 [**LINEADDRESSCAPS**](/windows/win32/api/tapi/ns-tapi-lineaddresscaps)結構的 **dwAvailableMediaModes** 成員 [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps)。</span><span class="sxs-lookup"><span data-stu-id="6acac-112">**TAPI 2.x:** See [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps), **dwAvailableMediaModes** member of [**LINEADDRESSCAPS**](/windows/win32/api/tapi/ns-tapi-lineaddresscaps) structure pointed to by *lpAddressCaps*, [LINEMEDIAMODE\_ Constants](./linemediamode--constants.md).</span></span>

<span data-ttu-id="6acac-113">**TAPI 3.x：** 請參閱 [**ITTerminal：： get \_ 媒體**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_mediatype)， [TAPIMEDIATYPE \_ 常數](tapimediatype--constants.md)。</span><span class="sxs-lookup"><span data-stu-id="6acac-113">**TAPI 3.x:** See [**ITTerminal::get\_MediaType**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_mediatype), [TAPIMEDIATYPE\_ Constants](tapimediatype--constants.md).</span></span>
