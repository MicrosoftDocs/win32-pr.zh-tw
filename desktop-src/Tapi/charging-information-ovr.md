---
description: 收費資訊是針對 ISDN Q. 931 標準所特有。 請參閱您的服務提供者檔，以說明這項資料的意義和使用。
ms.assetid: 5032e2cb-486a-4667-9873-bf88365f12cf
title: 收費資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14d988ec34e901a94e27156f321436b59714cffb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974141"
---
# <a name="charging-information"></a><span data-ttu-id="f40dd-104">收費資訊</span><span class="sxs-lookup"><span data-stu-id="f40dd-104">Charging Information</span></span>

<span data-ttu-id="f40dd-105">收費資訊是針對 ISDN Q. 931 標準所特有。</span><span class="sxs-lookup"><span data-stu-id="f40dd-105">Charging information is specific to the ISDN Q.931 standard.</span></span> <span data-ttu-id="f40dd-106">請參閱您的服務提供者檔，以說明這項資料的意義和使用。</span><span class="sxs-lookup"><span data-stu-id="f40dd-106">Please refer to your service provider's documentation on the meaning and use of this data.</span></span>

<span data-ttu-id="f40dd-107">並非所有服務提供者都支援使用這項資訊。</span><span class="sxs-lookup"><span data-stu-id="f40dd-107">Not all service providers support use of this information.</span></span>

<span data-ttu-id="f40dd-108">**TAPI 2.x：** 請參閱 [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**DwChargingInfoSize** 和 **dwChargingInfoOffset** *lpCallInfo*) 的成員。</span><span class="sxs-lookup"><span data-stu-id="f40dd-108">**TAPI 2.x:** See [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwChargingInfoSize** and **dwChargingInfoOffset** members of *lpCallInfo*).</span></span>

<span data-ttu-id="f40dd-109">**TAPI 3.x：** 請參閱 [**CALLINFO \_ 緩衝區**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer)) 的 [**ITCallInfo：： get \_ CallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfobuffer) (**CIB \_ CHARGINGINFOBUFFER** member。</span><span class="sxs-lookup"><span data-stu-id="f40dd-109">**TAPI 3.x:** See [**ITCallInfo::get\_CallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfobuffer) (**CIB\_CHARGINGINFOBUFFER** member of [**CALLINFO\_BUFFER**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer)).</span></span>

 

 
