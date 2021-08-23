---
description: 通話的速率或頻寬會指定資料傳輸的速度。 三個資料點會以目前的費率，識別指定之持有人模式的最大速率，以及持有人模式的最小費率。
ms.assetid: bc373ac5-a986-483f-a136-60cdc2e2c6b0
title: 費率
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce0af0b2dd6dfe34759753f52773bafe0bdf2bf8f4472ed863dcc6c8b0f10a0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060556"
---
# <a name="rate"></a>費率

呼叫的速率 (或頻寬) 會指定資料傳輸的速度。 三個資料點可識別速率：目前的費率、指定的持有人模式的最大速率，以及持有人模式的最小費率。

並非所有服務提供者都支援使用這項資訊。

* * TAPI 2.x： * *[**lineSetCallParams**](/windows/win32/api/tapi/nf-tapi-linesetcallparams)、 [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo)、 **DwMinRate** 或 **dwMaxRate** member of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)

* * TAPI 3.x： * *[**ITCallInfo：： get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong)、 [**ITCallInfo：:p MAXRATE \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong)、 **cil \_ MINRATE**、 **cil \_ CALLINFO** 或 [**\_ LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)的 **cil \_ RATE** 成員

* * TSPI： * *[**行 \_ CALLINFO**](/previous-versions/windows/desktop/legacy/ms725218(v=vs.85)) 訊息， *dwParam1* 設定為 LINECALLINFOSTATE \_ 率

 

 
