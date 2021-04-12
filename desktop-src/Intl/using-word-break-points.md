---
description: 當應用程式處理整個單字時，插入號的有效位置會以 SCRIPT LOGATTR 結構的 fWordStop 成員值標示 \_ 。 藉由呼叫 ScriptBreak 來取出此值。
ms.assetid: c9bbfb51-727a-45ff-8450-774bc106f9f7
title: 使用斷詞點
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b9cf68d5c90b6e93a6e6f15706ec357c7a33b23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195428"
---
# <a name="using-word-break-points"></a>使用斷詞點

當應用程式處理整個單字時，插入號的有效位置會以 [**SCRIPT \_ LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr)結構的 **fWordStop** 成員值標示。 藉由呼叫 [**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak)來取出此值。

單字之間的斷線有效位置會以 [**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak)所抓取的 **fSoftBreak** 值標示。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 



