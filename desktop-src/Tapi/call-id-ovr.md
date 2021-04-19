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
# <a name="call-id"></a>通話識別碼

呼叫識別碼與 [會話識別碼](session-identifier-ovr.md) 不同，有兩種主要方式：服務提供者會指派它，而每個處理會話的應用程式都是相同的。 它無法用於與 TAPI 相關的一般通訊，因為它與特定應用程式不相符。

呼叫識別碼會用於作業中，例如判斷會話識別碼群組是否實際參考一個呼叫，例如會議的案例，或是與其他應用程式的通訊。

並非所有服務提供者都支援使用這項資訊。

**TAPI 2.x：** 請參閱 [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**DwCallID** 成員的 [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)) 。

**TAPI 3.x：** 請參閱 [**ITCallInfo：： get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) ([**CALLINFO \_ LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)) 的 **CIL \_ CALLID** 成員。

 

 
