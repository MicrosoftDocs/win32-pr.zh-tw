---
description: 用來路由傳送呼叫的主幹數目。 此成員會用於傳入和傳出的呼叫。
ms.assetid: e57e1aac-a2f1-42b7-9a0c-c74009a75305
title: 主幹
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 676721df074d0fe84efbe3256da3e111e94932e0b99d5614d792ddbb0c860ca8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872558"
---
# <a name="trunk"></a>主幹

用來路由傳送呼叫的主幹數目。 此成員會用於傳入和傳出的呼叫。

並非所有服務提供者都支援使用這項資訊。

* * TAPI 2.x： * *[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo)、 **dwTrunk** of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)

* * TAPI 3.x： * *[**ITCallInfo：： get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong)，以 [**CALLINFO \_ LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)的 **CIL \_ 主幹** 成員呼叫

 

 
