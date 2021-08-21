---
description: 呼叫端識別會在接收傳入的會話時，提供呼叫方的相關資訊。 應用程式通常會使用此資料做為使用者的狀態訊息的一部分。
ms.assetid: aaaa5eae-e917-44a7-b9c5-97ca2d9a4eec
title: 呼叫端識別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db3e4e412af29664d5a3585ad783545c13991250db8c449901db07868ea8feb6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118870002"
---
# <a name="caller-identification"></a>呼叫端識別

呼叫端識別會在接收傳入的會話時，提供呼叫方的相關資訊。 應用程式通常會使用此資料做為使用者的狀態訊息的一部分。

這項資訊不一定會立即可用。 如果應用程式想要使用這項資訊，並已驗證服務提供者支援它，則應該先檢查數次，再假設資訊無法使用。

並非所有服務提供者都支援使用這項資訊。

**TAPI 2.x：** 請參閱 *dwCallerIDNameSize*) 的 [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwCallerIDFlags**、 **dwCallerIDSize**、 **dwCallerIDOffset**、 **dwCallerIDNameOffset**、 **dwCallerIDAddressType** 和 **lpCallInfo** 成員。

**TAPI 3.x：** 請參閱 [**ITCallInfo：： \_ get CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) () [**\_ LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)的 **\_ CALLERIDADDRESSTYPE** 成員、 [**ITCallInfo：： Get \_ CallInfoString**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring) (**CIS \_ CALLERIDNAME** 和 [**CALLERIDNAME \_ STRING**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)) 的 **cis \_ CALLINFO** 成員。

 

 
