---
description: 應用程式特定的資訊可讓應用程式透過 TAPI 傳遞有關會話的其他資訊。 這項資訊不會由 TAPI 解讀，而且使用方式完全由應用程式定義。
ms.assetid: e72e4164-3578-4e18-aea0-09d47d385b57
title: 應用程式特定資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bf4a10413f914eb0bb2da763022f1946811ce12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106974730"
---
# <a name="application-specific-information"></a><span data-ttu-id="78b98-104">應用程式特定資訊</span><span class="sxs-lookup"><span data-stu-id="78b98-104">Application-specific Information</span></span>

<span data-ttu-id="78b98-105">應用程式特定的資訊可讓應用程式透過 TAPI 傳遞有關會話的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="78b98-105">Application-specific information allows applications to pass each other information concerning a session through TAPI.</span></span> <span data-ttu-id="78b98-106">這項資訊不會由 TAPI 解讀，而且使用方式完全由應用程式定義。</span><span class="sxs-lookup"><span data-stu-id="78b98-106">This information is not interpreted by TAPI and usage is entirely defined by the applications.</span></span>

<span data-ttu-id="78b98-107">當某個應用程式變更應用程式特定資訊時，TAPI 會以監視器或擁有者許可權在會話上傳送具有「監視」或「擁有者」許可權的所有其他應用程式，該事件表示已發生變更。</span><span class="sxs-lookup"><span data-stu-id="78b98-107">When application-specific information is changed by one application, TAPI sends all other applications with monitor or owner privileges on the session an event indicating that a change has occurred.</span></span>

<span data-ttu-id="78b98-108">並非所有服務提供者都支援使用這項資訊。</span><span class="sxs-lookup"><span data-stu-id="78b98-108">Not all service providers support use of this information.</span></span>

<span data-ttu-id="78b98-109">**TAPI 2.x：** 請參閱 [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (*DwAppSpecific* member Of *lpCallInfo*) ， [**lineSetAppSpecific**](/windows/win32/api/tapi/nf-tapi-linesetappspecific)， [**LINE \_ CALLINFO**](./line-callinfo.md) message (*dwParam1* 設定為 LINECALLINFOSTATE \_ APPSPECIFIC) 。</span><span class="sxs-lookup"><span data-stu-id="78b98-109">**TAPI 2.x:** See [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (*dwAppSpecific* member of *lpCallInfo*), [**lineSetAppSpecific**](/windows/win32/api/tapi/nf-tapi-linesetappspecific), [**LINE\_CALLINFO**](./line-callinfo.md) message (*dwParam1* set to LINECALLINFOSTATE\_APPSPECIFIC).</span></span>

<span data-ttu-id="78b98-110">**TAPI 3.x：** 請參閱 [**APPSPECIFIC \_ LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)) 的 [**ITCallInfo：： get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong)、 [**ITCallInfo：:p CALLINFO \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong) (**CIL \_** 成員。</span><span class="sxs-lookup"><span data-stu-id="78b98-110">**TAPI 3.x:** See [**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), [**ITCallInfo::put\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong) (**CIL\_APPSPECIFIC** member of [**CALLINFO\_LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)).</span></span>

 

 
