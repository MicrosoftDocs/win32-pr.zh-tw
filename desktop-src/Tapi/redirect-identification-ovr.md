---
description: 當應用程式重新導向會話時，TAPI 會保留重新導向會話之位置的相關識別資訊，以及重新導向的位置。
ms.assetid: 08484b38-7c97-4acc-921e-0f566b2d3415
title: 重新導向識別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8316b7d1566a24ead21f7b1fdf2d16b1c48a2b15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985161"
---
# <a name="redirect-identification"></a><span data-ttu-id="f60cb-103">重新導向識別</span><span class="sxs-lookup"><span data-stu-id="f60cb-103">Redirect Identification</span></span>

<span data-ttu-id="f60cb-104">當應用程式重新 [導向](redirect-ovr.md) 會話時，TAPI 會保留重新導向會話之位置的相關識別資訊，以及重新導向的位置。</span><span class="sxs-lookup"><span data-stu-id="f60cb-104">When an application [redirects](redirect-ovr.md) a session, TAPI retains identification information about the location that redirected the session and the location to which it was redirected.</span></span>

<span data-ttu-id="f60cb-105">「重新導向」指的是叫用重新導向作業的位置。</span><span class="sxs-lookup"><span data-stu-id="f60cb-105">"Redirecting" refers to the location that invoked the redirect operation.</span></span> <span data-ttu-id="f60cb-106">「重新導向」可識別會話的新目的地。</span><span class="sxs-lookup"><span data-stu-id="f60cb-106">"Redirection" identifies the new destination for the session.</span></span>

<span data-ttu-id="f60cb-107">並非所有服務提供者都支援使用這項資訊。</span><span class="sxs-lookup"><span data-stu-id="f60cb-107">Not all service providers support use of this information.</span></span>

<span data-ttu-id="f60cb-108">\* \* TAPI 2.x： \* \*[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo)、 **dwRedirectionIDSize**、 **dwRedirectionIDOffset**、 **dwRedirectionIDNameSize**、 **dwRedirectionIDNameOffset**、 **dwRedirectingIDSize**、 **dwRedirectingIDOffset**、 **dwRedirectingIDNameSize** 和 **dwRedirectingIDNameOffset** 成員 [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)</span><span class="sxs-lookup"><span data-stu-id="f60cb-108">\*\*TAPI 2.x:  \*\*[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwRedirectionIDSize**, **dwRedirectionIDOffset**, **dwRedirectionIDNameSize**, **dwRedirectionIDNameOffset**, **dwRedirectingIDSize**, **dwRedirectingIDOffset**, **dwRedirectingIDNameSize**, and **dwRedirectingIDNameOffset** members of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)</span></span>

<span data-ttu-id="f60cb-109">\* \* TAPI 3.x： \* \*[**ITCallInfo：： get \_ CallInfoString**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring)，以 **cis \_ REDIRECTIONIDNAME**、 **cis \_ REDIRECTIONIDNUMBER**、 **cis \_ REDIRECTINGIDNAME** 或 [**REDIRECTINGIDNUMBER \_ STRING**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)的 **ci \_ CALLINFO** 成員呼叫</span><span class="sxs-lookup"><span data-stu-id="f60cb-109">\*\*TAPI 3.x:  \*\*[**ITCallInfo::get\_CallInfoString**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring)called with the **CIS\_REDIRECTIONIDNAME**, **CIS\_REDIRECTIONIDNUMBER**, **CIS\_REDIRECTINGIDNAME**, or **CIS\_REDIRECTINGIDNUMBER** member of [**CALLINFO\_STRING**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)</span></span>

 

 
