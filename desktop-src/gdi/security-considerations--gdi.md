---
description: 本主題提供與 GDI 相關的安全性考慮資訊。 本主題不提供您需要瞭解的安全性問題。 相反地，請使用它作為此技術領域的起點和參考。
ms.assetid: 374e3ac7-f635-47f1-a72a-14e1be85c795
title: 安全性考慮： GDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71644da7d313e2efe0f287002c3e41a3a813a733
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944691"
---
# <a name="security-considerations-gdi"></a>安全性考慮： GDI

本主題提供與 GDI 相關的安全性考慮資訊。 本主題不提供您需要瞭解的安全性問題。 相反地，請使用它作為此技術領域的起點和參考。

GDI 通常有一些安全性考慮，因為它會處理顯示而非輸入。 不過，以下是您應該考慮的一些問題。

點陣圖、中繼檔和字型是複雜的結構，可能會損毀。 最好的作法是嘗試確保這些專案不會被破壞，而不是來自可信任的來源。

應用程式可以為某些列印和幕後處理 Api 指定安全描述項。 在設定安全描述項時，您應該要小心。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Microsoft 安全性中心](https://www.microsoft.com/security/)
</dt> <dt>

[安全性開發人員中心](https://technet.microsoft.com/security/)
</dt> <dt>

[資訊安全技術中心](https://technet.microsoft.com/security/default.aspx)
</dt> </dl>

 

 



