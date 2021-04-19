---
description: 呼叫識別碼與會話識別碼不同，這兩個主要方式是服務提供者指派的，而每個處理會話的應用程式都是相同的。
ms.assetid: c9d0d43b-3053-4e3e-b442-57942f3448df
title: 通話識別碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef571b55f653cb9c7bc1d61cdc8a3f71e91ba8f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106989951"
---
# <a name="call-id"></a><span data-ttu-id="3471b-103">通話識別碼</span><span class="sxs-lookup"><span data-stu-id="3471b-103">Call ID</span></span>

<span data-ttu-id="3471b-104">呼叫識別碼與 [會話識別碼](session-identifier-ovr.md) 不同，有兩種主要方式：服務提供者會指派它，而每個處理會話的應用程式都是相同的。</span><span class="sxs-lookup"><span data-stu-id="3471b-104">The Call ID differs from the [Session Identifier](session-identifier-ovr.md) in two primary ways: the service provider assigns it, and it is the same for every application that handles the session.</span></span> <span data-ttu-id="3471b-105">它無法用於與 TAPI 相關的一般通訊，因為它與特定應用程式不相符。</span><span class="sxs-lookup"><span data-stu-id="3471b-105">It cannot be used for ordinary communication with TAPI concerning session operations because it does not match to a particular application.</span></span>

<span data-ttu-id="3471b-106">呼叫識別碼會用於作業中，例如判斷會話識別碼群組是否實際參考一個呼叫，例如會議的案例，或是與其他應用程式的通訊。</span><span class="sxs-lookup"><span data-stu-id="3471b-106">The Call ID is used in operations such as determining whether a group of session IDs actually refer to one call, as is the case for a conference, or for communications with another application.</span></span>

<span data-ttu-id="3471b-107">並非所有服務提供者都支援使用這項資訊。</span><span class="sxs-lookup"><span data-stu-id="3471b-107">Not all service providers support use of this information.</span></span>

<span data-ttu-id="3471b-108">**TAPI 2.x：** 請參閱 [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**DwCallID** 成員的 [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)) 。</span><span class="sxs-lookup"><span data-stu-id="3471b-108">**TAPI 2.x:** See [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwCallID** member of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)).</span></span>

<span data-ttu-id="3471b-109">**TAPI 3.x：** 請參閱 [**ITCallInfo：： get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) ([**CALLINFO \_ LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)) 的 **CIL \_ CALLID** 成員。</span><span class="sxs-lookup"><span data-stu-id="3471b-109">**TAPI 3.x:** See [**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**CIL\_CALLID** member of [**CALLINFO\_LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)).</span></span>

 

 
