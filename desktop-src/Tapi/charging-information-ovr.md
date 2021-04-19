---
description: 收費資訊是針對 ISDN Q. 931 標準所特有。 請參閱您的服務提供者檔，以說明這項資料的意義和使用。
ms.assetid: 5032e2cb-486a-4667-9873-bf88365f12cf
title: 收費資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14d988ec34e901a94e27156f321436b59714cffb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974141"
---
# <a name="charging-information"></a>收費資訊

收費資訊是針對 ISDN Q. 931 標準所特有。 請參閱您的服務提供者檔，以說明這項資料的意義和使用。

並非所有服務提供者都支援使用這項資訊。

**TAPI 2.x：** 請參閱 [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**DwChargingInfoSize** 和 **dwChargingInfoOffset** *lpCallInfo*) 的成員。

**TAPI 3.x：** 請參閱 [**CALLINFO \_ 緩衝區**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer)) 的 [**ITCallInfo：： get \_ CallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfobuffer) (**CIB \_ CHARGINGINFOBUFFER** member。

 

 
