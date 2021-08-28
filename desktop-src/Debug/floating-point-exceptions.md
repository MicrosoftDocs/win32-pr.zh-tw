---
description: 根據預設，系統會關閉所有 FP 例外狀況。
ms.assetid: efbea036-de9c-4f92-865a-494161da375e
title: 浮點例外狀況
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f2990929b712c65a09dcdae1e88d0a84b03d0f6d6cb3b6070fb3096ca998a10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691808"
---
# <a name="floating-point-exceptions"></a>浮點例外狀況

根據預設，系統會關閉所有 FP 例外狀況。 因此，計算結果會是 NAN 或無限大，而不是例外狀況。 在您可以使用結構化例外狀況處理來捕捉浮點數 (FP) 例外狀況之前，您必須呼叫[ \_ controlfp \_ ](/previous-versions/visualstudio/visual-studio-2010/c9676k6h(v=vs.100))的 C 執行時間程式庫函式，以開啟所有可能的 FP 例外狀況。 若只要攔截特定的例外狀況，請只使用對應至要攔截之例外狀況的旗標。 請注意，FP 錯誤的任何處理程式都應該呼叫[ \_ clearfp](/cpp/c-runtime-library/reference/clear87-clearfp?view=vs-2019)做為它的第一個 FP 指令。 此函式會清除浮點例外狀況。

 

 
