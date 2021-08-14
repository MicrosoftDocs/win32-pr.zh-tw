---
description: 撰寫元件最有問題的部分是處理可能的錯誤。
ms.assetid: 12f41eef-9953-4125-8490-07ff64967f95
title: 在 COM + 中處理錯誤
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04b66ecfd2d66d30b601fdc9e3e580d258ab912db5c10e3af422b9e7fde2b7a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118306547"
---
# <a name="handling-errors-in-com"></a>在 COM + 中處理錯誤

撰寫元件最有問題的部分是處理可能的錯誤。 在最佳情況下，嘗試判斷發生錯誤的原因，以及應採取的動作可能會很困難。 您的元件可能會檢查和處理的常見錯誤是失敗的網路連線、安全性錯誤，以及與無法連線之物件相關聯的失敗。

此外，您可以開發自己的錯誤碼來報告介面特定的錯誤，例如違反商務規則時。

為了保持 COM + 程式設計模型，物件可以 (，而且通常會) 呼叫其他物件上的介面方法來執行工作。 因為程式設計人員可以用不同的程式設計語言撰寫元件，所以 COM + 要求所有錯誤處理機制都必須是語言中立的，例如： Hresult 和 [**ErrorInfo**](errorinfo.md) 集合。

本節包含下表所述的主題，這些主題會討論在 COM + 應用程式中處理錯誤的技巧、COM + 中影響失敗行為的功能，以及診斷 COM + 錯誤的建議。



| 主題                                                                                           | 描述                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [在 COM + 中處理錯誤的策略](strategies-for-handling-errors-in-com-.md)<br/> | 列出並描述在 COM + 中處理錯誤的基本指導方針，包括使用 Hresult 和 [**ErrorInfo**](errorinfo.md) 集合的時機。<br/> |
| [COM + 如何修改傳回值](how-com--modifies-return-values.md)<br/>               | 識別 COM + 將標準 HRESULT 轉換回呼叫端之前，會將標準 HRESULT 轉換成 COM + 錯誤碼的單一條件。<br/>             |
| [錯誤隔離和 Failfast 原則](fault-isolation-and-failfast-policy.md)<br/>       | 顯示錯誤隔離和 failfast 原則如何影響 COM + 行為。<br/>                                                                          |
| [找出錯誤的來源](finding-the-source-of-an-error.md)<br/>                 | 說明如何診斷來源，以及取得應用程式錯誤的描述。 <br/>                                                       |
| [解讀錯誤碼](interpreting-error-codes.md)<br/>                             | 識別 Microsoft Visual C++、JAVA 語言和 Microsoft Visual Basic 的主流錯誤處理機制。 <br/>                    |
| [疑難排解](troubleshooting.md)<br/>                                               | 提供診斷錯誤的其他協助。<br/>                                                                                             |
| [聯絡支援](contacting-support.md)<br/>                                         | 識別在聯繫支援人員時應提供的重要問題解決資訊。<br/>                                                     |



 

如需處理與各種 COM + 服務相關聯之錯誤的詳細資訊，請參閱下列各節：

-   [藉由通知根物件來加速交易](speeding-transactions-by-notifying-the-root-object.md)
-   [處理](handling-errors-in-queued-components.md) 佇列元件的錯誤 () 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[偵錯工具 COM + 應用程式](debugging-com--applications.md)
</dt> </dl>

 

 




