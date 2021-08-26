---
description: 參數旗標會提供有關通訊會話之各種狀態旗標的資訊，例如是否應該封鎖呼叫端識別。 如需 \_ TAPI 所定義之旗標的清單，請參閱 LINECALLPARAMFLAGS 常數。
ms.assetid: 30511328-a310-42b7-a81e-3ef2abf586ed
title: 參數旗標
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf663ea4ff6121f3e130f9c2a2e4c3c1f86f8611be8cc3fef3762adc535e84bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959858"
---
# <a name="parameter-flags"></a>參數旗標

參數旗標會提供有關通訊會話之各種狀態旗標的資訊，例如是否應該封鎖呼叫端識別。 如需 TAPI 所定義之旗標的清單，請參閱 [LINECALLPARAMFLAGS \_ 常數](./linecallparamflags--constants.md) 。

並非所有服務提供者都支援使用這項資訊。

**TAPI 2.x：** 請參閱 [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**DwCallParamFlags** 成員的 *lpCallInfo*) 。

**TAPI 3.x：** 請參閱 [**ITCallInfo：： get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) ([**CALLINFO \_ LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)) 的 **CIL \_ CALLPARAMSFLAGS** 成員。

 

 
