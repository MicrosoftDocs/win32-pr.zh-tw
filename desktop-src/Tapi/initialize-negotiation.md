---
description: INITIALIZE \_ 協商資料類型是 DWORD 類型的特殊值。
ms.assetid: ce978913-47a1-4387-bd1b-1795aaf82dd7
title: INITIALIZE_NEGOTIATION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d24763b9214dcffab99c83f24028e451a33d70dd7e4210f4eff64b0c39306d6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117762775"
---
# <a name="initialize_negotiation"></a>初始化 \_ 協商

**INITIALIZE \_ 協商** 資料類型是 **DWORD** 類型的特殊值。 您可以在 [**TSPI \_ LineNegotiateTSPIVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion)和 [**TSPI \_ phoneNegotiateTSPIVersion**](/windows/win32/api/tspi/nf-tspi-tspi_phonenegotiatetspiversion)函式中，將它當作 *dwDeviceID* 參數傳遞。 這麼做表示 TAPI 可以協調與任何特定裝置無關的 TSPI 介面版本號碼。

 

 
