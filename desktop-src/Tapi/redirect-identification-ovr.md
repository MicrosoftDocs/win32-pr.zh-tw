---
description: 當應用程式重新導向會話時，TAPI 會保留重新導向會話之位置的相關識別資訊，以及重新導向的位置。
ms.assetid: 08484b38-7c97-4acc-921e-0f566b2d3415
title: 重新導向識別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa7648167e6f60dc2e8593a576053df9a0ff54eb0fadc9a446a66127b435e5c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060446"
---
# <a name="redirect-identification"></a>重新導向識別

當應用程式重新 [導向](redirect-ovr.md) 會話時，TAPI 會保留重新導向會話之位置的相關識別資訊，以及重新導向的位置。

「重新導向」指的是叫用重新導向作業的位置。 「重新導向」可識別會話的新目的地。

並非所有服務提供者都支援使用這項資訊。

* * TAPI 2.x： * *[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo)、 **dwRedirectionIDSize**、 **dwRedirectionIDOffset**、 **dwRedirectionIDNameSize**、 **dwRedirectionIDNameOffset**、 **dwRedirectingIDSize**、 **dwRedirectingIDOffset**、 **dwRedirectingIDNameSize** 和 **dwRedirectingIDNameOffset** 成員 [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)

* * TAPI 3.x： * *[**ITCallInfo：： get \_ CallInfoString**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring)，以 **cis \_ REDIRECTIONIDNAME**、 **cis \_ REDIRECTIONIDNUMBER**、 **cis \_ REDIRECTINGIDNAME** 或 [**REDIRECTINGIDNUMBER \_ STRING**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)的 **ci \_ CALLINFO** 成員呼叫

 

 
