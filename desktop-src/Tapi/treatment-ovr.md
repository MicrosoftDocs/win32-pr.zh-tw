---
description: 處理是指處理尚未接聽或已暫停的傳入會話（例如音樂）。 請參閱 LINECALLTREATMENT 的 \_ 常數，以取得 TAPI 所定義的一組治療。
ms.assetid: 0b8d1023-374a-4937-b39c-04043423eb47
title: 處理方式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60f29f8848c76029daa7828f40061c828b625ec046dea7fac35159b390a4d106
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139741"
---
# <a name="treatment"></a>處理方式

處理是指處理尚未接聽或已暫停的傳入會話（例如音樂）。 請參閱 [LINECALLTREATMENT 的 \_ 常數](./linecalltreatment--constants.md) ，以取得 TAPI 所定義的一組治療。

並非所有服務提供者都支援使用這項資訊。

**TAPI 2.x： **[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (** dwCallTreatment** 成員的 *lpCallInfo*) 

**TAPI 3.x： **[**ITCallInfo：： get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (** \_** [**CALLINFO \_ LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)) 的 CIL CALLTREATMENT 成員

 

 
