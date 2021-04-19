---
description: 每當 TAPI 呼叫下列其中一項功能時，服務提供者就必須建立一個或多個呼叫控制碼 (變數類型 HDRVCALL) 。
ms.assetid: 0a9d9afd-9786-4d9e-b0a2-12c9a1e13887
title: 暫止的呼叫控制碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c021ff10f2a1a812c46fb77663ac1a3a3a8d791
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991706"
---
# <a name="pending-call-handles"></a><span data-ttu-id="ef2d0-103">暫止的呼叫控制碼</span><span class="sxs-lookup"><span data-stu-id="ef2d0-103">Pending Call Handles</span></span>

<span data-ttu-id="ef2d0-104">每當 TAPI 呼叫下列其中一項功能時，服務提供者就必須建立一個或多個呼叫控制碼 (變數類型 [HDRVCALL](hdrvline.md)) ： [**TSPI \_ lineMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall)、 [**TSPI \_ lineCompleteTransfer**](/windows/win32/api/tspi/nf-tspi-tspi_linecompletetransfer)、 [**TSPI \_ lineForward**](/windows/win32/api/tspi/nf-tspi-tspi_lineforward)、 [**TSPI \_ linePickup**](/windows/win32/api/tspi/nf-tspi-tspi_linepickup)、 [**TSPI \_ linePrepareAddToConference**](/windows/win32/api/tspi/nf-tspi-tspi_lineprepareaddtoconference) [**、TSPI lineSetupConference、 \_**](/windows/win32/api/tspi/nf-tspi-tspi_linesetupconference) [**TSPI lineSetupTransfer \_**](/windows/win32/api/tspi/nf-tspi-tspi_linesetuptransfer)和 [**TSPI \_ lineUnpark**](/windows/win32/api/tspi/nf-tspi-tspi_lineunpark)。</span><span class="sxs-lookup"><span data-stu-id="ef2d0-104">A service provider is required to create one or more call handles (variables of type [HDRVCALL](hdrvline.md)) whenever TAPI calls one of these functions: [**TSPI\_lineMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall), [**TSPI\_lineCompleteTransfer**](/windows/win32/api/tspi/nf-tspi-tspi_linecompletetransfer), [**TSPI\_lineForward**](/windows/win32/api/tspi/nf-tspi-tspi_lineforward), [**TSPI\_linePickup**](/windows/win32/api/tspi/nf-tspi-tspi_linepickup), [**TSPI\_linePrepareAddToConference**](/windows/win32/api/tspi/nf-tspi-tspi_lineprepareaddtoconference), [**TSPI\_lineSetupConference**](/windows/win32/api/tspi/nf-tspi-tspi_linesetupconference), [**TSPI\_lineSetupTransfer**](/windows/win32/api/tspi/nf-tspi-tspi_linesetuptransfer), and [**TSPI\_lineUnpark**](/windows/win32/api/tspi/nf-tspi-tspi_lineunpark).</span></span> <span data-ttu-id="ef2d0-105">當服務提供者收到這類呼叫時，服務提供者必須將 TAPI 提供的變數設定為從呼叫傳回之前的控制碼值。</span><span class="sxs-lookup"><span data-stu-id="ef2d0-105">When a service provider receives such a call, the service provider must set the variable supplied by TAPI to the value of the handle before returning from the call.</span></span> <span data-ttu-id="ef2d0-106">TAPI 會將此「擱置的呼叫控制碼」視為暫時有效。</span><span class="sxs-lookup"><span data-stu-id="ef2d0-106">TAPI considers this "pending call handle" to be tentatively valid.</span></span> <span data-ttu-id="ef2d0-107">當服務提供者實際建立呼叫時，必須呼叫 [**非同步 \_ 完成**](/windows/win32/api/tspi/nc-tspi-async_completion) 回呼以正式驗證控制碼。</span><span class="sxs-lookup"><span data-stu-id="ef2d0-107">When the service provider actually creates the call, it must call the [**ASYNC\_COMPLETION**](/windows/win32/api/tspi/nc-tspi-async_completion) callback to formally validate the handle.</span></span>

<span data-ttu-id="ef2d0-108">如果在服務提供者正式驗證暫止的呼叫控制碼之前，TAPI 呼叫 [**TSPI \_ lineCloseCall**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall) 函式，服務提供者必須停止與呼叫控制碼相關的所有進一步處理，並使用錯誤值 LINEERR OPERATIONFAILED 來呼叫 [**非同步 \_ 完成**](/windows/win32/api/tspi/nc-tspi-async_completion) 回呼函數 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ef2d0-108">If TAPI calls the [**TSPI\_lineCloseCall**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall) function before the service provider formally validates a pending call handle, the service provider must stop all further processing associated with the call handle and call the [**ASYNC\_COMPLETION**](/windows/win32/api/tspi/nc-tspi-async_completion) callback function using the error value LINEERR\_OPERATIONFAILED.</span></span>

 

 
