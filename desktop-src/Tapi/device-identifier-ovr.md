---
description: 裝置識別碼是與應用程式無關的識別碼，適用于特定的通訊裝置。
ms.assetid: c7ca72a6-97fa-441f-92ce-a4c77a53765c
title: 裝置識別碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aeb9c88820ecfe26d3ecd971489d709a34af10f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513380"
---
# <a name="device-identifier"></a><span data-ttu-id="266c1-103">裝置識別碼</span><span class="sxs-lookup"><span data-stu-id="266c1-103">Device Identifier</span></span>

<span data-ttu-id="266c1-104">*裝置* 識別碼是與應用程式無關的識別碼，適用于特定的通訊裝置。</span><span class="sxs-lookup"><span data-stu-id="266c1-104">A *device ID* is an application-independent identifier for a specific communications device.</span></span> <span data-ttu-id="266c1-105">通常只有在 TAPI 應用程式需要將通訊會話中涉及不同 API 之函式的部分處理時，才需要這項功能。</span><span class="sxs-lookup"><span data-stu-id="266c1-105">It is typically needed only when a TAPI application needs to hand off part of the processing involving in a communications session to the functions of a different API.</span></span> <span data-ttu-id="266c1-106">例如，TAPI 2.2 應用程式可能無法直接存取媒體串流，而且可能會使用 Wave API。</span><span class="sxs-lookup"><span data-stu-id="266c1-106">For example, TAPI 2.2 applications may be unable to directly access a media stream and might use the Wave API.</span></span>

<span data-ttu-id="266c1-107">**TAPI 2.x：** 請參閱 [**lineGetID**](/windows/win32/api/tapi/nf-tapi-linegetid)。</span><span class="sxs-lookup"><span data-stu-id="266c1-107">**TAPI 2.x:** See [**lineGetID**](/windows/win32/api/tapi/nf-tapi-linegetid).</span></span>

<span data-ttu-id="266c1-108">**TAPI 3.x：** 請 [**參閱 ITAddressCapabilities：： get \_ AddressCapability**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability) (*AddressCap* 設定為 [**ADDRESS \_ 功能**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_capability)) 的 **AC \_ PERMANENTDEVICEID** 成員。</span><span class="sxs-lookup"><span data-stu-id="266c1-108">**TAPI 3.x:** See [**ITAddressCapabilities::get\_AddressCapability**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability) (*AddressCap* set to the **AC\_PERMANENTDEVICEID** member of [**ADDRESS\_CAPABILITY**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_capability)).</span></span>

 

 
