---
description: 來源是會話開始位置的一般描述，例如，它是在公司網路外部或內部。 如需 \_ TAPI 支援的來源清單，請參閱 LINECALLORIGIN 常數。
ms.assetid: d9779438-fd08-495a-ae3d-ffad9b543090
title: 來源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a1f4dafd2b4a3ee85b3a05b3c8ab8f95656237b0ad5bf292c53a5bbb2d3bed3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002826"
---
# <a name="origin"></a>來源

來源是會話開始位置的一般描述，例如，它是在公司網路外部或內部。 如需 TAPI 支援的來源清單，請參閱 [LINECALLORIGIN \_ 常數](./linecallorigin--constants.md) 。

並非所有服務提供者都支援使用這項資訊。

**TAPI 2.x：** 請參閱 [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**>dworigin** 成員的 *lpCallInfo*) 。

**TAPI 3.x：** 請參閱 [**CALLINFO \_ LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)) 的 [**ITCallInfo：： get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**CIL \_ 原始** 成員。

 

 
