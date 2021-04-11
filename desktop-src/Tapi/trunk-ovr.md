---
description: 用來路由傳送呼叫的主幹數目。 此成員會用於傳入和傳出的呼叫。
ms.assetid: e57e1aac-a2f1-42b7-9a0c-c74009a75305
title: 主幹
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb4afea1387c6d43dc4d9a2f5a6a12f260a8daeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194033"
---
# <a name="trunk"></a><span data-ttu-id="0458d-104">主幹</span><span class="sxs-lookup"><span data-stu-id="0458d-104">Trunk</span></span>

<span data-ttu-id="0458d-105">用來路由傳送呼叫的主幹數目。</span><span class="sxs-lookup"><span data-stu-id="0458d-105">The number of the trunk over which the call is routed.</span></span> <span data-ttu-id="0458d-106">此成員會用於傳入和傳出的呼叫。</span><span class="sxs-lookup"><span data-stu-id="0458d-106">This member is used for both incoming and outgoing calls.</span></span>

<span data-ttu-id="0458d-107">並非所有服務提供者都支援使用這項資訊。</span><span class="sxs-lookup"><span data-stu-id="0458d-107">Not all service providers support use of this information.</span></span>

<span data-ttu-id="0458d-108">\* \* TAPI 2.x： \* \*[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo)、 **dwTrunk** of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)</span><span class="sxs-lookup"><span data-stu-id="0458d-108">\*\*TAPI 2.x:  \*\*[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwTrunk** of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)</span></span>

<span data-ttu-id="0458d-109">\* \* TAPI 3.x： \* \*[**ITCallInfo：： get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong)，以 [**CALLINFO \_ LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)的 **CIL \_ 主幹** 成員呼叫</span><span class="sxs-lookup"><span data-stu-id="0458d-109">\*\*TAPI 3.x:  \*\*[**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), called with **CIL\_TRUNK** member of [**CALLINFO\_LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)</span></span>

 

 
