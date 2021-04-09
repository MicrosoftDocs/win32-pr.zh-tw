---
description: INITIALIZE \_ 協商資料類型是 DWORD 類型的特殊值。
ms.assetid: ce978913-47a1-4387-bd1b-1795aaf82dd7
title: INITIALIZE_NEGOTIATION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51a55879a0952d3f8b5e268ec6a01a666bdbf5ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691387"
---
# <a name="initialize_negotiation"></a><span data-ttu-id="f59eb-103">初始化 \_ 協商</span><span class="sxs-lookup"><span data-stu-id="f59eb-103">INITIALIZE\_NEGOTIATION</span></span>

<span data-ttu-id="f59eb-104">**INITIALIZE \_ 協商** 資料類型是 **DWORD** 類型的特殊值。</span><span class="sxs-lookup"><span data-stu-id="f59eb-104">The **INITIALIZE\_NEGOTIATION** datatype is a special value of type **DWORD**.</span></span> <span data-ttu-id="f59eb-105">您可以在 [**TSPI \_ LineNegotiateTSPIVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion)和 [**TSPI \_ phoneNegotiateTSPIVersion**](/windows/win32/api/tspi/nf-tspi-tspi_phonenegotiatetspiversion)函式中，將它當作 *dwDeviceID* 參數傳遞。</span><span class="sxs-lookup"><span data-stu-id="f59eb-105">It can be passed as the *dwDeviceID* parameter in the [**TSPI\_lineNegotiateTSPIVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion) and [**TSPI\_phoneNegotiateTSPIVersion**](/windows/win32/api/tspi/nf-tspi-tspi_phonenegotiatetspiversion) functions.</span></span> <span data-ttu-id="f59eb-106">這麼做表示 TAPI 可以協調與任何特定裝置無關的 TSPI 介面版本號碼。</span><span class="sxs-lookup"><span data-stu-id="f59eb-106">Doing so indicates that TAPI can negotiate a TSPI interface version number independent of any specific devices.</span></span>

 

 
