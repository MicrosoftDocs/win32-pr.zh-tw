---
description: 相容性緩衝區是針對 ISDN 931 標準所特有。 請參閱您的服務提供者檔，以說明這項資料的意義和使用。
ms.assetid: c4c87ca8-fbae-4275-9b69-7b32daf4c18f
title: 相容性緩衝區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8669e32cd47978c10e2f5abdbe076bcf08ba1862
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998078"
---
# <a name="compatibility-buffer"></a><span data-ttu-id="0cb1b-104">相容性緩衝區</span><span class="sxs-lookup"><span data-stu-id="0cb1b-104">Compatibility Buffer</span></span>

<span data-ttu-id="0cb1b-105">相容性緩衝區是針對 ISDN 931 標準所特有。</span><span class="sxs-lookup"><span data-stu-id="0cb1b-105">The compatibility buffer is specific to the ISDN Q.931 standard.</span></span> <span data-ttu-id="0cb1b-106">請參閱您的服務提供者檔，以說明這項資料的意義和使用。</span><span class="sxs-lookup"><span data-stu-id="0cb1b-106">Please refer to your service provider's documentation on the meaning and use of this data.</span></span>

<span data-ttu-id="0cb1b-107">並非所有服務提供者都支援使用這項資訊。</span><span class="sxs-lookup"><span data-stu-id="0cb1b-107">Not all service providers support use of this information.</span></span>

<span data-ttu-id="0cb1b-108">**TAPI 2.x：** 請參閱 *dwLowLevelCompOffset*) 的 [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwHighLevelCompSize**、 **dwHighLevelCompOffset**、 **dwLowLevelCompSize** 和 **lpCallInfo** 成員。</span><span class="sxs-lookup"><span data-stu-id="0cb1b-108">**TAPI 2.x:** See [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwHighLevelCompSize**, **dwHighLevelCompOffset**, **dwLowLevelCompSize**, and **dwLowLevelCompOffset** members of *lpCallInfo*).</span></span>

<span data-ttu-id="0cb1b-109">**TAPI 3.x：** 請參閱 [**CIB \_ 緩衝區**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer)) 的 [**ITCallInfo：： get \_ CallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfobuffer) (**CIB \_ HIGHLEVELCOMPATIBILITYBUFFER** 和 **LOWLEVELCOMPATIBILITYBUFFER \_ CALLINFO** 成員。</span><span class="sxs-lookup"><span data-stu-id="0cb1b-109">**TAPI 3.x:** See [**ITCallInfo::get\_CallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfobuffer) (**CIB\_HIGHLEVELCOMPATIBILITYBUFFER** and **CIB\_LOWLEVELCOMPATIBILITYBUFFER** member of [**CALLINFO\_BUFFER**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer)).</span></span>

 

 
