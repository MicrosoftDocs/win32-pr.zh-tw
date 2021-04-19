---
description: 許可權指的是應用程式擁有或正在監視會話。
ms.assetid: 0c02a88a-370f-4eb9-ba64-07a382bd2e87
title: Privilege
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2f773edb05afc029a8f9fb6b014cd8a737eef0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971523"
---
# <a name="privilege"></a><span data-ttu-id="d7629-103">Privilege</span><span class="sxs-lookup"><span data-stu-id="d7629-103">Privilege</span></span>

<span data-ttu-id="d7629-104">許可權指的是應用程式擁有或正在監視會話。</span><span class="sxs-lookup"><span data-stu-id="d7629-104">Privilege refers to whether an application owns or is monitoring the session.</span></span> <span data-ttu-id="d7629-105">如果應用程式擁有會話，就可以執行各種會話作業。</span><span class="sxs-lookup"><span data-stu-id="d7629-105">If the application owns the session, it is allowed to perform a variety of session operations.</span></span> <span data-ttu-id="d7629-106">如果應用程式只是監視，它就會接收狀態訊息，而且它可以存取會話資訊，但任何嘗試執行大部分的作業都會導致錯誤。</span><span class="sxs-lookup"><span data-stu-id="d7629-106">If the application is only monitoring, it will receive state messages and it can access session information, but any attempt to perform most operations will result in an error.</span></span>

<span data-ttu-id="d7629-107">在初始化期間，應用程式會告知 TAPI 所需的許可權層級在哪個位址上。</span><span class="sxs-lookup"><span data-stu-id="d7629-107">During initialization, an application tells TAPI which privilege level it requires on which addresses.</span></span> <span data-ttu-id="d7629-108">TAPI 僅針對已註冊擁有者或擁有者和監視許可權的應用程式，提供連入會話。</span><span class="sxs-lookup"><span data-stu-id="d7629-108">TAPI offers incoming sessions only to applications that have registered for either owner or owner and monitor privilege.</span></span>

<span data-ttu-id="d7629-109">應用程式在其建立的會話上的許可權一律為擁有者。</span><span class="sxs-lookup"><span data-stu-id="d7629-109">An application's privilege on a session it creates is always owner.</span></span>

<span data-ttu-id="d7629-110">**TAPI 2.x：** 請參閱 [**lineGetCallStatus**](/windows/win32/api/tapi/nf-tapi-linegetcallstatus)、 **DwCallPrivilege** member of [**LINECALLSTATUS**](/windows/win32/api/tapi/ns-tapi-linecallstatus)、 [**lineSetCallPrivilege**](/windows/win32/api/tapi/nf-tapi-linesetcallprivilege)。</span><span class="sxs-lookup"><span data-stu-id="d7629-110">**TAPI 2.x:** See [**lineGetCallStatus**](/windows/win32/api/tapi/nf-tapi-linegetcallstatus), **dwCallPrivilege** member of [**LINECALLSTATUS**](/windows/win32/api/tapi/ns-tapi-linecallstatus), [**lineSetCallPrivilege**](/windows/win32/api/tapi/nf-tapi-linesetcallprivilege).</span></span>

<span data-ttu-id="d7629-111">**TAPI 3.x：** 請參閱 [**ITCallInfo：： get \_ 許可權**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_privilege)、 [**ITCallInfo：： \_ get CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong)（以 **CIL \_ NUMBEROFOWNERS** 或 [**NUMBEROFMONITORS \_ LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)的 **cil \_ CALLINFO** 成員呼叫）。</span><span class="sxs-lookup"><span data-stu-id="d7629-111">**TAPI 3.x:** See [**ITCallInfo::get\_Privilege**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_privilege), [**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), called with the **CIL\_NUMBEROFOWNERS** or **CIL\_NUMBEROFMONITORS** member of [**CALLINFO\_LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long).</span></span>

 

 
