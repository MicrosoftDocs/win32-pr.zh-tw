---
description: 裝置特定緩衝區可能是擴充作業的服務提供者執行的一部分。 服務提供者定義這些緩衝區的意義。
ms.assetid: 5783f892-ec11-4340-afad-44f2ef55fd18
title: 裝置特定緩衝區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 628ee93e4f88fc733e744b3c52af3c0a1c31ecf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106985651"
---
# <a name="device-specific-buffer"></a>裝置特定緩衝區

裝置特定緩衝區可能是服務提供者執行擴充作業的一部分。 服務提供者定義這些緩衝區的意義。

並非所有服務提供者都支援使用這項資訊。

**TAPI 2.x：** 請參閱 [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**DwDevSpecificSize** 和 **dwDevSpecificOffset** [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)) 的成員。

**TAPI 3.x：** 請參閱 [**CALLINFO \_ 緩衝區**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer)) 的 [**ITCallInfo：： GetCallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-getcallinfobuffer) (**CIB \_ DEVSPECIFICBUFFER** 成員。

 

 
