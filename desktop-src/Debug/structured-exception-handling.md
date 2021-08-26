---
description: 例外狀況是在程式執行期間所發生的事件，而且需要在正常控制流程之外執行程式碼。
ms.assetid: 6b6326d8-6875-4146-a4e3-7873f4e400cb
title: 結構化例外狀況處理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c07e3bce1c15120f5bba8f4423d96a32495dcdab0262957980f2b829ac0fa68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120059008"
---
# <a name="structured-exception-handling"></a>結構化例外狀況處理

*例外* 狀況是在程式執行期間所發生的事件，而且需要在正常控制流程之外執行程式碼。 有兩種例外狀況：硬體例外狀況和軟體例外狀況。 CPU 會起始 *硬體例外* 狀況。 這可能是因為執行特定的指令序列（例如零除或嘗試存取不正確記憶體位址）所導致。 *軟體例外* 狀況是由應用程式或作業系統明確起始。 例如，當指定了不正確參數值時，系統可以偵測到。

*結構化例外狀況處理* 是一種處理硬體和軟體例外狀況的機制。 因此，您的程式碼將會以相同的方式處理硬體和軟體例外狀況。 結構化例外狀況處理可讓您完全掌控例外狀況的處理、支援偵錯工具，並且可在所有程式設計語言和電腦上使用。 *向量化例外狀況處理* 是結構化例外狀況處理的延伸。

系統也支援 *終止處理*，可讓您確保每當執行受保護的程式碼主體時，也會執行指定的終止程式碼區塊。 無論控制流程離開受保護主體的方式為何，都會執行終止程式碼。 例如，終止處理常式可保證即使在執行受保護的程式碼主體時發生例外狀況或其他錯誤，也會執行清除工作。

-   [關於結構化例外狀況處理](about-structured-exception-handling.md)
-   [使用結構化例外狀況處理](using-structured-exception-handling.md)
-   [結構化例外狀況處理參考](structured-exception-handling-reference.md)

 

 



