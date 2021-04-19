---
description: 傳入會話的可能原因（例如其已傳送）會列在 LINECALLREASON \_ 常數中。
ms.assetid: 94cc1a79-7ce4-47ec-bdd8-ee7f0d9f48ed
title: 原因
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79b3bfbbaded05853b447d1291a150113c75bbc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985025"
---
# <a name="reason"></a><span data-ttu-id="c68d6-103">原因</span><span class="sxs-lookup"><span data-stu-id="c68d6-103">Reason</span></span>

<span data-ttu-id="c68d6-104">傳入會話的可能原因（例如其已傳送）會列在 [LINECALLREASON \_ 常數](./linecallreason--constants.md)中。</span><span class="sxs-lookup"><span data-stu-id="c68d6-104">The possible reasons for an incoming session, such as that it was transferred, are listed in the [LINECALLREASON\_ Constants](./linecallreason--constants.md).</span></span>

<span data-ttu-id="c68d6-105">並非所有服務提供者都支援使用這項資訊。</span><span class="sxs-lookup"><span data-stu-id="c68d6-105">Not all service providers support use of this information.</span></span>

<span data-ttu-id="c68d6-106">**TAPI 2.x： **[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (** dwReason** 成員的 *lpCallInfo*) </span><span class="sxs-lookup"><span data-stu-id="c68d6-106">**TAPI 2.x:  **[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (** dwReason** member of *lpCallInfo*)</span></span>

<span data-ttu-id="c68d6-107">**TAPI 3.x： **[**ITCallInfo：： get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (** \_** [**CALLINFO \_ LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)) 的 CIL REASON 成員成員</span><span class="sxs-lookup"><span data-stu-id="c68d6-107">**TAPI 3.x:  **[**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (** CIL\_REASON** member of [**CALLINFO\_LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long))</span></span>

 

 
