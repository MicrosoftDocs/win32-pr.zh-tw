---
description: 來源是會話開始位置的一般描述，例如，它是在公司網路外部或內部。 如需 \_ TAPI 支援的來源清單，請參閱 LINECALLORIGIN 常數。
ms.assetid: d9779438-fd08-495a-ae3d-ffad9b543090
title: 來源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71105caff17850c76c1e2c388911086a4cf9ea8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115525"
---
# <a name="origin"></a><span data-ttu-id="55d63-104">來源</span><span class="sxs-lookup"><span data-stu-id="55d63-104">Origin</span></span>

<span data-ttu-id="55d63-105">來源是會話開始位置的一般描述，例如，它是在公司網路外部或內部。</span><span class="sxs-lookup"><span data-stu-id="55d63-105">Origin is a general description of where the session started, such as whether it is external or internal to a corporate network.</span></span> <span data-ttu-id="55d63-106">如需 TAPI 支援的來源清單，請參閱 [LINECALLORIGIN \_ 常數](./linecallorigin--constants.md) 。</span><span class="sxs-lookup"><span data-stu-id="55d63-106">See [LINECALLORIGIN\_ Constants](./linecallorigin--constants.md) for a listing of origins that TAPI supports.</span></span>

<span data-ttu-id="55d63-107">並非所有服務提供者都支援使用這項資訊。</span><span class="sxs-lookup"><span data-stu-id="55d63-107">Not all service providers support use of this information.</span></span>

<span data-ttu-id="55d63-108">**TAPI 2.x：** 請參閱 [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**>dworigin** 成員的 *lpCallInfo*) 。</span><span class="sxs-lookup"><span data-stu-id="55d63-108">**TAPI 2.x:** See [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwOrigin** member of *lpCallInfo*).</span></span>

<span data-ttu-id="55d63-109">**TAPI 3.x：** 請參閱 [**CALLINFO \_ LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)) 的 [**ITCallInfo：： get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**CIL \_ 原始** 成員。</span><span class="sxs-lookup"><span data-stu-id="55d63-109">**TAPI 3.x:** See [**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**CIL\_ORIGIN** member of [**CALLINFO\_LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)).</span></span>

 

 
