---
description: 找出錯誤的來源
ms.assetid: d7287cf1-9501-4d37-b022-b56c8008220c
title: 找出錯誤的來源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9b505981f12a6f8b23adc22e92cfc7b7c4b77b7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025991"
---
# <a name="finding-the-source-of-an-error"></a>找出錯誤的來源

您可以使用 COM + 和其他工具來診斷來源，並取得應用程式錯誤的描述。 如果您發現應用程式錯誤是由 COM + 所造成，您可以解讀 Winerror.h .h 檔案的錯誤訊息，或使用 Microsoft Visual C++ 錯誤公用程式。

如果您的伺服器應用程式失敗或造成非預期的行為，您必須先判斷發生錯誤的位置。 系統事件檢視器會追蹤應用程式、安全性和系統事件。 這裡會記錄許多「無訊息」錯誤。 不過，並非所有錯誤都會顯示在事件檢視器中。

您應該先參考事件檢視器中的應用程式記錄檔，檢查與事件訊息相關聯的應用程式。  (，因為您也可以封存事件記錄檔，所以您可以追蹤錯誤的事件歷程記錄。 ) 按兩下記錄檔中的專案，就會啟動 [ **事件** 內容] 頁面，以提供有關系統事件的進一步資訊。

For more information on debugging a COM+ application, see [Debugging COM+ Applications](debugging-com--applications.md).

## <a name="related-topics"></a>相關主題

<dl> <dt>

[錯誤隔離和 Failfast 原則](fault-isolation-and-failfast-policy.md)
</dt> <dt>

[COM + 如何修改傳回值](how-com--modifies-return-values.md)
</dt> <dt>

[解讀錯誤碼](interpreting-error-codes.md)
</dt> <dt>

[在 COM + 中處理錯誤的策略](strategies-for-handling-errors-in-com-.md)
</dt> <dt>

[疑難排解](troubleshooting-the-com--crm.md)
</dt> </dl>

 

 



