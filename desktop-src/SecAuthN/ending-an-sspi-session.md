---
description: 當用戶端完成與任何伺服器的通訊，或使用傳遞至 AcquireCredentialsHandle 函式的其他認證完成時，用戶端必須呼叫 FreeCredentialsHandle 函數。
ms.assetid: fa943e9b-d379-441f-8c6e-f0a0f5f7f1a3
title: 結束 SSPI 會話
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4669d3143b480df20f1a5f1d76e73cc75802766d1db83da9b75d304e256ae4dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008266"
---
# <a name="ending-an-sspi-session"></a>結束 SSPI 會話

在用戶端和伺服器完成通訊之後，雙方都會以各自的內容控制碼呼叫 [**DeleteSecurityCoNtext**](/windows/desktop/api/Sspi/nf-sspi-deletesecuritycontext) 函式。 當用戶端完成與任何伺服器的通訊，或使用傳遞至 [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) 函式的其他認證完成時，用戶端必須呼叫 [**FreeCredentialsHandle**](/windows/desktop/api/Sspi/nf-sspi-freecredentialshandle) 函數。 當伺服器準備好要關閉並卸載 DLL 之前，伺服器必須呼叫 **DeleteSecurityCoNtext**。

 

 
