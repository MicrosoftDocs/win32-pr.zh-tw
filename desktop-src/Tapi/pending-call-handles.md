---
description: 每當 TAPI 呼叫下列其中一項功能時，服務提供者就必須建立一個或多個呼叫控制碼 (變數類型 HDRVCALL) 。
ms.assetid: 0a9d9afd-9786-4d9e-b0a2-12c9a1e13887
title: 暫止的呼叫控制碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d082c0b9111d6d58debacec01d20ffe9af2d024aafd61b3f1085267e62d3d6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119518587"
---
# <a name="pending-call-handles"></a>暫止的呼叫控制碼

每當 TAPI 呼叫下列其中一項功能時，服務提供者就必須建立一個或多個呼叫控制碼 (變數類型 [HDRVCALL](hdrvline.md)) ： [**TSPI \_ lineMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall)、 [**TSPI \_ lineCompleteTransfer**](/windows/win32/api/tspi/nf-tspi-tspi_linecompletetransfer)、 [**TSPI \_ lineForward**](/windows/win32/api/tspi/nf-tspi-tspi_lineforward)、 [**TSPI \_ linePickup**](/windows/win32/api/tspi/nf-tspi-tspi_linepickup)、 [**TSPI \_ linePrepareAddToConference**](/windows/win32/api/tspi/nf-tspi-tspi_lineprepareaddtoconference) [**、TSPI lineSetupConference、 \_**](/windows/win32/api/tspi/nf-tspi-tspi_linesetupconference) [**TSPI lineSetupTransfer \_**](/windows/win32/api/tspi/nf-tspi-tspi_linesetuptransfer)和 [**TSPI \_ lineUnpark**](/windows/win32/api/tspi/nf-tspi-tspi_lineunpark)。 當服務提供者收到這類呼叫時，服務提供者必須將 TAPI 提供的變數設定為從呼叫傳回之前的控制碼值。 TAPI 會將此「擱置的呼叫控制碼」視為暫時有效。 當服務提供者實際建立呼叫時，必須呼叫 [**非同步 \_ 完成**](/windows/win32/api/tspi/nc-tspi-async_completion) 回呼以正式驗證控制碼。

如果在服務提供者正式驗證暫止的呼叫控制碼之前，TAPI 呼叫 [**TSPI \_ lineCloseCall**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall) 函式，服務提供者必須停止與呼叫控制碼相關的所有進一步處理，並使用錯誤值 LINEERR OPERATIONFAILED 來呼叫 [**非同步 \_ 完成**](/windows/win32/api/tspi/nc-tspi-async_completion) 回呼函數 \_ 。

 

 
