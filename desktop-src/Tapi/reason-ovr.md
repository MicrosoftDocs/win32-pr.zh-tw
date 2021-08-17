---
description: 傳入會話的可能原因（例如其已傳送）會列在 LINECALLREASON \_ 常數中。
ms.assetid: 94cc1a79-7ce4-47ec-bdd8-ee7f0d9f48ed
title: 原因
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4be431b5d3918714a11fb95411a8d5503a47f9e6d4cd462f9a208f00dfb96c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139951"
---
# <a name="reason"></a>原因

傳入會話的可能原因（例如其已傳送）會列在 [LINECALLREASON \_ 常數](./linecallreason--constants.md)中。

並非所有服務提供者都支援使用這項資訊。

**TAPI 2.x： **[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (** dwReason** 成員的 *lpCallInfo*) 

**TAPI 3.x： **[**ITCallInfo：： get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (** \_** [**CALLINFO \_ LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)) 的 CIL REASON 成員成員

 

 
