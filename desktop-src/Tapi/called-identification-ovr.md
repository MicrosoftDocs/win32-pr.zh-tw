---
description: 呼叫識別可識別會話的原始目的地位址。 在重新導向、轉送或傳輸會話的情況下，這會與連線的識別碼不同。
ms.assetid: a03286eb-83a9-4170-b514-e8899fd04c74
title: 稱為識別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63f862d18fb3deb661cb8379c90a4b3e70caab1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850479"
---
# <a name="called-identification"></a>稱為識別

呼叫識別可識別會話的原始目的地位址。 在重新導向、轉送或傳輸會話的情況下，這會與 [連線的識別碼](connected-identification-ovr.md)不同。

並非所有服務提供者都支援使用這項資訊。

**TAPI 2.x：** 請參閱 *dwCalledIDNameSize*) 的 [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwCalledIDFlags**、 **dwCalledIDSize**、 **dwCalledIDOffset**、 **dwCalledIDNameOffset**、 **dwCalledIDAddressType** 和 **lpCallInfo** 成員。

**TAPI 3.x：** 請參閱 [**ITCallInfo：： \_ get CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) () [**\_ LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)的 **\_ CALLEDIDADDRESSTYPE** 成員、 [**ITCallInfo：： Get \_ CallInfoString**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring) (**CIS \_ CALLEDIDNAME** 和 [**CALLEDIDNAME \_ STRING**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)) 的 **cis \_ CALLINFO** 成員。

 

 
