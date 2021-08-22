---
description: 若要釋放進程的符號處理常式所使用的所有記憶體，請使用 SymCleanup 函數。
ms.assetid: d442b2f2-9225-43fd-bd25-274322857834
title: 符號處理常式清除
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6db42f1fedfe68af4ab6eab885aefff0e8eb56e4ac9262f79adef8733f7ee7d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956957"
---
# <a name="symbol-handler-cleanup"></a>符號處理常式清除

若要釋放進程的符號處理常式所使用的所有記憶體，請使用 [**SymCleanup**](/windows/desktop/api/Dbghelp/nf-dbghelp-symcleanup) 函數。 此函式會列舉所有載入的模組、釋出每個模組，並釋出配置給模組清單的記憶體。 呼叫 **SymCleanup** 之後，您就無法在符號處理函式中使用進程控制碼，直到您呼叫 [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) 函式為止。

 

 



